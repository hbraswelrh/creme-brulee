## Step 2: Deep Dive into `ComplianceAsCode/oscal-content` 

_This repository houses authored OSCAL content initialized by complyscribe_


After completing the thorough review of the projects and tools in _Step 1: Read the docs_ you can strengthen your understanding by example.

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

Above, the PR in the `oscal-content` will trigger the workflow and make sure the changes are initialized by `complyscribe` and sending that back to the `ComplianceAsCode/content` repository.

The updates automatically trigger the request to propose changes to the `ComplianceAsCode/content` repository content. The deletion of rules from the `component-definition.json` trigger the automatic generation of this [PR](https://github.com/ComplianceAsCode/content/pull/13680) in `ComplianceAsCode/content`. The PR proposes changes to the levels applied to te control file [cis_rhel8](https://github.com/ComplianceAsCode/content/pull/13680/files#diff-c97f4c1b44844a9d76570cbbc2bf8fdbceb1dc1076461fc8408870ab612cad9cR33) in `ComplianceAsCode/content`

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

#### Self-assessment

_Let's see what you've learned_

[//]: # (Take the [self-assessment]&#40;https://form.typeform.com/to/EwVRNkJ4&#41; once you have completed Step 2: _Initializing oscal-content-demo with complyscribe_.)
Take the [self-assessment](https://docs.google.com/forms/d/e/1FAIpQLSccmDXNrEe5Tx_pkenjmtqvfZ90a8TIKy_8C-ZlSS15dHFBCw/viewform?usp=header) once you have completed Step 2: _Deep Dive into oscal-content_.

##### What You'll Submit

The changes made will be reflected in your Pull Request. Copy and paste the link of your Pull Request in the self-assessment. 

> Example: "ComplyTime Learning Course: {YOUR_NAME}."

## Perspective :book::custard:

Think of the relationship of `ComplianceAsCode/oscal-content` and `ComplianceAsCode/content` repository with this analogy.

**Imagine you have the original first-edition cookbook for all things pastries** :custard: :cookie:. 

- Let's call this book _The Original Project Bakeshop_, containing the foundational recipes for every pastry and treat from cupcakes, to NATA, to creme-brulee. It's the source of truth for all baking endeavors. 

**Now, you have a good friend, your baking confidant, who wants to specialize in the creme-brulee :custard: recipe section of _The Original Project Bakeshop_.**

- They want to have their own specialized version of your cookbook that builds on the results, but makes sure any recipe changes made in the first-edition are factored into their copy. 
- This version focuses only on creme-brulee, but i's based on the recipes available in _The Original Project Bakeshop_.

As you both bake, you'll tweak :magic_wand: a few things here and there. Potentially finding a better way to infuse vanilla or a better torching :fire: technique that creates an immaculate crispy top. You both want the recipe to be the best that it can be, and that means ensuring both the first-edition creme-brulee section and the creme-brulee dedicated book reflect the newfound methods. 

**GitHub Actions:** Culinary Coordinators :cook::magic_wand::bellhop_bell:

GitHub Actions is your incredibly efficient team of culinary coordinators. Their sole purpose is to ensure that any improvements made to the creme-brulee recipe in _The Original Project Bakeshop_ or the specialized creme-brulee book are perfectly synchronized, resulting in the best creme-brulee that is approved by the first-edition.

#### Here's how it works:

- Your update to the creme-brulee recipe of _The Original Project Bakeshop_ you're telling your culinary coordinators "Hey, I just made an improvement to creme-brulee! Everyone needs to know about this!"
- Your friend updates the specialized recipe discovering an even more efficient way to caramelize sugar with the torching method. They also reach out to the culinary coordinators.
- The coordinators get to work and compare the recipe books. If _The Original Project Bakeshop_ was updated, they make sure the improvement is reflected in your friend's specialized creme-brulee book :arrows_clockwise:. If the specialized book has a brilliant new discovery, the coordinators ensure that is exchanged and shared back to keep _The Original Project Bakeshop_ up-to-date. 
- The constant, automated synchronization keeps you and your friend working from the most refined and complete creme-brulee instructions. 

GitHub Actions act as the automated bridge to ensure specific, related recipe changes are synchronized for consistent final products.

## **Mastering the Recipe: A Compliance-as-Code Analogy 🍮📚**

Let's imagine the relationship between ComplianceAsCode/oscal-content and ComplianceAsCode/content using a delicious analogy.

### **The Master Cookbook: ComplianceAsCode/content**

**Think of ComplianceAsCode/content as your definitive, first-edition cookbook for all things compliance.** It contains the foundational, approved recipes (compliance rules, policies, benchmarks) for every aspect of your organization's security posture. This is the **source of truth** for all compliance endeavors.

### **The Specialized Cookbook: ComplianceAsCode/oscal-content**

**Now, imagine ComplianceAsCode/oscal-content as a specialized companion cookbook.** It's built directly from the Master Cookbook but focuses specifically on the "Creme Brûlée" section – representing the OSCAL (Open Security Controls Assessment Language) format.

This specialized book contains only the creme brûlée recipes, ensuring they are always up-to-date with the Master Cookbook, even as the original recipes evolve. It's designed for those who need to work exclusively with the OSCAL format, building upon the foundational recipes while maintaining perfect synchronization.

### **The Culinary Coordinators: GitHub Actions & Complyscribe 🧑‍🍳✨**

**GitHub Actions are your tireless team of culinary coordinators, and complyscribe is their specialized chef.** Their combined job is to ensure that any improvements or updates to the creme brûlée recipe – whether in the Master Cookbook or the Specialized Cookbook – are perfectly synchronized and reflected in both.

**Here's how they work:**

* **Master Cookbook Update:** When you refine the creme brûlée recipe in the Master Cookbook, your Culinary Coordinators (GitHub Actions) spring into action. They use complyscribe as their expert chef to automatically translate and update the Specialized Cookbook (ComplianceAsCode/oscal-content). This ensures that your friend, who relies on the specialized OSCAL version, always has the latest and greatest recipe.  
* **Specialized Cookbook Discovery:** If your friend discovers a more efficient way to caramelize the sugar (a new OSCAL implementation or refinement), the Culinary Coordinators (GitHub Actions) ensure this valuable insight is shared back and incorporated into the Master Cookbook.  
* **Constant Harmony:** This automated synchronization, powered by GitHub Actions and complyscribe, means you and your friend are always working from the most refined and complete creme brûlée instructions. GitHub Actions act as the automated bridge, with complyscribe handling the crucial conversion process, ensuring consistent, high-quality "compliance creme brûlée" across both repositories.

In essence, GitHub Actions automate the collaboration, and complyscribe facilitates the specific conversion and synchronization, ensuring that the specialized OSCAL content (oscal-content) remains perfectly aligned with the comprehensive compliance content (content), and vice versa, leading to a consistently delicious (and compliant\!) final product.

> 🗄️ Where you can find this content

<details>
<summary>Having trouble? 🤷</summary><br/>

- Reference the complyscribe [`README.md`](https://github.com/complytime/trestle-bot/blob/main/README.md).
- [The guide for navigating public templates](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)
- (replace-me: Additional troubleshooting tips as needed)

</details>
