---
lab:
    title: 'Lab: Entitlements and templates'
    module: 'Module 3: Service Level Management'
---

Module 3: Service Level Management
==================================

## Practice Lab 1 – Entitlements and templates

Scenario
--------

As a customer service manager at City Power & Light, you need to create
entitlements and entitlement templates to manage complex service offerings and
guide your team in processing cases from various channels. In this lab, you will
create an entitlement with entitlement channels. You will also create an
entitlement template and create an entitlement from the template.

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

Exercise 2 – Entitlements
-------------------------

In this exercise, you will create an entitlement for Adventure Works customer,
this entitlement will allow Adventure Works to create 50 case through Email
channel, 30 Cases through Web channel, 10 Cases each for Twitter and Facebook
channels.

### Task 1 – Create Entitlement

In this task, you will create an entitlement with 100 total terms for Adventure
Works customer.

1.  Navigate to <https://admin.powerplatform.microsoft.com/>

2.  Expand **Admin Center** and select **Dynamics 365**.

3.  Select your **Instance** and click **Open**.

4.  Click **Switch to Another App** and select **Customer Service Hub**.

5.  Click on the **Site Map** button, click on the **…** button and select
    **Service Management.**

6.  Click on the **Site Map** button and select **Entitlements**.

7.  Click **New**.

8.  Enter **Adventure Default Entitlement** for **Name**, select **Adventure
    Works** for **Primary Customer**, select today’s date for **Start Date**,
    and select a year from today for **End Date**.

9.  Select **Yes** for Restrict **Based on Entitlement Terms**.

10. Select **Number of Cases** for **Allocation Type**, select **Case Creation**
    for **Decrease Remaining On**, and enter **100** for **Total Terms**.

11. Click **Save**. DO NOT navigate away from the Entitlement form.

### Task 2 – Add Channels to the Default Entitlement

In this task, you will add entitlement channels to the default entitlement and
then activate the entitlement.

1.  Go to the **Entitlement Channel** sub-grid, click on the **… More Commands**
    button and select **Add New Entitlement Channel**.

2.  Select **Email** for **Name**, enter **50** for **Total Terms** and click
    **Save and Close**.

3.  Click on the **… More Commands** button and select **Add New Entitlement
    Channel**.

4.  Select **Web** for **Name**, enter **30** for **Total Terms** and click
    **Save and Close**.

5.  Click on the **… More Commands** button and select **Add New Entitlement
    Channel**.

6.  Select **Facebook** for **Name**, enter **10** for **Total Terms** and click
    **Save and Close**.

7.  Click on the **… More Commands** button and select **Add New Entitlement
    Channel**.

8.  Select **Twitter** for **Name**, enter **10** for **Total Terms** and click
    **Save and Close**.

9.  Click **Activate**.

10. Confirm the activation.

### Task 3 – Test the Entitlement

In this task, you will test the default entitlement for Adventure Works.

1.  Click on the **Site Map** button, click on the **…** button and select
    **Service**.

2.  Click on the **Site Map** button and select **Cases**.

3.  Click **+ New Case**.

4.  Enter **Audio System Setup Issues** for **Case Title**, select **Adventure
    Works** for **Customer**, select **Email** for **Origin**, select
    **Adventure Default Entitlement** for **Entitlement** and click **Save**.

5.  Click + New.

6.  Enter **Defective Speaker** for **Case Title**, select **Adventure Works**
    for **Customer**, select **Facebook** for **Origin**, select **Adventure
    Default Entitlement** for **Entitlement** and click **Save**.

7.  Scroll to the **Entitlement** field and click on the **Adventure Default
    Entitlement**.

8.  Go to the **Entitlement Terms** section and make sure you have **98
    Remaining Terms**.

9.  Go to the **Entitlement Channel** sub-grid and make sure you have **49
    Remaining Terms** for **Email**, **9 Remaining Terms** for **Facebook**,
    **10 Remaining Terms** for **Twitter**, and **30 Remaining Terms** for
    **Web**.

Exercise 3 – Entitlement Templates
----------------------------------

In this exercise, you will create an entitlement template that will have 20 free
terms and the customer will be able to select the channel they prefer during the
entitlement creation.

### Task 1 – Create Entitlement Templates

In this task, you will create an entitlement template with 20 terms.

1.  Click on the **Site Map** button, click on the **…** button and select
    **Service Management**.

2.  Click on the **Site Map** button and select **Entitlement Templates**.

3.  Click on the **Entitlement Template** lookup field and select **+ New**.

4.  Enter **20 Free Terms** for **Entitlement Template Name**, select **Yes**
    for **Restrict on Entitlement Terms**, select **Number of Cases** for
    **Allocation Type**, select **Case Creation** for **Decrease Remaining On**,
    enter **20** for **Total Terms** and click **Save**. DO NOT navigate away
    from this page.

### Task 2 – Create Entitlement from Template

In this task, you will create 20 phone call only entitlement from the
entitlement template you created.

1.  Click on the **Site Map** button and select **Entitlements**.

2.  Click on the **V** chevron button next to the **New** button and select
    **From Template**.

3.  Select **20 Free Terms** for **Entitlement Template** and click **Select**.

4.  Some of the fields will be auto-filled from the template.

5.  Enter **Phone Call Only Terms** for **Name**, select **Jim Glynn** for
    **Primary Customer**, select today’s date for **Start Date**, select a year
    from today for **End Date,** and click **Save**.

6.  Go to the **Entitlement Channel** sub-grid, click on the **… More Commands**
    button and select **+ Add New Entitlement Channel**.

7.  Select **Phone** for **Name**, enter **20** for **Total Terms** and click
    **Save & Close**.

8.  Click on the **… More Commands** button and select **+ Add New Entitlement
    Channel**.

9.  Select **Email** for **Name**, enter **0** for **Total Terms** and click
    **Save & Close**.

10. Click on the **… More Commands** button and select **+ Add New Entitlement
    Channel**.

11. Select **Web** for **Name**, enter **0** for **Total Terms** and click
    **Save & Close**.

12. Click on the **… More Commands** button and select **+ Add New Entitlement
    Channel**.

13. Select **Facebook** for **Name**, enter **0** for **Total Terms** and click
    **Save & Close**.

14. Click on the **… More Commands** button and select **+ Add New Entitlement
    Channel**.

15. Select **Twitter** for **Name**, enter **0** for **Total Terms** and click
    **Save & Close**.

16. Click **Activate**.

17. Confirm activation. DO NOT navigate away from this page.

### Task 3 – Test the Entitlement

In this task, you will test the entitlement you created from the entitlement
template.

1.  Click on the **Site Map** button, click on the **…** button and select
    **Service**.

2.  Click on the **Site Map** button and select **Cases**.

3.  Click **+ New Case**.

4.  Enter **Missing Parts** for **Case Title** and select **Jim Glynn** for
    **Customer**.

5.  Select **Phone** for **Origin**, select **Phone Call Only Terms** for
    **Entitlement** and click **Save**.

6.  Click **+ New**.

7.  Enter **Wrong Cables** for **Case Title** and select **Jim Glynn** for
    **Customer**.

8.  Select **Web** for **Origin**, select **Phone Call Only Terms** for
    **Entitlement** and click **Save**.

9.  Scroll down to the **Entitlement** field and click **Phone Call Only
    Terms**.

10. Click **Save**. You will get an error telling you that there are no
    available terms.

11. Click **OK**.

12. You should get the same error if you select Email, Facebook or Twitter for
    Origin.

13. Select **Web** for **Origin** and clear the **Entitlement** field.

14. Click **Save**.

15. Since you didn’t select the **Phone Call Only Terms** entitlement, the Case
    will now be created.

16. Click on the **Site Map** button, click on the **…** button and select
    **Service Management**.

17. Click on the **Site Map** button and select **Entitlements**.

18. Click to open the **Phone Call Only Terms**.

19. Make sure you have **19 Remaining Terms** and **19 Phone** channel
    **Remaining Terms**.
