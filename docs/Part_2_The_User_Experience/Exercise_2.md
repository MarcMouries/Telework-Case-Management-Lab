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