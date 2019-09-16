Module 2: Case Management
=========================

## Practice Lab 3 – Resolving cases

Scenario
--------

You are a customer service manager at City Power & Light who has been tasked
with trying the new case resolution and reactivation functionality before
rolling it out to your users. In this lab, you will resolve a case and reactive
that case.

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

Exercise 2 – Resolve Cases
--------------------------

### Task 1 – Resolve Case

1.  Go to your **Customer Service Hub** application.

2.  Click on the **Site Map** Button and select **Cases**.

3.  Locate and open the **Missing Power Supply** record you created.

4.  Click on the **Identify** stage of the **Business Process Flow**.

5.  Click **Next Stage**.

6.  The **Business process Flow** will advance to the **Research** stage. Click
    on the **Research** stage and click **Next Stage** again.

7.  The **Business process Flow** will advance to the **Resolve** stage. Click
    on the **Resolve** stage and click **Finish** again.

8.  Click on the **Resolve Case** button located in the command bar.

9.  Select **Problem Solved** for **Resolution Type** and enter **Sent
    Replacement** for **Resolution**.

10. Enter **0.5 hours** for **Billable Time**, enter **Sent replacement Power
    Supply** for **Remarks**, and click **Resolve**.

### Task 2 – Reactivate Resolved Case

1.  Click on the **Site Map** Button and select **Cases**.

2.  Change the **View** from **My active Cases** to **Resolved Cases**.

3.  Open the Case you resolved in task 1.

4.  Click on the **Reactivate Case** button located in the command bar.

5.  Click **Reactivate**. The case will be reactivated.

6.  Change the **Case Title** to **Power Supply Not Received** in the details
    tab.

7.  Click **Save**.
