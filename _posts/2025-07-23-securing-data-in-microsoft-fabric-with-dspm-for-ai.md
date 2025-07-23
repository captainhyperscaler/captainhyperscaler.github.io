---
title: Microsoft Purview - Securing Data in Microsoft Fabric with DSPM for AI
categories:
- 'Technical'
feature_image: "https://raw.githubusercontent.com/captainhyperscaler/captainhyperscaler.github.io/main/images/2023/banner/banner%20logo_without_background.png"
aside: true
---

# 🔐 Securing Data in Microsoft Fabric with DSPM for AI

As organizations embrace AI-driven insights across platforms like Microsoft Fabric, the need for robust data protection becomes paramount. Microsoft Purview’s **Data Security Posture Management (DSPM) for AI** offers a centralized, intelligent approach to securing sensitive data across Copilot experiences, enterprise AI apps, and third-party generative AI tools.

## 🧠 What Is DSPM for AI?

DSPM for AI is a Microsoft Purview solution that:
- Provides **visibility into AI interactions** across Microsoft 365 Copilot, Fabric Copilot, and third-party AI apps.
- Detects **risky prompts and responses**, including oversharing of sensitive data.
- Enables **one-click policies** to enforce data loss prevention (DLP), sensitivity labeling, and ethical AI usage.
- Supports **compliance mapping** with frameworks like NIST AI RMF.

## 🛠️ Installing Microsoft Fabric Extensions

To manage and develop Fabric artifacts securely, install the following **Visual Studio Code extensions**:

### 1. **Microsoft Fabric (Preview) Extension**
- Access and manage Fabric workspaces directly in VS Code.
- Create, rename, and edit Fabric items like notebooks and pipelines.
- [Install from Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=fabric.vscode-fabric)

### 2. **Fabric Data Engineering Extension**
- Develop for the Lakehouse platform using Spark and Python.
- Supports local debugging and publishing to Fabric.
- [Install from Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=SynapseVSCode.synapse)

### 3. **Optional Docker Setup**
- Use VS Code Dev Containers for a preconfigured environment.
- Includes JDK, Conda, and Jupyter support for seamless development.

## 👥 Onboarding Accounts and Devices

To enable DSPM for AI and secure interactions with third-party AI apps, follow these onboarding steps:

### 1. **Enable Microsoft Purview Audit**
- Required for capturing AI prompts and responses.
- Enabled by default for new tenants.

### 2. **Onboard Devices to Microsoft Purview**
- Necessary for endpoint DLP and AI site monitoring.
- Use Microsoft Defender or Intune to enroll devices.

### 3. **Deploy Microsoft Purview Browser Extension**
- Required for detecting visits to AI sites like ChatGPT or Gemini.
- Supports Chrome, Edge, and Firefox.

### 4. **Assign Roles and Permissions**
- Use Microsoft Entra ID to assign the **Compliance Administrator** role.
- Create **workspace identities** to securely authenticate Fabric items with external resources.

## 🧩 Activating DSPM for AI in Microsoft Fabric

Once prerequisites are met:
1. Go to **Microsoft Purview Portal > Solutions > DSPM for AI**.
2. Enable one-click policies such as:
   - Capture interactions for Copilot in Fabric.
   - Detect sensitive info shared with AI via network.
   - Block risky prompts from elevated-risk users.
3. Review **Reports** and **Activity Explorer** to monitor AI usage and data exposure.

## ✅ Final Thoughts

Microsoft Fabric’s integration with DSPM for AI empowers organizations to adopt AI responsibly—balancing innovation with governance. By installing the right extensions and onboarding accounts and devices, security teams can proactively detect risks, enforce compliance, and protect sensitive data across the AI landscape.


