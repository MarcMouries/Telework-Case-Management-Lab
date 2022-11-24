---
layout: default
title: Create the Request Form
parent: Part 2. Create the User Experience
nav_order: 2
---

# Create the Request Form

## Purpose

ServiceNow offers multiple ways to create a user experience for submitting a form. In this exercise, we will learn one quick way to get users off paper forms and emails.

1. Close the "Now Experience – Telework Request" App Engine Studio tab
 ![](RackMultipart20221028-1-d1lmac_html_6f3fe518bfb2eae2.png)


2. On the application homepage, locate the Experience section and click the ⨁ Add icon.
 ![](RackMultipart20221028-1-d1lmac_html_7528b4d3b454d89e.png)

This takes us to a selection where we can identify the type of experience we wish to create.

3. **Select** the **Record Producer** option.

    ![relative](./user_form/Select_the_Record_Producer_option.png)

1. This launches the record producer creator.

2. Click the [Begin](#){: .aes_button } button

3. Set the following values (💡 double-click, copy & paste into the form)

    Field Name            | Field Value
    ----------------------| --------------
    (1) Name              | Apply for Telework
    (2) Short Description | Use this form to apply for Telework

    ![relative](./user_form/Set_Record_Producer_Name.png)

    {: .note }
    A record producer is a specific type of catalog item that allows end users to create task-based records from the service catalog.

4. Click the [Continue](#){: .aes_button } button

5. Click the [Edit record producer](#){: .aes_button } button

6. Click on **Destination** , then type **Tel**, and select the **Telework Case** table

    ![relative](./user_form/Click_on_Destination.png)

7. Click on **Location** , then under **Catalogs**, click on **Browse**.

    ![relative](./user_form/Select_Catalog.png)

8. Click on **Service Catalog** , then click on the right arrow to move the item over to the Selected list

    ![relative](./user_form/selected_catalog.png)

9. At the bottom, click on the [Save selections](#){: .aes_button } buttonn

10. Under **Categories** , **click** on **Browse**

11. Move **Can We Help You?** to the right-hand side and click on the [Save selections](#){: .aes_button } buttonn

    Your screen should look like below
    ![relative](./user_form/selected_catalog_Final.png)

12. Let's add questions to the form

    {: .note }
    Unlike in a paper-based form, we don't need to ask users to fill personal information like first name, last name, …, or date of request. That information will be automatically attached to the case. This makes filling forms so much faster.


13. We want to allow users to open a case on behalf of another individual, so let's start by asking users " **Who is this request for?**" and " **When do you need this?"**

14. **Click** on Questions

15. **Click the arrow next to** Insert new questionthen click "Question set"

    ![relative](./user_form/Click_Insert_new_question.png)

16. Select "Standard Employee Questions" and click Submit

    ![relative](./user_form/Select_Standard_Employee_Questions.png)

    This will add two frequently asked questions on forms
    ![relative](./user_form/Standard_Employee_Questions_Added.png)


17. One key information we need users to provide is the type of arrangement they are applying for.
    1. Click Insert new question
    2. For Question type, select **Choice**
    3. For **Question subtype** , select **Record reference**

    ![relative](./user_form/Question_subtype_select_Record_reference.png)

    4. Scroll down to the **Details** section

    5. In the **Details** section, enter the following information: (💡 double-click, copy & paste into the form)

        Field Name                   | Field Value
        -----------------------------| --------------
        **Map to a specific field**  | We want to store that information so let's check the box
        **Table field**              | choose **Arrangement**
        **Question label**           | What type of Telework arrangement are you applying for? |
        **Mandatory**                | Checked |

        {: .note }
        Notice the **Question Preview** that shows what the question will look like to the user.

        ![relative](./user_form/question_Arrangement.png)

    6. Click on **Continue to Additional details →**

    7. In the **Additional details** section, set the **Source Table** to the **Arrangement** table we imported earlier. 
     as options for this question.

    8. then Click on the **Annotation** tab

        ![relative](./user_form/Click_on_the_Annotation_Tab.png)

    9. Today, the team is spending a lot of time correcting and manually re-routing applications due to people confusing the different types of Telework arrangement. Let's fix that.

    10. We'll use the  **Annotation**  tab to provide users with additional instructions for the question.

    11. Check the box **Show**** instructions**

    12. Open the file: **telework form annotation.docx**

    13. Copy all the text in the file ( ⌘ Cmd  or CTRL+A, CTRL+C )

    14. Paste it into the Annotation section of the Telework Form (⌘ Cmd  or CTRL+V )

    15. **Click** on the [Insert Question](#){: .aes_button } button

    ![relative](./user_form/add_Annotation_Complete.png)

18. Back to the main form, **click** on the [Insert new question](#){: .aes_button } button

    ![relative](./user_form/Click_on_Insert_New_Question.png)

19. When users select the arrangement type **Situational** , we'll prompt them for the number of days per week. 

    1. So, let's go ahead and in the **Type** section set the following values:

        Field Name                    | Field Value
         -----------------------------| --------------
         Question type                | Text
         Question subtype             | Single line

        ![relative](./user_form/question_Text_Single_line.png)

    2. Scroll down to the **Details** section

    3. In the **Details** section, enter the following information: (💡 double-click, copy & paste into the form)

        Field Name                   | Field Value
        -----------------------------| --------------
        Map to a specific field      | Checked
        Table field                  | Days per week
        Question label	             | Number of Days per Week?

    4. Click on **Additional details**

        ![relative](./user_form/Question_Number_of_Days_per_Week.png)

    5. In the **Additional details** section, for the **Text validation** field, select **Number**

    6. Click on **Insert Question**

20. Back to the **Questions** page, we're going to define the dynamic behavior of this question based on the answer to the previous question.

    1. Click on the **behavior** icon
    2. Click on the **Define new behavior** icon

    ![relative](./user_form/Click_on_the_Define_new_behavior_icon.png)

    3. In the **Actions** tab, we'll specify the behavior we need:

        Field Name                     | Field Value
        ------------------------------ | --------------
        ① Make the question mandatory | Yes
        ② Make the question visible   | Yes

        ③ Click on the **Conditions** tab

        ![relative](./user_form/Define_Behavior_Actions.png)

    4. In the **Conditions** tab,

        1. Set the filter to [arrangement] [is] [Situational Telework]

        2. Click on the [Add behavior](#){: .aes_button } button

        ![relative](./user_form/Define_Behavior_Condition.png)

21. Back to the questions page,

    ① Click on the [Save](#){: .aes_button } button

    ② Click on Preview

    1. **Click** on the [Save](#){: .aes_button } button

    2. Click on Preview

    ![relative](./user_form/Define_Behavior_Save_Preview.png)

22. The **Preview** page allows to visualize what our form will look like in different experiences. (You can interact with the item but not submit it).

    | **Mobile** | **Portal** |
    | --- | --- |
    | ![relative](./user_form/Preview_Mobile.png) |  ![relative](./user_form/Preview_Portal.png)  |

23. Close the Preview by clicking on the X on the top right

    ![relative](./user_form/Preview_Close.png)

    {: .note }
    If you want to preview your catalog item in the Virtual Agent you will need to activate the plugins_ _ **Glide Virtual Agent** and **Service Management Virtual Agent Topic Blocks**.
    Additional setup beyond that is required to get NLU to perform a topic conversation via the Virtual Agent.
    Feel free to experiment this after completing the entire lab.


24. Let's publish the form to the Service Portal

    1. Click on **Review and Submit**
    2. Click on Submit
   ![relative](./user_form/Click_on_Review_and_Submit.png)

25. Congratulations. The form is published on your development instance.

    ![relative](./user_form/Success_Submission_Catalog.png)

26. Let's see how users can easily find it on the Service Portal

27. Go to the tab with ServiceNow Admin Home page

    ![relative](./user_form/go_to_the_Home_tab.png)

28. and then open the Service Portal
    1. Click All
    2. Type **Portal**
    3. Click on **Service Portal**

    ![relative](../open_portal.png)


28. In the portal, search for "Telework"

    ![relative](./user_form/Sp_Search_for_Telework.png)

29. The catalog item is found.

31. Click on the item to apply for Telework

    ![relative](./user_form/Click_Apply_for_Telework.png)

32. In the **Details** section, enter the following information: (💡 double-click, copy & paste into the form)

    Field Name                     | Field Value
    ------------------------------ | --------------
    (1) Who is this request for?   | David Loo
    (2) When do you need this?     | This week
    (3) What type of arrangement?  | Situational
    (4) Number of days per week?   | 3

    5) Click on the [Submit](#){: .aes_button } button

    ![relative](./user_form/Form_Apply_for_Telework_Filled.png)


**Exercise Recap**

In this exercise, we learned how to use App Engine Studio (AES) to easily create customized Catalog Items that users can access in Service Portal and on mobile devices.

Our next exercise will focus on taking the building blocks created to this point and making them actionable to drive automation and process optimization

[Next > Automate Work](../Part_3_Automate_Work/Part_3.0_Main.md){: .btn .btn-green-sn }