# Parametric equipment task supplement

This is a document template, not a runtime binding schema. Attach it to the [model task](model-task.md) only for an explicitly assigned parametric scope; see [parametric equipment](../docs/parametric-equipment.md).

| Record | Fill with actual evidence |
| --- | --- |
| Scope/status | Source task, author, awaiting ACK / claimed / completed; static demonstration or confirmed dynamic scope |
| Identity | Stable source asset, new draft output identities/versions and relationship to preserved originals |
| Parameter table | Name, type, unit, default, supported finite sets/ranges, constraints, source, truth/confidence |
| Rebuild | Blender/generator version, dependencies, invocation and source SHA-256 |
| Demonstration sets | Exact parameter files, their SHA-256 and generated lossless blend/GLB bytes/SHA-256 |
| Geometry coupling | Measured output bounds; affected frame/guards/supports; semantic topology/names; no root-scale substitute |
| Node coupling | Final GLB node paths, local axes/pivots/limits and candidate interface positions for each set |
| Behavior | Candidate versus consumed capability; linked animation table, actual consumer contract path/commit or owner-pending |
| Rights | Actual source/material permissions; no implied public/cross-client grant |
| Acceptance | Assigned finite scope, official format report bound to output SHA, untested/pending items |

For behavior use the existing [animation requirements](../docs/data-driven-animation.md), linking geometry parameters to the actual consumer input source without inventing ABI slots. No author LOD/compression or runtime triangle limit applies to lossless masters.
