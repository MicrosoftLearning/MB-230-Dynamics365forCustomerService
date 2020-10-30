# MB-230: Connected Customer Service - Instructor Demos

# Instructor Led Demo 2

In this instructor led demonstration, you will create a Power Automate flow that
will get triggered on alert rule fired. The flow will create an IoT alert record
in Connected Customer Service.

## Task 1: Modify alert rule
-----------------------------

In this task, you modify the bin full alert rule.

1.  Navigate to [Azure Portal](https://portal.azure.com/) and click **All
    resources**.

2.  Search for smart and click to open **smart-trash** application you created.

3.  Click on the **IoT central application URL**.

4.  Select **Rules** and click to open the **Bin full alert**.

5.  Enable the alert and click **Save**.

6.  Scroll down to the **Condition** section and examine in what condition the
    alert will get fired. Bin full alert will get fired when the Fill level in
    more the 50, this is the max value you set for the Bin full alert threshold
    you set in exercise 1.

7.  Go to the **Actions** section and select **Microsoft Power Automate**.

8.  Click **Go**.

9.  Click on the **When a rule is fired** trigger.

10. Click **Sign in**.

11. Sign in with the azure credentials.

12. Select **smart-trash** for **Application**, select **Bin full alert** for
    **Rule**, rename the trigger **When bin full alert is fired**, and click **+
    New step**.

13. Search for create new record and select **Create a new record Common Data
    Service (current environment)**.

14. Click **Show advanced options.**

15. Select **IoT Alerts** for **Entity name**, click on the **Description**
    field and select **Device name** from the Dynamic content pane.

16. Type **: Surpassed the maximum fill level threshold, current fill level is**
    and select the second **Waste Bin monitors Fill level** from the Dynamic
    content pane.

17. Click on the **Device ID** field and select **Device ID** from the Dynamic
    content pane.

18. Rename the step **Create new IoT alert**.

19. Name the flow **Create bin full IoT alert** and click **Save**.

## Task 2: Test flow
---------------------

In this task, you will test the IoT alert flow you created.

1.  Navigate to [Power Apps maker portal](https://make.powerapps.com/) and make
    sure you are in the correct environment.

2.  Select **Apps** and click to launch the **Connected Field Service**
    application.

3.  Select **IoT Alerts** and **Refresh** the view until you see an alert
    record.

4.  Click to open the alert record.

5.  The **New IoT Alerts** tile should show at least 1 record. Click on the
    tile.

6.  The alerts should look like the image below. Close the popup window.

7.  Select Devices and click to open the test device.

8.  Select **Alerts** tab. You should see the alert as a related record here.

9.  Select **Customer Assets** and click to open the test record you created.

10. Click on the **Related** tab and select **IoT Alert**

11. You should see the alerts listed as related records here.

12. Select the **Summary** tab. The alerts should also show on the **New IoT
    Alerts** tile.

13. Go back to the IoT Central application, select **Rules** and click to open
    the **Bin full alert**.

14. Disable the rule and click **Save**. The maximum threshold is set to 50
    which too low, this will cause you to get too many alerts and consume a lot
    of resources.
