---
lab:
    title: 'Lab: Create knowledge articles'
    module: 'Module 4: Knowledge Management'
---


Module 4: Knowledge Management
==============================

## Practice Lab 1 – Create knowledge articles

Scenario
--------

As a customer care coordinator at City Power & Light, you are responsible for
instructing the customer service team and providing them with troubleshooting
articles to support case resolution. You need to create a knowledge article
within Dynamics 365 for Customer Service. In this lab, you will create a
knowledge article, walk through the publishing process and then revise that
article.

Exercise 1 - Acquire Tenant Information and Connect
---------------------------------------------------

**Note:** If you have already completed a practice recently, the virtual machine
might pick up where you left off and you will not need to login again.  In that
case you can skip ahead to exercise two and resume.

### Task 1 – Connect to the Power platform administration portal

1.  Sign into the Virtual Machine using the lab instructions provided by the lab hoster (if using).

2.  Outside the VM in the online lab interface click Files and choose D365
    Credentials. This will allocate a Dynamics 365 365 tenant for you to use in these
    labs.  It will display the user email and password for your tenant. 

3.  Launch Microsoft Edge from the taskbar. 

4.  Navigate in the browser to the Power Platform admin portal at https://admin.Powerplatform.microsoft.com.

5. Sign in using the provided credentials. Record the characters before the "@" symbol in your email address - it should be a first name and a last initial. These characters will become your "alias" throughout the course. Write them down somewhere you'll be able to access throughout the course.

**Important:** Please be aware that this tenant and the Dynamics 365 organization will be shared with the other students in your classroom, like employees would share a tenant when using the Dynamics 365 instance belonging to their organization. Do not use any PII (personally identifiable information) when creating records. It is also good practice to use your username prefix (ex., **mollyc**) in front of all records, data, apps, workflows, etc. you create.

6. Click the button to the left of the **Power Platform admin center** in the top menu to view all available apps. Select **Dynamics 365.**

Select the Customer Service Hub app from the list.
    .

Exercise 2 – Knowledge Management
---------------------------------

In this exercise, you will create, approve, publish, and revise an internal
Knowledge Article for missing parts.

### Task 1 – Create Internal Article

In this task, you will create an internal Knowledge Article for missing parts.

1.  Navigate to <https://admin.powerplatform.microsoft.com/>

2.  Expand **Admin Center** and select **Dynamics 365**.

3.  Select your **Instance** and click **Open**.

4.  Click **Dynamics 365** and select **Customer Service Hub**.

5.  Click on the **Sitemap** button and select **Service**.  Select **Knowledge Articles** under the **Knowledge** section

6.  Click **+ New**.

7.  Enter *[your prefix ex. mollyc]+ Missing Parts* for **Title**, enter **missing, parts** for
    **Keywords** and click **Save**.

8.  Go to the **Content** area and make sure you have the **Designer** tab
    selected.

9.  Type *[your prefix ex. mollyc]+ Purpose & Scope*.

10. Click on the **Paragraph Format** selector and select **H2**. This option
    will only appear if your screen is fully expanded.

11. Hit the **\<Return\>** key to start a new line. The **Format Selector**
    should change back to **Normal**.

12. Type the paragraph below.

    Use procedure below to resolve Phone call Cases that are related to missing
    parts.

13. Hit the **\<Return\>** key to start a new line.

14. Click on the **Paragraph Format** selector and select **H2**.

15. Type **Procedure**.

16. Hit the **\<Return\>** key to start a new line.

17. Go to the ribbon and click **Insert/Remove Numbered List**. This action will
    insert numbered list.

18. Provide the steps below.

    1.  Get Order Number for Customer.

    2.  Locate Order record.

    3.  Locate the product in question and open it.

    4.  Is the product the Customer received listed?

    5.  If yes, Send the Customer a replacement order and a return label.

    6.  If no, escalate Case.

19. Click Save.

20. Go to the **Business Process Flow** and click on the **Author** stage.

21. Select **Default Subject** for **Article Subject**, check the **Mark
    Complete** checkbox, and click **Next Stage**.

### Task 2 – Approve and Publish Knowledge Article

In this task, you will assume the role of the Knowledge Article Approver and
Approve the Knowledge Article you created, and then publish it.

1.  Go to the **Business Process Flow** and click on the **Review** stage.

2.  Select **Approved** for **Review**.

3.  Click **OK**.

4.  Go to the **Business Process Flow** and click on the **Review** stage.

5.  Click **Next Stage**.

6.  Click on the **Publish** stage.

7.  Check the **Set Product Association** checkbox and click **Finish**.

8.  Go to the command bar and click **Publish**. YOu may need to click the ellipsis to see it.

9.  Select Now for Publish, Published for Published Status, and click Publish.
    Do NOT navigate away from this page.

### Task 3 – Revise Knowledge Article

In this task, you will change step 6 of the Knowledge Article you created from
Escalate Case to Assign to Manager, and then you will revise the Knowledge
Article.

1.  Make sure you still have the Knowledge Article you created opened.

2.  Click **Create Minor Version** from the command bar. You may need to click the ellipsis to see this

3.  Click **OK**.

4.  Go to the **Content** section.

5.  Replace step **6** of the **Procedure** from **If no, escalate Case** to
    **If no, assign to manager**.

6.  Click **Save**.

7.  Click **Approve**. You may need to click the ellipsis to see this

9.  Click **Publish**.

10. Select **Now** and click **Publish** again.

11. Click on the Sitemap and select Knowledge Articles.

12. You should find the new version of the **Missing Parts** article in the **My
    Active Articles** view but not the old version.

13. Change the view to **Archived Articles**. You should find the old version of
    the **Missing Parts** article in this view.
