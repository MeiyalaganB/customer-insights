---
title: Data management settings 
description: Learn how to import, export, and clean data in Dynamics 365 Customer Insights - Journeys.
ms.date: 08/18/2023
ms.topic: article
author: alfergus
ms.author: alfergus
search.audienceType: 
  - admin
  - customizer
  - enduser
---

# Data management settings

[!INCLUDE [consolidated-sku-rtm-only](./includes/consolidated-sku-rtm-only.md)]

This topic describes what you can do when working in the **Advanced Settings** > **Data Management** section of the **Settings** menu ![The Settings menu icon.](media/settings-icon.png "The Settings menu icon") at the top of the page.

<a name="import"></a>

## Import data and manage imports

Bring your customer and sales data quickly into your app by importing it. You can import data into most record types.

Dynamics 365 Customer Insights - Journeys processes imports in the background. After an import is completed, you can review which records were successfully imported, failed to be imported, or were partially imported. To fix the records that failed to be imported, export them into a separate file, fix them, and then try to import them again (if necessary, you can start over by deleting all records associated with the previous import).

Data can be imported from:

- Most list views
- The **Settings** ![The Settings menu icon.](media/settings-icon.png "The Settings menu icon") > **Advanced settings** > **Data management** > **Imports** settings page

When you import data while working in the **Settings** work area, you must select the entity you want to import to (such as a lead or contact).

More information: [Import data](import-data.md)

<a name="export"></a>

## Export data or templates

Present information to people who don't have access to Dynamics 365 Customer Insights - Journeys by exporting the data to an Excel workbook. You can export just the data from a list, or you can export a template.

When you export a template, a ready-made workbook with column headings matching the fields of the record is created for you. Templates are already formatted as expected by Dynamics 365, so they are easy to edit and reimport later.

Data and templates can be exported from:

- Most list views
- The **Settings** ![The Settings menu icon.](media/settings-icon.png "The Settings menu icon") > **Advanced settings** > **Data management** > **Imports** page

When you export data or templates while working in the **Settings** work area, you must select the entity you want to export (such as a lead or contact). You can also choose the view that will be used for exporting. If you don't choose a view, the default view is selected, and the data or template for all the columns in that view are exported.

More information: [Export data](export-data-word-excel.md)

<a name="duplicate-detection"></a>

## Keep your data clean by using duplicate detection

> [!IMPORTANT]
> Duplicate detection settings only apply to outbound marketing, not Customer Insights - Journeys.

To maintain the integrity of your data, it's a good idea to set up duplicate detection to find duplicate records in the system. By default, duplicate detection is already enabled for outbound marketing.

### Duplicate detection rules

Outbound marketing includes duplicate detection rules for accounts and contacts. The rules are automatically published when duplicate detection is enabled.

- Accounts with the same account name are found
- Contacts with the same first name and last name are found
- Contacts with the same email address are found

If any of these rules are deleted, duplicate detection won't work as expected.

### Enable duplicate detection

If duplicate detection is disabled, duplicates won't be detected. To enable duplicate detection:

1. Go to **Settings** ![The Settings menu icon.](media/settings-icon.png "The Settings menu icon") > **Advanced Settings** > **Data Management** > **Duplicate Detection Settings**.
1. Check the box next to **Enable duplicate detection**.

### When does duplicate detection happen?

If duplicate detection is enabled, duplicates are detected when:

- **A record is created or updated**: The system checks for duplicates when a user enters or updates records.
- **During data import**: When you use the Import Data wizard to bring in contacts or accounts, the wizard detects any duplicate records.

> [!IMPORTANT]
> Duplicates aren't detected when a user merges two records, activates or deactivates a record, or saves a completed activity.

### Disable duplicate detection

If your system contains a large number of records, checking for duplicates can affect performance. You might want to disable duplicate detection at such times.

1. To disable duplicate detection, go to **Settings** > **Advanced Settings** > **Data Management** > **Duplicate Detection Settings**.
1. Uncheck the box next to **Enable duplicate detection**.

All the duplicate detection rules will be unpublished in the back end.

[!INCLUDE [footer-include](./includes/footer-banner.md)]
