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
| [java-ast-ssot](https://github.com/anchor-migration/java-ast-ssot) | Java source → AST SSOT + profiles (`javaee-ejb2-jboss`, `jpa`, `mybatis`) + `classify-lists` | Alpha |
| [anchor-explorer](https://github.com/anchor-migration/anchor-explorer) | Read-only crosswalk UI | Alpha |
| [rewrite-recipes](https://github.com/anchor-migration/rewrite-recipes) | OpenRewrite catalog (stack + L1/L2/L3) | Alpha |
| [parity-verify](https://github.com/anchor-migration/parity-verify) | Before/after AST structural parity (JSON) | Alpha |
| [pattern-catalog](https://github.com/anchor-migration/pattern-catalog) | Migration patterns (EJB → Spring, …) | Planned |

Schema + AST as ground truth · OpenRewrite for mechanical migration · AST + AI for bounded parity exploration

---

### Program progress (2026-06)

| Phase | Status |
|-------|--------|
| Schema SSOT + Duke's Bank demo | ✅ Alpha |
| Java AST SSOT + crosswalk + Explorer E2E | ✅ Alpha |
| OpenRewrite stack migration (Session/CMP) | ✅ Duke's Bank fixtures |
| Language modernization ADR-008 (L1/L2/L3) | ✅ v1 spike complete |
| Parity verification | 📋 Next |

[Architecture · Roadmap · Start here →](https://github.com/anchor-migration/migration-hub)
