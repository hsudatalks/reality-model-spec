<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Actual consumer owners must confirm the existing contract path and commit; historical message aliases do not establish an owner. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Generic equipment master briefs

24 classified kinds are drafted from 64 classified released references. Three additional released references retain their original unknown IDs and now have supplementary ASSUMED visual classifications; three other exported variants remain withheld. Each brief has one assembly BOM per kind, a generic process, broad dimension ranges, configurable quantities, motion groups, application states, sockets and LOD guidance. These are reviewable generic design drafts; no manufacturing BOM or unit certificate is implied.

**Read before modelling:** all hidden internals, kinematics, process recipes and exact quantities are assumptions. Reference physical units remain unverified. Generic masters must be authored directly in metres; reference envelopes must not set the final master dimensions. Large arrays, full lines, head/tail modules and single stations are explicitly separated in scope.

| Priority | Kind | Brief | BOM | Released refs | Assembly rows |
|---:|---|---|---|---:|---:|
| 1 | coater | [coater.md](coater.md) | embedded in brief | 2 | 16 |
| 2 | calender-slitter | [calender-slitter.md](calender-slitter.md) | embedded in brief | 3 | 16 |
| 3 | slitter | [slitter.md](slitter.md) | embedded in brief | 2 | 16 |
| 4 | winder | [winder.md](winder.md) | embedded in brief | 2 | 16 |
| 5 | hot-press | [hot-press.md](hot-press.md) | embedded in brief | 2 | 15 |
| 6 | filler | [filler.md](filler.md) | embedded in brief | 2 | 16 |
| 7 | formation-aging-rack | [formation-aging-rack.md](formation-aging-rack.md) | embedded in brief | 3 | 16 |
| 8 | inspection-machine | [inspection-machine.md](inspection-machine.md) | embedded in brief | 6 | 19 |
| 9 | slurry-mixer | [slurry-mixer.md](slurry-mixer.md) | embedded in brief | 7 | 16 |
| 10 | drying-oven | [drying-oven.md](drying-oven.md) | embedded in brief | 1 | 14 |
| 11 | baking-oven | [baking-oven.md](baking-oven.md) | embedded in brief | 1 | 14 |
| 12 | rewinder | [rewinder.md](rewinder.md) | embedded in brief | 1 | 14 |
| 13 | welding-machine | [welding-machine.md](welding-machine.md) | embedded in brief | 6 | 16 |
| 14 | wrapping-machine | [wrapping-machine.md](wrapping-machine.md) | embedded in brief | 2 | 17 |
| 15 | pairing-machine | [pairing-machine.md](pairing-machine.md) | embedded in brief | 3 | 15 |
| 16 | sorting-machine | [sorting-machine.md](sorting-machine.md) | embedded in brief | 1 | 14 |
| 17 | nitrogen-filling-machine | [nitrogen-filling-machine.md](nitrogen-filling-machine.md) | embedded in brief | 2 | 13 |
| 18 | pin-insertion-machine | [pin-insertion-machine.md](pin-insertion-machine.md) | embedded in brief | 1 | 14 |
| 19 | pin-removal-machine | [pin-removal-machine.md](pin-removal-machine.md) | embedded in brief | 1 | 14 |
| 20 | cleaning-machine | [cleaning-machine.md](cleaning-machine.md) | embedded in brief | 1 | 14 |
| 21 | vertical-lift | [vertical-lift.md](vertical-lift.md) | embedded in brief | 4 | 15 |
| 22 | conveyor | [conveyor.md](conveyor.md) | embedded in brief | 2 | 14 |
| 23 | dust-collection-system | [dust-collection-system.md](dust-collection-system.md) | embedded in brief | 8 | 16 |
| 24 | solvent-recovery-system | [solvent-recovery-system.md](solvent-recovery-system.md) | embedded in brief | 1 | 15 |

## Remaining / held

- **Stacker:** no stacker kind or released stacker reference is present in the supplied index. No reference-backed stacker BOM issued. A separate synthetic baseline brief is available: [stacker.md](stacker.md). It is not reference-backed.
- **Unknown:** the three originally unclassified references now have supplementary visual hypotheses below. Their original IDs/index are retained; no common functional BOM is invented for this bucket. No withheld references are included in any brief.

## Handoff contract

- The source handoff describes these row keys: `id`, `name_en`, `name_zh`, `function`, `qty`, `approx_dims_m`, `location`, `movable`, `joint_type`, `state_relevance`, `interfaces`, `confidence`, `evidence_scope` and `label_status`.
- `qty` is a generic configurable default. the quantity and dimension ranges shown in each brief are generic design ranges, never fitted measurements.
- `joint`, `states`, `sockets` and `evidence` are candidate authoring notes, not runtime contracts. Optional modules default to zero; select one technology where alternatives are described.
- No source meshes, source textures, exact fitted dimensions, source block names, raw filenames or project labels are part of this handoff. All source-to-master fitting remains local.
- These are prepared review drafts; publishing is a separate decision.

Review the process variant, module scope and motion assumptions before building each master.

## Evidence limitations

Delivery reports 70 references: 10 drawing matches (8 footprint, 2 outline), 60 assumed; 11 medium, 59 low, 0 high. This is the delivery author report, not an independent engineering audit. A match is not engineering approval. All reference units remain unverified. No uniform 0.1 transform is justified. No drawing, source archive, private mapping or fitted instance is included.

The 24 embedded BOM tables total 365 rows. The separate synthetic stacker is not part of this count. The three held variants are not used in these briefs. Source handoff JSON files are not included; the tables in these briefs are the delivered review content.

## Parameter sources and supplementary visual hypotheses

Continue through [parametric equipment](../../parametric-equipment.md) and its [task supplement](../../../templates/parametric-equipment-task.md); the [coater phase-1 source demonstration](../coater-parametric-phase1.md) is a finite static scope, now author-reported locally complete after ACK (not independently received/accepted). These briefs are starting candidates, not 24 claimed tasks or implemented dynamic contracts. Existing static acceptance and platform quality work continue.

The original three `unknown-*` classifications at 0.25 remain historical. Delivery has since supplied visual ASSUMED proposals, accepted provisionally by the coordinator (no independent re-review): unknown-01 → vertical lift/two-level transfer (0.6; two-level buffer alternative); unknown-02 → conveyor (0.9); unknown-03 → slurry-mixer feed/dosing **subassembly** (0.5). See the relevant briefs and [release directory note](../../reference-exports/industrial-20261104.md). Safe IDs, source/public digests, files and original index are unchanged. Classification confidence is separate from physical units/dimensions, which remain unverified. No added BOM rows, rights or Library tags follow from these proposals. Actual contract owners and their path/commit must be confirmed; historical “85” is an old message alias, not a verified dependency.


## Short-chain family scope

The delivery-selected proposal is **conveyor → bare-cell inspection → sorting (OK/NG lanes) → conveyor**, with three equipment families only. In/out conveyors are instances of one template. See the [finite conveyor master brief](../factory-roller-conveyor-parametric.md), awaiting author ACK. Inspection first considers an existing template pending safe handoff; sorting is proposed to Legion, awaiting ACK. The coater source exercise is independent and adds no fourth chain family. Final geometry/joint/interface candidates and acceptance await the pinned `battery-chain1-spec`; this is not proof of implemented business flow or a commitment to produce all 24 kinds.

The [finite dual-outlet sorter brief](../factory-sorter-parametric.md) assigns a proposed scope to Legion, awaiting ACK: two outlet-spacing values within one fixed-envelope template. It does not implement OK/NG semantics or add another chain family.
