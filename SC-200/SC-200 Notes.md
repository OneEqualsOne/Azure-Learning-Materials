# 365 Defender 
covers:
- iot
- office 365
- entra id protection
- cloud apps
- endpoints
- identity
- insider risk
## DLP
DLP consists of:
- Sensitivity labels - classification of document 
- Sensitive information types - looking for keywords or checksums to identity potentially harmful information such as Passport, ID or PCI-DSS 

Investigate incidents in Purview under Data Loss Prevention
## defender products:
- **Microsoft Defender for Office 365**
- **Microsoft Defender for Endpoint** 
- **Microsoft 365 Defender**
- **Microsoft Defender for Cloud Apps** 
- **Microsoft Defender for Identity** 
- **Microsoft Defender Vulnerability Management** 

The **More resources** option in the portal provides a list of these related portals:
- Purview
- AzAD
- AAD ID Protection
- AZ Information Protection
- MS Defender for cloud

## Auto investigation
- **Alerts** 
- **Devices**
- **Evidence**
- **Entities** 
- **Log** 
- **Pending actions** 
The Action Center brings investigations and other components together to be acted on. 
## Remediation for Defender for Office 365
terminology:
- actionable insights = correlated signals for a security incident, and actions that can be deployed
### safe attachments
Under the **Action for unknown malware** in Attachments:
    - **Off**  Attachments won't be scanned
    - **Monitor**  Continues delivering the message after malware is detected
    - **Block**  Blocks the current and future emails and attachments with detected malware.
    - **Replace** Blocks malware but delivers message body.
    - **Dynamic delivery** delivers the message body without attachments and reattaches attachments after scanning
## Safe links
protects your users from malicious URLs
Safe Links is available in the following apps:
- Microsoft 365 apps for enterprise
- Office for the web
- Word, Excel, PowerPoint, and Visio on Windows, as well as Office apps on mobile
- Microsoft Teams channels and chats
## Other
- Defender for Office 365 also has anti phishing policies. 
- You can also simulate attacks

# Defender for endpoint
use for:
- Threat and vulnerability management 
- Attack surface reduction
- Advanced protection (ML + deep learning)
- Endpoint detection and response 
- auto investigate alerts and remediate complex threats using AI

info:
- default data retention period is 6 months
- manage portal system settings to configure storage settings
## Deploying DfE
1. Go to ([https://security.microsoft.com](https://security.microsoft.com/))
2. Select **Settings**.
3. Select **Endpoints**.

### Device discovery
- 365 defender portal
- settings
- Discovery setup
- standard
- run

## RBAC setup:
1. Access 365 Defender portal with Security administrator or Global administrator role
2. **Settings** > **Endpoints**. Under the **Permissions** category, select **Roles**.
3. Select the **Turn on roles** button.
4. Select **+ Add item**.
5. Enter the role name, description, and permissions
6. Select **Next** to assign the role to an Azure AD Security group
7. Use filter to select the Azure AD group that you would like to add this role to.
8. Select **Save**.

## Device groups
1.  **Settings** > **Endpoints** and then under **Permissions** select **Device groups**.
2. Select **+ Add device group**.
3. Enter the group name and automation settings, specify the matching rule that determines which devices belong to the group
4. review devices that match against the rule
6. Assign the user groups that can access the device group you created
7. Select **Close**. The configuration changes are applied

## Security enhancements:
- ASR rules (attack surface reductiion)
- Hardware-based isolation
- Application control
- Exploit protection
- Network protection
- Web protection
- Controlled folder access
- Device control

## Investigations
- Devices list
- Alerts queue
- Security operations dashboard
- Any individual alert
- Any individual file details view
- Any IP address or domain details view

When you investigate a specific device, you'll see:
- Device details
- Response actions
- Cards (active alerts, logged on users, security assessment)

Response actions:
- Manage tags
- Isolate device
- Restrict app execution
- Run antivirus scan
- Collect investigation package
- Initiate Live Response Session
- Initiate automated investigation
- Consult a threat expert
- Action center

## Automation
Automate on folder exclusions:
- Select New folder exclusion.
- Enter the folder details:
    - Folder
    - Extensions
    - File names
    - Description
- Select **Save**.

# Defender for Identity
leverages your on-prem AD signals to identify, detect, and investigate threats/incidents
- Monitor users, entity behavior, and activities with learning-based analytics
- Protect user identities and credentials stored in Active Directory
- Identify and investigate suspicious user activities and advanced attacks throughout the kill chain
- Provide clear incident information on a simple timeline for fast triage

## Configure:
1. Create an instance on Microsoft Defender for Identity management portal
2. Specify an on-premises AD service account in Defender for Identity portal
3. Download and install the sensor package
4. Install the Microsoft Defender for Identity sensor on all domain controllers
5. Exclude the sensitive accounts you've listed during the design process
6. Configure the required permissions for the sensor to make SAM-R calls
7. Configure integration with Microsoft Defender for Cloud Apps
8. Configure integration with Microsoft 365 Defender 

# Defender for cloud
**Cloud Security Posture Management (CSPM)** - continually assesses your resources, subscriptions, and organization for security issues

it can secure following resources:
- Microsoft Defender for Servers
- Microsoft Defender for App Service
- Microsoft Defender for Storage
- Microsoft Defender for Databases
- Microsoft Defender for Containers
- Microsoft Defender for Key Vault
- Microsoft Defender for Resource Manager
- Microsoft Defender for DNS

## connecting resources
asset inventory uses Azure Resource Graph
- Defender for Cloud's sidebar, select Inventory.
    
- Filter by name to display a specific resource, or use filters as described below:
- Select the relevant options in the filters
- To use the Security findings contain filter

# Defender for Cloud Apps
it is a CASB
- **Discover and control the use of Shadow IT**
- **Protect your sensitive information anywhere in the cloud**
- **Protect against cyberthreats and anomalies**
- **Assess the compliance of your cloud apps**

- You can discover cloud apps in use across org
- protect data using conditional access app control
- classify and protect sensitive information
	- discover data
	- classify data
		- **Personal**
		- **Public**
		- **General** - cant be shared to public, but can with external partners
		- **Confidential** - could damage org if shared with unauthorized identities
		- **Highly confidential** - serious damage if shared with unauthorized identities
	- protect data
		-  Trigger alerts and email notifications.
		- Change sharing access for files.
		- Quarantine files.
		- Remove file or folder permissions.
		- Move files to a trash folder.
- Monitor and report

## DLP
- DLP alerts are available in MCAS 
- File policy is used for DLP in MCAS
- DLP policy is used to protect locations such as sharepoint

## Detect threats:
you can detect anomalies based on the following risk factors:
- Risky IP address
- Login failures
- Admin activity
- Inactive accounts
- Location
- Impossible travel
- Device and user agent
- Activity rate

## Anomaly policies
you can create your own polocies but most popular security issues to generate polocies around are:
- **Impossible travel**
- **Activity from infrequent country**
- **Malware detection**
- **Ransomware activity**
- **Activity from suspicious IP addresses**
- **Suspicious inbox forwarding**
- **Unusual multiple file download activities**
- **Unusual administrative activities**

# Secure Score
Products included in Secure Score:
- Microsoft 365 (including Exchange Online)
- Azure Active Directory
- Microsoft Defender for Endpoint
- Microsoft Defender for Identity
- Defender for Cloud Apps
- Microsoft Teams

The **Improvement actions** tab helps improve score

# Threat analytics:
shows:
- Active threat actors and their campaigns
- Popular and new attack techniques
- Critical vulnerabilities
- Common attack surfaces
- Prevalent malware

categorises as:
- Latest threats
- High-impact threats
- Highest exposure

You can do the following:
- View blocked or junked threat emails
- Set up email notifications for report updates
- Get list of impacted devices and mailboxes
- Get insight from Microsoft security researchers
- Review list of mitigations and the status of your devices

# Azure AD ID Protection
helps you to automatically detect, remediate, and investigate identity-based risks for your organization.

It protects by looking at:
- User risk
	- unusual behaviour
	- leaked creds
- sign in risk
	- unfamiliar signin properties
	- Atypical travel
	- malware linked ip's
	- anonymous ip's

Two ways to handle ID risk:
- Self Remediation 
	- when risk is detected, get user to reset password
- Admin remediation
	- when risk detected, notify admin to investigate and take action

To protect identity based risk:
- configure a policy
- investigate using a report
- remediate

## configure policy:
- Sign-in risk policy
	- The users this policy should target
	- The conditions that must be met, such as how high a score triggers the policy
	- How you want to respond
	- review
- User risk policy
	- users
	- conditions
	- controlls (require password change)
	- review

You can do MFA registration here. 

## Remediation
actions:
- Self-remediation
- Reset passwords manually
- dismiss risk 
- close detection 
- unblock users which may have been blocked due to user or signin risk

# Purview (The most boring)
Covers:
- Intellectual property (IP) theft
- Espionage
- Leaks of sensitive business assets
- Confidentiality violations
- Sabotage
- Fraud
- Insider trading
- Code-of-conduct violations
- Regulatory compliance violations

Scenarios:
- **Data theft by departing employee**
- **Leak of sensitive or confidential information**
- **Actions and behaviours that violate corporate policies**

## Insider risk management workflow
- Policies
- Alerts
- Triage
- Investigate
- Action

everything else is just about policies and insider risk policies (boring)

## Audit solutions:
Standard:
- enabled by default 
- thousands of audited events
- 90 day retention
- accessed by GUI, cmdlet and API
setup:
- verity subscription and user licensing
- assign permissions to audit log
- search audit log

Premium:
- longer retention
- custom retention polocies
- high value crucial events
- higher bandwith access to API
Setup:
- setup audit for users
	- ms 365 admin center
	- active users page
	- licenses and apps
	- licenses section verify E5 licenses for all users
	- expand apps section, verify MS 365 advanced auditing

Threat investigation with premium:
see events such as:
- when mail items were accessed.
- when mail items were replied to and forwarded.
- when and what a user searched for in Exchange Online and SharePoint Online.

## Content search 
Allows search across:
- Exchange Online
- OneDrive for Business
- SharePoint Online
- Microsoft Teams
- Microsoft 365 Groups
- Yammer teams

works in 3 ways:
- content search
	- search content
	- keyword queries
	- export search results
	- Role based permissions
- eDiscovery
	- search and export
	- case management
	- legal hold
- eDisco - Premium
	- custodian management (manage external parties access to data)
	- legal hold
	- advanced indexing
	- review set filtering
	- tagging
	- analytics
	- coding models
	- more...

for preview items, must have a max of 1k randomly selected items available
for optimisation, disable antivirus when downloading large data sets from search results

# Sentinel
Its a SIEM. You ingest all log sources to it for correlating incidents across tables

## setting up sentinel 
- tenant
	- subsciption
		- resource group
			- workspace
				- sentinel

## Automation rules
Automation rules used like ACL's, they are triggered when specific conditions are met. They also have a priority list for running sequentially. they need to be enabled and in the correct order under active automation tab. an example for order might be that you want specific suppressions for defender related rule to suppress entities mapped to incidents, and then run connection playbook to bring the incident in the form of a ticket into your ITSM platform. 

## Playbooks
Playbooks are essentially linked logic apps. These can be triggered via automation rules when conditions are met on incidents. Playbooks essentially provide your SOAR capability. to action incidents and enrich data from other sources such as TI or other third party services such as Virus Total or ChatGPT. 

## Workbooks
Workbooks are dashboards. You can set them up to correlate data into a single place to review KPI/activity etc...
## Behavioural analytics
A lot of bark, no bite. all ML algorithms unknown to the public, so they can raise incidents without clear indicators as of to why. Only way to tune is to suppress or mark as false positive and hope the L in ML actually does its job. 

## Data Normalisation
This is the process of mapping entities across tables. E.G:
table1 marks IP address as 'IP_Address'
table2 marks IP address as 'IpAddress'

normalisation is the process of mapping the two entities to be seen as the same (IP_Address == IpAddress)

### ASIM
Advanced Security Information Model (ASIM) is a layer that helps normalise logs from multiple sources.

I didnt want to share images in this file, but this image explains it the best:
![](https://learn.microsoft.com/en-us/training/wwl-sci/data-normalization-microsoft-sentinel/media/asim-architecture.png)

## Managing content
- **Data connectors** provide log ingestion from different sources
- **Parsers** provide log formatting/transformation into ASIM format
- **Workbooks** dashboards
- **Analytics** rules in sentinel as oppose to defender etc...
- **Hunting queries** used to query environment for potential bad items
- **Notebooks** allows extensive advanced lookups and querying with Jupyter Notebooks
- **Watchlists** Lists you can use to suppress items against rules (whitelist of users / IP's)
- **Playbooks** Logic Apps for automated investigations, remediations, and response scenarios

## Content Hub
content hub is a market place where you can download items related to an app. E.G
Azure Activity:
- 14 analytics rules
- 12 hunting queries
- 1 connector
- 4 playbooks

## Sentinel Repos
Use this to bring a CI/CD workspace into Sentinel allowing you to revert rule changes, push rule changes across multi tenant deployments, automatically have tuned rules for new customers in an MSSP environment etc...


## Notebooks
Notebooks are really cool. mainly because you can now use python on a Microsoft platform instead of el cancer powershell 

2 libraries for API access:
- Kqlmagic
- msticpy

# KQL
works like sql, but backwards, select the table and then filter options, where in sql you select options and then specify which table you want to query, and do calculations on data afterwards.  NOTE this area is my speciality so i have made quick notes, but i would recommend going through this section to understand KQL and especally joins / unions and join types better:
https://learn.microsoft.com/en-us/training/modules/build-multi-table-statements-kusto-query-language/3-use-join-operator
remember:
```
SigninLogs
| join kind = inner (AADNonInteractiveUserSignInLogs
) on UserPrincipalName

```

a good video to help visualise join types:
https://www.youtube.com/watch?v=66UDqdILgpc&t=306s

common statmenets:
- where
- let
- join
- extend
- summarize
- project
- order
- distinct
- render

some useful functions:
- count()
- date()
- bin()
- externaldata()
- not()
- has_any()
- arg_max()/arg_min()
- make_list()
- todynamic()
- tostring()
- extract()
- datatable()
- split()

understand how to get nested data:
```
SigninLogs
| extend dynProperties = todynamic(extendedproperties)
| extend IPAddress = dynProperties[0].IPAddress
| project tostring(IPAddress)
```
understand how to expand nested arrays to return all data:
```
SigninLogs
| extend dynProperties = todynamic(extendedproperties)
| mv-expand dynProperties
| extend IPAddress = dynProperties.IPAddress
| project tostring(IPAddress)
```
understand how to split string data:
```
SigninLogs
| extend Domain = split(emailAddress, "@")[-1]
| project tostring(Domain)
```
