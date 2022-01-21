# Deducing the impact of a compromised Azure AD user assigned to a Built-In-Role
Azure AD has an ever expanding number of built-in roles. A common question for both offensive and defensive security professionals is:

"What happens if a user with Azure AD role XYZ is compromised? Should we alert on this? What is the worst case scenario? As a pentester, should I target users with this role?"

This page seeks to answer these question in a simple and concise way.


# Role matrix

The following matrix breaks down known offensive abuse techniques corresponding to each Azure AD role.

Column descriptions:

*Azure AD Built-in Role* - The Azure AD built in roles, defined at https://docs.microsoft.com/en-us/azure/active-directory/roles/permissions-reference

*Abuse Technique* - A short name for any offensive technique that can take advantage of this role. If there is no standard name for a technique, I get creative :)

*Impact* - The immediate technical impact of the abuse. For example, "any user's password can be reset"

**Note: these techniques require that the attacker has compromised a user with the Azure AD role in the first column of the table. The initial compromise is not covered.**


|         Azure AD Built-in Role       |         Abuse technique               | Impact| 
|-----------|-------------------------------|-----------------------------|
|Application Administrator| Application impersonation          |Assumption of application permissions in directory, in customer directories, and on Azure resources   |
|    Application Developer    | No known techniques| |
| Attack Payload Author       | No known techniques| |
| Attack Simulation Administrator       | No known techniques| |
| Attribute Assignment Administrator       | No known techniques| |
| Attribute Assignment Reader       | No known techniques| |
| Attribute Definition Administrator       | No known techniques| |
| Attribute Definition Reader       | No known techniques| |
|Authentication Administrator         |Reset non-admin passwords         |Account takeover of non-admin account            |
|Authentication Policy Administrator        |?         |?            |
|Azure AD Joined Device Local Administrator        |Azure AD joined device escalation | Take over any Azure AD joined device as a local administrator|
|Azure DevOps Administrator        |? | ?|
|Azure Information Protection Administrator        |? | |
|B2C IEF Keyset Administrator        |No known techniques | |
|B2C IEF Policy Administrator        |No known techniques | |
|Billing Administrator        | ?| |
|Cloud App Security Administrator        |? | |
|Cloud Application Administrator        | ?| |
|Cloud Device Administrator        |? | |
|Compliance Administrator        | | |
|Compliance Data Administrator        | | |
|Conditional Access Administrator        | | |
|Customer LockBox Access Approver        | | |
|Desktop Analytics Administrator        | | |
|Directory Readers    |No known techniques | |
|Directory Synchronization Accounts    | | |
|Directory Writers    | | |
|Domain Name Administrator    | | |
|Dynamics 365 Administrator    | | |
|Edge Administrator    | | |
|Exchange Administrator    | | |
|Exchange Recipient Administrator    | | |
|External ID User Flow Administrator    | | |
|External ID User Flow Attribute Administrator    | | |
|External Identity Provider Administrator    | | |
|Global Administrator    | | |
|Global Reader    |No known techniques | |
|Groups Administrator    | | |
|Guest Inviter    | | |
|Helpdesk Administrator    | | |
|Hybrid Identity Administrator    | | |
|Identity Governance Administrator    | | |
|Insights Administrator    | | |
|Insights Business Leader    | | |
|Intune Administrator    | | |
|Kaizala Administrator    | | |
|Knowledge Administrator    | | |
|Knowledge Manager    | | |
|License Administrator    | | |
|Message Center Privacy Reader    | | |
|Message Center Reader    | | |
|Modern Commerce User    | | |
|Network Administrator    | | |
|Office Apps Administrator    | | |
|Partner Tier1 Support    | | |
|Partner Tier2 Support    | | |
|Password Administrator    | | |
|Power BI Administrator    | | |
|Power Platform Administrator    | | |
|Printer Administrator    | | |
|Printer Technician    | | |
|Privileged Authentication Administrator    | | |
|Privileged Role Administrator    | | |
|Reports Reader    | | |
|Search Administrator    | | |
|Search Editor    | | |
|Security Administrator    | | |
|Security Operator    | | |
|Security Reader    | | |
|Service Support Administrator    | | |
|SharePoint Administrator    | | |
|Skype for Business Administrator    | | |
|Teams Administrator    | | |
|Teams Communications Administrator    | | |
|Teams Communications Support Engineer    | | |
|Teams Communications Support Specialist    | | |
|Teams Devices Administrator    | | |
|Usage Summary Reports Reader    | | |
|User Administrator    | | |
|Windows 365 Administrator    | | |
|Windows Update Deployment Administrator    | | |








