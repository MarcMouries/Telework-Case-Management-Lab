---
layout: default
title: Create a Workflow
parent: Part 3. Automate Work
nav_order: 1
---
# Part 3 – Create a Workflow

1. Back to the App Engine tab, **click** on the [Return to my application](#){: .aes_button } button

    ![relative](images/work_Return_to_my_application.png)

2. In the Automation section, **click** the **Add a process or third-party integration** link

    ![relative](images/automation_click_Add_a_process.png)

    From the Add Automation Screen, we are provided with a variety of process automation templates we can use to speed creation of common activities.

3. Click "Flow"

    ![relative](images/automation_click_Flow_Tile.png)

4. Click **Build**** from ****scratch** to create a new workflow

    ![relative](images/automation_Click_Build_From_Scratch.png)

    A flow is a sequence of actions to automate processes on the Now Platform.

    Logic and automation use computers to manage repeatable processes instead of using people. Logic and automation can reduce human error and speed up processes. App Engine Studio allows creators to add process flows to their applications.

5. Create the flow with the following information:

    1. Name: Main

    2. Description: Manage the Telework flow of work

    3. Click [Continue](#){: .aes_button}

6. **Click** the **Edit this flow** button to begin the configuration process

    ![relative](images/automation_your_flow_is_ready.png)

7. Since this is the first time we've launched Flow Designer, we're given the opportunity to go through the Flow Designer product tour.

8. Let's skip the tour for now, by clicking the **Skip tour** button.

    The first thing we'll do is set up our trigger to define when this flow will run.


9. Click on " **Add a trigger**" in the upper left of the flow designer screen.

    ![relative](images/automation_click_Add_a_Trigger.png)

    Flow designer provides different options for triggering a workflow. You can kick off a flow based on a record being created or updated, , run on a scheduled basis, or based on a unique application component like an SLA task being triggered or an inbound email being received by the instance. For our use case we are going to:

    1. select "Created" from the Record section

    2. and select our **Telework Case** table

    3. Click [Done](#){: .aes_button} to close the trigger

    ![relative](images/automation_configure_Trigger.png)

    Note that there might be circumstances under which we need to have a particular flow to execute.

    In this case we can use the "Add filters" option to define conditions that must be met for this flow to execute. This helps making flow easier to maintain and reuse.

    For example, we could use a flow specific to new request, one for renewal or request.

    ![relative](images/automation_Example_Trigger.png)


10. Now we'll add the actions to execute when this flow fires.

    1. Click **Add an Action, Flow logic, or Subflow**

    2. Choose " **Action**"

    ![relative](images/automation_Add_Action.png)

11. The first step in the process we want to automate is managing the approvals across departments.

    1. In the search field, type "approval"

    2. Select "Ask for Approval"
    ![relative](images/automation_Select_Ask_for_Approval.png)

12. The first thing we need to configure is the record we'll be working with for this action.

    1. Click on the data picker

    2. Select "Trigger – Record Created"

    3. Select "Telework Case Record"
    ![relative](images/automation_Ask_for_Approval.png)

13. In the **Rules** section, let's configure the approval rule. Click

    1. Choose "**Anyone approves**" for the Approval rule.
    ![relative](images/Choose_Anyone_Approves.png)

    2. Click on the Data Pill Picker button (_the magic wand button_)

        ![relative](images/Click_on_the_Data_Pill_Picker.png)

    3. Click "**Trigger - Record created**"

        ![relative](images/Click_Trigger_Record_Created.png)

    4. Click on the chevron to access the list of fields
    ![relative](images/Click_on_the_chevron_to_access the_list_of_fields.png)

    5. Locate the "**Opened by**" field and click on the chevron next to it
        
        ![relative](images/Click_on_chevron_of_Opened_by_field.png)

    6. Select **Manager**

        ![relative](images/approval_Select_Manager.png)

        We just configured an approval request to the manager of the person who submitted the form

    7. Click: [Done](#){: .aes_button }

14. Now let's configure what happens when the manager approves

    1. Under the Ask for Approval, **click** on the **"Add an Action. Flow logic or Sub flow**

    2. Select **Flow Logic**"

        ![relative](images/Click_Flow_Logic.png)

    3. Select "If"

        ![relative](images/Select_If.png)


15. Let's define the condition

    1. Give it a name in the Condition field " **Manager approves**"

    ![relative](images/Set_Condition_To_Manager_approves.png)

    2. Click on the Data Pill Picker (_magic wand button_)

    3. Click "1 – Ask for Approval"

    4. Click "Approval State"

     ![relative](images/Click_Approval_State.png)

    5. Set drop-down to "Approved"

     ![relative](images/Set_dropdown_to_Approved.png)

    6. Click: [Done](#){: .aes_button }


{: .note }
we now have a branch where we can add actions or flow logic if the manager approves
Let's save the team from sending tasks via emails or other systems.

16. We'll automatically request I.T. to assign a Remote Access Token to the employee

    1. Under "If Manager approves" click the small + to add a step
    ![relative](images/Add_Step_Under_If_Manager_Approves.png)

    2. Select " **Action**" > **ServiceNow Core**" > **Create Task**
    5. For Table, select " **Ticket**"
    6. Click "Add field value"
    7. Search and select " **Parent**"
    8. Click on the Data Pill Picker (_magic wand button_)
    ![relative](images/Click_on_the_Data_Pill_Picker.png)

    9. Select " **Trigger - Record created**" -\> " **Telework Case Record**"
    ![relative](images/Select_Trigger_Record.png)

    10. Click "+ Add field value" and add two other fields:

        Field Name              | Field Value
        ------------------------| --------------
        (1) Short description   | Remote Access Token |
        (2) Assigned to         | for testing assign it to yourself (System administrator) |

        This is how the **Field Values** should look:

        ![relative](images/how_the_Field_Values_Look_After.png)

    11. Let's add an annotation and set it to **Request Remote Access Token**

        ![relative](images/Add_an_annotation_AFTER.png)

    12. Click [Done](#){: .aes_button} 

17. First, let's take care of automating the notifications that take too much time right now. We'll send an email to the applicant's and let them know their application has been approved

    1. Under "If Create Task" click the small + to add a step

        ![relative](images/add_setp_under_if_2.png)

    2. Select " **Action**"

    3. Select " **ServiceNow Core**"

    4. Select " **Send Email**"

        ![relative](images/create_Task_Send_Email.png)

    5. Let's add an annotation and set it to **Notify Requester**

        ![relative](images/Add_Annotation_Notify_Requester.png)
    
    6. For the Target record, use the Data Pill Picker to select " **Trigger - Record created**" -\> " **Telework Case Record**"

        ![relative](images/select_target_record.png)

    7. For the " **To"** field,
        1. Click on the record picker
        2. Select " **Trigger - Record created**"
        3. Click on the chevron to access the list of fields
        4. Locate the " **Opened by**" field and click on the chevron next to it
        5. Select " **Email**"

        ![relative](images/Select_Opened_by_Email.png)

    8. For the " **Subject**", enter "Your Telework application is approved"

    9. For the " **Body**",

        1. Start by entering: "_Dear_" followed by a whitespace

        2. Use the record picker to select the " **Opened by – Name"** field

        ![relative](images/Select_Opened_by_Name.png)

        3. Hit Enter to move to the next line.

        4. Type "_Your application for:_"

        5. Use the Data Pill Picker to select the " **Arrangement –\> Code"** field

        ![relative](images/Select_the_Arrangement_Code.png)

        6. Type "is approved" after the data pill.

        7. The Body should look like this

        ![relative](images/email_body.png)

18. Click [Done](#){: .aes_button}

19. Your flow should look like this:

    ![relative](images/final_flow.png)

20. Click on the Toggle view to visualize the flow as a Diagram

    ![relative](images/Toggle_Diagram_View.png)


20. Click [Save](#){: .aes_button} in the top right corner of the screen

    Although the Flow is saved, it won't run until we activate it.

21. Click [Activate](#){: .aes_button} on the left of the Save button

22. In the Confirmation box click the **Activate** button.

Congratulations! 🎉 You've built a flow that takes care of managing tasks and communications across multiple departments.

{: .note }
Note that by default Personal Developer Instances have "sending email" turned off by default.
If you want to receive the email, make sure that the user submitting the application has a valid email address on their user record.

Next, let's test our work and see it in action.

[Next: Test the Workflow](./Part_3.2_Test_the_Workflow.md){: .btn .btn-green-sn }