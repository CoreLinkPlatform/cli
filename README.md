# CoreLink CLI

The future command-line interface for CoreLink developers and operators.

## Current status

This repository is a scaffold; it contains no executable CLI, package manifest
or release artifact. Commands shown in external documentation must not claim
that this tool is installable until an implementation and versioned release are
published.

## Intended scope

- Authenticate with supported CoreLink OAuth flows.
- Select an explicit tenant and show the active context.
- Manage devices, provisioning and commands through the public API.
- Inspect safe operational state and validate configuration.
- Support automation-friendly output, error codes and non-interactive use.

## Implementation guardrails

- Generate or hand-write clients from reviewed `api-contracts` only.
- Require explicit tenant selection where token context is insufficient; never
  infer or bypass tenant boundaries.
- Do not accept, print or persist access tokens in shell history or logs.
- Keep operator-only commands separate from partner/public commands.
- Publish install, upgrade and compatibility instructions with each release.
