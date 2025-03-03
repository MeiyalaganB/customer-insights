---
title: New and upcoming features
description: Information about new features, improvements, and bug fixes in Dynamics 365 Customer Insights - Journeys releases.
ms.date: 10/30/2023
ms.topic: article
author: alfergus
ms.author: alfergus
search.audienceType:
  - admin
  - customizer
  - enduser
---

# What's new in Dynamics 365 Customer Insights - Journeys

[!INCLUDE [consolidated-sku-rtm-only](./includes/consolidated-sku-rtm-only.md)]

[!INCLUDE [marketing-trial-cta](./includes/marketing-trial-cta.md)]

We're excited to announce our newest updates! This article summarizes early access features, preview features, general availability enhancements, monthly updates, and bug fixes. To see the long-term feature plans, take a look at the [Dynamics 365 and Power Platform release plans](/dynamics365/release-plans/).

Customer Insights - Journeys updates are [pushed to customers automatically](https://cloudblogs.microsoft.com/dynamics365/it/2020/04/27/automatic-update-policy-for-dynamics-365-marketing/). Solutions are available for early validations. To manually update your instances, follow the steps in [Keep Customer Insights - Journeys up to date](apply-updates.md).

To submit and vote on **feature requests** and **product suggestions**, go to the [Dynamics 365 Application Ideas portal](https://experience.dynamics.com/ideas/categories/?forum=dfa5b83d-9e4c-e811-a956-000d3a1bef07&forumName=Dynamics%20365%20Marketing).

## October 2023 update

### Version number

| App              | GA release      |
|------------------|-----------------|
| Customer Insights - Journeys        |   1.1.32267.98     |

On September 1, 2023, Dynamics 365 Customer Insights - Journeys transitioned to focus on real-time marketing features only. To support this transition, in early August 2023, provisioning of new instances changed in the following ways:

- New customers no longer receive the outbound marketing module. New customers need to contact support to add outbound marketing features.
- Existing customers see the same provisioning change but can add outbound marketing features themselves using a self-serve interface available on the **Settings** > **Versions page**.

 > [!div class="mx-imgBorder"]
 > ![New dynamics 365 customer insights org](media/real-time-marketing-transition-graphic.png "New dynamics 365 customer insights org")

### General availability

- **Get inspired and use Copilot to create engaging emails - globally available in seven languages**
    - Content ideas, a Copilot feature, is now available worldwide in the following languages: Danish, Dutch, English, French, German, Italian, Spanish. Harness the power of content ideas to effortlessly generate captivating emails within minutes simply by providing a few short key points and selecting a desired tone of voice. Additionally, now you can generate ideas with no input required thanks to relevant, pre-filled key points that match your selected email or email template.
    - [Release plan](/dynamics365/release-plan/2023wave2/marketing/dynamics365-marketing/content-ideas-journey-creator-english-all-geos)
    - [Docs](content-ideas.md)

- **Engage customers with text messages sent using Azure Communication Services**
    - Send text messages to customers using your Azure Communication Services SMS subscription, simplifying your operations by using Microsoft’s native SMS provider for all your products. Leverage all the real-time functionalities such as personalization, templates, and analytics, expanding the potential of your Azure Communication Services subscription.
    - [Release plan](/dynamics365/release-plan/2023wave2/marketing/dynamics365-marketing/engage-customers-text-messages-sent-using-azure-communication-services)
    - [Docs](real-time-marketing-outbound-text-messaging.md)

- **Increase engagement using alphanumeric SMS senders**
    - With alphanumeric senders, you can now send one-way text messages to your customers using a custom string of letters or numbers, making it easier for customers to recognize that messages are from a trusted source. By using your brand or company name, you gain brand awareness, increase trust, and ultimately boost the overall effectiveness of your SMS marketing efforts.
    - [Release plan](/dynamics365/release-plan/2023wave2/marketing/dynamics365-marketing/increase-engagement-using-alphanumeric-sms-senders)
    - [Docs](real-time-marketing-outbound-text-messaging.md) 

### Public preview

- **Improve communication timing by setting up quiet times**
    - Quiet time settings ensure that your messages are only sent when you want them to be delivered, increasing engagement and meeting customer expectations. It’s also more important than ever to meet compliance obligations by only contacting your customers when they want to be reached. With quiet times, you can easily prevent messages from being delivered during nights, weekends, or holidays. You can control quiet times separately for different channels and message types as well as create unique settings for each line of business.
    - [Release plan](/dynamics365/release-plan/2023wave2/marketing/dynamics365-marketing/prevent-messages-sending-during-unwanted-times-setting-up-quiet-times-using-copilot)
    - [Docs](real-time-marketing-quiet-times.md)

- **Create compelling content with Copilot image recommendations**
    - Visual content is critical to capturing your audience’s attention, increasing engagement with your brand, and conveying your message more effectively. However, browsing your library to find meaningful, relevant images for your content can be tedious and time-consuming. Now, a new Copilot assistant automatically identifies a selection of images from your library that best complement your content. Quickly and easily choose images that resonate with your audience without spending time searching.
    - [Release plan](/dynamics365/release-plan/2023wave2/marketing/dynamics365-marketing/create-compelling-content-copilot-image-recommendations)
    - [Docs](upload-images-files.md)

- **Refresh or perfect your messaging with Copilot text editing and rewriting**
    - Creating content that effectively captures your audience's attention is tedious, requiring time-consuming effort to perfect the language and tone of your message. Now, you can rapidly iterate on your content using Copilot to help optimize your messaging. Whether you're creating content for email, text messages, push notifications, or forms, using Copilot, you can easily rephrase messages, adjust the tone of voice, and shorten or lengthen copy, increasing productivity and delivering better results. The content rewrite copilot is currently available in the United States in English language.
    - [Release plan](/dynamics365/release-plan/2023wave2/marketing/dynamics365-marketing/rewrite-change-tone-content-quickly-using-copilot-marketing)
    - [Docs](content-rewrite.md)

- **Use journey copilot to create customer journeys by describing them in your own words**
    - With Dynamics 365 Customer Insights - Journeys, anybody can now create customer journeys in minutes, even when they may have never done it before. Simply describe, in everyday words, what you want to create and rely on Copilot generative AI to build the journey for you. This empowers you to do more with less. Instead of spending time getting the mechanics of the journey right, you can now ensure that you’re delivering the most personalized experience for your customers by collaborating with your entire team and quickly driving stakeholder alignment. Using journey Copilot together with the content ideas copilot assistant for email creation, you can now get your customer experience ideas to market in no time.
    - [Release plan](/dynamics365/release-plan/2023wave2/marketing/dynamics365-marketing/create-customer-journeys-describing-them-own-words-using-copilot)
    - [Docs](real-time-marketing-use-copilot-create-journey.md)

### Monthly enhancements

**Journeys**
- Allow editing of default journey time zone in real-time journeys-only organizations
    - Organizations that only use real-time journeys can now edit the default time zone used when creating journeys. The default time zone can either be a single time zone across the organization for consistency or it can be set to use the time zone of the user who creates the journey for convenience. To set the default journey time zone, go to **Settings** and open **Journey Settings** in the **Customer engagement** section.
- Enable orchestration of email interaction triggers (email bounced, link clicked, and email blocked)
- Marketers can get a visual preview of the journey generated by Copilot so that they can decide if they are happy with the output

**Email**
- Search through data in email delivery and interaction details
    - In real time journeys, you can now effortlessly search through data in email delivery and interaction details. Search by email enables you to quickly pinpoint specific information within your analytics, making it easier than ever to find the insights that matter most.

**Personalization**
- Communicate clearly and concisely with conditional lists (#if within #each), advanced scope
    - Conditional lists can now be created using conditions on multi-select pick list (for example, pick a specific building our of many)
- Build conditions using data that is related via 1-to-many and many-to-many relationships
    - Conditions now support using data that is reached via 1-to-many or many-to-many relationship. For example, check if billed service units (an attribute of "Case") exceed a threshold for a contact’s most recent case. Previously, such a condition could not be defined because a contact can have multiple cases.

**Admin settings**
- Check the Customer Insights Journeys version and update
    - In the installation management experience, you can now check the version installed for the Customer Insights - Journeys application and update it if a newer version is available.
- Easily enable or disable all AI copilot features using a global opt-in toggle
    - All copilot features can now be enabled at once using one, global toggle, which is turned on by default.
- Non-US users can agree or disagree for cross-geography data flow to use AI copilot features
    - As Azure AI services are currently available only in North America (and Switzerland), all non-US users need to agree allow cross-geography data flow to use Copilot features.

**Security roles**
- Use compliance profiles from any business units in messages and forms
    - The default security roles for business units users have been updated to give permission to all users across the organization to use any compliance profile in real-time journeys emails and forms. If you use these security roles directly, you may want to consider if your users should have this expanded security. If you've created your own user roles, you may want to consider making these changes to enable full access to compliance profiles across business units. Specifically, we've changed the “Marketing Professional (BU Level) - Business” and “Marketing Manager (BU Level) - Business” security roles to have organization level **Read**, **Append**, and **Append To** privileges on the **Compliance Profile, Purpose, Topic** and **Preference Center** tables.

### New blogs and scenario docs

Learn how to make the most of the new Dynamics 365 Marketing features in our latest blogs and scenario docs:
- [Transition from Outbound to Real-time Marketing Playbook](https://community.dynamics.com/blogs/post/?postid=1b4394d5-7764-4484-aba9-c7f972292c10) has been updated with the latest release information.
- [Understanding Consent Management in Dynamics 365 CI Journey](https://community.dynamics.com/blogs/post/?postid=8b2a4ee8-1069-ee11-a81c-000d3a7a1a66)

## September 2023 update

### Version number

| App              | GA release      |
|------------------|-----------------|
| Customer Insights - Journeys        |   1.1.30993.107     |

On September 1, 2023, Dynamics 365 Customer Insights - Journeys transitioned to focus on real-time marketing features only. To support this transition, in early August 2023, provisioning of new instances changed in the following ways:

- New customers no longer receive the outbound marketing module. New customers need to contact support to add outbound marketing features.
- Existing customers see the same provisioning change but can add outbound marketing features themselves using a self-serve interface available on the **Settings** > **Versions page**.

 > [!div class="mx-imgBorder"]
 > ![New dynamics 365 customer insights org](media/real-time-marketing-transition-graphic.png "New dynamics 365 customer insights org")

### General availability

- **Simplify and summarize segments using query assist Copilot functionality**
    - Updated Copilot-enhanced query assist streamlines your workflow and enables effective teamwork. Use query assist Copilot functionality in real-time marketing to create segments by describing them in plain English. Then, ensure your segment logic matches the intended outcome by translating the logic into a natural language description of the segment. Users who view or consume segments created by others can use the Copilot functionality to identify which audience the segment captures without needing to understand the segment creation logic. Query assist also offers suggested improvements during segment creation to help eliminate redundant conditional statements and further improve segment comprehension and performance.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/simplify-summarize-segments-using-query-assist-copilot-functionality)
    - [Docs](real-time-marketing-natural-language-segments.md)

- **Communicate effectively with personalized lists**
    - Lists are a common way to organize and communicate a repeated set of information such as a list of speakers or sessions for an event, list of items in an order, etc. Since lists can be quite information packed, ensuring only the relevant information is included is important (including what to include when a list item is missing some information). One way to personalize a list is to only include certain rows (for example, rather than listing all sessions of an event, only include online sessions). Another way is to annotate items that meet certain conditions, for example, indicate which sessions require additional registration or fee. Finally, there are times when you need to include additional information that is not in the data source of the list but in a related table. Now it's easier than ever to achieve such highly personalized and informative lists with enhanced capabilities to specify conditions at the list item level, include relevant information in related tables, control date/time format, and specify default values when a list item is empty.
    - [Docs](real-time-marketing-personalize-lists.md)

- **Engage customers with text messages sent using Vibes**
    - Connect your existing Vibes account to reach out to your customers through text messages. Use all Customer Insights - Journeys text message features with your Vibes account to maximize customer engagement. Leverage out-of-the-box functionalities such as personalization, templates, and analytics to unlock the potential of Vibes.
    - [Docs](real-time-marketing-outbound-text-messaging.md#sign-up-for-and-configure-a-vibes-account)

### Public preview

- **Easily style your emails with Copilot**
    - Jumpstart your email creation process with Copilot. Effortlessly style email elements including buttons, text, and more using AI to quickly interpret styles from a website and apply them to your email. Save valuable time so you can focus on crafting compelling content instead of picking colors and font sizes.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/easily-style-emails-copilot)
    - [Docs](email-theme.md)

- **Use Copilot to style your forms and event registration pages to match your website**
    - Build forms and event registration pages that perfectly match your website and brand guidelines within minutes. Leverage Copilot assistance to interpret your website and instantly apply the same styles, saving time designing your marketing or event registration forms. Copilot copies label fonts, input fields styles, colors, and buttons from your website. You can then review and refine elements to perfectly match your brand guidelines.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/use-copilot-style-forms-event-registration-pages-match-website)
    - [Docs](real-time-marketing-manage-forms.md#style-your-forms-using-theme)

- **Automatically prevent duplicate emails to contacts that share the same email address**
    - Effective email management is crucial for maintaining strong customer relationships and ensuring your business's success. By enabling email deduplication, you can ensure that your message is sent only once, even when multiple contacts share the same email address. This helps keep your customers’ inboxes clutter-free, increases the chance that important messages avoiding the dreaded spam folder, and preserves your brand reputation.  
    - [Release plan](/dynamics365/release-plan/2023wave2/marketing/dynamics365-marketing/prevent-duplicate-emails-contacts-that-share-email-address)
    - [Docs](email-deduplication.md)

- **Increase engagement using alphanumeric SMS senders**
    - With alphanumeric senders, you can now send one-way text messages to your customers using a custom string of letters or numbers, making it easier for customers to recognize that messages are from a trusted source. By using your brand or company name, you gain brand awareness, increase trust, and boost the overall effectiveness of your SMS marketing efforts.
    - [Release plan](/dynamics365/release-plan/2023wave2/marketing/dynamics365-marketing/increase-engagement-using-alphanumeric-sms-senders)
    - [Docs](real-time-marketing-outbound-text-messaging.md#add-a-sender-number-from-an-infobip-link-mobility-telesign-twilio-or-vibes-account-worldwide)

### Monthly enhancements

- **Analytics: Optimize email marketing efforts with enhanced email insights**
    - With the introduction of key performance indicators such as email Open Rate, Click Rate, and Delivery Rate in email insights, you can get a deeper understanding of your email campaign effectiveness. Moreover, in delivery and interaction details, you can now export up to 50,000 records of interaction data, as well as view the people that interacted with your email messages.
- **Journeys: Make updates to your journey by describing them in conversational language with journey Copilot**
    - In this release, we’ve made it easier for marketers to make small changes to their journeys by describing them in their own words. For example, you want first create a journey that sends emails to your loyalty members about an upcoming sale, then later want to address a more specific audience like customers who have a birthday this month. You can make this change by simply asking Copilot to switch out the audience.
- **Journeys: Create leads and opportunities from journeys**
    - For businesses that use leads and opportunities to track sales activity, they are a crucial output of the marketing process. Now you can create leads and opportunities directly within customer journeys, giving you the control to create the right leads and opportunities at the right point in your customer’s experience.
- **Personalization: Performance improvements for journeys using audience entities with many custom attributes**
    - The personalization layer now loads only the needed set of columns (instead of the entire entity) for audience entities (contact, lead, or profile) during journey execution. This reduces execution time significantly (and drives much higher journey throughput) for customers who have added a large number of custom attributes to their audience entities.
- **Email: Subject line and preview text limit is increased from 500 characters to 4000 characters**
- **Consent: Create segments from consent topics and purposes**
    - Use the consent captured from your customers to create segments that target people who have opted into receiving specific types of communications. Segments now support creating segments from topic and purpose contact point consent records, so that you can get accurate segment sizes and don’t include people who would not receive your messages. For example, create a segment that only includes contacts that have opted in to receive your "Monthly Newsletter" topic. Or create a segment that only includes leads who have not opted out of receiving commercial messages.
- **Consent: Capture and share consent across multiple lines of business by sharing consent purposes**
    - Multi-brand compliance profiles enable you to build trust in your multiple brand(s) by giving your customers control over their communication preferences tailored to each line of business. With the added ability to create new consent purposes and share those purposes across compliance profiles, you can now use the same consent captured from one profile in other profiles and their preference centers. This enables you to capture consent for a parent brand and then share that consent with each of the child brands in your organization.
- **Consent: Preference center and consent support for custom channels**
    - Preference centers in real-time journeys now support custom channels for purpose and topic-based consent. Custom channel messages can set a preference center compliance profile, purpose, and (optional) topic and real-time journeys will respect the contact point consent for those messages. Messages sent to custom channels follow the same consent enforcement rules as SMS messages.

### New blogs and scenario docs

Learn how to make the most of the new Dynamics 365 Marketing features in our latest blogs and scenario docs:

- [Microsoft is named a Leader in 2023 Gartner® Magic Quadrant™ for B2B Marketing Automation Platform - Microsoft Dynamics 365 Blog](https://cloudblogs.microsoft.com/dynamics365/bdm/2023/09/25/microsoft-is-named-a-leader-in-2023-gartner-magic-quadrant-for-b2b-marketing-automation-platform/)
- [Microsoft Dynamics 365 Copilot is helping transform customer experiences - Microsoft Dynamics 365 Blog](https://cloudblogs.microsoft.com/dynamics365/bdm/2023/09/07/from-microsoft-to-global-brands-dynamics-365-copilot-is-helping-transform-customer-experiences-across-service-sales-and-marketing/) 
- [Transition to real-time marketing and transform your Customer Experience - Microsoft Dynamics 365 Blogs](https://cloudblogs.microsoft.com/dynamics365/it/2023/07/18/transition-to-real-time-marketing-and-transform-your-customer-experience/)
- [Dynamics 365 Customer Insights - Journeys ALM Best Practices: Getting Started - Dynamics FastTrack Blogs](https://community.dynamics.com/blogs/post/?postid=ed18eefc-a046-ee11-be6d-00224827ed7b)
- [Throttling Email Messages with Dynamics 365 Customer Insights Journeys - Dynamics FastTrack Blogs](https://community.dynamics.com/blogs/post/?postid=0e2a9bb2-7f4e-ee11-a81c-000d3ae68975)
- [Double Opt-In in Real-Time Marketing  - Dynamics FastTrack Blogs](https://community.dynamics.com/blogs/post/?postid=24df8cbc-5724-4734-b898-24cfe57d3c33)

## August 2023 update

### Version number

| App              | GA release      |
|------------------|-----------------|
| Customer Insights - Journeys        |   1.1.28488.146     |

On September 1, 2023, Dynamics 365 Customer Insights - Journeys will transition to focus on real-time marketing features only. To support this transition, in early August 2023, provisioning of new instances will change in the following ways:

- New customers will no longer receive the outbound marketing module. They will need to contact support to add outbound marketing features.
- Existing customers will also see the same provisioning change but will be able to add outbound marketing features themselves using a self-serve interface available on the **Settings** > **Versions page**.

 > [!div class="mx-imgBorder"]
 > ![New dynamics 365 customer insights org](media/real-time-marketing-transition-graphic.png "New dynamics 365 customer insights org")

### General availability

- **Prioritize best leads and empower sellers with new lead scoring builder**
    - To maximize return on investment from marketing activities, it is essential to identify the best prospects at the right moment when they're ready to engage with your sales team. With Customer Insights - Journeys, you can use a new simple but powerful lead scoring builder to define your scoring criteria and model more efficiently. Prioritize the most engaged leads from companies that match your ideal customer profile using engagement and profile-based scoring. With proper scoring, you can identify the best leads and empower the sales team to spend more time winning deals and less time chasing lukewarm opportunities.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/prioritize-best-leads-empower-sellers-new-lead-scoring-builder)
    - [Docs](real-time-marketing-create-lead-scoring-model.md)

- **Further personalize journeys using custom events with entity references**
    - Entity references for custom triggers enable greater personalization of messages sent to customers. Create entity references for custom events instead of adding multiple attributes manually, bypassing the previous limit of 30 attributes. For example, if you want to create a custom trigger that triggers a journey for all customers who purchased a specific product on your website, you can now capture the purchase event and the contents related to the SKU that was purchased. Instead of manually entering all attributes (with a maximum limit of 30) for the custom trigger, you can now add an entity reference to select as part of the custom trigger attribute definition.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/further-personalize-journeys-using-custom-events-entity-references)
    - [Docs](real-time-marketing-custom-triggers.md#1-initial-trigger-creation)

### Public preview

- **Use journey Copilot to create customer journeys by describing them in your own words**
    - With Dynamics 365 Customer Insights - Journeys, anybody can now create customer journeys in minutes, even when they may have never done it before. Simply describe, in everyday words, what you want to create and rely on Copilot generative AI to build the journey for you. This empowers you to do more with less. Instead of spending time getting the mechanics of the journey right, you can now ensure that you’re delivering the most personalized experience for your customers by collaborating with your entire team and quickly driving stakeholder alignment. Using journey Copilot together with the content ideas copilot assistant for email creation, you can now get your customer experience ideas to market in no time.
    - [Release plan](/dynamics365/release-plan/2023wave2/marketing/dynamics365-marketing/create-customer-journeys-describing-them-own-words-using-copilot)
    - [Docs](real-time-marketing-use-copilot-create-journey.md)

### New blogs and scenario docs

Learn how to make the most of the new Dynamics 365 Customer Insights - Journeys features in our latest blogs and scenario docs:

- [Transition to Customer Insights - Journeys and transform your Customer Experience - Microsoft Dynamics 365 Blog](https://cloudblogs.microsoft.com/dynamics365/it/2023/07/18/transition-to-real-time-marketing-and-transform-your-customer-experience/)
- [Push notification enhancements - Dynamics FastTrack Blogs](https://community.dynamics.com/blogs/post/?postid=7b7bfa64-e730-ee11-bdf3-000d3a4ef41d)

## July 2023 update

### Version number

| App              | GA release      |
|------------------|-----------------|
| Customer Insights - Journeys        |  1.1.26671.175      |

> [!IMPORTANT]
> With the July 2023 release, customer consent data began migration to utilize the new multi-brand consent features. For some Customer Insights - Journeys users, the migration changed the settings that control whether tracking links are included in messages. The changes may prevent tracking in messages if customers have not given explicit consent. After the migration, if you want to enable tracking links in messages for customers who have not provided tracking consent, [update the **Tracking purpose** enforcement model](real-time-marketing-email-text-consent.md#consent-enforcement-diagram) of your **Compliance Profile(s)** to "Non-restrictive." This enables tracking links to be substituted in emails as long as the receiver has not explicitly opted out of tracking.

> [!TIP]
> Starting in July 2023, custom workflows can no longer *read* from the **msdynmkt_contactpointconsent2** or **msdynmkt_contactpointconsent3** consent tables. To ensure continued functionality, you must update custom workflows to read from the latest **msdynmkt_contactpointconsent4** table.
>
> Custom workflows that *write* to the **msdynmkt_contactpointconsent2** or **msdynmkt_contactpointconsent3** consent tables will automatically have data synced to the latest **msdynmkt_contactpointconsent4** table with some delay (potentially 24 hours or longer). If your workflows depend on data being available sooner than that, you should update your workflows to *write* to the **msdynmkt_contactpointconsent4** table. The data sync will continue until June 1, 2024, at which time you'll need to have moved all workflows that write contact point consent records to target the **msdynmkt_contactpointconsent4** table.
>
> Additionally, as of June 2023, the **Consent Type** field is mandatory for the **msdynmkt_contactpointconsent4** entity. To ensure continued functionality of custom workflows, update the workflows to include this mandatory field.

### General availability

- **Make your push notifications more engaging by adding images**
    - Orchestrate beautiful, personalized push notifications with images to increase customer engagement. Add product images, promotional graphics, brand logos, or appealing illustrations to your push notifications to make them more informative and persuasive. New, eye-catching push notifications lead to higher user engagement and better campaign results.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/make-push-notifications-more-engaging-adding-images)
    - [Docs](real-time-marketing-push-notifications.md)

- **Easily set up your push notifications and engage customers worldwide**
    - We’ve streamlined the configuration process for push notifications with an enhanced, guided experience. It's now easier to set up the push notification channel and incorporate it into your marketing mix, reducing the time and effort required for implementation. Additionally, push notifications are now available worldwide, so you can engage customers across the globe, expand your market presence, and drive growth.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/easily-set-up-push-notifications-engage-customers-worldwide)
    - [Docs](real-time-marketing-developer-push.md)

- **Easily import outbound emails, content blocks, and templates to Customer Insights - Journeys**
    - Save time and resources, reuse and adapt your existing outbound assets to create engaging and relevant Customer Insights - Journeys experiences. Easily import your outbound marketing emails, templates, and content blocks into Customer Insights - Journeys to plug them into your real-time journeys.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/import-outbound-marketing-emails-templates-real-time-marketing)
    - [Docs](real-time-marketing-import-email-to-real-time.md)

- **Match your business needs with multi-brand consent and customizable preference centers**
    - In Customer Insights - Journeys, marketers can now fully customize out-of-the-box preference centers to better represent their brands and meet their business needs. Create separate preference centers per brand, allowing you to independently capture and manage consent for multiple lines of business. Keep your customers engaged by giving them control over the channels they want to connect to while ensuring that you capture the consent you need to satisfy legal and regulatory requirements.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/match-business-needs-more-granular-customizable-consent-preference-centers)
    - [Docs](compliance-overview.md)

- **Tailor communications to the topics customers want to receive**
    - Improve customer engagement and reduce unsubscriptions by giving customers granular control over the Customer Insights - Journeys messages they receive. Target your messages to the audience that wants to engage with your content the most by capturing detailed consent. Easily configure topics for messages, enabling per-topic customer opt-in or opt-out. Allow customers to subscribe to the topics that matter to them while capturing the consent you need to satisfy legal and regulatory requirements. Avoid embarrassing and costly configuration mistakes by leveraging Customer Insights - Journeys topic support, preventing the complications of maintaining and enforcing lists of subscribed customers, all while taking advantage of enhanced Customer Insights - Journeys preference centers that better represent your brand. 
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/tailor-communications-topics-customers-want-receive)
    - [Docs](real-time-marketing-email-text-consent.md)

- **Plan events with intuitive event registration form**
    - Easily plan events in Customer Insights - Journeys that drive high attendance, convert customers, and meet your business goals. Events are a critical part of marketing. With the updated event planning features based on new, intuitive registration forms, creating, and managing events is a breeze. Event planning’s tight integration with Customer Insights - Journeys makes it easier than ever to guide attendees to the next step in their journey.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/easily-plan-events-intuitive-event-registration-form-experience)
    - [Docs](set-up-event.md)

- **Confidently send emails after previewing trigger-based personalization**
    - Personalizing content is an effective strategy for boosting engagement but ensuring such personalized content is accurate for a variety of recipients can be a challenging task. We made this task easier in April 2023 release that added support for previewing emails using data from a selected audience record. This release extends this capability to include support for triggers. Now any personalization that uses data from any out of the box triggers can also be tested easily. Additionally, you can now enter values manually for selected personalization that override data from audience or trigger for easily testing edge cases.
    - [Docs](real-time-marketing-email.md#preview-and-test-send-your-email)

- **Easily include QR codes for event registration, link, page, or any custom text**
    - QR codes are widely used to share information that is easily actionable on mobile devices with just a simple scan. They are an effective tool for promoting and increasing engagement for various purposes like events, web pages, coupons, and more. The email designer already includes a feature that allows easy insertion of QR codes for commonly used targets such as events, URLs, surveys, and file downloads. Now, we've added two additional targets. The "Event registration code" target fills a gap in real-time functionality by supporting QR codes for event registration pages along with the registration code needed for check-in. The "Text" option enables you to generate a QR code for any text you type in. Additionally, you can make the QR code dynamic by using personalized data like discount codes or loyalty program membership numbers.
    - [Docs](email-design.md)

### Public preview

- **Scale your business with confidence with 300M maximum monthly interactions**
    - Reach up to 100 million contacts or leads and send up to 300 million messages per month with Dynamics 365 Customer Insights - Journeys customer journey orchestration. This added capacity empowers you to deliver personalized experiences at scale and delight customers in new ways. Additional interactions will help you grow your business, whether you’re increasing your customer base in new markets, reaching additional geographies, promoting new products, or expanding your prospective customer pipeline to reach higher sales targets.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/scale-business-confidence-300m-maximum-monthly-interactions)
    - [Docs](fair-use-policy.md)

### Monthly enhancements

- **Customizable form entity**
- **Create composite segments**
- **Subscriptions list support for load consent**

### New blogs and scenario docs
Learn how to make the most of the new Dynamics 365 Customer Insights - Journeys features in our latest blogs and scenario docs:

- [Revolutionize marketing with query assist and content ideas - Microsoft Dynamics 365 Blog](https://cloudblogs.microsoft.com/dynamics365/bdm/2023/06/21/copilot-in-dynamics-365-marketing-revolutionizes-marketing-with-query-assist-and-content-ideas/)

## June 2023 update

General availability features include improved copilot assistance for the query assist segmentation builder, enhancements to the asset and templates libraries, and business unit domain support for emails.

Public preview features include tailoring communications to improve customer engagement.

### Version number

| App              | GA release      |
|------------------|-----------------|
| Customer Insights - Journeys        |  1.1.25335.62    |

### General availability

- **Create better targeted segments using everyday language that include behavioral interactions with query assist, a copilot feature**
    - Marketers are now able to quickly build targeted segments using conversational everyday language that includes customer interactions with your marketing messages, websites, events, and other channels. With these updates, you can create complex segments that not only focus on demographic or firmographic data but also marketing behavioral data without requiring deep knowledge of the back-end data model.
    - [Docs](nl-segment-build.md)

- **Easily tag and update assets with an enhanced experience**
    - Swiftly manage and customize your assets. Need to rename, tag, or update assets? Now, it's just a matter of a few clicks. Our enhanced design ensures a visually appealing workspace, while the right-side pane provides quick previews of your files. Take control with editable property panes, allowing you to customize assets effortlessly. The new tagging controls simplifies file organization, enabling efficient categorization and effortless searching.
    - [Docs](upload-images-files.md)

- **Assign specific business units to your authenticated domains**
    - When modernized business units are turned on, and business unit scoping is enabled, the domain authentication wizard allows users to specify what business unit they want their domain to be authenticated. When a business unit is selected for a domain, this domain is solely available for that business unit unless you want to make it shareable across your organization.
    - [Docs](domain-authentication.md#domain-authentication-for-modernized-business-units)

### Public preview

- **Tailor communications to the topics customers want to receive**
    - Improve customer engagement and reduce unsubscriptions by giving customers granular control over the Customer Insights - Journeys messages they receive. Target your messages to the audience that wants to engage with your content the most by capturing detailed consent.  Allow customers to subscribe to the topics that matter to them while capturing the consent you need to satisfy legal and regulatory requirements. Avoid embarrassing and costly configuration mistakes by leveraging Customer Insights - Journeys topic support, preventing the complications of maintaining and enforcing lists of subscribed customers, all while taking advantage of enhanced Customer Insights - Journeys preference centers that better represent your brand.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/tailor-communications-topics-customers-want-receive)
    - [Docs](real-time-marketing-compliance-settings.md#topics)

### Monthly enhancements

- **Achieve more accurate results in your A/B tests by specifying a control group**
    - With the new control group features, marketers can now specify how many people to test a message on before releasing the remaining audience to the winning version. This update gives you more control over the testing process and helps ensure accurate results.

### New blogs and scenario docs

Learn how to make the most of the new Dynamics 365 Customer Insights - Journeys features in our latest blogs and scenario docs:
- [Create dynamic content for multiple countries and languages](real-time-marketing-dynamic-content-multiple-languages.md)
- [Identify and resolve errors with real-time customer care journeys - Scenario docs](real-time-marketing-customer-care-journey.md)
- [Deliver personalized customer experiences with Copilot in Dynamics 365 Customer Insights - Journeys and Customer Insights - Microsoft Dynamics 365 Blog](https://cloudblogs.microsoft.com/dynamics365/bdm/2023/03/14/deliver-personalized-customer-experiences-with-copilot-in-dynamics-365-marketing-and-customer-insights/)

## May 2023 update

The May 2023 release general availability features include the availability of interaction data in the segment builder, the ability to move custom triggers between environments, journey reminders, lead insights, and the ability to surface the next best action for leads with your sales team.

Public preview features include AI-powered milestone attribution analysis, multi-brand consent and customizable preference centers. We also continue to improve the content ideas and query assist Copilot features.

### Version number

| App              | GA release      |
|------------------|-----------------|
| Customer Insights - Journeys        |  1.1.24040.75    |

### General availability

- **Use interaction data to improve targeting in the redesigned segment builder**
    - Segments are critical for targeting the right customers and personalizing their experience. The redesigned Customer Insights - Journeys segment builder allows you to create segments based on customer interactions and engagement with your marketing messages, websites, events, or other channels. Combined with the demographic and firmographic attributes already available for segmentation, the segment builder enables you to reach the right customers at the right time. You can then use these segments for targeting, journey branching or content variants to personalize the experience for each customer.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/leverage-interaction-data-improve-targeting-using-re-designed-segmentation-builder)
    - [Docs](real-time-marketing-redesigned-segment-builder.md)

- **Save time by easily moving triggers between environments**
    - With Dynamics 365 Customer Insights - Journeys, you can create custom triggers in development or pre-production environments to securely test the intended behavior before you use them in production for live marketing journeys and campaigns. You can then move the triggers to a production environment using Power Platform Solutions in any state. The ability to move published triggers enables you to align your testing workflow with your application lifecycle management process. Dynamics 365 Customer Insights - Journeys automatically takes care of packaging the triggers and any related metadata when you export and import the solutions.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/save-time-easily-moving-triggers-between-environments)
    - [Docs](move-triggers-between-environments.md)

- **Boost your productivity with enhanced journey reminders**
    - You can now create journeys that nudge and remind a customer to take a required action, such as completing an application/survey, filling a health check, checking out their cart, and more. You can remind customers until they complete the call to action or until a certain date or time. Additionally, you can bypass certain journey steps when a customer action makes them irrelevant. For instance, if you’re welcoming/onboarding the customer to a product or service through daily messages, but they complete the onboarding before all the messages have been sent – you can skip the remaining messages by exiting the customer from that block. This simplifies not only the journey logic required to capture the whole scenario in a single journey, but also makes a single block of journey actions (such as a series of reminders) easy to analyze and optimize.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/boost-productivity-enhanced-journey-reminders)
    - [Docs](real-time-marketing-enhanced-journey-reminders.md)

- **Customize marketing strategies based on Lead insights**
    - Access Lead-specific insights in Customer Insights - Journeys and tailor your marketing experiences according to your Leads’ behavior. Lead insights provide a holistic view of each Lead's interactions with your marketing activities. This includes access to journey engagement history, encompassing past email sends, opens, clicks, form submissions, and other relevant data.
    - [Docs](real-time-marketing-analytics.md)

- **Surface the next best action to your sales team when a lead engages with Customer Insights - Journeys**
    - As you nurture leads and opportunities with real-time journeys, the lead's signals might indicate an urgency to engage with your sales teams. With Dynamics 365 Customer Insights - Journeys, you can now create sales activities such as tasks and phone calls directly from journeys so that leads get individualized attention when they’re most likely to engage. You can also activate a sales sequence to accelerate a deal, ensuring that sellers receive automated recommendations based on the sales playbook associated with the campaign.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/optimize-lead-management-process-engaging-sellers-right-away)
    - [Docs](real-time-marketing-optimize-lead-management.md)

### Public preview

- **Easily discover and use content ideas Copilot to create highly engaging emails**
    - With this enhancement you can easily start using Copilot to generate email content thanks to prefilled key points matching your selected topic, and by accessing it directly within your email flow.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/easily-create-engaging-content-using-ai-powered-content-ideas)
    - [Docs](content-ideas.md)

- **Understand how marketing activities contribute to defined milestones using AI**
    - Dynamics 365 Customer Insights - Journeys enables you to create highly personalized experiences to nudge customers toward important milestones in the buyer's journey such as completing a purchase, becoming a loyalty program member, or becoming a qualified sales opportunity. Now, you can define such milestones and measure them over time. You can then optimize your marketing mix using AI or rules-based attribution which quantifies the contribution of your journeys, channels, and messages in driving customers to complete those milestones.
    > [!NOTE]
    > This feature will be gradually rolled out during the month and may have delayed availability compared to the other May releases.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/understand-how-marketing-activities-contribute-defined-milestones)
    - [Docs](real-time-marketing-effectiveness.md)

- **Match your business needs with multi-brand consent and customizable preference centers**
    - In Customer Insights - Journeys, marketers can now fully customize out-of-the-box preference centers to better represent their brands and meet their business needs. Create separate preference centers per brand, allowing you to independently capture and manage consent for multiple lines of business. Keep your customers engaged by giving them control over the channels they want to connect to while ensuring that you capture the consent you need to satisfy legal and regulatory requirements.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/match-business-needs-more-granular-customizable-consent-preference-centers)
    - [Docs](compliance-overview.md)

### Monthly enhancements

- **Attribute branch supports complex conditions that can span multiple entity relationships**
    - Access attributes of entities related to a Contact or Lead, even if those entities are several hops away. For example, you can hop from the contact to the name of the account associated with that contact, making it easier to create more powerful and complex conditions.

- **Expanded audience insights: view text messages and push notifications engagement**
    - Now, in addition to email and form interactions, you can also access comprehensive insights for text messages, push notifications, and custom channels in Customer Insights - Journeys contact and lead insights. Get a holistic view of how your audience engages with all your marketing channels, make data-driven decisions, and optimize your strategies for even better results.

- **Clearly communicate dates and times in formats that match expectations of your audience**
    - Different parts of the world use different formats for date and time, so it is critical to use the right format your audience expects to avoid confusion. We are expanding available time formats to add 12-hour formats in certain languages/countries where they officially follow 24-hour format but in practice also use 12-hour format (for example, English (UK)). We also added recently used formats at the top. Not only does this save time, it also makes it easy to pick a single consistent format across the message.
    - [Docs](real-time-marketing-predefined-dynamic-text.md#communicate-dates-and-times-in-various-formats)

- **Create segments effortlessly using everyday language with the improved query assist experience**
    - The new query assist experience is designed to help marketers seamlessly switch between query assist and manual mode giving you more control over the segment creation process. We've also improved the feature ensures a more intuitive experience. With these updates, you can build segments using everyday language to target the right audience without requiring deep knowledge on the back-end data model.
    - [Docs](compliance-overview.md)

- **Create segments using Customer Insights - Journeys Lists and other entities that are related to Contacts/Leads with many:many relationships**
    - You can now create segments with data tables, such as Customer Insights - Journeys Lists, that have N:N relationships with target entities like Leads and Contacts.

### New blogs and scenario docs

Learn how to make the most of the new Dynamics 365 Customer Insights - Journeys features in our latest blogs and scenario docs:
- [Identify and resolve errors with real-time customer care journeys - Scenario docs](real-time-marketing-customer-care-journey.md)
- [Deliver personalized customer experiences with Copilot in Dynamics 365 Customer Insights - Journeys and Customer Insights - Microsoft Dynamics 365 Blog](https://cloudblogs.microsoft.com/dynamics365/bdm/2023/03/14/deliver-personalized-customer-experiences-with-copilot-in-dynamics-365-marketing-and-customer-insights/)
- [Use generative AI to drive customer engagement with 2023 release wave 1 for Dynamics 365 Customer Insights - Journeys and Customer Insights](https://cloudblogs.microsoft.com/dynamics365/bdm/2023/04/19/use-generative-ai-to-drive-customer-engagement-with-2023-release-wave-1-for-dynamics-365-marketing-and-customer-insights/)
- [Drive customer engagement with 2023 release wave 1 - Microsoft Dynamics 365 Blog](https://cloudblogs.microsoft.com/dynamics365/bdm/2023/04/19/use-generative-ai-to-drive-customer-engagement-with-2023-release-wave-1-for-dynamics-365-marketing-and-customer-insights/)

## April 2023 update

The April release marks the availability of many [2023 release wave 1](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/planned-features) features. General availability features include a simplified email editor, new email templates, send now email functionality, modernized forms for Customer Insights - Journeys, extending recipient lists with carbon copies, message frequency limits, UTM tagging, contact insights for Customer Insights - Journeys, one-to-many relationships for personalization, sample audience data for email previews, business units for Customer Insights - Journeys, and the ability to change your organization URL in the Power Platform Admin Center.

Monthly enhancements include tracking of unique opens and clicks, attachment support for custom channels, and extended regional availability for query assist.

> [!IMPORTANT]
> An earlier version of this article incorrectly announced the availability of the enhanced journey reminders preview in the April release. Enhanced journey reminders are *not* included in the April release.

### Version number

| App              | GA release      |
|------------------|-----------------|
| Customer Insights - Journeys        |  1.1.10512.27    |

### General availability

- **Create beautiful and engaging emails with ease**
    - The simplified email editor allows you to create engaging content within minutes, whether you are an experienced marketer or create emails occasionally to engage with your customers. Now, you can make basic content modifications and even add new elements and sections directly on canvas, and thus enjoy easy, delightful, and focused experience.
    - [Docs](real-time-marketing-email-get-started.md)

    > [!div class="mx-imgBorder"]
    > ![Screenshot showing the new email editor.](media/whats-new-easy-email.png "Screenshot showing the new email editor")

- **Easily find and select one of many new templates to create beautiful emails in minutes**
    - The new template gallery now features over 20 attractive templates for the most typical email types, such as: abandoned cart, event invitation, product launch, newsletter, and more. It is now possible to mark selected templates as favorites and all templates are grouped into relevant categories, making it easier than ever to find just the right template for your next email.
    - [Docs](real-time-marketing-email-get-started.md)

    > [!div class="mx-imgBorder"]
    > ![Screenshot showing the template gallery.](media/whats-new-template-gallery.png "Screenshot showing the template gallery")

- **Send emails quickly without building a journey**
    - Enable anyone to easily send branded, personalized emails with interaction analytics and link tracking. This simplified sending workflow allows you to select from a new template library, make changes easily with simplifications to the email editor, and send emails to the segment members you need to reach within minutes without being a marketing technology expert.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/send-segment-based-emails-quickly-without-building-journey)
    - [Docs](email-without-journey.md)

    > [!div class="mx-imgBorder"]
    > ![Screenshot showing sending emails without a journey.](media/whats-new-send-email-without-building-journey.png "Screenshot showing sending emails without a journey")

- **Easily create modern forms using the new intuitive form experience**
    - Lead capture forms are crucial for gathering marketing information, turning visitors into leads, and turning leads into valuable customers. With the new intuitive forms experience in Customer Insights - Journeys, you can easily create modern forms with advanced capabilities without depending on developers. Effortlessly create smart forms to place on your websites and capture your customers’ attention while allowing them to input their details.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/easily-create-modern-forms-using-new-intuitive-form-experience)
    - [Docs](real-time-marketing-form-overview.md)
 
    > [!div class="mx-imgBorder"]
    > ![Screenshot of Customer Insights - Journeys forms.](media/whats-new-lead-capture-forms.png "Screenshot of Customer Insights - Journeys forms") 

- **Keep stakeholders in the loop by seamlessly copying them on email campaigns**
    - Improve your customer experience by keeping your sales, customer service, and finance teams in the loop by copying key recipients on email campaigns. Enable other teams to follow up on hot leads or rapidly answer customers' inquiries, speeding up your pipeline and increasing customer satisfaction.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/keep-stakeholders-loop-seamlessly-copying-them-email-campaigns)
    - [Docs](real-time-marketing-add-cc-recipients.md)

    > [!div class="mx-imgBorder"]
    > ![Screenshot showing the recipient selection.](media/real-time-email-cc-select-recipient.png "Screenshot showing the recipient selection")

- **Prevent message fatigue by limiting the messages sent to a customer in a specific period**
    - Ensure that your customers receive the right message at the right moment and at the right frequency while preventing fatigue, minimizing unsubscribes, and facilitating optimal engagement with your key messages. Some customers qualify for multiple journeys and campaigns that run simultaneously, which may result in customers receiving multiple messages through one channel in a short period of time. Customers may perceive these messages as spam, which lowers their engagement. With the frequency cap feature, you can optimize engagement by controlling how many messages are sent across multiple channels over a period.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/prevent-message-fatigue-limiting-messages-sent-customer-specific-period)
    - [Docs](real-time-marketing-frequency-cap.md)

    > [!div class="mx-imgBorder"]
    > ![Frequency cap settings screenshot.](media/real-time-marketing-frequency-cap-settings.png "Frequency cap settings screenshot")

- **Measure marketing activity, web traffic, and conversion goals using automatic UTM tagging**
    - Urchin Tracking Module (UTM) codes help you track sources of traffic for your websites and landing pages, enabling you to attribute conversions to the right source. Customer Insights - Journeys messages can be a significant contributor to this traffic, but it is hard to track them without UTM parameters. They’re often left out entirely from the links in messages due to the time-consuming process of manually adding the tags to each link. In addition to automatically tagging all your messages with UTM parameters, you now can choose to customize your parameters so that it matches an existing UTM naming convention that your business already uses in google analytics reports. For example, you can choose UTM campaign to point to a campaign ID instead of the journey name.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/measure-marketing-activity-web-traffic-conversion-goals-using-automatic-utm-tagging)
    - [Docs](real-time-marketing-utm.md)

    > [!div class="mx-imgBorder"]
    > ![Customize UTM links screenshot.](media/real-time-marketing-utm-custom.png "Customize UTM links screenshot")

- **Review engagement history and tailor marketing efforts using contact insights**
    - Use contact insights in Customer Insights - Journeys to gain a better understanding of your audience's behavior and interests, make informed decisions based on past engagement, and tailor your marketing efforts to their specific needs and preferences.
    - [Docs](real-time-marketing-analytics.md)

    > [!div class="mx-imgBorder"]
    > ![Screenshot of contact insights.](media/whats-new-contact-insights.png "Screenshot of contact insights")

- **Drive engagement with personalized content using data with one-to-many relationships**
    - Unlock even more data for personalization with ability to define dynamic text using data that requires traversing one-to-many relations. Consider a university alumni donation campaign where you would want to include the name of the college attended by each alum for driving maximum engagement. However, an alum might have attended multiple colleges in that university, resulting in a "one-to-many" relationship between student and college records. You can now define dynamic text for such data.
    - [Docs](real-time-marketing-predefined-dynamic-text.md)

    > [!div class="mx-imgBorder"]
    > ![Screenshot showing one-to-many personalization.](media/whats-new-personalize-content-1-to-many.png "Screenshot showing one-to-many personalization")

- **Confidently send emails after quickly previewing emails using sample audience data**
    - Personalizing content is an effective strategy for boosting engagement. However, ensuring that the personalized content is accurate for a variety of recipients can be a challenging task. Fortunately, Customer Insights - Journeys makes this easy – simply select a sample audience member record to preview the exact content that will be delivered to that recipient.  
    - [Docs](real-time-marketing-email.md#preview-and-test-send-your-email)

    > [!div class="mx-imgBorder"]
    > ![Screenshot showing email sample data.](media/whats-new-quick-email-preview.png "Screenshot showing email sample data")

- **Scale your business effortlessly and define access to marketing assets**
    - Improve productivity by defining marketing asset access and visibility to match your business structure. As businesses create vast amounts of assets, organizing data according to organizational structure becomes critical. Well-organized assets are important to remaining compliant and productive. Now in Customer Insights - Journeys, you can effortlessly organize your digital assets, content, and journeys to match your organizational structure by separating business and customer data across organizational boundaries. Separating data enables you to gain comprehensive insights into a specific brand's marketing performance without losing sight of the bigger picture. Compliance risk is reduced by using out-of-the-box campaigns and data segregation capabilities across your organization.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/scale-business-effortlessly-define-access-marketing-assets)
    - [Docs](real-time-marketing-business-units.md)

- **Dynamics 365 Customer Insights - Journeys now supports changing the organization URL in Power Platform Admin Center**
    - People often want to change the URL of the Customer Insights - Journeys application to a branded name which is easy to remember. This has been supported for some time in the Power Platform Admin Center, but was not previously supported by the Dynamics 365 Customer Insights - Journeys application. With this release, you can now change the organization URL in Power Platform Admin Center and the Customer Insights - Journeys application continues to work without side effects.
    - [Docs](copy-or-restore.md#change-the-url-for-an-environment-with-customer-insights---journeys-or-outbound-marketing-installed)

### Monthly enhancements

- **Optimize your marketing strategy with unique opens and clicks**
    - Gain insight into the unique individuals who are engaging with your journeys, rather than simply counting the number of times an email or link has been opened or clicked. Tracking unique opens and clicks provides a more accurate picture of your campaign’s reach and engagement by eliminating duplicate interactions from the same customer.
    - [Docs](real-time-marketing-analytics.md)

    > [!div class="mx-imgBorder"]
    > ![Screenshot showing unique opens and clicks.](media/whats-new-unique-opens-and-clicks.png "Screenshot showing unique opens and clicks")

- **Support attachments in custom channel messages**
    - You can now personalize your communications even more by attaching images or other types of files to your custom channel messages. Build new channels like MMS and include images with your WhatsApp or Viber messages, making your customer interactions even more engaging.
    - [Docs](real-time-marketing-create-custom-channels.md)

- **Expanded regional availability for Query Assist**
    - Query Assist, a copilot capability powered by generative AI that enables you to build segments using everyday words, is now available in EUR (Europe).
    - [Docs](real-time-marketing-natural-language.md)

### New blogs and scenario docs

Learn how to make the most of the new Dynamics 365 Customer Insights - Journeys features in our latest blogs and scenario docs:

- [Identify and resolve errors with real-time customer care journeys - Scenario docs](real-time-marketing-customer-care-journey.md)
- [Deliver personalized customer experiences with Copilot in Dynamics 365 Customer Insights - Journeys and Customer Insights - Microsoft Dynamics 365 Blog](https://cloudblogs.microsoft.com/dynamics365/bdm/2023/03/14/deliver-personalized-customer-experiences-with-copilot-in-dynamics-365-marketing-and-customer-insights/)

## March 2023 update

The Dynamics 365 Customer Insights - Journeys March 2023 release general availability features include static segments in Customer Insights - Journeys, filtering for email lists, enriched marketing content with additional file types, support for SMS providers Infobip and LINK Mobility, customized journeys tailored to your business needs, enhanced real-time journey designer, and segments in Customer Insights - Journeys where specific people are always included or excluded.

Public preview features include AI-powered content ideas for engaging content creation, simplified email editor, sending segment-based emails without building a journey, preventing message fatigue by limiting the messages sent to a customer in a specific period, business units for Customer Insights - Journeys, and the ability to hop over one-to-many relationships for dynamic text.

Monthly enhancement includes an upgraded side pane for goals and exit criteria.

### Version number

| App              | GA release      |
|------------------|-----------------|
| Customer Insights - Journeys        |  1.92.2019.0    |

### General availability

- **Create a static snapshot of segment membership**
    - Static segment lists are an important part of audience management for marketers. Use static segments in one-off campaigns or newsletters where it’s essential to implement segment membership based on a specific date or time. Static segments ensure that new people that become eligible for the segment won't enter the one-off journey, even if it continues to be live. You can create static snapshots no matter how the segment is built (whether it uses query conditions or manual inclusions or exclusions). The flexibility in static segment creation separates how segments are defined from how you want to update or refresh segments.
    - [Release plan](/dynamics365-release-plan/2022wave2/marketing/dynamics365-marketing/create-static-snapshot-real-time-marketing-segment-membership)
    - [Docs](real-time-marketing-static-snapshot.md)
  
    > [!div class="mx-imgBorder"]
    > ![static snapshot](media/whats-new-static-snapshot.png "static snapshot")

- **Fine-tune email communications with filtered lists**
    - Including an entire list in an email is a common scenario. But there are times when it's more effective to only include items from a list that meet certain conditions. For example, in a confirmation email about an order, you may need to separately list items that are back-ordered. Similarly, communication about a multi-session conference is easier to consume if the sessions are organized by topic or track. Now you can easily achieve these scenarios by simply adding a filter to your email list.
    - [Release plan](/dynamics365-release-plan/2022wave2/marketing/dynamics365-marketing/fine-tune-email-communications-filtered-lists)
    - [Docs](real-time-marketing-personalize-lists.md)
  
    > [!div class="mx-imgBorder"]
    > ![personalized filtered lists](media/whats-new-personalize-lists.png "personalized filtered lists")

- **Seamlessly manage and embed assets into your content with an enhanced unified library**
    - Sending your customers’ rich, compelling content is key to keeping them engaged with your brand. With this release, using assets across Customer Insights - Journeys and outbound marketing got easier. With the enhanced unified library, you can now upload files once and use them where you need them. No need to copy or download assets for backup. Using additional file types, such as documents, PDFs, presentations, videos and more, you can now add asset links to your emails to create richer content for your customers.
    > [!NOTE]
    > To foster the new simplified way of managing and using assets, the [Customer Insights - Journeys library add-on](upload-images-files.md) is no longer available for installation. If you previously installed it, you could continue to use the add-on.
    - [Docs](upload-images-files.md)

    > [!div class="mx-imgBorder"]
    > ![enhanced asset library](media/whats-new-enhanced-asset-library.png "enhanced asset library")

- **Engage your customers with text messages sent using Infobip and LINK Mobility**
    - In addition to Twilio and Telesign, you can now integrate with Infobip and LINK Mobility to send text messages. Connect your existing Infobip or LINK Mobility account and use all Customer Insights - Journeys text message features to maximize customer engagement.
    - [Docs](real-time-marketing-outbound-text-messaging.md)

    > [!div class="mx-imgBorder"]
    > ![outbound text messaging](media/whats-new-outbound-text-messaging.png "outbound text messaging")

- **Customize the real-time journey designer to better streamline your business flows**
    - Customization of your customer journeys is now available in Dynamics 365 Real-time Customer Insights - Journeys. Not only can marketers use out-of-the-box Customer Insights - Journeys capabilities to effectively engage with their customers, but they can also now create personalized, flexible, and efficient solutions through Power Apps to better tailor the app to their specific business needs. For example, you can now extend your Real-time journey canvas to add any customized fields through Dataverse to better streamline your business processes for higher efficiency. This allows you to add custom fields such as 'campaign' to your journeys to better manage your assets, collaborate amongst your team members, and gives you more flexibility to create customized analytics reports.
    - [Docs](real-time-marketing-journey-designer.md)

    > [!div class="mx-imgBorder"]
    > ![customize journey designer](media/whats-new-journey-designer.png "customize journey designer")

- **Individually manage segment members with inclusions and exclusions**
    - Adding manual inclusions or exclusions is a powerful way to augment segment-building criteria. Manually include or exclude specific people to ensure that segments always reach VIP customers. Or use inclusions and exclusions as an easy way to build test segments for journeys.
    - [Release plan](/dynamics365-release-plan/2022wave2/marketing/dynamics365-marketing/individually-manage-segment-members-inclusions-exclusions)
    - [Docs](real-time-marketing-include-exclude.md)

### Public preview

- **Easily create engaging content using AI-powered Content ideas Copilot**
    - Content ideas uses generative AI to help you find inspiration and can be used as a starting point when composing text for your email. Now, Content ideas features a refreshed look & feel, and generated results are much more creative and of great quality. Additionally, you can select from one of available tone-of-voices (engaged, casual, adventurous, luxury, formal), to make your content even more engaging.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/easily-create-engaging-content-using-ai-powered-content-ideas)
    - [Docs](content-ideas.md)

- **Accurately target customers using improved AI-powered natural language segments**
    - The query assist feature is enhanced with generative AI capabilities. Use conversational, everyday language to quickly build targeted segments. Generate rules that are more accurate with less effort, allowing you to spend more time building customer relationships and less time constructing complex segments from scratch. For example, you can say “Please show me active contacts that attended the coffee tasting event”
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/accurately-target-customers-using-improved-ai-powered-natural-language-segments)
    - [Docs](real-time-marketing-natural-language-segments.md)

- **Create beautiful and engaging emails in minutes**
    - The simplified email editor with the improved template gallery allows you to create engaging content within minutes, whether you are an experienced marketer or create emails occasionally to engage with your customers. Now, you can make basic content modifications directly on canvas, and enjoy easy, delightful, and focused experience. Whereas the new template gallery makes it easier than ever to find just the right template for your next email. 
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/send-segment-based-emails-quickly-without-building-journey)

    > [!div class="mx-imgBorder"]
    > ![Screenshot of easy email editor.](media/whats-new-easy-email.png "Screenshot of easy email editor")

- **Send emails quickly without building a journey**
    - Send emails without creating a journey. This workflow allows you to select from a new template library, make changes easily with simplifications to the email editor, and send emails to the segment members you need to reach within minutes.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/send-segment-based-emails-quickly-without-building-journey)
    - [Docs](email-without-journey.md)

    > [!div class="mx-imgBorder"]
    > ![Screenshot showing sending emails without a journey.](media/whats-new-send-email-without-building-journey.png "Screenshot showing sending emails without a journey")

- **Prevent message fatigue by limiting the messages sent to a customer in a specific period**
    - Ensure that your customers receive the right message at the right moment and at the right frequency to prevent fatigue, avoid unsubscribes, and facilitate optimal engagement with your key messages. Some customers qualify for multiple journeys and campaigns that run simultaneously. This results in customers receiving multiple messages through one channel in a short period of time. Customers may perceive these messages as spam, which lowers their engagement. With the frequency cap feature, you can optimize engagement by controlling how many messages are sent across multiple channels over a period.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/prevent-message-fatigue-limiting-messages-sent-customer-specific-period)
    - [Docs](real-time-marketing-frequency-cap.md)

    > [!div class="mx-imgBorder"]
    > ![Frequency cap settings screenshot.](media/real-time-marketing-frequency-cap-settings.png "Frequency cap settings screenshot")

- **Scale your business effortlessly and define access to marketing assets**
    - Improve productivity by defining marketing asset access and visibility to match your business structure. As businesses create vast amounts of assets, organizing data according to organizational structure becomes critical. Well-organized assets are important to remaining compliant and productive. Now in Customer Insights - Journeys, you can effortlessly organize your digital assets, content, and journeys to match your organizational structure by separating business and customer data across organizational boundaries. Separating data enables you to gain comprehensive insights into a specific brand's marketing performance without losing sight of the bigger picture. Compliance risk is reduced by using out-of-the-box campaigns and data segregation capabilities across your organization.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/scale-business-effortlessly-define-access-marketing-assets)
    - [Docs](real-time-marketing-business-units.md)

- **Hop over one-to-many relationships for dynamic text**
    - With dynamic text data that requires traversing 1-to-many relations, unlock even more data for personalization. Consider a university alumni donation campaign where you would want to include the name of the college attended by each alum for driving maximum engagement. However, an alum might have attended multiple colleges in that university, resulting in a "1-to-many" relationship between student and college records. Dynamic text can now be defined for such data.
    - [Docs](real-time-marketing-predefined-dynamic-text.md)

    > [!div class="mx-imgBorder"]
    > ![dynamic text](media/whats-new-personalization-dynamic-text.png "dynamic text")

### Monthly enhancement

- **Updated journey side pane**
    - The new journey side pane is designed to improve productivity and streamline your workflow by displaying all the important information upfront. The entry and exit criteria and the journey’s goal and frequency cap settings are more discoverable, making it easier for you to remember to change or update these settings without leaving the journey canvas.

### New blogs and scenario docs

Learn how to make the most of the new Dynamics 365 Customer Insights - Journeys features in our latest blogs and scenario docs:

- [Customer Insights - Journeys – Using Conditional Content within your emails! - Dynamics FastTrack Blogs](https://community.dynamics.com/blogs/post/?postid=d87eb0dd-1965-404a-830c-b7b14c8577f4)
- [Level up customer journeys with advanced orchestration features in Dynamics 365 Customer Insights - Journeys - Microsoft Dynamics 365 Blog](https://cloudblogs.microsoft.com/dynamics365/it/2023/02/03/level-up-customer-journeys-with-advanced-orchestration-features-in-dynamics-365-marketing/)
- [Extend and optimize your customer outreach with custom channels - Microsoft Dynamics 365 Blog](https://cloudblogs.microsoft.com/dynamics365/it/2023/02/23/extend-and-optimize-your-customer-outreach-with-custom-channels/)

## February 2023 update

This month, the new Customer Insights - Journeys segment builder is generally available. Also, a new public preview feature allows you to measure marketing activity, web traffic, and conversion goals using automatic UTM tagging.

### Version number

| App              | GA release      |
|------------------|-----------------|
| Customer Insights - Journeys        |  1.91.2018.0    |

### General availability

- **Target the right audience using the new segment builder**
    - Improve your productivity by intuitively creating segments for contacts and leads in the new segment builder. To improve marketing return on investment, your segments must target the right audience. You can now build segments effortlessly by describing them in natural language (using GPT) or by using an easy drag-and-drop logic builder that doesn’t require specialized knowledge of complex data structures and logical operators. To further ensure your confidence in building segments, you can preview the members and estimate the size of draft segments as part of the creation process (within seconds for most segments). In addition, the segment builder enables you to build segments using leads. You can then target the leads directly using customer journeys for your demand generation programs.
    - [Release plan](/dynamics365-release-plan/2022wave2/marketing/dynamics365-marketing/target-right-audience-using-new-segment-builder)
    - [Docs](real-time-marketing-build-segments.md)

    > [!div class="mx-imgBorder"]
    > ![Screenshot of a new segment builder.](media/whats-new-segment-builder.png "Screenshot of a new segment builder")

### Public preview

- **Measure marketing activity, web traffic, and conversion goals using automatic UTM tagging**
    - Urchin Tracking Module (UTM) codes help you track sources of traffic for your websites and landing pages, enabling you to attribute conversions to the right source. Customer Insights - Journeys messages can be a significant contributor to this traffic, but it's hard to track them without UTM parameters. Links in messages are overlooked due to the time-consuming process of manually adding tags to each link. Dynamics 365 Customer Insights - Journeys now automatically tags all your links in messages with UTM parameters, following a consistent taxonomy. This gives you full visibility into your marketing contribution to web traffic, empowering you to optimize traffic and conversions.
    - [Release plan](/dynamics365/release-plan/2023wave1/marketing/dynamics365-marketing/measure-marketing-activity-web-traffic-conversion-goals-using-automatic-utm-tagging)
    - [Docs](real-time-marketing-utm.md)

    > [!div class="mx-imgBorder"]
    > ![Customize your UTM links screenshot.](media/real-time-marketing-utm-custom.png "Customize your UTM links screenshot")

### Monthly enhancements

- **View Total Opens and Total Clicks KPIs and interactions in Delivery and Interactions details**
    - Track the effectiveness of your customer experiences and make data-driven decisions to optimize your marketing strategies. Understanding how many people have seen a marketing message and how many people have engaged with the experience by clicking on a link can help identify which channels are driving more engagement, allowing you to make informed decisions on how to optimize your marketing strategy.
    > [!NOTE]
    > This feature includes the temporary removal of Unique clicks and Opens from Delivery and Interactions details. Unique clicks and Opens will be added back in an upcoming release.
- **Easily manage additional tables available for personalization**
    - You can use up to 50 tables for personalization in Customer Insights - Journeys (see details [here](real-time-marketing-predefined-dynamic-text.md#access-even-more-data-for-personalization)). You have control over which 50 tables to select. This selection step is easier now with additional pre-defined filters to quickly filter the tables list to all tables, tables selected by default, tables that you've selected, or tables that are in use in the current message.
- **Support for multi-line conditions in inline conditions**
    - Inline conditions are used to create HTML code for scenarios where conditional content is not appropriate such as changing one word in otherwise common content (for example, a salutation word). This user experience is now enhanced with the same condition builder experience used everywhere in the product, improving ease of use and delivering the added functionality of multi-line conditions. Learn more: [How to use inline conditions](real-time-marketing-personalize-inline-conditions.md).
- **No-code approach to adding marketing interactions to the unified timeline in custom contact/lead forms**
    - When using out-of-the-box contact/lead forms, marketing interactions based on journeys in Customer Insights - Journeys and outbound marketing are automatically populated in the unified timeline. But when marketers used custom contact/lead forms, they had to manually add the marketing interactions into the timeline by making code changes. With the February release, you can add marketing interactions to your custom contact/lead forms through a simple no-code approach by adding a custom connector to your custom forms through the Power Apps maker experience. Learn more: [How to enable marketing interactions in your contact/lead timeline](timeline.md#how-to-enable-marketing-interactions-in-your-contactlead-timeline).
- **Customer Insights - Journeys interactions in the unified timeline now showcase specific links clicked by contacts/leads in messages**
    - Sales reps and customer service agents now have visibility into specific links that a contact/lead clicked in their marketing messages. Viewing the specific links helps them understand the contact/lead’s past activities at a more granular level, enabling more personalized engagement. For instance, a credit card agent in a financial services firm can now understand which credit card offer (among many) a contact clicked on in a promotional message, allowing them to make a personalized follow-up call. Learn more: [Customer interactions timeline](timeline.md).

### New blogs and scenario docs

Learn how to make the most of the new Dynamics 365 Customer Insights - Journeys features in our latest blogs and scenario docs:
- [Boost event engagement with real-time journeys - Scenario docs](real-time-marketing-event-registration-journey.md)
- [Customer Insights - Journeys – Using Conditional Content within your emails! - Dynamics FastTrack Blogs](https://community.dynamics.com/blogs/post/?postid=d87eb0dd-1965-404a-830c-b7b14c8577f4)
- [Level up customer journeys with advanced orchestration features in Dynamics 365 Customer Insights - Journeys - Dynamics 365 IT Pro Blogs](https://cloudblogs.microsoft.com/dynamics365/it/2023/02/03/level-up-customer-journeys-with-advanced-orchestration-features-in-dynamics-365-marketing/)

## January 2023 update

There is no Dynamics 365 Customer Insights - Journeys release for January. We will be back in February with new feature improvements, updates, and bug fixes.

### New blogs and scenario docs

Learn how to make the most of the new Dynamics 365 Customer Insights - Journeys features in our latest blogs and scenario docs:

- [Boost event engagement with journeys - Scenario docs](real-time-marketing-event-registration-journey.md)
- [Real Time Marketing – Using Conditional Content within your emails! - Dynamics FastTrack Blogs](https://community.dynamics.com/blogs/post/?postid=d87eb0dd-1965-404a-830c-b7b14c8577f4)

> [!Tip]
> To read about updates from previous years, see the [What's new archive](whats-new-marketing-archive.md) article.

[!INCLUDE [footer-include](./includes/footer-banner.md)]
