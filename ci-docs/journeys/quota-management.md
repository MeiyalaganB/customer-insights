---
title: Monitor your monthly quotas
description: View your remaining monthly credits for sending marketing email messages and other metered services in Dynamics 365 Customer Insights - Journeys.
ms.date: 08/21/2023
ms.topic: article
author: alfergus
ms.author: alfergus
search.audienceType: 
  - admin
  - customizer
  - enduser
---

# Monitor your monthly quotas

[!INCLUDE [consolidated-sku-rtm-only](./includes/consolidated-sku-rtm-only.md)]

Dynamics 365 Customer Insights - Journeys is a subscription service that is billed monthly and sets organization-level quotas for the maximum number of marketing contact records and monthly outbound interactions that you can send. Other quotas may also apply. You can always upgrade your subscription if you need higher quotas.

The **Quota limits** page shows the total quota levels you have purchased and how much of each quota your organization has already used. To see how much of each quota you've used, go to **Settings** > **Overview** > **Quota limits**.

> [!div class="mx-imgBorder"]
> ![Screenshot of the quota limits area.](media/quota-limits.png)

The following usages and limits are tracked on this screen:

- **Monthly interaction quota**: Shows the total number of outbound interactions (email messages, text messages, and push notifications) that you have sent in the current month.
    - The interaction quota is reset on the first day of each month. 
    - Your interaction quota is equal to ten times your marketing contact quota.
- **Marketing contacts**: Shows the total number of *marketing Contacts* that you can have in your database according to your current Customer Insights - Journeys subscription.
    - Entities that count toward the marketing contact quota include Leads, Contacts, and CI profiles.
    - Marketing contacts only include those that you engage with through interactions such as emails, text messages, or push notifications.
    - Contacts that you never engage in marketing activities won't be counted as part of this quota.
    - If you have multiple environments, the contact quota for each environment is shown so that you can tell how much is being used by each environment.
    - For more information about marketing contacts and how they are counted, see [How Customer Insights - Journeys is licensed](purchase.md#how-licensed) and the [Administration and setup FAQ](setup-troubleshooting.yml#licensing).
    > [!NOTE]
    > Active marketing contacts are counted as contact entities in the Dataverse database if they have received a marketing interaction within the last 12 months prior to the current date. Once a contact hasn't received an interaction in the last 12 months, it is no longer counted as an active contact.
- **Litmus email previews**: Shows the total number of Litmus email previews (inbox previews) users at your organization can still use during the current month.
    - The pre-seeded capacity is shown together with your monthly consumption.
    - The pre-seeded capacity automatically resets on a monthly basis.
- **Free text messages**: For US-based instances, 1,000 free text messages per month can be sent using a toll-free number [created through Azure Communication Services](real-time-marketing-outbound-text-messaging.md#add-a-sender-number-using-the-azure-communication-services-free-trial-preview-us-only).
- **Paid text messages**: Customer Insights - Journeys offers [native integration with Twilio and TeleSign](real-time-marketing-outbound-text-messaging.md#sign-up-for-and-configure-a-twilio-account), enabling you to easily connect with mobile users.
    - You can purchase or reuse an existing SMS provider account with Twilio or TeleSign.
    - Consumption is recorded and displayed on the Quota limits page, but the allocated quota needs to be verified with the third-party provider.

The quota limits page also includes charts that show the monthly interaction usage and the annual total marketing contact usage.

> [!Note]
> Quotas and other limits are different based on whether you are running a trial, preview, or subscribed version of the product.
>
> - For subscribed (paid) versions, please download the [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/p/?linkid=866544).
> - For trials, see [Dynamics 365 Customer Insights - Journeys limits for trials](trial-preview-limits.md).
> 
> See also the [Readme](./known-issues.md) document for the latest news and updates.

[!INCLUDE [footer-include](./includes/footer-banner.md)]
