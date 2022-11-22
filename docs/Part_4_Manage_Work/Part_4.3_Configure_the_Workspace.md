---
layout: default
title: Configure the Workspace
parent: Part 4. Manage work
nav_order: 4
---
# Configure the Workspace

The Workspace Builder empowers users of all skill sets to build a custom workspace in a no-code environment. With this builder, you can quickly create a workspace and configure its layout, lists, and record pages. If you need access to more advanced functionalities and configurations, you can open the workspace in UI Builder from within this builder.

A lot has been pre-configured for us. We'll make a couple changes to improve it.

1. Let's make sure the scores point to the Telework table

2. (1) Click the **Unassigned Tasks** score, (2) Click Configure (3) Click the Task table

    ![relative](workspace/Edit_Visualization_Unassigned.png)

3. (1) Type "Telework", (2) <kbd>⏎ Enter</kbd>, (3) Click the Telework table, (4) Click **Add custom conditions**

    ![relative](workspace/edit_data_source.png)

4. Set the Condition to **Assigned to = Empty**
    1. Set the condition
    2. Click Run
    3. Click Apply

    ![relative](workspace/apply_data_source_filter_condition.png)

5. (1) Click the **Critical Tasks** score, (2) Click Configure (3) Click the Task table

    ![relative](workspace/Edit_Visualization_Critical_Tasks.png)

6. (1) Type "Telework", (2) <kbd>⏎ Enter</kbd>, (3) Click the Telework table, (4) Click **Add custom conditions**

    ![relative](workspace/edit_data_source.png)

7. Set the Condition to **Priority = Critical**
    1. Set the condition
    2. Click Run
    3. Click Apply

    ![relative](workspace/apply_data_source_filter_condition_Critical.png)

8. Click **Save**

    ![relative](workspace/Click_Save.png)



The business users want to be able to quickly see cases by priority.

1. Click on **Add new element** in top right of screen

    ![relative](workspace/Click_on_Add_new_element.png)


2. Find **Data visualization** in the list and select it

    ![relative](workspace/Click_on_Add_new_element.png)

![](RackMultipart20221028-1-d1lmac_html_f58161d1b5d9aee6.png)

1. Drag and drop the new data component from the bottom of the dashboard to right above the My Work section and size it to expand across the screen
 ![](RackMultipart20221028-1-d1lmac_html_7aa98cf4aed1ec34.png)
2. On the new component, click the ![](RackMultipart20221028-1-d1lmac_html_171eaa728617e887.png) . This will bring up the Configuration window on the right


3. In the configuration side panel, find **Visualization Type** , then select "Vertical bar"
 ![](RackMultipart20221028-1-d1lmac_html_781cd81ae7739227.png)


4. Click on **Header and border** to expand that section, then type "Cases by Priority" in the **Chart Title** field
 ![](RackMultipart20221028-1-d1lmac_html_46186d643ea3f822.png)


5. Under Data sources, click **+ Add data source**. In the window that opens, choose the Telework Case table as the source
 ![](RackMultipart20221028-1-d1lmac_html_7da045a3637fba4c.png)


6. Click **+ Add Custom Condition** and configure the filter like below
 ![](RackMultipart20221028-1-d1lmac_html_3e95e6be255f6478.png)


7. Click Add this source
 ![](RackMultipart20221028-1-d1lmac_html_7eccac64d95d8404.png)


8. In the **Group by** section, (_see screenshot below_)

  1. Click the pencil icon next to "Active"
  2. Click "Active" in the drop-down
  3. Type "priority" in the search
  4. Click the word "Priority"
  5. Click Apply

 ![](RackMultipart20221028-1-d1lmac_html_7fa49a243f63f588.png)

1. Click **Save** hen **Exit Edit Mode** on the top right to see your new dashboard!
 ![](RackMultipart20221028-1-d1lmac_html_c83dbcb19db33f5.png)

**Exercise Recap**

In this exercise, we learned how to create a custom workspace using UI Builder and used the Inline Dashboard Editor to display key performance indicators and organize information in ways that benefit our users.
