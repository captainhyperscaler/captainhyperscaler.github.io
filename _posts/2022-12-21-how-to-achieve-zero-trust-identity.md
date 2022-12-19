---
title: How to Achieve Zero Trust Identity Protection with Microsoft Entra
categories:
- 'Technical'
feature_image: "https://picsum.photos/2560/600?image=873"
aside: true
---

Apply Zero Trust to Identity
When you apply Zero Trust to your identity and access management strategy, you should have a plan in place. This planning includes the deployment objectives, federation with multi-cloud and on-premises identity providers and systems, applying policies for conditional access, and security operations that will remediate issues and review analytics for gaps in controls.

Let’s review the objectives for the deployment of Zero Trust for identity and access.

Deployment Objectives
A proper and successful deployment requires proper planning and preparation with business and user stakeholders. Without having clear communication with the business on their objectives for identity and access protection and governance, you may fall short of compliance requirements that the company needs to adhere to for privacy and protection of personally identifiable information (PII). The business is going to be concerned with both financial and reputational damage that could be caused by an identity breach.

Users need to be kept in communication regarding any changes in how they may access applications, systems, and data. They should be given the reason for any additional controls, such as MFA, before they are implemented. Without user understanding and recognition, the change management process for implementing a new control could be delayed through a lack of user adoption.

change management

There are many tasks and areas of focus to consider when planning for deployment. A partial list is included here:

Cloud identity federates with on-premises identity systems.
Conditional Access policies gate access and provide remediation activities.
Analytics improve visibility into potential vulnerabilities and threats.
Identities and access privileges are managed with identity governance.
User, device, location, and behavior are analyzed in real-time to determine risk and deliver ongoing protection. Real-time analysis is critical for determining risk and protection.
Integrate threat signals from other security solutions to improve detection, protection, and response. Other security solutions can be integrated for greater effectiveness.
All your users and apps are connected so you can extend the benefits of Single Sign-On to your users while improving your security posture. Maintaining a healthy pipeline of your employees’ identities and the necessary security artifacts (groups for authorization and endpoints for extra access policy controls) puts you in the best place to use consistent identities and controls in the cloud.
Your identities are verified with strong authentication. Identity is the front door. Strong authentication is the single most important change we can take.
Access is controlled with smart risk assessment to move past rigid, static rules that hinder productivity and can’t leverage all of the great signals your environment generates.
Access is enforced with strong governance to ensure users only get access to what they need, lowering the risk of bad actors abusing credentials.
The next section will discuss how to apply Zero Trust to a federated identity infrastructure with multi-cloud and on-premises applications to access.

zero trust

Federating Identity for Multi-Cloud and On-Premises Systems
The modern identity and access infrastructure expands beyond an on-premises infrastructure or even a single cloud infrastructure. Users are accessing a variety of applications on different platforms with their own identity and access management databases. These platforms include:

Software as a Service (SaaS) applications – Office 365, LinkedIn, Twitter, Facebook
Multi-cloud providers – Microsoft Azure, Amazon Web Services, Google Cloud Platform
On-premises applications – Line of business applications, Windows Active Directory
These different identity databases and identity providers create challenges to identity and access management, monitoring, and governance. You need to ensure users are who they say they are at every access attempt and regularly reaffirm their trustworthiness. Putting in place a federated trust relationship to these applications and providers allows us to enforce Zero Trust. This federated relationship allows you to enforce solutions such as MFA to protect your applications and to verify identity before granting access in the same way that users in the tenant verify identity. The user experience is simplified through the SSO capabilities that Microsoft provides. Microsoft provides the capability of building trusted relationships between Azure AD tenants and other cloud identity providers using external identities and cross-tenant access settings within Azure AD.

Figure 2 shows the integration of SaaS, on-premises, and multi-cloud connections into the Microsoft cloud.

zero trust policy
Figure 2 – Multi-cloud and Hybrid identity federation.
For partner users or single users that require access to resources for collaboration, external identities can be assigned while still being governed by Zero Trust.

Transform Management of External Identities
External identities are users that are not within the company tenant but need to collaborate with the member users in the tenant. Users are invited to the tenant and can use their own credentials to access Microsoft resources. This could be using their own Azure AD as the identity provider or another SAML-based identity provider (e.g. Facebook or Google).

You don’t have full control over the authentication methods and identity verification of these external users. You may not have the same level of control to enforce MFA for these users. In order to establish guardrails around the external identities, you’ll want to manage them through entitlements and access reviews.

Entitlements, or Permissions Management within Microsoft Entra, provide an establishment of a catalog of resources that an external identity has access to for a particular project or partner interaction. Within the governance of these permissions, there are defined access reviews for external identities to verify their continued need for access to resources. These access reviews should be completed by a member user within your tenant and not a self-review by the external users. This continued review and auditing of external users and their access rights to your company resources assist in the enforcement of Zero Trust within identity and access management.

Additional verification and enforcement for external identities and internal users can be applied through Conditional Access policies to protect against potential malicious activities involving sensitive information by external users. The next section will discuss this in more detail.

access management

Applying Conditional Access and Remediations
Microsoft Conditional Access gives you the power to enforce the core principle of Zero Trust—never trust, always verify. The Zero Trust security model relies on a security policy engine to make access decisions you can enforce throughout the digital estate. It enables organizations to fine-tune access policies based upon contextual factors such as user, device, location, app permissions, data sensitivity, session risk information, and more. That gives you better control over how users access corporate resources. You can then use additional challenges such as MFA, Terms of Use, or access restrictions to decide whether to allow, deny, or control access.

The Zero Trust security model relies on a security policy engine to make access decisions you can enforce throughout the digital estate. It enables organizations to fine-tune access policies based upon contextual factors—such as user, device, location, app permissions, data sensitivity, session risk information, and more. Within Microsoft, this policy engine is available through Conditional Access.

Conditional Access policies are available within Azure AD, Identity Protection, and Microsoft Defender for Cloud Apps to enforce Zero Trust verification based on the user risk, device risk, location risk, type of application, sensitivity of the data being accessed, and other triggers.

Figure 3 shows the workflow of Conditional Access policies in a Zero Trust methodology.

zero trust
Figure 3 – Conditional Access policy workflow.
Conditional access policies look at the status of a user, device, location, application, or website at the time that it is being accessed and determines whether additional verification is required. Something to note is that this verification takes place even if the user has previously authenticated and used MFA. Therefore, you should still have MFA enforced to all users as a first step. Conditional Access policies take this MFA enforcement an additional step as a user accesses company resources from another location or from other devices.

Closing Thoughts
Proper planning and stakeholder interaction are important to successfully implementing Zero Trust through Conditional Access policies and MFA. Correctly planning and defining how these policies will be enforced will avoid locking users out of systems that they require access to. Conditional Access policies can be tested with the What if functionality within the portal to provide a level of understanding as to how the policies will affect users, groups, and devices.

This was originally posted here: <https://www.avepoint.com/blog/protect/zero-trust-microsoft-entra>