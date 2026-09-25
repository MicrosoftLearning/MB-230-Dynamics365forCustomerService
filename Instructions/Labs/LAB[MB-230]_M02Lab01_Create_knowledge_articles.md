---
lab:
    title: 'Lab: Create knowledge articles'
    module: 'Module 2: Work with knowledge management in Dynamics 365 Customer Service'
    description: As a knowledge manager at Contoso Coffee, you create governed troubleshooting guidance for service representatives. In this lab, you create, review, publish, revise, and find a knowledge article. This exercise should take approximately 20 minutes to complete.
    duration: 20 minutes
    level: 100
    islab: true
    primarytopics:
        - Dynamics 365
---

# Practice Lab – Create and use knowledge articles

## Scenario

As a knowledge manager at Contoso Coffee, you create governed troubleshooting guidance for service representatives. In this lab, you create, review, publish, revise, and find a knowledge article. This exercise should take approximately 20 minutes to complete.

## Exercise 1 – Manage a knowledge article

In this exercise, you create, approve, publish, revise, and use an internal knowledge article for troubleshooting a coffee brewer that doesn't heat water.

### Task 1 – Create an internal article

In this task, you create an internal knowledge article for troubleshooting a coffee brewer that doesn't heat water.

1. Use the app selector to open **Copilot Service workspace**.

1. In the site map, go to **Service** > **Knowledge Articles**.

1. Select **New**.

1. Enter the following values:

    - **Title**: `Coffee Brewer Not Heating`
    - **Keywords**: `coffee, brewer, heating, reset`
    - **Description**: `Troubleshooting procedure for a coffee brewer that doesn't heat water.`

1. Select **Save**.

1. In the **Content** section, confirm that the **Designer** tab is selected.

1. Enter **Purpose and scope**, select the text, and then apply the **Heading 2** paragraph format.

1. Start a new line, return the paragraph format to **Normal**, and enter the following text:

    `Use the following procedure to troubleshoot cases where a Contoso Coffee Pro 100 Brewer doesn't heat water.`

1. Start a new line, enter **Procedure**, and then apply the **Heading 2** paragraph format.

1. Start a new line, return the paragraph format to **Normal**, and then select **Numbered list**.

1. Enter the following steps as the numbered procedure:

    ```
    1. Confirm that the coffee brewer is connected to a working power outlet.
    2. Confirm that the water reservoir is filled and seated correctly.
    3. Turn off the coffee brewer and unplug it from the power outlet.
    4. Wait 30 seconds.
    5. Reconnect the coffee brewer, turn it on, and run a heating cycle.
    6. If the coffee brewer still doesn't heat, escalate the case.
    ```

1. Select **Save**.

1. Set **Status Reason** to **Needs Review**.

1. In the business process flow, select the **Author** stage.

1. Select an appropriate value for **Article Subject**.

1. Set **Mark for Review** to **Completed**.

### Task 2 – Approve and publish the knowledge article

In this task, you act as an authorized knowledge reviewer and publisher. Your trial user must have permission to approve and publish knowledge articles.

1. On the command bar, select **Approve**. You might need to select **More commands** (...) to find the action.

1. In the confirmation dialog, select **OK**.

1. Confirm that the article status is **Approved**.

1. On the command bar, select **Publish**.

1. In the publish dialog, select **Now** for **Publish** and **Published** for **Published status**.

1. Select **Publish**, and then confirm that the article status is **Published**.

### Task 3 – Revise the knowledge article

In this task, you correct the escalation step by creating and publishing a minor version. The current published article remains available while you edit the new version.

1. Keep the published **Coffee Brewer Not Heating** article open.

1. On the command bar, select **Create Minor Version**. You might need to select **More commands** (...) to find the action.

1. In the confirmation dialog, select **OK**.

1. In the **Content** section, replace step 6 of the procedure with the following text:

    `If the coffee brewer still doesn't heat, assign the case to a manager.`

1. Select **Save**.

1. On the command bar, select **Approve**, and then select **OK** in the confirmation dialog.

1. On the command bar, select **Publish**.

1. Select **Now**, select **Published** for **Published status** if that field is displayed, and then select **Publish**.

1. Return to **Knowledge Articles** and select the **My Active Articles** view.

1. Open **Coffee Brewer Not Heating** and confirm that the published article contains the revised step.

1. On the **Summary** tab, under **Related Information**, select **Related Versions**.

1. Confirm that the current version is published and the earlier version is retained in the version history.

### Task 4 – Find the article from a case

In this task, you validate that a representative can find the published article while working on a case.

1. In the site map, select **Cases**.

1. Select the **My Active Cases** view, and then open **Coffee Brewer Still Not Heating After Reset**.

1. In the app side pane, select the **Knowledge search** icon.

1. If Knowledge Search displays **Knowledge Article entity is not enabled for Knowledge management**, complete these steps:

    1. Open a new browser tab and sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com/) as a system administrator.

    1. In the navigation pane, select **Manage**, and then select **Environments**.

    1. Select the environment that you use for this lab, and then select **Settings** on the command bar.

    1. Expand **Product**, and then select **Features**.

    1. Under **Dataverse search**, confirm that both of the following options are selected:

        - **Turn on search indexing to support Dataverse intelligence (Work IQ) in AI and agent experiences**
        - **Show global search bar in all model-driven apps and turn on search indexing to support search-only experiences**

    1. Select **Save**. Don't turn either option off; turning off Dataverse search removes the existing index.

    1. If the page indicates that search provisioning is in progress, wait for provisioning to finish.

    1. Return to **Copilot Service workspace**, refresh the browser, reopen **Knowledge search**, and then continue.

1. Replace the default search term with **coffee brewer not heating**, and then run the search.

1. Open **Coffee Brewer Not Heating** and confirm that the published article is available from the case context.

> [!NOTE]
> Don't send an article email in this trial lab. Email delivery requires an approved, configured mailbox, and a customer-accessible URL requires external portal configuration.
