---
layout: default
title: Import Data
parent: Part 1. Build the Foundation
nav_order: 4
---

## Section 3 – Import Legacy Data

1. Hover the column header **Number** , **right-click** to display the table menu options and then select **Import.**

    ![relative](images/Select_Import.png)

2. Select **Choose File** to upload the Excel file: Telework Cases.xlsx

    ![relative](images/Select_Choose_File_to_Upload_the_Excel_file.png)

3. Click **Upload** and wait until the import is complete.

    ![relative](images/Import_Click_Upload.png)

4. Once loaded, click on **Preview Imported Data**

    ![relative](images/click_on_Preview_Imported_Data.png)

5. Scroll down and click on the **Complete Import** button

    ![relative](images/Click_on_the_Complete_Impor_button.png)

6. You'll now see that we have migrated our data.

    ![relative](images/we_now_have_migrated_our_data.png)

7. Let's update the columns in this list layout.

8. Right click at the top of the Number column and click on "Configure" -\> "List Layout"

    ![relative](images/Click_on_Configure_List_Layout.png)

9. Move "Task type" to the left hand window and click Save
    ![relative](images/Remove_Task_type.png)

Next, let's start working and managing our records

10. Hover the column header **Priority** , **right-click** to display the menu and then select **Pie Chart**

    ![relative](images/select_Pie_Chart.png)

11. And voila, we get a Pie chart that shows us the distribution of cases by Priority

    ![relative](images/And_Voila_we_get_a_Pie_chart.png)

12. Explore the other tools in the Context Menu such as Visual Task Board
    
13. The team struggles managing and understand the status of related tasks. Let's fix that.
    
14. Click the back button on the Pie Chart report to get back to the list
    ![relative](images/Click_the_back_button_on_the_Pie_Chart_report.png)

15. Open a record by clicking the number field

    ![relative](images/Open_a_record_by_clicking_the_number_field.png)

16. Configure the related list by doing:

    1. Right-click on header
    2. Select **Configure**
    3. Then select **Related Lists**

    ![relative](images/Configure_the_related_list.png)

17. In the new form:

    1. Select the item " **Task → Parent**"
    2. Click on the button to move the item to the selected list
    3. Click he [Save](#){: .aes_button }

    ![relative](images/Add_Task_Parent.png)

Now a new tab at the bottom of the form will show records that have relationships to the current record.

    ![relative](images/related_list_shows_related_records.png)

18. Go back to the list view by clicking on the back button at the top

    ![relative](images/Go_back_to_the_list_view.png)

19. We can even start creating new records/cases

20. Click \_New\_ in the top right
    ![relative](images/Create_Case_Cilck_New_in_the top_right.png)

21. Fill out the form and click "Submit" to create a test record.

22. Close the Table Builder and Preview tab by **clicking** the **X** on them.
    ![relative](images/Close_the_Preview_Tab_by_clicking_the_X.png)

23. Next, we'll work on configuring the user experience.

**Exercise Recap**

In this exercise, we learned how to create a new application and map out the data elements important to enable our business process.

We learned to use the Table Builder to add and configure columns including Reference fields and Choice lists.

We were able to complete all these tasks using simple point-and-click administration and without requiring specialized application or database knowledge.

[Next: User Interface]( ../Part_2_The_User_Experience/Part_2.0_Main.html){: .btn .btn-green-sn }