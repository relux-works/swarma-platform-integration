# Swarma platform integration

Integration requirements and dependency planning for a qualified Swarma worker and the later signed-result trust chain. This repository contains documents, public source references and diagrams. It supplies no installer, service implementation, runtime harness or live deployment evidence.

The initial limited integration is one non-federated trusted Linux worker in an existing active station generation, using a qualified, owner-activated broker v0 worker-UID lease. The lease supplies credentials; it supplies no grant, binding or launch authority. A protected dispatcher launch policy, qualified caller authentication, shared independent custody, trusted time and whole-account stop remain separate requirements.

Full acceptance additionally requires narrowed grants, signed result delivery over Matrix, an independent verifier, current registry snapshots, freshness and external-root currency, expanded custody and complete security-revocation response. The limited integration does not satisfy those later predicates.

Start with the [integration plan](docs/integration-plan.md), [gates](docs/integration-gates.md), [ownership](docs/deployment-ownership.md), [activation proposal](docs/activation-proposal.md), [module gaps](docs/module-gaps.md), [status](docs/status.md) and [open questions](UNRESOLVED_QUESTIONS.md). Detailed constraints cover [authority events](docs/authority-lifecycle.md), [custody and recovery](docs/custody-and-recovery.md), [executor and results](docs/executor-and-results.md), [clocks and budgets](docs/clocks-and-budgets.md) and [host dependencies](docs/platform-host-dependencies.md). [Public source pins](docs/source-ledger.md) establish only source identity. [Three focused diagrams](diagrams/README.md) show required relationships rather than deployed placement.

## Tools and outputs

Run from the repository root. Graphviz is the only artifact build dependency; no minimum supported version is established here.

| Tool | Purpose and exact command | Output and limit |
| --- | --- | --- |
| Graphviz | `dot -V` | Installed renderer version; no host qualification |
| Graphviz | `dot -Tsvg diagrams/dependencies/initial-integration.dot -o diagrams/artefacts/initial-integration.svg` | Initial dependency view |
| Graphviz | `dot -Tsvg diagrams/dependencies/full-acceptance.dot -o diagrams/artefacts/full-acceptance.svg` | Full acceptance dependency view |
| Graphviz | `dot -Tsvg diagrams/dependencies/custody-topology.dot -o diagrams/artefacts/custody-topology.svg` | Logical custody topology |

The generated SVG files belong in `diagrams/artefacts/`. No public validation command or application test suite is supplied. Rendering confirms DOT acceptance; it does not establish semantics, privacy, installation, native qualification or runtime behavior. Source byte verification and migration privacy probes are separate preparation instruments and are not part of this public tool surface.

## License

[Apache License 2.0](LICENSE). Attribution is in [NOTICE](NOTICE).
