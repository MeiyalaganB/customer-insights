---
title: Transition event management
description: Learn how to transition event management capabilities from outbound marketing to real-time journeys in Dynamics 365 Customer Insights - Journeys.
ms.date: 10/04/2023
ms.topic: article
author: alfergus
ms.author: alfergus
search.audienceType: 
  - admin
  - customizer
  - enduser
---

# Transition event management

[!INCLUDE [consolidated-sku-rtm-only](./includes/consolidated-sku-rtm-only.md)]

Event management comprises three areas:
- Event setup (including tracks and sessions, speakers, registrants, etc.)
- Communication about events
- Publishing of information about events

More granularly, the event management areas can be broken down as follows:

| Event setup                                                       | Event communication                  | Event publishing          |
|-------------------------------------------------------------------|--------------------------------------|---------------------------|
| Events, speakers, tracks, sessions, registrants | Segments, emails, journeys | Forms, portal pages |

Creation and setup of events, tracks and sessions, speakers, and registrants is unaffected by the change to real-time journeys.

Communication about events is also largely unaffected by the transition to real-time journeys. New emails and journeys are required, but the process of inviting and registering attendees remains consistent. However, there are enhancements associated with the addition of triggers that should be considered when creating event invitation and registration real-time journeys.

Event-based communications in real-time journeys allow for more timely communication with attendees. This is illustrated below:

> [!div class="mx-imgBorder"]
> ![Transition event planning diagram.](media/transition-event-planning.png "Transition event planning diagram")

The one thing that changes with real-time journeys events is the publishing of event information now that the dependency on Power Pages is removed. With outbound marketing, Power Pages were used as a platform to present event data (sessions, speakers, etc.) and handle registrations.

With real-time journeys events, the Power Pages dependency changes and only the registration form is provided. Registration forms can be either self-hosted or embedded into a website. This allows you to create the online presence you require for events using your technology of choice while capturing event registrations into Customer Insights - Journeys. Your technology of choice can include Power Pages (as it did with outbound marketing) if so desired, but you need to create the necessary pages for the event.

[!INCLUDE [footer-include](./includes/footer-banner.md)]