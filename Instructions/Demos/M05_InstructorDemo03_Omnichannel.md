# MB-230: Omnichannel for Customer Service 

## Instructor Demo 3

In this Demonstration you will be creating and registering a Power Virtual
Agents bot, that your students will use when working through the labs.

## Task 1: Create a Power Virtual Agents chatbot

1.  Navigate to <https://powerva.microsoft.com/>. (You should verify prior to
    class the PVA has been added to the environment that you are working with.)

2.  Using the navigation menu at the top, select the Bot Icon, and click New
    Bot.

3.  Enter ILT OCS BOT for Name, select English for the Language, select your
    environment, and click Create. Make sure you do not have the default
    environment selected.

4.  Wait for the bot to be created. It might take a few minutes to complete.

5.  Click Explore Bot, If prompted.

6.  Wait for the bot to be created. It might take a few minutes to complete.

7.  Select Topics, and click + New topic

8.  Complete the new top as shown in the image below:

9.  Click the Save button to save the bot and leave it open. Once it is saved,
    click the Go to authoring canvas button.

10. In the Message node, enter the following text: I’d be happy to help you with
    that.

11. Select the Add Node button, from the list that appears select Ask a
    question.

12. In the Ask a Question field, enter: Which location are you interested in?

13. Add the following options:

    -   Seattle

    -   Redmond

14. Under the Seattle condition, add a message node with the following text.

    \`\`\`

    Our Seattle location is open:

    Mon – Fri: 8:00 AM to 9:00 PM  
    Saturdays: 10:00 AM to 7:00 PM

    Sundays: 12:00 PM to 5:00 PM

    \`\`\`

15. Under the Redmond condition, add a message node with the following text.

    \`\`\`

    Our Redmond location is open:

    Mon – Fri: 9:00 AM to 8:00 PM  
    Saturdays: 10:00 AM to 5:00 PM

    Sundays: Closed

    \`\`\`

16. **Save** the Topic

17. Select **Topics** again, open the **Escalate** topic, and select **Go to
    authoring canvas**.

18. Edit the message node to read: **No Problem, I will take you there now**.

19. Add a **Transfer to Agent** node with the following text: **This customer
    would like to talk to you**.

20. **Save** the Topic

21. Using the navigation on the left, select **Publish** and click the
    **Publish** button to publish the bot.  
    

## Task 2: Create an Azure Active Directory Application

Let's jump straight into creating the identity. If you run into a problem, check
the [required
permissions](https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal#required-permissions)
to make sure your account can create the identity.

1.  Open a new tab in the same browser session, and navigate to
    <https://portal.azure.com>

2.  If prompted to login, sign in with your credentials.

3.  Under Azure services, select **Azure Active Directory**.

4.  On the left side of the screen under manage, select **App registrations**
    can click the **New registration** button.

5.  Configure the application as follows:

    -   **Name:** Virtual Agent Bot

    -   **Supported Account types:** Accounts in this organizational directory
        only

    -   **Redirect URI:** Leave empty for now.

6.  Once finished, select the **Register** button.

*You have successfully created an Azure AD application and service principal
that can now be used with Omnichannel.*

## Task 2: Assign the application to a role

To access resources in your subscription, you must assign the application to a
role. Decide which role offers the right permissions for the application. To
learn about the available roles, see [RBAC: Built in
Roles](https://docs.microsoft.com/en-us/azure/role-based-access-control/built-in-roles).

You can set the scope at the level of the subscription, resource group, or
resource. Permissions are inherited to lower levels of scope. For example,
adding an application to the Reader role for a resource group means it can read
the resource group and any resources it contains.

1.  In your Azure portal, click in the **Search** bar at the top of the screen.

2.  In the search bar search for and select **Subscriptions**, or select
    **Subscriptions** on the **Home** page.

3.  Select the particular subscription to assign the application to.

    *If you don't see the subscription you're looking for, select* **global
    subscriptions filter***. Make sure the subscription you want is selected for
    the portal.*

4.  Locate and select **Access control (IAM)**, and under **Add a role
    Assignment**, click the **Add** button.

5.  Complete as follows:

    -   **Role:** Contributor

    -   **Assign Access to:** Azure AD User, Group, or Service Principal

    -   **Select:** Power Virtual Agent Bot

6.  Once you see Power Virtual Agent Bot in under Selected Members, click the
    **Save** button.

## Task 3: Configure hand-off in the Power Virtual Agents App

1.  Navigate back to the tab where you have your Power Virtual Agents bot open.

2.  Select the **Settings** icon, and then select **Transfer to agent**.

3.  Select the **Dynamics 365 Omnichannel for Customer Service** tile, click
    **Next** on the Privacy screen.

4.  Switch the browser tab where your Azure Portal is opened.

5.  In the search field, type **Azure Active Directory** and open the **Active
    Directory**.

6.  Under **Manage**, select **App Registrations**, and open the **Virtual Agent
    Bot** registration you created earlier.

7.  Copy the **Application (client) ID**

8.  Paste the Application ID it into the **Power Virtual Agents Application ID**
    field. Select **Next**.

9.  Power Virtual Agents uses a [Teams
    channel](https://docs.microsoft.com/en-us/power-virtual-agents/getting-started-deploy)
    to communicate with Omnichannel for Customer Service. If a Teams channel is
    not enabled, a Teams channel will be enabled when you select **Next**.

10. Select the environment where your Omnichannel for Customer Service instance
    is provisioned.

11. Once everything has finished provisioning, you will be taken to a summary
    screen. On the Summary screen, select the **Go to Omnichannel for Customer
    Service** link to [continue configuring the bot connection in Omnichannel
    for Customer
    Service](https://docs.microsoft.com/en-us/dynamics365/omnichannel/administrator/configure-bot-virtual-agent).

12. The application will open to your newly created Virtual Agent Record.

13. Under **Omnichannel Queues**, click **Add Existing Queue**.

14. Select the **Default Queue** and click the **Add** button.
