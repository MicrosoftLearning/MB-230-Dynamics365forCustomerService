---
lab:
    title: 'Lab: Service Level Agreements'
    module: 'Module 2: Service Level Agreements and Knowledge Management'
---

# Practice Lab – Service Level Agreements

## Scenario

As a customer service manager at City Power & Light, you need to create a Service Level Agreement and make it the default agreement. In this lab, you will create an SLA and test it. This exercise should take approximately 20 minutes to complete. 

## Exercise 1 – Service Level Agreements

In this exercise, you will create a Service Level Agreement and make it the default agreement.

### Task 1 – Holiday Schedule

In this task, you will create a holiday schedule to be used with Customer Service calendars.

1.  Open the **Customer Service admin center** app.

2.  Click on **Home** at the top of the left-hand side navigation.

3.  Click on **Calendar** under **Operations** section

4.  Click on **Manage** in the **Holiday calender** area.

5.  Click **+ New**.

6.  Enter **Holidays** for **Name**.

7.  Click **Create**. If a pop-up appears stating "service-level agreements (SLAs) are deprecated in the web client" Click **I acknowledge**.

8.  In the Holidays section, click **+ New**.

9.  Enter **Local festival** for **Name** and set the **Start Date** and **End Date** to be in two days time.

10. Click **OK**.

11. Click **Save & Close**.

### Task 2 – Customer Service Schedule

In this task, you will create a Customer Service Schedule to use with SLAs.

1.  Click on **Calendar** under **Operations** section

2.  Click on **Manage** in the **Customer Service calender** area.

3.  Click **+ New**.

4.  Enter **Customer Service Schedule** for **Name** and Click **Create**.

5.  Uncheck **Saturday** and **Sunday**.

6.  Click **Set Work Hours**.

7. Set Start to **9:00AM** and End to **5:00PM**.

8. Click **OK**.

9. Set **Holiday Schedule** to **Observe** and select the Holiday Schedule you created.

10. Select your local **Time Zone**.

11. Click **Save & Close**.

### Task 3 – Create Service Level Agreement

In this task, you will create a SLA that sets a 1 hour response time on a problem case.

1.  In the **Customer Service admin center** app, click on **SLA KPIs** in the **Service Terms** section.

2.  Click **+ New**.

3.  Enter **Case Response By** for **Name**.

4.  Select **Case** for **Entity Name**.

5.  Select **First Response By KPI** for **KPI FIeld**.

6.  Select **Created On** for **Applicable From**.

7. Click **Save**. DO NOT navigate away from this form.

8. Click **Activate** in the command bar.

9. Click **Activate**.

10. Click on **Service Level Agreements** in the **Service Terms** section.

11. Click **+ New**.

12. Enter **SLA** for **Name**.

13. Select **Case** for **Primary Entity**.

14. Click **Save**.

15. Click **+ New SLA Item**.

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

30. Click **Configure Actions**.

31. If prompted to connect to Dataverse, click **Continue**.

32. Expand the **Switch** step.

33. In the **Non-compliant** path, click on **Add an action**.

34. Search for an select **Microsoft Dataverse**.

35. Select the **Update a row** action.

36. Select **Cases** for **Table name**.

37. Select **Regarding ID** for **Row ID**.

38. Click **Show Advanced options**.

39. Set **Is Escalated** to **Yes**.

40. Click **Save** and close the Power Automate browser tab.

41. Click **Close** in the *SLA Item* dialog.

42. Click **Save**.

43. Click **Activate**.

44. Click **Activate**.

45. Click **Set As Default**. Click **OK** in the **Change default SLA** pop-up.

### Task 4 – Service Level Agreement settings

In this task, you will configure the settings for service level agreements.

1.  In the **Customer Service admin center** app, click on **Service Terms** in Operations section.

2.  Click **Manage** on other settings area.

3.  Verify that the **Disable SLAs** option is set to **No**.

4.  Set the **Apply SLA after manual override** to **Yes**.

5.  In **Select SLA Pause Status**, move **On Hold** and **Waiting for Details** from **Available** to **Selected**.

6.  Click **Save**.

### Task 5 – Test Service Level Agreements

In this task, you will test that the SLA is applied to cases. Make sure you are in **Customer Service Hub** app.

1.  Click on **Home** at the top of the left-hand side navigation.

2.  Click on **Cases** in the **Service** section of the sitemap.

3.  Click **+ New Case**.

4.  Enter  **SLA Test #1** for **Case Title** and select the **Relecloud** account for **Customer**.

5.  Select **Web** for **Origin**. In the Details tab, select **Problem** for Case Type. Click **Save**.

6.  Select the **SLA** tab. You should see the Case Response By SLA KPI in progress with failure time set to 1 hour's time.

7.  Select the **Details** tab and set **First Response Sent** to **Yes** and click **Save**.

8.  Select the **SLA** tab. You should see the Case Response By SLA KPI.

9.  Click **Go back**, click **+ New Case**.

10. Enter **SLA Test #2** for **Case Title** and select the **Relecloud** account for **Customer**.

11. Select **Email** for **Origin** and click **Save**.

12. Select the **SLA** tab. There should be no SLA KPI items.
