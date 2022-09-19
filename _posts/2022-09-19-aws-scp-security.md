---
title: AWS Service Control Policies (SCP) uses for the Security Specialty Exam
categories:
- 'Amazon-Web-Services'
feature_image: "https://picsum.photos/2560/600?image=873"
aside: true
---

This is part of a series of posts to use as a study guide for the AWS Security Specialty exam

**What is SCP?**

SCPs are Service control policies.  These are types of organization policies to manage permissions in your organization.  SCPs provide central control over the maximum available permissions that can be provided for all accounts within the organization.  SCPs are used as guardrails for your accounts to stay within the overall access control guidelines.  All features must be enabled within the organization to utilize SCPs.  SCPs cannot be used with consolidated billing.

SCPs set limits and provide guardrails on the actions that an account administrator can delegate to IAM users and roles within accounts.  IAM policies must still be attached by the administrator to grant permissions.  

SPCs have no affect on users or roles within the management account.  They do affect the member accounts within the organization.

**SCP effects on permission**

SCPs are similar to IAM permission policies and use the same syntax.  The major difference is that SCPs NEVER grant permissions.  They are policies that specify maximum permissions for affected accounts.  

Features and permissions for SCPs:
- Affect ONLY IAM users and roles that are managed by accounts that are part of the organization.
- SCP restricts permissions for IAM users and roles in member accounts NOT the management account.  This includes the root user of the member account.
- Users and roles must still be granted permissions with IAM policies.  SCP only applies limits.
- If an IAM permission policy grants access and the action is allowed by SCP, action can be performed.  If the action is not allowed or explicitly denied by the SCP, the action cannot be performed.
- SCPs DO NOT affect any service-linked role.
- When a SCP is disabled, it is detached from the organization.
- When a permission boundary and SCP are present, the action must be allowed by the permission boudary, SCP, and IAM policy.


I hope that you have enjoyed this security overview of managing AWS SCP.




