---
lab:
    title: 'Lab: Resolving cases'
    module: 'Module 2: Case Management'
---

Module 2: Case Management
=========================

## Practice Lab 3 – Resolving cases

Scenario
--------

You are a customer service manager at City Power & Light who has been tasked
with trying the new case resolution and reactivation functionality before
rolling it out to your users. In this lab, you will resolve a case and reactive
that case.

Exercise 1 - Acquire Tenant Information and Connect
---------------------------------------------------

**Note:** If you have already completed a practice recently, the virtual machine
might pickup where you left off and you will not need to login again.  In that
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

Exercise 2 – Resolve Cases
--------------------------

### Task 1 – Resolve Case

1.  Go to your **Customer Service Hub** application.

2.  Click on the **Sitemap** Button and select **Service**.  Then select **Cases** under the **Service** section.

3.  Locate and open the **[your prefix ex. mollyc]+ Missing Power Supply** record you created.

4.  Click on the **Identify** stage of the **Business Process Flow**.

5.  Click **Next Stage**.

6.  The **Business process Flow** will advance to the **Research** stage. Click
    on the **Research** stage and click **Next Stage** again.

7.  The **Business process Flow** will advance to the **Resolve** stage. Click
    on the **Resolve** stage and click **Finish**.
    
8.  Click on the **Related** tab and select **Activities**

9.  Click the **[your prefix ex. mollyc]+ Missing Power Supply** Activity you created.

10. Click the **Mark Complete** button located in the command bar.  You need to complete any open Activities associated with a Case before you resolve the Case.  Otherwise, the Activities will be cancelled.

11.  Click on the **Resolve Case** button located in the command bar. You may need to click the ellipsis to see it.

12.  Select **Problem Solved** for **Resolution Type** and enter **Sent
    Replacement** for **Resolution**.

13. Enter **30 minutes** for **Billable Time**, enter **Sent replacement Power
    Supply** for **Remarks**, and click **Resolve**.

### Task 2 – Reactivate Resolved Case

1.  Click **Cases** under the **Service** section.

2.  Change the **View** from **My active Cases** to **Resolved Cases**.

3.  Open the Case you resolved in task 1.

4.  Click on the **Reactivate Case** button located in the command bar.

5.  Click **Reactivate**. The case will be reactivated.

6.  Change the **Case Title** to ****[your prefix ex. mollyc]+ Power Supply Not Received** in the details
    tab.

7.  Click **Save & Close**.
