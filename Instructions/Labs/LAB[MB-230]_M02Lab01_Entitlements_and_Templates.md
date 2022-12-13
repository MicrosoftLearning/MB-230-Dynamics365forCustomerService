---
lab:
    title: 'Lab: Entitlements and templates'
    module: 'Module 2: Entitlements and Service Level Agreements'
---

# Practice Lab 5 – Entitlements and SLAs

## Scenario

As a customer service manager at City Power & Light, you need to create entitlements and entitlement templates to manage complex service offerings and guide your team in processing cases from various channels. In this lab, you will create an entitlement with entitlement channels. You will also create an entitlement template and create an entitlement from the template.

## Exercise 1 – Entitlements

In this exercise, you will create an entitlement for your user, this entitlement will allow you to create 50 case through Email channel, 30 Cases through Web channel, 10 Cases each for Twitter and Facebook channels.

### Task 1 – Create Entitlement

In this task, you will create an entitlement with 100 total terms for the Relecloud customer.

1.  Open the **Customer Service Hub** app.

2.  Click on **Home** at the top of the left-hand side navigation.

3.  Click on **Service** at the bottom of the **Site Map** in the left-hand navigation and select **Service Management**.

4.  Click on **Entitlements** in the **Service Terms** section.

5.  Click **+ New** located on the command bar.

6.  Enter **[your prefix ex. mollyc]** + **Entitlement 1** for **Name**, select the account you created for Relecloud in the earlier lab for **Primary Customer**, select today's date for **Start Date**, and select a month from today for **End Date**.

7.  Select **Yes** for **Restrict based on entitlement terms**.

8.  Select **Number of Cases** for **Allocation Type**, select **Case Creation** for **Decrease Remaining On**, and enter **100** for **Total Terms**.

9.  Click **Save**. DO NOT navigate away from the Entitlement form.

### Task 2 – Add Channels to the entitlement

In this task, you will add entitlement channels to the default entitlement and then activate the entitlement.

1.  In the **Entitlement Channel** section of the Entitlement form, click on the ellipsis (...) and select **+ New Entitlement Channel**.

2.  Select **Email** for **Name**, enter **50** for **Total Terms** and click **Save & Close**.

3.  Click on the ellipsis button and select **+ New Entitlement Channel**.

4.  Select **Web** for **Name**, enter **30** for **Total Terms** and click **Save and Close**.

5.  Click on the ellipsis button and select **+ New Entitlement Channel**.

6.  Select **Facebook** for **Name**, enter **10** for **Total Terms** and click **Save and Close**.

7.  Click on the ellipsis button and select **+ New Entitlement Channel**.

8.  Select **Twitter** for **Name**, enter **10** for **Total Terms** and click **Save and Close**.

9.  Click on the ellipsis button and select **+ New Entitlement Channel**.

10. Select **Phone** for **Name**, enter **0** for **Total Terms** and click **Save and Close**.

11. Click on the ellipsis button and select **+ New Entitlement Channel**.

12. Select **IoT** for **Name**, enter **0** for **Total Terms** and click **Save and Close**.

13. Click **Activate**.

14. Click **Activate**.

15. Click **Set as Default**.

16. Click **Confirm**.

### Task 3 – Test the Entitlement

In this task, you will test the default entitlement for Relecloud.

1.  Click on **Home** at the top of the left-hand side navigation.

2.  Click on **Cases** in the **Service** section of the sitemap.

3.  Click **+ New Case**.

4.  Enter **[your prefix ex. mollyc]** + **Audio System Setup Issues** for **Case Title**, select the **Relecloud** account you created in the earlier lab for **Customer**, select **Email** for **Origin** and click **Save & Close**. The entitlement should be applied automatically.

5.  Click **+ New Case**.

6. Enter **[your prefix ex. mollyc]** + **Defective Speaker** for **Case Title**, select the **Relecloud** account you created in the earlier lab for **Customer**, select **Facebook** for **Origin**, select the **Entitlement 1** record you created for **Entitlement** and click **Save & Close**.

7.  Click **+ New Case**.

8.  Enter **[your prefix ex. mollyc]** + **Product Query** for **Case Title**, select the **Relecloud** account you created in the earlier lab for **Customer**, select **Phone** for **Origin**, select the **Entitlement 1** record you created for **Entitlement** and click **Save**.

9. The following message will be displayed, *You can't create a case for this entitlement because there are no available terms.*

10. Click **OK**.

11. Scroll to the **Entitlement** field and click on the **[your prefix ex. mollyc]+ Entitlement 1**. Click **Discard changes**.

12. Go to the **Entitlement Terms** section and make sure you have **98 Remaining Terms**.

13. Go to the **Entitlement Channel** sub-grid and make sure you have **49 Remaining Terms** for **Email**, **9 Remaining Terms** for **Facebook**, **10 Remaining Terms** for **Twitter**, and **30 Remaining Terms** for **Web**.

## Exercise 2 – Entitlement Templates

In this exercise, you will create an entitlement template that will have 20 free terms and the customer will be able to select the channel they prefer during the entitlement creation.

### Task 1 – Create Entitlement Templates

In this task, you will create an entitlement template with 20 terms.

1.  Open the **Customer Service Hub** app.

2.  Click on **Home** at the top of the left-hand side navigation.

3.  Click on **Service** at the bottom of the **Site Map** in the left-hand navigation and select **Service Management**.

4.  Click on **Entitlements Templates** in the **Templates** section.

5.  Click **+ New**.

6.  Enter **[your prefix ex. mollyc]** + **20 Free Terms** for **Entitlement Template Name**, select **Yes** for **Restrict on Entitlement Terms**, select **Number of Cases** for **Allocation Type**, select **Case Creation** for **Decrease Remaining On**, enter **20** for **Total Terms**.

7.  Click **Save**. DO NOT navigate away from this page.

8.  Go to the **Entitlement Channel** sub-grid, click on the ellipsis and select **+ New Entitlement Template Channel**.

9.  Select **Phone** for **Name**, enter **20** for **Total Terms** and click **Save & Close**.

10. Click on the ellipsis and select **+ New Entitlement Template Channel**.

11. Select **Email** for **Name**, enter **0** for **Total Terms** and click **Save & Close**.

12. Click on the ellipsis and select **+ New Entitlement Template Channel**.

13. Select **Web** for **Name**, enter **0** for **Total Terms** and click **Save & Close**.

14. Click on the ellipsis and select **+ New Entitlement Template Channel**.

15. Select **Facebook** for **Name**, enter **0** for **Total Terms** and click **Save & Close**.

16. Click on the ellipsis and select **+ New Entitlement Template Channel**.

17. Select **Twitter** for **Name**, enter **0** for **Total Terms** and click **Save & Close**.

18. Click on the ellipsis and select **+ New Entitlement Template Channel**.

19. Select **IoT** for **Name**, enter **0** for **Total Terms** and click **Save and Close**.

### Task 2 – Create Entitlement from Template

In this task, you will create 20 phone call only entitlement from the entitlement template you created.

1.  Click on **Entitlements** in the **Service Terms** section.

2.  Click on the **V** chevron button next to the **+ New** button and select **From Template**.

3.  Select **20 Free Terms** template you created for **Entitlement Template** and click **Select**.

4.  Some of the fields will be auto-filled from the template.

5.  Enter **[your prefix ex. mollyc]** + **Phone Call Only Terms** for **Name**, select the **Relecloud** account for **Primary Customer**, select today's date for **Start Date**, select a year from today for **End Date**, and click **Save**.

6.  Click **Activate**.

7.  Confirm activation. DO NOT navigate away from this page.

### Task 3 – Test the Entitlement

In this task, you will test the entitlement you created from the entitlement template.

1.  Click on **Home** at the top of the left-hand side navigation.

2.  Click on **Cases** in the **Service** section of the sitemap.

3.  Click **+ New Case**.

4.  Enter **[your prefix ex. mollyc]** + **Missing Parts** for **Case Title** and select the **Relecloud** account for **Customer**.

5.  Select **Phone** for **Origin**, select **Phone Call Only Terms** for **Entitlement** and click **Save**.

6.  Click **Go back**, click **+ New Case**.

7.  Enter **[your prefix ex. mollyc]** + **Wrong cables** for **Case Title** and select the **Relecloud** account for **Customer**.

8.  Select **Web** for **Origin**.

9.  Scroll down to the **Entitlement** field and select **Phone Call Only Terms**.

10. Click **Save**. You will get an error telling you that there are no available terms.

11. Click **OK**.

12. You should get the same error if you select Email, Facebook or Twitter for Origin.

13. Select **Web** for **Origin** and clear the **Entitlement** field.

14. Click **Save**.

15. Since you didn’t select the **Phone Call Only Terms** entitlement, the case will now be created.

16. Click on **Service** at the bottom of the **Site Map** in the left-hand navigation and select **Service Management**.

17. Click on **Entitlements** in the **Service Terms** section.

18. Click to open the **Phone Call Only Terms** entitlement.

19. Make sure you have **19 Remaining Terms** and **19 Phone** channel **Remaining Terms**.

## Exercise 3 – Service Level Agreements

In this exercise, you will create a Service Level Agreement and make it the default agreement.

### Task 1 – Holiday Schedule

In this task, you will create A holiday schedule to be used with Customer Service calendars.

1.  Open the **Customer Service Hub** app.

2.  Click on **Home** at the top of the left-hand side navigation.

3.  Click on **Service** at the bottom of the **Site Map** in the left-hand navigation and select **Service Management**.

4.  Click on **Holiday Schedule** in the **Service Terms** section.

5.  Click **+ New**.

6.  Enter **[your prefix ex. mollyc]** + **Holidays** for **Name**.

7.  Click **Create**. If a pop-up appears stating "service-level agreements (SLAs) are deprecated in the web client" Click **I acknowledge**.

8.  In the Holidays section, click **+ New**.

9.  Enter **Local festival** for **Name**, set the **Start Date** and **End Date** to be in two days time.

10. Click **OK**.

11. Click **Save & Close**.

### Task 2 – Customer Service Schedule

In this task, you will create a Customer Service Schedule to use with SLAs.

1.  In the **Customer Service Hub** app. Click on **Customer Service Schedule** in the **Service Terms** section.

2.  Click **+ New**.

3.  Enter **[your prefix ex. mollyc]** + **Customer Service Schedule** for **Name**.

4.  Click **Create**.

5.  Uncheck **Saturday** and **Sunday**.

6.  Click **Set Work Hours**.

7. Set Start to **9:00AM** and End to **5:00PM**.

8. Click **OK**.

9. Set **Holiday Schedule** to **Observe** and select the Holiday Schedule you created.

10. Select your local **Time Zone**

11. Click **Save & Close**.

### Task 3 – Create Service Level Agreement

In this task, you will create a SLA that sets a 1 hour response time on a problem case.

1.  In the **Customer Service Hub** app, click on **SLA KPIs** in the **Service Terms** section.

2.  Click **+ New**.

3.  Enter **[your prefix ex. mollyc]** + **Case Response By** for **Name**.

4.  Select **Case** for **Entity Name**.

5.  Select **First Response By KPI** for **KPI FIeld**

6.  Select **Created On** for **Applicable From**

7. Click **Save**. DO NOT navigate away from this form.

8. Click **Activate** in the command bar.

9. Click **Activate**.

10. Click on **Service Level Agreements** in the **Service Terms** section.

11. Click **+ New**.

12. Enter **[your prefix ex. mollyc]** + **SLA** for **Name**.

13. Select **Case** for **Primary Entity**.

14. Click **Save**.

15. Click **+ New SLA Item**

16. Enter **Problems** for **Name**.

17. Select the **SLA KPI** you created for **KPI**.

18. Select the **Customer Service Schedule** you created for **Business Hours**.

19. Under **Applicable When**, click on **Add** and **Add row**.

20. In the left-hand side of the condition, select **Case Type (Case)**.

21. Select **Equals** for the operator.

22. In the right-hand side of the condition, select **Problem**.

23. Under **Success Conditions**, click on **Add** and **Add row**.

24. In the left-hand side of the condition, select **First Response Sent (Case)**.

25. Select **Equals** for the operator.

26. In the right-hand side of the condition, select **Yes**.

27. Set **Warn After** to **45 minutes**.

28. Set **Failure After** to **1 hour**.

29. Click **Save**.

30. Click **Configure Actions**

31. If prompted to connect to Dataverse, click **Continue**.

32. Expand the **Switch** step.

33. In the **Non-compliant** path, click on **Add an action**.

34. Search for an select **Microsoft Dataverse**.

35. Select the **Update a row** action.

36. Select **Cases** for **Table name**.

37. Select **Regarding ID** for **Row ID**.

38. Click **Show Advanced options**.

39. Set **Is Escalated** to **Yes**.

40. Click **Save** and close the Power Automate browser tab..

41. Click **Close** in the *SLA Item* dialog.

42. Click **Save**.

43. Click **Activate**.

44. Click **Activate**.

45. Click **Set As Default**. Click **OK** in the **Change default SLA** pop-up.

### Task 4 – Service Level Agreement settings

In this task, you will configure the settings for service level agreements.

1.  In the **Customer Service Hub** app, click on **Service Configuration Settings** in the **Service Terms** section.

2.  Verify that the **Disable SLAs** option is set to **No**.

3.  Set the **Apply SLA after manual override** to **Yes**.

4.  In **Select SLA Pause Status**, move **On Hold** and **Waiting for Details** from **Available** to **Selected**.

5.  Click **Save**.

### Task 5 – Test Service Level Agreements

In this task, you will test that the SLA is applied to cases.

1.  Click on **Home** at the top of the left-hand side navigation.

2.  Click on **Cases** in the **Service** section of the sitemap.

3.  Click **+ New Case**.

4.  Enter **[your prefix ex. mollyc]** + **SLA Test #1** for **Case Title** and select the **Relecloud** account for **Customer**.

5.  Select **Web** for **Origin** and click **Save**.

6.  Select the **SLA** tab. You should see the Case Response By SLA KPI in progress with failure time set to 1 hour's time.

7.  Select the **Details** tab and set **First Response Sent** to **Yes** and click **Save**.

8.  Select the **SLA** tab. You should see the Case Response By SLA KPI with status on **Succeeded**.

9.  Click **Go back**, click **+ New Case**.

10. Enter **[your prefix ex. mollyc]** + **SLA Test #2** for **Case Title** and select the **Relecloud** account for **Customer**.

11. Select **Email** for **Origin** and click **Save**.

12. Select the **SLA** tab. There should be no SLA KPI items.
