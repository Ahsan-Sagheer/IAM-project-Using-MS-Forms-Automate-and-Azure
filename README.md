# Automating User Creation in Azure Using Microsoft Forms and Power Automate

![Automating User Creation](./path_to_overview_screenshot)

## Introduction

This project demonstrates an automated solution for creating Azure Active Directory (Azure AD) users based on form submissions. By integrating Microsoft Forms with Power Automate, the onboarding process becomes efficient, accurate, and scalable.

---

## Key Features

- **Automated User Creation**: Automatically creates Azure AD users based on form responses.
- **Dynamic Group Assignments**: Users are added to relevant Azure AD groups via dynamic rules.
- **Error Reduction**: Eliminates manual data entry errors.
- **Scalable Workflow**: Easily adaptable for organizational needs.

---

## Workflow Overview

### 1. Microsoft Forms Setup

A **"New Employee Onboarding Form"** was created to collect essential employee details, including:

- **Last Name**
- **Start Date**
- **Email Address**
- **Department**
- **Equipment Needs**

![Microsoft Form Screenshot](./path_to_form_screenshot)

### 2. Power Automate Workflow

A Power Automate flow processes the form responses and creates users in Azure AD. Key steps include:

1. Trigger the workflow when a new form response is submitted.
2. Retrieve form details and map them to Azure AD fields.
3. Create a new user in Azure AD with default configurations (e.g., disabled account, predefined password).

![Power Automate Workflow Screenshot](./path_to_workflow_screenshot)

### 3. Dynamic Group Configuration

Dynamic Azure AD groups ensure users are automatically assigned to appropriate groups based on their department.

**Example Membership Rule:**


