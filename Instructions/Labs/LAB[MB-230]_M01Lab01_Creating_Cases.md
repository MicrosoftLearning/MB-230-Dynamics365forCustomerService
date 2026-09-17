---
lab:
  title: 'Lab: Creating cases'
  module: 'Module 1: Manage cases, workloads, and service commitments in Dynamics 365 Customer Service'
  description: You are a customer service manager at Contoso Coffee who is preparing the case management experience for service representatives. In this lab, you create the customer, product, case, and activity records used in this and later labs. This exercise should take approximately 20 minutes to complete.
  duration: 20 minutes
  level: 100
  islab: true
---

# Practice Lab – Creating cases

## Scenario

You are a customer service manager at Contoso Coffee who is preparing the case management experience for service representatives. In this lab, you create the customer, product, case, and activity records used in this and later labs. This exercise should take approximately 20 minutes to complete.

## Exercise 1 – Open Copilot Service workspace

In this exercise, you open the representative application used to manage cases.

### Task 1 – Open Copilot Service workspace

1. On the Dynamics 365 apps page, select **Copilot Service workspace**.

1. If another Dynamics 365 application is open, use the app selector to open **Copilot Service workspace**.

1. If the **Trial** dashboard is displayed by default, select the **Customer Service Rep Dashboard** tab.

## Exercise 2 – Create case

In this exercise, you will create an Account, a Contact, a Subject, a Product, and a Case record. You will also add a Phone Call activity to the case.

### Task 1 – Create Account

1. Select **Accounts** in the site map.

1. Select **+ New** on the command bar.

1. Enter **Relecloud** for **Account Name** and **555-0100** for **Phone**.

1. Select the **Details** tab.

1. Select **Consulting** for **Industry**.

1. At the top of the record, expand the caret next to the owner name. Enter **$5,000,000** for **Annual Revenue** and **250** for **Number of Employees**.

1. Select **Save & Close**.

### Task 2 – Create Contacts

1. Select **Contacts** in the site map.

1. Select **+ New** on the command bar.

1.  Enter **Avery** for **First Name**.

1.  Enter **Howard** for **Last Name**.

1. In the **Account Name** field, search for and select the **Relecloud** account that you created in Task 1.

1. Select **Save & Close**.

### Task 3 – Create Subject

1. Use the app selector to open **Copilot Service admin center**.

1. Select **Case Settings** in **Customer Support**.

1. In the **Subjects** section, select **Manage**.

1. On the **Subject tree** page, in **Subject tree management**, select the ellipses and then select **+Add**.

1. Enter **Maintenance** for **Title**.

1. Leave **Parent subject** blank, turn on **Visibility** if it isn't already on, and then select **Save and close**.

### Task 4 – Create Product

1. Use the app selector to open **Power Platform Environment Settings**.

1. Select **Product Catalog** in the **Business** section of the site map.

1. Select **Families and products**.

1. On the command bar, select **Add Product**.

1. Enter **Contoso Coffee Pro 100 Brewer** for **Name** and **CC-P100** for **Product ID**.

1. Select **Quantity** for **Unit Group**.

1. Select **Quantity** for **Default Unit**.

1. Select **0** for **Decimals Supported**.

1. Select **Save**.

1. On the command bar, select **Publish**, and then confirm the action.


### Task 5 – Create Case

Avery is calling to report that the coffee brewer isn't heating. Create a case to track the issue.

Use the app selector to return to **Copilot Service workspace**.

1. Select **Cases** in the site map.

1. On the command bar, select **+ New Case**.

1.  Enter **Coffee Brewer Not Heating** for **Case Title**.

1. In the **Customer** field, search for and select the **Relecloud** account that you created in Task 1.

1. In the **Subject** field, select **Maintenance**.

1. At the top of the record, expand the caret next to the owner name, and then select **Phone** for **Origin**.

1. In the **Product** field, search for and select **Contoso Coffee Pro 100 Brewer**.

1.  Enter **Coffee brewer does not heat water** in the **Description** field.

1. If the enhanced quick case form is displayed, select **Save and close**, and then open the **Coffee Brewer Not Heating** case to continue on the full case form.

1. Select the **Details** tab.

1. Select **Problem** from the **Type** drop-down field.

1. Select **Save**.

1. Select the **Summary** tab. In the timeline, select **+**, and then select **Phone Call**.

1. Enter **Further details** for **Subject**.

1. Select **Outgoing** from the **Direction** drop-down field.

1. Ensure that your user record is set for **Call From**.

1. In **Call To**, remove **Relecloud**, and then add the **Avery Howard** contact.

1. Select **15 minutes** from the **Duration** drop-down field.

1. Select **tomorrow's date** and **9:00AM** for **Due**.

1. Select **High** from the **Priority** drop-down field.

1. Select **Save & Close**.

## Exercise 3 – Create case from an activity

In this exercise, you will create a Phone Call activity and then convert the activity to a Case.

### Task 1 – Create Phone Call activity

Due to the coffee maker issue, Avery requests that her company, Relecloud, be put on an ongoing maintenance plan to prevent further coffee maker issues in their office. Record the request as an incoming phone call.

1. Select **Accounts** in the site map.

1. Select the **Relecloud** account that you created in Exercise 2, Task 1.

1. In the timeline, select **+**, and then select **Phone Call**.

1. Enter **Annual Maintenance Required** for **Subject**.

1.  Select **Incoming** from the **Direction** drop-down field.

1. Ensure that the Relecloud account is set for **Call From**.

1.  Ensure that your user record is set for **Call To**.

1. In the **Description** field, enter **Relecloud requests an ongoing maintenance plan for its coffee brewers**.

1. In the **Duration** field, enter **15 minutes**.

1. Select today's date for **Due**.

1. Select **Save and Close**.

### Task 2 – Convert Phone Call activity

1. In the timeline, select the **Open Record** icon for the phone call that you created.

1. On the command bar, select **Convert To** > **To Case**. (You might need to select **More commands** (...) to find **Convert To**.)

1. In the **Convert to Case** dialog, confirm **Relecloud** is selected as the **Customer.**

1. In the **Subject** field, select **Maintenance**.

1. Select **Convert**.

1. Review the case that was created. Note that the customer is set to Relecloud and the origin is set to Phone.
