Automating User Creation in Azure Using Microsoft Forms and Power Automate



Introduction

In this project, I automated the creation of Azure Active Directory (Azure AD) users based on responses submitted through a Microsoft Form. By integrating Microsoft Forms with Power Automate, this workflow streamlines employee onboarding, reducing manual effort and improving accuracy.

Key Features

Automated user creation in Azure AD based on form submissions.

Dynamic group assignment using Azure AD membership rules.

Scalability to adapt to various organizational requirements.

Course of Action

Microsoft Forms Setup

I created a form titled "New Employee Onboarding Form" to collect essential employee information. This form includes fields for:

Last Name

Start Date

Email Address

Department

Equipment Requirements



Power Automate Workflow

Using Power Automate, I built a workflow to trigger upon form submission. The workflow retrieves responses and creates users in Azure AD with the following configurations:

Account Status: Disabled by default

Display Name: Concatenation of First and Last Name

Email Configuration: Automatically assigned based on form input

Password: Predefined temporary password



Dynamic Group Configuration

Dynamic groups were created in Azure AD to automatically assign users to specific groups based on their department. For example, a rule for the "Help Desk" group ensures that any user with the department "help desk" is automatically added.

Dynamic Membership Rule Example:

(user.department -eq "help desk")



Verification and Results

Once the workflow ran, users were successfully created and verified in Azure AD. They were automatically assigned to their respective dynamic groups based on their form inputs.



Results

Efficiency: Significantly reduced onboarding time.

Accuracy: Ensured error-free user creation by automating data mapping.

Scalability: Simplified group management with dynamic rules.

Future Enhancements

Implement email notifications for IT and HR teams upon user creation.

Add an approval step to enable accounts after initial creation.

Extend the workflow to assign specific roles based on department.

YAML files for Power Automate configurations.

Dynamic membership rules for Azure AD groups.

Sample onboarding form JSON structure.
