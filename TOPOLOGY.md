<!--
SPDX-License-Identifier: MPL-2.0
Copyright (c) Jonathan D.A. Jewell <j.d.a.jewell@open.ac.uk>
-->
<!-- Copyright (c) 2026 Jonathan D.A. Jewell (hyperpolymath) <j.d.a.jewell@open.ac.uk> -->

# TOPOLOGY.md — refugia

## Purpose

Kea is a curiosity-driven, post-platform security ecosystem addressing the Surveillance Paradox. It provides distributed, high-assurance architecture for separating administration from runtime, assembling fragmented security logic across 165+ repositories into a cohesive, auditable system with formal verification and policy-as-code.

## Module Map

```
refugia/
├── contractiles/        # Declarative security orchestration modules
├── .machine_readable/   # Checkpoint files (state, ecosystem, metadata)
├── .bot_directives/     # Bot behavior configuration
├── flake.nix           # Nix environment and build definition
└── .github/workflows/   # CI/CD pipelines (security scanning, etc.)
```

## Data Flow

```
[Security Policy] ──► [Policy Engine] ──► [Compliance Check] ──► [Audit Report]
                           ↓
                   [Distributed Agents] ──► [Enforcement]
```

## Core Problems Addressed

- **Static Panopticons**: Dynamic threat response vs. rigid surveillance
- **Platform Dependency**: Post-platform architecture, vendor independence
- **Artifact Fragmentation**: Unified security logic across ecosystem
