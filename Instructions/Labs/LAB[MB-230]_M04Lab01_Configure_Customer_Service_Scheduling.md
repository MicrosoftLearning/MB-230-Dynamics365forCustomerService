---
lab:
    title: 'Lab: Configure Customer Service Scheduling'
    module: 'Module 4: Implement routing and scheduling'
---

# Practice Lab - Configure Customer Service Scheduling

## Scenario

You are the scheduling manager at City Power & Light who has been tasked with setting up the new Service Scheduling functionality to perform services for customers at three of your locations. This exercise should take approximately 20 minutes to complete. 

## Exercise 1: Configure Customer Service Scheduling

In this exercise, you will create organizational units, define a business closure, and create facility/equipment records for organization units.

### Task 1: Define Organization Units

In this task, you will define three organizational units to act as service locations for scheduling.

1.  Open the **Customer Service Hub** app.

2.  Click **Settings** and select **Personalization Settings**.

3.  Select your **Time Zone** and click **OK**.

4.  Click on **Home** at the top of the left-hand side navigation.

5.  Click on **Service** at the bottom of the **Site Map** in the left-hand navigation and select **Scheduling**.

6. Click on (hierarchy icon) **Organization Units** in the **Settings** section.

7.  Click **+ New**.

8. Enter **Main Ave Location** for **Name**. Click on the **Scheduling** tab and enter a valid number for both Latitude and Longitude. 

9. Click **Save and Close**.

10. Create two more **Sites** with the values listed in the table below.

 -19th Ave Location 
 
 -35th St Location 

11. You should now have three Sites.

12. Do not navigate away from this application.

## Task 2: Define Business Closure

In this task, you will define a new business closure.

1.  Click on **Business Closures** in the **Settings** section.

2.  Click **+ New**.

3.  Enter **Worldwide Rest Day** for **Name**, select a date one week from now for **Start Date**, and click **OK**.

4.  Do not navigate away from this application.

## Task 3: Create Facilities/Equipment Records

In this task, you will create facilities/equipment records for the organizational units you created and set their working hours.

1.  Click on **Facilities/Equipment** in the **Scheduling** section.

2.  Click **+ New**.

3.  Enter **Main Ave** - **Service Bay 1** for **Name**, select **Main Ave Location** for **Organizational Unit**, select a *Time Zone**, select the root **Business Unit**, and click **Save**.

4.  Select the **Work Hours** tab, click on one of the events listed on the calendar, click **Edit**, and select **All events in the series**.

5.  Select **08:00 AM to 08:00 PM**, remove **Saturday** and **Sunday**, and click **Remove end date**, if there is an end date selected.

6.  Toggle **Observe Business Closure** to **On**

7.  Click **Save** to save the working hours.

8.  Click **Save and Close**.

9.  Click **+ New**.

10. Enter **Main Ave - Service Bay 2** for **Name**, select **Main Ave Location** for **Organizational Unit**, select your **Time Zone**, select the root **Business Unit**, and click **Save**.

11. Select the **Work Hours** tab, click on one of the events listed on the calendar, click **Edit**, and select **All events in the series**.

12. Select **08:00 AM to 08:00 PM**, remove **Saturday** and **Sunday**, click **Remove end date** if one is selected, and click Save.

13. Toggle **Observe Business Closure** to **On**

14. Click **Save** to save the working hours, and then click **Save and Close**.

15. Repeat the previous 5 steps and create the **Facilities/Equipment** listed in the table below.

| **Name**                 | **Organizational Unit** | **Time Zone**  | **Business Unit**  | **Working Hours**        |
|--------------------------|-------------------------|----------------|--------------------|--------------------------|
| Main Ave - Tire Jack     | Main Ave Location       | Your time zone | Root business unit | Mon-Fri 8:00AM to 8:00PM |
| 19th Ave - Service Bay 1 | 19th Ave Location       | Your time zone | Root business unit | Mon-Fri 8:00AM to 8:00PM |
| 19th Ave - Service Bay 2 | 19th Ave Location       | Your time zone | Root business unit | Mon-Fri 8:00AM to 8:00PM |
| 19th Ave - Tire Jack     | 19th Ave Location       | Your time zone | Root business unit | Mon-Fri 8:00AM to 8:00PM |
| 35th St - Service Bay 1  | 35th St Location        | Your time zone | Root business unit | Mon-Fri 8:00AM to 8:00PM |
| 35th St - Service Bay 2  | 35th St Location        | Your time zone | Root business unit | Mon-Fri 8:00AM to 8:00PM |
| 35th St - Tire Jack      | 35th St Location        | Your time zone | Root business unit | Mon-Fri 8:00AM to 8:00PM |

16. You should now have total of 9 Facilities/Equipment records.

## Exercise 2: Resource Configuration

In this exercise, you will create contact records, create resource categories, and create resources.

### Task 1: Create Contacts

In this task you will create new contact records.

1.  Open the **Customer Service Hub** app.

2.  Click on **Home** at the top of the left-hand side navigation.

3.  Click on **Contacts** in the **Customers** section.

4.  Click **+ New**.

5.  Enter **Mike** for **First Name**, **Smith** for **Last Name**, and click **Save and Close**.

6.  Repeat the previous two steps and create the **Contact** records listed in the table below.

| **First Name** | **Last Name** |
|----------------|---------------|
| Jennifer       | Leary         |
| Judy           | Anderson      |
| Allan          | Jackson       |
| Sven           | Locarte       |
| Alex           | Nelson        |

7.  You should now have six contact records.

8.  Do NOT navigate away from this application.

## Task 2: Create Resource Categories

In this task you will create new resource categories.

1.  Click on **Service** at the bottom of the **Site Map** in the left-hand navigation and select **Scheduling**.

2.  Click on **Resource Categories** in the **Scheduling** section.

3.  Click **+ New**.

4.  Enter **Senior Technician** for **Name** and click **Save and Close**.

5.  Click **+ New**.

6.  Enter **Technician** for **Name** and click **Save and Close**.

7.  Create two more **Resource Categories** and name them **Service Bay Facility** and **Tire Jack Equipment**.

8.  You should now have 4 **Resource Categories**.

9.  Do NOT navigate away from this application.

## Task 3: Create Resources

In this task you will create resources using the contacts you created.

1.  Click on **Resources** in the **Scheduling** section.

2.  Click **+ New**.

3.  Select **Contact** for **Resource Type**, select **Mike Smith** for **Contact**, and select the **Scheduling** tab.

4.  Select **Organizational Unit Address** for **Start** and **End Locations**, select **Main Avenue Location** for **Organizational Unit**, and click
    **Save**.

5.  Select the **Work Hours** tab, click on one of the events on the calendar, click **Edit**, and select **All events in the series**.

6.  Select **08:00 AM** to **04:30 PM** and click **Add Break**.

7.  Remove **Saturday** and **Sunday**, select **Observe Business Closure**, then click **Save**.

8.  Select the **General** tab.

9.  Select the **Related** tab and select **Resource Category Assns**  and click **+ New Bookable Resource Category Assn**.

10. Select **Senior Technician** and click **Save and Close**.

11. Repeat the previous 9 steps and create the resources listed in the table below.

| **Resource Type** | **Contact**    | **Start and End Locations** | **Organizational unit** | **Work Hours**                                               | **Resource Category Assn** |
|-------------------|----------------|-----------------------------|-------------------------|--------------------------------------------------------------|----------------------------|
| Contact           | Judy Anderson  | Organizational Unit Address | 19th Ave Location       | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Senior Technician          |
| Contact           | Sven Locarte   | Organizational Unit Address | 35th St Location        | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Senior Technician          |
| Contact           | Jennifer Leary | Organizational Unit Address | Main Avenue Location    | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Technician                 |
| Contact           | Allan Jackson  | Organizational Unit Address | 19th Ave Location       | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Technician                 |
| Contact           | Alex Nelson    | Organizational Unit Address | 35th St Location        | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Technician                 |

12. You should now have 6 resources. Click **+ New**.

13. Select **Facility** for **Resource Type**, select **19th Ave – Service Bay 1** for **Facility Equipment**, and select the **Scheduling** tab.

14. Select **Organizational Unit Address** for **Start** and **End Locations**, and then click **Save**.

15. Select the **General** tab.

16. Select the **Related** tab and select **Resource Category Assns**  and click **+ New Bookable Resource Category Assn**.

17. Select **Service Bay Facility** and click **Save and Close**.

18. Repeat the previous 3 steps and create the resources listed in the table below.

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

19. You should now have 15 Resources.
