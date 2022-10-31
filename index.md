![](RackMultipart20221028-1-d1lmac_html_a032cad86d0e8a1.png)

# Creator Workflows Lab Guide

## Telework Case Management

| Date | August 29, 2022 |
| --- | --- |
| Author | Marc.Mouries@servicernow.com / Dale.Stubblefield@servicenow.com/
[Rafael.Yew@servicenow.com](mailto:Rafael.Yew@servicenow.com) /
[Kristy.Merriam@servicenow.com](mailto:Kristy.Merriam@servicenow.com) |
| Version | 3.0 |
| Applies to | ServiceNow Tokyo Release - App Engine Studio v22.0.3 |

# Table of Contents

_**[Introduction 3](#_Toc95730439)**_

**[Goals 3](#_Toc95730440)**

**[Use-case 3](#_Toc95730441)**

[Challenges 3](#_Toc95730442)

[Planning 4](#_Toc95730443)

_**[Takeoff Checklist 🚀 5](#_Toc95730444)**_

_**[Exercise 1: Build the Foundation 8](#_Toc95730445)**_

**[Section 1 – Create the application 8](#_Toc95730446)**

**[Section 2 – Creating the Data 11](#_Toc95730447)**

**[Section 3 – Import Legacy Data 20](#_Toc95730448)**

_**[Exercise 2: Create the User Experience 25](#_Toc95730449)**_

**[Section 1 – Create a Workspace Experience 25](#_Toc95730450)**

[Bulk Assignment 28](#_Toc95730451)

[Finding Answers with the Analytics Center 29](#_Toc95730452)

**[Section 2 – Configure the Workspace 30](#_Toc95730453)**

**[Section 2 – Create the Request Form 33](#_Toc95730454)**

**[Purpose 33](#_Toc95730455)**

_**[Exercise3–Automate the work 48](#_Toc95730456)**_

**[Section1–BuildinganAutomation Flow 48](#_Toc95730457)**

**[Section 2– Testing a Flow 56](#_Toc95730458)**

_**[Conclusion 59](#_Toc95730459)**_

[Supplemental Resources 59](#_Toc95730460)

_**[APPENDIX 60](#_Toc95730461)**_

[Lab Features 60](#_Toc95730462)

[Org Chart of users in Personal Developer Instances 61](#_Toc95730463)

# Introduction

## Goals

Digital transformation is more relevant than ever. Powered by the Now Platform, App Engine fuels rapid delivery of Creator Workflows with great experiences for everyone. With more people building with less complexity, App Engine lets you create low-code apps fast, and safely scale cross-enterprise experiences that users love.

Our goals for this workshop are to allow you to:

1. Gain valuable experience through practice with Creator Workflow Builder essentials
2. Convert a real-world use case with process bottlenecks to a streamline, cross enterprise workflow
3. Take back to your organization the knowledge of how you can make your world of work better.

## Use-case

Amanda is part of the Office of Regulatory Affairs and her team responsible for managing different cases across the agency. One of their responsibilities is to ensure employees are approved to work remotely and have the necessary I.T. equipment to protect and manage the records and other sensitive information stored on telework devices and transmitted across external networks. Currently, her team has no centralized case management solution for tracking the status of telework cases and tasks across 3 departments (the employee's department, the HR department, and the IT department). Today the team is using:

| **Emails** | **Spreadsheet** |
| --- | --- |
|
1. Receive Submissions
2. Track approvals & tasks across departments
  1. IT for Remote Access request
  2. HR for Safety & Manager
3. Communicate task updates
 |
- Manage updates to Telework cases
 |
| **PDF / Word Form**
- Telework request form
 |
|
 |

### Challenges

The lack of a single platform to manage their work results in:

| **Wasted Time** wasted staff time coordinating and communicating updates. |
 | **Staff Burnout** Staff Burnout as much of the work focuses on the crisis of the moment instead of planned and leveled workload |
| --- | --- | --- |
| **Unnecessary Firefighting** Unnecessary Firefighting by the team to avoid security and safety issues |
 | **Poor Visibility** Lack of clear status of the work across departments. |

Amanda and her team have reached out to the IT department for help, but they have no availability to take on new projects. However, they gave Amanda access as a Citizen Developer to the organization's ServiceNow development instance.

Today your mission, and you have accepted it, is to play the role of Amanda and create a solution to efficiently manage cross-departmental work.

Let's make her world of work better…

### Planning

Along with the ServiceNow instance URL and credentials, the I.T department sent you an email to start your Citizen Developer Journey on ServiceNow App Engine.

![Shape1](RackMultipart20221028-1-d1lmac_html_9635ab4c0a180660.gif)

💡 **Prework to start your Citizen Developer Journey on ServiceNow**

**Prework**

1. Make a list of the data you need to track. Ex: Category of work
2. Reach for help on the channel @transformNow
3. If you're using a spreadsheet today, make a copy and keep only the data required. See the Don'ts section
4. Use the record producer to create a form quickly and reuse any relevant questions set
5. If case workers need to create and see tasks related to the case, add the related list ( "Task-\>Parent") to a form ([see documentation](https://docs.servicenow.com/bundle/sandiego-platform-administration/page/administer/form-administration/concept/configure-form-layout.html))
6. **Read the** [**No-Code Citizen Developer Guide for the Now Platform**](https://developer.servicenow.com/dev.do#!/guides/rome/now-platform/citizen-dev-guide/cd-planning)

**Don'ts**

1. Don't create and import the following data. ServiceNow will take care of that for you
  1. Approvals tracking data such as approval status and dates
  2. Dates related to the case. Ex "submission date"

Nicole made a list of the key data that the team is tracking and is eager to start

# Takeoff Checklist 🚀

Let's make sure you have everything you need to get started.

☑ You have the following files

☑ File 1: App Engine Lab - Telework v30.pdf (This lab guide to follow on your own)

☑ File 2: telework App Logo.png

☑ File 3: Telework Cases.xlsx

☑ File 4: Telework Data.xlsx

☑ File 5: Telework icon.png

☑ ![](RackMultipart20221028-1-d1lmac_html_ce92986e4935f92b.png)A ServiceNow POV instance URL and credentials.

# Exercise 1: Build the Foundation

**purpose**

In this exercise, we will learn how to create the core data elements of our application.

**getting started**

1. If the  **Getting Started** dialog opens, close it by clicking the \_Get Started\_ button.

![](RackMultipart20221028-1-d1lmac_html_6d6f46a7ab4e2bb6.png)

1. This reveals the homepage of App Engine Studio. From this page:

- you can create new applications or extend previously developed applications.
- There are a variety of templates provided out of the box that contain examples of configurations that address common business challenges.
- Feel free to return here later to review some of the capabilities enabled with these templates.

## Section 1 – Create the application

1. Click the \_Create app button

![](RackMultipart20221028-1-d1lmac_html_3dbf61a4c97af290.png)

1. Configure the app

  1. _Name_: **[your initials]****Telework Request**

_Note: Your initials will prevent you from using the same app name as another lab attendee._

  1. _Description_: **Manage Telework requests across departments**

1. _ **Optional** _ – Add an image to the application. Images can be a great way to personalize and provide character for your application.

  1. Click the Drag app logo or browse to upload tile.
  2. Browse to and select the  **telework App Logo.png** file you downloaded.

1. The screen should look like below

![](RackMultipart20221028-1-d1lmac_html_711d284dcd16e550.png)

1. Click the \_Continue button
2. The screen should look like below
 ![](RackMultipart20221028-1-d1lmac_html_1ae20ac566ffad8c.png)
3. Click the \_Continue button
4. The app will be created. Once it is finished, click the \_Go to app dashboard button

![](RackMultipart20221028-1-d1lmac_html_b0ef3b03ab3cbda.png)

**Review the guidance**

In this section of the exercise, you will review and turn off Guidance.

1. Read the _Add data_ flyout.

![](RackMultipart20221028-1-d1lmac_html_c054f4c5dc5b4863.png)

1. In the _Guidance_ pane, click the  **Experience**  tab and read the _Add experience_ flyout.

![](RackMultipart20221028-1-d1lmac_html_fbf0526240e0eaa0.png)

1. Select each of the tabs in the _Guidance_ pane to review the different application components.
2. Click the  **Guidance**  toggle to turn off the _Guidance_ pane.

![](RackMultipart20221028-1-d1lmac_html_53d91cc28b0e47fa.png)

1. Optional: Look in the top right corner for the "Enter full screen" button. Click it to maximize your viewing area.

 ![](RackMultipart20221028-1-d1lmac_html_52b59d05c9b91ce7.png)

## Section 2 – Creating the Data

We will create the core tables for our application. To create a table in App Engine Studio:

1. Click the  **Add**  icon (⨁ Add) for _Data_ on the _App Home_ tab.

![](RackMultipart20221028-1-d1lmac_html_a8c68acd5d28b638.png)

1. On the _How do you want to add data to your app?_ screen, select the **Create a table** tile.
 ![](RackMultipart20221028-1-d1lmac_html_829981879f222cfa.png)
2. Click the Get started button.
3. On the _How do you want to create a table?_ screen, select the  **Upload a spreadsheet**  tile.
4. Click the \_Continue button

![](RackMultipart20221028-1-d1lmac_html_7b497aa45c4ae83d.png)

1. On the _Let's choose the spreadsheet you want to upload_ screen, click the  **Drag and drop or browse to upload spreadsheet**  link

![](RackMultipart20221028-1-d1lmac_html_de939b34a16d5ba0.png)

1. Browse and select the  **Telework Data.xlsx**  file you downloaded

![](RackMultipart20221028-1-d1lmac_html_5df00921005dc0c4.png)

1. Click \_Continue\_

1. Our spreadsheet has multiple sheets. **We only need the first one**"Telework Arrangement".
2. Select ☑ **Import spreadsheet data** in the "Telework Arrangement" box.
3. Click on **Convert to table** to the right of the Telework Arrangement Sheet name.

![](RackMultipart20221028-1-d1lmac_html_80cdc3a4a15485d6.png)

1. Click the  **Expand/Collapse**  icon (⌄) to see advanced configuration options.
2. Check _ **Display** _: To use this field as the display value for the table when used as a reference field

![](RackMultipart20221028-1-d1lmac_html_24d17a296112ecad.png)

1. Click \_Continue\_
2. Set the table label to **Arrangement**.The table name will auto populate.

![](RackMultipart20221028-1-d1lmac_html_c9a1870c6f219756.png)

1. Click \_Continue\_
2. Click the "All" checkbox for the "admin" role.
3. Click the "Read" checkbox for the "user" role.

![](RackMultipart20221028-1-d1lmac_html_9f4713c15c814d25.png)

1. Click \_Continue\_
2. A loading screen will appear while the table is being created. When it completes, click \_Done\_
3. We haven't converted all the sheets in the spreadsheets, so we'll see this message pop up

![](RackMultipart20221028-1-d1lmac_html_37ed133783f17dd6.png)

1. Click \_Yes, leave\_
2. Again, click the  **Add**  icon (⨁ Add) for _Data_ on the _App Home_ tab.

![](RackMultipart20221028-1-d1lmac_html_85ba8501cec36f39.png)

1. On the _How do you want to add data to your app?_ screen, select the **Create a table** tile.
 ![](RackMultipart20221028-1-d1lmac_html_829981879f222cfa.png)
2. Click the Begin button.
3. On the _How do you want to create a table?_ screen, Select _ **Create from an existing table** _.

![](RackMultipart20221028-1-d1lmac_html_adebc1af9ec55c46.png)

1. Click the \_Continue button

1. Type **Task,** then select the table **Task [task]** and Click \_Continue\_

![](RackMultipart20221028-1-d1lmac_html_b9af041d53d01ee6.png)

1. Give the table the following properties

  1. **Table label** : Telework Case
  2. Select ☑ Auto number
  3. Enter in prefix as TLW.

![](RackMultipart20221028-1-d1lmac_html_5751f3694a2e5162.png)

1. Click \_Continue\_
2. Click the "All" checkbox for the "admin" role.
3. Click the "Create", "Read", and "Write" checkboxes for the "user" role.

![](RackMultipart20221028-1-d1lmac_html_7d2f37b80443b7bf.png)

1. Click \_Continue\_
2. Once the table is ready, we'lladdourdatacolumnstothisnewtablebyclicking **Edit**** table**.

![](RackMultipart20221028-1-d1lmac_html_2667c66792115dff.png)

1. We now see the Table Builder screen. From this screen, we can see the fields that were automatically added to our table by the system, as well as add additional columns.

![](RackMultipart20221028-1-d1lmac_html_89b2babe9f590d98.png)

1. Review the introduction to Table Builder then **click** the **Next** button to walk through each information pane. From the last screen, **click** the **Get Started** button.
2. Now let's add the data columns for our application. Start by **clicking** the **Add new field** link at the top of the screen

![](RackMultipart20221028-1-d1lmac_html_e46aaa0edeb6c225.png)

1. In the new row created, add the following values:

  1. Label: **Arrangement**
  2. Hit the [ENTER] key
  3. Column name: arrangement (auto-generated)
  4. Hit the arrow key ▸ [twice]
  5. Hit the [ENTER] key
  6. Type: **Reference** then select Arrangement

1. Again, **click** the **Add new field** link at the top of the screen
2. In the new row created, add the following values:

  1. Label: " **Number of Days**"
  2. Hit the [ENTER] key
  3. Column name: (auto-generated)
  4. Type: **Integer**

1. Again, **click** the **Add new field** link at the top of the screen
2. In the new row created, add the following values:

  1. Label: **Reason**
  2. Hit the [ENTER] key
  3. Column name: reason (auto-generated)
  4. Hit the arrow key ▸ [twice]
  5. Hit the [ENTER] key
  6. Type: **Choice**
  7. Choice Type: Dropdown with -- None –
  8. Choices:
    1. Emergency
    2. Occasional
    3. Medical
    4. Reasonable Accommodation
    5. COVID

1. Click \_Done\_
2. We now have all the data elements we need to manage our use case.
3. Click the \_Save\_ button at the top right to finalize your configurations.
4. Congratulations, you've built the first tables in your solution.

**Let's take a look at the form that has been generated for our table and adjust the layout.**

1. At the top-center of the table, click **Form views**

![](RackMultipart20221028-1-d1lmac_html_a00fc6291231fe4f.png)

As we created our table by extending the Task table, we inherited some fields we don't need for our use case.

1. Remove the following fields (by clicking the X)

 ![](RackMultipart20221028-1-d1lmac_html_fd9e6d0375905ef0.png)

    1. Number
    2. Configuration Item,
    3. Active,
    4. Description

Let's add the fields we need

1. The Fields tab to the left is where existing fields can be added. Notice how there are 63 fields available to use

![](RackMultipart20221028-1-d1lmac_html_65731ef6c85e9ef6.png)

1. Type "Opened by" in the Search box
2. Drag it onto the form
 ![](RackMultipart20221028-1-d1lmac_html_aa45badcb4df43b9.png)

 ![](RackMultipart20221028-1-d1lmac_html_98bab37d0603d053.png)


3. Click on "Formatters"
 ![](RackMultipart20221028-1-d1lmac_html_e6c123abe7ddd15e.png)


4. Drag the "**Activities (filtered)**" field onto the form below the Short description field.

![](RackMultipart20221028-1-d1lmac_html_5ac3f7d630bdfa8.png)

1. Move the 2 fields " **Arrangement"** and " **Number of Days**" to the main section of the form.

Your form should look like this:

![](RackMultipart20221028-1-d1lmac_html_4d7634fd3aa66107.png)

1. On the top right, click \_Save\_ to save the form.

![](RackMultipart20221028-1-d1lmac_html_4dcce73d662eb3e0.png)

1. Click the **Table** button on the top banner.

![](RackMultipart20221028-1-d1lmac_html_55e86488f314fa5f.png)

1. Click the **Preview** button on the top right.

![](RackMultipart20221028-1-d1lmac_html_eee056e195d417c8.png)

You'll notice that there's no data

![](RackMultipart20221028-1-d1lmac_html_d18a5f98a5733521.png)

Let's fix that….

## Section 3 – Import Legacy Data

1. Hover the column header **Number** , **right-click** to display the table menu options and then select **Import.**

![](RackMultipart20221028-1-d1lmac_html_f0072d5979854ef5.png)

1. Select **Choose File** to upload the Excel file: Telework Cases.xlsx

![](RackMultipart20221028-1-d1lmac_html_4a8ec72f7a78b80d.png)

1. Click \_Upload and wait until the import is complete.

![](RackMultipart20221028-1-d1lmac_html_a64fae6a6f51b957.png)

1. Once loaded, click on **Preview Imported Data**

![](RackMultipart20221028-1-d1lmac_html_4583dd9fad3aa1e6.png)

1. Scroll down and click on the **Complete Import** button
 ![](RackMultipart20221028-1-d1lmac_html_7831047deb4d7cee.png)

1. You'll now see that we have migrated our data.

![](RackMultipart20221028-1-d1lmac_html_96c5b9d9100e45ba.png)

1. Let's update the columns in this list layout.
2. Right click at the top of the Number column and click on "Configure" -\> "List Layout"

![](RackMultipart20221028-1-d1lmac_html_b7a8266e068a80ac.png)

1. Move "Task type" to the left hand window and click Save

 ![](RackMultipart20221028-1-d1lmac_html_484ea2f2832e483d.png)

Next, let's start working and managing our records

1. Hover the column header **Priority** , **right-click** to display the menu and then select **Pie Chart**

![](RackMultipart20221028-1-d1lmac_html_d01b914ab4265f31.png)

1. And voila, we get a Pie chart that shows us the distribution of cases by Priority

![](RackMultipart20221028-1-d1lmac_html_23725093697e690d.png)

1. Explore the other tools in the Context Menu such as Visual Task Board

1. The team struggles managing and understand the status of related tasks. Let's fix that.


2. Click the back button on the Pie Chart report to get back to the list
 ![](RackMultipart20221028-1-d1lmac_html_c472453da4310651.png)
3. Open a record by clicking the number field

![](RackMultipart20221028-1-d1lmac_html_244058beaddd9a63.png)

1. Right-click on header

  1. Select **Configure**
  2. Then select **Related Lists**

![](RackMultipart20221028-1-d1lmac_html_1d45a2f3a9a1d904.png)

1. In the new form:

  1. Select the item " **Task -\> Parent**"
  2. Click on the button to move the item to the selected list

  1. Click \_Save\_

![](RackMultipart20221028-1-d1lmac_html_e0c88ad53ab5c6d4.png)

Now a new tab at the bottom of the form will show records that have relationships to the current record.

![](RackMultipart20221028-1-d1lmac_html_26bae987b8392a99.png)

1. Go back to the list view by clicking on the back button at the top

![](RackMultipart20221028-1-d1lmac_html_b065bf9b0230b92b.png)

1. We can even start creating new records/cases


2. Click \_New\_ in the top right
 ![](RackMultipart20221028-1-d1lmac_html_d49e90b5aa7de824.png)

1. Fill out the form and click "Submit" to create a test record.
2. Close the Table Builder and Preview tab by **clicking** the **X** on them.
 ![](RackMultipart20221028-1-d1lmac_html_d16112e35dae392d.png)
3. Next, we'll work on configuring the user experience.

**Exercise Recap**

In this exercise, we learned how to create a new application and map out the data elements important to enable our business process.

We learned to use the Table Builder to add and configure columns including Reference fields and Choice lists.

We were able to complete all these tasks using simple point-and-click administration and without requiring specialized application or database knowledge.

# Exercise 2: Create the User Experience

**purpose**

In this exercise, we will learn how to create user experiences for interacting with our application. We will leverage App Engine Studio to create a new Workspace experience designed to allow the team to track and manage cases across the enterprise.

## Section 1 – Create a Workspace Experience

![](RackMultipart20221028-1-d1lmac_html_7528b4d3b454d89e.png)Wewill now createandconfigurethecoreWorkspaceexperienceforournewapplication.

1. On the application homepage, locate the **Experience** section and click the ⨁ Add icon.

![](RackMultipart20221028-1-d1lmac_html_5eb57f8f138baffd.png)This takes us to a selection where we can identify the type of experience we wish to create.

1. **Click** the **Workspace** option to create a workspace to help users manage and fulfill requests sent to them

1. Thislaunchestheworkspacecreator.Click \_ **Get Started** \_

![](RackMultipart20221028-1-d1lmac_html_b504e7bb92037dc7.png)

1. Next, provide the following information:
  1. **Name:** leave the default value
  2. **Description:** (optional)
  3. **URL:** leave the default value
  4. **Roles:** leave the default values

 ![](RackMultipart20221028-1-d1lmac_html_3959046e513d09df.png)

1. Click \_Continue\_
2. Next, we'll select the data tables we want to work on in this experience.
3. Remove any unnecessary table, by clicking on the X at the end of the table name.

![](RackMultipart20221028-1-d1lmac_html_fb547513e39e2dcd.png)

1. Set the **primary** and secondary tables to: **Telework**** Case **and** Arrangement** like below:

![](RackMultipart20221028-1-d1lmac_html_644b54f6d3786047.png)

1. Click \_Continue\_

1. YournewWorkspaceexperienceiscompleted.
Click \_Done\_toreturntotheAppHomepage

 ![](RackMultipart20221028-1-d1lmac_html_2ce12abd632f0d72.png)

2. From the App Home page, **click** the **Preview** link byyournewlycreatedExperience

![](RackMultipart20221028-1-d1lmac_html_2d224281353adff9.png)

1. We now have a fully functioning workspace to get work done.


2. Click on **Critical Tasks**

![](RackMultipart20221028-1-d1lmac_html_549cfd50dcfeabb.png)

1. Select all rows, Click **Edit** , Select **Assign to me** , Click **Back**
 ![](RackMultipart20221028-1-d1lmac_html_c2467e611454dc21.png)


2. You now have 2 tasks assigned to you.
 ![](RackMultipart20221028-1-d1lmac_html_88fdc6365093eb55.png)

1. In the **My Work** list, click on the Refresh icon to see the new tasks
 ![](RackMultipart20221028-1-d1lmac_html_e7a6390ffc47fce.png)

1. **Great!** Let's handle an emergency ⚠️.

 Our team member _Luke Wilson_ is out sick today. We need to reassign his work to another case worker. (_It is hard to do when the work is managed via emails and spreadsheets!_)

### Bulk Assignment

1. Click the List icon. ![](RackMultipart20221028-1-d1lmac_html_6c132fbd461c859e.png)


2. Click on **Open** in the Telework Case section
 ![](RackMultipart20221028-1-d1lmac_html_539b7d7c1e7fe1b1.png)


3. Click the button next to "Luke Wilson" and click "Show Matching"
 ![](RackMultipart20221028-1-d1lmac_html_1a596fd6344994b0.png)


4. Select all rows, then click **Edit**
 ![](RackMultipart20221028-1-d1lmac_html_23f3824dcc4c7d47.png)


5. Type "Andrew Och" in the "Assigned to" field, then click his name in the drop down
 ![](RackMultipart20221028-1-d1lmac_html_c2e95b91ee1c336.png)
6. Click Update
7. You should see this message:
 ![](RackMultipart20221028-1-d1lmac_html_ee4ec083a9f40f80.png)

### Finding Answers with the Analytics Center

1. Now let's check the Analytics Center to quickly find the data we need
2. Click the Analytics Center button
 ![](RackMultipart20221028-1-d1lmac_html_5a43ff5c1897c89a.png)

1. Let's ask some question about our data
2. ![Shape2](RackMultipart20221028-1-d1lmac_html_ff39988a991b3b0.gif)Note: As you type in a query, Analytics Q&A suggests recent searches, indicators, tables, and columns that match what you have typed so far. Only the tables and columns to which you have access are shownClick In the box "What do you want to see?" then type the following query:

 "show me all the telework cases grouped by reason as a bar chart"

 ![](RackMultipart20221028-1-d1lmac_html_d9a3306233b83d22.png)


3. Click the button Ask

1. And here is the answer

![](RackMultipart20221028-1-d1lmac_html_1f906e4639fa203f.png)

1. In the query box remove the part "show me all the". It should read as:
 "telework cases grouped by reason as bar chart"
2. Click the Ask button, and we'll get the same result
3. Try with "as pie chart"
4. Try with "as list". (You can ask for a list first, ex: "list of telework cases grouped by reason"
5. It even understands our own data; Try with "open COVID telework case"

**Exercise Recap**

In this exercise, we learned how to generate a new Workspace and explored the out-of-the-box capabilities.

## Section 2 – Configure the Workspace

Let's use the Analytics Center to configurea new Dashboardforourneeds.

1. In Analytics Center, click on **Dashboards** , then choose the dashboard created for your workspace

![](RackMultipart20221028-1-d1lmac_html_e72ba77dd34e74f8.png)

1. Once the dashboard opens, click Edit in the top right of the screen

![](RackMultipart20221028-1-d1lmac_html_8d2b9e4941d7e381.png)

Screen should look similar to below

![](RackMultipart20221028-1-d1lmac_html_ddb02fdce6af3b84.png)

1. Click on **Add new element** in top right of screen
 ![](RackMultipart20221028-1-d1lmac_html_dbf37376499b10de.png)


2. Find **Data visualization** in the list and select it

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

## Section 2 – Create the Request Form

## Purpose

ServiceNow offers multiple ways to create a user experience for submitting a form. In this exercise, we will learn one quick way to get users off paper forms and emails.

1. Close the "Now Experience – Telework Request" App Engine Studio tab
 ![](RackMultipart20221028-1-d1lmac_html_6f3fe518bfb2eae2.png)


2. On the application homepage, locate the Experience section and click the ⨁ Add icon.
 ![](RackMultipart20221028-1-d1lmac_html_7528b4d3b454d89e.png)

This takes us to a selection where we can identify the type of experience we wish to create.

1. **Select** the **Record Producer** option.

![](RackMultipart20221028-1-d1lmac_html_9536c6184b57a2ad.png)

1. Thislaunchestherecord producer creator.
2. Click \_Get Started\_

1. ![Shape3](RackMultipart20221028-1-d1lmac_html_e0e6bd50915a4eb8.gif) **Note** : A record producer is a specific type of catalog item that allows end users to create task-based records from the service catalogNext, provide the following information: (💡 double-click, copy & paste into the form)

| **Name** | Apply for Telework |
| --- | --- |
| **Short Description** | Use this form to apply for Telework |

1. Click \_Continue\_

1. Click \_Edit record producer\_

1. Click on **Destination**** , **then type "** Tel" **, and select the** Telework Case** table

![](RackMultipart20221028-1-d1lmac_html_e846e2c003348f3.png)

1. Click on **Location**** , **then under** Catalogs **,** click **on** Browse ****.**
 ![](RackMultipart20221028-1-d1lmac_html_2179b09e5fb85e70.png)
2. Click on **Service Catalog** , then click on the right arrow to move the item over to the Selected list

1. At the bottom, **click** on \_Save selections\_

1. Under **Categories** , **click** on **Browse****.**
2. Move "Can We Help You?" to the right-hand side and click Save selections

Your screen should look like below

![](RackMultipart20221028-1-d1lmac_html_9d7f868bcbe00d53.png)

Let's add questions:

Unlike in a paper-based form, we don't need to ask users to fill personal information like first name, last name, …, or date of request. That information will be automatically attached to the case. This makes filling forms so much faster.

We want to allow users to open a case on behalf of another individual, so let's start by asking users " **Who is this request for?**" and " **When do you need this?"**

1. **Click** on Questions
2. **Click the arrow next to** Insert new questionthen click "Question set"
 ![](RackMultipart20221028-1-d1lmac_html_ec16fe2cba49f65f.png)


3. Select "Standard Employee Questions" and click Submit
 ![](RackMultipart20221028-1-d1lmac_html_b7d5d77b4ba92e.png)

One key information we need users to provide is the type of arrangement they are applying for.

1. Click Insert new question


2. For Question type, select **Choice**
3. For **Question subtype** , select **Record reference**

![](RackMultipart20221028-1-d1lmac_html_9172c76ae5a3366c.png)

1. Scroll down to the **Details** section

1. In the **Details** section, enter the following information: (💡 double-click, copy & paste into the form)

 (_see screenshot below_)

|

  1. **Map to a specific field**
 | We want to store that information so let's check the box |
| --- | --- |
|

  1. **Table field**
 | choose **Arrangement** |
|

  1. **Question label**
 | What type of Telework arrangement are you applying for? |
|

  1. **Mandatory**
 | Check the box |
|

  1. _Notice the **Question Preview** that shows what the question will look like to the user._
 |
|
 |

![](RackMultipart20221028-1-d1lmac_html_88a82a55060dcc11.png)

1. Click on Continue to Additional details→


2. In the **Additional details** section, we'll use the data we imported earlier as options for this question.

 Enter the following information:

|

  1. **Source Table**
 | Select **Arrangement** |
| --- | --- |
|

  1. Click on the **Annotation** tab
 |

![](RackMultipart20221028-1-d1lmac_html_bca9359bea849c12.png)

Today, the team is spending a lot of time correcting and manually re-routing applications due to people confusing the different types of Telework arrangement. Let's fix that.

1. We'll use the  **Annotation**  tab to provide users with additional instructions for the question.

  1. Check the box **Show**** instructions**

  1. Open the file: telework\_form\_annotation.docx

  1. Copy all the text in the file ( ⌘ Cmd  or CTRL+A, CTRL+C )
  2. Paste it into the Annotation section of the Telework Form (⌘ Cmd  or CTRL+V )

  1. **Click** on \_ Insert Question \_

![](RackMultipart20221028-1-d1lmac_html_67dde9ff5eb0d1a0.png)

1. Back to the main form, **click** on \_ Insert new question \_

![](RackMultipart20221028-1-d1lmac_html_b630a890638b7b3d.png)

When users select the arrangement type **Situational** , we'll prompt them for the number of days per week. So, let's go ahead and in the **Type** section

  1. For **Question type** , select **Text**
  2. For **Question subtype** , select **Single line**

![](RackMultipart20221028-1-d1lmac_html_ed8893fb58e3ed69.png)

1. Scroll down to the **Details** section

1. In the **Details** section, enter the following information: (💡 double-click, copy & paste into the form)

|

  1. **Map to a specific field**
 | Check the box |
| --- | --- |
|

  1. **Table field**
 | choose **Number of Days per Week?** |
|

  1. **Question label**
 | Number of Days per Week? |
|

  1. Click on **Additional details**
 |

![](RackMultipart20221028-1-d1lmac_html_52467679362ef826.png)

1. In the **Additional details** section,

  1. For the **Text validation** field, select **Number**
  2. **Click** on \_Insert Question\_

1. Back to the **Questions** page, we're going to define dynamic behavior of this question based on the answer to the previous questions

  1. Click on the **Define behavior** icon
  2. Click on the **Define new behavior** icon

![](RackMultipart20221028-1-d1lmac_html_a2f05b5266c777e.png)

1. In the **Additional details** section, we'll use the data we imported earlier as options for this question. Enter the following information:

  1. **Make the question mandatory = Yes**
  2. **Make the question visible = True**
  3. Click on the **Conditions** tab

![](RackMultipart20221028-1-d1lmac_html_eb8172c5528d09b9.png)

1. In the **Conditions** tab,

  1. Set the filter to arrangement is SituationalTelework
  2. **Click** on \_Add behavior\_

![](RackMultipart20221028-1-d1lmac_html_e5654c8536bb155d.png)

1. Back to the questions page,

  1. **Click** on \_ Save \_
  2. Click on   Preview

![](RackMultipart20221028-1-d1lmac_html_e66bf3acee8ede38.png)

1. The **Preview** page allows to visualize what our form will look like in different experiences. You can interact with the item but not submit it.

| **Mobile** | **Portal** |
| --- | --- |
| ![](RackMultipart20221028-1-d1lmac_html_bf02ef9477373d58.png) | ![](RackMultipart20221028-1-d1lmac_html_6dae315ae67eafa8.png) |
|
 |
 |

2. _If you want to preview your catalog item in the Virtual Agent you will need to activate the plugins_ _ **Glide Virtual Agent** _ _(com.glide.cs.chatbot) and_ _ **Service Management Virtual Agent Topic Blocks** _ _(com.glideapp.cs.sm\_topic\_blocks)._
  1.
  2. _Additional setup beyond that is required to get NLU to perform a topic conversation via the Virtual Agent._
  3.
  4. _Feel free to experiment this after completing the entire lab._
**Close** the Preview by clicking on the X on the top right


 ![Shape4](RackMultipart20221028-1-d1lmac_html_f2f8752b0fd53e2f.gif)

![](RackMultipart20221028-1-d1lmac_html_5650e1c528c06ab5.png)

Let's publish the form

  1. **Click** on **Review and Submit**
  2. **Click** on \_ Submit \_

![](RackMultipart20221028-1-d1lmac_html_c11c7a6578bef371.png)

Congratulations. The form is published on your development instance.

![](RackMultipart20221028-1-d1lmac_html_98cecb29c3d93b2.png)

**Let's see how users can easily find it on the Service Portal**

1. Navigate to https://\<instance\>.service-now.com/sp to view the Service Portal
2. Search for "Telework"

![](RackMultipart20221028-1-d1lmac_html_6d7a857afff3f0c9.png)

1. The catalog item is found.
2. Click on the item to apply for Telework

![](RackMultipart20221028-1-d1lmac_html_9df445249f8a3921.png)

1. In the **Details** section, enter the following information: (💡 double-click, copy & paste into the form)

|

  1. Who is this request for?
 | **David Loo** |
| --- | --- |
|

  1. When do you need this?
 | **Next week** |
|

  1. What type of arrangement?
 | **Situational** |
|

  1. Number of days per week
 | **3** |
|

  1. Click \_Submit\_
 |

![](RackMultipart20221028-1-d1lmac_html_9133453ef171c673.png)

**Exercise Recap**

In this exercise, we learned how Use App Engine Studio (AES) to easily create customized Catalog Items that users can access in Service Portal and on mobile devices.

Our next exercise will focus on taking the building blocks created to this point and making them actionable to drive automation and process optimization

# Exercise3–Automate the work

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

# Conclusion

In this lab, we built, implemented, and tested an application using the fundamental part of an application: Data, User Experience, and Automation.

The team managing the work will be more efficient and the users will get what they need faster.

Of course, the examples in these exercises are just the beginning when it comes to the power of leveraging Automation Engine.

The possibilities are limited only by your imagination as a Creator. If you can dream it, you can workflow it on the Now Platform.

Here are some resources to help you continue your journey on the ServiceNow platform

### Supplemental Resources

In addition to this Lab Guide and the resources discussed in the live workshop, the following resources are always available to help with this, or any other ServiceNow activities.

- Get a free Personal Development instance and more free training on:
  - [https://developer.servicenow.com/](https://developer.servicenow.com/)
- Online community forums
  - [https://community.servicenow.com/](https://community.servicenow.com/)
- Online training and certification (Many additional free trainings, some are for a fee)
  - [https://nowlearning.service-now.com/](https://nowlearning.service-now.com/)
- Customer Success Center
  - [https://www.servicenow.com/success.html](https://www.servicenow.com/success.html)

# APPENDIX

### Lab Features

Summary of features we went through in this lab.

1. The sample data spreadsheet contains users that exist in Personal Developer Instances
  1. The _open by_ is set to users who have a manager.
  2. The _assigned to_ is set to users who
2. Create App
3. Create Data Model
  1. Table created from a spreadsheet
  2. Table extending Task with reference to another table
  3. Change the layout of the form
  4. Add and remove fields
  5. Add related task
4. Create Case Worker Experience
  1. Create Workspace
  2. Bulk Task assignment
  3. Use the Analytics Center to ask question about the data
  4. Use of Impersonation for testing purposes
  5. Configure Workspace with UI Builder
5. Create the User Experience
  1. Expose a form to users via the Service Portal
6. Automate the work
  1. Create a Flow
    1. Create Tasks for several departments
    2. Send an email
  2. Test the flow
    1. Use impersonation
    2. Check for approval
    3. Check for email sent

### Org Chart of users in Personal Developer Instances

Use this chart to select different users for testing purposes.

![Shape5](RackMultipart20221028-1-d1lmac_html_8559be6d2908e863.gif)