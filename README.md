Automating User Creation in Azure Using Microsoft Forms and Power Automate



Introduction

In this project, I automated the creation of Azure Active Directory (Azure AD) users based on responses submitted through a Microsoft Form. The integration was achieved using Power Automate to process the form responses and dynamically create users in Azure AD, streamlining the onboarding process for new employees.

Key Features

Automated user creation based on form inputs.

Dynamic group assignment using Azure AD.

Scalability and accuracy for onboarding workflows.

Implementation Overview

Architecture



The architecture consists of:

Microsoft Forms: To collect employee onboarding information.

Power Automate: To trigger workflows and process data.

Azure AD: For user management and dynamic group assignments.

Workflow Details

Microsoft Form Setup:

A form titled "New Employee Onboarding Form" was created to capture essential employee details like last name, start date, email, department, and equipment requirements.



Power Automate Workflow:

Triggered upon form submission, the workflow retrieves the form responses and creates a user in Azure AD.



Key Configurations:

- Trigger: "When a new response is submitted"
  Details:
    FormID: "New Employee Onboarding Form"
- Action: "Create user in Azure AD"
  Details:
    AccountEnabled: false
    DisplayName: "John Doe"
    MailNickname: "John"
    Password: "$pring1234!"
    UserPrincipalName: "john.doe@example.com"

Dynamic Group Configuration in Azure AD:

Created dynamic security groups with membership rules based on user attributes (e.g., department).



Rule Syntax:

(user.department -eq "help desk")

Verification:

Users were verified in Azure AD for successful creation and proper group assignments.



Results

Efficiency: Reduced manual effort and onboarding time.

Accuracy: Eliminated errors by automating data mapping.

Scalability: Dynamic groups ensure users are automatically assigned based on predefined criteria.

Future Enhancements

Notifications: Add email notifications for IT and HR teams upon user creation.

Approvals: Introduce approval workflows before enabling accounts.

Role Assignments: Automate role assignment based on form inputs.

Repository Content

This repository contains:

Workflow screenshots and architecture diagrams.

YAML files for Power Automate configurations.

Dynamic membership rules for Azure AD groups.

Sample onboarding form JSON structure.
