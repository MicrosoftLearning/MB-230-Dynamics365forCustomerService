---
demo:
    title: 'Demo: Set up Customer Service environment'
    module: 'Module 1: Case management'
---

# Demo - Set up Customer Service environment

**Note:** This is a **required prerequisite** to the students completing Module 1, Lab 1, Creating Cases. You may choose to do this demo as a live demo, or you may complete this demo prior to the course starting. If your students are encountering errors finding the products and data in Module 1, Lab 1, please confirm that you have done these steps correctly. 

## Scenario 

In this demo, you will use the Power Apps maker portal to publish the tables necessary for your students to complete your lab. 

## Exercise 1: Create demo data

### Task 1: Navigate to the Power Apps maker portal

1. Navigate to <make.powerapps.com> and log in using the tenant admin credentials you recieved from your Authorized Lab Hoster.

1. Using the environment selector, select your **WWLLABnnn** environment, where nnn is a number.

1. Once you have switched environments, select **Tables** from the left menu.

1. Find the **Products** table in the list of tables. Select the ellipses to open the table options.

1. Select **Publish.**

1. Wait for the table to publish. You can check your status by viewing the **Publish** button in the command bar.

### Task 2: Create products

1. Navigate to the **Apps** section. Select **Field Service.**

1. When the app opens, navigate to the areas and switch to **Settings.**

1. Select **Products.** Click **New Product.**

  - For **Name,** enter **JBO Top D. Hifi.**
  - For **Product ID**, enter **12345.**
  - Choose **Default Unit** for **Unit Group.**
  - Choose **Primary Unit** for **Default Unit.**
  - Enter **0** for **Decimals Supported.**
 
1. Select **Save.**

1. Select **Publish.**

### Task 3: Create Case Subjects 

1. Select **Field Service** at the top of the screen to open the list of available applications.

1. Select the **Customer Service admin center.**

1. In the **Customer support** section, select **Case settings.**

1. Under **Subjects**, select **Manage.**

1. Under **Subject tree management**, select **+Add.**
  - Enter **Service** for **Title.**
  - Leave **Parent subject** blank. 
  - Select **Save and close.**

1. Select **+Add** again to add another subject.
  - Enter **Maintenance** for **Title.**
  - Select **Service** for **Parent subject.**
  - Select **Save and close.**


