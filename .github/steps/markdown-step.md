# Step 2: Practice Communicating using Markdown and Git

> You should've completed the _Communicate Using Markdown_ GitHub Skills course as a pre-requisite. 

Follow the [help guide](https://github.com/hbraswelrh/creme-brulee/blob/main/docs/issue-help.md) for creating issues.

## 🧰 What you'll need

After completing [**Step 1:** _Read the docs_](https://github.com/hbraswelrh/creme-brulee/blob/main/.github/steps/1-step.md) you'll need to copy the link to the exercise issue and include it in the Pull request.


Follow the steps in the [manual_steps.md]() for an in-depth walkthrough and example of editing content in the `markdown/` folder.
---

## **Getting Started**

Follow these steps to edit content in the markdown/ folder. For a detailed walkthrough and an example, refer to the **manual steps**.

1. **Create a New Branch**: In your copy of the learning course, create a new branch named `learn-complytime/step-2`. 
2. **Switch Branches**: Switch to the `learn-complytime/step-2` branch. This is where you'll start working with Git and Markdown.  
3. **Navigate and Review**: Go to the `markdown/` folder and review its contents. You'll find catalogs, profiles, and component definitions that were initialized by `complyscribe`.  
   * **Editing Example**: The in-depth walkthrough in the [course_layout.md](https://github.com/hbraswelrh/creme-brulee/blob/main/steps/course_layout.md) provides an example of editing Markdown in the `markdown/profiles/rhel10-anssi-enhanced/r1/r1.md` file. Use this as a guide to make changes in the "Editable Content" section of your control files. **Directions are hidden until you begin editing the Markdown file.**  
4. **Commit Your Changes**: Commit your changes to your `learn-complytime/step-2` branch. You can make several commits as you work.  
5. **Open a Pull Request**: Open a Pull Request and update its description to clearly explain the changes you've made in the Markdown files.  
6. **Submit Your Work**: Copy the link to your Pull Request and submit it in the self-assessment.  
7. **Keep Practicing\!**: There's no limit to how many times you can retry this exercise. Simply follow the steps in the [**manual steps**](https://github.com/hbraswelrh/creme-brulee/blob/main/steps/manual_steps.md) again. For additional help, refer to the [**course layout**](https://github.com/hbraswelrh/creme-brulee/blob/main/steps/course_layout.md).

---

1. Create a new branch in your copy of the learning course. The name of the branch must be `learn-complytime/step-2`.
2. Switch to the `learn-complytime/step-2` branch to start working with Git and Markdown.
3. Navigate to the `markdown/` folder and review the contents. There are catalogs, profiles, and component definitions initialized by `complyscribe`. In the in-depth walkthrough, there is an example of editing Markdown in the `markdown/profiles/rhel10-anssi-enhanced/r1/r1.md` file. Follow the same procedure to make changes the "Editable Content" section of the control files. Directions are hidden until editing the Markdown file.
4. Commit several changes to your `learn-complytime/step-2` branch.
5. Open a Pull Request and update the description to reflect what changes you made in the markdown files.
6. Copy the link to your Pull Request and submit it in the self-assessment.
7. Keep practicing! There is no limit to the amount of times you can retry this exercise. Just follow the same steps in the [manual_steps.md](https://github.com/hbraswelrh/creme-brulee/blob/main/steps/manual_steps.md). Reference the [course_layout.md](https://github.com/hbraswelrh/creme-brulee/blob/main/steps/course_layout.md) for additional help/ 

## :octocat: Open a Pull Request

You'll need to create a New Branch in your copy of the `creme-brulee` ComplyTime module (ex: `learn-complytime/{user_name}`). After switching to that branch, update markdown **Control Statements** in the `markdown/` folder of your workspace. Then, open a Pull Request from your branch `learn-complytime/{user_name}` that proposes changes to `main`. Then, using the Pull Request template, update the contents of the Pull Request to reflect the changes introduced.

> The Pull Request will be part of the attestation of course completion.

## What You'll Submit

The [self-assessment]() will require submission of the link to your GitHub issue for taking notes and the Pull request opened with markdown changes. 
## RHEL10 ANSSI Enhanced Profile Example

---
x-trestle-global:
  profile:
    title: rhel10-anssi-enhanced
  sort-id: r12
---

# r12 - \[REPLACE_ME\] Ipv4 Configuration Options

## Control Statement

# Editable Content

<!-- Make additions and edits below -->
<!-- The above represents the contents of the control as received by the profile, prior to additions. -->
<!-- If the profile makes additions to the control, they will appear below. -->
<!-- The above markdown may not be edited but you may edit the content below, and/or introduce new additions to be made by the profile. -->
<!-- If there is a yaml header at the top, parameter values may be edited. Use --set-parameters to incorporate the changes during assembly. -->
<!-- The content here will then replace what is in the profile for this control, after running profile-assemble. -->
<!-- The current profile has no added parts for this control, but you may add new ones here. -->
<!-- Each addition must have a heading either of the form ## Control my_addition_name -->
<!-- or ## Part a. (where the a. refers to one of the control statement labels.) -->
<!-- "## Control" parts are new parts added after the statement part. -->
<!-- "## Part" parts are new parts added into the top-level statement part with that label. -->
<!-- Subparts may be added with nested hash levels of the form ### My Subpart Name -->
<!-- underneath the parent ## Control or ## Part being added -->
<!-- See https://oscal-compass.github.io/compliance-trestle/tutorials/ssp_profile_catalog_authoring/ssp_profile_catalog_authoring for guidance. -->


#### Add the following sections

# ac-1 - \[Access Control\] Access Control Policy and Procedures

## Control Statement

The organization:

- \[a.\] Develops, documents, and disseminates to {{ insert: param, ac-1_prm_1 }}:

  - \[1.\] An access control policy that addresses purpose, scope, roles, responsibilities, management commitment, coordination among organizational entities, and compliance; and
  - \[2.\] Procedures to facilitate the implementation of the access control policy and associated access controls; and

- \[b.\] Reviews and updates the current:

  - \[1.\] Access control policy {{ insert: param, ac-1_prm_2 }}; and
  - \[2.\] Access control procedures {{ insert: param, ac-1_prm_3 }}.

## Control Objective

Determine if the organization:

- \[AC-1(a)\]

  - \[AC-1(a)(1)\]

    - \[AC-1(a)(1)[1]\] develops and documents an access control policy that addresses:

      - \[AC-1(a)(1)[1][a]\] purpose;
      - \[AC-1(a)(1)[1][b]\] scope;
      - \[AC-1(a)(1)[1][c]\] roles;
      - \[AC-1(a)(1)[1][d]\] responsibilities;
      - \[AC-1(a)(1)[1][e]\] management commitment;
      - \[AC-1(a)(1)[1][f]\] coordination among organizational entities;
      - \[AC-1(a)(1)[1][g]\] compliance;

    - \[AC-1(a)(1)[2]\] defines personnel or roles to whom the access control policy are to be disseminated;
    - \[AC-1(a)(1)[3]\] disseminates the access control policy to organization-defined personnel or roles;

  - \[AC-1(a)(2)\]

    - \[AC-1(a)(2)[1]\] develops and documents procedures to facilitate the implementation of the access control policy and associated access control controls;
    - \[AC-1(a)(2)[2]\] defines personnel or roles to whom the procedures are to be disseminated;
    - \[AC-1(a)(2)[3]\] disseminates the procedures to organization-defined personnel or roles;

- \[AC-1(b)\]

  - \[AC-1(b)(1)\]

    - \[AC-1(b)(1)[1]\] defines the frequency to review and update the current access control policy;
    - \[AC-1(b)(1)[2]\] reviews and updates the current access control policy with the organization-defined frequency;

  - \[AC-1(b)(2)\]

    - \[AC-1(b)(2)[1]\] defines the frequency to review and update the current access control procedures; and
    - \[AC-1(b)(2)[2]\] reviews and updates the current access control procedures with the organization-defined frequency.

## Control guidance

This control addresses the establishment of policy and procedures for the effective implementation of selected security controls and control enhancements in the AC family. Policy and procedures reflect applicable federal laws, Executive Orders, directives, regulations, policies, standards, and guidance. Security program policies and procedures at the organization level may make the need for system-specific policies and procedures unnecessary. The policy can be included as part of the general information security policy for organizations or conversely, can be represented by multiple policies reflecting the complex nature of certain organizations. The procedures can be established for the security program in general and for particular information systems, if needed. The organizational risk management strategy is a key factor in establishing policy and procedures.

## ANSSI _for example..._ 

As a Compliance Manager, you would edit the markdown using bullet points (-) and the Markdown syntax standard.

# r1 - \[REPLACE_ME\] Hardware Support

## Control Statement

It is recommended to apply the configuration recommendations for Hardware support mentioned in ANSSI DAT-24.

______________________________________________________________________

## What is the solution and how is it implemented?

<!-- For implementation status enter one of: implemented, partial, planned, alternative, not-applicable -->

<!-- Note that the list of rules under ### Rules: is read-only and changes will not be captured after assembly to JSON -->

<!-- Add control implementation description here for control: r1 -->

### Rules:

  - rule-r1

### Implementation Status: planned

______________________________________________________________________


# r2 - \[REPLACE_ME\] Hardware Configuration

## Control Statement

It is recommended to apply the configuration recommendations for BIOS/UEFI mentioned in ANSSI DAT-24.

______________________________________________________________________

## What is the solution and how is it implemented?

<!-- For implementation status enter one of: implemented, partial, planned, alternative, not-applicable -->

<!-- Note that the list of rules under ### Rules: is read-only and changes will not be captured after assembly to JSON -->

<!-- Add control implementation description here for control: r2 -->

### Rules:

  - rule-r2

### Implementation Status: planned

______________________________________________________________________
