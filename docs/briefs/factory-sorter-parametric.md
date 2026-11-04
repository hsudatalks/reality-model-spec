# Generic dual-outlet sorter parameter master — phase 1

**Task:** `FACTORY-SORTING/parametric-master-phase1`, priority P1, proposed author Legion. **Status: awaiting_ack**, not claimed or started. This is the sorting family already included in the three-family chain, not a fourth family or two separate outlet devices. The earlier filtration-skid handoff remains received with its author identity/DRAFT version and pending rights unchanged; no new supplement is requested for it. Historical research candidates remain outside this task.

An original **synthetic** static dual-outlet diverter/sorter template, proposed for `battery-chain1`; no claim of real machinery or implemented OK/NG business behavior. Sources are this original synthetic brief and the [fixed generic sorting-machine reference brief](https://github.com/hsudatalks/reality-model-spec/blob/51e37552c920ec74cd0631acc306d951b637ec79/docs/briefs/industrial-bom/sorting-machine.md). Use the actual `sorting-machine.md` path. No customer CAD/source or another author's geometry is allowed.

## Finite parameter scope

| Item | Required synthetic definition |
| --- | --- |
| Fixed complete envelope | X=2.4 m, Y=1.2 m, Z=3.0 m |
| Only demonstration parameter | `outlet_spacing_X_m`, number/metres; default 1.2, supported values **{1.2,1.6}** only |
| Outlet centres | `[-S/2,0.8,+1.5]` and `[+S/2,0.8,+1.5]` |
| Inlet geometric reference | `[0,0.8,-1.5]`, fixed |
| Outlet candidate names | `lane_a`, `lane_b`; **not formal OK/NG sockets** |
| Diverter candidate pivot/axis | `[0,0.8,0]`, local Y; record zero pose/candidate axis only, no rotation, invented limits or control mapping |
| Coordinates/origin | Metres, +Y up, +Z inlet-to-outlet direction, complete AABB bottom-centre Ymin=0 |

These are two demonstrated sets, not a certified continuous engineering range. Use separate ASCII semantic nodes: `base_frame`, `infeed_deck`, `lane_a_deck`, `lane_b_deck`, `diverter`, individual side guides and `support_legs`; record actual local pivots. As S changes, regenerate outlet support surfaces, side guides and branch-junction geometry together. Keep the inlet, outer frame and complete bottom-AABB centre fixed; locate legs correctly beneath their supporting structures. Root non-uniform scaling does not demonstrate regeneration. No mechanical load, collision or process certification is required.

## Deliverables and exclusions

Supply parameter type/unit/default/finite support/constraints/source-truth documentation, rebuildable source/dependencies/invocation, and lossless blend/GLB outputs for both sets. Report measured complete bounds, outlet positions, diverter pivot/axis and coupling behavior for each set. Bind every file with bytes/SHA-256 and include the necessary official Validator 0-error reports tied to output SHA. No whole-domain fuzzing or repeated rendering is required; untested state/consumer acceptance remains pending.

Use the author's own neutral PBR, no brand mesh text or baked scene/state appearance. No rig, animation, LOD, compression, scheduling, real OK/NG decisions or added moving electrical/detection/sensor/gripper behavior. Master quality is not constrained by runtime budgets. Align actual geometry/joint/interface declarations after delivery supplies the pinned `battery-chain1-spec`; do not invent runtime wire formats or ABI slots.

Candidate source identity: `legion-generic-battery-sorter@0.1.0`, subject to the author's traceable draft output identities. Deliver under the author's existing authorized Legion directory `FACTORY-SORTING/<author-version>/DRAFT/`; do not overwrite earlier assets, alter permissions or infer public/cross-client licensing. This public brief grants no additional asset rights.

See [parametric equipment](../parametric-equipment.md) and the [parameter task supplement](../../templates/parametric-equipment-task.md).
