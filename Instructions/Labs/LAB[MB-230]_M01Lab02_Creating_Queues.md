---
lab:
    title: 'Lab: Creating queues'
    module: 'Module 1: Case Management'
---

# Practice Lab – Queues

## Scenario

You are a customer service manager at City Power & Light. You need to create queues for the customer service representatives to use for processing cases. In this lab, you will create a create multiple queues and add cases to activities to queues.

## Exercise 1 – Create Queues

In this exercise, you will create four queues.

### Task 1 – Create Queues

1.  Open the **Customer Service admin center** app.

2.  Click on **Queues** in the **Customer support** section.

3.  Click **Manage** in Basic queues area.

4.  Click **+ New** located on the command bar.

5.  Enter  **Support** for **Name** and select **Public** for **Type**, and enter **[your prefix ex. mollyc]** + **.support@test.invalid** for **Incoming Email**.

6.  Click **Save**.

7.  Click **+ New**.

8.  Enter **Bronze** for **Name** and select **Private** for **Type**.

9.  Click **Save**.

10. Click **+ New**.

11. Enter **Silver** for **Name** and select **Private** for **Type**.

12. Click **Save**.

13. Click **+ New**.

14. Enter **Gold** for **Name** and select **Private** for **Type**.

15. Click **Save**.

16. Click **Queues** under the **Customer support** section.

17. Select the **My Active Queues** view.

18. You should now see a private queue that was created for your user automatically, the public queue, and three private queues that you created in this lab.

### Task 2 – Add cases to queues

1.  Open the **Customer Service Hub** app.

2.  Click on **Cases** in the **Service** section of the sitemap.

3.  Select the **Service Required** case you created in the earlier lab.

4.  Click **Add to Queue** located on the command bar.

5.  Enter *Bronze* in the **Queue** field, click on the lookup icon and select the **Bronze** queue you created.

6.  Click **Add**.

7.  Click on **Cases** in the **Service** section of the sitemap.

8.  Select the **Defective Screen** case you created in the earlier lab.

9.  Click **Add to Queue** located on the command bar.

10. Enter *Support* in the **Queue** field, click on the lookup icon and select the **Support** queue you created.

11. Click **Add**.

12. Click **Queues** under the **Service** section.

13. Change the view from **Items I am working on** to **All items**.

14. You should see the Service Required case listed for the Bronze queue.

15. Change the queue selector from **Queues I'm a member of** to **All Public Queues**.

16. You should see the Defective Screen case listed for the Support queue.

17. Change the queue selector to **All Queues**.

### Task 3 – Perform actions on queue items

1.  Click **Queues** under the **Service** section.

2.  Change the view from **Items I am working on** to **Items available to work on**.

3.  Change the queue selector to **Queues I'm a member of**.

4.  You should see the Service Required case listed for the Bronze queue.

5.  Click to the left of the case in the queue to select it.

6.  Click **Queue Item Details** located on the command bar.

7.  Note that **Worked By** is blank.

8.  Click **Close**

9.  Click to the left of the case in the queue to select it.

10. Click **Pick** located on the command bar.

11. Leave the *Also remove the item(s) from the Queue* option set to **No**, and click **Pick**.

12. Change the view from **Items available to work on** to **Items I am working on**.

13. Click to the left of the case in the queue to select it.

14. Click **Queue Item Details** located on the command bar.

15. Note that **Worked By** is set to your user.

16. Click **Close**.

17. Click to the left of the case in the queue to select it.

18. Click **Release** located on the command bar and click **Release**.
