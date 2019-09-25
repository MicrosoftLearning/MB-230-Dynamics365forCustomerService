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

**Important Note:** This lab will provide you with an actual Dynamics 365 tenant
and licenses for the Power Platform applications you will be using in this
course. You will only be provided with one tenant for the practice labs in this
course. The settings and actions you take within this tenant do not roll-back or
reset, whereas the virtual machine you are provided with does reset each time
you close the lab session. Please be aware that Dynamics 365 is evolving all the time. The
instructions in this document may be different from what you experience in your
actual Dynamics 365 tenant. It is also possible to experience a delay of several
minutes before the virtual machine has network connectivity to begin the labs.

Exercise 1 - Acquire Tenant Information and Connect
---------------------------------------------------

**Note:** If you have already completed a practice recently, the virtual machine
might pick up where you left off and you will not need to login again.  In that
case you can skip ahead to exercise two and resume.

### Task 1 – Connect to the Power platform administration portal

1.  On Virtual machine MB200-Dynamics_Lab, sign in as Admin with the password
    Pa55w.rd if you are not already logged in.

2.  Outside the VM in the online lab interface click Files and choose D365
    Credentials. This will allocate an Office 365 tenant for you to use in these
    labs.  It will display the admin email and password for your tenant.  You
    should copy this information to notepad or similar for your reference.

3.  In MB200-Dynamics_Lab launch Microsoft Edge from the taskbar. By default,
    the browser opens Office 365. Use the O365 credentials you just acquired in
    the previous step to login.

4.  Navigate in the browser to the Power platform admin portal at
    [https://admin.Powerplatform.microsoft.com](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fadmin.Powerplatform.microsoft.com&data=02%7C01%7Cv-juya%40microsoft.com%7C4be5a28c6f1e41eefee808d687ae2dc7%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636845580068684293&sdata=cLrD%2FhTDb5sRbajtFR9RrztfyTDCo0xGS4k8FSxTaIc%3D&reserved=0)
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

4.  Click **Switch to Another App** and select **Customer Service Hub**.

5.  Click on the **Site Map** button and select **Knowledge Articles**.

6.  Click **+ New**.

7.  Enter **Missing Parts** for **Title**, enter **missing, parts** for
    **Keywords** and click **Save**.

8.  Go to the **Content** area and make sure you have the **Designer** tab
    selected.

9.  Type **Purpose & Scope**.

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

8.  Go to the command bar and click **Publish**.

9.  Select Now for Publish, Published for Published Status, and click Publish.
    Do NOT navigate away from this page.

### Task 3 – Revise Knowledge Article

In this task, you will change step 6 of the Knowledge Article you created from
Escalate Case to Assign to Manager, and then you will revise the Knowledge
Article.

1.  Make sure you still have the Knowledge Article you created opened.

2.  Click **Create Minor Version**.

3.  Click **OK**.

4.  Go to the **Content** section.

5.  Replace step **6** of the **Procedure** from **If no, escalate Case** to
    **If no, assign to manager**.

6.  Click **Save**.

7.  Click **Approve**.

8.  Click **OK**.

9.  Click **Publish**.

10. Select **Now** and click **Publish** again.

11. Click on the Sitemap and select Knowledge Articles.

12. You should find the new version of the **Missing Parts** article in the **My
    Active Articles** view but not the old version.

13. Change the view to **Archived Articles**. You should find the old version of
    the **Missing Parts** article in this view.
