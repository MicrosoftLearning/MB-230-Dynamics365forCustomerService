**MB-230: Connected Customer Service - Instructor Demos**

**Instructor Demo 1**
=====================

In this instructor led demo, you will be walking student through the process of
deploying and configuring an IoT Central application that can be potentially be
used in conjunction with a Connected Customer Service implementation. In this
exercise, you will create an IoT central application and add two devices.

**Task 1: Create an IoT Central Application**
---------------------------------------------

1.  Navigate to [Azure Portal](https://portal.azure.com/) and click **+ Create a
    resource**.

2.  Search for iot central and select **IoT Central Application**.

3.  Click **Create**.

4.  Enter **smart-trash-fl** (replace **fl** with the first and last initials of
    your alias ie AS for alans) for **Resource Name**, provide a unique
    **Application URL** (use smarttrashMMDDYYInitials), select your
    subscription, and click **Create new Resource group**.

5.  Enter **smarttrashcontainerlab** for **Name** and click **OK**.

6.  Select **Standard 1** for **Pricing plan**, select **Connected Waste
    Management** for **Template**, select your **Location**, and click
    **Create**.

7.  Wait for the deployment to complete and click **Go to resource**.

8.  Open the application by clicking on the IoT Central Application URL.

9.  Select Devices. You should see one device group named **Connected Waste
    Bin** that has two sample devices.

10. Click **+ New**.

11. Select **Connected Waste Bin** for **Template type**, enter **19th Ave
    Location** for **Device name**, set **Simulate this device** to **Yes**, and
    click **Create**.

12. Click to open the **19th Ave Location** you just created.

13. Select the **Cloud Properties** tab, go to the **Trash bin install
    location** section, enter Microsoft building in the **Address** field, and
    select **Microsoft Building 4** from the suggested addresses.

14. The GPS coordinates should get auto filled. Click **Save**.

15. Select **Devices** and click **+ New** again

16. Select **Connected Waste Bin** for **Template type**, enter **35th St
    Location** for **Device name**, set **Simulate this device** to **Yes**, and
    click **Create**.

17. Click to open the **35th St Location** you just created.

18. Go to the **Trash bin install location** section, enter Microsoft in the
    **Address** field, and select **Microsoft Main Campus** from the suggested
    addresses.

19. The GPS coordinates should get auto filled. Click **Save**.

20. Do not navigate away from this page.

**Task 2: Tour IoT Central Application**
----------------------------------------

In this task, you will tour the IoT Central application.

1.  Select **Dashboard**.

2.  Templates come with a default dashboard, you can edit the default dashboard
    or create a new dashboard.

3.  The default dashboard is not showing information about the devices you
    added. Click **Edit**.

4.  Go to the map tile and click **Configure**.

5.  Go to the **Configure** pane and click on the **Devices** dropdown.

6.  Select the all the devices and click **Update**.

7.  Click **Save**.

8.  The map tile should now show all four location. The locations are simulated
    and refreshed often.

9.  You may edit other tiles.

10. Select **Devices** and click to open the **35th St Location** device.

11. Select the Cloud properties. Here, you can provide more information about
    the device and edit the device alert thresholds.

12. Select the Divce dashboard tab. This is a device specific dashboard that
    comes with the connected waste bin template.

13. Select the **Device properties** tab. This tab shows information including
    the device model, manufacturer, type, and location.

14. Select the **Raw data** tab. This tab shows raw unprocessed data received
    form the in the last 7 days. Click to expand one of the records.

15. Click **Filter**.

16. You can show all message types, just telemetry message type, or Property
    message type. Click **Edit time range**.

17. Click on the **Time range selection** dropdown. You can select to show one
    of the ranges provided or create a custom range.

18. Select **Custom**.

19. Here, you can create a custom range. Click **Cancel**.

20. Do not navigate away from this page.

**Task 3: Set bin full alert threshold**
----------------------------------------

In this task, you will set the minimum and maximum bin full threshold.

1.  Select **Device Templates** and click to open the **Connect Waste Bin
    template**.

2.  Templates come with a default dashboard, you can edit the default dashboard
    or create a new dashboard.

3.  Select **Cloud properties**.

4.  Locate the **Bin full alert threshold** and click **Expand**.

5.  Enter **10** for **Min value**, **50** for **Max value**, and click
    **Save**.

6.  Click **Publish** to publish your changes.

7.  Click Publish again to confirm.
