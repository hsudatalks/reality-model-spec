# Generic coater parameter-source demonstration — phase 1

**Task:** `P1-A1/parametric-source-phase1`, priority P1, author edge-01. **Status: author ACK followed by author-reported local completion**; no independent acceptance or receipt is implied. The original awaiting-ACK state is historical. This supplements the author's existing locally completed generic coater master. Preserve that original and the previous eleven locally completed items unchanged; this is not a twelfth completed item. The next master-production plan remains proposed, separately scoped and unauthorized until confirmed.

## Finite demonstration scope

| Parameter | Type / unit | Baseline/default | Only demonstration variant | Supported scope / truth |
| --- | --- | ---: | ---: | --- |
| `width_X` | positive number / m | 3 | 3 | These two exact sets only; synthetic/assumed |
| `height_Y` | positive number / m | 3 | 3 | These two exact sets only; synthetic/assumed |
| `length_Z` | positive number / m | 6 | 7.2 | These two exact sets only; synthetic/assumed |

The full supported set is `{(3,3,6), (3,3,7.2)}` in X/Y/Z metres. No arbitrary engineering domain, manufacturer range or real coater process is claimed. The table/script may be extensible without claiming untested ranges. Final GLB: +Y up, +Z front, full AABB bottom-centre with Ymin=0 and X/Z centred.

Reuse the author's own source and materials, without customer CAD or another author's geometry. Regenerate the appropriate frame, enclosure and support geometry/positions for the length change; update both reference roller centres and their local-X candidate axes together. Keep semantic component topology and names traceable (frame, housing, infeed/outfeed roller and coating-head exterior). Do not substitute negative/non-uniform root scaling for generation. The reference rollers and flow direction are synthetic visual choices, not a recovered coating process.

## Local evidence to report

- Rebuildable Blender/generation source and dependencies/invocation; documented parameters, defaults, finite supported sets, constraints and synthetic source truth.
- Lossless blend and GLB for both sets, measured final GLB bounds, and a roller-centre/local-axis table for both outputs. Include parameter/source/output bytes and SHA-256 provenance and the necessary official Validator reports with 0 errors, bound to actual output SHA. Do not require byte identity or repeated multi-view rendering.
- Preserve the stable original asset ID and record the author's traceable new draft variant output identities/versions; never overwrite the original. Update existing author production/delivery documentation and manifest rather than inventing parallel records.
- Describe candidate roller rotation in documentation only. Slot/consumer binding, action ranges and initial/missing/stale behavior remain pending FACTORY-INV1 and owner confirmation; no fake ABI fields. This phase has no real motion, rig, clips, slot binding, LOD or compression. Runtime budgets do not constrain the master.

**Permission:** local production only. No cloud directory creation, upload or change of sharing permissions; previous eleven items and new outputs retain existing delivery restrictions. No added public or cross-client reuse license. Report local progress/completion/blockers through the existing check-in process; actual transfer needs its existing separate authorization. The public brief itself conveys no rights in existing models or references.

See [parameter-source requirements](../parametric-equipment.md), [task supplement](../../templates/parametric-equipment-task.md) and [animation documentation](../data-driven-animation.md). Pending contracts do not block this static source demonstration.

## Author-reported local completion update

The author reports both finite sets rebuilt, coupled frame/enclosure/support and roller positions, no root non-uniform scale, and candidate roller centres `(0, 0.45*H, ±0.43*L)` with local-X axes. Both author Validator reports are 0 errors / 0 warnings / 64 unused-UV infos, with 32 file hashes reported. These are author checks of two sets, not an independently verified parameter domain. The original twenty files were preserved and nothing uploaded. The previous eleven original locally completed items remain eleven; one supplementary parameter-source scope is now author-reported complete, not twelve received assets or twelve new models. Delivery and rights restrictions remain unchanged.
