---
lab:
  title: 'Lab: Define Services'
  module: 'Module 4: Implement routing and scheduling'
  description: In this task you will create an oil change service.
  duration: 15 minutes
  level: 100
  islab: true
---

# Practice Lab - Define services

> [!NOTE]
> This lab is archived because service scheduling isn't part of the current MB-230 course. Its procedures haven't been validated for the current product experience.

## Scenario

You are the scheduling manager at City Power & Light who has been tasked with testing the Service Scheduling functionality to perform services for customers at your locations. This exercise should take approximately 15 minutes to complete. 

## Exercise 1: Define Services

In this exercise, you will define oil change and tire rotation services.

### Task 1: Create Oil Change Service

In this task you will create an oil change service.

1. Open the **Customer Service Hub** app.

2. Select **Home** at the top of the left-hand side navigation.

3. Select **Service** at the bottom of the **Site Map** in the left-hand navigation and select **Scheduling**.

4. Select **Services** in the **Scheduling** section.

5. Select **+ New**.

6. Enter **Oil Change** for **Name** and select **Save**.

7. Select the **Resource Requirements** tab, change the **Name** to **Oil Change**, select **All** for **Select**, and select **Organizational Unit** for **Part of Same**.

8. Select **+ Requirement**.

9. Enter **30 minutes** for **Duration**.

10. Enter **Service Technician** for **Name** and select **Technician** for **Resource Categories**.

11. Select the **Oil Change** row and select **+ Requirement**.

12. Enter **Service Bay** for **Name**, select **Service Bay Facility** for **Resource Categories**

13. Select **Save**

### Task 2: Create Tire Service

1. Select + **New** in the command bar.

2. Enter **Tire Rotation** for **Name** and select **Save**.

3. Select the **Resource Requirements** tab, change the **Name** to **Tire Rotation**, select **All** for **Select**, and select **Organizational Unit** for **Part of Same**.

4. Select **+ Requirement**.

5. Enter **1 hour** for **Duration**.

6. Enter **Senior Technician** for **Name** and select **Senior Technician** for **Resource Categories**.

7. Select the **Tire Rotation** row and select **+ Requirement**.

8. Enter **Service Bay** for **Name** and select **Service Bay Facility** for **Resource Categories**.

9. Select the **Tire Rotation** row and select **+ Requirement**.

10. Enter **Service Technician** for **Name** and select **Technician** for **Resource Categories**.

11. Select the **Tire Rotation** row and select **+ Requirement**.

12. Enter **Tire Jack** for **Name** and select **Tire Jack Equipment** for **Resource Categories**.

13. The **Tire Rotation** service should now have **4** requirements.

14. Select **Save**.

## Exercise 2: Create and schedule Service activities 

In this exercise, you create and schedule service activities for an oil change and a tire rotation.

### Task 1: Schedule Oil Change Service

In this task you will create and schedule an oil change service activity.

1. Open the **Customer Service Hub** app.

2. Select **Home** at the top of the left-hand side navigation.

3. Select **Service** at the bottom of the **Site Map** in the left-hand navigation and select **Scheduling**.

4. Select **Service Activities** in the **Scheduling** section.

5. Select **Service Activity**.

6. Enter **Oil Change Service** for **Subject**, select **Oil Change** for **Service**, select **Main Ave Location** for **Organizational Unit**, and
   select **Save**.

7. Select **Book**.

8. Select **Filters**. Select **Main Ave Location** for **Organizational Unit**, and select **Search**.

9. Select the arrow next to one of the available slots to expand it and view the resources it includes. For example, **Service Bay 2** and **Jennifer Leary**.

10. Select the first slot, and on the **Create Booking** pane, select the **calendar icon** next to **Estimated Arrival Date**.

11. Select a data one week from today. The rest of the dates will change to reflect the change you made.

12. Select **Book & Exit**.

13. Refresh the service activity record.

14. The status should now change form **Requested** to **Scheduled**.

15. Select the **Bookings** tab. You should see the booked resources for this service activity.

16. Select **Scheduling** in the **Tools** section.

17. Select **Main Ave Location** for **Organizational Units** and select **Apply**.

18. On the toolbar, make sure the view dropdown is set to **Gantt** (the horizontal timeline view). Then select the **date range** (calendar icon) next to today´s date to open the date picker.

19. Select the date you booked the **Oil Change** service activity.

20. **Jennifer Leary** and **Service Bay 2** should show as booked for **30** minutes. Select the **Jennifer Leary’s** booking.

21. Go to the **Details panel** on the right. You should see more information about the booking.
