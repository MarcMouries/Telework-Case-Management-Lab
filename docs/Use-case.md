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