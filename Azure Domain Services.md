# Azure Domain Services

## What is Azure AD Domain Services?
- Azure AD domain services is essentially a **managed version** of a traditional on-prem Active Directory
    - Offers Domain Join, Group Policy, LDAP, Kerberos, and NTLM authentication
    - Does not require deployment or management of DCs
- Azure AD Domain Services works with your existing Azure AD tenant
    - Fully compatible with cloud only Azure AD tenants
    - Compatible with Azure AD tenants that are synced with an on-prem AD
    - Users synced into Azure AD will show up in Azure AD domain services 

## How does Azure ADDS Work?
When Azure ADDS is deployed, a managed domain is created on the virtual network that you specify.
- Azure spins up two Windows server domain controllers that run on VMs
- You cannot manage, or even access, the domain controllers
- Azure performs all management of the domain controllers
- The managed domain that is spun up is configured for one-way synchronization from Azure AD
![8](8.PNG)
![9](9.PNG)
- Azure AD Domain Services is tightly integrated with Azure Active Directory.
    - Accounts in external directories that are linked to your Azure AD will not be available in Azure Active Directory domain services
    - Because users and their credentials are synchronized from Azure Active Directory into Azure Active Directory domain services, users only have to remember one set of credentials to sign in and to authenticate against Azure Active Directory domain services
## Azure ADDS Best Practices
- CLOUD-ONLY BEST PRACTICE:
    - Create resources in Azure Active Directory and let them sync over to the managed domain service.
- HYBRID BEST PRACTICE:
    - Create users in the on-prem AD so they synchronize over to Azure Active Directory with Azure AD connect.
    - After syncing to Azure AD, they will sync to Azure AD domain services

## Azure ADDS Authentication
Azure ADDS supports Kerberos & NTLM authentication.
- Allows you to deploy applications that rely on Windows integrated authentication
- Simplifies lift and shift of applications to Azure

## Azure ADDS Availability
Because Azure Active Directory domain services includes multiple domain controllers, the managed domain is always available

## Note
- An Azure Active Directory domain services managed domain is a **standalone** domain.
- Azure Active Directory domain services managed domain **IS NOT** an extension of an. onprem Active Directory domain

***