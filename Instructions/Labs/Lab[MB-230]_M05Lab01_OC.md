---
lab:
    title: 'Lab: Omnichannel Lab 1'
    module: 'Module 5: Omnichnnel'
---

In this module, you will be configuring an SMS channel that you will be using
throughout the rest of the course. It will be important when were get to the
finial steps, that you are naming everything exactly as described in the lab.
This will reduce the chance of accidentally selecting an object created by
another student during the process.

**Note:**  Please add your lab user prefix before any data you create in Dynamics 365.  Ex: **[MollyC] + case**

# Exercise 1: Configure an SMS Channel

Before you can create an SMS channel in the OCS, you will need to signup with
and SMS provider. We will be leveraging Twilio because Twilio numbers are
available to be consumed right away.

## Task 1: Sign up for a Twilio account that that can be leveraged with the system
-------------------------------------------------------------------------------------

1.  In the same browser session that you are currently logged into the
    Omnichannel Administration application with, navigate to
    <https://twilio.com>**.** *(you will be directed to a 3rd party site (Twilio) to sign up for a free trial. Information that you enter when you sign up may be used by the 3rd party. We recommend that you review their privacy statement before signing up)*
    
    *(If you are not currently logged into Omnichannel
    Administration, use the credentials provided to you by your instructor to
    log in.)*

2.  Select the **Sign-up** button.

3.  You will be asked to provide your contact and detail information including:
    First Name, Last Name, Email, Password. Once you have provided those details
    and accepted the terms of service, select the **Start your Free Trial**
    Button.

4.  To complete the registration process, you will need to respond to the
    verification email sent to you by clicking the **Confirm your Email link**.

5.  You will be taken to the Twilio sign in page. Sign in using the username and
    password you created earlier.

6.  You will likely need to verify your phone number to start your trial. Select
    your country code, enter your phone number, and select **Verify**.

7.  Enter the verification code that was sent to you through SMS and click
    **Submit**.

8.  You may be asked some questions about yourself, Answer the questions to
    complete the process.

9.  Once you arrive at your dashboard page, leave the page open so you can
    return to it later.

## Task 2: Configure an SMS Work Stream
------------------------------------------

Now that you have a Twilio account that you can leverage, the next step in the
process is to create a dedicated SMS work Stream that will leverage that will
leverage that number to facilitate SMS communication.

**IMPORTANT:** *If you would prefer to use a TeleSign account, you can setup a
TeleSign account instead of Twilio.*

1.  If the Omnichannel Administration application is not open in another tab,
    open it in a new tab by navigating to <https://home.dynamics.com>.

2.  Under **Work Distribution Management**, select **Work Stream**, select the
    new button to create a new **Work Stream**.

3.  Under **General Information**, configure the SMS work stream as follows:

    -   **Name:** Yourusername Twillio SMS Support *(use the account name
        provided to you by your instructor.)*

    -   **Channel:** SMS

    -   **Capacity:** 20

    -   **Auto-Close after Inactivity:** 2 Days

>   *Because there can often be a delay in communication with customers engage
>   through SMS channels, you want to ensure that you are allowing enough time
>   for the customer to communicate back with you. For this reason, you should
>   always set the auto-close after inactivity option to a minimum of 2 days.*

1.  To ensure that SMS conversations are automatically routed to agents, set the
    **Work Distribution mode** to **Push**.

2.  Set **Allowed Preferences** to **Available** and **Busy**.

3.  Select the **Save** button to save the work stream but leave the record
    open.

4.  Select the **SMS Settings** tab.

5.  Ensure that the **SMS provider field** is set to **Twilio**.

6.  If Twilio is not open in another tab, open the tab that contains your Twilio
    account information.

7.  Locate the **Account SID** and **Auth Token** for your account. Copy and
    paste the details into the **Account SID** and **Auth Token** under the
    Twilio Account Information from the workstream.

8.  Select **Save**. The Twilio inbound URL will be generated and displayed.

## Task 3: Obtain an SMS number from Twilio 
----------------------------------------------

Twilio needs to register the Inbound URL for the application with your account.
Once this is done, you can add a phone number to your account that will be used
with SMS channel.

1.  If you closed the tab with your Twilio Account, open your it in a new tab in
    the current browser session. **Note:** *You may need to verify your identity
    when signing in. You may receive an SMS message with an Access code.*

2.  Using the navigation menu on the left, select the **ellipsis** icon, and
    under super network, select **Phone Numbers**.

3.  Under **Active Numbers,** click the **Get Started** link.

4.  In the **Get Started with Phone Numbers screen,** click the **Get your first
    Twilio phone number** button.

5.  A number with Voice, SMS, and MMS capabilities will be displayed, click the
    **Choose this Number** button. *(If you would like to find a different
    number, you can select Search for a different number.)*

6.  Once your new number is provided, click the **Done** button.

7.  Leave Twilio open for later

## Task 4: Add your new number to your SMS work stream
---------------------------------------------------------

Once you have obtained a phone number, you are ready to create an SMS channel in
the application to use the phone number.

1.  Navigate to, or if necessary, open the **Omnichannel Administration**
    application in another tab.

2.  Under **Work Distribution Management**, open the **[Yourlabuser] Twilio SMS**
    work stream with your name or initials that you created in the previous
    exercise, and click the **SMS Numbers** tab.

3.  Select the **New SMS Number** button from the SMS numbers sub-grid

4.  Configure the number as follows:

-   **Number:** “The number you got in the previous tab”

>   *Make sure you include the country code and do not include any spaces in the
>   name*

-   **Type:** Long Code

-   **Work Stream:** Yourlabuser Twillo SMS Support

-   **Operating Hours:** 24/7

1.  Select **Save**.

2.  Click the **Validate API Key** button.

It can take a minute or two for the validation process to proceed. After it is
complete, your SMS work stream is configured and is ready to accept SMS
requests.

## Task 5: Establish a connection between Omnichannel for Customer Service and the Twilio account
--------------------------------------------------------------------------------------------------

Perform the following steps to configure the URL in Twilio for the SMS messages
from Omnichannel for Customer Service to be processed in Twilio:

1.  Copy the value in **Twilio inbound URL** of the work stream for Twilio.

2.  Go to your Twilio account \> **Phone Numbers** \> **Active Numbers**, and
    then select the SMS phone number.

3.  In the **Messaging** section, paste the Twilio inbound URL.  The configuration should be set to **Webhook**

# Exercise 2: Create a PVA bot to handle conversations

## Task 1: Sign-up for a PVA trial and create the bot
------------------------------------------------------

In this task, you will sign up for a trial Microsoft Power Virtual Agents and
create your first bot.

1.  Navigate to <https://powerva.microsoft.com/>.

2.  Using the navigation menu at the top, select the **Bot Icon**, and click
    **New Bot**.

3.  Enter **Customer service bot (You Initials)** for **Name**, select your
    **Language**, select your environment, and click **Create**. Make sure you
    do not have the default environment selected.

4.  Wait for the bot to be created. It might take a few minutes to complete.

5.  Click **Explore Bot**, If prompted.

## Task 2: Create support categories entity
--------------------------------------------

In this task, you will create a new entity named support categories that has
three items, order question, delivery and setup, and weather related.

1.  Select **Entities**.

2.  Click **+ New custom entity.**

3.  Enter **Support categories** for **Name**.

4.  Enter **Order question** as an item and click **Add**.

5.  Enter **Delivery & setup** as an item and click **Add**.

6.  Enter **Weather related** as an item and click **Add**.

7.  Support category custom entity should now have three items. Make sure
    **Start matching** is turned on and click **Save**.

8.  Click **Close**.

## Task 3: Create order entity
-------------------------------

>   In this task, you will create a new entity named order that has two items,
>   place order and cancel order.

1.  Make sure you still have **Entities** selected and click **+ New custom
    entity**.

2.  Enter **Order** for **Name**.

3.  Enter **Place order** as an item and click **Add**.

4.  Enter **Cancel order** as an item and click **Add**.

5.  The order custom entity should now have two items. Make sure **Smart
    matching** is turned on and click **Save**.

6.  Click **Close**.

## Task 4: Create a Cancel Order Topic:
----------------------------------------

1.  Select **Topics** and click **+ New topic**.

2.  Enter **Cancel order** for Name, enter **Cancel order** as a trigger phrase
    and click **Add**.

3.  Enter **Cancel** as a trigger phrase and click **Add**.

4.  The **Cancel order** topic should now have two trigger phrases. Click **Go
    to authoring canvas**.

5.  Enter **Orders must be canceled at least 48 hours before you scheduled
    event. Your deposit will not be refunded** for **Message** and click **Add
    node**. Note: when you copy and paste from the lab, you may see some styling
    in the canvas. Feel free to keep the styling or change it to your
    preferences.

6.  Select **Show a message**.

7.  Enter **Only live agents can process a cancelation request** for **Message**
    and click **Add node.**

8.  Select **Ask a question**.

9.  Enter **Would you like to talk to one now?** for question, enter **Yes** as
    an option, and click **+ New option**.

10. Enter **No** as the second option. You should now have two conditions.

11. Go to the **Yes** branch and click **Add node**.

12. Hover over the **End the conversation** option and select **Transfer to
    agent**.

13. Enter **Customer would like to cancel order** for **Private message to
    agent**.

14. Go to the **No** branch and click **Add node**.

15. Select **Show a message**.

16. Enter **Can I help you with anything else?** for **Message**.

17. Click **Save**.

## Task 5: Create a New order Topic
-------------------------------------

1.  Select **Topics** and click **+ New topic**.

2.  Enter **New order** for **Name**, enter **New order** as a trigger phrase
    and click **Add**.

3.  Enter **Place an order** as a trigger phrase and click **Add**.

4.  Enter **Make a new order** as a trigger phrase and click **Add**.

5.  The New order topic should now have three trigger phrases. Click **Go to
    authoring canvas**.

6.  Enter **Be advised that all new orders required a non-refundable \$100.00
    deposit that will be applied to your total order cost** for **Message** and
    click **Add node**.

7.  Select **Show a message**.

8.  Enter **Let me transfer you to an agent to process your request** for
    Message and click Add node.

9.  Hover over the **End the conversation** option and select **Transfer to
    agent**.

10. Enter **Customer would like to place an order** for **Private message to
    agent**.

11. The New order topic should now have three nodes. Click **Save**.

## Task 6: Create a check weather topic
----------------------------------------

1.  Select **Topics** and click **+ New topic**.

2.  Enter **Check weather** for **Name**, enter **Weather** as a trigger phrase
    and click **Add**.

3.  Enter **Today’s weather** as a trigger phrase and click **Add**.

4.  Enter **What is the weather like** as a trigger phrase and click **Add**.

5.  Enter **Will it rain today** as a trigger phrase and click **Add**.

6.  Enter **Check weather** as a trigger phrase and click **Add**.

7.  The Check weather topic should now have five trigger phrases. Click **Go to
    authoring canvas**.

8.  Enter **I can help you with that, I just need some additional information**
    for **Message** and click **Add node**.

9.  Select **Ask a question**.

10. Enter **What City do you live in?** click **Identify** and select **User’s
    entire response**.

11. Click **Edit** variable.

12. Enter **City** for **Name** and close the **Variable properties** pane.

13. Click **Add node**.

14. Select **Ask a question**.

15. Enter **What is your postal code?** click **Identify** and select **User’s
    entire response**.

16. Click **Edit variable**.

17. Enter **ZipCode** for **Name** and close the **Variable properties** pane.

18. Click **Add note**.

19. Select **Call an action** and select **Create a flow**.

20. Power automate should open on a new browser window or tab.

21. Select your **country/region** and click **Get started**, if prompted.

22. Click **+ Add an input**.

23. Select Text.

24. Enter **City**, enter **Provide city**, and click **+ Add an input** again.

25. Select **Text** again.

26. Enter **Zip code** and enter **Provide zip code**.

27. Hover over between the flow trigger and the step, and then click on the
    **+** button. You are adding a step between the trigger and the return
    values step.

28. Select **Add an action**.

29. Search for msn and select **Get forecast for today**.

30. Click on the Location field, go to the Dynamic content pane and select City,

31. Add comma after the city and then select **Zip code** form the Dynamic
    content pane.

32. Select your preferred units. For this lab, we are selecting **Imperial**.

33. Click to expand the **Return value(s) to Power Virtual** Agents step.

34. Click **+ Add an output**.

35. Select **Text**.

36. Enter **Day_Summary** for name, click on the **Day_summary** field and
    select **Day Summary** from the Dynamic content pane.

37. Click **Add an output**.

38. Select **Text**.

39. Enter **Location** for **Name**, click on the **Location** field and select
    **Location** from the Dynamic content pane.

40. Click **Add an output** again.

41. Select **Text**.

42. Enter **Chance_of_rain** for **Name**, click on the **Chance of rain** field
    and select **Rain chance** from the Dynamic content pane.

43. Rename the flow to **Check weather** and click **Save**.

44. Wait for the flow to be saved.

45. Go back to **Power Virtual Agents**.

46. Click **Add node**.

47. Select **Call an action** and then select the **Check weather** flow you
    created.

48. Click on the **City** dropdown and select **City**.

49. Click on the **Zip code** dropdown and select **ZipCode**.

50. Click **Add node**.

51. Select **Show a message**.

52. Click **Insert a variable**.

53. Select **Day_Summary**.

54. Type **with a chance of** and insert **Chance_of_Rain** variable.

55. Type **percent of rain in** and insert **Location** variable.

56. The **Message**

57. Click **Save** to save the topic.

## Task 7: Create a Delivery and Setup topic
---------------------------------------------

1.  Select **Topics** and click **+ New topic**.

2.  Enter **Delivery and setup** for **Name**.

3.  Enter **Delivery** as a trigger phrase and click **Add**.

4.  Enter **When will my order be delivered** as a trigger phrase and click
    **Add**.

5.  Enter **Who will setup the items** as a trigger phrase and click **Add**.

6.  Enter **Who will remove the items** as a trigger phrase and click **Add**.

7.  Enter **Schedule a setup** as a trigger phrase and click **Add**.

8.  Enter **Schedule delivery** as a trigger phrase and click **Add**.

9.  Enter **Schedule removal** as a trigger phrase and click **Add**.

10. The Delivery and setup topic should now have seven trigger phrases. Click
    **Go to authoring canvas**.

11. Enter **Items are delivered 1 hour before your scheduled event** for
    **Message** and click **Add node**.

12. Select **Show a message**.

13. Enter **Two delivery people will come and setup your items** for **Message**
    and click **Add node.**

14. Select **Show a message**.

15. Enter **What else can I assist with?** for **Message**.

16. Click **Save** to save the topic.

## Task 8: Add an Order Topic:
-------------------------------

1.  Select **Topics** and click **+ New topic**.

2.  Enter **Order** for **Name**.

3.  Enter **Order question** for trigger phrase and click **Add**.

4.  Click **Go to authoring canvas**.

5.  Enter **I can help you with that** for Message and click Add node.

6.  Select **Ask a question**.

7.  Enter **What do you want to do?** enter **Place an order** for the first
    option and click **+ New option.**

>   Enter **Cancel order** for the second option.

1.  You should now have two condition branches. Go to the **Place an order**
    branch and click **Add node**.

2.  Select **Go to another topic**.

3.  Select the **New order** topic you created.

4.  Go to the **Cancel order** branch and click **Add node**.

5.  Select **Go to another topic** again.

6.  Select the **Cancel order** topic you created.

7.  Click **Save** to save the topic.

8.  Wait for the topic to be saved.

## Task 9: Modify the Greeting system topic: 
----------------------------------------------

1.  Select **Topics**.

2.  Search for **greeting**, hover over the **Greeting** topic and click **Go to
    authoring canvas**.

3.  Replace the first message with **Hi! I am a virtual agent here to help with
    questions ranging from ordering questions, to weather related questions**.

4.  Replace the second message with **If you would like to speak to a human at
    any time, just let me know**.

5.  Click on the **… Options** button of the last message and click **Delete**.

6.  Click **Add node**.

7.  Select **Ask a question**.

8.  Enter **What can I help you with?** for question.

9.  Enter **Order questions** for first option and click **+ New option**.

10. Enter **Delivery and setup** and click **+ New option** again.

11. Enter **Weather related** for the third option.

12. You should have three condition branches. Go to the **Order questions**
    branch and click **Add node**.

13. Select **Go to another topic**.

14. Select the **Order** topic you created.

15. Go to the **Deliver and setup** branch and click **Add node**.

16. Select **Go to another topic**.

17. Select the **Delivery and setup** topic you created.

18. Go to the **Weather related** branch and click **Add node**.

19. Select **Go to another topic**.

20. Select the **Check Weather** topic you created.

21. Click **Save** to save the topic.

## Task 10: Test your bot
-------------------------

1.  Click on the **Test your bot** button located on the bottom-left of the
    screen.

2.  Turn on **Track between topics**.

3.  Type **Hello** and click **Send** or **[ENTER]**.

4.  The bot should greet you and give you options. Keep a watch on the current
    topic.

5.  Select **Delivery and setup** from the options.

6.  The topic should change to the **Delivery and setup** topic and the bot
    should replay with the delivery and setup messages.

7.  Enter **Order question** and **Send**.

8.  The topic should change to the **Order** topic and the bot should give you
    options to place an order or cancel an order.

9.  Choose **Cancel order**.

10. The bot should display the order cancelation messages. Type **Will it rain
    today** and **Send**.

11. The topic should change to the **Check weather** topic and the bot should
    ask you to provide your city.

12. Enter city name and **Send**.

13. Provide your zip code and **Send**.

14. The bot should trigger the flow and reply with the result of MSN weather
    connector.

15. Type **Goodbye** and **Send**.

16. The bot should conclude the chat.

17. Click **Hide bot**.

## Task 11: Publish your bot
-----------------------------

1.  Select **Publish** and click Publish.

2.  Click **Publish** again to confirm and wait for the publishing to complete.

3.  Click on the **Demo website link**.

4.  Try to interact with bot on the demo website and see how it performs.

5.  You may share the demo website with others.

# Exercise 3: Configure Omnichannel to use the PVA Bot

**Task 1: Create a queue for yourself and the Botuser.** 
---------------------------------------------------------

1.  If necessary, open the **Omnichannel Administration** application, and
    select **Queues**.

2.  Click the **New** button to create a new queue.

3.  Enter the following information into the Queue

    1.  **Name:** Yourlabuser Queue (Ex. DerikB Queue)

    2.  **Priority:** Enter a number in the 100’s

4.  Click **Save**

5.  In the **Users** sub-grid, select **Add existing** user, and choose the bot
    user that your instructor created during the demo.

6.  You queue should include both your user account and the Botuser.

7.  Click **Save and Close**.

## Task 1: Configure a routing rule to send items to the bot
---------------------------------------------------------------

1.  Under the **Work Distribution Management**, select **Work Streams**, and
    open the **Twilio SMS** workstream with your initials that you created
    earlier.

2.  Select the **Routing Rules** tab, and in the **Rule items** sub-grid select
    **Add**.

3.  Configure the Rule item as follows:

    1.  **Name:** Route to Your Name Queue (Ex. DerikB Queue)

    2.  **Work stream:** Your Twilio SMS work Stream

    3.  **Queue:** Your Queue

4.  In the Condition section, select Add Condition and configure the Condition
    as follows.

    1.  **Entity:** SMS Engagement Context (Conversation)

    2.  **Attribute:** Customer Phone Number

    3.  **Operator:** Equals

    4.  **Value:** Enter your mobile number with out the country code (Ex.
        7775551234)

5.  Click **Save**
