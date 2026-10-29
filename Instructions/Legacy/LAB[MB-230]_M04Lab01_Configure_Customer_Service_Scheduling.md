---
lab:
  title: 'Lab: Configure Customer Service Scheduling'
  module: 'Module 4: Implement routing and scheduling'
  description: In this task you will create new contact records.
  duration: 20 minutes
  level: 100
  islab: true
---

# Practice Lab - Configure Customer Service Scheduling

> [!NOTE]
> This lab is archived because service scheduling isn't part of the current MB-230 course. Its procedures haven't been validated for the current product experience.

## Scenario

You are the scheduling manager at City Power & Light who has been tasked with setting up the new Service Scheduling functionality to perform services for customers at three of your locations. This exercise should take approximately 20 minutes to complete. 

## Exercise 1: Configure Customer Service Scheduling

In this exercise, you will create organizational units, define a business closure, and create facility/equipment records for organization units.

### Task 1: Define Organization Units

In this task, you will define three organizational units to act as service locations for scheduling.

1. Open the **Customer Service Hub** app.

2. Select **Settings** and select **Personal Settings**.

3. Select your **Time Zone** and select **Save**.

4. Select **Home** at the top of the left-hand side navigation.

5. Select **Service** at the bottom of the **Site Map** in the left-hand navigation and select **Scheduling**.

6. Select (hierarchy icon) **Organizational Units** in the **Settings** section.

7. Select **+ New**.

8. Enter **Main Ave Location** for **Name**. Select the **Scheduling** tab and enter a valid number for both **Latitude** and **Longitude** (for example, 47.6062 for **Latitude** and -122.3321 for **Longitude**). 

9. Select **Save & Close**.

10. Create two more **Sites** with the values listed in the table below.

 -19th Ave Location 
 
 -35th St Location 

11. You should now have three Sites.

12. Do not navigate away from this application.

## Task 2: Define Business Closure

In this task, you will define a new business closure.

1. Select **Business Closures** in the **Settings** section.

2. Select **+ New**.

3. Enter **Worldwide Rest Day** for **Name**, select a date one week from now for **Start Date**, and select **OK**.

4. Do not navigate away from this application.

## Task 3: Create Facilities/Equipment Records

In this task, you will create facilities/equipment records for the organizational units you created and set their working hours.

1. Select **Facilities/Equipment** in the **Scheduling** section.

2. Select **+ New**.

3. Enter **Main Ave** - **Service Bay 1** for **Name**, select **Main Ave Location** for **Organizational Unit**, select a **Time Zone**, select the root **Business Unit**, and select **Save**.

4. Select the **Work Hours** tab, select one of the events listed on the calendar, select **Edit**, and select **All events in the series**.

5. Select **08:00 AM to 08:00 PM**, remove **Saturday** and **Sunday**. If an end date is configured, select **Remove end date**.

6. Toggle **Observe Business Closure** to **On**

7. Select **Save** to save the working hours.

8. Select **Save & Close**.

9. Select **+ New**.

10. Enter **Main Ave - Service Bay 2** for **Name**, select **Main Ave Location** for **Organizational Unit**, select your **Time Zone**, select the root **Business Unit**, and select **Save**.

11. Select the **Work Hours** tab, select one of the events listed on the calendar, select **Edit**, and select **All events in the series**.

12. Select **08:00 AM to 08:00 PM**, remove **Saturday** and **Sunday**, select **Remove end date** if one is selected, and select **Save**.

13. Toggle **Observe Business Closure** to **On**

14. Select **Save** to save the working hours, and then select **Save & Close**.

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

16. You should now have total of 8 Facilities/Equipment records.

## Exercise 2: Resource Configuration

In this exercise, you will create contact records, create resource categories, and create resources.

### Task 1: Create Contacts

In this task you will create new contact records.

1. Open the **Customer Service Hub** app.

2. Select **Home** at the top of the left-hand side navigation.

3. Select **Contacts** in the **Customers** section.

4. Select **+ New**.

5. Enter **Mike** for **First Name**, **Smith** for **Last Name**, and select **Save & Close**.

6. Repeat the previous two steps and create the **Contact** records listed in the table below.

| **First Name** | **Last Name** |
|----------------|---------------|
| Jennifer       | Leary         |
| Judy           | Anderson      |
| Allan          | Jackson       |
| Sven           | Locarte       |
| Alex           | Nelson        |

7. You should now have six contact records.

> [!NOTE] 
> Your list might also include sample contacts that already exist in the environment, so the total number of records might be higher than six.

8. Stay in the **Customer Service Hub** app. You'll continue working in it in the next tasks.

## Task 2: Create Resource Categories

In this task you will create new resource categories.

1. Select **Service** at the bottom of the **Site Map** in the left-hand navigation and select **Scheduling**.

2. Select **Resource Categories** in the **Scheduling** section.

3. Select **+ New**.

4. Enter **Senior Technician** for **Name** and select **Save & Close**.

5. Select **+ New**.

6. Enter **Technician** for **Name** and select **Save & Close**.

7. Create two more **Resource Categories** and name them **Service Bay Facility** and **Tire Jack Equipment**.

8. You should now have 4 **Resource Categories**.

9. Stay in the **Customer Service Hub** app.

## Task 3: Create Resources

In this task you will create resources using the contacts you created.

1. Select **Resources** in the **Scheduling** section.

2. Select **+ New**.

3. Select **Contact** for **Resource Type**, select **Mike Smith** for **Contact**, and select the **Scheduling** tab.

4. Select **Organizational Unit Address** for **Start Location** and **End Location**, select **Main Ave Location** for **Organizational Unit**, and select **Save**.

5. Select the **Work Hours** tab, select one of the events on the calendar, select **Edit**, and select **All events in the series**.

6. Set **Start time** to **8:00 AM** and **End time** to **4:30 PM**.

7. Select the ellipsis **(...)** next to **Capacity**, and then select **Add break**.

8. Remove **Saturday** and **Sunday**, select **Observe Business Closure**, select **Save**, and then select **OK**.

9. Select the **General** tab.

10. Select the **Related** tab, select **Resource Category Associations**,  and select **+ New Bookable Resource Category Assn**.

11. Select **Senior Technician** for **Resource Category**, and select **Save and Close**.

12. Repeat the previous 10 steps and create the resources listed in the table below.

| **Resource Type** | **Contact**    | **Start and End Locations** | **Organizational unit** | **Work Hours**                                               | **Resource Category Assn** |
|-------------------|----------------|-----------------------------|-------------------------|--------------------------------------------------------------|----------------------------|
| Contact           | Judy Anderson  | Organizational Unit Address | 19th Ave Location       | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Senior Technician          |
| Contact           | Sven Locarte   | Organizational Unit Address | 35th St Location        | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Senior Technician          |
| Contact           | Jennifer Leary | Organizational Unit Address | Main Avenue Location    | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Technician                 |
| Contact           | Allan Jackson  | Organizational Unit Address | 19th Ave Location       | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Technician                 |
| Contact           | Alex Nelson    | Organizational Unit Address | 35th St Location        | Mo – Fr 08:00AM to 04:30 PM + Break Observe Business Closure | Technician                 |

13. You should now have 6 resources. Select **+ New**.

> [!NOTE] 
> Your list might also include other resources that already exist in the environment, such as **Trial User**.

14. Select **Facility** for **Resource Type**, select **19th Ave – Service Bay 1** for **Facility Equipment**, and select the **Scheduling** tab.

15. Select **Organizational Unit Address** for **Start Location** and **End Location**, and then select **Save**.

16. Select the **General** tab.

17. Select the **Related** tab and select **Resource Category Associations**  and select **+ New Bookable Resource Category Assn**.

18. Select **Service Bay Facility** for **Resource Category** and select **Save and Close**.

19. Repeat the previous 6 steps and create the resources listed in the table below.

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

20. You should now have 15 Resources.
