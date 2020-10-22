# Omnichannel for Customer Service

## Instructor Demo 1

In this instructor led demo, you will be walking through how to configure some
of the more common elements in Omnichannel for Customer Service. The Instructor
led is particularly important for this class since, the students will be using a
shared lab environment. The items that you will be configuring in this demo will
be leveraged by students as they work through the Hands-on-Labs.

There is a pre-recorded click through demo that you can use during actual class
room presentation, but it is highly recommended that you still walk through the
demo to make sure that everything is configured for the environment that you are
teaching out of at that time.

## Before Class Begins

If Omnichannel for Customer service is not already set up in your environment,
you will need to deploy the application and create some sample users that can be
used as part of the course. If possible, this process should be completed at
least the night before class since it can take several hours from Omnichannel
for Customer Service to deploy.

## Task 1: Deploy Omnichannel for Customer Service

1.  Navigate <https://admin.powerplatform.microsoft.com>.

2.  In the **Power Platform admin center**, expand **Resources** and, select
    Dynamics 365 apps.

3.  Scroll down and select Omnichannel for Customer Service. *(If you have more
    than one, that’s OK. They will all take you to the same spot.)* Click
    **Manage**.

4.  Select **OK** to go to the Dynamics 365 apps admin page. If you are asked to
    sign in, use the credentials that you are currently logged in with.

    *You will be taken to an Omnichannel Provisioning consent screen. You will
    need to provide consent in order to ensure that the application can function
    properly.*

5.  Select the **Consent on behalf of your organization** check box and then
    select the **Accept** button.

6.  In the admin center, click **Add Environment**:

7.  You will be taken to Omnichannel setup screen. First, select the environment
    that you want to configure Omnichannel for customer service for. Click the
    **Next** button to advance to the next phase in the deployment process.

8.  In the **Enable chat with Omnichannel** screen, set the **Add chat** slider
    to **Yes**. Click the **Next** button to advance to the next screen.

9.  In the **Enable SMS with Omnichannel** screen, set the **Add SMS** slider to
    **Yes**. *(Accept the SMS Terms)*. Click the **Next** button to **Advance**
    to the next screen.

10. In the **Enable Social Channels with Omnichannel** screen, set the **Add
    Social** slider to **Yes**. Click the **Next** button to advance to the next
    screen.

11. In the **Enable Microsoft Teams with Omnichannel** screen, set the **Add
    Microsoft Teams** slider to **Yes**. Click the **Next** button to advance to
    the next screen.

12. On the finial page of the Omnichannel setup screen, verify that all of the
    channels that you want to deploy to are set to be enabled. Click the
    **Finish** button to deploy Omnichannel in that environment.

    \*\***IMPORTANT:** *It can take several hours to deploy Omnichannel. It is
    highly recommended that you deploy before class, and then walk through the
    steps as part of the demo.*

## Task 2: Deploy a Power Platform Portal

In order to deploy a chat channel, as well as configure settings related to
portal functionality, you must have a portal that can be used to deploy the chat
channel to. This could be a custom portal, or a Power Apps Portal. For our
purposes, we will be deploying to a Power Apps Portal.

Before we can deploy a chat channel to the portal, we will need to create a
portal that we can use to deploy the channel to.

1.  Navigate to <https://make.powerapps.com>, and select **Create** from the
    site navigation.

2.  Under **Start from template**, locate and select the **Customer
    self-service** template.

3.  In the **Name** field, enter something like **Customer Self Service
    Portal**.

4.  In the address field, enter a unique URL address for your portal.

    1.  If you cannot think of something, you can use something like the word
        omni followed by the month and year number as well as your initials.  
        **For example:** omni0120dab.

5.  Click the **Create** button to start the process of provisioning your
    portal.

**Note:** *It can take from 10 to 30 minutes for your portal to spin up. While
it is deploying, you can move begin with Task 1. Your portal should be ready
when you are ready to deploy a chat channel to it.*

# Instructor Demo1: Setup up Omnichannel Users & Queues

## Scenario

Omnichannel for Customer Service’s routing and distribution system relies
heavily on Queues and Users to both route and distribute conversations as they
come in from customers across different channels. Your organization primarily
supports billing and service cases. While some agents are qualified to handle
both billing and service-related support cases, most agents either specialize in
one or the other. It is important to ensure the application understands not only
what queues an agent can work on items from, but also that it is able to
determine if the agent is able to handle additional work based on what they are
currently working on.

To ensure that items are routed and distributed correctly, You need to create
the necessary queues, assign users, and configure users to define how many items
that can handle and when items can be assigned to them.

## Task 1: Create new user accounts in Microsoft 365 Admin Center.

1.  Open a new browser tab and navigate to <https://admin.microsoft.com>.

2.  Expand the **Users** node, select **Active Users**, and click **Add a
    User**.

3.  Complete the user as follows:

    -   **First Name:** Alex

    -   **Last Name:** Allman

    -   **Display Name:** Alex Allman

    -   **Username:** alexallman

4.  Under password settings, select let me create the password,

    -   Enter something like **pass\@word1** *(or some other password you would
        prefer)* for the password.

5.  Ensure that **Require this user to change their password when they first
    sign in** is **NOT** checked, click the **Next** button.

6.  To ensure that Alex can access everything he needs to, under **Assign a
    product license**, select the following options:

    -   **Dynamics 365 Customer Engagement Plan**

    -   **Dynamics 365 Customer Service Chat**

7.  Click the **Next** button

8.  Do not make any modifications under **Optional Settings**, click **Next**.

9.  Click **Finish Adding** to complete the process.

10. Repeat steps 2 – 9 to add the two following users.

| First name | Last name | User alias   |
|------------|-----------|--------------|
| Lilly      | Michael   | lillymichael |
| Penelope   | Mayo      | penelopemayo |

>   After each user has been added, your Active users screen should resemble the
>   following image:

![](media/b2d0b5eb384581709bb089194c23678e.png)

## Task 2: Assign security roles to define Omnichannel Users

Before users can access the necessary Omnichannel functionality, they will need
to be assigned at least one of the omnichannel security roles based on what they
will be doing. Here you will leverage security roles to assign access to
omnichannel applications such as Omnichannel Administration, as well as Agent
and Supervisory experiences.

1.  In another browser tab, navigate to
    <https://admin.powerplatform.microsoft.com>.

2.  Locate and select the environment that you deployed Omnichannel for Customer
    Service to. Click the **Settings** button to open the environment settings.

3.  Expand **Users and Permissions**, select **Users**.

4.  Select and open the user record associated with your name. Click the
    **Manage Roles** button. Assign the following Security Roles to your user
    account. Click **OK** when finished.

    -   Omnichannel Administrator

    -   Omnichannel Agent

    -   Omnichannel Supervisor

5.  Repeat step 5 to assign security roles to additional users based on the
    table below.

| First name | Last name | User alias   | Role                                            |
|------------|-----------|--------------|-------------------------------------------------|
| Alex       | Allman    | alexallman   | Omnichannel Supervisor                          |
| Lilly      | Michael   | lillymichael | System Administrator, Omnichannel Administrator |
| Penelope   | Mayo      | penelopemayo | Omnichannel Agent                               |

## Task 3: Configure users in Omnichannel Administration

Items are distributed to agents based on their overall capacity. As items are
assigned agents, their capacity is reduced based on the item that is assigned to
them. When an agent’s capacity falls below the amount required for a specific
channel, no items of that channel type will be distributed to the agent.

As the agent completes items that capacity is added back to the agent.
Additionally, agents can often only be assigned items based on their presence.
To ensure this is handled properly, you must first configure the total capacity
and presence information for each omnichannel agent.

1.  If you do not currently have the Omnichannel Administration application
    open, open a new browser tab, and navigate to <https://home.dynamics.com>.

2.  Under My **Apps,** locate and open the **Omnichannel Administration** app.

3.  Using the application navigation menu, select **Users** from the **Users &
    Queues** group, locate and open your omnichannel user record.

4.  In the **Nickname** field, enter your **First Name** and **Last** initial.
    *(Ex. Derik B.)*

5.  On your user record, select the **Omnichannel** tab to display omnichannel
    specific settings.

6.  Ensure that your capacity is set to **100**, and that your default presence
    is set to **available**.

7.  Since both Alex and Penelope were defined as Agents, repeat steps 4 – 7 for
    both the **Alex Allman**, and **Penelope Mayo** user records.

## Task 4: Setup and Configure Omnichannel Queues

As work items come in, they are first routed to a Queue before they will be
distributed to an agent in that queue based on their current presence and
available capacity.

1.  Under **Users & Queues**, select **Queues**, and from the command bar,
    select the **New** button.

2.  Configure the Queue as follows:

    -   **Name:** Billing

    -   **Priority:** 10

3.  Click **Save** button to save the queue and leave it open.

4.  In the **User (Agents)** sub-grid click **Add Existing User**.

5.  Select **Alex Allman** and click **Add**.

6.  Close the **Billing** queue.

7.  In the Queue list, click the **New** button again.

8.  Configure the Queue as follows:

    -   **Name:** Service

    -   **Priority:** 20

9.  Click the **Save** button to save the queue and leave it open.

10. In the **User (Agents)** sub-grid, click **Add Existing** user

11. Select **your user record** and click **Add**.

12. Close the **Service** queue.

13. From the Omnichannel queue list, open the **Default Queue**.

14. In the **User (Agents)** sub-grid, click **Add Existing** user.

15. Select both **Alex Allman** and **your user record**, click Add.

## Task 5: Mask Credit Card and Social Security numbers

1.  In the **Omnichannel administration application**, under **Settings**,
    select **Data Masking Settings**.

2.  Ensure that **Mask Private agent data from the customer** is set to **No**,
    and that **Mask private customer data from the agent** is set to **Yes**.

3.  In the Masking rules sub-grid, select the **Credit Card** and **SSN**
    records. Click the **Activate** button and confirm activation of the 2
    masking rules.

    *When this information in transmitted through chat conversations, Credit
    Card numbers and SSN numbers will be masked according to the settings
    defined.*

## Task 6: Create standard and extended Operating Hours for chat support

1.  Under **Settings**, select **Operating Hours**, and from the list of
    **Active Operating Hours**, select the **New** button.

2.  Configure the Operating Hour record as follows:

    -   **Name:** Standard

    -   **24/7:** No

    -   **Start time (HH:mm):** 7:00

    -   **End Time (HH:mm):** 18:00

    -   **Work Days:** Mon, Tue, Wed, Thur, Fri

    -   **Time Zone:** Select your Time Zone.

3.  Use the drop-down menu on the at the bottom to select **Save & Create New**.

4.  Configure the Operating Hour record as follows:

    -   **Name:** 24/7

    -   **24/7:** yes

5.  Click the **Save and Close** button.

6.  Your newly added Operating Hour records should resemble the image below.

![](media/a5d9cf540ead1fd72e18fe1da3f1c239.png)

## Task 7: Configure Omnichannel Authentication and Capture Portal Navigation

1.  Under **Settings**, select **Authentication Settings**, and from the
    **Active Authentication Settings** view, click the **New** button.

2.  Configure the **Authentication** settings as follows:

    -   **Name:** Support Portal Authentication

    -   **Authentication Type:** OAuth 2.0 implicit flow

    -   **Public key URL:**
        [https://”your_power_app_portal_url.com/_services/auth/publickey]().
        Example:
        [https://”yourname.powerappsportals.com/services/auth/publickey]().

    -   **JavaScript client Function:** auth.getAuthenticationToken

        ![](media/880b0636ebc82b91820882d77f352277.png)

3.  Click **Save and Close**

4.  Under **Settings**, select **Portal Navigation.**

5.  Set **Portal Navigation** to **Yes.**
