### Policy as Code

**What is it?**

Policy as Code defines, updates, shares, and enforces policies using code ([Policy as Code](https://www.redhat.com/en/blog/policy-as-code-automation)).


**Breakdown:**

- Policy is a rule, condition, or instruction that governs operations or processes. Additionally, policy is defined as a set of rules or guidelines for an organization, people, or process to achieve compliance, standards or consistency ([Policy as Code](https://www.redhat.com/en/blog/policy-as-code-automation)).
- Less discussion of the measures taken to comply with specific guidelines, and more machine-readable evidence of compliance. 

Common examples include testing automation scripts to ensure that your defined policies are being properly enforced. 

Policy Engine: used to enforce the policies
- Kyverno -> a policy engine for Kubernetes resources
- Audittree -> GitOps tool for evidence collection and verification, especially for cloud services via APIs

**Projects that exemplify Policy as Code**

[`compliance-to-policy`](https://github.com/oscal-compass/compliance-to-policy)
[`compliance-to-policy-go`](https://github.com/oscal-compass/compliance-to-policy-go)
