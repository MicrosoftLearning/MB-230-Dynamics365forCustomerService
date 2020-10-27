# Exercise 1: Define Services 

In this exercise, define oil change and tire rotation services.

## Task 1: Create Oil Change Service
-------------------------------------

In this task you will create an oil change service.

1.  Navigate to [Power Apps maker portal](https://make.powerapps.com) and make
    sure you are in the correct environment.

2.  Select **Apps** and click to open the **Customer Service Hub** application.

3.  Select **Services** and click **+ New**.

4.  Enter **Oil Change** for **Name** and click **Save**.

5.  Select the **Resource Requirements** tab, change the **Name** to **Oil
    Change**, select **All** for **Select**, and select **Organizational Unit**
    for **Part of Same**.

6.  Click **+ Requirement**.

7.  Enter **Service Technician** for **Name** and select **Technician** for
    **Resource Category**.

8.  Select the **Oil Change** row and click **+ Requirement**.

9.  Enter **Service Bay** for **Name**, select **Service Bay Facility** for
    **Resource Category**, and click + **New** again.

10. Enter **Tire Rotation** for **Name** and click **Save**.

11. Select the **Resource Requirements** tab, change the **Name** to **Tire
    Rotation**, select **All** for **Select**, and select **Organizational
    Unit** for **Part of Same**.

12. Click **+ Requirement**.

13. Enter **1 hour** for **Duration**.

14. Enter **Senior Technician** for **Name** and select **Senior Technician**
    for **Resource Category**.

15. Select the **Tire Rotation** row and click **+ Requirement**.

16. Enter **Service Bay** for **Name** and select **Service Bay Facility** for
    **Resource Category**.

17. Select the **Tire Rotation** row and click **+ Requirement**.

18. Enter **Service Technician** for **Name** and select **Technician** for
    **Resource Category**.

19. Select the **Tire Rotation** row and click **+ Requirement**.

20. Enter **Tire Jack** for **Name** and select **Tire Jack Equipment** for
    **Resource Category**.

21. The **Tire Rotation** service should now have **4** requirements.

# Exercise 2: Create and Schedule Service Activities 

In this exercise, you create and schedule service activities for an oil change
and a tire rotation.

## Task 1: Create Oil Change Service
-------------------------------------

In this task you will create and schedule an oil change service activity.

1.  Navigate to [Power Apps maker portal](https://make.powerapps.com) and make
    sure you are in the correct environment.

2.  Select **Apps** and click to open the **Customer Service Hub** application.

3.  Select **Service Activities** and click create **Service Activity**.

4.  Enter **Oil Change Service** for **Subject**, select **Oil Change** for
    **Service**, select **Main Ave Location** for **Organizational Unit**, and
    click **Save**.

5.  Click **Book**.

6.  Go to the **Filter View**, select **Main Ave Location** for **Organizational
    Unit**, and click **Search**.

7.  Expand one of the available slots and see what resources are included in it.
    In our case Service Bay 1 and Jennifer Leary will be included.

8.  Go to the Resources pane and click on the Start date picker.

9.  Select a data one week from today. The rest of the dates will change to
    reflect the change you made.

10. Click **Book & Exit**.

11. Refresh the service activity record.

12. The status should now change form **Requested** to **Reserved**.

13. Select the **Bookings** tab. You should see the booked resources for this
    service activity.

14. Select **Scheduling**, select **Main Ave Location** for **Organizational
    Units** and click **Search**.

15. Select **Horizontal View** and click on the date picker.

16. Select the date you booked the **Oil Change** service activity.

17. **Jennifer Leary** and **Service Bay 1** should show as booked for **30**
    minutes. Click on the **Jennifer Leary’s** booking.

18. Go to the Details pane. You should see more information about the booking.
