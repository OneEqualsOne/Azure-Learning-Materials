# Security and compliance concepts 
-   Describe the shared responsibility and the defense in-depth security models. 
-   Describe the Zero-Trust model. 
-   Describe the concepts of encryption and hashing. 
-   Describe some basic compliance concepts. 

On prem = 100% responsible  
Shared responsibility changes depending on service type: 
![Shared responsability model](https://learn.microsoft.com/en-us/training/wwl-sci/describe-security-concepts-methodologies/media/3-shared-responsibility-model.png)

## Defence in depth 
Concept meaning multiple layers of security  
![D in D](https://learn.microsoft.com/en-us/training/wwl-sci/describe-security-concepts-methodologies/media/4-defense-depth.png)
Perimeter = Security of corporate network to the internet 
Compute = Securing access to VM's and on prem ports/computers
CIA triad also used here (Confidentiality, Integrity, Accessibility)

## Zero Trust model 
Assumes everything is open and untrusted even behind firewalls and networks.  
### Principals of Zero Trust
- **Verify Explicitly** – always authenticate and authorize based on available data points, user id, location, device, service, workload, data classification and anomalies  
- **Least Privilege** – always limit user access to just what they need and nothing more.  
- **Assume breach** – Segment network access, user, device and application access. Use encryption to encrypt in transit and at rest. Use analytics to detect and prevent threats.  

Access pillars (pillars = artefacts that can affect an outcome of access) in the zero trust model:
-   Identities 
-   Devices 
-   Applications 
-   Data 
-   Infrastructure 
-   Networks  

## Describe encryption and hashing 
- **Symmetric** - same key, used for encrypting files, is more efficient memory wise.  
- **Asymmetric** - different keys, used for authentication or 1 way communication over https to stop MITM (Man In The Middle) attacks.  
- **Hashing** = fixed length values, 1 way functions (irreversible) often used for normalizing data and storing passwords. 

## Compliance concepts 
- **Data residency** – physical locations where data can be stored, how and when it can be transferred, processed or accessed internationally.
- **Data Sovereignty** – personal data subject to laws where it is physically collected, heled or processed.
- **Data privacy** – transparent about the collection, processing, use and sharing of personal data. PII laws

# Describe Identity Concepts 
-   Understand the difference between authentication and authorization. 
-   Describe the concept of identity as a security perimeter. 
-   Describe identity-related services. 

## Difference between authentication and authorization 
- **Authentication** - proving a person is who they say they are 
- **Authorization** - Access to resources once authenticated 

## Identity as the primary security perimeter:
![ID as primary security perimeter](https://learn.microsoft.com/en-us/training/wwl-sci/describe-identity-principles-concepts/media/3-identity-new-security-perimeter.png)
There are 4 pillars of an identity infrastructure: 
-   Administration 
-   Authentication 
-   Authorization 
-   Auditing 

## Role of ID provider 
It is essentially to provide a centralised point where you pass security tokens between the IdP and the client. This stops the cumbersome process of re-authenticating, having different logins for everything and processing more compute. This also helps with automation.
Modern authentication is an umbrella term for authentication and authorization methods between a client, such as your laptop or phone, and a server, like a website or application. At the centre of modern authentication is the role of the identity provider. An identity provider creates, maintains, and manages identity information while offering authentication, authorization, and auditing services. 
SSO is also good for helping prove identities and managing access. 
Claims are information about an identity calling out to the server. This can be a user, device, process etc... one of the claims is the 'subject' this is a one time immutable access entity.  
Another claim is the 'issued at' claim. This says when the token is no longer valid.  
The audience claim tells the server which token can be used and where (authorization) 

## AD DS and AD 
AD = set of directory services for on prem, domain-based networks 
AD DS = centralised component in orgs with in-prem who want to manage infra components and systems using a single identity per user.  

## Federation 
Enables access of services across organizational or domain boundaries by establishing trust relationships between domains id providers.  
No need for user to have different creds  
Federation relies on IdP A and IdP B establishing a trust relationship to be able to allow access
