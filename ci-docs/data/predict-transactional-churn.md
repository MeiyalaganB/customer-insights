---
title: Predict transaction churn (contains video)
description: "Predict whether a customer is at risk for no longer purchasing your products or services."
ms.date: 10/03/2023
ms.reviewer: mhart
ms.topic: how-to
author: zacookmsft
ms.author: zacook
ms.custom: bap-template 
---

# Predict transaction churn

[!INCLUDE [consolidated-sku](./includes/consolidated-sku.md)]

Transactional churn prediction helps predict if a customer will no longer purchase your products or services in a given time window.

You must have business knowledge to understand what churn means for your business. For instance, a business with annual events can define their churn measured in years, while a business that caters to weekly sales may measure churn in months. We support time-based churn definitions, meaning a customer is considered to have churned after a period of no purchases.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWN6Eg]

For example, Contoso wants to know how engaged customers are so they can run an email campaign dedicated to retention. Through the transaction churn model, Contoso can determine the likelihood that customers will buy again. They can see the leading patterns that lead to customers leaving the brand, allowing them to adjust other strategies.

## Prerequisites

- At least [Contributor permissions](user-roles.md).
- At least 500 customer profiles, preferably more than 1,000 unique customers.
- Customer Identifier, a unique identifier to match transactions to your customers.
- Transaction data for at least double the selected time window such as two to three years of transaction history. Ideally at least two transactions per customer. Transaction history must include:
  - **Transaction ID**: Unique identifier of a purchase or transaction.
  - **Transaction Date**: Date of the purchase or transaction.
  - **Value of the transaction**: Currency or numerical value amount of the transaction.
  - **Unique product ID**: ID of the product or service purchased if your data is at a line item level.
  - **Whether this transaction was a return**: A true/false field that identifies if the transaction was a return or not. If the **Value of the transaction** is negative, we infer a return.
- Customer activity data:
  - Customer Identifier, a unique identifier to map activities to your customers.
  - **Primary key:** Unique identifier for an activity. For example, a website visit or a usage record showing the customer tried a sample of your product.
  - **Timestamp:** Date and time of the event identified by the primary key.
  - **Event:** Name of the event you want to use. For example, a field called "UserAction" in a grocery store might be a coupon use by the customer.
  - **Details:** Detailed information about the event. For example, a field called "CouponValue" in a grocery store might be the currency value of the coupon.
- Less than 20% of missing values in the data field of the table provided

## Create a transaction churn prediction

1. Go to **Insights** > **Predictions**.

1. On the **Create** tab, select **Use model** on the **Customer churn model** tile.

1. Select **Transaction** for the type of churn and then **Get started**.

1. **Name this model** and the **Output table name** to distinguish them from other models or tables.

1. Select **Next**.

### Define customer churn

Select **Save draft** at any time to save the prediction as a draft. The draft prediction displays in the **My predictions** tab.

1. Set the **Prediction window**. For example, predict the risk of churn for your customers over the next 90 days to align to your marketing retention efforts. Predicting churn risk for a longer or shorter period of time can make it more difficult to address the factors in your churn risk profile, but it depends on your specific business requirements.

1. Enter the number of days to define churn in the **Churn definition** field. For example, if a customer hasn't made a purchase in the last 30 days, they might be considered as churned for your business.

1. Select **Next**.

### Add purchase history

1. Select **Add data** for **Customer transaction history**.

1. Select the semantic activity type, **SalesOrder** or **SalesOrderLine**, that contains the transaction history information. If the activity hasn't been set up, select **here** and create it.

1. Under **Activities**, if the activity attributes were semantically mapped when the activity was created, choose the specific attributes or table you'd like the calculation to focus on. If semantic mapping didn't occur, select **Edit** and map your data.

   :::image type="content" source="media/transaction-churn-select-activity.PNG" alt-text="Side pane showing choosing specific activities under the semantic type.":::

1. Select **Next** and review the attributes required for this model.

1. Select **Save**.

1. Add more activities or select **Next**.

### Add additional data (optional)

1. Select **Add data** for **Customer activities**.

1. Select the semantic activity type that contains the data you would like to use. If the activity hasn't been set up, select **here** and create it.

1. Under **Activities**, if the activity attributes were semantically mapped when the activity was created, choose the specific attributes or table you'd like the calculation to focus on. If semantic mapping didn't occur, select **Edit** and map your data.

1. Select **Next** and review the attributes required for this model.

1. Select **Save**.

1. Select **Next**

### Set update schedule

1. For the **Data updates** step, choose a frequency to retrain your model. This setting is important to update the accuracy of predictions as new data is ingested. Most businesses can retrain once per month and get a good accuracy for their prediction.

1. Select **Next**.

### Review and run the model configuration

The **Review and run** step shows a summary of the configuration and provides a chance to make changes before you create the prediction.

1. Select **Edit** on any of the steps to review and make any changes.

1. If you're satisfied with your selections, select **Save and run** to start running the model. Select **Done**. The **My predictions** tab displays while the prediction is being created. The process may take several hours to complete depending on the amount of data used in the prediction.

[!INCLUDE [progress-details](includes/progress-details-pane.md)]

## View prediction results

1. Go to **Insights** > **Predictions**.

1. In the **My predictions** tab, select the prediction you want to view.

There are three primary sections of data within the results page:

[!INCLUDE [predict-transaction-results](includes/predict-transaction-results.md)]

> [!NOTE]
 > In the output table for this model, *ChurnScore* shows the predicted probability of churn and *IsChurn* is a binary label based on *ChurnScore* with 0.5 threshold. If this default threshold doesn't work for your scenario, [create a new segment](segments.md) with your preferred threshold. Not all customers are necessarily active customers. Some of them may not have had any activity for a long time and are considered as churned already, based on you churn definition. Predicting the churn risk for customers who already churned isn't useful because they are not the audience of interest.
>
> To view the churn score, go to **Data** > **Tables** and view the data tab for the output table you defined for this model.

[!INCLUDE [footer-include](includes/footer-banner.md)]
