# 📚 OSCAL Content: Your Central Hub for Compliance

[![OSCAL](https://img.shields.io/badge/OSCAL-Content-blue?style=for-the-badge&logo=github)](https://github.com/ComplianceAsCode/oscal-content)
[![Red Hat](https://img.shields.io/badge/Focus-Red%20Hat-red?style=for-the-badge&logo=redhat)](https://www.redhat.com/)
[![Automation](https://img.shields.io/badge/Powered%20by-GitHub%20Actions-green?style=for-the-badge&logo=github-actions)](https://github.com/features/actions)

---

## 🌟 Overview

This repository is your **go-to place** for managing and storing security compliance content in the **Open Security Controls Assessment Language (OSCAL)** format. Our primary focus is on **Red Hat (RH)** products.

> 🎯 **Purpose**: Centralized hub for OSCAL compliance content management and synchronization

---

## **Mastering the Recipe: A Compliance-as-Code Analogy 🍮📚**

Let's imagine the relationship between `ComplianceAsCode/oscal-content` and `ComplianceAsCode/content` using a delicious analogy.

### **The First-edition Cookbook: ComplianceAsCode/content**

**Think of `ComplianceAsCode/content` as your definitive, first-edition cookbook for all things compliance.** It contains the foundational, approved recipes (compliance rules, policies, benchmarks) for every aspect of your organization's security posture. This is the **source of truth** for all compliance endeavors.

### **The Specialized Cookbook: ComplianceAsCode/oscal-content**

**Now, imagine ComplianceAsCode/oscal-content as a specialized companion cookbook.** It's built directly from the First-Edition Cookbook but focuses specifically on the "Creme Brûlée" section – representing the OSCAL (Open Security Controls Assessment Language) format.

This specialized book contains only the creme brûlée recipes, ensuring they are always up-to-date with the First-edition Cookbook, even as the original recipes evolve. It's designed for those who need to work exclusively with the OSCAL format, building upon the foundational recipes while maintaining perfect synchronization.

### **The Culinary Coordinators: GitHub Actions & complyscribe 🧑‍🍳✨**

**GitHub Actions are your tireless team of culinary coordinators, and complyscribe is their specialized chef.** Their combined job is to ensure that any improvements or updates to the creme brûlée recipe – whether in the First-edition Cookbook or the Specialized Cookbook – are perfectly synchronized and reflected in both.

**Here's how they work:**

* **First-edition Cookbook Update:** When you refine the creme brûlée recipe in the First-edition Cookbook, your Culinary Coordinators (GitHub Actions) spring into action. They use complyscribe as their expert chef to automatically translate and update the Specialized Cookbook (ComplianceAsCode/oscal-content). This ensures that your friend, who relies on the specialized OSCAL version, always has the latest and greatest recipe.  
* **Specialized Cookbook Discovery:** If your friend discovers a more efficient way to caramelize the sugar (a new OSCAL implementation or refinement), the Culinary Coordinators (GitHub Actions) ensure this valuable insight is shared back and incorporated into the First-edition Cookbook.  
* **Constant Harmony:** This automated synchronization, powered by GitHub Actions and `complyscribe`, means you and your friend are always working from the most refined and complete creme brûlée instructions. GitHub Actions act as the automated bridge, with `complyscribe` handling the crucial conversion process, ensuring consistent, high-quality "compliance creme brûlée" across both repositories.

In essence, GitHub Actions automate the collaboration, and complyscribe facilitates the specific conversion and synchronization, ensuring that the specialized OSCAL content (oscal-content) remains perfectly aligned with the comprehensive compliance content (content), and vice versa, leading to a consistently delicious (and compliant\!) final product.

## Visual Representation

```mermaid
flowchart LR
ComplianceAsCode/content --> complyscribe --> ComplianceAsCode/oscal-content 
ComplianceAsCode/content --> ComplianceAsCode/oscal-content
ComplianceAsCode/oscal-content --> change --> sync-oscal-cac --> ComplianceAsCode/content
ComplianceAsCode/content --> change --> sync-cac-oscal --> ComplianceAsCode/oscal-content
```

- **`ComplianceAsCode/content`:** first-edition-cookbook
- **`ComplianceAsCode/oscal-content`:** specialized-cookbook
- **`complyscribe`:** specialized-chef
- **`sync-oscal-cac`** & **`sync-cac-oscal`:** culinary-coordinators

```mermaid
flowchart LR
first-edition-cookbook --> specialized-chef  --> specialized-cookbook 
first-edition-cookbook --> specialized-cookbook
specialized-cookbook --> change --> culinary-coordinators --> first-edition-cookbook
first-edition-cookbook  --> change --> culinary-coordinators --> specialized-cookbook
```

## 🚀 Automated Content Sync

Initialized by [**complyscribe**](https://github.com/complytime/complyscribe), this repository features powerful GitHub Actions designed for seamless content synchronization:

### 🔄 Sync Workflows

| Workflow             | Direction       | Purpose                                       | Source                                                                  |
|----------------------|-----------------|-----------------------------------------------|-------------------------------------------------------------------------|
| **`sync-comp`**      | ➡️ **Inbound**  | Generate OSCAL content from ComplianceAsCode  | [ComplianceAsCode/content](https://github.com/ComplianceAsCode/content) |
| **`sync-controls`**  | ➡️ **Inbound**  | Generate OSCAL controls from ComplianceAsCode | [ComplianceAsCode/content](https://github.com/ComplianceAsCode/content) |
| **`sync-oscal-cac`** | ⬅️ **Outbound** | Sync OSCAL updates back to ComplianceAsCode   | [ComplianceAsCode/content](https://github.com/ComplianceAsCode/content) |

### 🔄 Bidirectional Synchronization

> **`sync-oscal-cac`** and **`sync-cac-oscal`** create a powerful **two-way synchronization**, ensuring both projects stay updated with each other's content changes.

---

## ⚙️ How Content Synchronization Works

> ⚠️ **Development Status**: These CI systems are currently in active development. We're refining the user experience based on ongoing feedback.

### 📥 From ComplianceAsCode to OSCAL

**Workflow**: `sync-cac-oscal` transforms content from ComplianceAsCode/content into OSCAL format using the complyscribe CLI.

#### 🔄 Process Steps

| Step  | Action                 | Description                                                            |
|-------|------------------------|------------------------------------------------------------------------|
| **1** | 🔍 **Detect Changes**  | Identifies updates in source content (controls, profiles, rules, vars) |
| **2** | 🛠️ **Prepare**        | Gathers necessary arguments for Complyscribe                           |
| **3** | 🔄 **Transform**       | Runs complyscribe to convert source files into OSCAL                   |
| **4** | 📝 **Propose Updates** | Automatically creates a Pull Request with new OSCAL content            |

#### 📊 Real Example

```mermaid
graph LR
    A[ComplianceAsCode PR #13580] --> B[Workflow Triggered]
    B --> C[Content Transformation]
    C --> D[OSCAL Content PR #28]
```

**Live Example**: 
- ComplianceAsCode merge: [PR #13580](https://github.com/ComplianceAsCode/content/pull/13580)
- Triggered workflow: [Successful run](https://github.com/ComplianceAsCode/content/actions/runs/15688668981/job/44198205023)
- Generated OSCAL PR: [PR #28](https://github.com/ComplianceAsCode/oscal-content/pull/28)

---

### 📤 From OSCAL to ComplianceAsCode

**Workflow**: `sync-oscal-cac` handles reverse sync, reflecting OSCAL content updates back into ComplianceAsCode/content.

#### 🔄 Process Steps

| Step  | Action                        | Description                                                                |
|-------|-------------------------------|----------------------------------------------------------------------------|
| **1** | ⚡ **Trigger**                 | Activated upon merging PR with OSCAL file changes                          |
| **2** | 🔍 **Detect Updates**         | Identifies updated OSCAL files (catalogs, profiles, component-definitions) |
| **3** | 🔄 **Sync with ComplyScribe** | Transforms OSCAL updates back into standard formats                        |
| **4** | 📝 **Create Upstream PR**     | Automatically creates PR in ComplianceAsCode/content                       |

#### 📊 Real Example

```mermaid
graph LR
    A[OSCAL Content PR #33] --> B[Workflow Triggered]
    B --> C[Content Transformation]
    C --> D[ComplianceAsCode PR #13617]
```

**Live Example**:
- OSCAL content merge: [PR #33](https://github.com/ComplianceAsCode/oscal-content/pull/33)
- Triggered workflow: [Successful run](https://github.com/ComplianceAsCode/oscal-content/actions/runs/15841883094/job/44656004616)
- Generated ComplianceAsCode PR: [PR #13617](https://github.com/ComplianceAsCode/content/pull/13617)

---

## 🎥 Demo Recordings

### 📺 Watch the Workflows in Action

| Workflow             | Demo                                                                                    | Description                                      |
|----------------------|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| **`sync-oscal-cac`** | [📹 Watch Demo](https://drive.google.com/file/d/1ZOc-H4f5zG_NCf_5rEuQMSwMZ52PkFzY/view) | OSCAL Content changes → ComplianceAsCode/content |
| **`sync-cac-oscal`** | [📹 Watch Demo](https://drive.google.com/file/d/1rvRlNkCzlvTh7NIC9JCKNIkiJCxW_S3W/view) | ComplianceAsCode/content changes → OSCAL Content |

---

## 🛠️ Tooling

We utilize [**ComplyScribe**](https://github.com/complytime/complyscribe) to help author and manage OSCAL content, ensuring adherence to required standards and formats.

### 🎯 Why ComplyScribe?

| Feature                    | Benefit                                   |
|----------------------------|-------------------------------------------|
| **📝 Content Authoring**   | Simplified OSCAL content creation         |
| **✅ Standards Compliance** | Ensures adherence to OSCAL specifications |
| **🔄 Format Management**   | Consistent content formatting             |
| **🤖 Automation Ready**    | Seamless CI/CD integration                |

---

## 🔍 Why Review `ComplianceAsCode/oscal-content`?

> 💡 **Key Insight**: The `ComplianceAsCode/oscal-content` repository is the **same concept** as your own `oscal-content-demo` repository.

### 🎯 Future Vision

**This repository will eventually be maintained by Compliance Managers**, providing:

- **Centralized Content Management**: Single source of truth for OSCAL content
- **Automated Synchronization**: Seamless updates between systems
- **Collaborative Workflows**: Team-based content authoring and review
- **Scalable Architecture**: Growing with organizational needs

---

## 🤝 Contributing

### 🚀 How to Contribute

**Maintainers** can contribute by:

1. **Fork**: Create a fork of the repository
2. **Author/Edit**: Modify OSCAL content files
3. **Pull Request**: Open a PR with your changes
4. **Auto-Sync**: Once merged, `sync-oscal-cac` workflow triggers automatically

### 📋 Contribution Workflow

```mermaid
graph LR
    A[Fork Repository] --> B[Edit OSCAL Content]
    B --> C[Create Pull Request]
    C --> D[Review & Merge]
    D --> E[Auto-Sync Triggered]
```

---

<div align="center">

### 🚀 Ready to Manage OSCAL Content?

**Transform your compliance workflow with automated OSCAL synchronization!**

[![Get Started](https://img.shields.io/badge/Get%20Started-Repository-blue?style=for-the-badge&logo=github)](https://github.com/ComplianceAsCode/oscal-content)
[![ComplyScribe](https://img.shields.io/badge/Learn-ComplyScribe-green?style=for-the-badge&logo=github)](https://github.com/complytime/complyscribe)

</div>

---

> 🔄 **Automation**: Bidirectional sync ensures your compliance content stays consistent across all platforms!
