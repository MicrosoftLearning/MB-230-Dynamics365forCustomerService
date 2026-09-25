---
lab:
  title: 'Lab: Capture feedback with Customer Voice'
  module: 'Module 6: Extend and analyze Dynamics 365 Customer Service'
  description: As a customer service manager at Contoso Coffee, you create and test a case feedback survey, configure satisfaction metrics, and review distribution and automation options.
  duration: 30 minutes
  level: 100
  islab: true
---

# Practice Lab – Capture feedback with Customer Voice

> [!IMPORTANT]
> Customer Voice is included with the Dynamics 365 Customer Service trial and doesn't require separate installation. Sign in with the same Microsoft Entra account that you use for the course environment. If Customer Voice or the course environment isn't available, notify your instructor. You can skip this final lab without affecting any other lab.

## Scenario

As a customer service manager at Contoso Coffee, you need to evaluate Customer Voice as a way to capture feedback after a case is resolved. In this lab, you create and preview a case feedback survey, review its satisfaction metrics, prepare an email template, and examine case-resolution automation. This exercise should take approximately 30 minutes to complete.

## Exercise 1 – Create a survey project

### Task 1 – Access Customer Voice

1. In a browser, go to [Dynamics 365 Customer Voice](https://customervoice.microsoft.com).

1. Sign in with the same Microsoft Entra account that you use for the course environment.

1. Confirm that the **All projects** page opens.

1. If access is denied, confirm that you used the correct account, and then ask your instructor to verify that your user has access to the course environment.

### Task 2 – Create a support project

Before you begin, choose a unique prefix that contains three through eight alphanumeric characters. Use the same prefix wherever the lab asks for `<prefix>`.

1. On the **All projects** page, select **New project**.

1. Select the **Support** template.

1. Select **Next**.

1. On the **Survey location** page, select **See all environments**.

1. Select the Dynamics 365 environment that you use for the course.

1. Select **Select and close**, and then select **Create**.

1. On the **All projects** page, rename the project `<prefix> Case Feedback`.

### Task 3 – Customize the survey

1. Open the `<prefix> Case Feedback` project, and then open its survey.

1. Change the survey title to **How did we do?**.

1. Set the first two survey questions to **Required**.

1. After the last question, select **Add new**, and then add a **Net Promoter Score** question.

1. Enter **How likely are you to recommend Contoso Coffee?**, and then set the question to **Required**.

1. In **Post-survey message**, enter **Thank you for your feedback** for the heading and **We review all feedback to improve our service.** for the message.

1. In the footer, enter **Contoso Coffee uses your feedback to improve customer service.**

## Exercise 2 – Personalize and evaluate the survey

### Task 1 – Add a case reference variable

1. On the survey's **Design** tab, expand **Customization**, and then select **Personalization**.

1. Select **Add variable**.

1. Enter `casereference` for the variable name.

1. Enter `Your support case` for the default value.

1. Select **Save**, and then close the **Personalization** pane.

1. Add a section heading at the start of the survey.

1. Insert the `casereference` variable followed by the text **has been resolved.**

### Task 2 – Review satisfaction metrics

1. Expand **Customization**, and then select **Satisfaction metrics**.

1. Review the customer satisfaction and sentiment metrics provided by the **Support** template.

1. Select **Add metrics**, and then select **Net Promoter Score**.

1. Enter `Recommendation` for the metric name.

1. Associate the metric with the **How likely are you to recommend Contoso Coffee?** question.

1. Select **Save**, and then close the **Satisfaction metrics** pane.

### Task 3 – Preview and test the survey

1. Select **Preview** on the survey toolbar.

1. Confirm that **Your support case has been resolved.** appears at the start of the survey.

1. Enter test responses and verify that the required questions can't be skipped.

1. Switch to the mobile preview and confirm that the survey remains readable.

1. Submit the preview response.

1. Select **Back** to return to the survey editor.

## Exercise 3 – Prepare survey distribution

The survey preview is the required validation path for this lab. Complete the following tasks if email distribution is available in your course environment.

### Task 1 – Create an email template

1. On the survey, select the **Send** tab.

1. Select **Email**.

1. Open the **Template** list, and then select **Create new**.

1. Enter `<prefix> Case Resolution` for the template name, and then select **Add**.

1. Replace the subject with **Please provide feedback on**, insert the `casereference` personalized variable, and then add the survey link to the message if it isn't already present.

1. Select **Save**.

1. Select **Cancel** to close the email composer without sending a message.

### Task 2 – Send a test invitation (optional)

1. On the **Send** tab, select **Email**.

1. Select the `<prefix> Case Resolution` template.

1. Enter your email address in **Recipients**.

1. For `casereference`, enter `Coffee Brewer Still Not Heating After Reset`.

1. Select **Send**.

1. If delivery is permitted, open the invitation and confirm that the case reference appears in the subject or survey.

> [!NOTE]
> Email delivery can be restricted in a course trial. The lab is complete even if you don't send or receive the optional test invitation.

## Exercise 4 – Review case-resolution automation (optional)

The **Support** project includes automation for sending a survey when a Dynamics 365 case is resolved. Connections and recipient data vary by environment, so you review or configure the flow without activating it.

### Task 1 – Configure the flow

1. On the survey's **Send** tab, select **Automation**.

1. Select **Send a survey when a case is resolved in Dynamics 365**. If the flow already exists, open it in Power Automate.

1. If prompted, select **Fix connection**, sign in with your course account, and then select **Continue**.

1. Select your course environment for the Dynamics 365 connection.

1. Select `<prefix> Case Feedback` for **Dynamics 365 Customer Voice Project**.

1. Select the survey and the `<prefix> Case Resolution` email template that you created.

1. Select **Create** or **Save**.

### Task 2 – Review the inactive flow

1. In Power Automate, go to **My flows**, and then open the case-resolution survey flow.

1. Confirm that the trigger monitors changes to Dynamics 365 cases.

1. Confirm that the flow checks for a resolved case and uses the Customer Voice **Send a survey** action.

1. Review how the recipient, project, survey, email template, and case reference are mapped.

1. Leave the flow turned off. Activating and testing it requires a case contact with a valid email address and is outside the required lab path.
