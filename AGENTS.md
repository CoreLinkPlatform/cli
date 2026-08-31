# CoreLink CLI Agent Context

This repository is part of the CoreLink product.

## Canonical context

Follow `CoreLinkPlatform/product-planning/AGENTS.md`, `PRODUCT_ARCHITECTURE.md`, `GLOSSARY.md`, `STANDARDS.md`, and `architecture/repository-map.yaml`. Public API behavior is normative in `CoreLinkPlatform/api-contracts`.

## Repository responsibility

`cli` owns the supported command-line developer/operator interface for CoreLink public and explicitly supported operational workflows.

## Boundaries

- Prefer supported CoreLink APIs and contracts over direct database or provider access.
- Do not expose internal provider credentials or identifiers as normal user concepts.
- Commands and output terminology must follow the canonical glossary.
- Destructive or privileged operations must be explicit, auditable where applicable, and require appropriate authorization.
- Do not move business logic into the CLI when it belongs in platform services.
