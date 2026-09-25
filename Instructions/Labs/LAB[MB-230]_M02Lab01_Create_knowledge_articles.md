---
lab:
    title: 'Lab: Create knowledge articles'
    module: 'Module 2: Work with knowledge management in Dynamics 365 Customer Service'
    description: As a knowledge manager at Contoso Coffee, you create governed troubleshooting guidance for service representatives. In this lab, you create, review, publish, revise, find, and link a knowledge article. This exercise should take approximately 20 minutes to complete.
    duration: 20 minutes
    level: 100
    islab: true
    primarytopics:
        - Dynamics 365
---

# Practice Lab – Create and use knowledge articles

## Scenario

As a knowledge manager at Contoso Coffee, you create governed troubleshooting guidance for service representatives. In this lab, you create, review, publish, revise, find, and link a knowledge article. This exercise should take approximately 20 minutes to complete.

## Exercise 1 – Manage a knowledge article

In this exercise, you create, approve, publish, revise, and use an internal knowledge article for missing parts.

### Task 1 – Create an internal article

In this task, you create an internal knowledge article for missing parts.

1. Use the app selector to open **Copilot Service workspace**.

2. In the site map, go to **Service** > **Knowledge Articles**.

3. Select **New**.

4. Enter the following values:

    - **Title**: `Missing Parts`
    - **Keywords**: `missing, parts, replacement`
    - **Description**: `Procedure for handling an order with missing parts.`

5. Select **Save**.

6. In the **Content** section, confirm that the **Designer** tab is selected.

7. Enter **Purpose and scope**, select the text, and then apply the **Heading 2** paragraph format.

8. Start a new line, return the paragraph format to **Normal**, and enter the following text:

    `Use the following procedure to resolve phone call cases that are related to missing parts.`

9. Start a new line, enter **Procedure**, and then apply the **Heading 2** paragraph format.

10. Start a new line, return the paragraph format to **Normal**, and then select **Numbered list**.

11. Enter the following steps as the numbered procedure:

    ```
    1. Get the customer's order number.
    2. Locate the order record.
    3. Locate and open the product in question.
    4. Confirm whether the product that the customer received is listed.
    5. If it is listed, send the customer a replacement order and a return label.
    6. If it isn't listed, escalate the case.
    ```

12. Select **Save**.

13. Set **Status Reason** to **Needs Review**.

14. In the business process flow, select the **Author** stage.

15. Select an appropriate value for **Article Subject**.

16. Set **Mark for Review** to **Completed**.

### Task 2 – Approve and publish the knowledge article

In this task, you act as an authorized knowledge reviewer and publisher. Your trial user must have permission to approve and publish knowledge articles.

1. On the command bar, select **Approve**. You might need to select **More commands** (...) to find the action.

2. In the confirmation dialog, select **OK**.

3. Confirm that the article status is **Approved**.

4. On the command bar, select **Publish**.

5. In the publish dialog, select **Now** for **Publish** and **Published** for **Published status**.

6. Select **Publish**, and then confirm that the article status is **Published**.

### Task 3 – Revise the knowledge article

In this task, you correct the escalation step by creating and publishing a minor version. The current published article remains available while you edit the new version.

1. Keep the published **Missing Parts** article open.

2. On the command bar, select **Create Minor Version**. You might need to select **More commands** (...) to find the action.

3. In the confirmation dialog, select **OK**.

4. In the **Content** section, replace step 6 of the procedure with the following text:

    `If it isn't listed, assign the case to a manager.`

5. Select **Save**.

6. On the command bar, select **Approve**, and then select **OK** in the confirmation dialog.

7. On the command bar, select **Publish**.

8. Select **Now**, select **Published** for **Published status** if that field is displayed, and then select **Publish**.

9. Return to **Knowledge Articles** and select the **My Active Articles** view.

10. Open **Missing Parts** and confirm that the published article contains the revised step.

11. On the **Summary** tab, under **Related Information**, select **Related Versions**.

12. Confirm that the current version is published and the earlier version is retained in the version history.

### Task 4 – Find and link the article from a case

In this task, you validate that a representative can find the published article while working on a case. Available article actions depend on the workspace configuration and your permissions.

1. In the site map, select **Cases**.

2. Select the **My Active Cases** view, and then open **Coffee Brewer Still Not Heating After Reset**.

3. In the app side pane, select the **Knowledge search** icon.

4. Replace the default search term with **missing parts**, and then run the search.

5. Open **Missing Parts** and review the article to confirm that its published guidance applies to the case scenario.

6. Select **Link article to case**. Depending on your workspace layout, the link action might appear as an icon on the result card or under **More options** (...).

7. Confirm that the article is marked as linked to the case.

> [!NOTE]
> Don't send an article email in this trial lab. Email delivery requires an approved, configured mailbox, and a customer-accessible URL requires external portal configuration.
