# CoreLink CLI

> **Maturity: Scaffold / Planned** — this repository does not yet contain an executable CLI, package manifest, or supported release artifact.

CoreLink CLI is the planned command-line client for developer and operator workflows that are explicitly exposed through versioned CoreLink contracts.

## Planned responsibilities

- authenticate through supported CoreLink flows without unsafe token persistence;
- select/show explicit tenant context;
- inspect supported devices and other public resources;
- submit and inspect supported commands with correct idempotency semantics;
- provide safe diagnostics for configuration/API compatibility;
- support automation-friendly output, exit codes and non-interactive use;
- keep public/partner commands separate from privileged operator-only commands.

## Security rules

- Do not accept or persist secrets in shell history when safer input methods are available.
- Never infer or bypass tenant boundaries.
- Do not expose internal/provider credentials or IDs as public CLI contracts.
- Public commands must consume version-identifiable CoreLink contracts.
- Operator-only commands require an explicit ownership/security boundary and must not silently appear in the public client.

## Backlog

- [CLI-01](https://github.com/CoreLinkPlatform/cli/issues/3) — implementation stack and public/operator command boundary.
- [CLI-02](https://github.com/CoreLinkPlatform/cli/issues/2) — secure auth, tenant, device, command and diagnostics workflows.
- [CLI-03](https://github.com/CoreLinkPlatform/cli/issues/4) — cross-platform packaging, signing, documentation and conformance.

## Related sources

- [Developer docs](https://github.com/CoreLinkPlatform/developer-docs)
- [API contracts](https://github.com/CoreLinkPlatform/api-contracts)
- [Release policy](https://github.com/CoreLinkPlatform/.github/blob/main/RELEASE_POLICY.md)

Commands shown in external documentation must not be presented as installable until CLI-01/02/03 produce a real versioned artifact. When that happens, this README will add installation, upgrade, authentication and compatibility instructions.