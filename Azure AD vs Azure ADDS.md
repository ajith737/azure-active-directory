# Azure AD vs Azure AD DS
Azure Active Directory and Azure AD domain services share common names and technologies but are really are two different offerings that are designed to provide different services.

## Azure Active Directory
- Azure Active Directory is a cloud-based identity and mobile device managemnet solution.
- Provides user account and authentication services.
- Synchronize traditional on-prem AD to Azure AD to provide a single identity solution.

## Azure AD Domain Services
Azure AD Domain Services is a fully managed domain services offering.
- Includes a fully-compatible subset of features found in a traditional AD
    - Domain Join
    - Group Policy
    - LDAP
    - Kerberos & NTLM Authentication
- Integrates with Azure AD
- Can be synchronized with Azure AD

## Azure AD Features
- Azure AD allows users to registers their personal devices with the directory.
    - Creates identities for devicces that can be authenticated by Azure AD.
    - Device managemnet is performed via MDM software like Microsoft InTune.
- Computers & laptops can be joined to Azure AD
    - Provides the same benefits as registring personal devices with Azure AD.
    - Secure applications with single sign-on.
    - Leverage eterprise policy compliant roaming of user settings across different devices.

## Azure AD vs Azure AD DS

- When a user with an Azure AD joined for Azure AD register device authenticates, that authentication is performed via modern OAuth or Open ID connect based protocols.

However..
- When a user authenticates from a Azure AD domain services joined device, applications can user Kerberos and NTLM protocols for authentication instead.

![6](6.PNG)

***