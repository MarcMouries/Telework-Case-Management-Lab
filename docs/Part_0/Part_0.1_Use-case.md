---
layout: default
title: Use-case
parent: Introduction
nav_order: 1
---
## Use-case

Amanda is part of the Office of Regulatory Affairs and her team responsible for managing different cases across the agency. One of their responsibilities is to ensure employees are approved to work remotely and have the necessary I.T. equipment to protect and manage the records and other sensitive information stored on telework devices and transmitted across external networks. Currently, her team has no centralized case management solution for tracking the status of telework cases and tasks across 3 departments (the employee's department, the HR department, and the IT department). Today the team is using:

**PDF / Word Form**
- A PDF form to fill the details about the request

**Emails**
1. Email to send the request in PDF format
2. Email to receive Submissions
3. Communicate task updates

 **Spreadsheet**
1. Spreadsheet to track approvals & tasks across departments
  1. IT for Remote Access request
  2. HR for Safety & Manager
 2. Manage updates to Telework cases

### Challenges

The lack of a single platform to manage their work results in:


| xxx       | yyy                           | 
| ------------- | -------------------------------- | 
| **Wasted Time** <br>wasted staff time coordinating and communicating updates.           | Marc.Mouries@servicernow.com     | 
| 2.0           | Dale.Stubblefield@servicenow.com | 


| --- | --- |
| **Wasted Time** <br> wasted staff time coordinating and communicating updates. |  **Staff Burnout** <br>  Staff Burnout as much of the work focuses on the crisis of the moment instead of planned and leveled workload |
| **Unnecessary Firefighting**  <br>Unnecessary Firefighting by the team to avoid security and safety issues | **Poor Visibility**  <br>Lack of clear status of the work across departments. |

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

[Next: Planning](./Part_0.2_Planning.md){: .btn .btn-green }
