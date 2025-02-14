---
lab:
    title: 'Lab: Creating cases'
    module: 'Module 1: Case Management'
---

# Practice Lab – Creating cases

## Scenario

You are a customer service manager at City Power & Light who has been tasked with trying the new case functionality before rolling it out to your users. In this lab, you will create new customer cases and create a phone calls associated with the cases.

## Exercise 1 – Navigate to Dynamics 365 Customer Service Hub

In this exercise, you will navigate to the Dynamics 365 Customer Service Application.

### Task 1 – Navigate to Customer Service Hub app

1.  Navigate to Access <https://admin.powerplatform.microsoft.com/environments>.

2.  Select the CustomerService Trail environment.

3.  Click **Open**.

4.  You should be in the **Customer Service Hub** app. If you are in a different app, click on the name of the app in the top left of the application next to Dynamics 365 and from the list of published apps, select the **Customer Service Hub** app

5.  You should now be showing the **Dashboard** view.

## Exercise 2 – Create case

In this exercise, you will create an Account, a Contact, a Subject, a Product, and a Case record. You will also add a Phone Call activity to the case.

### Task 1 – Create Account

1.  Click on **Accounts** in the **Customers** section of the sitemap.

2.  Click **+ New** located on the command bar.

3.  Enter **Relecloud** for **Account Name**.

4.  Click **Save & Close**.

### Task 2 – Create Contacts

1.  Click on **Contacts** in the **Customers** section of the sitemap.

2.  Click **+ New** located on the command bar.

3.  Enter **Jane** for **First Name**.

4.  Enter **Doe** for **Last Name**.

5.  Enter **Relecloud** in the **Account Name** field, click on the lookup icon and select the account you created in Task 1.

6.  Click **Save & Close**.

### Task 3 – Create Subject

1. Open **Customer Service admin center** app. If you are in a different app, click on the name of the app in the top left of the application next to Dynamics 365 and from the list of published apps, select the **Customer Service admin center** app

2. Click on **Case settings** in the **Customer support** section of the sitemap.

3. Click **Manage** in the Subjects area.

4. Click **+Add** for Subject tree management.

5. Enter **Maintenance** for **Title**.

6. Click **Save & Close**.

### Task 4 – Create Product

1. You should be in the **Power Platform Environment Settings** app. If you are in a different app, click on the name of the app in the top left of the application next to Dynamics 365 and from the list of published apps, select the **Power Platform Environment Settings** app.

2. Click on **Product Catalog** in the **Business** section of the sitemap.

3. Click on **Families and products**.

4. Click **Add Product** from Command bar.

5. Enter **JBO Top D. Hifi** for **Name** and Enter **HBO** for **Product ID**.

6. Enter **Quantity** for **Unit Group** and **Default Unit**.

7. Click **Save**.

8. Click **Publish** from Command bar and confirm.


### Task 5 – Create Case

Make sure you are in the **Customer Service Hub** app.

1.  Click on **Cases** in the **Service** section of the sitemap.

2.  Click **+ New Case** located on the command bar.

3.  Enter **Defective Screen** for **Case Title**.

4.  Click on the **Subject** field and select **Maintenance**.

5.  Enter **Relecloud** in the **Customer** field, click on the lookup icon and select the account you created in Task 1.

6.  Select **Phone** from the **Origin** drop-down field.

7.  Enter *JBO* in the **Product** field, click on the lookup icon and select the **JBO Top D. Hifi** product.

8.  Enter **Laptop display is too bright** in the **Description** field.

9.  Click on the **Identify** stage in the business process flow.

10. Enter **Jane Doe** in the **Find Contact** field, click on the lookup icon and select the **Jane Doe** contact you created in Task 2.

11. Select the **Details** tab.

12. Select **Problem** from the **Type** drop-down field.

13. Click **Save**.

14. Click on the **Identify** stage in the business process flow, and select **Next Stage**.

15. Select the **Summary Tab**. In the Timeline, click on **+**, and select **Phone Call**.

16. Enter **Further details** for **Subject**.

17. Select **Outgoing** from the **Direction** drop-down field.

18. Ensure that your user record is set for **Call From**.

19. Ensure that the Jane Doe contact is set for **Call To**.

20. Select **15 minutes** from the **Duration** drop-down field.

21. Select **tomorrow's date** and **9:00AM** for **Due**.

22. Select **High** from the **Priority** drop-down field.

23. Select **Save & Close**

## Exercise 3 – Create case from an activity

In this exercise, you will create a Phone Call activity and then convert the activity to a Case.

### Task 1 – Create Phone Call activity

1.  Click on **Contacts** in the **Customers** section of the sitemap.

2.  Select the **Jane Doe** contact you created in Task 2.

3.  In the Timeline, click on **+**, and select **Phone Call**.

4.  Enter **Service required** for **Subject**.

5.  Select **Incoming** from the **Direction** drop-down field.

6.  Ensure that the Jane Doe contact is set for **Call From**.

7.  Ensure that your user record is set for **Call To**.

8.  In the Description field, enter **Annual service needs to be scheduled for Jane**

9.  Click into the **Duration** field and type **15 minutes**.

10. Select today's date for **Due**.

11. Select **Save and Close**

### Task 2 – Covert Phone Call activity

1.  In the Timeline, click on the **Open Record** icon for the phone call you just created.

2.  Click **Convert To** located on the command bar [Note:you may need to click on the ellipsis (...)] and select **To Case**.

3.  Click on **Customer** field in the **Convert to Case** window.

4.  Select the **Jane Doe** contact you created in Task 2.

5.  Click on the **Subject** field and select **Maintenance**.

6.  Click **Convert**.

7.  Review the case that was created. Note that the customer is linked to the contact and the origin is set to Phone.
