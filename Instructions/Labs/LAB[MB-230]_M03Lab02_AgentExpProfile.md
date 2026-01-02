---
lab:
    title: 'Lab: Agent experience profiles'
    module: 'Module 3: Customer Service workspaces'
---

# Practice Lab – Agent experience profiles

## Scenario

You are a customer service manager at City Power & Light who has been tasked with configuring the agent experience profiles for Customer Service workspace. In this lab, you will configure a new profile.

## Exercise 1 – Create an agent experience profile

In this exercise you will learn how to create an agent experience profile in the Customer Service admin center.

### Task 1 – Manage agent experience profiles

1.  Open the **Customer Service admin center** app. If you are in the Customer Service Workspace or Customer Service hub applications, click on the name of the app in the top left of the application next to Dynamics 365 and from the list of published apps, select the **Customer Service admin center** app.

2. In the Agent Experience section, click on **Workspaces.**

3.  On the **Workspaces** page, navigate to the **Agent experience profiles** area.

4.  Click **Manage** in the Agent experience profiles area.

5.  Click on **+ New**

6.  Enter **CS Temp** for **Name**, **[your prefix ex. mollyc]** + **_ CS** (without the space) for **Unique Name**. 
    - Please be aware that your unique name must follow the specificatons outlined under the text box. If your Unique Name is longer than 8 characters or contains anything other than alphanumeric characters, change it to comply with the requirements. Otherwise you will recieve an error. 

7. Select **Create.**

8. Click **+Add entity session template** and click **+Create entity session template.**
    - For **Name**, enter **Entity Temp**.
    - For **Unique Name**, enter **[your prefix ex. mollyc] _ ET** (without the space).
    - Select **Entity** for **Type**.
    - Select **Case** for **Entity**.
    - Enter **{casetitle}** for **Title**.
    - Select **Docked** for **Communication panel mode**.

7.  Click **Save**.

8.  In **Additional Tabs**, click **Add Existing Application Tab Template**.

9.  Select the **Search** button to expand the dropdown list and select **Customer Summary.** Select **Add.**

10. Select the **Agent scripts** tab and click **Add Existing Agent script**.

11. Click **+ New Record**, select **Agent scripts** and click **OK**.

12. Enter **Script 1** for **Name** and **[your prefix ex. mollyc] _ script1** (without the spaces) for **Unique Name**.

13. Click **Save**.

14. In **Agent script steps**, click **+New Agent script step**.

15. Enter **Step 1** for **Name**, **[your prefix ex. mollyc] _ step1** for **Unique Name** (without the spaces), enter **1** for **Order**, select **Text** for **Action Type**, and enter **Hi, how can I help you today?**

16. Click **Save & Close**.

17. You should return to the session template titled **Entity Temp.**

18. Select the **Agent scripts** tab (if it is not already open) and click **Add Existing Agent script**.

19. Select the agent script you just created and click **Add**.

20. Select **Save and close.**

21. You should return to the **Entity session templates** screen on your **Agent experience profile.** Select **+Add.**

22. Select **Case** for Entity and select your **Entity Temp** template for Session template.

23. Select **Add**. Select **Save and close.**

### Task 2 – Configure the productivity pane 

1. On your agent experience profile, select **Turn on** in the Productivity pane section.

2. Toggle **Productivity pane** to **On.**

3. Toggle **Default mode** to **Expanded.**

4. Toggle **Smart assist** to **On**.

5. Toggle **Agent scripts** to **On**.

6. Select **Save and close.**

### Task 3 – Assign users to the agent experience profile

1. On your agent experience profile, select **+Add user** in the Users section.

2. Select One user from the list.

3.  Select **Add.**

## Exercise 2 – Test the agent experience profile

In this exercise you will test the agent experience profile you created.

### Task 1 – Open the Customer Service workspace

1.  Open the **Customer Service workspace** app. If you are in the Customer Service admin center, click on the name of the app in the top left of the application next to Dynamics 365 and from the list of published apps, select the **Customer Service workspace**.

2.  In the Customer Service Agent Dashboard, find the **Defective Screen** case, and click on the case to open it.

3.  A new session starts in the left-hand pane for the case and **Smart assist** opens in the **Productivity pane** and a **Customer Summary** tab is available. Explore the Smart assist.

5.  Click on the **Agent script** icon. You should see the script to created earlier in this lab.
