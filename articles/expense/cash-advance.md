---
title: Cash advance
description: This topic provides information about cash advances.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: 
ms.search.validFrom: 2020-10-01
---

# Cash advance

_**Applies To:** Project Operations for resource/non-stocked based scenarios_

A cash advance allows employees to borrow money from their company prior to incurring any expenses. When a requested cash advance is approved and paid, the employee can use the money for the business expenses they may be about to incur. 

## Create and submit a cash advance request

1. Under **My Expenses**, select **Cash advances** > **New** to create a new cash advance. 
2. On the **New cash advance request** page, enter the expense purpose and select the location where the expense will be incurred.
3. Enter the requested amount and currency, and then select **Save**. 
4. When you are ready to submit the cash advance request, on the **Cash advance request** page, select **Workflow** > **Submit**.

## Modify a cash advance request

You can modify a cash advance request if it has not been submitted for approval.

1. Under **My Expenses: Cash Advances** locate and select the cash advance you want to edit.
2. Select **Edit**, and make the necessary changes to the cash advance request. 
3. Select **Save and close**.


## View cash advance requests
You can review the list of all the cash advances that are in draft, submitted, in review, or paid under **My Expenses: Cash Advances**. 

## Approve cash advance requests

Managers or users configured as approvers in the workflow will be able to approve the cash advances submitted to them for review. 

1. To approve a cash advance, under **Process cash advances**, select **Cash advances for my review**.
2. Select the cash advance you need to review and select **Approve**.  

## Pay cash advances 
The following procedure is typically completed by an accountant or a user with accounting permissions.

1. To post approved cash advances, select **Approved cash advances**, and then select **Pay and transfer**.  
2. Provide the journal details for the cash advances, and then select **OK**. 

## Submit an expense report against a paid cash advance 

When you create and submit an expense report for the cash advance you already received, the expenses will be automatically adjusted against that advance. If your cash advance is greater than the expensed amount, you must return the balance to the company using the **Return cash** expense category. If the company-paid cash advance is less than the amount you expensed, the company must reimburse you the balance. 

### Example
You plan to travel for a conference from Seattle to New York City. You create a cash advance request for 3000.00 USD as you have estimated the cost of the conference ticket, flights, hotel, meals, and taxi to be apporximately this amount. You will not be paid unless your manager approved this request. After your manager approves, the requested cash advance is paid as 3000.00 USD into your bank account. You then attend the conference. After completing your trip, you find that the total expenditure was only 2790.00 USD. Select **Cash** in the **Payment method** field, and submits your expense for 2790.00 USD. Your submitted expense amount is automatically adjusted against the cash advance of 3000.00 USD that was loaned to you. You now owe a balance of 210.00 USD (3000.00-2790.00) to the company, which you can return to company using the **Return cash** expense category. 