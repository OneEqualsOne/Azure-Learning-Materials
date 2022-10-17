# Azure AD 
-   Describe what Azure AD does. 
-   Describe the identity types that Azure AD supports. 
Azure Active Directory is a cloud based ID and access management service. It enables guests and employees to sign in and access resources both internal (corporate intranet) and external (MS365) resources. Azure AD can be synchronized with existing on-premises Active Directory, synchronized with other directory services, or used as a standalone service. 

## Available Azure AD Editions 
- **Free** - create users / groups, sync with on-prem, self-service password change for cloud users, SSO (Single Sign-On)
- **Office 365 Apps** - self-service password reset, device write back, o365 apps 
**P1** - advanced admin. Synamic groups, self service group management, MSIdM 
**P2** - PAM/PIM, JIT, Advanced monitoring 

## Azure AD Identity Types 
- **User** - Representation of a user 
- **Service principal** - identity for an application. Must be registered with Azure AD to enable integration 
- **Managed Identity** - Type of SP that automatically managed in Azure AD. No need for devs to manage creds 

Types of managed identity: 
-   **System-Assigned** – identity created in Azure AD tied to lifecycle of service instance, when deleted azure auto deletes the identity 
-   **User-Assigned** – identity is managed separately to the service it is assigned to.  

Devices can be in 3 states: 
-   **Azure AD Registered** – provide users with support for BYOD 
-   **Azure AD Joined** – joined through an org account. Devices generally are owned by the org 
-   **Hybrid Azure AD joined** – joined to on-prem and AZ AD using the same org account 

## Types of external ID 
**B2B** - Guest access with another business 
**B2C** - sign in with social, enterprise or local account id's to get SSO to apps (P1&P2 feature) 

## Hybrid Identity's 
- **Pass hash sync** - hash of the hash  
- **Azure AD Pass through** - directly validating password of user againsed the on-prem AD environment, not in cloud
- **Federated auth** - use for advanced features not currently supported in azure AD. SSO for smart cards, Certs, SSO using on-prem MFA and sign on using third party applications 

# AZ AD Authentication mechanisms 
-   Describe the authentication methods of Azure AD. 
-   Describe multi-factor authentication in Azure AD 
-   Describe the password protection and management capabilities of Azure AD 

- **Passwords** - Written information passcodes we remember and use to validate our requests
![Auth password](https://learn.microsoft.com/en-us/training/wwl-sci/explore-authentication-capabilities/media/3-passwords-supplemented-replaced.png)
- **Phone** - SMS based, Vlice call 
- **OAuth - Open Auth, OTP codes generated uses software or hardware to gen codes (***NOTE** DO NOT get confused with **OAuth2**. OAuth2 is Authorization, OAuth is authentication*).
- **Passwordless** - FIDO2 sec key or windows hello. Hello for business replaces with 2fa  
- **FIDO2** - fast id online, open standard for password-less authentication 

## MFA in Azure AD 
MFA in Azure AD requires authentication mechanisms of the following types: 
-   Something you know 
-   Something you have 
-   Something you are 

It does this via the following methods: 
-   Microsoft Authenticator app 
-   Windows Hello for Business 
-   FIDO2 security key 
-   OATH hardware token (preview) 
-   OATH software token 
-   SMS 
-   Voice call 

MFA massivley reduces organisational risk. However, it is not the all end all. Here are some good security practices on top of MFA controls: 
-   Enforcing Azure Active Directory Multi-Factor Authentication registration for all users. 
-   Forcing administrators to use multi-factor authentication. 
-   Requiring all users to complete multi-factor authentication when needed. 

## Self-service password reset (SSPR) 
SSPR works in following scenarios: 
-   **Password change** – user knows pass but wants to change it 
-   **Password reset** - doesn’t know their password 
-   **Account unlock** – user cant sign in because its locked 

To use it users must be:
-   Assigned an Azure AD license 
-   Enabled for SSPR by an admin 
-   Registered with the authentication method/s they want to use 

The following authentication methods are available for SSPR: 
-   Mobile app notification 
-   Mobile app code 
-   Email 
-   Mobile phone 
-   Office phone    
-   Security questions 

## Password protection 
To protect passwords, Microsoft maintains a list of passwords which it will ban from being used as they have been compromised from other security related events across the world. It does this by constantly looking online for data breached passwords, creating a hash of those passwords and comparing the newly created password hash to the hash in its database to determine if it has been compromised in the past. As an Azure AD admin, we can also add our own custom banned wordlists, these can be more specific to our organisation and potential passwords users might use. Azure automatically monitors sign ins to protect against password spraying and brute force . It also can manage hybrid security by sending the globally banned password list and custom one (if applicable) to on prem via the password protect policy's from AZ AD. 

# Describe access management capabilities 
-   Describe Conditional Access in Azure AD. 
-   Describe the benefits of Azure AD roles and role-based access control. 

## Conditional access in Azure AD 
Access is only granted to users based on conditions we can specify. Here are some common signals that conditional access works with: 
-   User or group membership 
-   Named location info 
-   Device 
-   Application  
-   Real-time sign-in risk detection 
-   Cloud apps 
-   User risk  

Based on these signals, and the behaviour of these signals we can perform the following access controls actions: 
-   Block access 
-   Grant access 
-   Require one or more conditions to be met before granting access: 
    -   Require multi-factor authentication. 
    -   Require device to be marked as compliant. 
    -   Require hybrid Azure AD joined device.   
    -   Require approved client app. 
    -   Require app protection policy.
    -   Require password change. 

## Benefits of Azure AD roles and RBAC  
Roles are used to specify what users should be able to access different resources within the organisation, and also prevent users from having more access than they need. Here are some of the basic built-in roles for Azure AD: 
- **Global admin** - Able to do everything in the environment. Microsoft recommends having a max of 5 global admin accounts across the whole organisation. 
- **User admin** – create and manage all user and group aspects 
- **Billing admin** – make purchases, manage subs and support tickets, monitor service health 
- **Custom roles** - Granular permissions for roles 
The idea behind having roles is to grant the access users need but nothing more.  
Categories of Azure AD roles:
- **Azure AD specific** – manage resources in Azure AD only 
- **Service specific roles** – for services 
- **Cross-service roles** – Azure AD span through services  

### Difference between Azure AD RBAC AND Azure RBAC 
- **Azure AD RBAC** – AZ AD roles control access to AZ AD resources such as users, groups, applications 
- **Azure RBAC** – access to AZ Resources such as VM's, or storage using AZ resource management  

# Identity protection and governance in Azure AD 
-   Describe the identity governance capabilities of Azure AD. 
-   Describe Privileged Identity Management (PIM). 
-   Describe the capabilities of Azure AD Identity Protection. 

## Identity governance in AZ AD 
Azure AD allows you to: 
-   Govern the identity lifecycle. 
-   Govern access lifecycle. 
-   Secure privileged access for administration. 

It's intended to help organizations address these four key questions: 
-   Which users should have access to which resources? 
-   What are those users doing with that access? 
-   Are there effective organizational controls for managing access? 
-   Can auditors verify that the controls are working? 

### Identity lifecycle: 
![Id Lifecycle](https://learn.microsoft.com/en-us/training/wwl-sci/describe-identity-protection-governance-capabilities/media/2-identify-lifecycle-management.png)
Azure AD Premium allows for HR systems and Microsoft identity manager to manage identity access and lifecycle of employees and identity's . Essentially if someone leaves it helps enable HR to ensure there identity is managed in a single place and easy to remove / grant access as opposed to being stationed across several locations where if not properly removed, they might have access even after they leave the organisation.

### Access lifecycle :
The access lifecycle is the process of managing access throughout the users organisational life. Users require different levels of access at different points.  
#### Privileged access lifecycle 
When we allow accounts to use privileged access, we need to ensure  we are monitoring when privileged access is needed, accessed, processed and activity around potential misuse or said access. We can use such as PIM to help uplift this principal. 

## Entitlement management and access reviews 
Entitlement management is an identity governance feature that enables organizations to manage the identity and access lifecycle at scale. 

It includes the following features: 
-   **Delegate** the creation of access packages to non-administrators 
-   **Managing external users** - When a user who isn't yet in your directory requests access, and is approved, they're automatically invited into your directory and assigned access 

## Access reviews 
Access reviews are helpful when:
-   You have too many users in privileged roles, such as global administrator. 
-   When automation isn't possible, such as when HR data isn't in Azure AD. 
-   You want to control business critical data access. 
-   Your governance policies require periodic reviews of access permissions. 
Access reviews can be created through Azure AD access reviews, or Azure AD Privileged Identity Management (PIM). 

We can add a terms of use section to help ensure users are using the data appropriately. Here are some example use cases where employees or guests may be required to accept terms of use: 
-   Before they access sensitive data or an application. 
-   On a recurring schedule, so they're reminded of regulations. 
-   Based on user attributes, such as terms applicable to certain roles. 
-   Presenting terms for all users in your organization. 

## PIM - Privileged Identity Management
Privileged identity Management is used to help ensure users are performing privileged actions only at times it is applicable to their role. PIM is: 
-   Just in time, providing privileged access only when needed, and not before. 
-   Time-bound, by assigning start and end dates that indicate when a user can access resources. 
-   Approval-based, requiring specific approval to activate privileges. 
-   Visible, sending notifications when privileged roles are activated. 
-   Auditable, allowing a full access history to be downloaded. 

## Azure Identity Protection 
Azure Identity Protection is a tool that allows organizations to accomplish three key tasks: 
-   Automate the detection and remediation of identity-based risks. 
-   Investigate risks using data in the portal. 
-   Export risk detection data to third-party utilities for further analysis. 
Identity Protection categorizes risk into three tiers: low, medium, and high. It can also calculate the sign-in risk, and user identity risk. 

sign in risks that Identity Protection in Azure AD is able to identify: 
-   Anonymous IP address. 
-   Atypical travel.  
-   Malware linked IP address 
-   Unfamiliar sign-in properties.  
-   Password spray.  
-   Azure AD threat intelligence. 

user risks that Identity Protection in Azure AD is able to identify: 
-   Leaked creds 
-   Azure AD Threat intel