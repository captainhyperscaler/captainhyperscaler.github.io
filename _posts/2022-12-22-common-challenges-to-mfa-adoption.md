---
title: Common Challenges to MFA Adoption and Enforcing Protection With Conditional Access
categories:
- 'Technical'
feature_image: "https://picsum.photos/2560/600?image=873"
aside: true
---

Modern authentication utilizing Identity Providers within the cloud creates a unique set of challenges. The most apparent of these is that users are utilizing their personal or work email addresses across multiple websites and applications on the public Internet. This is generally done without a complete understanding of where these identities are stored and who has access to them.

In addition to the sprawl of email addresses as the primary form of identification, most users utilize the same password for multiple sites within multiple geographies. This scenario creates the potential for identity theft and, if it is a work email address, potential identity breach and data theft. This article will provide some options for adopting multi-factor authentication and protecting identities with Conditional Access.

**Multi-Factor Authentication**
Multi-factor authentication, or MFA, addresses the potential of a password to be compromised by requiring the user requesting access to provide an additional form of identification before they are authenticated and authorized access. There are three forms of identification that are used for MFA, and MFA is configured to require any two of these three factors to verify a user’s identity. The three forms are:

- Something you know
- Something you have
- Something you are
Let’s look at each of these in more detail by defining each and giving some examples of how they’re used.

**Conditional access**

Something You Know
Something you know is a form of identification that you provide from your memory. This is in many cases your password. It could also be a personal identification number (PIN) or the answer to a security question. In most systems for verification, this is usually the primary form of verification and then the second form is one of the next two options.

Something You Have
Something you have is probably the most difficult to comprehend at times. This factor requires something physically in your possession to verify your identity. In most cases, this generally is a cell phone that you have identified when enrolling into the MFA service. On that cell phone, you can then be provided ways to verify your identity through a code being sent via text message, a phone call to that cell phone number, a code within an authenticator app on the phone, or pushing an approval notification through the authenticator app. In addition to a cell phone being something that you have, some companies may provide a separate token-generating device that rotates a code every few minutes.

Secure your M365 collaboration with a Zero Trust framework. Request a demo today.
Something You Are
Something you are is when some form of biometrics is used as the second factor for verification.  Usually, the most popular use here is fingerprints or facial recognition. To use this factor, the devices being used must be equipped with the capability to provide and process this information. This is a more complex factor than the other two and may not be technically or financially feasible for a company that has older systems. However, many new systems have these capabilities built in, such as Windows 10 and Apple or Android smartphones.

Figure 1 shows how these three factors can work together to provide the verification of user identities for authentication.

mfa authentication

Utilizing MFA for users addresses the challenge of a compromised username and password. If enabled and enforced correctly, MFA will protect against almost all identity attacks. Unfortunately, there are challenges to using MFA. Let’s discuss some of these and how to mitigate and remediate the challenges.

User Adoption
Probably the number one challenge to having MFA properly utilized across an organization is user adoption. Depending on the process and procedures for enabling MFA, users may be slow to adopt the use of MFA and in some cases, avoid it or find workarounds. Workarounds to MFA may be to use other applications (or Shadow IT) rather than sanctioned company applications that require MFA for access.  Companies have the ability within identity providers and applications to enforce MFA for all users, which is a recommended practice. However, if this enforced MFA creates a perceived difficulty in gaining access to an application, users will still fight the process. This creates vulnerabilities to the organization.  Proper change control processes and communications with the users within the organization can assist with this challenge. Proper planning and implementation can also assist.

Proper Implementation
As stated, proper planning and implementation is a way to address the user adoption challenge.  However, other challenges are created if implementation is not done properly and does not communicate with the user environment. The MFA implementation should account for the user experience as well as the level of security within the implementation.

For example, making a user access a one-time expiring code that is sent through SMS with a timeout that is too short to retrieve the code and enter it will create a frustrating user environment. A more user-friendly implementation would be to send a push notification to an authentication app behind a fingerprint or facial identification software. The user only needs to select “yes” to verify their identity and the process is much more streamlined. This also addresses another challenge of social engineering being utilized to compromise someone’s identity.



**Man-in-the-Middle and Social Engineering**
MFA fatigue has caused users to become careless about identity and access management. As was stated in the previous section, proper implementation is key. We have seen recent attacks where someone misrepresenting themselves as an IT resource has gained access to company resources by calling a user and social engineering them into providing both their password AND their MFA code.

This can be further addressed and remediated with a push notification response, but also proper education about man-in-the-middle attacks such as this. Also, NEVER trust a caller that says that they are from your IT department. Ask their name and reach out to verify that this person is within your organization.  Microsoft recently announced some ways to address potential identity threats through authentication strength within conditional access policies.

**Applying Conditional Access Remediations**
Conditional access policies are available within Azure AD, Identity Protection, and Microsoft Defender for Cloud Apps to enforce Zero Trust verification based on the user risk, device risk, location risk, type of application, sensitivity of the data being accessed, and other triggers.


**MFA adoption**

Conditional access policies look at the status of a user, device, location, application, or website at the time that it is being accessed and determines whether additional verification is required. Something to note is that this verification takes place even if the user has previously authenticated and used MFA. Therefore, you should still have MFA enforced to all users as a first step. Conditional access policies take this MFA enforcement an additional step as a user accesses company resources from another location or from other devices.

Proper planning and stakeholder interaction is important to successfully implementing Zero Trust through Conditional access policies. Correctly planning and defining of how these policies will be enforced will avoid locking users out of systems that they require access. Conditional access policies can be tested with the What if functionality within the portal to provide a level of understanding as to how the policies will affect users, groups, and devices.

Sign-in activity can also be reviewed to determine if users are being blocked from accessing resources. Periodically reviewing these activity logs can assist in identifying potential malicious activity and also false positives in failed login attempts that may require a review of Conditional Access policies.

More information on accessing activity logs can be found here: How To: Access activity logs in Azure AD.

This continuous review and auditing of activity, along with access reviews to monitor and manage the governance of identity and access, can expose potential gaps in Zero Trust to address. The next section will discuss additional tools that can be used to bring this together.

**Conditional access**

Analytics to Bridge Gaps
As discussed in the previous sections on federation, external identities, and conditional access policies, the governance and continuous auditing and assessing of an identity and access management environment is important. These reviews verify the need for users to have access to resources, potential vulnerabilities, and risks on users and devices, as well as activity anomalies within the environment.

The tools that are provided within Microsoft Entra for Permission management provide governance to resources within the catalog and access packages for internal and external groups to collaborate. Azure AD Identity Protection continuously monitors login activity and identifies when potentially malicious activity may be taking place. Reviewing these activities is necessary for an identity and access management administrator to understand areas of concern and gaps within the enforcement of Zero Trust.

The Microsoft Entra admin center provides a full set of tools to review the identity and access management environment to determine these potential gaps.

**Closing Thoughts**
There are many different challenges and remediations for identity and access management within the cloud. Even though enforcing MFA can become a challenge, proper planning and communication to the users can make it very successful in protecting user and company information. Identity is the primary perimeter of protection within a cloud ecosystem, and you should do everything that you can to protect it. MFA is the first option and provides a low-cost solution to protect against identity theft. Just be sure that you take the proper precautions and address user objections prior to enforcement.

This was originally posted here: <https://www.avepoint.com/blog/protect/mfa-adoption-conditional-access>