# GitHub security controls

This repository already has a Code Quality workflow and a multi-platform release workflow, including platform-specific artifact checksum and attestation steps. Preserve the existing release/signing pipeline rather than introducing a competing publisher.

Additional controls: weekly npm dependency update PRs, monthly GitHub Actions update PRs, and a scheduled/PR-triggered production dependency JSON report. The dependency workflow is advisory while the existing lockfile vulnerabilities are triaged; it does not block merges. To make quality checks required, configure repository branch rules using the existing actual passing check name. Do not automatically publish or merge dependency updates without testing.
