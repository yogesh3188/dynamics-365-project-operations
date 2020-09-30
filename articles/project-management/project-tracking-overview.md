---
# required metadata

title: Project tracking overview
description: This topic provides information about how to track project progress and cost consumption.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customer-service
ms.reviewer: kfend
ms.author: ruhercul
---

# Project tracking overview

_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_

The need to track progress against a schedule varies by industry. Some industries track at a granular level, where other industries track at a higher level. This topic shows how to schedule in order to meet your organization's requirements.

## Effort tracking view

The **Effort tracking** view tracks the progress of tasks in the schedule by comparing the actual effort hours spent on a task to the task's planned effort hours. Dynamics 365 Project Operations uses the following formulas to calculate the tracking metrics:

- **Progress percentage**: Actual effort spent to date ÷ Estimate at complete (EAC) 
- **Estimate to complete (ETC)**: Planned effort – Actual effort spent to date 
- **EAC**: Remaining effort + Actual effort spent to date 
- **Projected effort variance**: Planned effort – EAC

Project Operations shows a projection of the effort variance on the task. If the EAC is more than the planned effort, the task is projected to take more time than was originally planned and is behind schedule. If the EAC is less than the planned effort, the task is projected to take less time than was originally planned and is ahead schedule.

## Reprojecting effort

Project managers often revise the original estimates on a task. Project reprojections are a project manager's perception of estimates, given the current state of a project. However, we don't recommend that project managers change the baseline numbers. This is because the project baseline represents the established source of truth for the project schedule and cost estimate, and all project stakeholders have agreed to it.

There are two ways that a project manager can reproject effort on tasks:

- Override the default ETC with a new estimate of the actual remaining effort on the task. 
- Override the default progress percentage with a new estimate of the true progress on the task.

Each approach causes a recalculation of the task's ETC, EAC, progress percentage, and the projected effort variance on a task. The EAC, ETC, and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.

## Reprojection of effort on summary tasks

Effort on summary tasks or container tasks can be reprojected. Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:

- The EAC, ETC, and progress percentage on the task are calculated.
- The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.
- The new EAC on each of the individual tasks down to the leaf node tasks is calculated. 
- The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value. This results in a new projection for the effort variance of the task. 
- The EACs of the summary tasks all the way to the root node are recalculated.

### Cost tracking view 

The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task. 

> [!NOTE]
> This view shows only labor costs and doesn’t include costs from the expense estimates. 
Project Operations uses the following formulas to calculate the tracking metrics:

- **Percentage of cost consumed**: Actual cost spent to date ÷ Estimated cost at completion
- **Cost to complete (CTC)**: Planned cost – Actual cost spent to date
- **EAC**: Remaining cost + Actual cost spent to date
- **Projected cost variance**: Planned cost – EAC

A projection of the cost variance is shown on the task. If the EAC is more than the planned cost, the task is projected to cost more than was originally planned. Therefore, it's trending over budget. If the EAC is less than the planned cost, the task is projected to cost less than was originally planned. Therefore, it's trending under budget.

## Project manager’s reprojection of cost

When effort is reprojected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.

## Project status summary

Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels. The **Status** section on the **Project entity** page shows a summary of project-level status.

## Status summary fields

The **Overall project status** field is an editable field that shows the overall status of the project. It uses color-coding, such as green, yellow, and red, to indicate increasing risk. The **Comments** field lets the project manager enter specific comments about the status. The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.

The **Schedule performance** and **Cost performance** fields are set from the tracking date. When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**. When the schedule and cost variance for the root node are negative, you can set them to **Behind**.