---
title: Push notification setup for application developers
description: Learn developer settings for push notifications in Dynamics 365 Customer Insights - Journeys.
ms.date: 09/08/2023
ms.topic: article
author: alfergus
ms.author: alfergus
search.audienceType: 
  - admin
  - customizer
  - enduser
---

# Push notification setup for application developers

[!INCLUDE [consolidated-sku-rtm-only](./includes/consolidated-sku-rtm-only.md)]

To enable push notifications in Customer Insights - Journeys, you need to complete the following steps:

1. [App registration](real-time-marketing-push-notifications.md#create-a-mobile-app-configuration)
1. [Device registration](real-time-marketing-developer-push.md#implement-user-mapping)
1. [Receiving notifications and creating interactions](real-time-marketing-developer-notifications.md)

## Implement user mapping

In order for push notifications from a mobile application to work correctly, you will need to configure mapping from Dynamics 365 Customer Insights - Journeys customers to mobile application users. This ensures that the correct person (represented with the correct entity and record ID) receives the expected mobile push notification.

This step is not related to the mobile application setup (whether on Android or Apple devices), but rather, to the logical connection between the person represented as a Customer Insights - Journeys record and the counterpart record as a mobile application user.

First, to implement user mapping, the correct entity must be selected. This step is crucial because, in Customer Insights - Journeys, it's possible to orchestrate to multiple Microsoft Dataverse entities (such as a Contact or Lead), or to a Customer Insights - Data profile. Then, the correct record ID should be passed along to the mobile application and the mobile application should identify the user with that ID.

### User mapping example

As an example, if the Contact Dataverse entity is used and the email address field is used as the unique key for an end user as a Contact, one possibility to retrieve the correct ID using an OData GET call to Dataverse is the following:

```
https://<your Customer Insights - Journeys instance>.dynamics.com/api/data/v9.0/contacts?$filter=emailaddress1 eq 'andrew@contosoltd.com'
```

This query to Dataverse will return a single contact that has *andrew@contosoltd.com* as the email address. Once this ID is acquired (in this example, a Contact ID), it should be used as the UserId parameter in the mobile application.

There are more options available to implement this mapping and they depend on the needs and requirements of your scenario.

## Device registration

To complete the mobile app configuration, the developer must register devices. There are two ways to register a device:

1. **ServerToServer registration (recommended):**

    In this approach, the ApnsToken should be sent to your own server, which will then make a call to a Dynamics endpoint along with the ApiToken to complete the device registration. This is more secure as the ApiToken resides on your server and is less likely to get compromised.

1. **ApplicationToServer registration:**

    Whenever a new or updated token is received, it should be sent to Dynamics using a secured endpoint with the ApiToken.

    With this approach, once the configuration is complete, you must also implement the user mapping at runtime. This ensures that the correct person in the Customer Insights - Journeys app (represented as a Contact, Lead, or Customer Insights - Data profile) is mapped to the correct person using the mobile app on a particular device.

Select the tab that corresponds with your device's operating system:

# [iOS - API v.1](#tab/ios-v1)

To register a device running an iOS application, the following request should be issued:

Request URL:

```
POST
{PublicEndpoint}/api/v1.0/orgs/{OrganizationId}/pushchannel/apps/{ApplicationId}/devices/{UserId}
```

Request Body:

```
{
    "ApnsDeviceContract": {
        "ApnsToken": {ApnsToken}
    },
    "ApiToken": {ApiToken}
}
```

Parameters:

- **PublicEndpoint**: Taken from the "Public Endpoint" field of the mobile app configuration entity.
- **OrganizationId**: Taken from the "Organization ID" field of the mobile app configuration entity.
- **ApplicationId**: Taken from the "Application ID" field of the mobile app configuration entity.
- **UserId**: Identifier of the user in CRM. Can be a Contact ID, a Lead ID, or a Customer Insights - Data profile ID.
- **ApiToken**: Access token taken from the "Access Tokens" section of the mobile app configuration entity.
- **ApnsToken**: Device registration token. [Learn more about how to locate the token](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns).

#### Sample code to extract and save the device token

```
- (void)application:(UIApplication*)app didRegisterForRemoteNotificationsWithDeviceToken:(NSData*)devToken
{

// Parse token bytes to string
    const char *data = [devToken bytes];
    NSMutableString *token = [NSMutableString string];
    for (NSUInteger i = 0; i < [devToken length]; i++)
    {
        [token appendFormat:@"%02.2hhX", data[i]];
    }
    
// Print the token in the console
    NSLog(@"Push Notification Token: %@", [token copy]);
    [[NSUserDefaults standardUserDefaults] setObject:  [token copy] forKey:@"deviceToken"];
    [[NSUserDefaults standardUserDefaults]synchronize];
}
```

#### Sample code to register the device token with Dynamics 365

```
- (IBAction)registerDevice:(id)sender {
// organizationid - ID of the organization
// appId - ID of the application created in Dynamics UI in Application Registration
// profileId - ID of a contact in dynamics
// apiToken - API Token obtained in dynamics UI in Application Registration
// ApnsToken - DeviceToken fetched in step 1 above

// URL builder
    NSString *url = [NSString stringWithFormat: @"https://%@/api/v1.0/orgs/%@/pushchannel/apps/%@/devices/%@", [_endpoint text],[_organizationid text],[_appid text], [_profileid text]];
    
    NSMutableURLRequest *urlRequest = [[NSMutableURLRequest alloc] initWithURL:[NSURL URLWithString:url]];
    [[NSUserDefaults standardUserDefaults] setValue:[_organizationid text] forKey:@"organizationId2"];
    [[NSUserDefaults standardUserDefaults] setValue:[_endpoint text] forKey:@"endpoint2"];
    [[NSUserDefaults standardUserDefaults] synchronize];
    
// DeviceRegistrationContract for the request body
    NSString *userUpdate =[NSString stringWithFormat:@"{\"ApnsDeviceContract\":{\"ApnsToken\":\"%@\"},\"ApiToken\": \"%@\"}",[_devicetoken text],[_apitoken text]];

// Create the method "GET" or "POST"
    [urlRequest setHTTPMethod:@"POST"];
    [urlRequest setAllHTTPHeaderFields:@{@"content-type": @"application/json"}];

// Convert the string to data
    NSData *data1 = [userUpdate dataUsingEncoding:NSUTF8StringEncoding];

// Apply the data to the body
    [urlRequest setHTTPBody:data1];
    NSURLSession *session = [NSURLSession sharedSession];
    NSURLSessionDataTask *dataTask = [session dataTaskWithRequest:urlRequest completionHandler:^(NSData *data, NSURLResponse *response, NSError *error) {
        NSHTTPURLResponse *httpResponse = (NSHTTPURLResponse *)response;
        if(httpResponse.statusCode == 200)
        {
            NSLog(@"Login SUCCESS");
        
            dispatch_async(dispatch_get_main_queue(), ^{
                [self->_result setText:@"The device was successfully registered"];
            });
        }
        else
        {
            NSString *errorMessage = [NSString stringWithFormat: @"Error. Status code: %ld. Content: %@.", (long)httpResponse.statusCode, httpResponse.description];
            NSLog(@"Error");
            
            dispatch_async(dispatch_get_main_queue(), ^{
                [self->_result setText:errorMessage];
            });
        }
    }];
    [dataTask resume];
}
@end
```
# [iOS - API v.2](#tab/ios-v2)

1. Device Registration (single):

Request URL:

```
POST https://public-eur.mkt.dynamics.com/api/v1.0/orgs/%ORG_ID%/pushdeviceregistration/devices
```

Body:
```
{
    "MobileAppId": "%APP_ID%",
    "UserId": "%USER_ID%",
    "ApiToken": "%API_TOKEN",
    "ApnsDeviceToken": "%APNS_DEVICE_TOKEN%"
}
```
Headers:

- **x-ms-callback-url:** When not empty, failed or successful device registration will trigger POST request webhook.
- **x-ms-callback-url-headers:** Contains a serialized JSON of a string-to-string dictionary, representing headers passed for webhook requests. Used only when x-ms-callback-url is defined.

Returns: 202 on success, 400 if the request is not valid.

2. Device Registration (multiple):

```
POST https://public-eur.mkt.dynamics.com/api/v1.0/orgs/%ORG_ID%/pushdeviceregistration/devices/batch
```

Body: array of items equal to body from (1), up to 100 items

Headers: see **(1)**

Returns: 202 on success, 400 if the request is not valid

3. Device Registration Status Webhook (single): 

```
POST to URL provided within x-ms-status-callback-url header of (1) or (2) 
```

Body: 
```
{ 

    "Status": "Success|Failed", 
    "Signature": "%SIGNATURE%", 
    "FailureReason": " DuplicateExists|DryRunSendingFailed|DeviceTokenTooLong|FailedToStoreDevice|ApiTokenNotValid" 

} 
```

**Note #1**: Signature is HMACSHA256 hash of callback URL calculated using API token as a key. Can be used to verify that the call was indeed made by the CRM org the user owns. This can be done by hashing the callback URL with the API token on the webhook’s side, using the same algorithm, and comparing the values.

**Note #2:** Attempt to make a request will be made only once. Any failure to execute a request, such as an incorrect callback URL, REST API call timeout, or unexpected response status code will cause the notification to be lost. 

Expected Return: 200

Expected Body: Empty body


4. Device Cleanup (single):

```
POST https://public-eur.mkt.dynamics.com/api/v1.0/orgs/%ORG_ID%/pushdeviceregistration/devices/cleanup
```

Body:
```
{
    "MobileAppId": "%APP_ID%",
    "ApiToken": "%API_TOKEN%",
    "UserId": "%USER_ID%",
    "DeviceToken": "%OPTIONAL_FCM_OR_APNS_DEVICE_TOKEN% )"
}
```
Returns: 202 on success, 400 if the request is not valid

5. Device Cleanup (multiple):

```
POST https://public-eur.mkt.dynamics.com/api/v1.0/orgs/%ORG_ID%/pushdeviceregistration/devices/cleanup/batch
```

Body: array of items equal to body from (3), up to 100 items

Returns: 202 on success, 400 if the request is not valid


#### Sample code to extract and save the device token

```
func application(_ application: UIApplication, didRegisterForRemoteNotificationsWithDeviceToken deviceToken: Data) { 

        let tokenComponents = deviceToken.map { data in String(format: "%02.2hhx", data) } 

        let deviceTokenString = tokenComponents.joined() 

        UserDefaults.standard.set(deviceTokenString, forKey: "deviceToken") 

    } 

```

#### Sample code to register the device token with Dynamics 365 

```
@IBAction func registerDevice(_ sender: Any){ 

        let orgId = organizationid.text; 
        let endP = endpoint.text; 
        let apiToken = apitoken.text; 
        let appId = appid.text; 
        let profileId = profileid.text; 
        let url = URL(string: String(format:"https://%@/api/v1.0/orgs/%@/pushdeviceregistration/devices", endP ?? "", orgId ?? ""))!; 
        let session = URLSession.shared 

        // Create the URLRequest object using the url object 

        var request = URLRequest(url: url) 
        request.httpMethod = "POST" 

        // Add headers for the request 

        request.addValue("application/json", forHTTPHeaderField: "Content-Type") // change as per server requirements 
        request.addValue("application/json", forHTTPHeaderField: "Accept") 

        do { 

          // convert parameters to Data and assign dictionary to httpBody of request 

            let deviceToken = UserDefaults.standard.string(forKey: "deviceToken"); 
            let userUpdate = String(format:"{\"MobileAppId\":\"%@\",\"UserId\":\"%@\",\"ApnsDeviceToken\":\"%@\",\"ApiToken\": \"%@\"}", appId, profileId ,deviceToken, apiToken); 

            //Convert the String to Data 

            let data = (userUpdate as NSString).data(using: NSUTF8StringEncoding); 
            request.httpBody = data; 

        } catch let error { 

          print(error.localizedDescription) 
          return 

        } 

        // Create dataTask using the session object to send data to the server 

        let task = session.dataTask(with: request) { data, response, error in 

            if let error = error { 

                print("Post Request Error: \(error.localizedDescription)") 
            	 return 

            } 


            // ensure there is valid response code returned from this HTTP response 

            guard let httpResponse = response as? HTTPURLResponse, 

                (200...299).contains(httpResponse.statusCode) 

            else { 

                let httpRespose = response as? HTTPURLResponse; 
                print("Invalid Response received from the server. StatusCode: \(httpRespose?.statusCode) Error: \(httpRespose?.description)"); 
                return 

            } 

             

            print("Device Registration successful.") 

        } 

        // Resume the task 

        task.resume() 

    } 
```


# [Android - API v.1](#tab/android-v1)

To register a device for an Android application, the following request should be issued:

Request URL:

```
POST
{PublicEndpoint}/api/v1.0/orgs/{OrganizationId}/pushchannel/apps/{ApplicationId}/devices/{UserId}
```

Request Body:

```
{
    "FcmDeviceContract": {
        "FcmToken": {FcmToken}
    },
    "ApiToken": {ApiToken}
}
```

Parameters:

- **PublicEndpoint**: Taken from the "Public Endpoint" field of the mobile app configuration entity.
- **OrganizationId**: Taken from the "Organization ID" field of the mobile app configuration entity.
- **ApplicationId**: Taken from the "Application ID" field of the mobile app configuration entity.
- **UserId**: Identifier of the user in CRM. Can be a contact ID, a lead ID, or a Customer Insights - Data profile ID.
- **ApiToken**: Access token taken from the "Access Tokens" section of the mobile app configuration entity.
- **FcmToken**: Device registration token. [Learn more about how to locate the token.](https://firebase.google.com/docs/cloud-messaging/android/client#retrieve-the-current-registration-token)

##### Sample code to register the device token with Dynamics 365

```
public class DeviceRegistrationContract { 
    private static final String LOG_TAG = "DeviceRegistrationContract"; 
    private String mDeviceToken; 
    private String mApiToken; 
 
    public DeviceRegistrationContract(String deviceToken, String apiToken) { 
        this.setDeviceToken(deviceToken); 
        this.setApiToken(apiToken); 
    } 
 
    public String getDeviceToken() { 
        return mDeviceToken; 
    } 
 
    public void setDeviceToken(String deviceToken) { 
        this.mDeviceToken = deviceToken; 
    } 
 
    public String getApiToken() { 
        return mApiToken; 
    } 
 
    public void setApiToken(String apiToken) { 
        this.mApiToken = apiToken; 
    } 
 
    public String toJsonString() { 
        JSONObject jsonObject = new JSONObject(); 
        try { 
            JSONObject tokenObject = new JSONObject(); 
            tokenObject.put("FcmToken", mDeviceToken); 
            jsonObject.put("FcmDeviceContract", tokenObject); 
            jsonObject.put("ApiToken", mApiToken); 
        } catch (JSONException e) { 
            Log.d(LOG_TAG, "Json exception while creating device registration contract: " + e.getMessage()); 
        } 
 
        return jsonObject.toString(); 
    } 
}
```
# [Android - API v.2](#tab/android-v2)

1. Device Registration (single):

Request URL:
```
POST https://public-eur.mkt.dynamics.com/api/v1.0/orgs/%ORG_ID%/pushdeviceregistration/devices
```

Body:
```
{
    "MobileAppId": "%APP_ID%",
    "UserId": "%USER_ID%",
    "ApiToken": "%API_TOKEN",
    "FcmDeviceToken": "%FCM_DEVICE_TOKEN%",
}
```

Headers:

- **x-ms-callback-url:** When not empty, failed or successful device registration will trigger POST request webhook.
- **x-ms-callback-url-headers:** Contains a serialized JSON of a string-to-string dictionary, representing headers passed for webhook requests. Used only when x-ms-callback-url is defined.

Returns: 202 on success, 400 if request is not valid

2. Device Registration (multiple):
```
POST https://public-eur.mkt.dynamics.com/api/v1.0/orgs/%ORG_ID%/pushdeviceregistration/devices/batch
```

Body: array of items equal to body from (1), up to 100 items

Headers: see **(1)**

Returns: 202 on success, 400 if request is not valid

3. Device Registration Status Webhook (single): 

```
POST to URL provided within x-ms-status-callback-url header of (1) or (2) 
```

Body: 
```
{ 

    "Status": "Success|Failed", 
    "Signature": "%SIGNATURE%", 
    "FailureReason": " DuplicateExists|DryRunSendingFailed|DeviceTokenTooLong|FailedToStoreDevice|ApiTokenNotValid" 

} 
```

**Note #1**: Signature is HMACSHA256 hash of callback URL calculated using API token as a key. Can be used to verify that the call was indeed made by the CRM org the user owns. This can be done by hashing the callback URL with the API token on the webhook’s side, using the same algorithm, and comparing the values.

**Note #2:** Attempt to make a request will be made only once. Any failure to execute a request, such as an incorrect callback URL, REST API call timeout, or unexpected response status code will cause the notification to be lost. 

Expected Return: 200 

Expected Body: Empty body


4. Device Cleanup (single):
```
POST https://public-eur.mkt.dynamics.com/api/v1.0/orgs/%ORG_ID%/pushdeviceregistration/devices/cleanup
```

Body:
```
{
    "MobileAppId": "%APP_ID%",
    "ApiToken": "%API_TOKEN%",
    "UserId": "%USER_ID%",
    "DeviceToken": "%OPTIONAL_FCM_OR_APNS_DEVICE_TOKEN%)"
}
```

Returns: 202 on success, 400 if request is not valid

5. Device Cleanup (multiple):
```
POST https://public-eur.mkt.dynamics.com/api/v1.0/orgs/%ORG_ID%/pushdeviceregistration/devices/cleanup/batch
```

Body: array of items equal to body from (3), up to 100 items

Returns: 202 on success, 400 if request is not valid

#### Sample code to register the device token with Dynamics 365 

```
public String toJsonString() {  
        JSONObject jsonObject = new JSONObject();  
        try {  
            jsonObject.put("DeviceToken ", mDeviceToken);  
            jsonObject.put("ApiToken", mApiToken);  

            jsonObject.put("MobileAppId ", mMobileAppId);  
            jsonObject.put("UserId", mUserId); 
        } catch (JSONException e) {  
            Log.d(LOG_TAG, "Json exception while creating device registration contract: " + e.getMessage());  
        }  
  
        return jsonObject.toString();  
    } 
```

---

[!INCLUDE [footer-include](./includes/footer-banner.md)]
