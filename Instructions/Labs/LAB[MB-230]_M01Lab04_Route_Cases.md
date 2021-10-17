---
lab:
    title: 'Lab: Routing cases'
    module: 'Module 1: Case Management'
---

# Practice Lab 4 – Routing cases

## Scenario

You are a customer service manager at City Power & Light who has been tasked with trying the new case routing functionality before rolling it out to your users. In this lab, you will create record creation rules, and case routing rules and test how they work.

## Exercise 1 – Configure record creation rules

### Task 1 – Enable a case to be created from an email in a queue

1.  Open the **Customer Service Hub** app.

2.  Click on **Service** at the bottom of the **Site Map** in the left-hand navigation and select **Service Management**.

2.  Click on **Automatic record creation and update rules** in the **Case Settings** section.

4.  Click **+ New** located on the command bar.

5.  Enter **[your prefix ex. mollyc]** + **Create case for suppport email** for **Rule name**, select the **Support** queue you created, and select **Email** for **Activity type to monitor**.

6.  Click **Save**.

7.  In **Step two: conditions to evaluate and actions to take**, click **+ New**.

8.  Enter **High priority emails** for **Condition name**.

9.  Click on **Add** and **Add row** .

10. In the left-hand side of the condition, select **Priority (Email)**

11. Select **Equals** for the operator.

12. In the right-hand side of the condition, select **High**.

13. Click **Save and open Power Automate**.

14. If prompted to connect to Dataverse, click **Continue**.

15. Expand the **Create a record (don't rename this step)** step.

16. Set the **Case Type** to **Request**.

17. Set the **Priority field** to **High**.

18. Click **Save** and close the Power Automate browser tab.

19. Click **Close** in the *Record Creation and Update Rule Item* dialog.

20. In **Step two: conditions to evaluate and actions to take**, set *Automatically reply to email*  to **Yes**.

21. In *Select email template*, search for and select **Case Auto Response**.

22. Click **Save**.

23. Click **Activate**.

24. Click **Activate**.

25. Due to the lack of administrative access to email mailboxes, you will not be able to test this rule.

## Exercise 2 – Basic routing

### Task 1 – Configure basic routing rule set

1.  Open the **Customer Service Hub** app.

2.  Click on **Home** at the top of the left-hand side navigation.

3.  Click on **Service** at the bottom of the **Site Map** in the left-hand navigation and select **Service Management**.

4.  Click on **Routing Rule Sets** in the **Case Settings** section.

5.  Click **+ New** located on the command bar.

6.  Enter **[your prefix ex. mollyc]** + **basic case routing rules** for **Name**.

7.  Click **Save**.

8.  Click **+ New Rule Item**.

9.  Enter **Problem** for **Name**.

10. Click on **Add** and **Add row**.

11. In the left-hand side of the condition, select **Case Type (Case)**.

12. Select **Equals** for the operator.

13. In the right-hand side of the condition, select **Problem**.

14. Select **Queue** for **Route To**.

15. Search for and select the **Gold** queue you created in the earlier lab.

16. Click **Save & Close**.

17. Click **+ New Rule Item**.

18. Enter **Maintenance** for **Name**.

19. Click on **Add** and **Add row**.

20. In the left-hand side of the condition, select **Subject (Case)**.

21. Select **Equals** for the operator.

22. In the right-hand side of the condition, select **Maintenance**.

23. Select **Queue** for **Route To**.

24. Search for and select the **Silver** queue you created in the earlier lab.

25. Click **Save & Close**.

26. Click **+ New Rule Item**.

27. Enter **Questions and Requests** for **Name**.

28. Click on **Add** and **Add row**.

29. In the left-hand side of the condition, select **Case Type (Case)**.

30. Select **Equals** for the operator.

31. In the right-hand side of the condition, select **Question** and select **Request**.

32. Select **Queue** for **Route To**.

33. Search for and select the **Bronze** queue you created in the earlier lab.

34. Click **Save & Close**.

35. Click **Save**.

36. Click **Activate** and click **Yes**.

## Exercise 3 – Route cases

### Task 1 – Route cases

1.  Open the **Customer Service Hub** app.

2.  Click on **Home** at the top of the left-hand side navigation.

3.  Click on **Cases** in the **Service** section of the sitemap.

4.  Enter *your prefix ex. mollyc* in the **Search this view** field, click on the lookup icon.

5.  Open the **Defective Screen** case you created.

6.  Click **Queue Item Details** located on the command bar.

7.  The following message should be displayed *This record is not added to any queue.*

8.  Click **OK**.

9.  Click **Save & Route** and click **Route**.

10. Open the **Defective Screen** case again.

11. Click **Queue Item Details** located on the command bar.

12. The case will be have been routed to the *Gold* queue.

13. In the case view, click to the left of the **Service Required** case to select it.

14. Click **Apply Routing Rule** and click **Route**.

15. Open the **Service Required** case.

16. The case will be have been routed to the *Silver* queue.

