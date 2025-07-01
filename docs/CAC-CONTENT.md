### ComplianceAsCode Content 

#### What is Compliance as Code?

The `ComplianceAsCode/content` project is an open-source project that caters to simplification and maintenance of security content for operating systems and applications. The primary purpose of CaC/content is to develop and provide security policy content. The ComplianceAsCode/content project establishes a zero-tolerance policy for redundancies in developing security content. The driver of the project is combating the need for developing security content, separately, in multiple formats. The powerful build system requires the content to be written once, and then generated into multiple formats. 

**What does that mean?**

The meat of CaC is the powerful build system, making security content available in a "write-once" format (OpenControl-inspired YAML formatting). Automatically generating additional common security automation formats like SCAP, Ansible Playbooks, and Bash fix scripts. The ComplianceAsCode/content project enables more efficient development throughout multiple organizations, and supports diverse deployment. 


Not only does the CaC/content project have static documentation, but it encompasses executables that are meant to:
- **Evaluate compliance:** checking if the system build complies with security baselines.
- **Remediate non-compliance:** automatically configures a system to enforce and satisfy compliance.  

**How does it help Compliance Managers?**
- The auditing process can be aided through use of the standardized reporting and evidence provisioning of compliance. 


** Deep Dive**
The YAML Rule Files as input are the OpenControl-inspired YAML "write-once" styled formatting. 
- Templating: reduces redundancies by templating capabilities
- Centralized Security Identifiers: (NIST ID, SITG) are sourced from the rules files and ensure consistency in generated output. 

More can be seen on the [README.md](https://github.com/ComplianceAsCode/content/blob/master/README.md) of the ComplianceAsCode/content repository. 

#### What you _need_ to know

As a Compliance Professional, you'll inevitably need to collaborate with the Product Experts that work on CaC. Therefore, gaining a thorough understanding of the codebases and use-cases could fill in gaps during collaboration.

#### Resources for learning how to use ComplianceAsCode

- [Say Hello to ComplianceAsCode workshop](https://github.com/ComplianceAsCode/content/blob/master/docs/workshop/lab1_introduction.adoc)
- [ComplianceAsCode/content/controls](https://complianceascode.readthedocs.io/en/latest/flowcharts/flowchart_controls.html) for the content that will be used for creating OSCAL Catalogs.
- [ComplianceAsCode/content/products](https://complianceascode.readthedocs.io/en/latest/flowcharts/flowchart_products.html) for the content that will be used in tandem with OSCAL Catalogs to create OSCAL Profiles and Component Definitions.
