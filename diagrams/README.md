# Integration diagrams

Each DOT/SVG pair has one purpose. Edges show required logical dependencies, not deployed services, placement, completion or passing evidence.

| View | DOT source | Generated SVG |
| --- | --- | --- |
| Initial limited integration | [Source](dependencies/initial-integration.dot) | [View](artefacts/initial-integration.svg) |
| Full acceptance | [Source](dependencies/full-acceptance.dot) | [View](artefacts/full-acceptance.svg) |
| Custody topology | [Source](dependencies/custody-topology.dot) | [View](artefacts/custody-topology.svg) |

Use Graphviz from the repository root:

```sh
dot -V
dot -Tsvg diagrams/dependencies/initial-integration.dot -o diagrams/artefacts/initial-integration.svg
dot -Tsvg diagrams/dependencies/full-acceptance.dot -o diagrams/artefacts/full-acceptance.svg
dot -Tsvg diagrams/dependencies/custody-topology.dot -o diagrams/artefacts/custody-topology.svg
```

Inspect rendered labels and metadata after edits. Dashed custody edges are later/conditional scopes: ordinary manager operations do not consume the initial custodian. The initial executor/result joins remain explicit dependencies. A render proves syntax acceptance only; native custody, stop, signing and qualified-time behavior require independent evidence. No minimum renderer version or runtime qualification is asserted.
