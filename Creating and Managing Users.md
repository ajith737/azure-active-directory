# Creating and Managing Users

- Azure account is needed to access Azure resources
- Users are authenticated using their accounts
    - Allows users to sign on
- Once authenticated, Azure AD will authorize the user
    - Determines what resources that user can access

## Defining Users in Azure AD
Users in Azure Active Directory can be defined in THREE ways:
- Cloud Identities
- Directory Synchronized Identities
- Guest Users

## Cloud Identities
Show up in the Azure AD Portal as Azure Active Directory users or External Azure Active Directory users.
- Members of local Azure AD = Azure Active Directory users
- Users defined in another Azure AD = External Azure AD users

- Cloud Identities show up in the Azure AD Portal as **Azure Active Directory** users or **External Azure Active Directory users**.
- Members of local Azure AD are called Azure Active Directory users.
- Users defined in another Azure AD are called External Azure AD users.

## Directory Synchronized
Identities Directory Synchronized Identities show up in the Azure AD Portal as Windows
**Server AD** users.
- Users that have been synchronized to Azure AD from an on-prem active directory via Azure AD connect.

## Guest Users
Guest users are Azure AD users that exist outside of the Azure Active Directory.
- Guest users are accounts in Azure AD from other cloud providers.
- Users with Microsoft accounts.
- Will show up in the Azure AD users list as **invited users**.

## Adding Cloud Identities to Azure AD
Several ways to add cloud identities in Azure Active Directory
- Sync users from an on-prem Active Directory
- Use the Azure portal to manually add new users
- Use the command line
    - Azure PowerShell
    - Azure CLI
- Create users from a CSV file in PowerShell
- Azure AD graph API
- Office 365 admin center
- Microsoft InTune admin console

***