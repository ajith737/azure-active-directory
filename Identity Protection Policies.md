# Identity Protection Policies

Azure Active Directory Identity Protection includes **3 default policies** that administrators can enable:
- Azure AD MFA registration policy
- User risk policy
- Sign-in risk policy

## Azure AD MFA Registration Policy
The Azure AD MFA Registration Policy ensures new users have registered for MFA on their first day.
- Multi-factor authentication is a selfremediation method for risk events within Identity Protection that allows users to take action on their own to reduce helpdesk call volume.


## User Risk Policy
- Used to calculate what Identity Protection believes is normal behavior for a user.
- Calculates probability that an identity has been compromised.
- Administrator can make a decision based on this risk score signal.
    - Block access
    - Allow access
    - Allow access / require password change via SSPR
- Users can perform self-service password reset to self-remediate.

## Sign-In Risk Policy
Identity Protection analyzes signals from each sign-in, both real-time and offline.
- Calculates a risk score based on the probability that a specific sign-in wasn't performed by the actual user.

Administrators can choose to:
- Block access
- Allow access
- Allow access but require MFA

## Custom Conditional Access Policy
Administrators can create custom Conditional Access policies that include sign-in risk as an assignment condition. 

***