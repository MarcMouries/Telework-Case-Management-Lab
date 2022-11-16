---
layout: default
title: Create the tables
parent: Part 1. Build the Foundation
nav_order: 2
---

# Create the Data

We will create the core tables for our application. To create a table in App Engine Studio:

1. Click the  **Add**  icon (⨁ Add) for _Data_ on the _App Home_ tab.

    ![relative](images/data_add_icon.png)

2. On the _How do you want to add data to your app?_ screen, select the **Create a table** tile.

    ![relative](images/data_create_table_tile.png)

    ![relative](images/1_Add_Table_Begin.png)

3. Click on the [Begin](#){: .aes_button } button

4. On the _How do you want to create a table?_ screen, select the  **Upload a spreadsheet**  tile.

    ![relative](images/data_upload_a_spreadsheet.png)

5. Click on the [Continue](#){: .aes_button } button

6. On the _Let's choose the spreadsheet you want to upload_ screen, click the  **Drag and drop or browse to upload spreadsheet** link

    ![relative](images/data_drag_drop_spreadsheet.png)

7. Browse and select the  **Telework Data.xlsx**  file you downloaded

    ![relative](images/data_drag_drop_spreadsheet.png)

8. Click [Continue](#){: .aes_button } button

9. Our spreadsheet has multiple sheets. **We only need the first one** "Telework Arrangement".

10. Select ☑ **Import spreadsheet data** in the "Telework Arrangement" box.

11. Click on **Convert to table** to the right of the Telework Arrangement Sheet name.

    ![relative](images/data_Convert_to_table.png)

    {: .note}
    We need to set what value to display when these records will be referenced

12.  Let's set the display value

     1. Click the  **Expand/Collapse**  icon (⌄) to see advanced configuration options.

     2. Check **Display**

     3. Click [Continue](#){: .aes_button } button

     ![relative](images/data_Check_Display.png)

15. Set the table label to **Arrangement**.The table name will auto populate.

    ![relative](images/data_Set_the_table_label.png)

16. Click [Continue](#){: .aes_button } button

17. Click the **All** checkbox for the **admin** role.

18. Click the **Read** checkbox for the **user** role.

     **TODO**: update screenshot
     
     ![relative](images/data_add_table_permissions.png)


    {: .note}
    We need to set what value to display when these records will be referenced

19. Click [Continue](#){: .aes_button } button

20. A loading screen will appear while the table is being created. When it completes, click [Done](#){: .aes_button }

21. We haven't converted all the sheets in the spreadsheets, so we'll see this message pop up

    ![relative](images/data_leave_without_converting_other_sheets.png)

22. Click [Yes, leave](#){: .aes_button }

23. Again, click the  **Add**  icon (⨁ Add) for _Data_ on the _App Home_ tab.

    ![relative](images/data_add_icon.png)

24. On the _How do you want to add data to your app?_ screen, select the **Create a table** tile.

    ![relative](images/data_create_table_tile.png)

25. Click [Begin](#){: .aes_button} button

26. On the _How do you want to create a table?_ screen, Select **Create from an existing table**.

    ![relative](images/data_Create_from_an_existing_table.png)

27. Click the [Continue](#){: .aes_button } button

28. Type **Task,** then select the table **Task [task]** and Click [Continue](#){: .aes_button }

    ![relative](images/data_select_the_table_Task.png)

29. Give the table the following properties

    Field Name      | Field Value
    ----------------| --------------
    (1) Table label | Telework Case
    (2) Auto number | Checked ☑
    (3) Prefix      | TLW

    {: .note }
    You can add an identifiable tracking number to your records to make them easier to manage and follow. Selecting this option will automatically add your designated tracking number to each record in this table.

    ![relative](images/data_new_table_properties.png)

30. Click [Continue](#){: .aes_button }


31. Click the **All** checkbox for the **admin** role.

32. Click the **Create**, **Read**, and **Write** checkbox for the **user** role.

    ![relative](images/data_add_table_permissions.png)

33. Click [Continue](#){: .aes_button }

34. Once the table is ready, let's add the fields (columns) we need. Clic **Edit table**.

    ![relative](images/data_edit_table.png)

35. We now see the Table Builder screen. From this screen, we can see the fields that were automatically added to our table by the system, as well as add additional columns.

    ![relative](images/data_intro_table_builder.png)

36. Review the introduction to Table Builder then **click** the **Next** button to walk through each information pane. From the last screen, **click** the **Get Started** button.

37. Now let's add the data columns for our application. Start by **clicking** the **Add new field** link at the top of the screen

    ![relative](images/data_Add_new_field.png)

38. In the new row created, add the following values:

    1. Label: **Arrangement**
    2. Hit the [ENTER] key
    3. Column name: arrangement (auto-generated)
    4. Hit the arrow key ▸ [twice]
    5. Hit the [ENTER] key
    6. Type: **Reference** then select Arrangement

    ![relative](images/Table_Add_Arrangement_Field.png)

39. Again, **click** the **Add new field** link at the top of the screen

40. In the new row created, add the following values:

    1. Label: " **Number of Days**"
    2. Hit the [ENTER] key
    3. Column name: (auto-generated)
    4. Type: **Integer**

41. Again, **click** the **Add new field** link at the top of the screen

42. In the new row created, add the following values:

    1. Label: **Reason**
    2. Hit the [ENTER] key
    3. Column name: reason (auto-generated)
    4. Hit the arrow key ▸ [twice]
    5. Hit the [ENTER] key
    6. Type: **Choice**
    7. Choice Type: Dropdown with -- None –
    8. Choices:
        1. Dependent Care
        2. Medical
        3. Reasonable Accommodation

    ![relative](images/table_add_reason_choices.png)

43. Click [Done](#){: .aes_button }

44. We now have all the data elements we need to manage our use case.

45. Click the [Save](#){: .aes_button } button at the top right to finalize your configurations.

    ![relative](images/Create_Table_Click_the_Save_button.png)

46. Congratulations, you've built the first tables in your solution.

    **Let's take a look at the form that has been generated for our table and adjust the layout.**

47. At the top-center of the table, click **Form views**

    ![relative](images/data_layout_click_form_views.png)

    As we created our table by extending the Task table, we inherited some fields we don't need for our use case.

48. Remove the following fields (by clicking the X)

    1. Number
    2. Configuration Item,
    3. Active,
    4. Parent

    ![relative](images/data_layout_remove_fields.png)

49. Users want to see who opened the case. We can easily fulfill the requirement by reusing the Opened by field from the Task table. In the Fields tab to the left is where existing fields can be added. Notice how there are 63 fields available to use.

    ![relative](images/data_layout_add_form_elements.png)

50. Type **Opened by** in the Search box

51. Drag the **Opened by** field onto the form

    ![relative](images/data_Drag_the_Opened_by_field.png)

    ![relative](images/data_Drag_the_Opened_by_field_AFTER.png)

52. Click on "Formatters"

    {: .note }
    CLEAR the  search field
    ![relative](images/data_Click_on_Formatters.png)

53. Drag the "**Activities (filtered)**" field onto the form below the Short description field.

    ![relative](images/data_Drag_the_Activities_field.png)

54. Add the **Arrangement"** field to the main section of the form.

    ![relative](images/form_add_the_Arrangement_field.png)

55. Add the **Number of Days** field to the main section of the form.

    Your form should look like this:

    ![relative](images/data_final_form_layout.png)

56. On the top right, click [Save](#){: .aes_button }

    ![relative](images/form_Click_Save.png)

57. Click the **Table** button on the top banner.

    ![relative](images/data_click_table.png)

58. Click the **Preview** button on the top right.

    ![relative](images/data_click_Preview.png)

    When records will be created they will appear here.

    ![relative](images/data_no_records.png)


**Exercise Recap**

In this exercise, we learned how to create a new application and map out the data elements important to enable our business process.

We learned to use the Table Builder to add and configure columns including Reference fields and Choice lists.

We were able to complete all these tasks using simple point-and-click administration and without requiring specialized application or database knowledge.

[Next: User Experience](../Part_2_The_User_Experience/Part_2.0_Main.md){: .btn .btn-green-sn }