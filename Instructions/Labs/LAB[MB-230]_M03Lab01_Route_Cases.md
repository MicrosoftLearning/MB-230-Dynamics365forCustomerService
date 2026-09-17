---
lab:
  title: 'Lab: Configure case routing'
  module: 'Module 3: Route and distribute work in Dynamics 365 Customer Service'
  description: As a customer service manager at Contoso Coffee, you configure email intake and unified routing for case records. You classify an existing problem case by its required skill, route it to an advanced queue, and verify its assignment to a qualified representative.
  duration: 60 minutes
  level: 100
  islab: true
---

# Practice Lab – Configure case routing

## Scenario

As a customer service manager at Contoso Coffee, you need predictable intake and routing for customer cases. In this lab, you configure an automatic record creation rule for high-priority email requests and set up unified routing for case records. You then classify an existing problem case by its required skill, route it to an advanced queue, and verify its assignment to a qualified representative. This exercise should take approximately 60 minutes to complete.

## Exercise 1 – Configure case intake

### Task 1 – Configure automatic case creation from email

In this task, you configure the deterministic intake rule but don't send an email. The lab doesn't require an approved, tested mailbox for the **Support** queue.

1. Use the app selector to open **Copilot Service admin center**.

1. Go to **Customer support** > **Case settings**.

1. In the **Automatic record creation and update rules** section, select **Manage**.

1. Select **New**.

1. Enter the following values:

  - **Rule name**: `Create case for support email`
  - **Activity type to monitor**: `Email`
  - **Queue to monitor**: `Support`

1. Select **Save**.

1. In **Step two: conditions to evaluate and actions to take**, select **New**.

1. Enter **High priority emails** for **Condition name**.

1. Select **Add row** and add the following condition:

  `Priority (Email)` **Equals** `High`

1. Select **Save and open Power Automate**.

> [!NOTE]
> If the flow opens in the new designer, turn off the **New designer** toggle to use the classic designer. The classic designer surfaces Customer Service fields and choices by their labels. The new designer might require underlying values, which are outside the scope of this Customer Service lab.

1. If prompted to configure a Dataverse connection, use the current connection and select **Continue**.

1. Expand the predefined **Create a record** step. Don't rename or delete the predefined trigger or **Create a record** step.

1. Set **Case Type** to **Request** and **Priority** to **High**.

1. Select **Save**, and then close the Power Automate browser tab.

1. Return to the rule item dialog, and then select **Save and Close**.

1. On the automatic record creation rule, select **Save**.

1. Select **Activate**, and then confirm the activation.

> [!NOTE]
> Don't enable an automatic reply or attempt an inbound email test. Those actions require an approved mailbox, server-side synchronization, and a working email address. You validate record routing with an existing case later in this lab.

## Exercise 2 – Prepare unified routing resources

### Task 1 – Confirm unified routing

Basic queues such as **Bronze**, **Silver**, and **Gold** support manual queue work and mailbox scenarios. Unified routing uses advanced queues, workstreams, classification rules, and assignment methods to distribute work to eligible representatives.

1. In Copilot Service admin center, go to **Customer support** > **Routing**.

1. In **Manage unified routing**, select **Manage**.

1. Confirm that **Unified routing** is set to **Yes**.

1. If unified routing is off, set it to **Yes**, select **Save**, and wait for enablement to finish before continuing.

  > [!IMPORTANT]
  > If the setting reports that required services aren't installed, stop this exercise and notify your instructor. Don't provision Contact Center or other channels to complete this lab.

### Task 2 – Create and assign a skill

In this task, you create a skill for complex product issues and assign it to your user. Unified routing can then compare the skill requirement attached to a case with your representative profile.

1. In Copilot Service admin center, go to **Customer support** > **User management**.

1. In the **Skills hub** section, select **Manage**.

1. In the **Skills** section, select **Manage**. The **Active Characteristics** page opens.

1. Select **New**.

1. Enter **Coffee brewer troubleshooting** for **Skill name**.

1. Select **Skill** for **Type**.

1. Select **Save**.

1. In the **Users (Agents)** section, select **New Bookable Resource Characteristic**.

1. In the **Quick Create: Bookable Resource Characteristic** pane, select **5 (Excellent)** for **Rating Value**.

1. Select your user for **User (Agent)**. (Your user will probably be named **Trial User.**)

1. Select **Save and Close**, and then confirm that your user appears in the **Users (Agents)** section.

### Task 3 – Create an advanced queue

In this task, you create a record queue for Gold-level cases and use capacity-aware assignment. The assignment method considers queue membership, presence, available capacity, and required skills when it selects a representative.

1. Go to **Customer support** > **Queues**.

1. In the **Advanced queues** section, select **Manage**.

1. Select **New queue**.

1. Enter the following values:

  - **Name**: `Gold - Unified Routing`
  - **Type**: `Record`
  - **Queue priority**: `1`
  - **Description**: `Routes complex coffee brewer cases to representatives with troubleshooting expertise.`

1. Select **Create**.

1. Select **Add users**.

1. Select your current user (it may be called **MOD Administrator** here), and then select **Add**.

1. Confirm that your user is listed for the queue.

1. For **Assignment method**, confirm that **Highest capacity** is configured.

## Exercise 3 – Configure classification, routing, and assignment

### Task 1 – Create a record workstream and intake rule

In this task, you create a case workstream in **Push** mode. After classification and queue routing, unified routing automatically assigns a work item to an eligible representative.

1. In Copilot Service admin center, go to **Customer support** > **Routing**.

1. In the **Set up record routing** section, select **Manage**.

1. Confirm that **Case** is listed as a record type.

1. If **Case** isn't listed, select **Add**, select **Case** for **Record type**, and then select **Add**.

1. Go to **Customer support** > **Workstreams**.

1. Select **New workstream**.

1. Select **Inbound** and select **Next.**

1. Enter the following values:

  - **Name**: `Contoso Coffee cases`
  - **Type**: `Record`
  - **Record type**: `Case`
  - **Work distribution mode**: `Push`

1. For **Fallback queue**, select **Choose existing**, and then select **Default entity queue**.

1. Select **Create**. (It may take a minute or so for the workstream to be created.)

1. In the **Work distribution** section, select **See more**.

1. Enter `1` for **Unit-based capacity**.

1. For **Allowed presences**, select **Available** only.

1. For **Default skill matching algorithm**, select **Exact Match**.

1. Select **Save and close**.

1. In the **Intake rules** section of the workstream, select **Create rule**.

1. Enter **Active cases** for **Rule name**.

1. Add the following condition by selecting **Add row**:

  `Status` **Equals** `Active`

1. Under **Map to**, select **Workstream**, and then select **Contoso Coffee cases** for **Workstream**.

1. Select **Create**.

### Task 2 – Classify problem cases by required skill

In this task, you create a logical classification rule. When a problem case enters the workstream, the rule attaches the **Coffee brewer troubleshooting** skill before queue routing and assignment occur.

1. In **Contoso Coffee cases**, locate the **Routing rules** section.

1. Next to **Work classification**, select **Create ruleset**.

1. Select **Create new**.

1. Select **Logical rules** for **Rule type**.

1. Enter **Case skill classification** for the name and **Assigns coffee brewer troubleshooting expertise to problem cases.** for the description.

1. Select **Create**.

1. In the **Decision list**, select **Create Rule**.

1. Enter **Coffee brewer troubleshooting for problem cases** for **Rule Name**.

1. Add the following conditions below the existing condition by selecting **+Add** and **Add row**: 

  `Case Type` **Equals** `Problem`

  `Product` **Equals** `Contoso Coffee Pro 100 Brewer`

1. In **Output**, enter the following values:

  - **Attribute**: `Skills`
  - **Operator**: `Set to`
  - **Value**: `Coffee brewer troubleshooting`
  - **Proficiency**: `Excellent`

1. Select **Create**.

1. Confirm that the rule appears in **Case skill classification**.

### Task 3 – Configure the route-to-queue rule

In this task, you route problem cases to the advanced Gold queue. Queue assignment then evaluates the skill attached during classification together with representative presence and capacity.

1. In **Contoso Coffee cases**, locate the **Routing rules** section.

1. Next to **Route to queues**, select **Create ruleset**.

1. Enter **Case queue routing** for the ruleset name, and then select **Create**.

1. In the **Decision list**, select **Create Rule**.

1. Enter **Problem cases to Gold** for **Rule Name**.

1. Below the existing condition, select **+Add** and **Add row** to add a new condition.

1. Add the following condition:

  `Case Type` **Equals** `Problem`

1. Under **Route to queues**, select **Gold - Unified Routing**.

1. Select **Create**.

1. Confirm that the rule is listed in the ruleset and that **Gold - Unified Routing** is the destination queue.

## Exercise 4 – Route and verify a case

### Task 1 – Route the existing problem case

1. Allow several minutes for the routing configuration to propagate.

1. Use the app selector to open **Copilot Service workspace**.

1. Set your presence to **Available**.

1. In the site map, select **Cases**.

1. Select the **My Active Cases** view, and then open **Coffee Brewer Still Not Heating After Reset**.

1. On the **Details** tab, confirm that **Type** is **Problem** and **Status** is **Active**.

1. On the command bar, select **Save and route**. You might need to select **More commands** (...) to find the action.

1. Confirm the routing action if prompted.

1. Wait for unified routing to process the case, and then refresh the page.

1. Select **Queue Item Details**.

1. Confirm that the case is in **Gold - Unified Routing** and is assigned to your user.

1. In the site map, select **Queues**.

1. Select the **Queues I'm a member of** view, and then select **Gold - Unified Routing**.

1. Confirm that **Coffee Brewer Still Not Heating After Reset** appears as a queue item and that **Worked By** shows your user.

If the case doesn't route after the configuration has propagated, verify these settings in Copilot Service admin center:

- The **Active cases** intake rule maps active cases to **Contoso Coffee cases**.
- The **Coffee brewer troubleshooting for problem cases** classification rule attaches **Coffee brewer troubleshooting**.
- The **Problem cases to Gold** rule tests **Case Type Equals Problem**.
- **Gold - Unified Routing** is a **Record** queue and includes your user.
- The case is active and its **Type** is **Problem**.

If the case reaches the queue but isn't assigned, confirm that:

- Your presence is **Available**.
- Your user has the **Coffee brewer troubleshooting** skill at the required proficiency.
- The workstream uses **Exact Match**, allows the **Available** presence, and requires one unit of capacity.
- **Gold - Unified Routing** uses the **Highest capacity** assignment method.
- Your user has enough available capacity for the work item.

