---
title: RMF Select
categories:
- 'CGRC'
feature_image: "https://raw.githubusercontent.com/captainhyperscaler/captainhyperscaler.github.io/main/images/2023/banner/banner%20logo_without_background.png"
aside: true
---

## NIST Risk Management Framework ##

# RMF Select #


![](/images/cgrc/rmf1.png)

This is the series of articles to use as a study guide for the (ISC)2 CGRC exam.  In this article, we will discuss the Select steps in the Risk Management Framework.

### Select Tasks ###

- S-1 – Control Selection
- S-2 – Control Tailoring
- S-3 – Control Allocation
- S-4 – Documentation of Planned Control Implementation
- S-5 – Continuous Monitoring Strategy - System
- S-6 – Plan Review and Approval

- Primary roles S-1, S-2, S-4, S-5 – CCP and SO
- Primary roles S-3 – Security/Privacy Architect, System Security/Privacy Officer
- Primary role S-6 – AO and AO DR

### Standards and Regulations for Select phase ###

- 800-37 – Guide for RMF
- FIPS 200 – Minimum Security requirements for Federal systems
- 800-18 – Guide for developing Security Plans
- 800-30 – Guide for Risk assessments
- 800-53 – Security and Privacy controls for Federal Systems (Program Management, PII, and Supply Chain control families)
- 800-53B – Control Baseline
- CNSS 1253 – Security Categorization and Control selection
- 800-160 – Systems Security Engineering
- 800-137 – Information Security Continuous Monitoring
- ISO 27001:2013 – ISMS
- ISO 15408:2009 – Common Criteria

### Select Task Details ###

- S-1 – Control Selection
  - Input – security categorization, system component inventory, list of security and privacy requirements, system elements
  - Output – Controls selected for the system and environment of operation
  - Primary role – CCP and SO
  - Related tasks – C-2, P2, P-3, P-4, P-8, P-10, P-14, P-15, P-17
  - SDLC – Development/Acquisition
  - Common baseline catalogs from 800-53B and CNSSI 1253
  - 800-53B control baselines in low, moderate, and high
  - AC-1 – Policy and Procedure
  - AC-2 – Account Management
  - 17 families of security controls
  - CNSSI 1253 – low, moderate, and high baselines based on CIA security objectives

- S-2 – Control Tailoring
  - Input – initial control baselines, risk assessment results (org and system-level), system element information, system component inventory, BIA, risk management strategy
  - Output – list of tailored controls
  - Primary role – CCP and SO
  - Related tasks – S1, P3, P4, P5, P8, P10, P14, P15, P17
  - SDLC – new: development/acquisition
  - Tailoring includes:
    - Identifying common controls
    - Specifying organization-defined values
  - Adding additional controls
    - Providing additional specification to controls
    - Compensating controls – technical
    - Organizational defined parameters – standards and regulations (HIPAA, GDPR, etc)
    - 800-53B control overlays (for tailoring guidance)
  - Provides the opportunity to add or eliminate controls
  - Addresses special requirements or compliance mandates
  - Establishes community-wide parameters
  - Extends supplemental guidance for tailoring

- S-3 – Control Allocation
  - Input – security categorization, enterprise architecture, security and privacy architectures, list of security and privacy requirements, list of common controls
  - Output – List of security and privacy controls allocated to the system, system elements, and environment of operation
  - Primary role – Security/Privacy Architect, System Security/Privacy Officer
  - Related tasks – C1, C2, S1, S2, P3, P5, P10, P14, P15, P16, P17
  - SDLC – initiations
  - Control designations:
    - System specific – applied to the system only
    - Hybrid – Shared between system and common control provider
    - Common – applied by the CCP

- S-4 – Documentation of Planned Control Implementation
  - Input – security categorization, risk assessment results, BIA, risk management strategy, list of selected controls
  - Output – Security and Privacy Plans for the system
  - Primary role – CCP and SO
  - Related tasks – C2, S1, S2, S3, P2, P3, P5, P7, P8, P10, P14, P15, P16, P17
  - SDLC – development/acquisition

- S-5 – Continuous Monitoring Strategy – System
  - Input – organizational risk management strategy, organizational continuous monitoring strategy, org and system-level risk assessments, security and privacy plans, organizational security and privacy policies
  - Output – continuous monitoring strategy for system (including time-based trigger for on-going authorization)
  - Primary role – CCP and SO
  - Related tasks – S4, P2, P3, P7, P14
  - SDLC – development/acquisition

![](/images/cgrc/contmonitor.png)

- S-6 – Plan Review and Approval
  - Input – security and privacy plans, org and system-level risk assessment results
  - Output – security and privacy plans approved by the authorizing official
  - Primary role – AO or AO DR
  - Related tasks – S4, P3, P14
  - SDLC – development/acquisition

The Security and Privacy Plans are created within the select phase. After categorizing information and selecting the controls, it is time to implement those controls.
