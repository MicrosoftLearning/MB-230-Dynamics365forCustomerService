---
lab:
    title: 'Lab 2: Power BI'
    module: 'Module 1: Customer Service Overview'
---

Module 1: Customer Service Overview
===================================

## Practice Lab 2 – Power BI

Scenario
--------

You are a business analyst working on the Dynamics 365 for Customer Service
implementation for your company, City Power & Light. Your users are very excited
to see their data shown through PowerBI and you are tasked with connecting your
Dynamics 365 for Customer Service to PowerBI and making some PowerBI elements
visible to your users. In this lab, you will enable and use PowerBI, add a
PowerBI dashboard to your environment and create a Dynamics 365 dashboard with
PowerBI tiles.

**Important Note:** This lab will provide you with an actual Dynamics 365 tenant
and licenses for the Power Platform applications you will be using in this
course. You will only be provided with one tenant for the practice labs in this
course. The settings and actions you take within this tenant do not roll-back or
reset, whereas the virtual machine you are provided with does reset each time
you close the lab session. Please be aware that Dynamics 365 is evolving all the time. The
instructions in this document may be different from what you experience in your
actual Dynamics 365 tenant. It is also possible to experience a delay of several
minutes before the virtual machine has network connectivity to begin the labs.

Exercise 1 - Acquire Tenant Information and Connect
---------------------------------------------------

**Note:** If you have already completed a practice recently, the virtual machine
might pick up where you left off and you will not need to login again.  In that
case you can skip ahead to exercise two and resume.
 
### Task 1 – Connect to the Power platform administration portal

1.  On Virtual machine MB200-Dynamics_Lab, sign in as Admin with the password
    Pa55w.rd if you are not already logged in.

2.  Outside the VM in the online lab interface click Files and choose D365
    Credentials. This will allocate an Office 365 tenant for you to use in these
    labs.  It will display the admin email and password for your tenant.  You
    should copy this information to notepad or similar for your reference.

3.  In MB200-Dynamics_Lab launch Microsoft Edge from the taskbar. By default,
    the browser opens Office 365. Use the O365 credentials you just acquired in
    the previous step to login.

4.  Navigate in the browser to the Power platform admin portal at
    [https://admin.Powerplatform.microsoft.com](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fadmin.Powerplatform.microsoft.com&data=02%7C01%7Cv-juya%40microsoft.com%7C4be5a28c6f1e41eefee808d687ae2dc7%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636845580068684293&sdata=cLrD%2FhTDb5sRbajtFR9RrztfyTDCo0xGS4k8FSxTaIc%3D&reserved=0)

Exercise 2 – Power BI with Dynamics 365
---------------------------------------

### Task 1 – Enable Power BI

1.  Navigate <https://admin.powerplatform.microsoft.com/>

2.  Expand **Admin Center** and select **Dynamics 365**.

3.  Select your instance and click **Open**.

4.  Navigate to **Settings > Administration**.

5.  Select **System Settings**.

6.  Select the **Reporting** tab and set **Allow Power BI Visualization
    Embedding** to **Yes**.

7.  Click **OK**.

8.  Click **Switch to Another App** and select **Customer Service Hub.**

9.  Click on the **Site Map** button and select **Dashboards**.

10. Click **New**. You will now have an option for creating **Power BI
    Dashboards**.

11. Click **New** and select **Power BI Dashboard**. You will get a message
    telling you to create power bi dashboard first.

12. Click **Cancel**.

13. Click **New** again and select **Dynamics 365 Dashboard**.

14. Select **2 Column Regular Dashboard** and click **Create**.

15. You should have an option for adding **Power BI Tile**.

16. Click **Add Power BI Tile**. You will get message telling you that you don’t
    have Power BI tiles or Dashboards.

17. Click **Cancel**.

18. Close the create dashboard window without saving it.

19. Click **Done**.

20. Do not close this browser window.

### Task 2 – Use Power BI Application

1.  Start a new browser window and navigate to <https://powerbi.microsoft.com/>

2.  Click **Sign in**.

3.  Click **Sign in** again to sign in with existing account.

4.  Click **Start**.

5.  Click **Skip**.

6.  Locate the **Services** tile and click **Get**.

7.  Locate or Search for **Customer Service Analytics for Dynamics 365** and
    click **Get it Now**.

8.  Enter for **URL**. Replace [Org Name] with your organization name.

9.  Click **Next**.

10. Select **OAuth2** for **Authentication Method** and click **Sign in**.

11. Provide your credentials.

12. Select Apps. You should see the application you connected to your
    organization.

13. Click on the **Customer Service Analytics for Dynamics 465** app. The
    dashboard will load.

14. Locate and click on the **Active Activities (Last 30 Days)** tile. The
    selected report will load.

15. Go to the **Activities Type** chart on the report and select **Task**. The
    report will reflect your selection.

16. Go to the **Activities by Status and Priority section** chart and select
    **Active**. The report will reflect your selection.

17. Select the **Active Cases in Organization** located on the bottom of the
    report.

18. Go ahead and explore the report.

### Task 3 – Add Power BI Dashboard to Dynamics 365 

1.  Go back to your **Customer Service Hub** application.

2.  Click **New** and select **Power BI Dashboard**.

3.  You should see the **Customer Service Analytics for Dynamics 365**
    dashboard. Select the **Customer Service Analytics for Dynamics 365**
    dashboard and click **Save**.

4.  The **Power BI Dashboard** should load in your **Dynamics 365**.

5.  Click on the **Total Active Cases** tile.

6.  Click **Open Power BI Report.**

7.  The report should load. Go to **Cases by Priority** chart and select
    **Normal**. The report should be interactive.

### Task 4 – Mix Power BI Tiles and Dynamics 365 

1.  Click on the **Site Map** button and select **Dashboards**.

2.  Click **New** and select **Dynamics 365 Dashboard**.

3.  Select **2-Column Regular Dashboard** and click **Create**.

4.  Click **Add Power BI Tile**. You should now be able to select individual
    tiles form the sample dashboard.

5.  Select **Total Active Cases** for **Tile** and Click **OK**.

6.  Click **Add Power BI Tile** again.

7.  Select **Active Cases by Location** for **Tile** and Click **OK**.

8.  Click Insert **Chart**.

9.  Select **Case** for **Record Type,** select **My Active Cases** for
    **View**, select **Active Cases by Agent** for **Chart** and click **Add**.

10. Select **Insert List**.

11. Select **Contacts** for **Record Type**, select **All Contacts** for
    **View** and click **Add**.

12. Click **Add Power BI Tile**.

13. Select **Cases by Priority** for **Tile** and click **OK**.

14. Enter **Mixed Dash** for **Name** and click **Save**.

15. Click **Close**.

16. The **Mixed Dash** should load.
