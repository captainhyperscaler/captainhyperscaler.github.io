---
title: How to Protect Multi-Cloud Identities with Zero Trust in Microsoft 365
categories:
- 'Technical'
feature_image: "https://picsum.photos/2560/600?image=873"
aside: true
---

The traditional way of securing identities does not provide the business agility, user experiences, and protections needed for a rapidly-evolving digital estate. Many organizations are implementing Zero Trust to alleviate these challenges and enable the new normal of working anywhere, with anyone, at any time.

However, the expanded ecosystem of remote users with multiple devices creates more attack surfaces to be exploited. This leads to the potential for an attacker to gain information on a user or device in order to gain access. Zero Trust methods assist in the mitigation of these threats before they become active attacks.

The new model for identity and access increases the flexibility of users and devices to access applications and data, as shown below in Figure 1. In addition, the wide range of devices, applications, and data connected to the Internet creates a broad spread of where identities are located and expands the attack surface for bad actors.

However, user identities today have a strong reliance on usernames and passwords for access to applications. Utilization of multi-factor authentication (MFA) along with conditional access policies help to mitigate some of the risk. Companies should be reviewing and planning ways to optimize identity and access management to decrease or remove the requirement of passwords.

The optimal approach to identity and access management is to utilize the following tips:

Password-less authentication is enabled across all devices and applications.
Devices accessing company applications and resources should be registered with mobile device management (MDM) or mobile application management (MAM) policies.
User, device, location, and behavior are analyzed in real-time to determine risk and deliver ongoing protection
Optimizing identity and access management ensure that users are who they say they are at every access attempt, and regularly reaffirm their trustworthiness. This is the foundation of implementing the Zero Trust methodology.

Enforcing Zero Trust through password-less solutions utilizes MFA to protect your applications with two sources of validation. These sources of validation include something they are (a biometric fingerprint or facial recognition) and something they have (a phone or token) to verify identity before granting access. Note that the something you know (passwords or pin numbers) is taken out of the MFA scenario. With several authentication methods available, admins can choose the one that best fits their users’ workflow.

Microsoft has solutions within its identity and access management platform for password-less authentication.

“Password-less” Microsoft MFA credentials include:

Microsoft Authenticator: For the greatest flexibility, convenience, and cost, we recommend using the Microsoft Authenticator mobile app. Microsoft Authenticator supports biometrics, push notifications, and one-time passcodes for any Azure AD-connected app. It’s free to download from the Apple and Android app stores.
zero trust identity protection
Windows Hello: For a great built-in experience on the PC, we recommend using Windows Hello. It uses your face or fingerprint to sign in automatically.
Fast Identity Online (FIDO2) security keys are now available from several vendors like Yubico, Feitian Technologies, and HID Global in a USB, NFC-enabled badge, or biometric key. FIDO2 is an open standard for password-less authentication.
Additional information on Microsoft’s password-less authentication options can be found here.

Many companies have been forced to move away from the traditional and into the more modern identity and access management methods.  Though these companies are still not in the fully optimized category, they can still begin to move in that direction by enforcing MFA for all users and plan for additional Zero Trust methods of verification with conditional access and Identity Protection policies. The following section will provide you with a better understanding around implementing a Zero Trust framework.

The Zero Trust Framework
A sharp focus on Identity and Access Management comes up as the two fundamental control planes within this framework, the identities themselves, and the governance used to monitor and manage access to resources. Microsoft has addressed these control planes through the Microsoft Entra product family.

Let’s look at how the identity control plane can be used within the Zero Trust framework.

Identity
Identities, whether they represent people, services, or IOT devices, define the Zero Trust control plane. When an identity attempts to access a resource, we need to verify that identity with strong authentication, ensure access is compliant and typical for that identity, and follow privilege access principles.

Azure Active Directory (Azure AD) is Microsoft’s service for providing cloud identity to users, groups, and resources. Azure AD is used as the cloud provider for cloud-native users and resources for access to cloud applications. Azure AD can be used as the identity provider for third-party SaaS applications as well as on-premises applications that’re registered in Azure AD. Azure AD provides features to secure identities against password attacks and can enforce additional Zero Trust capabilities. These Zero Trust capabilities include strong passwords, multi-factor authentication (MFA), passwordless authentication, and conditional access policies.

mfa

Azure AD Identity Protection can be used in parallel with conditional access policies to recognize user and sign-in risks.  Within Azure AD Identity Protection, risks are the potential that a user’s identity has of been compromised or stolen, or that a sign-in is not being executed by the user that the credentials belong to. These risk levels are based on typical user and tenant behavior with Microsoft’s machine learning and artificial intelligence solutions flagging users and sign-ins that fall outside of normal behavior. Conditional access policies can then enforce additional verification steps such as MFA, require a password reset, or block access.

It’s critical that only the right people with the right resources on secure devices can access your data from anywhere. Microsoft Conditional Access is an intelligent policy engine built for ensuring this. Its robust controls allow you to define specific conditions for how users authenticate and gain access to apps and data. You can customize and manage automated policies and get reporting on the policies applied for each sign-in.

Closing Thoughts
As should be the case with any cloud security journey, planning and education are key areas to success. Users must be educated to manage change and provide understanding about the importance of this Zero Trust methodology and the protection of their identity.  Managing change and planning for potential gaps in security controls and assessing risks will allow you to execute a strong level of identity protection for users, devices, and resources within your cloud and hybrid environments.

This was originally posted here: <https://www.avepoint.com/blog/protect/zero-trust-identity-protection>