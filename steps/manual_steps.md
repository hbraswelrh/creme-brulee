## Learning Course Steps 

> Prerequisites must be completed prior to attempting the ComplyTime module 

## **📚 Reading `creme-brulee` Course Documentation**

This is the _first_ step of the learning course. Get started by reviewing the docs that will set the stage for your learning journey within the `creme-brulee` project.


### **✅ Mandatory Review Materials for Course Completion**

Ensure you've reviewed these foundational resources for your success in the course.

| Topic                    | Where you can find the docs                                                                             | 
|--------------------------|---------------------------------------------------------------------------------------------------------|
| ComplianceAsCode/content | [`docs/CAC-CONTENT.md`](https://github.com/hbraswelrh/creme-brulee/blob/main/docs/CAC-CONTENT.md)       |
| Policy as Code           | [`docs/POLICY-AS-CODE.md`](https://github.com/hbraswelrh/creme-brulee/blob/main/docs/POLICY-AS-CODE.md) |
| CNCF                     | [`docs/CNCF.md`](https://github.com/hbraswelrh/creme-brulee/blob/main/docs/CNCF.md)                     |
| Compliance Trestle       | [`TRESTLE-OVERVIEW.md`](https://github.com/hbraswelrh/creme-brulee/blob/main/docs/TRESTLE-OVERVIEW.md)  |


### **📝 Take the Self-Assessment**

Once you've thoroughly reviewed all the documentation above, take this short [self-assessment quiz](https://form.typeform.com/to/tiOAik8G). Good luck\! 🚀



## Step 2: Initialize the `trestle-workspace` 🤖

_This will house the authored OSCAL content_

#### 📖 Theory: Author OSCAL Content and Update it in your [trestle-workspace](https://github.com/hbraswelrh/trestle-workspace/tree/main)

The [trestle-workspace](https://github.com/hbraswelrh/trestle-workspace/tree/main) is a public template that can be leveraged with trestle-bot in GitHub CI. The file structure layout is seen in the tree below. 

#### ⌨️ Activity: Interact with the trestle-workspace

To interact with the trestle workspace, you will need to create your own copy of the [trestle-workspace](https://github.com/hbraswelrh/trestle-workspace/tree/main) public repository template. This will allow you to have your own trestle-workspace directly out of the box. 

**Step 1🖱️:** Navigate to the [trestle-workspace](https://github.com/hbraswelrh/trestle-workspace/tree/main). Click the green box in the upper right corner that says "Use this template."

<img src="https://github.com/user-attachments/assets/7f0d54c1-daef-488a-b8e4-0887cf7e491a" alt="text" width="375" height="200">

**Step 2🖱️🟩:** Click "Create a new repository." This step is comparable to the "Make a Copy" functionality when duplicating a Google Doc. 

<img src="https://github.com/user-attachments/assets/0ce8f4a7-453d-408e-8174-75cec1cc507a" alt="text" width="250" height="85">

**Step 3🖱️🟩:** Ensure that you are the repository owner and create a name for your new trestle-workspace template. Then, click "Create Repository."

_You can choose to make the repository Public or Private_

<img src="https://github.com/user-attachments/assets/bb4ffe1a-20f0-4ab7-abd7-d76a2eb10573" alt="text" width="250" height="250">

**Step 4🪄:** Your repository has now been created and will be available under `{YOUR_GITHUB_USERNAME}/{OSCAL_CONTENT_DEMO_NAME}`

<img src="https://github.com/user-attachments/assets/f7fd13d0-4e58-4613-851c-57bb09f5b7f2" alt="text" width="375" height="200">


#### Trestle Workspace Context: 

##### Running complyscribe commands in GitHub Actions 

The trestle-workspace supports running complyscribe commands in GitHub Actions. The available actions are autosync, create, and rules-transform. The workflows can be seen [here](https://github.com/hbraswelrh/trestle-workspace/blob/main/.github/workflows/README.md). This is a simplistic way to get started with your first few tests.

1. Navigate to the Actions tab in the trestle-workspace
   
<img alt="img_1.png" height="120" src="https://github.com/hbraswelrh/creme-brulee/blob/1f1547fec174dd47a01c38e1a3b56d254a92d5a1/.github/steps/images/img_1.png" width="150"/>

<img alt="img.png" height="40" src="https://github.com/hbraswelrh/creme-brulee/blob/1f1547fec174dd47a01c38e1a3b56d254a92d5a1/.github/steps/images/img.png" width="400"/>

2. Click "Run workflow."

This will prompt for your input depending on the command being run. If you are authoring Component Definitions, the fields will populate for indicating profile, component title, component description, etc. Autosync will run based on the trigger of "Run workflow."

<img alt="img_2.png" height="200" src="https://github.com/hbraswelrh/creme-brulee/blob/1f1547fec174dd47a01c38e1a3b56d254a92d5a1/.github/steps/images/img_2.png" width="150"/>

<img alt="img_6.png" height="200" src="https://github.com/hbraswelrh/creme-brulee/blob/1f1547fec174dd47a01c38e1a3b56d254a92d5a1/.github/steps/images/img_6.png" width="150"/>

<img alt="img_3.png" height="80" src="https://github.com/hbraswelrh/creme-brulee/blob/1f1547fec174dd47a01c38e1a3b56d254a92d5a1/.github/steps/images/img_3.png" width="160"/>
   
3. Make sure the `branch: main` is indicated, and then click the green box "Run Workflow."

<img alt="img_4.png" height="100" src="https://github.com/hbraswelrh/creme-brulee/blob/1f1547fec174dd47a01c38e1a3b56d254a92d5a1/.github/steps/images/img_4.png" width="250"/>
   
<img alt="img_5.png" height="100" src="https://github.com/hbraswelrh/creme-brulee/blob/1f1547fec174dd47a01c38e1a3b56d254a92d5a1/.github/steps/images/img_5.png" width="325"/>
   



<img alt="img_7.png" height="100" src="https://github.com/hbraswelrh/creme-brulee/blob/1f1547fec174dd47a01c38e1a3b56d254a92d5a1/.github/steps/images/img_7.png" width="325"/>


<img alt="img_8.png" height="100" src="https://github.com/hbraswelrh/creme-brulee/blob/1f1547fec174dd47a01c38e1a3b56d254a92d5a1/.github/steps/images/img_8.png" width="325"/>

#### Reviewing generated OSCAL Content from ComplianceasCode/content

The trestle-workspace supports running complyscribe commands in GitHub Actions. The `sync-cac-content` command that generates OSCAL Catalogs, Profiles, and Component Definitions is not currently available as a GitHub Action. The RHEL9 product OSCAL Catalogs, Profiles, and Component Definitions that are available using the ComplianceAsCode/content repository are available on the `feat/rhel9-content` branch of the public template repository. See [here](https://github.com/hbraswelrh/trestle-workspace/tree/feat/rhel9-content). 

#### Annotated File Tree 📂

The annotated file tree can be referenced in [annotated-tree.md](https://github.com/hbraswelrh/creme-brulee/blob/95c4bbb99cbb0e0b28b459f19950983ca13d34b7/docs/annotated-tree.md) which shows the current state of the trestle-workspace public template. The annotations are consistent with the table below. 

**Example:** 

You want to create an OSCAL Catalog, OSCAL Profile, and an OSCAL Component Definition for a RHEL9 CIS Benchmark. The [ComplianceAsCode/content](https://github.com/ComplianceAsCode/content) repository houses up-to-date security content that is leveraged for transformation to OSCAL Content. 

Starting with the OSCAL Catalog, you want to base it off of the CIS Benchmark for RHEL9. Let trestle-bot do the magic 🪄 in GitHub Actions.


| OSCAL Content Created in `trestle-workspace`                                                                                                                               |                                 ComplianceAsCode/content location                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------:|
| [OSCAL Catalog](https://github.com/hbraswelrh/my-trestle-workspace/blob/main/catalogs/cis_rhel9/catalog.json)                                                              |    [cis_rhel9](https://github.com/ComplianceAsCode/content/blob/master/controls/cis_rhel9.yml)     | 
| [OSCAL Profile](https://github.com/hbraswelrh/my-trestle-workspace/tree/main/profiles)                                                                                     | [cis](https://github.com/ComplianceAsCode/content/blob/master/products/rhel9/profiles/cis.profile) |
| [OSCAL Component Definition](https://github.com/hbraswelrh/my-trestle-workspace/blob/main/component-definitions/rhel9/rhel9-cis_rhel9-l1_server/component-definition.json) | [cis](https://github.com/ComplianceAsCode/content/blob/master/products/rhel9/profiles/cis.profile) |

- The `annotated-tree.md`indicates "Control File cis_rhel9 from ComplianceAsCode/content" and "RHEL9 Profile for cis_rhel9-l1_x/12_x." Reference the second column of the table for how the elements of the ComplianceAsCode/content repository align with the trestle-workspace content.
- 
- The base file tree without annotations can be found in [workspace-tree.md](https://github.com/hbraswelrh/creme-brulee/blob/520790e4c8b261cfe2b83a804c1c2728bdacb3ef/docs/workspace-tree.md)

<!--The ComplianceAsCode/content repository is used for syncing and transforming content to OSCAL format.--> 

#### Workspace file tree 

```bash
.
├── assessment-plans
├── assessment-results
├── catalogs
│   └── cis_rhel9
│       └── catalog.json
├── component-definitions
│   └── rhel9
│       └── rhel9-cis_rhel9-l1_server
│           └── component-definition.json
├── markdown
│   ├── assessment-plans
│   ├── assessment-results
│   ├── catalogs
│   ├── component-definitions
│   ├── plan-of-action-and-milestones
│   ├── profiles
│   └── system-security-plans
├── plan-of-action-and-milestones
├── profiles
│   ├── rhel9-cis_rhel9-l1_server
│   │   └── profile.json
│   ├── rhel9-cis_rhel9-l1_workstation
│   │   └── profile.json
│   ├── rhel9-cis_rhel9-l2_server
│   │   └── profile.json
│   └── rhel9-cis_rhel9-l2_workstation
│       └── profile.json
└── system-security-plans


```

<details>
<summary>Having trouble? 🤷</summary><br/>

- Reference the trestle-bot [`README.md`](https://github.com/complytime/trestle-bot/blob/main/README.md).
- Comment on the GitHub issue that was created when starting this workflow.
- [The guide for navigating public templates](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)
- (replace-me: Additional troubleshooting tips as needed)

</details>
