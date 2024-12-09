# Automating User Creation in Azure Using Microsoft Forms and Power Automate




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

<img width="600" alt="Screenshot 2024-12-09 at 4 33 39 PM" src="https://github.com/user-attachments/assets/128b2652-214e-48db-a17e-ae48202874a5">

### 2. Power Automate Workflow

A Power Automate flow processes the form responses and creates users in Azure AD. Key steps include:

1. Trigger the workflow when a new form response is submitted.
2. Retrieve form details and map them to Azure AD fields.
3. Create a new user in Azure AD with default configurations (e.g., disabled account, predefined password).

<img width="600" alt="Screenshot 2024-12-09 at 4 37 21 PM" src="https://github.com/user-attachments/assets/1225c6af-46a8-4fca-a481-e04f1ddc1e6a">


### 3. Dynamic Group Configuration

Dynamic Azure AD groups ensure users are automatically assigned to appropriate groups based on their department.

**Example Membership Rule:**


