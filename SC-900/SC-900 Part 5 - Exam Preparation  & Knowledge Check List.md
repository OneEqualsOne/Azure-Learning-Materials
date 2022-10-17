# Overview
This certification is used as an overview for security, compliance and identity. following this exam we can delve deeper into each of the concepts:
- SC-200 - Security Operations
- SC-300 - Identity and access
- SC-400 - Information and governance

## Skills Measured
- Concepts of security compliance and identity **(5-10%)**
- Capabilities of MS Identity and access management solutions **(25-30%)**
- Capabilities of MS Security solutions **(30-35%)**
- Capabilities of MS compliance solutions **(25-30%)**
You don't need to know how to implement features for the exam, only what they are and what problems they solve. 

## Exam details
The exam is 60 minutes long and between 40-60 questions

# Skills Measured
## Describe the concepts of security, compliance, and identity (10–15%) 
### Describe security and compliance concepts 
• Describe the shared responsibility model 
![Shared responsability model](https://learn.microsoft.com/en-us/training/wwl-sci/describe-security-concepts-methodologies/media/3-shared-responsibility-model.png)
• Define defence in depth 
```
The idea of layers of security, not just secuting the perimeter.
```
• Describe the Zero-Trust model 
```
assume compromise, verify explicitly, least privilege to perform an action
```
• Describe encryption and hashing
`encryption = two way function used to scramble data to be reassemblled by a trusted party`
`Hashing = one way function to standardize data into a single format`
• Describe compliance concepts 
`Data residency = where data can be stored` 
`Data Sovereignty = personal data subject to laws` 
`Data privacy = how data is used / collected` 
### Define identity concepts
• Define identity as the primary security perimeter
`identity ties all points together and access`
• Define authentication 
`verifying the user is who they say they are. This is normally to give access to resources, however this is authorization`
• Define authorization 
`Permission to perform an action on a resource`
• Describe identity providers  
`Creates, maintains, and manages identity information while offering authentication, authorization, and auditing services.`
`SSO / Providers that allow you to use the same cred across apps / orgs`
• Describe Active Directory 
`On-Prem based domain network. It is very different to Azure AD`
• Describe the concept of Federation
`Establishing a trust relationship. Trusts and establishing IdP trusts between orgs / domain boundaries` 
## Describe the capabilities of Microsoft Identity and Access Management Solutions (25–30%) 

### Describe the basic identity services and identity types of Azure AD 
• Describe Azure Active Directory
`Microsoft’s cloud-based identity and access management service`
• Describe Azure AD identities  
`User = Representation of a user` 
`Service principal = identity for an application. Must be registered with AZ AD to enable integration` 
`Managed Identity = Type of SP that automatically managed in AZ AD. No need for devs to manage creds` 
• Describe hybrid identity 
`2 types of managed identity:`
	- `System-Assigned – identity created in AZ AD tied to lifecycle of service instance, when deleted azure auto deletes the identity` 
	- `User-Assigned – identity is managed separately to the service it is assigned to` 
• Describe the different external identity types 
	- `B2B` 
	- `B2C` 

### Describe the authentication capabilities of Azure AD 
• Describe the authentication methods available in Azure AD 
	- `Password based` 
	- `Password less -  FIDO2 sec key or windows hello. Hello for business replaces with 2fa`  
• Describe Multi-factor Authentication 
`Proving you are who you say you are with 2 known artifacts to the system you are authenticating to`
• Describe self-service password reset  
	-   `Password change – user knows pass but wants to change it` 
	-   `Password reset - doesn’t know their password` 
	-   `Account unlock – user cant sign in because its locked` 
• Describe password protection and management capabilities available in Azure AD 
`Global banned password list of known ones` 
`Custom banned password lists – can make own lists of banned passwords` 
`Protect against password spraying and brute force` 
`Hybrid security – on prem receives the global ban list and custom password protect policy's from AZ AD`

### Describe access management capabilities of Azure AD 
• Describe conditional access 
`Security before allowing authenticated users to access data or other assets`
• Describe the benefits of Azure AD roles X  
• Describe the benefits of Azure AD role-based access control X  

### Describe the identity protection & governance capabilities of Azure AD 
• Describe identity governance in Azure AD:
	-   `Govern the identity lifecycle.` 
	-   `Govern access lifecycle.` 
	-   `Secure privileged access for administration.` 
• Describe entitlement management and access reviews 
`Entitlement management is an identity governance feature that enables organizations to manage the identity and access lifecycle at scale` 
• Describe the capabilities of Azure AD Privileged Identity Management (PIM) X  
• Describe Azure AD Identity Protection 
`Identity Protection is a tool that allows organizations to accomplish three key tasks:` 
	-  `Automate the detection and remediation of identity-based risks.` 
	-  `Investigate risks using data in the portal.` 
	-   `Export risk detection data to third-party utilities for further analysis` 

## Describe the capabilities of Microsoft Security solutions (25–30%) 

### Describe basic security capabilities in Azure 
• Describe Azure DDoS protection  
`2 types, advanced allows automatic tuning` 
• Describe Azure Firewall 
  `Fully stateful, cloud-native network firewall security service. It provides threat protection for cloud workloads running in Azure.`
• Describe Web Application Firewall 
`Centralized protection for web applications. WAF on Azure Application Gateway provides protection from common exploits and vulnerabilities`

• Describe Network Segmentation with VNet 
`Segmentation is used to minimize network footprint ensuring restrictions to the wider organisation's network stopping access to items outside of the virtual network without explicit permission to do so.`
• Describe Azure Network Security groups
` filter network traffic between Azure resources in an Azure virtual network. A NSG contains security rules that allow or deny inbound network traffic to, or outbound network traffic from, several types of Azure resources. For each rule, you can specify source and destination, port, and protocol.`
• Describe Azure Bastion and JIT Access 
`Azure Bastion is a service you deploy that lets you connect to a virtual machine using your browser and the Azure portal, or via the native SSH or RDP client already installed on your local computer`
`JIT or Just in Time manages the access to ensure users with correct credentials are authorized to access said resources based on specified conditions`
• Describe ways Azure encrypts data 
	- `Storage service encryption - data at rest auto encrypted`
	- `Azure Disk Encryption - encrypts windows and linux VM disks`
	- `Transparent data encryption - protect SQL databases and Azure Data warehouse against malicious activity`
	- `Azure KeyVault - used to store secrets, keys and certs securely`

## Describe security management capabilities of Azure 
• Describe Cloud security posture management (CSPM) 
`Improves higher level cloud security functions and relations of cloud objects` 
• Describe Microsoft Defender for Cloud 
• Describe the enhanced security features of Microsoft Defender for Cloud 
`Enables the capabilities of the free mode to workloads running in Azure, hybrid, and other cloud platforms. Integrated Microsoft Defender plans, specific to the types of resources in your subscriptions and provide enhanced security features for your workloads.` 
• Describe security baselines for Azure 
`Benchmark provides prescriptive best practices and recommendations to help improve the security of workloads, data, and services on Azure` 
`Baselines applies guidance from the Azure Security Benchmark to the specific service for which it's defined` 

### Describe security capabilities of Microsoft Sentinel 
• Define the concepts of SIEM and SOAR 
`SIEM - Used to ingest data from multiple different sources and correlate them in a centralised point.`
`SOAR - responding to incidents automatically.`
• Describe how Microsoft Sentinel provides integrated threat management 
`collects data, detects, invedtigates and responds to threats`

### Describe threat protection with Microsoft 365 Defender 
• Describe Microsoft 365 Defender services 
`Defender for 365, cloud, endpoint, cloud apps` 
• Describe Microsoft Defender for Identity (formerly Azure ATP) 
`cloud-based security solution that identifies, detects, and helps to investigate advanced threats, compromised identities, and malicious insider actions` 
• Describe Microsoft Defender for Office 365 (formerly Office 365 ATP) 
`protect against malicious threats posed by email messages, links (URLs), and collaboration tools.` 
• Describe Microsoft Defender for Endpoint (formerly Microsoft Defender ATP) 
`Endpoint solution for defender` 
• Describe Microsoft Defender for Cloud Apps 
`Cloud app security solution`
• Describe the Microsoft 365 Defender portal 
`Combines protection, detection, investigation, and response to the following:`
	- `Email`
	- `Collaboration (B2B, B2C)`
	- `Identity`
	- `Devices`
	- `Cloud app threats`

## Describe the capabilities of Microsoft compliance solutions (25–30%) 
### Describe Microsoft’s Service Trust Portal and privacy principles 
• Describe the offerings of the Service Trust portal 
	- `Certifications, Regulations, and Standards`
	- `Reports, Whitepapers, and Artifacts`
	- `Industry and Regional Resources`
	- `Resources for your Organization`
• Describe Microsoft’s privacy principles 
	- `control`
	- `transparency`
	- `security`
	- `strong legal protections`
#### Describe the compliance management capabilities of Microsoft Purview 
• Describe the Microsoft Purview compliance portal 
`brings together all of the tools and data that are needed to help understand and manage an organization’s compliance needs.`
`provides prebuilt assessment, workflow capabilities, step-by-step improvement and scoring.`
• Describe compliance manager 
`feature that helps admins manage compliance requirements`
• Describe the use and benefits of compliance score 
`calculated using scores that are assigned to actions`
`2 types of action:`
	- `Your improved actions: actions that the organization is expected to manage.`
	- `Microsoft actions: actions that Microsoft manages for the organization.`

### Describe information protection and data lifecycle management capabilities of Purview
#### Microsoft Purview 
• Describe data classification capabilities 
`Identifying and classifying sensitive items within the org in 3 ways:`
	- `Manual by users`
	- `Automated pattern based recognition, kind of how sensitive information types work`
	- `Machine Learning`
• Describe the benefits of content and activity explorer
`Content explorer uses the data classification paine to get visibility into content from overview pane`
`Activity explorer shows what content has been discovered and labeled`
• Describe sensitivity labels 
`enable the protection of content without affecting productivity and collaboration.`
• Describe Data Loss Prevention (DLP) 
`a way to protect sensitive information and prevent its inadvertent disclosure`
• Describe Records Management 
`lebaling content, retention policy applied, event based retention, review and validated, proof of deletion, export info about disposed items.`
• Describe Retention Polices and Retention Labels 
`content is kept only for a required time, and then permanently deleted.`
### Describe insider risk capabilities in Microsoft Purview 
• Describe Insider Risk Management 
`there is a broad range of internal risks. Risk management is centered around transparency, intrgration workflows, actions and configs relating to insider risks`
• Describe communication compliance 
` insider risk solution that helps minimize communication risks detecting, capturing, and acting on uncompliant messages`
• Describe information barriers 
`Information barrier policies determine and prevent unauthorized communications`
## Describe resource governance capabilities in Azure 
• Describe Azure Policy 
`Designed to help enforce standards and assess compliance across an organization.`
• Describe Azure Blueprints 
`Declarative way to orchestrate the deployment of various resource templates and other artifacts`
• Describe the capabilities in the Microsoft Purview governance portal
`Create holistic maps of data landscape with automated functions, enable data curators to manage and secure estate, makes searching data more valuable and integral.`