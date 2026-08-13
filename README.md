# Codex governance workflows

This public repository contains only the reusable, read-only governance-evidence
validator for public repositories. It contains no product code, credentials,
private repository data, or deployment logic.

Callers must pin `attest-governance-evidence.yml` to a full commit SHA, grant only
`contents: read` and `pull-requests: read`, and never check out or execute PR code
from a `pull_request_target` workflow. The validator reads PR metadata and evidence
through the GitHub API and treats every PR file as untrusted data.

The initial workflow blob is byte-identical to the independently reviewed
governance validator with SHA-256
`231814f8b9b7725e18da918a2643a88d3c8b8894f5672a6696f7928903f548a4`.
Future callers must pin this repository to a full commit SHA; a changed workflow
requires its own fixed-SHA review before callers update their pins.

The workflow validates evidence provenance and routing; it does not authenticate a
semantic code review, production deployment, or business acceptance.
