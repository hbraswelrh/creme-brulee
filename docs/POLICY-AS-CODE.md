### Policy as Code

#### What is it?

Policy as Code defines, updates, shares, and enforces policies using code ([Policy as Code](https://www.redhat.com/en/blog/policy-as-code-automation)).

#### Goals

Integrate compliance frameworks and existing policy engines, while enabling usage of heterogeneous policy engines in compliance check operations. 

> Flexibility in choice of policy engines and compliance frameworks

> Community driven plugin extension

#### Breakdown

- Policy is a rule, condition, or instruction that governs operations or processes. Additionally, policy is defined as a set of rules or guidelines for an organization, people, or process to achieve compliance, standards or consistency ([Policy as Code](https://www.redhat.com/en/blog/policy-as-code-automation)).
- Less discussion of the measures taken to comply with specific guidelines, and more machine-readable evidence of compliance. 

Common examples include testing automation scripts to ensure that your defined policies are being properly enforced. 

**Policy Engine:** used to enforce the policies
- [**Kyverno**](https://kyverno.io/docs/introduction/) -> a policy engine for Kubernetes resources
- [**Auditree**](https://auditree.github.io/) -> GitOps tool for evidence collection and verification, especially for cloud services via APIs

**Projects that exemplify Policy as Code**

The `compliance-to-policy` projects aim to bridge the gap between Compliance as Code and Policy as Code.

**Consider the following:**

> **Compliance As Code** = OSCAL
> **Policy As Code** = used by Policy Validation Points (PVP)

1. C2P running in GitOps Pipeline, Kubernetes controller, or Python/Go environment
2. C2P receives Compliance as Code -> OSCAL Component Definition - mapping controls and policies by policy name/id.
3. C2P generates policies through use of a plugins for _each_ policy engine.
   - The plugin is responsible for handling policy names/ids and returning policies.
4. Policies then get delivered to the policy engines.
5. Results are collected from policy engines
6. C2P aggregates the results of the policy engines by controls through a plugin for each policy engine.
   - The plugin is responsible for implementing the handling of verdict and sorting of reasoning for each of the policies. 
7. C2P produces Compliance Assessment Results -> OSCAL Assessment Results - representative of assessment results of each control. 

**Where does C2P come into play?**

C2P generates policies in the _native_ format of PVP _from_ the OSCAL Component Definitions. Then, OSCAL Assessment Results are produced _from_ native assessment results of PVP.
-  C2P can be integrated into your Continuous Compliance pipelines:
  - GitHub Actions
  - Tekton Pipelines
  - Agile Authoring Pipelines

#### GitHub Repositories 
- [`compliance-to-policy`](https://github.com/oscal-compass/compliance-to-policy)
- [`compliance-to-policy-go`](https://github.com/oscal-compass/compliance-to-policy-go)
