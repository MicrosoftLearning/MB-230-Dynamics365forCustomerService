---
lab:
    title: 'Lab: Creating queues'
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

## Practice Lab 2 – Creating queues

Scenario
--------

You are a customer service manager at City Power & Light. You need to create
queues for the customer service representatives to use for processing cases. In
this lab, you will create a create multiple queues.



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

Exercise 2 – Create Queues
--------------------------

In this exercise, you will create four Queues.

### Task 1 – Create Queues

1.  Go back to your **Customer Service Hub** application.

2.  Click on the … button located below the **Site Map** button and select
    **Service Management**.

3.  Click on the **Sitemap** button in the bottom left and select **Queues**.

4.  Click **+ New** located on the command bar.

5.  Enter *[your prefix ex. mollyc]+ Support* for **Name** and select **Public** for **Type**.

6.  Click **Save**.

7.  Click **+ New**.

8.  Enter *[your prefix ex. mollyc]+ Bronze* for **Name** and select **Public** for **Type**.

9.  Click **Save**.

10. Click **+ New**.

11. Enter *[your prefix ex. mollyc]+ Silver** for **Name** and select **Public** for **Type**.

12. Click **Save**.

13. Click **+ New**.

14. Enter *[your prefix ex. mollyc]+ Gold** for **Name** and select **Public** for **Type**.

15. Click **Save**.

16. Click **Queues** under the **Case Settings** section.

17. You should now see a Private Queue that was created by default and the four
    Public Queues you created. (note: you might see other queues created by other students in your class)
