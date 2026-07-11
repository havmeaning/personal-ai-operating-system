# Security

## Reporting Issues

Open a GitHub issue for documentation or evidence-governance issues that do not expose private material.

Do not include secrets, private records, credentials, raw exports, or participant data in an issue.

## Public Repository Controls

This repository should avoid:

- secrets
- private source exports
- direct identifiers
- protected source records
- unreviewed participant data

## Maintainer Review

Before merging changes that add reports, source-derived examples, or validation data, maintainers should run:

- Markdown link check
- privacy scan
- claims-register review
- source-manifest review
