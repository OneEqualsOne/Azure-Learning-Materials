# Service trust portal
-   Describe the offerings of the Service Trust Portal.
-   Describe Microsoft’s privacy principles.
-   Describe Microsoft Priva.

## Service trust portal categories
The Service Trust Portal landing page includes content that is organized into the following categories:
-   Certifications, Regulations, and Standards
-   Reports, Whitepapers, and Artefacts
-   Industry and Regional Resources
-   Resources for your Organization

## Microsoft privacy principals
- control
- transparency
- security
- strong legal protections
- **no content based targeting** - not using email, chat files or personal to target advertising
- benefits:
	- troubleshooting
	- feature improvement 
	- personalized experience

## Microsoft Priva
Priva helps you meet the challenges of:
-   **Helping** employees adopt sound data handling practices and training them to spot and fix issues
-   **Understanding** the potential risks in the amount and type of personal data they store and share
-   **Fulfilling** data subject requests, or subject rights requests, efficiently and on-time

Priva evaluates your organization's data stored in the following Microsoft 365 services within your Microsoft 365 tenant:
-   Exchange Online
-   SharePoint Online
-   OneDrive for Business
-   Microsoft Teams

it also can help you:
-   **Detect** overexposed personal data so that users can secure it.
-   **Spot** and limit transfers of personal data across departments or regional borders.
-   **Help** users identify and reduce the amount of unused personal data that you store.

# Compliance management in Purview
-   Describe the Microsoft Purview compliance portal.
-   Describe Compliance Manager.
-   Describe the use and benefits of compliance score.

## Purview portal
The Microsoft Purview compliance portal brings together all of the tools and data that are needed to help understand and manage an organization’s compliance needs. The compliance portal is available to customers with a Microsoft 365 SKU with one of the following roles:
-   Global administrator
-   Compliance administrator
-   Compliance data administrator

The default compliance portal home page contains several cards including:
-   The **Compliance Manager** card
    [![The compliance score card](https://learn.microsoft.com/en-us/training/wwl-sci/describe-compliance-management-capabilities-microsoft-365/media/3-compliance-scorecard-inline.png)](https://learn.microsoft.com/en-us/training/wwl-sci/describe-compliance-management-capabilities-microsoft-365/media/3-compliance-scorecard-expanded.png#lightbox)
-   The **Solution catalogue** card, links to collections of integrated solutions to help you manage end-to-end compliance scenarios. Solutions areas included:
    -   **Information protection & governance**
    -   **Privacy**
    -   **Insider risk management**
    -   **Discovery & respond**
-   The **Active alerts** card includes a summary of the most active alerts and a link where admins can view more detailed information, such as alert severity, status, category, and more.

## Compliance Manager
Purview compliance manager is a feature that helps admins manage compliance requirements 
Compliance Manager helps simplify compliance and reduce risk by providing:
-   Prebuilt assessments based on common regional and industry regulations and standards. 
-   Workflow capabilities that enable admins to efficiently complete risk assessments for the organization.
-   Step-by-step improvement actions that admins can take to help meet regulations and standards relevant to the organization.
-   Compliance score, which is a calculation that helps an organization understand its overall compliance posture by measuring how it's progressing with improvement actions.

### Controls
Compliance Manager tracks the following types of controls:
-   **Microsoft-managed controls** - controls for Microsoft cloud services, which Microsoft is responsible for implementing.
-   **Your controls** - sometimes referred to as customer-managed controls, these are implemented and managed by the organization.
-   **Shared controls** - responsibility for implementing these controls is shared by the organization and Microsoft.
Compliance manager is also used to assess, template and give improvement actions for said controls.

## Benefits of compliance scoring
Admins can get a breakdown of the compliance score in the Compliance Manager overview pane.

### How to understand the compliance score
The overall compliance score is calculated using scores that are assigned to actions. Actions come in two types:
-   **Your improved actions** - actions that the organization is expected to manage.
-   **Microsoft actions** - actions that Microsoft manages for the organization.

Actions are categorized as mandatory, discretionary, preventative, detective, or corrective:
-   **Mandatory** – these actions shouldn’t be bypassed. For example, creating a policy to set requirements for password length or expiration.
-   **Discretionary** - these actions depend on the users understanding and adhering to a policy. For example, a policy where users are required to ensure their devices are locked before they leave them.
The following are subcategories of actions that can be classified as mandatory or discretionary:
- Preventative
- Detective
- Corrective

### What is the difference between Compliance Manager and compliance score?
- **Compliance Manager** is an end-to-end solution in the Microsoft Purview compliance portal to enable admins to manage and track compliance activities.
**Compliance score** is a calculation of the overall compliance posture across the organization. The compliance score is available through Compliance Manager.

# information protection and data lifecycle management
-   Describe data classification capabilities.
-   Describe data loss prevention.
-   Describe records management.

## Know your data, protect your data, and govern your data
Microsoft Purview Information Protection discovers, classifies, and protects sensitive and business-critical content throughout its lifecycle across your organization.
-   **Know your data**: Organizations can understand their data landscape and identify important data across on-premises, cloud, and hybrid environments. 
-   **Protect your data**: Organizations can apply flexible protection actions including encryption, access restrictions, and visual markings.
-   **Prevent data loss**: Organizations can detect risky behaviour and prevent accidental oversharing of sensitive information. 
-   **Govern your data**: Organizations can automatically keep, delete, and store data and records in a compliant manner.

## data classification capabilities
Identifying and classifying sensitive items that are under your organization's control is the first step in the Information Protection discipline. Microsoft Purview provides three ways of identifying items so that they can be classified:
-   manually by users
-   automated pattern recognition, like sensitive information types
-   machine learning

### Sensitive information types
Examples include:
-   Credit card numbers
-   Passport or identification numbers
-   Bank account numbers
-   Health service numbers
Also supported is exact data match (EDM) classification. EDM-based classification enables you to create custom sensitive information types.

### Trainable classifiers
Trainable classifiers use artificial intelligence and machine learning to intelligently classify your data.
-   **Pre-trained classifiers** - pretrained classifiers 
-   **Custom trainable classifiers** - Create and train custom classifiers.

### Understand and explore the data
-   The number of items classified as sensitive information and which classifications they are.
-   Details on the locations of data based on sensitivity.
-   Summary of actions that users are taking on sensitive content across the organization.

### Content explorer
This is a tab in data classification Paine that helps get visibility into content from overview pane 

### Activity explorer
The activity explorer shows what content has been discovered and labelled. Here are a few of the activity types that can be analysed:
-   File copied to removable media
-   File copied to network share
-   Label applied
-   Label changed

Admins can use more than 30 filters for data including:
-   Location
-   User
-   Sensitivity label
-   Retention label

## Sensitivity labels and policies
enable the labelling and protection of content, without affecting productivity and collaboration
Labels are:
-   Customizable
-   Clear text
-   Persistent

Sensitivity labels can be configured to:
-   **Encrypt** email only or both email and documents.
-   **Mark the content** when Office apps are used
-   **Apply the label automatically** The label can be applied automatically or configured to prompt users to apply the recommended label.
-   Protect content in containers such as sites and groups
-   Extend sensitivity labels to third-party apps and services
-   Classify content without using any protection settings

### Label policies
After sensitivity labels are created, they need to be published to make them available to people and services in the organization. 
-   **Choose the users and groups that can see labels**. Labels can be published to specific users, distribution groups, Microsoft 365 groups in Azure Active Directory, and more.
-   **Apply a default label** to all new emails and documents that the specified users and groups create.
-   **Require justifications for label changes**. If a user wants to remove a label or replace it, admins can require the user to provide a valid justification to complete the action. 
-   **Require users to apply a label (mandatory labeling)**. It ensures a label is applied before users can save their documents, send emails, or create new sites or groups.
-   **Link users to custom help pages**. It helps users to understand what the different labels mean and how they should be used.

## DLP
Microsoft Purview Data Loss Prevention (DLP) is a way to protect sensitive information and prevent its inadvertent disclosure. With DLP policies, admins can:
-   **Identify, monitor, and automatically protect** sensitive information across Microsoft 365, including:
    -   OneDrive for Business
    -   SharePoint Online
    -   Microsoft Teams
    -   Exchange Online
-   **Help users learn how compliance works** without interrupting their workflow
-   **View DLP reports** showing content that matches the organization's DLP policies

DLP policies protect content through the enforcement of rules that consist of:
-   **Conditions** that the content must match before the rule is enforced.
-   **Actions** that the admin wants the rule to take automatically when content that matches the conditions has been found.
-   **Locations** where the policy will be applied, such as Exchange, SharePoint, OneDrive, and more.

DLP policies can help:
-   Identify any document containing a credit card number stored in users’ OneDrive for Business accounts.
-   Automatically block an email containing employee personal information from being sent outside the organization.

### Endpoint DLP
Endpoint DLP extends the activity monitoring and protection capabilities of DLP to sensitive items that are physically stored on Windows 10, Windows 11, and macOS (Catalina 10.15 and higher) devices
 
Endpoint DLP enables admins to audit and manage activities that users complete on sensitive content. Listed below are a few examples:
-   Creating an item
-   Renaming an item
-   Copying items to removable media
-   Copying items to network shares
-   Printing documents
-   Accessing items using unallocated apps and browsers

## Retention policies and retention labels
retention policies are used to help organizations to manage and govern information by ensuring content is kept only for a required time, and then permanently deleted.
-   **Comply proactively with industry regulations and internal policies** that require content to be kept for a minimum time.
-   **Reduce risk when there's litigation or a security breach** by permanently deleting old content that the organization is no longer required to keep.
-   **Ensure users work only with content that's current and relevant to them**. When content has retention settings assigned to it, that content remains in its original location. 

Retention settings work with the following different workloads:
-   [SharePoint and OneDrive](https://learn.microsoft.com/en-us/microsoft-365/compliance/retention-policies-sharepoint?view=o365-worldwide)
-   [Microsoft Teams](https://learn.microsoft.com/en-us/microsoft-365/compliance/retention-policies-teams?view=o365-worldwide)
-   [Yammer](https://learn.microsoft.com/en-us/microsoft-365/compliance/retention-policies-yammer?view=o365-worldwide)
-   [Exchange](https://learn.microsoft.com/en-us/microsoft-365/compliance/retention-policies-exchange?view=o365-worldwide)

**Retention policies**
-   Retention policies are used to assign the same retention settings to content at a site level or mailbox level.
-   A single policy can be applied to multiple locations, or to specific locations or users.
-   Items inherit the retention settings from their container specified in the retention policy. If a policy is configured to keep content, and an item is then moved outside that container, a copy of the item is kept in the workload's secured location. However, the retention settings don't travel with the content in its new location.

**Retention labels**
-   Retention labels are used to assign retention settings at an item level, such as a folder, document, or email.
-   An email or document can have only a single retention label assigned to it at a time.
-   Retention settings from retention labels travel with the content if it’s moved to a different location within your Microsoft 365 tenant.
-   Admins can enable users in the organization to apply a retention label manually.
-   A retention label can be applied automatically if it matches defined conditions.
-   A default label can be applied for SharePoint documents.
-   Retention labels support disposition review to review the content before it's permanently deleted.

## Records management 
 Microsoft Purview Records Management includes many features, including:
-   Labelling content as a record.
-   Establishing retention and deletion policies within the record label.
-   Triggering event-based retention.
-   Reviewing and validating disposition.
-   Proof of records deletion.
-   Exporting information about disposed items.

When content is labelled as a record, the following happens:
-   Restrictions are put in place to block certain activities.
-   Activities are logged.
-   Proof of disposition is kept at the end of the retention period.

### Common use cases for records management
-   manually apply retention and deletion actions for documents and emails.
-   Automatically applying retention and deletion actions to documents and emails.
-   set default retain and delete actions for all content in a SharePoint library, folder, or document set.
-   automatically apply retain and delete actions to emails by using Outlook rules.

# Insider risk in purview
-   Describe insider risk management.
-   Describe communication compliance.
-   Describe information barriers.

## insider risk management
there is a broad range of internal risks from employees:
-   Leaks of sensitive data and data spillage
-   Confidentiality violations
-   Intellectual property (IP) theft
-   Fraud
-   Insider trading
-   Regulatory compliance violations

Insider risk management is centred around the following principles:
-   **Transparency** - Balance user privacy versus organization risk with privacy-by-design architecture.
-   **Configurability** - Configurable policies based on industry, geographical, and business groups.
-   **Integration** - Integrated workflow across Microsoft Purview solutions.
-   **Actionable** - Provides insights to enable user notifications, data investigations, and user investigations.

### workflow
-   **Policies** - Insider risk management policies are created using predefined templates and policy conditions that define what risk indicators are examined in Microsoft 365 feature areas. 
-   **Alerts** - Alerts are automatically generated by risk indicators that match policy conditions and are displayed in the **Alerts dashboard**. 
-   **Triage** - New activities that need investigation automatically generate alerts that are assigned a _Needs review_ status. Reviewers in the organization can quickly identify these alerts and scroll through each to evaluate and triage
-   **Investigate** - Cases are created for alerts that require deeper review and investigation of the details and circumstances around the policy match. 
-   **Action** - After cases are investigated, reviewers can quickly act to resolve the case or collaborate with other risk stakeholders in the organization.
    -   Actions can be as simple as sending a notification when employees accidentally or inadvertently violate policy conditions.
    -   In more serious cases, reviewers may need to share the insider risk management case information with other reviewers in the organization. Escalating a case for investigation makes it possible to transfer data and management of the case to eDiscovery (Premium) in Microsoft Purview.

# Communication compliance
Communication compliance in Microsoft Purview uses the following workflow:
![[Pasted image 20221017142926.png]]
-   **Configure** – config compliance policies.
-   **Investigate** –tools include alerts, issue management to help remediation, document reviews, reviewing user history, and filters.
-   **Remediate** –resolving an alert, tagging a message, notifying the user, escalating to another reviewer, marking an alert as a false positive, removing a message in Teams, and escalating for investigation.
-   **Monitor** – Monitor using Communication compliance dashboard widgets, export logs, and events recorded in the unified audit logs can be used to continually evaluate and improve your compliance posture.

Some important compliance areas where communication compliance policies can assist with reviewing messages include:
-   **Corporate policies** - With communication compliance, admins can scan user communications across the organization for potential concerns of offensive language or harassment.
-   **Risk management** - Communication compliance can help admins scan for unauthorized communication about projects that are considered to be confidential, such as acquisitions, earnings disclosures, and more.
-   **Regulatory compliance** - Most organizations are expected to follow some regulatory compliance standards during their day-to-day operations. For example, a regulation might require organizations to review communications of its brokers to safeguard against potential insider trading, money laundering, or bribery. 

Examples of how information barriers can be applied:
-   **Education**: Students in one school can't look up contact details for students of other schools.
-   **Legal**: Maintaining confidentiality of data obtained by the lawyer of one client from being accessed by a lawyer for the same firm representing a different client.
-   **Professional services**: A group of people in a company is only able to chat with a client or specific customer via federation or guest access during a customer engagement.

### Information barriers in Microsoft Teams
In Microsoft Teams, information barrier policies determine and prevent the following kinds of unauthorized communications:
-   Searching for a user
-   Adding a member to a team
-   Starting a chat session with someone
-   Starting a group chat
-   Inviting someone to join a meeting
-   Sharing a screen
-   Placing a call
-   Sharing a file with another user
-   Access to file through sharing link

# eDiscovery (disco) and audit in purview
-   Describe the eDiscovery solutions in Microsoft Purview.
-   Describe the auditing solutions in Microsoft Purview.

## eDiscovery solutions in Microsoft Purview
![[Pasted image 20221017142904.png]]
-   **Content Search**. Use the Content search tool to search for content across Microsoft 365 data sources and then export the search results to a local computer.
-   **eDiscovery (Standard)**.  The eDiscovery (Standard) solution also lets you associate searches and exports with a case and lets you place an eDiscovery hold on content locations relevant to the case.
-   **eDiscovery (Premium)**.  provides an end-to-end workflow to identify, preserve, collect, review, analyse, and export content that's responsive to your organization's internal and external investigations. It lets legal teams manage custodians, people that you've identified as people of interest in the case, and the workflow to communicate with custodians. It allows you to collect and copy data into review sets, where you can filter, search, and tag content so you can identify and focus on content that's most relevant. The eDiscovery (Premium) solution provides analytics and machine learning-based predictive coding models to further narrow the scope of your investigation to the most relevant content.

# Audit solutions in Microsoft Purview
![[Pasted image 20221017142852.png]]
-   **Audit (Standard)** log and search for audited activities and power your forensic, IT, compliance, and legal investigations. Turned on by default for all organizations with the appropriate subscription. You can search for a wide-range of audited activities that occur in most of the Microsoft 365 services in your organization. Audit records can also be retrieved using the Office 365 Management Activity API.
-   **Audit (Premium)**. provides audit log retention policies and longer retention of audit records. It provides audit records for high-value crucial events that can help your organization investigate possible security or compliance breaches and determine the scope of compromise. Audit (Premium) also provides organizations with more bandwidth to access auditing logs through the Office 365 Management Activity API.

# Resource governance 
-   Describe Azure Policy.
-   Describe Azure Blueprints.
-   Describe the capabilities in the Microsoft Purview governance portal.
## Azure Policy
designed to help enforce standards and assess compliance across your organization.
Azure Policy evaluates all resources in Azure and Arc enabled resources (specific resource types hosted outside of Azure).

### Evaluation outcomes
Azure Policy evaluates resources at specific times during the resource lifecycle and the policy assignment lifecycle, and for regular ongoing compliance evaluation. The following events or times will trigger an evaluation:
-   A resource has been created, deleted, or updated in scope with a policy assignment.
-   A policy or an initiative is newly assigned to a scope.
-   A policy or an initiative that's been assigned to a scope is updated.
-   The standard compliance evaluation cycle (happens once every 24 hours).

Organizations will vary in how they respond to non-compliant resources. Here's some examples:
-   Deny a change to a resource.
-   Log changes to a resource.
-   Alter a resource before or after a change.
-   Deploy related compliant resources.

### What’s the difference between Azure Policy and Azure role-based access control (RBAC)?
Policy enforces standards and assesses compliance, RBAC assigns access based on user actions, scopes and definitions. not sure why this is a comparison in ms docs ngl...

## Azure Blueprints
Azure Blueprints are a declarative way to orchestrate the deployment of various resource templates and other artefacts such as:
-   Role Assignments
-   Policy Assignments
-   Azure Resource Manager templates (ARM templates)
-   Resource Groups
Essentially, they are used by architects to design and build new resources and templates, its a way to have a subscription template to start from as an example. It also helps with the fore-mentioned aspects of Azure artefact orchestration 

## Capabilities in the Microsoft Purview governance portal
The Microsoft Purview governance portal allows you to:
-   Create a holistic, up-to-date map of your data landscape with automated data discovery, sensitive data classification, and end-to-end data lineage.
-   Enable data curators to manage and secure your data estate.
-   Empower data consumers to find valuable, trustworthy data.
![[Pasted image 20221017142820.png]]

### Data map
 By scanning registered data sources, Azure Purview Data Map is able to capture metadata about enterprise data, to identify and classify sensitive data. Microsoft Purview supports Azure data sources and various data source categories including databases, file storage, and applications and services from third parties.

### Data Catalog
With the Microsoft Purview Data Catalog, business and technical users can quickly and easily find relevant data using a search experience with filters based on various lenses like glossary terms, classifications, sensitivity labels and more.

### Data Estate Insights
With the Microsoft Purview Data Estate Insights, data officers and security officers can get a bird’s eye view and at a glance understand what data is actively scanned, where sensitive data is, and how it moves.

### Data Sharing and Data Policy (preview)
Microsoft Purview Data Sharing enables organizations to securely share data both within your organization or cross organizations with business partners and customers.
