# MB-230: Customer Service Scheduling

# Exercise 1: Configure Customer Service Scheduling
=====================================================

In this exercise, you will create business units, define a business closure,
create facility/equipment records for organization units, and create resources.

## Task 1: Define Organization Units
-------------------------------------

1.  Navigate to [Power Apps maker portal](https://make.powerapps.com) and make
    sure you are in the correct environment.

2.  Select **Apps** and click to open the **Customer Service Hub** application.

3.  Click **Settings** and select **Personalize Settings**.

4.  Select your **Time Zone** and click **OK**.

5.  Click **Change area** and select The **Scheduling** area.

6.  Go to the **Settings** group and select **Organizational Units**.

7.  Click **+ New**.

8.  Enter **Main Ave Location** for **Name** and select the **Scheduling** tab.

9.  Enter **47.63993** for Latitude, **-122.12557** for Longitude and click
    **Save and Close**. You may use different GPS locations but make sure they
    are valid locations.

10. Create two more **Organizational Units** with the values listed in the table
    below.

| **Name**          | **Latitude** | **Longitude** |
|-------------------|--------------|---------------|
| 19th Ave Location | 47.63962     | \-122.12853   |
| 35th St Location  | 47.64284     | \-122.13009   |

11. You should now have three Organizational Units.

12. Do not navigate away from this application.

## Task 2: Define Business Closure
-----------------------------------

In this task, you will define a new business closure.

1.  Select **Business Closures**.

2.  Click **+ New**.

3.  Enter **Worldwide Rest Day** for **Name**, select a date one week from now
    for **Start Date**, and click **OK**.

4.  Do not navigate away from this application.

## Task 3: Create Facilities/Equipment Records
-----------------------------------------------

In this task, you will create facilities/equipment records for the
organizational units you created and set their working hours.

1.  Select **Facilities/equipment** and click **+ New**.

2.  Enter **Main Ave** - **Service Bay 1** for **Name**, select **Main Ave
    Location** for **Organizational Unit**, select a **Time Zone**, select
    **Business Unit**, and click **Save**. This is the default business unit
    that gets created automatically.

3.  Select the **Work Hours** tab, click on one of the events listed on the
    calendar, click **Edit**, and select **All events in the series**.

4.  Select **08:00 AM to 08:00 PM**, remove **Saturday** and **Sunday**, and
    click **Remove end date**, if there is an end date selected.

5.  Click **Save** to save the working hours.

6.  Click **Save and Close**.

7.  Click **+ New** again.

8.  Enter **Main Ave - Service Bay 2** for **Name**, select **Main Ave
    Location** for **Organizational Unit**, select your **Time Zone**, select
    your **Business Unit**, and click **Save**.

9.  Select the **Work Hours** tab, click on one of the events listed on the
    calendar, click **Edit**, and select **All events in the series**.

10. Select **08:00 AM to 08:00 PM**, remove **Saturday** and **Sunday**, click
    **Remove end date** if one is selected, and click Save.

11. Click **Save and Close**.

12. Repeat the previous 5 steps and create the **Facilities/Equipment** listed
    in the table below.

| **Name**                 | **Organizational Unit** | **Time Zone**  | **Business Unit**  | **Working Hours**        |
|--------------------------|-------------------------|----------------|--------------------|--------------------------|
| Main Ave - Tire Jack     | Main Ave Location       | Your time zone | Your business unit | Mon-Fri 8:00AM to 8:00PM |
| 19th Ave - Service Bay 1 | 19th Ave Location       | Your time zone | Your business unit | Mon-Fri 8:00AM to 8:00PM |
| 19th Ave - Service Bay 2 | 19th Ave Location       | Your time zone | Your business unit | Mon-Fri 8:00AM to 8:00PM |
| 19th Ave - Tire Jack     | 19th Ave Location       | Your time zone | Your business unit | Mon-Fri 8:00AM to 8:00PM |
| 35th St - Service Bay 1  | 35th St Location        | Your time zone | Your business unit | Mon-Fri 8:00AM to 8:00PM |
| 35th St - Service Bay 2  | 35th St Location        | Your time zone | Your business unit | Mon-Fri 8:00AM to 8:00PM |
| 35th St - Tire Jack      | 35th St Location        | Your time zone | Your business unit | Mon-Fri 8:00AM to 8:00PM |

13. You should now have total of 9 Facilities/Equipment records.

# Exercise 2: Resource Configuration
======================================

In this exercise, you will create contact records, create resource categories,
and create resources.

## Task 1: Create Contacts
---------------------------

In this task you will create new contact records.

1.  Navigate to [Power Apps maker portal](https://make.powerapps.com) and make
    sure you are in the correct environment.

2.  Select **Apps** and click to open the **Customer Service Hub** application.

3.  Click **Change area** and select The **Service** area if not already
    selected.

4.  Select **Contacts** and click **+ New**.

5.  Enter **Mike** for **First Name**, **Smith** for **Last Name**, and click
    **Save and Close**.

6.  Repeat the previous two and create the **Contact** records listed in the
    table below.

| **First Name** | **Last Name** |
|----------------|---------------|
| Jennifer       | Leary         |
| Judy           | Anderson      |
| Allan          | Jackson       |
| Sven           | Locarte       |
| Alex           | Nelson        |

7.  You should now have six contact records.

8.  Do not navigate away from this application

## Task 2: Create Resource Categories
--------------------------------------

In this task you will create new resource categories.

1.  Click **Change area** and select The **Scheduling** area.

2.  Go to the **Resource Categories** and click **+ New**.

3.  Enter **Senior Technician** for **Name** and click **Save and Close**.

4.  Click **+ New again**.

5.  Enter **Technician** for **Name** and click **Save and Close**.

6.  Create two more **Resource Categories** and name them **Service Bay
    Facility** and **Tire Jack Equipment**.

7.  You should now have 4 **Resource Categories**.

8.  Do not navigate away from this application.

## Task 3: Create Resources
----------------------------

In this task you will create new contact type resources.

1.  Select **Resources** and click **+ New**.

2.  Select **Contact** for **Resource Type**, select **Mike Smith** for
    **Contact**, and select the **Scheduling** tab.

3.  Select **Organizational Unit Address** for **Start** and **End Locations**,
    select **Main Avenue Location** for **Organizational Unit**, and click
    **Save**.

4.  Select the **Work Hours** tab, click on one of the events on the calendar,
    click **Edit**, and select **All events in the series**.

5.  Select **08:00 AM** to **04:30 PM** and click **Add Break**.

6.  Remove **Saturday** and **Sunday**, select **Observe Business Closure**,
    then click **Save**.

7.  Select the **General** tab.

8.  Go to the Resource Categories sub-grid and click + New Bookable Resource
    Category Assn.

9.  Select **Senior Technician** and click **Save and Close**.

10. Repeat the previous 9 steps and create the resources listed in the table
    below.

| **Resource Type** | **Contact**    | **Start and End Locations** | **Organizational unit** | **Work Hours**                                               | **Resource Category Assn** |
|-------------------|----------------|-----------------------------|-------------------------|--------------------------------------------------------------|----------------------------|
| Contact           | Judy Anderson  | Organizational Unit Address | 19th Ave Location       | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Senior Technician          |
| Contact           | Sven Locarte   | Organizational Unit Address | 35th St Location        | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Senior Technician          |
| Contact           | Jennifer Leary | Organizational Unit Address | Main Avenue Location    | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Technician                 |
| Contact           | Allan Jackson  | Organizational Unit Address | 19th Ave Location       | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Technician                 |
| Contact           | Alex Nelson    | Organizational Unit Address | 35th St Location        | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Technician                 |

11. You should now have 6 resources. Click **+ New**.

12. Select **Facility** for **Resource Type**, select **19th Ave – Service Bay
    1** for **Facility Equipment**, and select the **Scheduling** tab.

13. Select **Organizational Unit Address** for **Start** and **End Locations**,
    and then click **Save**.

14. Select the **General** tab.

15. Go to the Resource Categories sub-grid and click + New Bookable Resource
    Category Assn.

16. Select **Service Bay Facility** and click **Save and Close**.

17. Repeat the previous 3 steps and create the resources listed in the table
    below.

| **Resource Type** | **Facility Equipment**   | **Start and End Locations** | **Resource Category Assn** |
|-------------------|--------------------------|-----------------------------|----------------------------|
| Facility          | 19th Ave – Service Bay 2 | Organizational Unit Address | Service Bay Facility       |
| Facility          | 35th St – Service Bay 1  | Organizational Unit Address | Service Bay Facility       |
| Facility          | 35th St – Service Bay 2  | Organizational Unit Address | Service Bay Facility       |
| Facility          | Main Ave – Service Bay 1 | Organizational Unit Address | Service Bay Facility       |
| Facility          | Main Ave – Service Bay 2 | Organizational Unit Address | Service Bay Facility       |
| Equipment         | 19th Ave – Tire Jack     | Organizational Unit Address | Tire Jack Equipment        |
| Equipment         | 35th St – Tire Jack      | Organizational Unit Address | Tire Jack Equipment        |
| Equipment         | Main Ave – Tire Jack     | Organizational Unit Address | Tire Jack Equipment        |

18. You should now have 15 Resources.

# Exercise 3: Define Services 
================================

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

# Exercise 4: Create and Schedule Service Activities 
=======================================================

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
