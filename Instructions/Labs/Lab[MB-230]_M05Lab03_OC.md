Now that the Omnichannel for Customer Service environment that you are working
in has been successfully configured by both you and the instructor; we will
examine what the interface might look like from an agent standpoint.

IMPORTANT: Because we are working in shared environments, we are not going to be
able to demonstrate the chat experience. When a chat is initiated, we will not
be able to guarantee that the items will be routed to the right person.

For this reason, we will only be working with the SMS channels you created in
the labs. Because of the routing rules, we can ensure that you will be getting
the items as they come in.

### Learning Objectives

After completing the exercises in this lab, you will be able to:

-   Use Omnichannel for Customer Service to resolve cases.

-   See how the bot user handles incoming conversations before routing to an
    agent.

-   Accept conversations that are initiated by users.

-   Work with items in the conversation window.

-   Enable the productivity pane for agents to leverage scripts

### Estimated time to complete this lab: 30 minutes

# Exercise 1: Use Omnichannel for Customer Service to assist customers 

To successfully complete this exercise, you are going to need three items:
--------------------------------------------------------------------------

-   A mobile device that you can text from.

-   The Omnichannel Administration application open in a browser tab.

-   The Omnichannel for Customer Service app, open in a browser tab.

## Task 1: Initiate a conversation with OCS
----------------------------------------------

1.  If it is not already open in another tab, navigate to the Omnichannel
    Administration application. *(You will use this to get the support number
    that will be used.)*

2.  In a new browser tab, navigate to <https://home.dynamics.com>

3.  Locate and select the **Omnichannel for Customer Service** app.

>   **NOTE:** To simulate what will happen when a customer interacts with an
>   agent. We will be sending an SMS message to the queue that we created
>   earlier. Switch to the tab that the Omnichannel Administration application
>   is open in.

1.  Select **Work Streams** and open the SMS work stream that you created
    earlier. *(Make sure to select the one that has your lab user credentials)*.

2.  On the work stream, select the **SMS** number tab, and note the **SMS
    number** associated with it.

3.  On your mobile device, create a **new chat conversation** to the SMS number
    in the Work Stream. In the message of the conversation enter something like
    **“Hello, I need help”**.

>   **NOTE:** *Your message app will likely look different.

1.  After several seconds you should receive a message back from the virtual
    agent asking what it can help you with.

2.  Enter **What are your hours**?

3.  The bot will respond by asking you what store you are interested in. Enter
    **Seattle**.

4.  After the bot tells you the hours, enter **Talk to an agent**.

5.  The bot will tell you that it can help you with that, and then transfer you
    to a live agent.

## Task 2: Communicate with the customer

Next you will switch to the Omnichannel for Customer Service agent application
and be working as an agent would with the customer. It is important that you
were signed in earlier to make sure that you will get the conversation request
when it comes through.

1.  Make sure you have the omnichannel application open as an agent.

2.  After several seconds, you will receive a notification for the conversation.
    Select **Accept**.

3.  When the session opens, you will see the complete conversation that has
    taken place up to this point. Scroll through the conversation to view the
    details of it and then return to the end.

4.  Start by expanding the **Productivity pane** on the right side of the
    screen. Once expanded, it will display **Agent Guidance**.

5.  Ensure that the **yourlabusername script** you created earlier is selected.
    *(If it is not use the dropdown menu to select it.)*

6.  On the script, expand **Greet the customer** step.

7.  After reviewing the text, select the **Quick reply’s** icon in the
    conversation panel.

8.  Enter the word **Hello**. From the list of options displayed, select
    **Hello, you’re chatting with . . .** Press the **Enter key** on your
    keyboard.

9.  Once the message is sent, mark the **Greet the Customer** task as **Done**.

10. On your mobile device, send the following message: **I’m getting frustrated
    because things are damaged.**  *(Notice at the top of the conversation
    panel, that the tone of the conversation is changing to slightly negative.)*

11. Back on your mobile device, send the message: **I’m really upset.** *(Notice
    that the tone of the conversation is changed to Negative.)*

12. On your Mobile Device, send the message: **The Item I received was broken.**

>   **Note:** To ensure that we have all the related details. Next, we will
>   associate this conversation with a customer. *(Normally these details could
>   be passed to the conversation from the mobile device, but for out purposes
>   we will like the conversation manually.)*

1.  In the conversation summary, select **Search Customer**.

2.  Change the lookup to **Contacts.**

3.  Select **Jim Glynn (sample)**. *Notice how additional details are now
    populated to the case record. This will help to provide additional context
    as we work with the customer.*

4.  We need to open a new case for this item. On the **Open a New Case** step in
    the agent script, select the **Run Macro**. *Once complete, a new case will
    be created and linked to the conversation.*

5.  If necessary, select the **Customer Summary** tab, to return to the customer
    summary screen.

6.  Now that we have tied the case to the customer and have opened a new case,
    let’s solve the customers issue. On the agent script expand the **Search for
    Relevant KB Article** step.

7.  Based on the guidance provided by the script, on the conversation select the
    **ellipsis.** From the menu that appears, select **Knowledge Articles**.
    *The Knowledge Search window appears.*

8.  Enter **Damaged** into the search field and press enter.

9.  From the list of articles, select the **Damaged or Defective products**
    article to display the contents. **NOTE:** *We could send this article to a
    customer by configuring email integration with the channel integration
    framework. However, that is out of scope of the class. For this example, we
    will assume that the article was sent to the customer.*

10. In the conversation window: **ask the customer if they received the
    article?**

11. On your mobile device, enter: **Yes I did, thank you.** *Notice the
    conversation tone begins to change* to more positive.

12. In the conversation window in OCS, ask them if **they would like you to walk
    them through the process?**

13. On your mobile device, enter: **No, this helps a lot, thanks.** *The
    conversation tone is getting more positive.*

14. Back in OCS go back to the **Agent Script** in the **Productivity Pane**.
    Select the **Icon** next to **Search for relevant KB article** to mark the
    step as **Done**.

15. Select the **View** button on the **Proceed to Closing** step. *The current
    script will be closed, and the Closing Script will open.*

16. On the **Resolve Case** step, select the **Run** button. Once the macro is
    completed, the associated case will be resolved.

17. Expand the **Have a nice day** step. Per the step instructions, in the
    conversation window **ask them if there is anything else you can assist them
    with**.

18. On your mobile device, enter: **Nope, all good, thanks again**.

19. In the conversation window, enter **Thanks for your time, Have a great
    day**.

20. On the **Closing** agent script, mark the **Have a Nice Day** step as
    **Done.**

21. On the conversation, select the **End** button located at the top of the
    conversation. *Notice that the conversation stays open, but changes to
    Internal. This let’s you do any finial wrap up on the conversation.*

22. On the **Session’s** list on the left navigation, Click the **X** to close
    the Jim Glynn session. on the dialog that appears, select the **close**
    button to confirm the selection.

23. On the Omnichannel Agent dashboard, you will see the Jim Glynn conversation
    has been moved to the **Closed** area.
