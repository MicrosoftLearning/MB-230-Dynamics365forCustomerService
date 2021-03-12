---
lab:
    title: 'Lab: Configure Customer Service Insights'
    module: 'Module 8: Customer Service Insights'
---

# MB-230: Customer Service Insights

## Before Students begin HOL

You should verify that Customer Service Insights is installed and attached to
the Dynamics 365 Customer Service environment that you are working with. You can
do that by navigating to <https://CSI.ai.dynamics.com> and verifying that the
sample work space is there. That is all you need to do with the environment at
this point.

# Exercise 1: Configure Topic Settings

## Task 1: Configure how topics are grouped

1.  Open an in-private browser and navigate to
    <https://CSI.ai.dynamics.com>**.** *(If prompted for credentials, use the
    same credentials that you have been using for the training environment)*

2.  Using the navigation at the top of the application, select the
    **Workspaces** icon. From the list of available environments, select the
    **workspace** that your Instructor created during the demo.

3.  Using the navigation at the top of the application, select the **Settings**
    icon.

4.  From the list that appears, select **Topic Granularity**.

5.  Adjust the **Granularity** setting to **Very Low**. Click the **Save**
    button twice to confirm your changes.

6.  For your changes to display in the application you will need to click the
    **Refresh** button. *(After the refresh is complete you will likely have
    only 2 topics. If your number is different, that is OK.)*

7.  To ensure that we have enough topics to work with in remaining exercises,
    select the **Settings** icon again. From the list that appears, select
    **Topic Granularity**.

8.  Adjust the **Granularity** setting to **High**. Click the **Save** button
    twice to confirm your changes.

9.  For your changes to display in the application you will need to click the
    **Refresh** button. *(After the refresh is complete you will likely have 4
    topics. If your number is different, that is OK.)*

10. You may find after you have ingested topics that adjusting how the data is
    mapped may provide better results. You can adjust the data mapping settings,
    to ensure case data is mapped correctly. Using the navigation at the top of
    the application, select the **Settings** icon again.

11. Select **Data Mapping**. On the **case** table, click the **pencil** icon
    to change the mapping fields.

12. Notice you can select a different table if needed. *(Since we are working
    in a shared environment with other students, please do not change the table
    currently.)*

13. Click **Next**

14. Here you could modify how fields from the source table are mapped to
    destination fields. *(Again, since we are working in shared an environment,
    please do not change the table at this time.)*

15. Since we are not going to be making any changes currently, select the **X**
    in the upper right corner to leave cancel and leave the mapping settings.

16. With **Topics** selected, select the **Product feature information
    required** topic.

17. If you decide the name of the topic the application provides is not the best
    option, it can be changed to something more appropriate by clicking the
    **Rename** button. *(Since we are sharing an environment, do not rename the
    item)*

18. One of the key advantages of Customer Service Insights is that Topics
    surfaced in the application can turned into Power Virtual Agent topics that
    can be used in bots. *(Appropriate Power Virtual Agent licensing is
    required).* To create a PVA topic, click the **Automate** button.

19. Since a Power Virtual Agent bot was created earlier, Power Virtual Agents
    will open, and a new topic be created automatically.

20. Notice that trigger phrases have been populated. Additional trigger phrases
    could be added as needed. *(Additionally, you could open the authoring
    canvas and design an appropriate conversation path for the topic. Again,
    because of the shared environment we will not be making any changes and will
    close the PVA window.)*

21. After closing the window, select **Cases** to see the cases that make up
    this topic.

22. From the list of topics, select a case such as **Product Question
    (Sample)**. This will open the case record in Dynamics 365 Customer Service.
    Agents or managers could examine the case or work with it based on their
    needs. *(Once finished working with the case, close the tab to return to the
    case list.)*

23. After reviewing the case, we can see that it was placed in the correct
    topic. Use your mouse to hover over **Product Question (Sample)** again and
    select the **thumbs up** icon to note this.

# Exercise 2: Use Customer Service Insights

## Task 1: Configure how topics are grouped

1.  In you are not already in **Customer Service Insights**, navigate to
    <https://CSI.ai.dynamics.com>

2.  Using the **Navigation** at the top of the application, select the
    Workspaces icon. From the list of available environments, select sample
    environment.

3.  Using the left navigation, select **Customer Satisfaction**.

4.  In the **Customer satisfaction** driver graphic, locate and select the
    **volume** column heading.

5.  Once sorted, you can see that almost between 15 & 20 percent of your cases
    were related to the use of a promo code. Over the last Thirty days, the
    overall customer satisfaction has started to fall slightly.

6.  Using the time period filters at the top, change the time with period to
    **Last 7** days. You can see that the topic is trending downward and the
    customer satisfaction has fallen by **almost 2 percent**.

7.  Change the Time Period to Last 24 hours. Over the last 24 hours the score
    has fallen even more.

8.  We can see by the CSAT visual, most of the customer dissatisfactions appear
    to be centered around Twitter and Facebook.

9.  Back in **the Customer satisfaction** drivers, select **Details** on the use
    of customer promo code topic.

10. In the **Analytics** tab, we can see that there is a severe resolution time
    problem related to **Athletic Socks**, and **Kids Rain boots**. Based on
    this data, it would be idea to create a PVA topic to address this. This is
    where we would select **Automate** to address the situation if we were not
    working in a shared environment.
