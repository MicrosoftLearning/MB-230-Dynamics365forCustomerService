In this lab, you will be configuring the Dynamics 365 productivity tools so
Agents can take advantage of the Agent script feature. You will be creating four
items that will make up the agent script solution.

These items are:

-   A macro that will assist agents in creating a new case while they are
    working on an item.

-   A macro that will be leveraged to close the case.

-   A general agent script that provides some simple instructions to agents.

-   A closing script that will assist the agent in closing issues.

### **Learning Objectives**

After completing the exercises in this lab, you will be able to:

-   Create macros that can be leverage in agent scripts

-   Create agent scripts to assist agents

-   Configure script, text, and macro, script steps in a script

-   Enable the productivity pane for agents to leverage scripts

### Estimated time to complete this lab: 30 minutes

# Exercise 1: Create a Macro that will be leveraged in an Agent Script

## Task 1: Build the Create Case Macro 
-----------------------------------------

1.  Sign in to the Omnichannel Administration app.

2.  Under **Agent Experience**, select **Macro**.

3.  On the **Active Macros** page, select **+ New**.

4.  On the Macro page, specify the following:

    -   **Name:** Your lab username - Create Case and Link to Conversation

    -   **Description:** This macro action is used to create a case and link the
        record to the conversation.

5.  Under **Predefined Automation Actions**, select **Productivity Automation**.

6.  Select **Start macro execution**. *A trigger will be added, and you will not
    need to provide any additional details.*

7.  Under the **Start macro execution** trigger, select the **+ New Step**
    button.

8.  Under **Predefined automation actions**, select **Session Connector**.

9.  Select **get the current tab**. *You will not need to provide any additional
    details.*

10. Select the **+ New Step** button.

11. Under **Predefined automation actions**, select **Productivity Automation**.

12. Select **Open a new form to create a record**.

13. In the **Entity logical name**, enter **incident**.

14. Select **show advanced options**.

15. Set **Attribute Name – 1** to **title**, and **Set Attribute Value -1** to
    **Broken Item**

16. Select the **Add new item** button again.

17. Set **Attribute Name – 2** to **customerid, Set Attribute Value -2** to
    **{customerRecordId}**

18. Repeat steps **16 & 17** to add the following additional attributes:

| Attribute Name | Attribute Value               |
|----------------|-------------------------------|
| Customeridtype | \${customerEntityName}        |
| Customeridname | \${\$Session.customerName}    |
| Description    | Customers item is not working |

19. Once completed, your **open new form and create case record** step, should
    resemble the image below:

20. Select the **+ New Step** button.

21. Under **Predefined automation actions**, select **Productivity Automation**.

22. Select **Save the record**.

23. Select the **+ New Step** button again.

24. Under **Predefined automation actions**, select **Omnichannel Connector**.

25. Select **Link record to the conversation**.

26. Select the **Entity logical name** field, in the Dynamic content window,
    select **Entity logical name** from the **Save the Record** step.

27. Set **Entity record ID** to the **Entity record ID** from the **Save the
    Record step**.

28. Set **Entity record ID** to the **Entity record ID** from the **Save the
    Record step**.

29. Your completed step should resemble the image below:

30. Select the **+ New Step** button.

31. Under **Predefined automation actions**, select **Session Connector**.

32. Chose **Focus on the tab**

33. Set the **Tab ID** to the **Tab ID** from the **Get the current tab step.**

34. Your completed macro should look like the image below:

35. Scroll to the bottom of the screen and select the **Save and Close** button

## Task 2: Build the Resolve Case Macro
------------------------------------------

1.  Under **Agent Experience**, select **Macro**.

2.  On the **Active Macros** page, select **+ New**.

3.  On the Macro page, specify the following:

    -   **Name:** Yourlabusername – Resolve current case

    -   **Description:** This macro action is used to resolve the case you
        opened.

4.  Under **Predefined Automation Actions**, select **Productivity Automation**.

5.  Select **Start macro execution**. *A trigger will be added, and you will not
    need to provide any additional details.*

6.  Under the **Start macro execution** trigger, select the **+ New Step**
    button.

7.  Under **Predefined automation actions**, select **Productivity Automation**.

8.  Select **Resolve case**

9.  Complete the action step as follows:

    -   **Billable time:** 0

    -   **Incident ID:** {caseId}

    -   **Resolution:** KBArticle

# Exercise 2: Build an Agent Script to assist agents

## Task 1: Build the Closing session Script 
---------------------------------------------

1.  If you are not already logged in from the previous exercise, sign in to the
    Omnichannel Administration app.

2.  Under **Agent Experience**, select **Agent Scripts**.

3.  On the **Active Agent scripts** page, select **+ New**.

4.  On the **New Agent script** page, specify the following:

    -   **Name:** Yourlabusername Closing Script (ex. Alan Script)

    -   **Description:** Created by yourlabusername to be used by agents when
        closing a case.

5.  Select **Save** to save the script. The **Agent script steps** appears.

6.  In the **Agent script steps** section, select **+ New Agent script step**. 

7.  Complete the Agent script step as follows:

    -   **Name:** Resolve Case

    -   **Agent Script:** Yourlabusername script

    -   **Order:** 1

    -   **Action Type:** Macro

    -   **Description:** Greet the customer with the welcome message from the
        quick reply repository.

    -   Target macro: Yourlabusername – Resolve Case

8.  Select **Save and Close**.

9.  Select **+ New Agent script step** button again. 

10. Complete the Agent script step as follows:

    -   **Name:** Have a Nice Day!

    -   **Agent Script:** Yourlabusername Closing script

    -   **Order:** 2

    -   **Action Type:** Text

    -   **Text Instructions:** Ask the customer is there is anything you can
        assist them with. If not, thank them for their time and end the call.

11. Select **Save and Close**.

12. Close the Closing Script Record

## Task 2: Build the General Script 
-------------------------------------

1.  Under **Agent Experience**, select **Agent Scripts**.

2.  On the **Active Agent scripts** page, select **+ New**.

3.  On the **New Agent script** page, specify the following:

    -   **Name:** Yourlabusername Script (ex. Alan Script)

    -   **Description:** Created by yourlabusername to be used by agents working
        on sessions.

4.  Select **Save** to save the script. The **Agent script steps** appears.

5.  In the **Agent script steps** section, select **+ New Agent script step**. 

6.  Complete the Agent script step as follows:

    -   **Name:** Greet the Customer

    -   **Agent Script:** Yourlabusername script

    -   **Order:** 1

    -   **Action Type:** Text

    -   **Text Instructions:** Greet the customer with the welcome message from
        the quick reply repository.

7.  Select **Save and Close**.

8.  In the **Agent script steps** section, select **+ New Agent script step**
    button again. 

9.  Complete the Agent script step as follows:

    -   **Name:** Open a New Case

    -   **Agent Script:** Yourlabusername script

    -   **Order:** 2

    -   **Action Type:** Macro

    -   **Description:** This will automatically create a new case for the
        existing customer and link it to the current conversation.

    -   **Target Macro:** Create Case and Link to Conversation

10. Select **Save and Close**.

11. Select **+ New Agent script step** button again. 

12. Complete the Agent script step as follows:

    -   **Name:** Search for relevant KB article.

    -   **Agent Script:** Yourlabusername script

    -   **Order:** 3

    -   **Action Type:** Text

    -   **Text instructions:** Use Knowledgebase to look for a relevant
        knowledge article that might resolve the issue.

13. Select **Save and Close**.

14. Select **+ New Agent script step** button again. 

15. Complete the Agent script step as follows:

    -   **Name:** Proceed to Closing

    -   **Agent Script:** Yourlabusername script

    -   **Order:** 4

    -   **Action Type:** Script

    -   **Description:** Starts the process of wrapping up the conversation with
        the customer.

    -   **Target Script:** Yourlabusername Closing Script

16. Select **Save and Close**.

17. Close the **Closing Script** record

# Exercise 3: Configure OCS to use the Agent Script

## Task 1: Attach the script to SMS-Sessions 
-----------------------------------------------

1.  Under **Agent Experience**, select **Sessions**.

2.  Locate and open the **SMS – Default session**.

3.  Select the **Agent Scripts** tab

4.  In the Agent Scripts Sub Grid, Select the add Existing Agent Script Button.

5.  Select the **Yourlabusername** script, and click **Add**

## Task 2: Enable the productivity pane to allow agents to leverage agent scripts 
------------------------------------------------------------------------------------

1.  Under **Agent Experience**, select **Productivity pane**.

2.  Set **Enable productivity pane** to **Enabled**.

3.  Leave the **Default mode** set to **Collapsed**.
