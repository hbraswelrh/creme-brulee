## Step xyz: Deep dive into `ComplianceAsCode/oscal-content` 

_This repository houses authored OSCAL content initialized by complyscribe_


After completing the thorough review of the projects and tools in _Step 1: Read the docs_ you can strengthen your understanding by example.

### 📖 Theory: Author OSCAL Content and Update it in your [oscal-content-demo](https://github.com/hbraswelrh/oscal-content-demo/tree/main)

The [oscal-content-demo](https://github.com/hbraswelrh/trestle-workspace/tree/main) is a public repository template that can be leveraged with complyscribe in GitHub CI. The file structure layout is seen in the tree below. 

## Mapping `oscal-content-demo` to the `ComplianceAsCode/oscal-content`

### Bidirectional Synchronization
Stay updated wth content changes where `sync-oscal-cac` and `sync-cac-oscal` make sure that the _back and forth_ exchange of information is accurate. 

#### `sync-oscal-cac` 

Once there is a change made in the `oscal-content` repository, there is an automatic trigger that transforms the `ComplianceAsCode/content` content and requests a change to that material. 

_Goal: updates should be synchronized and accurate_

```mermaid
graph LR
    A[OSCAL Content PR #33] --> B[Workflow Triggered]
    B --> C[Content Transformation]
    C --> D[ComplianceAsCode PR #13617]
```

This functionality would be present when doing ...

#### `sync-cac-oscal`

Once there is a change in the `ComplianceAsCode/content` content, there is an automatic trigger that will transform the content that `complyscribe` handles and then requests for that transformed change to be placed back in the `ComplianceAsCode/oscal-content` repository. 


```mermaid
graph LR
    A[ComplianceAsCode PR #13580] --> B[Workflow Triggered]
    B --> C[Content Transformation]
    C --> D[OSCAL Content PR #28]
```
> I know you're probably wondering why this is important...but, check this out!

Above, the control file defines the RHEL8 HIPAA profile. The change makes it simpler to reference this [hipaa control file](https://github.com/ComplianceAsCode/content/blob/master/controls/hipaa.yml) in the [RHEL8 HIPAA Profile](https://github.com/ComplianceAsCode/content/blob/master/products/rhel8/profiles/hipaa.profile). The rules associated with the controls are now in the control file and referenced in the RHEL8 Profile. The table below outlines the Rule, `ComplianceAsCode/content` representation, and the PDF reference to the requirement that the rule satisfies.


| Rule                            | ComplianceAsCode/content                                                                                                                                                                                                  | PDF Format                                                                                                                                                                                                                                           |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| coreos_disable_interactive_boot | [coreos_disable_interactive_boot](https://github.com/ComplianceAsCode/content/blob/213ff61cc3ea47773f478297e95d559fb6a15a6d/linux_os/guide/system/accounts/accounts-physical/coreos_disable_interactive_boot/rule.yml#L4) | [Risk Management 164.308(a)(1)(ii)(B)](https://www.ecfr.gov/current/title-45/part-164/section-164.308#p-164.308(a)(1)(ii)(B))                                                                                                                        |
| disable_ctrlaldel_burstaction   | [disable_ctrlaldel_burstaction](https://github.com/ComplianceAsCode/content/blob/213ff61cc3ea47773f478297e95d559fb6a15a6d/linux_os/guide/system/accounts/accounts-physical/disable_ctrlaltdel_burstaction/rule.yml#L4)    | [Risk Management 164.308(a)(1)(ii)(B)](https://www.ecfr.gov/current/title-45/part-164/section-164.308#p-164.308(a)(1)(ii)(B)), [Risk Management 164.308(a)(7)(i)](https://www.ecfr.gov/current/title-45/part-164/section-164.308#p-164.308(a)(7)(i)) |

The control ids are updated in the OSCAL Content PR #28 triggered by the update in ComplianceAsCode/content. The `oscal-content` profiles for RHEL8/HIPAA - [rhel8-hipaa-required](https://github.com/ComplianceAsCode/oscal-content/blob/1bf63ff5e400f1bd4934007e5251a586cbcafa7a/profiles/rhel8-hipaa-required/profile.json)

### ⌨️ Activity: Interact with the oscal-content-demo

To interact with the `oscal-content-demo`, you will need to create your own copy. This public repository template [oscal-content-demo](https://github.com/hbraswelrh/trestle-workspace/tree/main) allows you to create unlimited copies, providing a safe and secure sandbox for testing the tools directly.

**Step 1🖱️:** Navigate to the [oscal-content-demo](https://github.com/hbraswelrh/oscal-content-demo/tree/main). Click the green box in the upper right corner that says "Use this template."

<img src="https://github.com/user-attachments/assets/7f0d54c1-daef-488a-b8e4-0887cf7e491a" alt="text" width="375" height="200">

**Step 2🖱️🟩:** Click "Create a new repository." This step is comparable to the "Make a Copy" functionality when duplicating a Google Doc. 

<img src="https://github.com/user-attachments/assets/0ce8f4a7-453d-408e-8174-75cec1cc507a" alt="text" width="250" height="85">

**Step 3🖱️🟩:** Ensure that you are the repository owner and create a name for your new oscal-content-demo template. Then, click "Create Repository."

_You can choose to make the repository Public or Private_

<img src="https://github.com/user-attachments/assets/bb4ffe1a-20f0-4ab7-abd7-d76a2eb10573" alt="text" width="250" height="250">

**Step 4🪄:** Your repository has now been created and will be available under `{YOUR_GITHUB_USERNAME}/{OSCAL_CONTENT_DEMO_NAME}`

<img src="https://github.com/user-attachments/assets/f7fd13d0-4e58-4613-851c-57bb09f5b7f2" alt="text" width="375" height="200">

### Getting Comfortable with the `oscal-content-demo` flow

Follow the steps on the [oscal-content-demo](https://github.com/hbraswelrh/oscal-content-demo/tree/main?tab=readme-ov-file#getting-started) `README.md`for making your first change.

### `oscal-content-demo` Context: 

#### Running `complyscribe` commands in GitHub Actions 

The oscal-content-demo supports running `complyscribe` commands in GitHub Actions. The available actions are `autosync`, `create-cd`, and `rules-transform`. The workflows can be found [here](https://github.com/hbraswelrh/oscal-content-demo/blob/main/.github/workflows/README.md). This is a simplistic way to get started with your first few tests.

1. Navigate to the Actions tab in your oscal-content-demo workspace. 
   
<img alt="img_1.png" height="120" src="https://raw.githubusercontent.com/hbraswelrh/creme-brulee/4b8054ba9e94bd83b14d991cebda3d575d2420dd/docs/images/img_1.png" width="150"/>

<img alt="img.png" height="40" src="https://raw.githubusercontent.com/hbraswelrh/creme-brulee/4b8054ba9e94bd83b14d991cebda3d575d2420dd/docs/images/img.png" width="400"/>

2. Click "Run workflow."

This will prompt for your input depending on the command being run. If authoring Component Definitions, the input fields will populate for indicating profile, component title, component description, etc. Those are manual inputs. Autosync will run based on the trigger of "Run workflow."

<img alt="img_2.png" height="200" src="https://raw.githubusercontent.com/hbraswelrh/creme-brulee/4b8054ba9e94bd83b14d991cebda3d575d2420dd/docs/images/img_2.png" width="150"/>

<img alt="img_6.png" height="200" src="https://raw.githubusercontent.com/hbraswelrh/creme-brulee/4b8054ba9e94bd83b14d991cebda3d575d2420dd/docs/images/img_6.png" width="150"/>

<img alt="img_3.png" height="80" src="https://raw.githubusercontent.com/hbraswelrh/creme-brulee/4b8054ba9e94bd83b14d991cebda3d575d2420dd/docs/images/img_3.png" width="160"/>
   
3. Make sure the `branch: main` is indicated, and then click the green box "Run Workflow."

<img alt="img_4.png" height="100" src="https://raw.githubusercontent.com/hbraswelrh/creme-brulee/4b8054ba9e94bd83b14d991cebda3d575d2420dd/docs/images/img_4.png" width="250"/>
   
<img alt="img_5.png" height="100" src="https://raw.githubusercontent.com/hbraswelrh/creme-brulee/4b8054ba9e94bd83b14d991cebda3d575d2420dd/docs/images/img_5.png" width="325"/>


<img alt="img_7.png" height="100" src="https://raw.githubusercontent.com/hbraswelrh/creme-brulee/4b8054ba9e94bd83b14d991cebda3d575d2420dd/docs/images/img_7.png" width="325"/>


<img alt="img_8.png" height="100" src="https://raw.githubusercontent.com/hbraswelrh/creme-brulee/4b8054ba9e94bd83b14d991cebda3d575d2420dd/docs/images/img_8.png" width="325"/>

#### Self-assessment

_Let's see what you've learned_

Take the [self-assessment](https://form.typeform.com/to/EwVRNkJ4) once you have completed Step 2: _Initializing oscal-content-demo with complyscribe_.

##### What You'll Submit

Once completing Step 2: _Initializing oscal-content-demo with complyscribe_, you will have made changes on the `develop` branch of your `oscal-content-demo` repository. 

The changes made will be reflected in your Pull Request. Copy and paste the link of your Pull Request in the self-assessment. 

> Example: "ComplyTime Learning Course: {YOUR_NAME}."

#### Reviewing generated OSCAL Content from ComplianceAsCode/content

The oscal-content-demo supports running `complyscribe` commands in GitHub Actions. The `sync-cac-content` command that generates OSCAL Catalogs, Profiles, and Component Definitions is not currently available as a GitHub Action. The RHEL8, RHEL9, and RHEL10 product OSCAL Catalogs, Profiles, and Component Definitions are available in your workspace. The content from `ComplianceAsCode/content` was used with the `complyscribe sync-cac-content` commands to populate this content. The `ComplianceAsCode/oscal-content` repository is ongoing development and will synchronize the `ComplianceAsCode/content` resources with the `ComplianceAsCode/oscal-content` repository to continuously sync changes.  

#### Annotated File Tree 📂

The annotated file tree can be referenced in [annotated-tree.md](https://github.com/hbraswelrh/creme-brulee/blob/95c4bbb99cbb0e0b28b459f19950983ca13d34b7/docs/annotated-tree.md) which shows the current state of the oscal-content-demo public template. The annotations are consistent with the table below. 

**Example:** 

You want to create an OSCAL Catalog, OSCAL Profile, and an OSCAL Component Definition for a RHEL9 CIS Benchmark. The [ComplianceAsCode/content](https://github.com/ComplianceAsCode/content) repository houses up-to-date security content that is leveraged for transformation to OSCAL Content. 

Starting with the OSCAL Catalog, you want to base it off of the CIS Benchmark for RHEL9. Let trestle-bot do the magic 🪄 in GitHub Actions.


| OSCAL Content Created in `oscal-content-demo`                                                                                                                            |                                 ComplianceAsCode/content location                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------:|
| [OSCAL Catalog](https://github.com/hbraswelrh/oscal-content-demo/blob/main/catalogs/cis_rhel9/catalog.json)                                                              |    [cis_rhel9](https://github.com/ComplianceAsCode/content/blob/master/controls/cis_rhel9.yml)     | 
| [OSCAL Profile](https://github.com/hbraswelrh/oscal-content-demo/tree/main/profiles)                                                                                     | [cis](https://github.com/ComplianceAsCode/content/blob/master/products/rhel9/profiles/cis.profile) |
| [OSCAL Component Definition](https://github.com/hbraswelrh/oscal-content-demo/blob/main/component-definitions/rhel9/rhel9-cis_rhel9-l1_server/component-definition.json) | [cis](https://github.com/ComplianceAsCode/content/blob/master/products/rhel9/profiles/cis.profile) |


> 🗄️ Where you can find this content

<details>
<summary>Having trouble? 🤷</summary><br/>

- Reference the complyscribe [`README.md`](https://github.com/complytime/trestle-bot/blob/main/README.md).
- [The guide for navigating public templates](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)
- (replace-me: Additional troubleshooting tips as needed)

</details>
