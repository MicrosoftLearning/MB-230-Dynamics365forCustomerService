---
lab:
    title: 'Lab: App profile manager'
    module: 'Module 6: Customer Service workspace'
---

# Practice Lab 11 – App profiles

## Scenario

You are a customer service manager at City Power & Light who has been tasked with configuring the app profile for Customer Service workspace . In this lab, you will configure a new profile.

## Exercise 1 – Create an app profile

In this exercise you will learn how to navigate the App profile manager, create a profile and templates.

### Task 1 – Open the App profile manager

1.  Open the **Customer Service admin center** app. If you are in the Customer Service Workspace or Customer Service hub applications, click on the name of the app in the top left of the application next to Dynamics 365 and from the list of published apps, select the **Customer Service admin center** app.

2. In the Agent Experience section, click on **Workspaces.**

3.  On the **Workspaces** page, navigate to the **Agent experience profiles** area.

4.  Click **Manage** in the Agent experience profiles area.

5.  Click on **+ New**

6.  Enter **[your prefix ex. mollyc]** + **CS Temp** for **Name**, **[your prefix ex. mollyc]** + **_ c** (without the space) for **Unique Name**. Select **Entity** for **Type**, select **Case** for **Entity**, enter **{casetitle}** for **Title**, select **Docked** for **Communication panel mode**.
    - Please be aware that your unique name must follow the specificatons outlined under the text box. If your Unique Name is longer than 8 characters or contains anything other than alphanumeric characters, change it to comply with the requirements. Otherwise you will recieve an error. 

7.  Click **Save**.

8.  In **Additional Tabs**, click **Add Existing Application Tab Template**.

9.  Select **Customer Summary** and **Search** and click **Add**.

10. Select the **Agent scripts** tab and click **Add Existing Agent script**.

11. Click **+ New Record**, select **Agent scripts** and click *OK**

12. Enter **[your prefix ex. mollyc]** + **Script 1** for **Name**, **[your prefix ex. mollyc]** +**_script1** for **Unique Name**,

13. Click **Save**.

14. In **Agent script steps**, click **+New Agent script step**.

15. Enter **[your prefix ex. mollyc]** + **Step 1** for **Name**, **[your prefix ex. mollyc]** +**_step1** for **Unique Name**, enter **1** for **Order**, select **Text** for **Action Type**, and enter **Hi, how can I help you today?**

16. Click **Save & Close**.

17. Click **Save & Close**. You should return to the session template you created.

18. Select the **Agent scripts** tab and click **Add Existing Agent script**.

19. Select the agent script you just created and click **Add**

### Task 3 – Create an app profile

1.  Navigate to the Power Apps Maker portal <https://make.powerapps.com>.

2.  Select the **WWLLABnnn** Dynamics 365 environment.

3.  Click on **Apps**.

4.  Click on the ellipsis (...) in the **Customer Service workspace** app and select **App profile manager**.

5.  Click App profiles.

6.  Click **+New profile**.

7.  Enter **[your prefix ex. mollyc]** + **app profile** for **Name**, **[your prefix ex. mollyc]** +**_profile** for **Unique Name**

8.  Click **Save**.

9.  Open the profile you just created.

10. Select the **Session templates** tab.

11. Search for and select the **Case Session** template you created earlier in this lab.

12. Select the **Productivity pane** tab.

13. Toggle **Turn on Productivity pane** to **On**.

14. Toggle **Default mode** to **Expanded**.

15. Toggle **Smart assist** to **On**.

16. Toggle **Agent scripts** to **On**.

### Task 4 – Assign users to the app profile

1.  Navigate to the Power Apps Maker portal <https://make.powerapps.com>.

2.  Select the **WWLLABnnn** Dynamics 365 environment.

3.  Click on **Apps**.

4.  Click on the ellipsis (...) in the **Customer Service workspace** app and select **App profile manager**.

5.  Click App profiles.

6.  Click on the profile you created earlier in this lab.

7.  Click **Assign users**.

8.  Click **OK**.

9.  Click **+ Add users**

10. Search for and select your user and click on **Add**

## Exercise 2 – Test the app profile

In this exercise you will test the app profile you created.

### Task 1 – Open the Customer Service workspace

1.  Open the **Customer Service workspace** app. If you are in the Customer Service hub, click on the name of the app in the top left of the application next to Dynamics 365 and from the list of published apps, select the **Customer Service workspace**.

2.  In the Customer Service Agent Dashboard, find the **Defective Screen** case, and click on the case to open it.

3.  A new session starts in the left-hand pane for the case and **Smart assist** opens in the **Productivity pane**. The Agent script is available but the knowledge search is missing. There are three tabs, one for the case, another for **Search**, and another for the **Customer summary**.

4.  Click on the **Search** tab.

5.  Click on the **Agent script** icon. You should see the script to created earlier in this lab.

6.  Expand the script and **Mark as done**
