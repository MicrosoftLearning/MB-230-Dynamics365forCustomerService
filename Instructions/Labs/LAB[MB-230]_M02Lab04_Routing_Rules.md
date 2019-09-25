---
lab:
    title: 'Lab: Routing rules'
    module: 'Module 2: Case Management'
---

Module 2: Case Management
=========================

## Practice Lab 4 – Routing rules

Scenario
--------

You are a customer service manager at City Power & Light. You need to create
routing rules. In this exercise you will create and test several rules to route
to the queues you have created.

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

Task 1 – Connect to the Power platform administration portal
------------------------------------------------------------

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

Exercise 2 – Create and Routing Rules
-------------------------------------

In this exercise, you will create a routing rule set and add routing rules.

### Task 1 – Create Routing Rule Set

1.  Navigate to <https://admin.powerplatform.microsoft.com>

2.  Expand the **Admin Center** and select **Dynamics 365**.

3.  Select your instance and click **Open**.

4.  Navigate to **Settings \|Service Management**.

5.  Click **Routing Rule Sets**.

6.  Click **+New**

7.  Enter **Service Level Routing** for **Name** and click **Save**.

8.  Do not navigate away from this page.

### Task 2 – Create Bronze Routing Rule

1.  Go to the **Rule Items** sub grid and click **+** Add Rule Item Record.

2.  Enter **Route Bronze Cases** for **Name**.

3.  Go to the If **Conditions** section, click on the select dropdown, and
    select **Case**.

4.  Click on the second select dropdown to the right of Case and select
    **Service Level**.

5.  Click on the third select dropdown to the right of Service Level and select
    **Equals**.

6.  Hover over the Enter Value field and click **…**.

7.  Select **Bronze** from the **Available Values** list and click on the
    **\>\>** button.

8.  Click **OK**.

9.  Go to the **Then Conditions** section and select **Queue** for **Route To**.

10. Click on the **Add to Queue** lookup button and select **Bronze**.

11. Click **Save and Close**.

### Task 3 – Create Silver Routing Rule

1.  Go to the **Rule Items** sub grid and click **+** Add Rule Item Record.

2.  Enter **Route Silver Cases** for **Name**.

3.  Go to the If **Conditions** section, click on the select dropdown, and
    select **Case**.

4.  Click on the second select dropdown and select **Service Level**.

5.  Click on the third select dropdown and select **Equals**.

6.  Hover over the Enter Value field and click **…**.

7.  Select **Silver** from the **Available Values** list and click on the
    **\>\>** button.

8.  Click **OK**.

9.  Go to the **Then Conditions** section and select **Queue** for **Route To**.

10. Click on the **Add to Queue** lookup button and select **Silver**.

11. Click **Save and Close**.

### Task 4 – Create Gold Routing Rule

1.  Go to the **Rule Items** sub grid and click **+** Add Rule Item Record.

2.  Enter **Route Gold Cases** for **Name**.

3.  Go to the If **Conditions** section, click on the select dropdown, and
    select **Case**.

4.  Click on the second select dropdown and select **Service Level**.

5.  Click on the third select dropdown and select **Equals**.

6.  Hover over the Enter Value field and click **…**.

7.  Select **Gold** from the **Available Values** list and click on the **\>\>**
    button.

8.  Click **OK**.

9.  Go to the **Then Conditions** section and select **Queue** for **Route To**.

10. Click on the **Add to Queue** lookup button and select **Gold**.

11. Click **Save and Close**.

### Task 5 – Create General Support Routing Rule

1.  Go to the **Rule Items** sub grid and click **+** Add Rule Item Record.

2.  Enter **Route Support Cases** for **Name**.

3.  Go to the If **Conditions** section, click on the select dropdown, and
    select **Case**.

4.  Click on the second select dropdown and select **Service Level**.

5.  Click on the third select dropdown and select **Does Not Contain Data**.

6.  Go to the **Then Conditions** section and select **Queue** for **Route To**.

7.  Click on the **Add to Queue** lookup button and select **Support**.

8.  Click **Save and Close**.

9.  Your Routing Rule Set should now have four Rule Items.

10. Click **Activate**.

11. Confirm activation.

### Task 6 – Add Service Level Field to the Case Form

1.  Navigate to <https://web.powerapps.com>

2.  Make sure you **DON’T** have the **Default** environment selected.

3.  Select **Apps**.

4.  Select the **Customer Service Hub** application and click on the **Edit**
    button located on the command bar.

5.  Locate the **Case** entity and select **Forms**.

6.  Hover over the **Case for Interactive Experience** form located in the
    **Components** pane and click **Edit**.

7.  Locate the **Service Level** field from the **Field Explorer** pane, drag it
    to the form and place it below the **Entitlement** field.

8.  Click **Save and Close** to close the form editor.

9.  Click **Save**.

10. Click **Publish**.

11. Click **Save and Close** to close the **App Designer**.

### Task 7 – Test Routing Rules

1.  Go to the **Customer Service Hub** application.

2.  Click on the **Site Map** button and select **Queues**.

3.  Change the View from **Items I’m a Working on** to **All Items**.

4.  Change the Queue from **Queues I’m a Member of** to **All Queues**.

5.  There should be no Queues. Click on the **Site Map** button and select
    **Cases**.

6.  Click **+ New Case**.

7.  Enter **Case for Gold Service Level** for **Case Title** and select
    **Adventure Works** for **Customer**.

8.  Scroll down and select **Gold** for **Service Level**.

9.  Click **Save**.

10. Click **Save & Route**.

11. Click **Route**.

12. Click **+ New Case** again.

13. Enter **Case for Bronze Service Level** for **Case Title** and select **A.
    Datum Corporation** for **Customer**.

14. Scroll down and select **Bronze** for **Service Level**.

15. Click **Save**.

16. Click **Save & Route**.

17. Click **Route**.

18. Click **+ New Case** again.

19. Enter **Case Without Service Level** for **Case Title** and select **Alpine
    Ski House**.

20. Click **Save**.

21. Click **Save & Route**.

22. Click **Route**.

23. Click on the **Site Map** button and select **Queues**.

24. Change the View from **Items I’m a Working on** to **All Items**.

25. Change the Queue from **Queues I’m a Member of** to **All Queues**.

26. You should see three Queues of type Case.

    One **Gold**.

    One **Bronze**.

    One **Support**.
