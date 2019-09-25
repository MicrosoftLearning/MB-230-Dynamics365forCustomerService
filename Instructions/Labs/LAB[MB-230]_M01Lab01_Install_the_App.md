---
lab:
    title: 'Lab: Install the app'
    module: 'Module 1: Customer Service Overview'
---

Module 1: Customer Service Overview
===================================

## Practice Lab 1 – Install the app

Scenario
--------

You are a business analyst working on the Dynamics 365 for Customer Service
implementation for your company, City Power & Light. You need to install the
Customer Service application in your environment.

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

Note: If you have already completed practice recently, the virtual machine might
pick up where you left off and you will not need to log in again. In that case,
you can skip ahead to Exercise 2 and resume.

### Task 1 – Connect to the Power platform administration portal

1.  On virtual machine MIA-BI, sign in as Student with the password Pa55w.rd if
    you are not already logged in.

2.  Outside the VM in the online lab interface click Files and choose O365
    Credentials. This will allocate an Office 365 tenant for you to use in these
    labs. It will display the admin email and password for your tenant. You
    should copy this information to notepad or similar for your reference.

3.  In virtual machine MIA-BI, launch Microsoft Edge from the taskbar. By
    default, the browser opens Office 365. Use the O365 Credentials you just
    acquired in the previous step to login.

4.  Navigate in the browser to the Power platform admin portal at
    <https://admin.powerplatform.microsoft.com>

Exercise 2 – Install Dynamics 365 Customer Service Hub
------------------------------------------------------

In this exercise, you will install the Dynamics 365 Customer Service Application
and then install sample data.

### Task 1 – Install Customer Service Application

1.  Navigate to <https://admin.powerplatform.microsoft.com>

2.  Expand **Admin Center** and click **Dynamics 365**.

3.  Choose “None. Do not customize” and make sure none of the above apps are
    checked.

4.  Once the demo has loaded, navigate to **Setting** and click on **Security**.
    Click on **Users** and find your user name on the list. Check the box next
    to your user name and select “Promote to Admin” from the ribbon.

5.  Navigate to <https://admin.powerplatform.microsoft.com>

6.  Expand **Admin Center** and click **Dynamics 365**.

7.  Select your instance and click **Edit Solutions**. There are two edit
    buttons one for editing the instance and another for managing your
    solutions, click on the smaller one next to the Solutions.

8.  Locate and select **Customer Service Hub**.

9.  Click **Install**.

10. Read the terms of service and click **Install**.

11. Wait for the installation to complete. The status column will change to
    Installed when completed. You will be able to complete step 2 while the
    installation is in progress.

### Task 2 – Install Sample Data

The Dynamics 365 Customer Service Application installation must complete before
starting this task.

1.  Navigate to <https://admin.powerplatform.microsoft.com>

2.  Expand **Admin Center** and click **Dynamics 365**.

3.  Select your instance and click **Open**.

4.  Navigate to **Settings** and select **Data Management**.

5.  Click **Sample Data**.

6.  Click **Install Sample Data**.

7.  Wait for the sample data installation to start and click **Close**. The
    sample data installation process will run in the background for a few
    minutes before you will see results.

8.  Click on the **Site Map** button and select the **Customer Service Hub**
    app.

9.  Your dashboard should now show some data. You may have to refresh the page
    before you can see the data.
