---
lab:
    title: 'Lab 3: Agent collaboration'
    module: 'Module 6: Customer Service workspace'
---

# Practice Lab - Agent collaboration

## Scenario 

Your organization provides billing and customer support on the Circuit Boards
and other electronic products that it manufactures. With more and more new
agents coming on board, your organization is looking for more ways to help newer
agents solve customer problems faster. One way that they have identified how to
do this is by providing more collaboration options for their agents. Since they
use Microsoft Teams, they have decided to leverage the collaboration
capabilities available between Microsoft Teams and Dynamics 365.

Throughout this lab, you will configure the different collaboration features
available. Upon successful completion of the lab, you will have performed the
following:

-   Enabled the Embedded Teams Collaboration features

-   Enabled the Case Swarming Feature

-   Configured the Case Swarming Capabilities.

## Exercise 1: Enable the necessary collaboration features in your environment 

Before your agents can begin collaborating subject matter experts at your
organization, you will need to ensure that you have enabled the necessary
features in your environment.

### Task 1: Enable collaboration features**

1.  Open the **Customer Service admin center** application.

2.  Using the navigation on the left, select **Collaboration**.

3.  Select **Manage** next to **Embedded chat using Teams**.

4.  Set the following Items to **On**

    -   Turn on the linking of Dynamics 365 records to Microsoft Teams channels

    -   Turn on Microsoft Teams chats inside Dynamics 365

5.  Select the **Save** button

6.  Using the navigation on the left, select Collaboration again.

7.  Select **Manage** next to **Customer support swarming**.

8.  On the **Customer support swarming** screen, ensure that Swarming is set to
    **On**.

9.  Under the **Case details** section, select **Activate case form for
    swarming**.

10. From the list of available case forms, locate the **Case form for
    swarming**.

    -   If the status of the form is set to **On**, you can close the browser
        tab to return to the Customer support swarming screen.

    -   If the status of the form is set to **Off,** select the **vertical
        ellipsis** next to the from name, and from the menu that appears, select
        **Turn On**. Once turned on, you can close the browser tab to return to
        the Customer support swarming screen.

### Task 2: Create bookable resource records that can be used as experts.

1.  In the **Customer Service Admin Center** application, use the navigation on
    the left to select **Service scheduling**.

2.  Locate **Resources**, and select **Manage**.

3.  From the **Active Bookable Resources** screen, select the **New Button**
    from the command bar.

4.  Configure the new Bookable resource as follows:

    1.  **Resource Type:** User

    2.  **Contact:** Alan Steiner.

5.  Leave everything else as is and select the **Save and Close** button.

6.  Select the **New** button from the command bar again.

7.  Configure the new Bookable resource as follows:

    1.  **Resource Type:** User

    2.  **Contact:** Allie Bellew

8.  Leave everything else as is and select the **Save and Close** button.

## Exercise 2: Configure Case Swarming

Now that we have enabled the necessary features and have defined the resources
that will be used as part of our solution, we are now going to configure the
Case Swarming capabilities in the application. This will consist of two primary
tasks:

-   Defining Skills & assigning those Skills to Experts

-   Defining Condition rules to assign Skills to swarming requests


### Task 1: Configure skills

1.  If necessary, open the **Customer Service Admin** center.

2.  Using the navigation on the left, select the **Collaboration**.

3.  Next to **Customer support swarming**, select the **Manage** button.

4.  Under the **Skills** section. Select **Go to Skills**.

5.  On the **Active Characteristics** screen, select the **New** button from the
    command bar.

6.  Configure the Characteristic as follows:

    -   **Name:** Billing

    -   **Type:** Skill

    -   **Description:** Expert for Billing questions

7.  Select the **Save** button to save the record and leave it open.

8.  Select the **Related** tab.

9.  From the menu that appears, select **Bookable Resource Characteristics**.
    This will open the **Bookable Resource Characteri**stics tab.

10. Select the **New Bookable Resource Characteristic** button.

11. Configure the **Bookable Resource Characteristic** as follows:

    -   **Skill Name:** Billing

    -   **User (Agent):** Alan Steiner

12. Select **Save and Close**

13. Select the **New Bookable Resource Characteristic** button again.

14. Configure the **Bookable Resource Characteristic** as follows:

    1.  **Skill Name:** Billing

    2.  **User (Agent):** Allie Bellew

15. Select **Save and Close**

16. Select **Save and Close** to close the **Billing** skill.

17. Back on the **Active Characteristics** screen, select the **New** button
    from the command bar.

18. Configure the Characteristic as follows:

    1.  **Name:** Circuit Board Expert

    2.  **Type:** Skill

    3.  **Description:** Expert in repairing Circuit boards

19. Select the **Save** button to save the record and leave it open.

20. Select the **Related** tab.

21. From the menu that appears, select **Bookable Resource Characteristics**.
    This will open the **Bookable Resource Characteristics** tab.

22. Select the **New Bookable Resource Characteristic** button.

23. Configure the Bookable Resource Characteristic as follows:

    1.  **Skill Name:** Circuit Board Expert

    2.  **User (Agent):** Alan Steiner

24. Select **Save and Close**

25. Select the **New Bookable Resource Characteristic** button again.

26. Configure the Bookable Resource Characteristic as follows:

    1.  **Skill Name:** Circuit Board Expert

    2.  **User (Agent):** Allie Bellew

27. Select **Save and Close**

28. Select **Save and Close** to close the Circuit Board Expert skill

### Task 2: Create Condition rules to assign necessary skills**

1.  Using the navigation on the left, select the **Collaboration**.

2.  Under the **Condition Rules** section, select the **Create Rule** button

3.  In the **Rule Name** field, enter **Billing rule.**

4.  Configure the conditions section as follows:

    1.  **Swarm request** – **Contains** – **Billing**

    2.  Delete the Swarm related record condition.

5.  In the **Skills** section, select the **Lookup** Icon.

6.  In the **Lookup Records** box, select the **Look for Characteristic** field.

7.  Enter the text **Billing**.

8.  Select the **Billing** skill.

9.  Select the **Add** button.

10. Back on the **Create swarm rule** screen, select the **Create** button.

11. In the **Condition rules** section select the **See more** icon.

12. In the **Decision List** screen, select the **Create Rule** button.

13. In the **Rule Name** field, enter **Circuit Board Rule**.

14. Configure the conditions as follows:

    1.  **Swarm request** – **Contains** – **Circuit Board**

    2.  Delete the Swarm related record condition.

15. In the **Skills** section, select the **Lookup** Icon.

16. In the **Lookup Records** box, select the **Look for Characteristic** field.

17. Enter the text **Circuit**.

18. Select the **Circuit Board Expert** skill.

19. Select the **Add** button.

20. Back on the **Create swarm rule** screen, select the **Create button**.

## Exercise 3: Leverage the different collaboration features 

### Task 1: Initiate an embedded Teams Chat

1.  Open the **Customer Service Workspace** application.

2.  One the **Customer Service Agent Dashboard**, select the **New Case** button
    on the **My Active Case**s sub-grid.

3.  In the **Quick Create Case** screen, configure the new case record as
    follows.

    -   **Customer:** Adventure Works

    -   **Case Title:** Circuit Board Damaged

    -   **Case Type:** Problem

    -   **Case Status:** In Progress

    -   **Priority:** Normal

4.  Select the **Save and Close** button.

5.  In the **My Active Cases** sub-grid, select the **Search** this view field.

6.  Enter the text Circuit and press the enter key.

7.  Open the **Circuit Board Damaged** case.

8.  On the right side of the screen, in the **Productivity Pane**, select the
    **Microsoft Teams** icon.

9.  Select the **Start a New Chat** button.

10. In the **Name** field, select **Molly Clarke**.

11. Enter the Message you want to send to Molly.

### Task 2: Create a Case Swarm

Another way you can locate help is to initiate a swarm request. When initiating
a case swarm the system will identify multiple Experts you could potentially
assist you in resolving your issue.

1.  On the **Case** record select the **Create Swarm** button. (*You may need to
    select the vertical Ellipsis to display more options*.)

2.  In the **Swarm Request**, enter the text **Having a Billing Issue**.

3.  In the **Steps already tried** field, enter **Tried issuing a credit.**

4.  Notice that the **Billing** skill has already been added to the skills.

5.  Click in the **Enter more skills** field, and select **Circuit Board
    Expert**.

6.  Select the **Save and Send** invitation button.

7.  After a short period of time, a new **Swarm** will appear. You can enter
    text into the message section.


