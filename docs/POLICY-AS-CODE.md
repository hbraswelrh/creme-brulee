# 📋 Policy as Code

---

## 🔍 What is it?

**Policy as Code** defines, updates, shares, and enforces policies using code, enabling automated compliance and governance across your infrastructure.

> 💡 **Learn more**: [Policy as Code Automation](https://www.redhat.com/en/blog/policy-as-code-automation)

---

## 🎯 Goals

### 🔧 Core Objectives

- **Integration**: Integrate compliance frameworks and existing policy engines
- **Flexibility**: Enable usage of heterogeneous policy engines in compliance check operations
- **Community**: Community-driven plugin extension

### ✨ Key Benefits

> 🎛️ **Flexibility** in choice of policy engines and compliance frameworks

> 🌍 **Community driven** plugin extension

---

## 🧩 Breakdown

### 📖 Definition

**Policy** is a rule, condition, or instruction that governs operations or processes. It's defined as a set of rules or guidelines for an organization, people, or process to achieve compliance, standards, or consistency.

### 🎯 Focus Areas

- **Evidence-Based**: Less discussion of measures, more machine-readable evidence of compliance
- **Automation**: Common examples include testing automation scripts to ensure defined policies are properly enforced

---

## 🛠️ Policy Engines

### 🚀 Popular Tools

| Engine | Description | Use Case |
|--------|-------------|----------|
| **[Kyverno](https://kyverno.io/docs/introduction/)** | Policy engine for Kubernetes resources | Kubernetes governance |
| **[Auditree](https://auditree.github.io/)** | GitOps tool for evidence collection and verification | Cloud services via APIs |

---

## 🏗️ Projects that Exemplify Policy as Code

The **`compliance-to-policy`** projects aim to bridge the gap between **Compliance as Code** and **Policy as Code**.

### 🔗 Key Relationship

```
Compliance As Code = OSCAL
Policy As Code = used by Policy Validation Points (PVP)
```

---

## 🔄 C2P Workflow

### 📋 Process Overview

| Step | Process | Description |
|------|---------|-------------|
| **1** | 🚀 **Initialization** | C2P runs in GitOps Pipeline, Kubernetes controller, or Python/Go environment |
| **2** | 📥 **Input** | C2P receives Compliance as Code → OSCAL Component Definition mapping controls and policies |
| **3** | 🔧 **Policy Generation** | C2P generates policies through plugins for each policy engine |
| **4** | 📤 **Delivery** | Policies get delivered to the policy engines |
| **5** | 📊 **Collection** | Results are collected from policy engines |
| **6** | 📈 **Aggregation** | C2P aggregates results by controls through engine-specific plugins |
| **7** | 📋 **Assessment** | C2P produces Compliance Assessment Results → OSCAL Assessment Results |

### 🎯 Plugin Responsibilities

- **Policy Generation**: Handle policy names/IDs and return policies
- **Result Processing**: Handle verdict and reasoning for each policy

---

## 🌐 Where does C2P come into play?

### 🔄 Native Format Translation

**C2P** generates policies in the **native** format of Policy Validation Points (PVP) **from** OSCAL Component Definitions, then produces OSCAL Assessment Results **from** native assessment results of PVP.

### 🏗️ Integration Options

**C2P** can be integrated into your **Continuous Compliance pipelines**:

- **GitHub Actions**
- **Tekton Pipelines**  
- **Agile Authoring Pipelines**

---

## 📂 GitHub Repositories

### 🏗️ Core Projects

[![compliance-to-policy](https://img.shields.io/badge/GitHub-compliance--to--policy-blue?style=for-the-badge&logo=github)](https://github.com/oscal-compass/compliance-to-policy)

[![compliance-to-policy-go](https://img.shields.io/badge/GitHub-compliance--to--policy--go-green?style=for-the-badge&logo=github)](https://github.com/oscal-compass/compliance-to-policy-go)

> 📖 **Reference**: Check the README.md of each repository for detailed information on Policy as Code implementation

---

<div align="center">

**🚀 Automate your compliance with Policy as Code! 🚀**

*Bridging Compliance as Code and Policy as Code for seamless governance*

</div>
