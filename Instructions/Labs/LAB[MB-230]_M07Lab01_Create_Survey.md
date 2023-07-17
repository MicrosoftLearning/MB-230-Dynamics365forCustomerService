---
lab:
    title: 'Lab: Create survey'
    module: 'Module 7: Customer Voice'
---

# Practice Lab 7 – Customer Voice

## Scenario

You are a customer service manager at City Power & Light who has been tasked with trying the new Customer Voice functionality to capture feedback on cases before rolling it out to your customers.

## Exercise 1: Create survey

In this exercise, you will create a project and use a template to create a survey.

### Task 1: Create project

1.  Navigate to <https://customervoice.microsoft.com>

2.  Sign in with your Dynamics 365 tenant credentials if necessary.

3.  You should arrive at the **Create a project** page.

4.  Select the **Support** template.

5.  Click **Next**.

6.  Select **See all environments** and select the the **WWLnnn** Dynamics 365 environment (where **nnn** if your unique environment).

7.  Select **Select and close.** Select **Create.**

8.  Select **All Projects**.

9.  Click on the ellipsis next your **Support** project and select **Rename**.

10.  Enter **[your prefix ex. mollyc]** + **Case Feedback** and click on **Rename**.

### Task 2: Customize survey

1.  Select your project.

2.  Click in the **Header** and change **Customer Service feedback** to **How did we do?**. Select anywhere outside the header after you have edited the text.

3.  Hover the mouse over the header and click on the **Theme color** icon (looks like a painting pallette) and change from 2266e3 to **ffdd66**.

4.  Hover the mouse over the header and click on the **Image** icon and choose one of the images from the gallery.

5.  Select question 1 and set as **Required**.

6.  Select question 2 and set as **Required**.

7.  Select the last question in the survey and click on **+ Add new**. Select the chevron (V) and select the **Net Promoter Score** question type. Set the question as **Required**.

8.  Click on **Post-survey message** and change the Heading from **Thanks!** to **Thank you for your feedback** and change the Message to **We look at all feedback to improve our service.**

9.  Click in the Footer and enter **The feedback you submit will not be shared outside of the company.**

10. Expand **Customization** and select **Personalization**.

11. Click + **Add variable** and enter **casereference** with default value **Your support case**.

12. Click **Save**.

13. Click **Close**.

14. Select **Formatting**.

15. Toggle **Progress bar** to **Off** and close the formatting pane.

16. Select Section 1. Select the **Variables** drop down and select **casereference**.

17. Add the text **has been resolved**.

18. Click **Preview**.

19. Click **Back**.

### Task 3: Satisfaction metrics

1.  Select your survey.

2.  Expand **Customization** and select **Satisfaction metrics**.

3.  Click **+ Add metric**.

4.  Select **CSAT**. Under the **Case resolution survey questions**, select the first question.

5.  Click **Save**.

6.  Click **+ Add metric**

7.  Select **Net Promoter Score** and select the last question.

8.  Click **Save**.

9.  Click **+ Add metric**.

10.  Select **Sentiment** and select the text question.

11.  Click **Save**.

## Exercise 2: Send survey

In this exercise, you will create an email template and send the survey by email.

### Task 1: Configure email template

1.  Navigate to <https://customervoice.microsoft.com>.

2.  Select your project.

3.  Click on the **Send** tab.

4.  Click on the **Email** tile.

5.  Click on the **Template** drop-down and select **Create new**.

6.  Enter **[your prefix ex. mollyc]** + **Case Resolution** and click **Add**.

7.  Click on the **Insert** drop-down and select **First question in survey**.

8.  Replace the subject line with **Please provide feedback on**, click on the **Insert** drop-down and select **Personalized variables** and then select **casereference**.

9.  Click **Save**.

10. Click **Cancel**.

### Task 2: Send the survey

1.  Click on the **Send** tab.

2.  Click on the **Email** tile.

3.  Click on the **Template** drop-down and select the **Case Resolution** template you created.

4.  Click in the Recipients field and enter your email address.

5.  Click **Send**.

## Exercise 3: Send survey when a case is resolved

In this exercise, you will use Power Automate to send a survey when a case is resolved.

### Task 1: Configure automation

1.  Navigate to <https://customervoice.microsoft.com>.

2.  Select your project.

3.  Click on the **Send** tab.

4.  Click on **Resend** and select **Automate**. 

5.  Select the **Send a survey when a case is resolved in Dynamics 365** template. You may need to click on **See more templates**.

6.  If the connections require action, click **Fix connection** and sign in when prompted.

7.  Click **Continue**.

12. Select the **WWLLABnnn** Dynamics 365 environment for your environments.

13. Select the survey project starting with your prefix for **Dynamics 365 Customer Voice Project.**

14. Select your survey for **Dynamics 365 Customer Voice Survey.**

15. Select your email template for **Dynamics 365 Customer Voice Email template.**

17. Click **Create**.
