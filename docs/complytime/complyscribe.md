# `complyscribe` overview

ComplyScribe is a Command Line Interface (CLI) tool designed to help users integrate [Compliance-Trestle](https://github.com/oscal-compass/compliance-trestle) into their Continuous Integration/Continuous Delivery (CI/CD) workflows for managing OSCAL (Open Security Controls Assessment Language) formatted compliance content.

### 🗝️ Key Features and Commands:

`autosync`: Synchronizes Trestle-generated Markdown files into OSCAL JSON files, supporting all top-level models.

`rules-transform`: Transforms rules defined in YAML into an OSCAL Component Definition JSON file.

`create compdef`: Creates a new OSCAL Component Definition, setting up the workspace for rules-transform and autosync.

`sync-upstreams`: Syncs and validates OSCAL content from a Git repository to a local Trestle workspace, with options to include or exclude specific models.

`create ssp`: Creates a new OSCAL System Security Plan (SSP), preparing the workspace for autosync by managing the ssp-index.json file.

`sync-cac-content`: Transforms "Compliance as Code" (CaC) content into OSCAL models within a Trestle workspace.

`sync-oscal-content`: Synchronizes OSCAL models back to CaC content in a Trestle workspace.

### ⏲️ Current Status and Usage:

The project is currently under initial development, meaning its APIs may change. Many of its commands are available as GitHub Actions, and it supports GitHub and GitLab for creating pull requests. ComplyScribe can also be run as a container using podman.

Read more on the [complyscribe](https://github.com/complytime/complyscribe) repository README.md. 
