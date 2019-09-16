Module 3: Service Level Management
==================================

## Practice Lab 2 – Building and using SLAs

Scenario
--------

As a customer service manager at City Power & Light, you need to create service
level agreements to help ensure that customer expectations are met on the
timeliness of case handling. In this lab, you will create service level
agreements, add SLA details and actions and add the SLA to an entitlement.

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

Note: If you have already completed a practice recently, the virtual machine
might pickup where you left off and you will not need to login again.  In that
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

Exercise 2 – Service Level Agreements
-------------------------------------

In this exercise, you will create two SLAs with the following properties:

1.  Cases with Gold service level will generate a warning if they don’t get
    first response in one minute and a failure if they don’t get first response
    in two minutes. This SLA will send an email when it fails.

2.  All other Cases will generate a warning if they don’t get first response in
    one day and a failure if they don’t get first response in two days.

### Task 1 – Create the Gold SLA

In this task, you will create an SLA for Cases with Gold Service Level.

1.  Navigate to <https://admin.powerplatform.microsoft.com/>

2.  Expand **Admin Center** and select **Dynamics 365**.

3.  Select your **Instance** and click **Open**.

4.  Navigate to **Settings \| Service Management**.

5.  Go to the **Service Terms** section and select **Service Level Agreements**.

6.  Click **+ New**.

7.  Enter **Gold First Response** for **Name** and click **OK**.

8.  Select **Created On** for **Applicable From**, select **Enhanced** for **SLA
    Type**, select **Allow** for **Allow Pause and Resume** and click **Save**.
    DO NOT navigate away from this page.

### Task 2 – Add SLA Details for Gold

In this task, you will add an SLA Details for the Cases with Gold Service Level.

1.  Go to the **SLA Details** section and click **+ Add SLA Item Record**.

2.  Enter **Gold Cases** for **Name** and select **First Response By KPI** for
    **SLA KPI**.

3.  Go to the **Applicable When** section, click on the **Select** text and
    select **Case**.

4.  Click on the second **Select** text when it appears to the right and select
    **Service Level**.

5.  Click on the third **Select** text and select **Equals**.

6.  Hover over the **Enter Value** text and click on the **…** button.

7.  Select **Gold** and click **Add**.

8.  Click **OK**.

9.  Go to the **Success Criteria** section, click on the **Select** text and
    select **Case**.

10. Click on the second **Select** text when it appears to the right and select
    **First Response Sent**.

11. Click on the third **Select** text and select **Equals**.

12. Hover over the **Enter Value** text and click on the **…** button.

13. Select **Yes** and click **Add**.

14. Click **OK**.

15. Go to the **SLA Item Failure** section and enter **2 minutes** for **Failure
    After**.

16. Go to the **SLA Item Warning** section and enter **1 minute** for **Warn
    After**.

17. Click **Save**. DO NOT navigate away from this page.

### Task 3 – Add Action

In this task, you will add a failure action that will send an email.

1.  Go to the **SLA Item Failure** section, click **Add Step** and select **Send
    Email**.

2.  Click Set Property.

3.  Click to select the **From** field.

4.  Go to the **Form Assist** pane, select **Case** from the **Look For:** drop
    down, select **Owning User**, and click **Add**.

5.  Click **OK**.

6.  Click to select the **To** field. Usually, this email will go to the
    customer and/or to manager, but in this practice, we will just send it to
    the owner.

7.  Go to the **Form Assist** pane, select **Case** from the **Look For:** drop
    down, select **Owning User**, and click **Add**.

8.  Click **OK**.

9.  Enter **SLA Failure** for **Subject**.

10. Click to select the **Body** of the email.

11. Type **Dear**

12. Go to the **Form Assist** pane, select **Customer (Contact)** from the
    **Look For:** drop down, select **First Name**, and click **Add**.

13. Click **OK**.

14. Start a new line and type **This is a test Email ……**

15. Start a new line and type Thanks,

16. Start a new line.

17. Go to the **Form Assist** pane, select **Owning User (User)** from the
    **Look For:** drop down, select **Full Name**, and click **Add**.

18. Click **OK**.

19. Click **Save and Close** to close the email form.

20. Click **Save and Close** to close SLA Item editor.

21. Click **Activate**.

22. Confirm activation. DO NOT navigate away from this page.

### Task 4 – Create the Default SLA

In this task, you will create a default SLA.

1.  Click **+ New**.

2.  Enter **Default First Response** for **Name** and click **OK**.

3.  Select **Created On** for **Applicable From**, select **Enhanced** for **SLA
    Type**, select **Allow** for **Allow Pause and Resume** and click **Save**.
    DO NOT navigate away from this page.

### Task 5 – Add SLA Details for Default

In this task, you will add an SLA Details to the default SLA.

1.  Go to the **SLA Details** section and click **+ Add SLA Item Record**.

2.  Enter **Default SLA Item** for **Name** and select **First Response By KPI**
    for **SLA KPI**.

3.  Go to the **Success Criteria** section, click on the **Select** text and
    select **Case**.

4.  Click on the second **Select** text when it appears to the right and select
    **First Response Sent**.

5.  Click on the third **Select** text and select **Equals**.

6.  Hover over the **Enter Value** text and click on the **…** button.

7.  Select **Yes** and click **Add**.

8.  Click **OK**.

9.  Go to the **SLA Item Failure** section and enter **2 days** for **Failure
    After**.

10. Go to the **SLA Item Warning** section and enter **1 day** for **Warn
    After**.

11. Click **Save and Close**.

12. Click **Activate**.

13. Confirm activation.

14. Click **Set as Default**.

15. Click **OK**.

### Task 6 – Edit Entitlement

In this task, you will edit the Phone Call Only Entitlement you created in early
labs and select the Gold First Response Agreement you created in task 1.

1.  Click **Switch to Another App** and select **Customer Service Hub**.

2.  Click on the **Site Map** button, click on the **…** button and select
    **Service Management**.

3.  Click on the **Site Map** button and select **Entitlements**.

4.  Click to open the **Phone Call Only Terms** Entitlement record.

5.  Click **Deactivate**.

6.  Confirm deactivation.

7.  Locate the **Primary Customer** field and make note of the owner of this
    entitlement (Jim Glynn).

8.  Locate the **SLA** field and select **Gold First Response**.

9.  Click **Save**.

10. Click **Activate**.

11. Confirm the activation.

Exercise 3 – Test Your Work
---------------------------

In this exercise, you will test the SLAs you created.

### Task 1 – Test Default SLA

1.  Click on the **Site Map** button, click on the **…** button and select
    **Service**.

2.  Click on the **Site Map** button and select **Cases**.

3.  Click **+ New Case**.

4.  Enter **Default SLA Case** for **Case Title**, select **Coho Winery** for
    **Customer**, and click **Save**.

5.  Locate the **First Response in** field and make sure the timer is counting
    down from two days.

6.  Select the **SLA** tab.

7.  The **SLA KPI Instance** status should be set **In Progress**.

8.  Select the **Details** tab.

9.  Locate the **First Response Sent** field and select **Yes**.

10. Click **Save**.

11. Select the **Summary** tab.

12. Locate the **First Response in** field and make sure it is set to
    **Succeeded**. You may need to refresh your page. DO NOT navigate away from
    this page.

### Task 2 – Test Gold SLA

1.  Click **+ New**.

2.  Enter **Gold SLA Case** for **Case Title**, select **Jim Glynn** for
    **Customer**.

3.  Select **Phone Call Only Terms** for **Entitlement**.

4.  Select **Gold** for **Service Level** and click **Save**.

5.  Locate the **First Response in** field and make sure the timer is counting
    down from two minutes.

6.  Select the **SLA** tab.

7.  The **SLA KPI Instance** status should be set **In Progress**.

8.  Select the **Summary** tab.

9.  Locate the **First Response in** field and wait for it to **Expire**.

10. The **First Response in** should start incrementing and it should change
    color to **Red**.

11. Click on the **Site Map** button and select **Activities**.

12. Change the view to **All Emails** and select **All**.

13. You should have one email. Click on the **SLA Failure** email.

14. Examine the email body and make sure content is what you expected.
