# Part 3 – Automate the work

**Purpose**

In this exercise, we will move beyond simply digitizing data entry and we will focus on ways we can drive optimization though automation

## Section1–BuildinganAutomation Flow

1. Back to the App Engine tab, **click** on the \_ Return to my application \_

![](RackMultipart20221028-1-d1lmac_html_c95dc1f45f320adb.png)

1. In the Automation section, **click** the **Add a process or third-party integration** link

![](RackMultipart20221028-1-d1lmac_html_5b2e2567b75bd0fd.png)

From the Add Automation Screen, we are provided with a variety of process automation templates we can use to speed creation of common activities.

1. Click "Flow"
 ![](RackMultipart20221028-1-d1lmac_html_991f4007666333e8.png)


2. Click **Build**** from ****scratch** tocreateanewcustomflow

![](RackMultipart20221028-1-d1lmac_html_85ae604dcb17d8e.png)

A flow is a sequence of actions to automate processes on the Now Platform.

Logic and automation use computers to manage repeatable processes instead of using people. Logic and automation can reduce human error and speed up processes. App Engine Studio allows creators to add process flows to their applications.

1. Set up the flow

|

  1. Name
 | **Main** |
| --- | --- |
|

  1. Description
 | **Manage the flow of work** |
|

  1. Click \_Continue\_
 |

1. **click** the **Edit this flow** button to begin the configuration process

![](RackMultipart20221028-1-d1lmac_html_ea5bd0d382f5405b.png)

1. Since this is the first time we've launched Flow Designer, we're given the opportunity to go through the Flow Designer product tour.


2. Let's skip the tour for now, by clicking the Skip tour button.

The first thing we'll do is set up our trigger to define when this flow will run.

1. Click on " **Add a trigger**" in the upper left of the flow designer screen. ![](RackMultipart20221028-1-d1lmac_html_d5d2dc069803d64b.png)

Flow designer provides different options for triggering a workflow. You can kick off a flow based on a record being created or updated, , run on a scheduled basis, or based on a unique application component like an SLA task being triggered or an inbound email being received by the instance.

For our use case we are going to :

  1. select "Created" from the Record section
  2. and select our **Telework Case** table
  3. Click \_ Done \_ to close the trigger

![](RackMultipart20221028-1-d1lmac_html_65fd0d872f4dcb02.png)

Note that there might be circumstances under which we need to have a particular flow to execute.

In this case we can use the "Add filters" option to define conditions that must be met for this flow to execute. This helps making flow easier to maintain and reuse.

For example, we could use a flow specific to new request, one for renewal or request.

![](RackMultipart20221028-1-d1lmac_html_8125caf7712d33dc.png)

1. Now that we have configured the trigger, we need to set up what will happen when this flow fires.

  1. Click **Add an Action, Flow logic, or Subflow**
  2. Choose " **Action**"

 ![](RackMultipart20221028-1-d1lmac_html_e451db40e40bb726.png)

1. The first step in the process we want to automate is managing the approvals across departments.

  1. In the search field, type "approval"
  2. Select "Ask for Approval"

 ![](RackMultipart20221028-1-d1lmac_html_3cb4d6a5f1f5b0d9.png)

1. The first thing we need to configure is the record we'll be working with for this action.

  1. Click on the data picker
  2. Select "Trigger – Record Created"
  3. Select "Telework Case Record"

![](RackMultipart20221028-1-d1lmac_html_d14a0bc9da16c5e8.png)

1. In the **Rules** section, let's configure the approval rule. Click

  1. Choose " **Anyone approves**" for the Approval rule.
 ![](RackMultipart20221028-1-d1lmac_html_ccb99ae69aa11e60.png)


  2. Click on the Data Pill Picker button (_the magic wand button_)
 ![](RackMultipart20221028-1-d1lmac_html_4e54c98c647f8534.png)

  3. Click " **Trigger - Record created**"
 ![](RackMultipart20221028-1-d1lmac_html_f9652c2c7236ad34.png)


  4. Click on the chevron to access the list of fields
 ![](RackMultipart20221028-1-d1lmac_html_923f11226bd9f3e9.png)


  5. Locate the " **Opened by**" field and click on the chevron next to it
 ![](RackMultipart20221028-1-d1lmac_html_d47b8c8cb9baf8a0.png)


  6. Select " **Manager**"
 ![](RackMultipart20221028-1-d1lmac_html_979db6a36e9864be.png)

We just configured an approval request to the manager of the person who submitted the form

  1. Click: \_Done\_

1. Now let's configure what happens when the manager approves

  1. Under the Ask for Approval, **click** on the **"Add an Action. Flow logic or Sub flow**
  2. Select " **Flow Logic**"
 ![](RackMultipart20221028-1-d1lmac_html_47904dee3e0bdc24.png)


  3. Select "If"
 ![](RackMultipart20221028-1-d1lmac_html_fe810a9bd09dac53.png)

1. Let's define the condition

  1. Give it a name in the Condition field " **Manager approves**"
 ![](RackMultipart20221028-1-d1lmac_html_9af12c9c3d8471d1.png)


  2. Click on the Data Pill Picker (_magic wand button_)
  3. Click "1 – Ask for Approval"
  4. Click "Approval State"
 ![](RackMultipart20221028-1-d1lmac_html_47eed24bcc382bd3.png)


  5. Set drop-down to "Approved"
 ![](RackMultipart20221028-1-d1lmac_html_4440cf00c216bbcc.png)
  6. Click: \_Done\_

**Notice that we now have a branch where we can add actions or flow logic if the manager approves.**

**Let's save the team from sending tasks via emails or other systems.**

1. We'll automatically request I.T. to assign a Remote Access Token to the employee

  1. Under "If Manager approves" click the small + to add a step ![](RackMultipart20221028-1-d1lmac_html_24642acc6df97c16.png)

  1. Select " **Action**"
  2. Select " **ServiceNow Core**"
  3. Select " **Create Task**"
  4. For Table, select " **Ticket**"
  5. Click "Add field value"
  6. Search and select " **Parent**"
  7. Click on the Data Pill Picker (_magic wand button_)
 ![](RackMultipart20221028-1-d1lmac_html_27d50e8cce8fcf9f.png)


  8. Select " **Trigger - Record created**" -\> " **Telework Case Record**"
 ![](RackMultipart20221028-1-d1lmac_html_104fbbb80a4abe56.png)


  9. Click "+ Add field value" and add two other fields:

| 1) Short description | Remote Access Token |
| --- | --- |
| 2) Assigned to | for testing assign it to yourself (System administrator) |

This is how the **Field Values** should look:
 ![](RackMultipart20221028-1-d1lmac_html_404845ed288148fa.png)

  1. Let's add an annotation and set it to Remote Access Token
 ![](RackMultipart20221028-1-d1lmac_html_a0db7730fdd7d936.png)

 ![](RackMultipart20221028-1-d1lmac_html_de3d46ab4784c452.png)

  1. Click: \_Done\_

1. First, let's take care of automating the notifications that take too much time right now. We'll send an email to the applicant's and let them know their application has been approved

  1. Under "If Create Task" click the small + to add a step

 ![](RackMultipart20221028-1-d1lmac_html_386c1d411b71843d.png)

  1. ![](RackMultipart20221028-1-d1lmac_html_a1e3bfbfc1cd333a.png)Select " **Action**"
  2. Select " **ServiceNow Core**"
  3. Select " **Send Email**"

  1. For the Target record, use the Data Pill Picker to select " **Trigger - Record created**" -\> " **Telework Case Record**"
 ![](RackMultipart20221028-1-d1lmac_html_a40276aaa1ece30.png)


  2. For the " **To"** field,
    1. Click on the record picker
    2. Select " **Trigger - Record created**"
    3. Click on the chevron to access the list of fields
    4. Locate the " **Opened by**" field and click on the chevron next to it
    5. Select " **Email**"

![](RackMultipart20221028-1-d1lmac_html_6ff09e45d1be73e6.png)

  1. For the " **Subject**", enter "Your Telework application is approved"
  2. For the " **Body**",

| 1) Start by entering: "Dear" followed by space |
| --- |
| 2) Use the record picker to select the " **Opened by – Name"** field
 ![](RackMultipart20221028-1-d1lmac_html_dd46a5132b0d5aac.png) |
| 3) Hit Enter to move to the next line. |
| 4) Type "Your application for: "

 |
| 5) Use the Data Pill Picker to select the " **Arrangement –\> Code"** field
 ![](RackMultipart20221028-1-d1lmac_html_e21933aec52a817a.png)


6) Type "is approved" after the data pill.

7) The Body should look like this
 ![](RackMultipart20221028-1-d1lmac_html_e789f767a8878c07.png) |

1. Click: \_Done\_


2. Click: \_Save\_ in the top right corner of the screen

Although the Flow is saved, it won't run until we activate it.

1. Click on the \_Activate\_ button on the left of the Save button

1. In the Confirmation box click the Activate button.

Congratulations! 🎉 You've built a flow that takes care of managing tasks and communications across multiple departments.

Note that by default Personal Developer Instances have "sending email" turned off by default.

If you want to receive the email, make sure that the user submitting the application has a valid email address on their user record.

Next, let's test our work and see it in action.

## Section 2– Testing a Flow

In this section, we will test the flow we just created and make sure it functions as expected.

We need to test with a user who has a manger, fortunately ServiceNow allows to impersonate other authenticated users for testing purposes

Let's go back to the ServiceNow admin page

1. In the banner frame, click your profile photo in the top right to open the user menu.
2. Select  **Impersonate User**.
 ![](RackMultipart20221028-1-d1lmac_html_e5b3c305c9c87e33.png)

The Impersonate User dialog box appears.

1. Search for "David Loo" (who has a manager).
2. Select him
3. Click Impersonate User
4. Close the pop-up
 ![](RackMultipart20221028-1-d1lmac_html_76f709f143a1a46e.png)

Let's go back to the ServiceNow Portal page and submit a new application.

1. Open a new browser tab and go to https://\<instance\_name\>.service-now.com
2. Search for Telework
3. Open the catalog item
4. Complete and Submit the form
 ![](RackMultipart20221028-1-d1lmac_html_6d6676a854d98f3f.png)

**Let's check the execution:**

1. Go back to the ServiceNow admin page
2. Impersonate David Loo's manager : Bud Richman"
3. With email enabled on the instance and a valid email address, the manager would get an email notification and allow the manager to approve or reject.
4. Let's check if the manager has any approval request in "My Approvals list"
  1. In the search, type "my approvals"
 ![](RackMultipart20221028-1-d1lmac_html_3debc5c8c48ee299.png)
  2. Click on "My approvals"


  3. Yes. There is one. Right-click on the "Requested"


  4. Select "Approve"
 ![](RackMultipart20221028-1-d1lmac_html_f74aeaa1fa465721.png)

1. Next, let's check if an email was sent
  1. In the top right, click the profile photo to open the User menu.
  2. Select  **"End Impersonation"**.
 ![](RackMultipart20221028-1-d1lmac_html_7836a501e0dcc8f3.png)


  3. on the top-left, type " **Outbox**"
  4. Select " **Outbox**"
 ![](RackMultipart20221028-1-d1lmac_html_911f49aebc43b40f.png)


  5. We have an email! Click on it to open it
 ![](RackMultipart20221028-1-d1lmac_html_ab840a5dfa38d075.png)

  1. On the email record, scroll down to the bottom of the page, and click on Preview Email
 ![](RackMultipart20221028-1-d1lmac_html_874007f64808961c.png)

  1. And voila! Observe the email that was sent.

    1. We have automated case updates notifications.


    2. Notice the watermark at the bottom of the email. ServiceNow generates a watermark label at the bottom of each notification email to allow matching incoming email to existing records. This helps track emails sent as part of a case and manage responses to emails.

![](RackMultipart20221028-1-d1lmac_html_996d6bfd66649a8.png)

Congratulations! You successfully built and tested a workflow that saves a lot of time in the organization and makes sure tasks are assigned.

