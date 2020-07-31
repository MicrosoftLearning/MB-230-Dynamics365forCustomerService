---
lab:
    title: 'Lab: Install the app'
    module: 'Module 1: Customer Service Overview'
---

**Important Note:** This lab will provide you with an actual Dynamics 365 tenant
and licenses for the Power Platform applications you will be using in this
course. You will only be provided with one tenant for the practice labs in this
course. The settings and actions you take within this tenant do not roll-back or
reset, whereas the virtual machine you are provided with does reset each time
you close the lab session. Please be aware that Dynamics 365 is evolving all the time. The
instructions in this document may be different from what you experience in your
actual Dynamics 365 tenant. It is also possible to experience a delay of several
minutes before the virtual machine has network connectivity to begin the labs.

Module 1: Customer Service Overview
===================================

## Practice Lab 1 – Install the app

Scenario
--------

You are a business analyst working on the Dynamics 365 for Customer Service
implementation for your company, City Power & Light. You need to install the
Customer Service application in your environment.

Exercise 1 - Acquire Tenant Information and Connect
---------------------------------------------------

Note: If you have already completed practice recently, the virtual machine might
pick up where you left off and you will not need to log in again. In that case,
you can skip ahead to Exercise 2 and resume.

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

Select the [MARKETING, SALES HUB, WHATEVER YOU'RE USING] app from the list.

Exercise 2 – Install Dynamics 365 Customer Service Hub
------------------------------------------------------

In this exercise, you will install the Dynamics 365 Customer Service Application
and then install sample data.

### Task 1 – Install Customer Service Application

1.  Go back to <https://admin.Powerplatform.microsoft.com>

2.  Expand **Admin Centers** and select **Dynamics 365**.

3.  Select the **Edit** button. You will open the Contoso environment in the **Power Platform Admin center.**

4.  Enter **[your prefix ex. mollyc]+ CustServicePractice** for Name and URL if available (or enter a different URL). We will refer to this environment throughout the labs as the **Practice** environment. 

6.  Click **Save**.  

It will take few minutes to save the environment. 

### Task 2 – Install Sample Data

The Dynamics 365 Customer Service Application installation must complete before
starting this task.

1.  Navigate to <https://admin.powerplatform.microsoft.com>

2.  Expand **Admin Center** and click **Dynamics 365**.

3.  Select your instance and click **Open**.

4. Click the gear icon in the top right and select **Advanced Settings** (this will open a new window or tab)

4.  Navigate to **Settings** and select **Data Management**.

5.  Click **Sample Data**.

6.  Verify sample data is installed.  If not, Click **Install Sample Data**.

7.  Wait for the sample data installation to start and click **Close**. The
    sample data installation process will run in the background for a few
    minutes before you will see results.

8.  Click on the **Site Map** button and select the **Customer Service Hub**
    app.

9.  Your dashboard should now show some data. You may have to refresh the page
    before you can see the data.  Search between different dashboards and get familiar with the app.
