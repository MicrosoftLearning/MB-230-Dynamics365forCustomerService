---
lab:
  title: 'Lab: Configure service-level agreements and entitlements'
  module: 'Module 1: Manage cases, workloads, and service commitments in Dynamics 365 Customer Service'
  description: As a customer service manager at Contoso Coffee, you configure service calendars, a service-level agreement, and an entitlement. You then validate how these records apply to customer cases.
  duration: 45 minutes
  level: 100
  islab: true
---

# Practice Lab – Configure service-level agreements and entitlements

## Scenario

As a customer service manager at Contoso Coffee, you need to define predictable response commitments and the support terms available to Relecloud. In this lab, you create service calendars, configure and test a service-level agreement (SLA), and associate an entitlement with an existing case. This exercise should take approximately 45 minutes to complete.

## Exercise 1 – Configure service commitments

In this exercise, you create a Unified Interface SLA and an entitlement that uses it.

### Task 1 – Create a holiday schedule

In this task, you create a holiday schedule for use with a customer service schedule.

1. Use the app selector to open **Copilot Service admin center**.

1. In the site map, go to **Operations** > **Calendar**.

1. In the **Holiday calendar** section, select **Manage**.

1. Select **New**.

1. Enter **Contoso Coffee Holidays** for **Name**, and then select **Create**.

1. In the **Contoso Coffee Holidays** section, select **New**.

1. Enter **Local festival** for **Name**.

1. Set **Start Date** and **End Date** to the same date, two days from today.

1. Select **OK**.

1. Select **Save & Close**.

### Task 2 – Create a customer service schedule

In this task, you define the business hours used to calculate SLA warning and failure times.

1. Return to **Operations** > **Calendar** in Copilot Service admin center.

1. In the **Customer service schedule** section, select **Manage**.

1. Select **New**.

1. Enter **Contoso Coffee Support Hours** for **Name**, and then select **Create**.

1. Clear **Saturday** and **Sunday**.

1. Select **Set Work Hours**.

1. Set the start time to **9:00 AM** and the end time to **5:00 PM**.

1. Select **OK**.

1. Set **Holiday Schedule** to **Observe**, and then select **Contoso Coffee Holidays**.

1. Select your local **Time Zone**.

1. Select **Save & Close**.

### Task 3 – Create and activate an SLA

In this task, you create an SLA that allows one business hour for the first response to a problem case. You also configure a noncompliance action that marks the case as escalated.

1. In Copilot Service admin center, go to **Operations** > **Service terms**.

1. In the **SLA KPIs** section, select **Manage**.

1. Select **New**.

1. Enter the following values:

  - **Name**: `Case Response By`
  - **Entity Name**: `Case`
  - **KPI Field**: `First Response By KPI`
  - **Applicable From**: `Created On`

1. Select **Save**, and then select **Activate**.

1. Confirm the activation if prompted.

1. Return to **Operations** > **Service terms**.

1. In the **Service-level agreements (SLAs)** section, select **Manage**.

1. Select **New**.

1. Enter **Contoso Coffee Case Response SLA** for **Name**, select **Case** for **Primary Entity**, and then select **Save**.

1. In the **SLA Items** section, select **New SLA Item**.

1. Enter **Problem Case First Response** for **Name**.

1. Select **Case Response By** for **KPI**.

1. Select **Contoso Coffee Support Hours** for **Business Hours**.

1. Under **Applicable When**, select **Add row** and add the following condition:

  `Case Type (Case)` **Equals** `Problem`

1. Under **Success Conditions**, select **Add row** and add the following condition:

  `First Response Sent (Case)` **Equals** `Yes`

1. In **Warn and Fail Duration**, set **Warn After** to **45 minutes** and **Failure After** to **1 hour**.

1. Select **Save**.

1. Select **Configure Actions**. Power Automate opens in a new browser tab.

> [!NOTE]
> If the flow opens in the new designer, turn off the **New designer** toggle to use the classic designer. The classic designer surfaces Customer Service fields and choices by their labels. The new designer might require underlying values, which are outside the scope of this Customer Service lab.

1. If prompted to configure a Dataverse connection, use the current connection and select **Continue**.

1. Expand **Switch**, and then expand the **Is Non-compliant** path. Don't modify the predefined trigger or switch steps.

1. In the **Is Non-compliant** path, select **Add an action**.

1. Search for and select the Microsoft Dataverse **Update a row** action.

1. Select **Cases** for **Table name**.

1. For **Row ID**, insert the **Regarding ID** dynamic value.

1. In the advanced parameters, set **Is Escalated** to **Yes**.

1. Select **Save**, and then close the Power Automate browser tab.

1. Return to the SLA item dialog, and then select **Save and Close**.

1. On the **Contoso Coffee Case Response SLA** record, select **Activate**, and then confirm the activation.

1. Select **Set As Default**, and then select **OK** in the confirmation dialog.

### Task 4 – Configure and test SLA behavior

In this task, you configure organization-level pause behavior and validate the SLA against two cases. You don't need to wait for the warning or failure duration to elapse.

1. In Copilot Service admin center, go to **Operations** > **Service terms**.

1. In the **Other SLA Settings** section, select **Manage**.

1. Confirm that **Disable SLAs** is set to **No**.

1. Set **Apply SLA after manual override** to **Yes**.

1. Under **Select SLA Pause Status**, move **On Hold** and **Waiting for Details** from **Available** to **Selected**.

1. Select **Save**.

1. Use the app selector to open **Copilot Service workspace**.

1. In the site map, select **Cases**, and then select **New Case**.

1. Enter the following values:

  - **Case Title**: `SLA Test #1`
  - **Customer**: `Relecloud`

1. At the top of the case form, expand the caret next to **Owner**, and then set **Origin** to **Web**.

1. On the **Details** tab, set **Case Type** to **Problem**.

1. Select **Save**.

1. Use the form selector to switch to the **Enhanced full case form**.

1. Open the **SLA** tab or SLA details area. Confirm that **Case Response By** is **In Progress** and has warning and failure times.

1. Return to the **Multi-session experience** form and navigate to the **Details** tab. Set **First Response Sent** to **Yes**, and then select **Save**.

1. Return to the **Enhanced full case form** to view the SLA details and confirm that **Case Response By** is **Succeeded**.

1. Return to **Cases**, and then select **New Case**.

1. Enter the following values:

  - **Case Title**: `SLA Test #2`
  - **Customer**: `Relecloud`

1. At the top of the case form, expand the caret next to **Owner**, and then set **Origin** to **Email**.

1. On the **Details** tab, set **Case Type** to **Request**.

1. Select **Save**.

1. Open the SLA details by selecting the **Enhanced full case form** and confirm that no SLA KPI item was created because the case doesn't meet the **Case Type Equals Problem** condition.

### Task 5 – Create and activate an entitlement

In this task, you create case-based support terms for Relecloud and associate the SLA with the entitlement.

1. Use the app selector to open **Copilot Service admin center**.

1. Go to **Operations** > **Service terms**.

1. In the **Entitlements** section, select **Manage**.

1. Select **New**.

1. Enter the following values:

  - **Name**: `Relecloud Standard Support`
  - **Primary Customer**: `Relecloud`
  - **Start Date**: Today's date
  - **End Date**: One year from today
  - **Restrict based on entitlement terms**: `Yes`
  - **SLA**: `Contoso Coffee Case Response SLA`
  - **Allocation Type**: `Number of cases`
  - **Decrease Remaining On**: `Case Resolution`
  - **Total Term**: `10`

1. Select **Save**.

1. Confirm that **Remaining Term** is **10**.

1. On the command bar, select **Activate**.

1. In the confirmation dialog, select **Activate**.

1. Confirm that the entitlement status is **Active**.

### Task 6 – Apply the entitlement and verify term consumption

In this task, you apply Relecloud's support terms to an SLA test case and resolve it. Because the entitlement decreases on case resolution, the remaining term changes only after you resolve the case.

1. Keep the current **Copilot Service admin center** browser tab open. Duplicate the tab, and then use the app selector in the duplicate tab to open **Copilot Service workspace**. Keep both tabs open throughout the task.

1. In the site map, select **Cases**.

1. Select the **My Active Cases** view, and then open **SLA Test #1**.

1. On the **Details** tab, select **Relecloud Standard Support** in the **Entitlement** field.

1. Select **Save**.

1. In the **Copilot Service admin center** browser tab, return to the **Relecloud Standard Support** entitlement and confirm that **Remaining Term** is still **10**. The term decreases when the associated case is resolved.

1. In the **Copilot Service workspace** browser tab, return to **SLA Test #1**.

1. On the command bar, select **Resolve case**. You might need to select **More commands** (...) to find the action.

1. If a message indicates that the case has an open activity, select **Confirm**.

1. In the **Resolve Case** dialog, select **Problem Solved** for **Resolution Type**.

1. Enter `Validating entitlement term consumption` for **Resolution**, and then select **Resolve**.

1. In the **Copilot Service admin center** browser tab, return to **Relecloud Standard Support**.

1. Select **Refresh** in the command bar.

1. Confirm that **Remaining Term** is now **9**.
