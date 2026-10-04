Auto Ticket Classification using Flow Designer

Project Overview

Auto Ticket Classification using Flow Designer is a ServiceNow System Administrator project designed to automate the categorization of IT support tickets.

The solution examines the Short Description provided in a ticket and automatically determines the suitable Category and Subcategory through ServiceNow Flow Designer.

Problem Statement

School IT helpdesks commonly handle support issues including Wi-Fi connectivity problems, projector issues, forgotten passwords, and slow or unresponsive computers.

Manually checking and categorizing each request takes additional time and may lead to inconsistent ticket classification.

To address this, the project uses ServiceNow Flow Designer to automate the ticket classification process.

Objectives

- Automatically categorize IT tickets at the time of creation.
- Minimize the need for manual ticket classification.
- Improve the efficiency of ticket routing.
- Ensure consistent and standardized ticket details.
- Notify the caller through email after classification.
- Implement the automation using an easy-to-manage no-code approach.

Technologies Used

- ServiceNow
- ServiceNow System Administrator
- Flow Designer
- Custom Tables
- Choice Fields
- Reference Fields
- Dependent Choice Fields
- Email Notification
- Update Sets
- XML

Main Components

Custom Table

A custom table named:

"Incident Workflow"

is used for managing the IT support tickets.

The table includes the following fields:

- Number
- Caller
- Category
- Subcategory
- Short Description
- Description
- State
- Assigned Group
- Assigned to

Category and Subcategory Mapping

Category| Subcategory
Network| Wi-Fi
Hardware| Projector
Access| Forgot Password
Performance| Slow Computer

Flow Designer Automation

The automation flow is called:

"Auto Classify School IT Tickets"

It starts automatically whenever a new record is created in the Incident Workflow table.

Classification Logic

The flow checks the issue or keywords present in the ticket and assigns the corresponding category and subcategory.

Keyword / Issue| Category| Subcategory
WiFi / Network| Network| Wi-Fi
Projector| Hardware| Projector
Password / Login| Access| Forgot Password
Slow / Hanging| Performance| Slow Computer

Once the classification is completed, an email notification is sent to the caller.

Testing

Test Case 1

Input:

""WiFi not working in library""

Expected Result:

- Category → Network
- Subcategory → Wi-Fi
- Email notification → Sent to caller

Test Case 2

Input:

""Projector not turning on""

Expected Result:

- Category → Hardware
- Subcategory → Projector
- Email notification → Sent to caller

ServiceNow Update Set

The complete project configuration is available as:

"Project_Update_Set.xml"

This XML file can be imported into another ServiceNow instance as an Update Set to transfer the project configuration.

Project Purpose

The project showcases how ServiceNow Flow Designer can be utilized to build a no-code automation workflow for classifying IT support tickets and notifying the respective caller.

Future Enhancements

The solution can be further extended with the following capabilities:

- Automatic routing of tickets to appropriate support groups
- SLA monitoring and tracking
- Support for additional ticket categories
- Expansion of keyword-based classification rules
- Predictive Intelligence integration
- Advanced reports and dashboards
