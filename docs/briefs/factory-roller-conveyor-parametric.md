# Generic roller conveyor parameter master — phase 1

**Task:** `FACTORY-CONVEYOR/parametric-master-phase1`, priority P1, proposed author Hidden. **Status: awaiting_ack**. This scope follows the author's request for another task; it is not an accepted or started production task. The earlier dock and camera scopes are unchanged.

Original generic synthetic roller-conveyor module, using only the author's own geometry and the existing neutral PBR style. Design reference: [fixed generic conveyor brief](https://github.com/hsudatalks/reality-model-spec/blob/51e37552c920ec74cd0631acc306d951b637ec79/docs/briefs/industrial-bom/conveyor.md). Do not use restricted customer material or reuse reference geometry. This is a synthetic parameter candidate awaiting the final pinned `battery-chain1-spec`; it is not formally usable by the chain yet. Infeed and outfeed use different instances of the same template, not two asset families.

## Exactly two demonstration sets

| Item | Definition / truth |
| --- | --- |
| Parameter | `length_Z_m`, number in metres; supported values **{3, 4}** only; default 3 |
| Fixed width / height | X=1.2 m, Y=0.8 m |
| Outputs | X/Y/Z = 1.2/0.8/3 m and 1.2/0.8/4 m |
| Roller radius / centre height | 0.05 m / Y=0.75 m |
| Roller pitch | 0.2 m |
| Roller Z centres | `-L/2 + 0.2 + i*0.2`, ending at `L/2 - 0.2`; i=0..13 for L=3, i=0..18 for L=4 |
| Derived roller counts | 14 / 19 respectively |
| Roller centre / candidate axis | `(0, 0.75, Z_i)`; pivot at centre; local X candidate rotation axis |
| Four leg positions | X=±0.45 m, Z=±(L/2−0.35) m; positions change with L; author records the actual vertical origin/geometry |
| Candidate infeed / outfeed points | `[0,0.8,-L/2]` / `[0,0.8,+L/2]`; geometry candidates, **not formal sockets** |
| Coordinate frame | Metres, +Y up, +Z conveyor length/flow candidate, full AABB bottom-centre Ymin=0 |

All values are **synthetic/assumed**, not manufacturer ranges, load ratings or a general engineering domain. Make two side frames, four legs, every roller and end caps separate semantic components. Regenerate frame lengths, roller count/centres, support positions and candidate interface points from L; preserve traceable component naming and topology intent. Root non-uniform scaling does not demonstrate regeneration.

## Deliverables and boundaries

Document the parameter type/unit/default/finite support/constraints/source truth; supply rebuildable Blender/generator source, dependencies and invocation, and both lossless `.blend`/GLB outputs. For each set report measured bbox, counts, roller centre/axis table, leg positions and candidate in/out points; bind parameters/source/outputs by bytes and SHA-256. Include the necessary official Validator reports with 0 errors bound to output SHA. No fuzz tests or repeated rendering are required.

Candidate source identity: `hidden-generic-roller-conveyor@0.1.0`; author confirms actual draft identity and traceable output variants without overwriting originals. Rights follow the existing authorized project-DRAFT scope, with no automatic open-source, public-redistribution or cross-client grant. Existing authorized Hidden delivery directory: `FACTORY-CONVEYOR/<author-version>/DRAFT`; the author follows existing delivery permission rather than changing access.

No animation, rig, state binding, process scheduling, LOD/compression or load certification is in this phase. Quality masters have no runtime triangle budget. Candidate capabilities are documented, not invented ABI slots. Actual source/parameter binding and G4 acceptance await the pinned chain spec; G5 needs real runtime versions/digests, per-LOD and node-preservation evidence from the platform. Previous master drafts are not runtime acceptance.

See [parametric equipment](../parametric-equipment.md) and the [task supplement](../../templates/parametric-equipment-task.md). This brief creates no new service interface or consumer wire format.
