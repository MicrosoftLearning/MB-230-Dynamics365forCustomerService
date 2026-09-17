---
lab:
  title: 'Lab: Creating queues'
  module: 'Module 1: Manage cases, workloads, and service commitments in Dynamics 365 Customer Service'
  description: You are a customer service manager at Contoso Coffee. You need to create queues that service representatives can use to process cases. In this lab, you create public and private queues, add cases to queues, and work with queue items. This exercise should take approximately 20 minutes to complete.
  duration: 20 minutes
  level: 100
  islab: true
---

# Practice Lab – Queues

## Scenario

You are a customer service manager at Contoso Coffee. You need to create queues that service representatives can use to process cases. In this lab, you create public and private queues, add cases to queues, and work with queue items. This exercise should take approximately 20 minutes to complete.

## Exercise 1 – Create queues

In this exercise, you create four basic queues. Unified routing is configured in a later lab.

### Task 1 – Create queues

1. Use the app selector to open **Copilot Service admin center**.

1. Select **Queues** in **Customer support**.

1. On the **Queues** page, select **Manage** for **Basic queues**.

1. On the command bar, select **+ New**.

1. Enter **Support** for **Name**, select **Public** for **Type**, and enter **support@crmdemo.dynamics.com** for **Incoming Email**.

1. Select **Save & Close**.

> **Note:** A later lab reviews email record-creation configuration without requiring you to send an email to this address.

1. On the command bar, select **+ New**.

1. Enter **Bronze** for **Name** and select **Private** for **Type**.

1. Select **Save**.

1. In the **Members** section, select **Add Existing User**, and then add your user account. (Because you are the owner, your account may already be listed - you do not need to re-add it if it already appears in the list.)

1. Select **Save & Close**.

1. Repeat steps 7-11 to create the following private queues and add your user account as a member of each queue:

  - **Silver**
  - **Gold**

1. Return to the **Basic queues** list, and then select the **My Active Queues** view.

1. Confirm that the list includes the **Support**, **Bronze**, **Silver**, and **Gold** queues.

### Task 2 – Add cases to queues

1. Use the app selector to open **Copilot Service workspace**.

1. Select **Cases** in the site map.

1. Select the **Annual Maintenance Required** case that you created in Lab 1.

1. On the command bar, select **Add to Queue**.

1. In the **Queue** field, search for and select the **Bronze** queue.

1. Select **Add**.

1. Return to **Cases**.

1. Select the **Coffee Brewer Not Heating** case that you created in Lab 1.

1. On the command bar, select **Add to Queue**.

1. In the **Queue** field, search for and select the **Support** queue.

1. Select **Add**.

1. Select **Queues** in the site map.

1. Select the **All Items in Selected Queues** view, and then select **All Queues** in the queue list.

1. Confirm that **Annual Maintenance Required** is listed for the **Bronze** queue.

1. Confirm that **Coffee Brewer Not Heating** is listed for the **Support** queue.

> **Note:** If either case is missing, return to Lab 1 and confirm that the case exists, and then repeat the applicable **Add to Queue** steps.

### Task 3 – Perform actions on queue items

1. Select **Queues** in the site map.

1. Select the **Items available to work on** view.

1. Select **Queues I'm a member of** in the queue list.

1. Confirm that **Annual Maintenance Required** is listed for the **Bronze** queue.

1. Select the checkbox next to the case.

1. On the command bar, select **Queue Item Details**.

1. Confirm that **Worked By** is blank.

1. Select **Save & Close**.

1. Select the checkbox next to the case.

1. On the command bar, select **Pick**.

1. Leave **Also remove the item(s) from the Queue** set to **No**, and then select **Pick**.

1. Select the **Items I am working on** view.

1. Select the checkbox next to the case.

1. On the command bar, select **Queue Item Details**.

1. Confirm that **Worked By** is set to your user.

1. Select **Save & Close**.

1. Select the checkbox next to the case.

1. On the command bar, select **Release**, and then confirm by selecting **Release**.

1. Confirm that the case no longer appears in **Items I am working on**.
