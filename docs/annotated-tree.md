#### Annotated File Tree 📂

The trestle-workspace that was created will have a file structure similar to the one pictured below.

Branches of the trestle-workspace are initialized with different contents to keep your changes organized. 

:tree: 
- <img alt="img.png" height="50" src="branches.png" width="100"/>
  

- **feat/rhel8-content**
Link to [ComplianceAsCode RHEL8 content](https://github.com/ComplianceAsCode/content/tree/master/products/rhel8) used to initialize and sync the OSCAL Content.

- **feat/rhel9-content**
Link to [ComplianceAsCode RHEL9 content](https://github.com/ComplianceAsCode/content/tree/master/products/rhel9) used to initialize and sync the OSCAL Content.


- **feat/rhel10-content**
Link to [ComplianceAsCode RHEL10 content](https://github.com/ComplianceAsCode/content/tree/master/products/rhel10) used to initialize and sync the OSCAL Content.

```bash
.
├── assessment-plans/
├── assessment-results/
├── catalogs/
│   └── cis_rhel9/    # Control file cis_rhel9 in CaC/content
│       └── catalog.json    # OSCAL Catalog created through transformed CaC/content
├── component-definitions/
│   └── rhel9/
│       └── rhel9-cis_rhel9-l1_server/  # RHEL9 cis_rhel9-l1_server profile from CaC/content
│           └── component-definition.json  # OSCAL Component Definition from transformed CaC/content
├── markdown/
│   ├── assessment-plans/
│   ├── assessment-results/
│   ├── catalogs/
│   ├── component-definitions/
│   ├── plan-of-action-and-milestones/
│   ├── profiles/
│   └── system-security-plans/
├── plan-of-action-and-milestones/
├── profiles/
│   ├── rhel9-cis_rhel9-l1_server/ # RHEL9 cis_rhel9-l1_server profile from CaC/content
│   │   └── profile.json    # OSCAL Profile created from transformed CaC/content
│   ├── rhel9-cis_rhel9-l1_workstation/ # RHEL9 cis_rhel9-l1_workstation profile from CaC/content
│   │   └── profile.json    # OSCAL Profile created from transformed CaC/content
│   ├── rhel9-cis_rhel9-l2_server/ # RHEL9 cis_rhel9-l2_server profile from CaC/content
│   │   └── profile.json    # OSCAL Profile created from transformed CaC/content
│   └── rhel9-cis_rhel9-l2_workstation/ # RHEL9 cis_rhel9-l2_workstation profile from CaC/content
│       └── profile.json    # OSCAL Profile created from transformed CaC/content
└── system-security-plans/

```
