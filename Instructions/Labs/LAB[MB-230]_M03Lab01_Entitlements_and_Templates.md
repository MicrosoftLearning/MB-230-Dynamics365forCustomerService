---
lab:
    title: 'Lab: Entitlements and templates'
    module: 'Module 3: Service Level Management'
---

Module 3: Service Level Management
==================================

## Practice Lab 1 – Entitlements and templates

Scenario
--------

As a customer service manager at City Power & Light, you need to create
entitlements and entitlement templates to manage complex service offerings and
guide your team in processing cases from various channels. In this lab, you will
create an entitlement with entitlement channels. You will also create an
entitlement template and create an entitlement from the template.

Exercise 1 – Entitlements
-------------------------

In this exercise, you will create an entitlement for your user,
this entitlement will allow you to create 50 case through Email
channel, 30 Cases through Web channel, 10 Cases each for Twitter and Facebook
channels.

### Task 1 – Create Entitlement

In this task, you will create an entitlement with 100 total terms for Adventure
Works customer.

1.  Navigate to you environment.

2.  Open **Customer Service Hub**.

3.  Click on the **Sitemap** button in the bottom left corner and click **Service Management.**

4.  Click on **Entitlements** in the **Service Terms** section.

5.  Click **New**.

6.  Enter **[your prefix ex. mollyc]+ Entitlement 1** for **Name**, select *your user* for **Primary Customer**, select today’s date for **Start Date**,
    and select a year from today for **End Date**.

7.  Select **Yes** for **Restrict Based on Entitlement Terms**.

8. Select **Number of Cases** for **Allocation Type**, select **Case Creation**
    for **Decrease Remaining On**, and enter **100** for **Total Terms**.

9. Click **Save**. DO NOT navigate away from the Entitlement form.

### Task 2 – Add Channels to the Default Entitlement

In this task, you will add entitlement channels to the default entitlement and
then activate the entitlement.

1.  Go to the **Entitlement Channel** sub-grid, click on the ellipsis
    button and select **New Entitlement Channel**.

2.  Select **Email** for **Name**, enter **50** for **Total Terms** and click
    **Save & Close**.

3.  Click on the ellipsis button and select **New Entitlement
    Channel**.

4.  Select **Web** for **Name**, enter **30** for **Total Terms** and click
    **Save and Close**.

5.  Click on the ellipsis button and select **New Entitlement
    Channel**.

6.  Select **Facebook** for **Name**, enter **10** for **Total Terms** and click
    **Save and Close**.

7.  Click on the ellipsis button and select **New Entitlement Channel**.

8.  Select **Twitter** for **Name**, enter **10** for **Total Terms** and click
    **Save and Close**.

9.  Click **Activate**.

10. Confirm the activation.

### Task 3 – Test the Entitlement

In this task, you will test the default entitlement for Adventure Works.

1.  Click on the **Sitemap** button and select **Service**.

2.  Click **Cases**.

3.  Click **+ New Case**.

4.  Enter *[your prefix ex. mollyc]+ Audio System Setup Issues* for **Case Title**, select *your user* for **Customer**, select **Email** for **Origin**, select
    *[your prefix ex. mollyc]+ Entitlement 1* for **Entitlement** and click **Save**.

5.  Click **+ New**.

6.  Enter *[your prefix ex. mollyc]+ Defective Speaker* for **Case Title**, select *your user* for **Customer**, select **Facebook** for **Origin**, select **[your prefix ex. mollyc]+ Entitlement 1** for **Entitlement** and click **Save**.

7.  Scroll to the **Entitlement** field and click on the **[your prefix ex. mollyc]+ Entitlement 1**

8.  Go to the **Entitlement Terms** section and make sure you have **98
    Remaining Terms**.

9.  Go to the **Entitlement Channel** sub-grid and make sure you have **49
    Remaining Terms** for **Email**, **9 Remaining Terms** for **Facebook**,
    **10 Remaining Terms** for **Twitter**, and **30 Remaining Terms** for
    **Web**.

Exercise 2 – Entitlement Templates
----------------------------------

In this exercise, you will create an entitlement template that will have 20 free
terms and the customer will be able to select the channel they prefer during the
entitlement creation.

### Task 1 – Create Entitlement Templates

In this task, you will create an entitlement template with 20 terms.

1.  Click on the **Sitemap** button and select
    **Service Management**.

2.  Click **Entitlement Templates**.

3.  Click **+ New**.

4.  Enter *[your prefix ex. mollyc]+ 20 Free Terms* for **Entitlement Template Name**, select **Yes**
    for **Restrict on Entitlement Terms**, select **Number of Cases** for
    **Allocation Type**, select **Case Creation** for **Decrease Remaining On**,
    enter **20** for **Total Terms** and click **Save**. DO NOT navigate away
    from this page.

### Task 2 – Create Entitlement from Template

In this task, you will create 20 phone call only entitlement from the
entitlement template you created.

1.  Click **Entitlements**.

2.  Click on the **V** chevron button next to the **New** button and select
    **From Template**.

3.  Select *[your prefix ex. mollyc]+20 Free Terms* for **Entitlement Template** and click **Select**.

4.  Some of the fields will be auto-filled from the template.

5.  Enter *[your prefix ex. mollyc]+ Phone Call Only Terms* for **Name**, select *your user* for
    **Primary Customer**, select today’s date for **Start Date**, select a year
    from today for **End Date,** and click **Save**.

6.  Go to the **Entitlement Channel** sub-grid, click on the ellipsis and select **+New Entitlement Channel**.

7.  Select **Phone** for **Name**, enter **20** for **Total Terms** and click
    **Save & Close**.

8.  Click on the ellipsis and select **+New Entitlement Channel**.

9.  Select **Email** for **Name**, enter **0** for **Total Terms** and click
    **Save & Close**.

10. Click on the ellipsis and select **+New Entitlement Channel**.

11. Select **Web** for **Name**, enter **0** for **Total Terms** and click
    **Save & Close**.

12. Click on the ellipsis and select **+New Entitlement Channel**.

13. Select **Facebook** for **Name**, enter **0** for **Total Terms** and click
    **Save & Close**.

14. Click on the ellipsis and select **+New Entitlement Channel**.

15. Select **Twitter** for **Name**, enter **0** for **Total Terms** and click
    **Save & Close**.

16. Click **Activate**.

17. Confirm activation. DO NOT navigate away from this page.

### Task 3 – Test the Entitlement

In this task, you will test the entitlement you created from the entitlement
template.

1.  Click on the **Sitemap** button and select
    **Service**.

2.  Click **Cases**.

3.  Click **+ New Case**.

4.  Enter *[your prefix ex. mollyc]+ Missing Parts* for **Case Title** and select *your user* for
    **Customer**.

5.  Select **Phone** for **Origin**, select *[your prefix ex. mollyc]+ Phone Call Only Terms* for
    **Entitlement** and click **Save**.

6.  Click **+ New**.

7.  Enter *[your prefix ex. mollyc]+ wrong cables* for **Case Title** and select **Jim Glynn** for
    **Customer**.

8.  Select **Web** for **Origin**, select *[your prefix ex. mollyc]+Phone Call Only Terms* for
    **Entitlement** and click **Save**.

9.  Scroll down to the **Entitlement** field and click **Phone Call Only
    Terms**.

10. Click **Save**. You will get an error telling you that there are no
    available terms.

11. Click **OK**.

12. You should get the same error if you select Email, Facebook or Twitter for
    Origin.

13. Select **Web** for **Origin** and clear the **Entitlement** field.

14. Click **Save**.

15. Since you didn’t select the **Phone Call Only Terms** entitlement, the Case
    will now be created.

16. Click on the **Sitemap** button and select
    **Service Management**.

17. Click on the **Site Map** button and select **Entitlements**.

18. Click to open the *[your prefix ex. mollyc]+ Phone Call Only Terms*.

19. Make sure you have **19 Remaining Terms** and **19 Phone** channel
    **Remaining Terms**.
