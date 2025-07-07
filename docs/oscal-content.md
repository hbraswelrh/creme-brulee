# oscal-content

# **📚** oscal-content: Your Central Hub for Compliance

This repository is your go-to place for managing and storing security compliance content in the Open Security Controls Assessment Language (OSCAL) format. Our primary focus is on Red Hat (RH) products.

## 🚀 Overview: Automated Content Sync

Initialized by [complyscribe](https://www.google.com/search?q=%5Bhttps://github.com/complytime/complyscribe%5D\(https://github.com/complytime/complyscribe\)), this repository features powerful GitHub Actions designed for seamless content synchronization:

* `sync-comp`: ➡️ Consumes data from upstream [ComplianceAsCode/content](https://www.google.com/search?q=%5Bhttps://github.com/ComplianceAsCode/content%5D\(https://github.com/ComplianceAsCode/content\)) to generate related OSCAL content.  
* `sync-controls`: ➡️ Also consumes data from upstream [ComplianceAsCode/content](https://www.google.com/search?q=%5Bhttps://github.com/ComplianceAsCode/content%5D\(https://github.com/ComplianceAsCode/content\)) to generate OSCAL content.  
* `sync-oscal-cac`: ⬅️ Syncs OSCAL content updates *back* to [ComplianceAsCode/content](https://www.google.com/search?q=%5Bhttps://github.com/ComplianceAsCode/content%5D\(https://github.com/ComplianceAsCode/content\)). It works in tandem with [ComplianceAsCode/content's sync-cac-oscal CI](https://www.google.com/search?q=%5Bhttps://github.com/ComplianceAsCode/content/blob/master/.github/workflows/sync-cac-oscal.yml%5D\(https://github.com/ComplianceAsCode/content/blob/master/.github/workflows/sync-cac-oscal.yml\)).

🔄 Bidirectional Sync: sync-oscal-cac and sync-cac-oscal create a powerful two-way synchronization, ensuring both projects stay updated with each other's content changes.

## 🔄 How Content Synchronization Works

⚠️ Heads Up\! These CI systems are currently in active development. We're refining the user experience based on ongoing feedback.

### From ComplianceAsCode to OSCAL (sync-cac-oscal Workflow)

This workflow transforms content from ComplianceAsCode/content into the OSCAL format, powered by the complyscribe CLI.

* **Detect Changes:** Identifies updates in source content (controls, profiles, rules, vars).  
* **Prepare:** Gathers necessary arguments for Complyscribe.  
* **Transform:** Runs complyscribe to convert source files into OSCAL.  
* **Propose Updates:** Automatically creates a Pull Request (PR) with the new OSCAL content for review.

**Example:** A merge in ComplianceAsCode/content ([PR \#13580](https://github.com/ComplianceAsCode/content/pull/13580)) triggered a successful [workflow run](https://github.com/ComplianceAsCode/content/actions/runs/15688668981/job/44198205023), which then created an oscal-content [PR \#28](https://github.com/ComplianceAsCode/oscal-content/pull/28) to sync changes.

### From OSCAL to ComplianceAsCode (sync-oscal-cac Workflow)

This workflow handles the reverse sync, reflecting OSCAL content updates back into the ComplianceAsCode/content repository.

* **Trigger:** Activated upon merging a PR with OSCAL file changes.  
* **Detect Updates:** Identifies updated OSCAL files (catalogs, profiles, component-definitions).  
* **Sync with ComplyScribe:** Calls Complyscribe to transform OSCAL updates back into standard control and product profile formats.  
* **Create Upstream PR:** Automatically creates a new PR in the ComplianceAsCode/content repository.

**Example:** oscal-content [PR \#33](https://github.com/ComplianceAsCode/oscal-content/pull/33) triggered a successful [workflow run](https://github.com/ComplianceAsCode/oscal-content/actions/runs/15841883094/job/44656004616), which generated ComplianceAsCode/content [PR \#13617](https://github.com/ComplianceAsCode/content/pull/13617) to contribute changes back.

### Watch the demos 

Demo [recording](https://drive.google.com/file/d/1ZOc-H4f5zG_NCf_5rEuQMSwMZ52PkFzY/view) for `sync-oscal-cac` GitHub Action that syncs OSCAL Content changes to ComplianceAsCode/content.

Demo [recording](https://drive.google.com/file/d/1rvRlNkCzlvTh7NIC9JCKNIkiJCxW_S3W/view) for `sync-cac-oscal` GitHub Action that sync ComplianceAsCode/content changes to OSCAL Content.
## 🛠️ Tooling

We utilize [ComplyScribe](https://www.google.com/search?q=%5Bhttps://github.com/complytime/complyscribe%5D\(https://github.com/complytime/complyscribe\)) to help author and manage OSCAL content, ensuring adherence to required standards and formats.

### Why you should review `ComplianceAsCode/oscal-content`

The `ComplianceAsCode/oscal-content`repository is the same concept as your own `oscal-content-demo` repository. That repository will eventually be maintained by Compliance Managers.
Here's your document on "Policy as Code," reformatted for clarity, conciseness, and enhanced UX with emojis and blockquotes.

Here's a reformatted version of your README.md for improved UX, conciseness, and clarity.

## 🤝 Contributing

Maintainers can contribute by authoring or editing OSCAL content files in a forked repository and opening a Pull Request. Once merged, the sync-oscal-cac workflow will automatically trigger.
