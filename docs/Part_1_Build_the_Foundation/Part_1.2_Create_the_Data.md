---
layout: default
title: Create the Data
parent: Part 1. Build the Foundation
nav_order: 2
---

# Create the Data

We will create the core tables for our application. To create a table in App Engine Studio:

1. Click the  **Add**  icon (⨁ Add) for _Data_ on the _App Home_ tab.

![relative](images/data_add_icon.png)


2. On the _How do you want to add data to your app?_ screen, select the **Create a table** tile.
 ![](RackMultipart20221028-1-d1lmac_html_829981879f222cfa.png)

![relative](images/data_create_table_tile.png)

3. Click the Get started button.

4. On the _How do you want to create a table?_ screen, select the  **Upload a spreadsheet**  tile.

![relative](images/data_upload_a_spreadsheet.png)

4. Click the \_Continue button


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

[Next: Import Legacy Data](./Part_1.3_Import_Data.md){: .btn .btn-green-sn }

