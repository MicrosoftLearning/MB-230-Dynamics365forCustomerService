---
lab:
    title: 'Lab: Creating cases'
    module: 'Module 2: Case Management'
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

Module 2: Case Management
=========================

## Practice Lab 1 – Creating cases

Scenario
--------

You are a customer service manager at City Power & Light who has been tasked
with trying the new case functionality before rolling it out to your users. In
this lab, you will create a case and create a phone call associated with that case.

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

Select the Customer Service app from the list.

Exercise 2 – Create Cases
-------------------------

In this exercise, you will create a Case record, you will also add a Phone Call
activity and then convert the activity to Case.

### Task 1 – Create Case

1.  Navigate to <https://admin.powerplatform.microsoft.com>

2.  Expand **Admin Center** and select **Dynamics 365**.

3.  Select your instance and click **Open**.

4.  Click **Dynamics 365 drop-down arrow** and select **Customer Service Hub**
    application.

5.  Click on **Cases** in the **Service** section of the sitemap.

6.  Click **+ New Case** located on the command bar.

7.  Enter *[your prefix ex. mollyc]+ Defective Screen* for **Case Title**, select **Default Subject**
    for **Subject**, type *your user name* in the **Customer** field, click on the lookup
    button and select *your user*.

8.  Click **Save**.

### Task 2 – Create Phone Call Activity

1.  Go back to your **Customer Service Hub** application.

2.  Click **Cases** from the **Service** section of the sitemap

3.  Open the case you just created

4.  Click the **Related** tab and select **Activities**

5.  Click on the **+New Activity drop-down** button and select **Phone Call**.

4.  Enter *[your prefix ex. mollyc]+ Defective Screen* for **Subject**.

5.  Ensure your user record is set for **Call From** and **Call To**

6.  Select **Incoming** for **Direction**, enter **15 Minutes** for **Duration**
    and click **Save & Close**
