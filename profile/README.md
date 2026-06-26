# Anchor Migration

**SSOT-driven toolkit for AI-assisted legacy modernization.**

An open engineering program demonstrating **architecture-led, AI-assisted development**: the developer defines system design and boundary protocols; AI implements most of the code; the product is **deterministic Python and Java** — reproducible, test-gated, and verifiable.

---

### How we build

| Human (developer) | AI (implementation partner) |
|-------------------|----------------------------|
| Architecture & repo boundaries | Feature code, tests, docs |
| Boundary protocols (SSOT schemas, entity keys, CLI contracts) | Dialect SQL, adapters, scaffolding |
| Acceptance criteria & merge decisions | Bulk implementation under those contracts |

**Deliverable rule:** core pipeline = 100% deterministic execution. Optional AI self-healing nodes may *suggest* fixes or tests, but never bypass export / verify gates.

→ [Full development model](https://github.com/anchor-migration/migration-hub/blob/main/docs/DEVELOPMENT-MODEL.md)

---

### Repositories

| Repository | Role | Status |
|------------|------|--------|
| [migration-hub](https://github.com/anchor-migration/migration-hub) | Program docs & architecture | Active |
| [db-metadata](https://github.com/anchor-migration/db-metadata) | Live DB → schema SSOT (SQLite) | Alpha |
| [java-ast-ssot](https://github.com/anchor-migration/java-ast-ssot) | Java source → Java AST SSOT | Alpha |
| rewrite-recipes | OpenRewrite rule catalog | Planned |
| parity-verify | Old vs new parity verification | Planned |
| pattern-catalog | Migration patterns (EJB → Spring, …) | Planned |

Schema + AST as ground truth · OpenRewrite for mechanical migration · AST + AI for bounded parity exploration

[Architecture · Roadmap · SSOT contracts →](https://github.com/anchor-migration/migration-hub)
