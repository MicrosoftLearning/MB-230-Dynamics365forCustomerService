---
lab:
  title: 'Lab: Configure a representative experience profile'
  module: 'Module 4: Configure AI and the service representative experience'
  description: As a customer service manager at Contoso Coffee, you configure a targeted Copilot Service workspace experience with a case session, an application tab, a guidance script, and knowledge search.
  duration: 30 minutes
  level: 100
  islab: true
---

# Practice Lab – Configure a representative experience profile

## Scenario

As a customer service manager at Contoso Coffee, you need a consistent workspace experience for representatives who handle cases. In this lab, you create a guidance script and case session template, configure a representative experience profile, assign one user, and validate the resulting experience. This exercise should take approximately 30 minutes to complete.

> [!NOTE]
> The product interface uses labels such as **Agent scripts** and might still display **Agent experience profiles**. In this lab, *representative* refers to a person who handles customer service work; *agent* is retained only when it is part of a product label.

## Exercise 1 – Create supporting workspace components

### Task 1 – Create a representative guidance script

Before you begin, choose a unique prefix that contains three through eight alphanumeric characters. Use the same prefix wherever the lab asks for `<prefix>`. For example, if your name is Molly Clark, you might use `molclark`.

1. Use the app selector to open **Copilot Service admin center**.

1. Go to **Support experience** > **Productivity**.

1. In the **Scripts** section, select **Manage**.

1. Select **+ New**.

1. Enter the following values:

  - **Name**: `Script 1`
  - **Unique Name**: `<prefix>_script1`
  - **Language**: `English`
  - **Description**: `Guidance for representatives who open a case session.`

1. Select **Save**.

1. In the **Script steps** section, select **+ New script step**.

1. Enter the following values:

  - **Name**: `Step 1`
  - **Unique Name**: `<prefix>_step1`
  - **Order**: `1`
  - **Action type**: `Text`
  - **Text instructions**: `Hi, how can I help you today?`

1. Select **Save and Close**.

1. Select **Save** on the script record.

### Task 2 – Create a case session template

1. In Copilot Service admin center, go to **Support experience** > **Workspaces**.

1. In the **Session templates** section, select **Manage**.

1. On the **Active Session Templates** view, select **+ New**.

1. Enter the following values:

  - **Name**: `Entity Temp`
  - **Unique Name**: `<prefix>_et`
  - **Type**: `Entity`
  - **Entity**: `Case`
  - **Title**: `{casetitle}`
  - **Communication panel mode**: `Hidden`
  - **Description**: `Session template for Contoso Coffee cases.`

1. Select **Save**.

1. In **Additional Tabs**, select **Add Existing Application Tab Template**.

1. Search for and select **Customer Summary**, and then select **Add**.

1. Select the **Scripts** tab.

1. In the **Scripts** section, select **Add Existing script**.

1. Search for and select **Script 1**, and then select **Add**.

1. Select **Save**.

## Exercise 2 – Create and assign the experience profile

### Task 1 – Remove your existing experience profile assignment

A user can be assigned to only one experience profile at a time. Trial environments commonly assign the administrator to **Customer Service Trial profile**, so remove that assignment before creating and assigning the new profile.

1. Return to **Support experience** > **Workspaces**.

1. In the **Experience profiles** section, select **Manage**.

1. Select **Search by user**.

1. Search for and select your current user.

1. Select the **Assigned Experience Profile** link to open the assigned profile. It will probably be named **Customer Service Trial profile**.

1. In the **Users** section, select **Edit**.

1. Select the checkbox next to your user, and then select **Remove users**.

1. Close the **Edit Users** page, and then confirm that your user is no longer listed in the **Users** section.

### Task 2 – Create the experience profile

1. Return to **Support experience** > **Workspaces**.

1. In the **Experience profiles** section, select **Manage**.

1. Select **+ New**.

1. Enter the following values:

  - **Name**: `CS Temp`
  - **Unique name**: `<prefix>_CS`
  - **Description**: `Case workspace experience for Contoso Coffee representatives.`

1. Select **Create**.

1. On the profile page, select **Add entity session template**.

1. Select **Case** for the entity and **Entity Temp** for the session template.

1. Select **Add**.

### Task 3 – Configure the productivity pane

1. In the **Productivity pane** section of **CS Temp**, select **Turn on**.

1. Set **Productivity pane** to **On**.

1. Set **Default mode** to **Expanded**.

1. Set **Knowledge search** to **On**.

1. Set **Agent scripts** to **On**.

1. Select **Save and close**.

### Task 4 – Assign one user

1. In the **Users** section of **CS Temp**, select **+ Add users**.

1. Select your current user.

1. Select **Add**.

1. Confirm that your user is listed in the profile.

## Exercise 3 – Validate the representative experience

### Task 1 – Open a configured case session

1. Use the app selector to open **Copilot Service workspace**. Refresh the browser if the profile changes aren't visible immediately.

1. In the site map, select **Cases**.

1. Select the **My Active Cases** view, and then open **Coffee Brewer Still Not Heating After Reset**.

1. Confirm that a case session opens and its title uses the case title.

1. Confirm that **Customer Summary** opens as an additional application tab.

1. In the productivity pane, select **Knowledge search** and confirm that the search control opens.

1. Select **Agent scripts**.

1. Select **Script 1** if it isn't already selected.

1. Confirm that **Step 1** displays the instruction **Hi, how can I help you today?**
