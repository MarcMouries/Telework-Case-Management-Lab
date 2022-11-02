---
layout: default
title: Test the Workflow
parent: Part 3. Automate Work
nav_order: 2
---
# Let's Test the Workflow

In this section, we will test the flow we just created and make sure it functions as expected.

We need to test with a user who has a manger, fortunately ServiceNow allows to impersonate other authenticated users for testing purposes

Let's go back to the ServiceNow admin page

1. In the banner frame, click your profile photo in the top right to open the user menu.

2. Select  **Impersonate User**.

    ![relative](images/Select_Impersonate_User.png)

    The Impersonate User dialog box appears.

1. Search for "David Loo" (it's one of the demo user who has a manager).
2. Select him
3. Click *Impersonate User*
4. Close the pop-up

![relative](images/Close_the_Impersonation_Pop-up.png)

Let's go back to the ServiceNow Portal page and submit a new application.

1. Open a new browser tab and go to https://\<instance\_name\>.service-now.com
2. Search for Telework
3. Open the catalog item
4. Complete and Submit the form

    ![relative](images/catalog_item_form.png)


**Let's check the execution:**

1. Go back to the ServiceNow admin page
2. Impersonate David Loo's manager : Bud Richman"
3. With email enabled on the instance and a valid email address, the manager would get an email notification and allow the manager to approve or reject.
4. Let's check if the manager has any approval request in "My Approvals list"
  1. In the search, type "my approvals"

      ![relative](images/catalog_item_form.png)

  2. Click on "My approvals"


  3. Yes. There is one. Right-click on the "Requested"


  4. Select "Approve"
 ![](RackMultipart20221028-1-d1lmac_html_f74aeaa1fa465721.png)

1. Next, let's check if an email was sent
  1. In the top right, click the profile photo to open the User menu.

  2. Select  **"End Impersonation"**.
    ![relative](images/Click_on_End_Impersonation.png)

  3. on the top-left, type " **Outbox**"

  4. Select " **Outbox**"

    ![relative](images/Click_the_Outbox_link.png)

  5. We have an email! Click on it to open it
    ![relative](images/Click_on_the_email_link.png)

  1. On the email record, scroll down to the bottom of the page, and click on Preview Email

    ![relative](images/Click_on_Preview_Email.png)

  1. And voila! Observe the email that was sent.

    1. We have automated case updates notifications.

    2. Notice the watermark at the bottom of the email. ServiceNow generates a watermark label at the bottom of each notification email to allow matching incoming email to existing records. This helps track emails sent as part of a case and manage responses to emails.

    ![relative](images/Preview_Email_Telework.png)

Congratulations! You successfully built and tested a workflow that saves a lot of time in the organization and makes sure tasks are assigned.