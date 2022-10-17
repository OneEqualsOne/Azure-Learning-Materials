# Basic Security Capabilities in AZ 
-   Describe Azure security capabilities for protecting your network. 
-   Describe how Azure can protect your VMs. 
-   Describe how encryption on Azure can protect your data. 

## Describe Azure DDoS protection 
Distributed Denial of Service attacks 
The three most frequent types of DDoS attack are: 
-   **Volumetric attacks** - These are volume-based attacks that flood the network with seemingly legitimate traffic, overwhelming the available bandwidth. Measured in bits per second  
-   **Protocol attacks** - Protocol attacks render a target inaccessible by exhausting server resources with false protocol requests that exploit weaknesses in layer 3 (network) and layer 4 (transport) protocols. measured in packets per second. 
-   **Resource (application) layer attacks**: These attacks target web application packets, to disrupt the transmission of data between hosts. 

What is Azure DDoS Protection? 

help protect your applications and servers by analysing network traffic and discarding anything that looks like a DDoS attack. 

![DDoS Protection](https://learn.microsoft.com/en-us/training/wwl-sci/describe-basic-security-capabilities-azure/media/2-network-flow.png)
2 tiers of DDoS protection:
- **Default DDoS infrastructure protection** – auto enabled for every property in azure with no extra cost 
- **DDoS protection standard** – enhanced mitigation and auto tunes to help specific resources 

## Azure Firewall 
protects your Azure virtual network (VNet) resources from attackers.
![Azure Firewall](https://learn.microsoft.com/en-us/training/wwl-sci/describe-basic-security-capabilities-azure/media/2-azure-firewall.png)
you can scale up the usage to accommodate changing network traffic flows 

Key features:
-   **Built-in high availability and availability zones** - Azure Firewall can be configured to span multiple availability zones for increased availability. 
-   **Network and application level filtering** - Use IP address, port, and protocol to support fully qualified domain name filtering for outbound HTTP(s) traffic and network filtering controls. 
-   **Outbound SNAT and inbound DNAT to communicate with internet resources** – Keep addresses private and routed internally 
-   **Multiple public IP addresses** - These addresses can be associated with Azure Firewall and not link back to the origin after translation. 
-   **Threat intelligence** - Threat intelligence-based filtering can be enabled for your firewall to alert and deny traffic from/to known malicious IP addresses and domains. 
-   **Integration with Azure Monitor** - Integrated with Azure Monitor to enable collecting, analysing, and acting on telemetry from Azure Firewall logs. 

## Network segmentation in Azure 
The main reasons for network segmentation are: 
-   The ability to group related assets that are a part of (or support) workload operations. 
-   Isolation of resources. 
-   Governance policies set by the organization. 
Network segmentation also supports the Zero Trust model and defence in depth. Network segmentation can secure interactions between perimeters.

## Azure Virtual Network 
Azure VNet is the fundamental building block for your organization's private network in Azure. It enables organizations to segment their network. Essentially, this means no traffic is allowed across VNets or inbound to the VNet, by default. This is helpful for ensuring access to organisational resources is only used when it is needed ensuring, if the network was compromised, an attacker would not be able to access the whole network. Chopping off the arm rather than destroying the body. 

## NSG's 
let you filter network traffic to and from Azure resources in a VNet. You can associate only ONE network security group to each virtual network subnet and network interface in a virtual machine. An NSG is made up of inbound and outbound security rules. They are evaluated by priority using five information points: 
- source address
- source port 
- destination
- destination port
- protocol
to either allow or deny the traffic. Lower values are processed first. 

## NSG V Firewall: 
NSG's provide distributed network layer traffic filtering to limit traffic to resources within virtual networks in each subscription. Azure Firewall is a fully stateful, centralized network firewall as-a-service, which provides network and application-level protection across different subscriptions and virtual networks. 

## Azure Bastion and JIT 
You have multiple VNets in combination with NSG's and Azure firewall. You are protected from external threats, but now we need to look at internal threats. Traditionally you would need to expose RDP or SSH to the internet. This causes significant attack surface increase.  

### Azure bastion: 
Bastion is a service you deploy that lets you connect to a virtual machine using your browser and the Azure portal. It is a fully platform-managed PaaS. It provides secure and seamless RDP and SSH connectivity to your virtual machines directly from the Azure portal using TLS.

Bastion deployment is done per virtual network with support for virtual network peering, not per subscription/account.
-   RDP and SSH directly in Azure portal 
-   Remote session over TLS and firewall traversal for RDP/SSH 
-   No Public IP required on the Azure VM 
-   No hassle of managing NSGs 
-   Protection against port scanning 
-   Hardening in one place to protect against zero-day exploits 

### Just-in-time 
Allows lock down of the inbound traffic to your VMs, reducing exposure to attacks while providing easy access to connect to VMs when needed. 
When you enable just-in-time VM access, you can select the ports on the VM to which inbound traffic will be blocked 
When a user requests access to a VM, Defender for Cloud checks that the user has RBAC permissions for it.  If approved, Defender for Cloud configures the NSGs and Azure Firewall to allow inbound traffic to the selected ports from the relevant IP address (or range), for the amount of time that was specified.  
After the time has expired, Defender for Cloud restores the NSGs to their previous states.  
JIT requires Microsoft Defender for servers to be enabled on the subscription. 

## Encryption On Azure 
Microsoft Azure provides many different ways to secure your data, each depending on the service or usage required. 
-   Azure Storage Service Encryption helps to protect data at rest 
-   Azure Disk Encryption helps you encrypt Windows and Linux IaaS virtual machine disks.  
-   Transparent data encryption (TDE) helps protect Azure SQL Database and Azure Data Warehouse against the threat of malicious activity. It performs real-time encryption and decryption of the database, associated backups, and transaction log files at rest without requiring changes to the application. 

### What is Azure Key Vault? 
It's useful for different kinds of scenarios: 
-   Secrets management - control access to tokens, passwords, certificates, Application Programming Interface (API) keys, and other secrets. 
-   Key management - easier to create and control the encryption keys used to encrypt your data. 
-   Certificate management - provision, manage, and deploy your public and private TLS certificates for Azure, and internally connected, resources more easily. 
-   Store secrets backed by hardware security modules (HSMs). The secrets and keys can be protected either by software or by FIPS 140-2 Level 2 validated HSMs. You need premium key-vault for this feature. 

# Management in azure 
-   Describe cloud security posture management. 
-   Describe the capabilities of Microsoft Defender for Cloud 
-   Understand the Azure Security Benchmark and security baseline in Azure. 

## Cloud security posture management 
Cloud security posture management (CSPM) is a relatively new class of tools designed to improve your cloud security management. 

CSPM uses a combination of tools and services: 
-   **Zero Trust-based access control** - Considers the active threat level during access control decisions. 
-   **Real-time risk scoring** 
-   **Threat and vulnerability management (TVM)** - Establishes a holistic view of the organization's attack surface and risk  
-   **Discover risks** - To understand the data exposure of enterprise intellectual property, on sanctioned and unsanctioned cloud services. 
-   **Technical policy** - Apply guardrails to audit and enforce the organization's standards and policies to technical systems. 
-   **Threat modelling systems and architectures** - Used alongside other specific applications. 
The goal is to assess the posture of the cloud environments and focus on where attackers can get the most out of the system.  

## Defender for Cloud 
Microsoft Defender for Cloud fills three vital needs as you manage the security of your resources and workloads in the cloud and on-premises: 
-   **Continuously assess** - Know your security posture, identify and track vulnerabilities. 
-   **Secure** - Harden all connected resources and services. 
-   **Defend** - Detect and resolve threats to resources, workloads, and services. 
It covers  two broad pillars of cloud security: cloud security posture management and cloud workload protection 

In Microsoft Defender for Cloud, the posture management features provide: 
-   **Visibility** - to help you understand your current security situation 
-   **Hardening guidance** - to help you efficiently and effectively improve your security 
It provides hardening recommendations based on any identified security misconfigurations and weaknesses. 

## Enhanced security of Microsoft Defender for Cloud 
Microsoft Defender for Cloud is offered in two modes: 
-   **Microsoft Defender for Cloud (Free)** - provides the secure score and its related features: security policy, continuous security assessment, and actionable security recommendations to help you protect your Azure resources. 
-   **Microsoft Defender for Cloud with enhanced security features** – Enables the capabilities of the free mode to workloads running in Azure, hybrid, and other cloud platforms, providing unified security management and threat protection across your workloads. Cloud workload protections are delivered through integrated Microsoft Defender plans, specific to the types of resources in your subscriptions and provide enhanced security features for your workloads. 

### Plans 
-   **Microsoft Defender for servers** - adds threat detection and advanced defences for your Windows and Linux machines. 
-   **Microsoft Defender for App Service** - identifies attacks targeting applications running over App Service. 
-   **Microsoft Defender for Storage** - detects potentially harmful activity on your Azure Storage accounts. 
-   **Microsoft Defender for SQ** - secures your databases and their data wherever they're located. 
-   **Microsoft Defender for Kubernetes** - provides cloud-native Kubernetes security environment hardening, workload protection, and run-time protection. 
-   **Microsoft Defender for container registries** - protects all the Azure Resource Manager based registries in your subscription.
-   **Microsoft Defender for Key Vault** - is advanced threat protection for Azure Key Vault. 
-   Microsoft Defender for Resource Manager - automatically monitors the resource management operations in your organization. 
-   **Microsoft Defender for DNS** - provides an additional layer of protection for resources that use Azure DNS's Azure-provided name resolution capability. 
-   **Microsoft Defender for open-source relational protections** - brings threat protections for open-source relational databases. 

### Enhanced security features 
-   Comprehensive endpoint detection and response 
-   Vulnerability scanning 
-   Multi-cloud security – AWS, GCP etc... 
-   Hybrid security – Get a unified view of security across all of your on-premises and cloud workloads 
-   Threat protection alerts 
-   Track compliance with a range of standards 
-   Access and application controls   

## Azure Security Benchmark and security baselines 
ASB provides prescriptive best practices and recommendations to help improve the security of workloads, data, and services on Azure.
Key features: 
-   ASB ID 
-   Control domain 
-   Mapping to industry frameworks 
-   Recommendation 
-   Security principles
-   Azure Guidance 

### Security baselines 
Security baselines help apply guidance from the Azure Security Benchmark to the specific service for which it's defined 
-   Azure ID 
-   **Azure control** - The content is grouped by control domain area, as listed in the Azure Security Benchmark, and that is applicable to the service for which the security baseline is defined. 
-   Benchmark Recommendation 
-   **Customer guidance** - The rationale for the recommendation and links to guidance on how to implement it. 
-   Responsibility
-   Microsoft Defender for Cloud monitoring 

# Sentinel 
-   Describe the security concepts for SIEM and SOAR. 
-   Describe how Microsoft Sentinel provides integrated threat protection. 
-   Describe the pricing models of Microsoft Sentinel. 
A SIEM system is a tool that an organization uses to collect data from across the whole estate, correlate that data to produce alerts and analyse the alerts to find incidents.

A SOAR system takes alerts from many sources, such as a SIEM system. The SOAR system then triggers action-driven automated workflows and processes to run security tasks that mitigate the issue. 

## Threat management in sentinel 
![Threat intel in sentinel](https://learn.microsoft.com/en-us/training/wwl-sci/describe-security-capabilities-of-azure-sentinel/media/3-four-aspects-azure-sentinel.png)
This diagram shows the end-to-end functionality of Microsoft Sentinel. 
-   **Collect** data at cloud scale across all users, devices, applications, and infrastructure, both on-premises and in multiple clouds. 
-   **Detect** previously uncovered threats and minimize false positives using analytics and unparalleled threat intelligence. 
-   **Investigate** threats with artificial intelligence (AI) and hunt suspicious activities at scale, tapping into decades of cybersecurity work at Microsoft. 
-   **Respond** to incidents rapidly with built-in orchestration and automation of common security tasks. 

Connecting data: 
- Comes with connectors and agents 
- Workbooks help analyse data 
- Analytics correlates data 
- Use it for incident management 
- SOAR is also available in the form of playbooks and integrated logic apps / auto workflow 
- It supports Jupiter notebooks to share docs 

## Costs 
-   **Capacity Reservations** - With Capacity Reservations, you're billed a fixed fee based on the selected tier, enabling a predictable total cost for Microsoft Sentinel. 
-   **Pay-As-You-Go** - With Pay-As-You-Go pricing, you're billed per gigabyte (GB) for the volume of data ingested for analysis in Microsoft Sentinel and stored in the Azure Monitor Log Analytics workspace. 

# MS 365 Defender 
-   Describe the Microsoft 365 Defender service. 
-   Describe how Microsoft 365 Defender provides integrated protection against sophisticated attacks. 
-   Describe and explore Microsoft 365 Defender portal. 

## Services 
Defender takes the layers of defence in depth and unifies data in a single viewpoint.
-   Identities are secured with Microsoft Defender for Identity and Azure AD Identity Protection 
-   Endpoints are secured with Microsoft Defender for Endpoint Applications with Microsoft Defender for Cloud Apps 
-   Email and collaboration efforts are secured with Microsoft Defender for Office 365  

## Defender for Office 365 
Defender for Office 365 focusses on securing email messages, links (URLs), and collaboration tools, including Microsoft Teams, SharePoint Online, OneDrive for Business, and other Office clients. 
Microsoft Defender for Office 365 covers these key areas: 
-   Threat protection policies 
-   Reports 
-   Threat investigation and response capabilities 
-   Automated investigation and response capabilities 
There are 2 plans with differing features

### Features of Plan 1 
-   **Safe Attachments** - Checks email attachments for malicious content. 
-   **Safe Links - Links are scanned for each click. A safe link remains accessible, but malicious links are blocked. 
-   Safe Attachments for SharePoint, OneDrive, and Microsoft Teams: Protects your organization when users collaborate and share files by identifying and blocking malicious files in team sites and document libraries. 
-   **Anti-phishing protection** - Detects attempts to impersonate your users and internal or custom domains. 
-  **Real-time detections** - A real-time report that allows you to identify and analyse recent threats. 

### Features of Plan 2 
-   Threat Trackers 
-   Threat Explorer 
-   **Automated investigation and response (AIR)** - Includes a set of security playbooks that can be launched automatically, such as when an alert is triggered, or manually. A security playbook can start an automated investigation 
-   **Attack Simulator - Allows you to run realistic attack scenarios 
-   Proactively hunt for threats with advanced hunting in Microsoft 365 Defender 
-   Investigate alerts and incidents in Microsoft 365 Defender 
Microsoft Defender for Office 365 is included in certain subscriptions, such as Microsoft 365 E5, Office 365 E5, Office 365 A5, and Microsoft 365 Business Premium. 

## Defender for Endpoint 
This tool is used to help secure endpoints such as but not limited to clients, computers, laptops and mobile devices. Microsoft Defender for Endpoint includes the following features:
-   Threat and vulnerability management 
-   Attack surface reduction 
-   **Next generation protection** - machine learning, big data analysis, in-depth threat resistance research. 
-   Endpoint detection and response 
-   Automated investigation and remediation 
-   Microsoft Threat Experts 
-   Management and APIs 
Defender for Endpoint includes Microsoft Secure Score for devices.

## Defender for Cloud Apps 
Microsoft Defender for Cloud Apps is a Cloud Access Security Broker (CASB). A CASB acts as a gatekeeper to broker real-time access between your enterprise users and the cloud resources 
It enables: 
-   **Visibility** - Detect cloud services and app use and provide visibility into Shadow IT. 
-   **Threat protection** - Monitor user activities for anomalous behaviours, control access to resources through access controls, and mitigate malware. 
-   **Data security** - Identify, classify and control sensitive information, protecting against malicious actors. 
-   **Compliance** - Assess the compliance of cloud services. 

## Defender for Cloud Apps framework 
Microsoft Defender for Cloud Apps is built on a framework that provides the following capabilities: 
-   **Discover** and control the use of Shadow IT 
-   **Protect** against cyberthreats and anomalies 
-   **Protect** your sensitive information anywhere in the cloud 
-   **Assess** your cloud app's compliance

### Functionality: 
Defender for Cloud Apps Security delivers on the components of the framework through an extensive list of features and functionality:
-   Cloud Discovery 
-   Sanctioning and un-sanctioning apps 
-   App connectors 
-   Conditional Access  
-   Use policies to detect risky behaviour, violations, or suspicious data points and activities in your cloud environment.  

## Office 365 Cloud App Security 
Office 365 Cloud App Security is a subset of Microsoft Defender for Cloud Apps that provides enhanced visibility and control for Office 365. Azure Active Directory Premium P1 includes Azure Active Directory Cloud App Discovery at no extra cost. 

## Microsoft Defender for Identity 
This uses your on-premises Active Directory data (called signals) to identify, detect, and investigate advanced threats, compromised identities, and malicious insider actions 
Microsoft Defender for Identity provides security professionals managing hybrid environments functionality to: 
-   **Monitor** and profile user behaviour and activities. 
-   **Protect** user identities and reduce the attack surface. 
-   **Identify** and investigate suspicious activities and advanced attacks across the cyberattack kill-chain. 
-   Provide clear incident information on a simple timeline for fast triage 

## Microsoft 365 Defender portal 
The Microsoft 365 Defender portal home page shows many of the common cards that security teams need. The cards fall into these categories: 
-   **Identities** - Monitor the identities in your organization and keep track of suspicious or risky behaviours. 
-   **Data** - Help track user activity that could lead to unauthorized data disclosure. 
-   **Devices** - Get up-to-date information on alerts, breach activity, and other threats on your devices. 
-   **Apps** - Gain insight into how cloud apps are being used in your organization. 

### Incidents and alerts 
Microsoft 365 services and apps create alerts when they detect a suspicious or malicious event or activity 
The incidents queue is a central location lists each incident by severity including:
-   All the alerts related to the incident. 
-   All the users that have been identified to be part of or related to the incident. 
-   All the mailboxes that have been identified to be part of or related to the incident. 
-   All the automated investigations triggered by the alerts in the incident. 
-   All the supported evidence and response. 
You can also get threat analytics and secure score in it.