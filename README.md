# 🎫 Auto Ticket Classification using Flow Designer

> A ServiceNow System Administrator project that automates the classification of school IT support tickets using Flow Designer.

---

## 📌 Project Overview

Auto Ticket Classification using Flow Designer is a ServiceNow automation project developed to automatically classify IT support tickets.

The system analyzes the **Short Description** of a newly created ticket and assigns the appropriate **Category** and **Subcategory** using ServiceNow Flow Designer.

The project also sends an email notification to the caller after the classification process is completed.

---

## 🎯 Objectives

The main objectives of this project are to:

- ⚡ Automatically classify IT tickets when they are created.
- ⏱️ Reduce the effort required for manual ticket classification.
- 🔄 Improve the efficiency of ticket routing.
- 📋 Maintain standardized ticket information.
- 📧 Send email notifications to the caller.
- 🛠️ Provide an easy-to-maintain no-code automation solution.

---

## ❗ Problem Statement

School IT helpdesks receive different types of support requests, such as:

- Wi-Fi connectivity problems
- Projector failures
- Password and login issues
- Slow or hanging computers

Manually reviewing and categorizing each ticket requires additional effort and may result in inconsistent classification.

This project addresses the problem by using ServiceNow Flow Designer to automatically identify and classify tickets based on keywords in their descriptions.

---

## 🧰 Technologies Used

| Technology / Feature | Purpose |
|---|---|
| ServiceNow | IT service management platform |
| Flow Designer | Ticket classification automation |
| Custom Tables | Stores project ticket records |
| Choice Fields | Provides predefined selections |
| Reference Fields | Maintains reference-based information |
| Dependent Choice Fields | Connects Category and Subcategory |
| Email Notification | Notifies the caller |
| Update Sets | Transfers project configuration |
| XML | Stores the exported Update Set |

---

## 🗂️ Main Components

### 1. Custom Table

The project uses a custom table named:

**`Incident Workflow`**

The table contains the following fields:

| Field |
|---|
| Number |
| Caller |
| Category |
| Subcategory |
| Short Description |
| Description |
| State |
| Assigned Group |
| Assigned to |

---

### 2. Category & Subcategory Mapping

The ticket classification is based on the following mapping:

| Category | Subcategory |
|---|---|
| Network | Wi-Fi |
| Hardware | Projector |
| Access | Forgot Password |
| Performance | Slow Computer |

---

## ⚙️ Flow Designer Automation

### Flow Name

**`Auto Classify School IT Tickets`**

The flow is configured to run whenever a new **Incident Workflow** record is created.

### 🔍 Classification Logic

The flow analyzes the ticket information and identifies the appropriate classification based on the issue or keyword.

| Keyword / Issue | Category | Subcategory |
|---|---|---|
| WiFi / Network | Network | Wi-Fi |
| Projector | Hardware | Projector |
| Password / Login | Access | Forgot Password |
| Slow / Hanging | Performance | Slow Computer |

### 🔔 Notification

After the ticket has been classified:

```text
Ticket → Classification → Email Notification → Caller
```

An email notification is sent to the caller after the classification process.

---

## 🧪 Testing

### Test Case 01 — Wi-Fi Issue

**Input**

```text
WiFi not working in library
```

**Expected Result**

| Field | Expected Value |
|---|---|
| Category | Network |
| Subcategory | Wi-Fi |
| Email Notification | Sent to caller |

---

### Test Case 02 — Projector Issue

**Input**

```text
Projector not turning on
```

**Expected Result**

| Field | Expected Value |
|---|---|
| Category | Hardware |
| Subcategory | Projector |
| Email Notification | Sent to caller |

---

## 📦 ServiceNow Update Set

The project configuration has been exported as:

**`Project_Update_Set.xml`**

The XML file can be imported into another ServiceNow instance as an Update Set.

This allows the project configuration to be transferred and reused in another instance.

---

## 📁 Repository Structure

```text
Auto-Ticket-Classification-using-Flow-Designer/
│
├── README.md
│
├── ServiceNow/
│   └── Project_Update_Set.xml
```

---

## 💡 Project Purpose

This project demonstrates how ServiceNow Flow Designer can be used to create a no-code automation solution for:

- IT ticket classification
- Category and subcategory assignment
- Ticket notification

The solution helps reduce manual classification work while maintaining consistent ticket information.

---

## 🚀 Future Enhancements

The project can be extended with additional capabilities such as:

- 👥 Automatic assignment to support groups
- ⏰ SLA tracking
- 🗃️ Additional ticket categories
- 🔎 More keyword-based classification rules
- 🤖 Predictive Intelligence
- 📊 Advanced reporting and dashboards

---

## 📌 Project Summary

| Item | Details |
|---|---|
| Platform | ServiceNow |
| Project Type | System Administrator |
| Automation Tool | Flow Designer |
| Custom Table | Incident Workflow |
| Flow Name | Auto Classify School IT Tickets |
| Classification | Category & Subcategory |
| Notification | Email to Caller |
| Deployment File | Project_Update_Set.xml |
