## `complyctl` overview

ComplyCTL is a tool that uses OSCAL to conduct compliance assessment activities. It operates by leveraging a plugin-based architecture for each stage of the compliance lifecycle.

### Core Functionality:

ComplyCTL guides users through the compliance assessment process, starting with defining a baseline and creating an OSCAL Assessment Plan. This Assessment Plan acts as the configuration for its generation and scanning operations.

### Basic Usage Workflow:

`complyctl list`: Lists available compliance frameworks.

`complyctl info <framework-id>`: Displays detailed information about a specific framework's controls and rules.

`complyctl plan <framework-id>`: Generates an assessment-plan.json file, which can be customized using a config.yml file.

`complyctl generate`: Generates policy artifacts based on the assessment plan.

`complyctl scan`: Executes the generated artifacts and produces assessment-results.json (and optionally assessment-results.md).

### Additional Information:

ComplyCTL provides detailed documentation for installation, quick start, and sample component definitions.

It encourages contributions and offers guidelines for contributing, style, and a code of conduct.

Users interested in extending its capabilities can write their own plugins.

Reference the [complyctl](https://github.com/complytime/complyctl) repository README.md for additional context.
