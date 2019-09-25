---
lab:
    title: 'Lab: Creating queues'
    module: 'Module 2: Case Management'
---

Module 2: Case Management
=========================

## Practice Lab 2 – Creating queues

Scenario
--------

You are a customer service manager at City Power & Light. You need to create
queues for the customer service representatives to use for processing cases. In
this lab, you will create a create multiple queues.

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

Exercise 2 – Create Queues
--------------------------

In this exercise, you will create four Queues.

### Task 1 – Create Queues

1.  Go back to your **Customer Service Hub** application.

2.  Click on the … button located below the **Site Map** button and select
    **Service Management**.

3.  Click on the **Site Map** button and select **Queues**.

4.  Click **+ New** located on the command bar.

5.  Enter **Support** for **Name** and select **Public** for **Type**.

6.  Click **Save**.

7.  Click **+ New**.

8.  Enter **Bronze** for **Name** and select **Public** for **Type**.

9.  Click **Save**.

10. Click **+ New**.

11. Enter **Silver** for **Name** and select **Public** for **Type**.

12. Click **Save**.

13. Click **+ New**.

14. Enter **Gold** for **Name** and select **Public** for **Type**.

15. Click **Save**.

16. Click on the **Site Map** button and select **Queues**.

17. You should now have a Private Queue that was created by default and the four
    Public Queues you created.
