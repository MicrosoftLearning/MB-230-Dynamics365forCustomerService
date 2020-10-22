# MB-230: Omnichannel for Customer Service

## Instructor Demo 2

### Task 1: Create a Chat Work Stream

Each channel that is deployed requires a Work Stream. Work Streams help to
define how items will be routed and distributed. Through the work stream, you
will define settings such as the capacity that is consumed, how items should be
distributed, routing rules, and more. Since your organization would like to
surface a live chat widget on their site, you will need to configure a work
stream to facilitate it.

1.  Under **Work Distribution Management**, select **Work Streams**, from the
    **Active Work Stream** list, click the **New** button.

2.  Configure the Work Stream as follows:

    -   **Name:** Standard Portal Chat

    -   **Channel:** Live Chat

    -   **Capacity:** 25

    -   **Auto-Close after inactivity:** 5 minutes

    -   **Assign Work item After Decline or Time Out:** 2 minutes

3.  Under Work Distribution configure as follows:

    -   **Work Distribution Mode:** Push

    -   **Allowed Presences:** Available, Busy

4.  Click the **Save and Close** button to Close the Work Stream.

## Task 2: Create a Channel

Now that you have defined the Work Stream that will be used for Live Chats, you
need to build the Chat Widget that you will surface to customers on a portal.
When you architect a chat channel, you can define the specific behavior
associated with it. This might include using authentication settings to identify
the user and populate information in the solution based on who the user is. You
can also define items such as attachment and transcript options and build
pre-chat surveys that will be presented to customer prior to the initiation of
the chat. This information can be used to help ensure that the appropriate data
is populated to the agent in the solution when the conversation is initiated.

1.  Under **Channels**, select **Chat**, from the **Active Chat Widgets** list,
    click the **New** button.

2.  Configure the chat widget as defined below:

    -   **Name:** Standard Chat

    -   **Language:** English – United States

    -   **Agent Display Name:** Nickname

    -   **Authentication Settings:** Support Portal Authentication

    -   **Work Distribution:** Standard Portal Chat

3.  Configure File Attachments as follows:

    -   **Enable file attachments for Customers:** Yes

    -   **Enable file attachments for Agents:** Yes

4.  Configure Chat Transcripts as follows:

    -   **Allow download of transcript:** Yes

    -   **Allow email of transcript:** No

5.  Set **Show Position in Queue** to **yes**.

6.  Your Chat widget screen should resemble the image below:

![](media/5c22d0ecb10ba14a0442ce145a9fc136.png)

1.  Click the **Save** button to save the chat widget and leave it open.

## Task 3: Modify the Design Elements of the Chat widget.

1.  If necessary, open the **Standard Portal** Chat widget that you created in
    the previous Task. Select the **Design** tab.

2.  To change the theme color that is used for the chat widget, select the color
    you want to use from the **Theme Color** drop down menu.

3.  Change the **Title** to **Talk to Agent**.

4.  Leave the **Subtitle** as **We’re Online**

5.  In the **Operating Hours** field, select the **24/7** record you created
    earlier.

6.  If necessary, click the **Save** button in the lower right corner of the
    screen to save you changes and leave the record open. *(You do not need to
    save your changes, as the changes will be auto-saved after 30 seconds.)*

## Task 4: Configure a Pre-Chat Survey

When customers initiate a chat from the portal, you can present the user with a
pre-chat survey to capture attritional information that can assist the agent in
resolving the customers issue. Additionally, answers to pre-chat survey
questions can help to ensure that the correct information is presented in the
Customer Summary screen when it is loaded in the application. This might include
capturing the account or contact name, or case number when they are referencing
an existing case.

1.  If necessary, open the **Standard Portal** Chat widget. Select the
    **Pre-Chat** survey tab.

2.  Set the **pre-chat survey** field to **Yes**.

3.  In the **Pre-chat unauthenticated** questions sub-grid, select **Add
    Question.**

4.  Configure the Question as follow:

    1.  **Question Name:** CaseNumber

    2.  **Question Text:** What Case Number is this related to?

    3.  **Answer Type:** Single Line

    4.  **Mandatory:** No

5.  Click **Save and Close** to close the question

## Task 5: Deploy your Chat widget to a Portal

As you build the chat channel, the application generates a Code Snippet that is
used to deploy the chat widget to your portal location.

1.  If you do not already have it open in a different tab, open a new browser
    tab, and navigate to <https://make.powerapps.com>

2.  In a separate tab have the **Omnichannel Administration** application open.

3.  In the **Power Apps Admin** screen, select **Apps** and open the **Dynamics
    365 Portals App**.

4.  In the **Dynamics 365 Portals** App, select **Content Snippets** under
    **Content**.

5.  In the **Search for Records** Box, enter **Chat** and hit enter. Open the
    **Chat Widget Code** content snippet for your customer service portal.

6.  In the **Value (HTML)** field, select the **HTML** tab.

7.  Switch to tab that contains the **Omnichannel administration** application.

8.  Under **Channels** \> **Chat**, open the **Standard Chat Channel** you
    created earlier.

9.  Locate the **Widget snippet code** field. Highlight and copy the entire
    script from that field.

10. Switch back to the **Chat Widget Code** item in the other tab where you have
    the **Dynamics 365 Portal Application** open.

11. Paste the value into the value field. **Important:** *Make Sure that the
    HTML tab is selected.*

12. To ensure that the entire script was pasted in correctly, select the
    **Designer** tab. If the screen is empty the script was correctly copied
    into the application. If you see the script text in the field, it is likely
    the entire script was not pasted into the field.

**Note:** *If you are using Power Apps portals, after the script has been
deployed from the Chat Widget Code snippet, it can take up to 15 minutes before
you will see the chat widget available on your portal.*

## Task 6: Verify you Chat widget has been deployed

1.  If you do not already have it open in a different tab, open a new browser
    tab, and navigate to<https://make.powerapps.com>.

2.  Navigate to Apps and locate the Customer Self-Service Portal that you
    created in the previous exercise.

3.  Open the **Customer Self Service Portal**.

4.  Verify that your chat widget is being displayed on the Portal.

**Tip:** *If you are still not seeing the chat widget in the portal, look at the
working hours associated with the chat to verify that you are within the work
hour defined.*
