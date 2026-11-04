# Parametric equipment masters

Reference GLBs and generic assembly BOMs are starting evidence. The longer-term goal is rebuildable equipment, real consumer-state-driven parts and a verified manufacturing flow. These are separate stages; publishing this plan does not assign every equipment kind, certify dynamic readiness or invalidate accepted static work. Existing static tasks and platform quality work continue in parallel.

## Three layers and evidence

- **Generic parameter source:** reusable author-owned geometry generation, parameter definitions and candidate component capabilities.
- **Vertical equipment template:** domain-specific module choices, constraints and assumptions, such as battery equipment. Generic design ranges are priors, not manufacturer-certified operating domains.
- **Project instance:** approved fitting, exact dimensions and project subject/relation semantics remain in the authorized project environment. Restricted customer data never enters the public template.

Reference units remain unverified until established per source. Record dimension ranges and their source, method and confidence separately from visual functional classification confidence. Do not infer engineering dimensions from a plausible silhouette or apply a blanket conversion. Public materials omit customer identifiers, exact project counts, private paths and restricted source mappings. Public reference access does not grant new model, source, texture or cross-client rights.

## Parametric delivery

A parametric submission includes a rebuildable Blender source and generation script, documented invocation/dependencies, parameter definitions and a selected lossless `.blend`/GLB output for each agreed demonstration set. Document every parameter's name, type, unit, default, supported values/range, constraints, source and truth (measured, declared or synthetic/assumed). Distinguish a demonstrated finite set from a general supported engineering domain.

Bind the exact parameter file, source scripts/dependencies and generated outputs with bytes and SHA-256 provenance. Record author-confirmed identity/version, generator version and relevant spec commit. Preserve earlier outputs; new draft variants remain traceable to the stable source asset and never overwrite accepted originals. Byte-identical rendering or rebuild output is not implied unless explicitly supported and tested.

Parameter changes must actually regenerate appropriate geometry and update dependent frame, enclosure and supports, movable-node positions, local axes/pivots and interface candidate points. Preserve semantic component names and topology intent; describe any deliberate topology change. Root negative or non-uniform scaling alone does not demonstrate parameterization. Final GLB is metres, +Y up and +Z front; document axes and points in final GLB coordinates.

Quality masters have no runtime triangle budget. Authors do not need to produce LODs, meshopt or KTX2/compressed runtime files. Platform derivation and consumer compatibility are separate evidence; no new service API or runtime wire format is introduced here.

## Parameter source to consumer behavior

Use the existing [data-driven animation tables](data-driven-animation.md) for each device. Link each geometry parameter and candidate capability to the relevant parameter source/output digest; distinguish a **candidate capability** from an **actually consumed state**. The record covers source, type, unit, supported range, initial/missing/stale/reset behavior, stable node/clip mapping, local axis and pivot, limits, timing/interpolation and required derivation preservation. Where unavailable, write “pending owner confirmation” in the document. Do not invent ABI slots, subtypes, sockets or unknown encodings.

GLB exposes geometry and nodes, and clips only where agreed. Process scheduling, material-flow decisions and data logic belong to the consumer. Retrieve production assets through Library exact version plus digest/provenance; a static PASS or format-valid GLB does not establish dynamic usability. Consumer behavior and LOD node fidelity must be checked against actual supported capabilities.

Application inventory/contract evidence is owned by the actual consumer owner. **FACTORY-INV1 is delivered and read**: [docs/FACTORY-INV1.md at 09e58265b5a841b0e4cf26a16f45bccc27f48fc4](https://github.com/hsudatalks/univers-ext-factory/blob/09e58265b5a841b0e4cf26a16f45bccc27f48fc4/docs/FACTORY-INV1.md). It is a source inventory marked PARTIAL, not scenario acceptance or installed-package proof. The earlier roughly two-hour ETA is historical.

At that historical pin, the inventory identifies four generic ASSUMED kinds (`factory.site`, `factory.production-line`, `factory.machine`, `factory.buffer`) and seven generated state channels; example values are not declared engineering limits. The panel has no TTL/expiry decision. Missing later business keys remain unchanged in the player until a new value; no business freshness timeout or automatic stop is supplied. Native reset/default handling is separate, and text-fact validity is a separate supported path. Existing native node/clip/textSlot source contracts are listed in the inventory, but **factory business slot→node/clip mapping was absent at that inventory pin**; the later Apps publication notice below supplies business kind/field semantics, without proving asset bindings. Aggregate WIP is not per-cell flow; generic relation events are not formal OK/NG/rework/scrap semantics. All four proposed chain scenarios remain untested.

The delivery-owned `battery-chain1-spec` is now reported pinned at **3ec1c5c1**. Models plus platform own the three-family parameter masters/template parameter binding (G4) and actual runtime pins, per-LOD and node-preservation evidence (G5). Earlier master drafts do not satisfy runtime acceptance. Conveyor, bare-cell inspection and sorting remain three families; the coater exercise adds no chain family. Static handoffs and the separately scoped phase2a work do not establish dynamic G4/G5 acceptance.

## Apps publication notice: factory.11

Source: Apps formal publication notice, `@univers/ext-factory@0.3.0-dev.factory.11`, reported source **cbf487d4**, inbox **c25199c8**, aligned with `battery-chain1-spec` **3ec1c5c1**. These are the supplied short pins, not invented full commit hashes. The full npm package/source was not read or independently tested for this update.

| Published kind | Fields / units / declared constraints |
| --- | --- |
| `factory.conveyor` | `speed`: m/s, ≥0; `occupancy`: integer |
| `factory.inspection-machine` | `cycleTime`: s, ≥0; `headStroke`: signed m |
| `factory.sorter` | `flow`: 1/h, ≥0; `diverterAngle`: rad |
| `factory.lane` | `occupancy`, `capacity`: integers; occupancy ≤ capacity |
| `factory.cell` | `serial`: text; `quality`: uninspected / OK / NG |

Inherited fields include `powerkW` and the state values off/running/fault. The notice specifies that `headStroke` drives the real inspection head and `diverterAngle` drives the diverter. These kind/field meanings are no longer all pending. Source-field selection, hardware limits, exact asset node bindings and runtime evidence remain unconfirmed; this table creates no wire schema, ABI binding, TTL rule or completed implementation. It does not apply the factory contract to the separate coater.

Current supplements: [conveyor phase2a inventory](briefs/factory-roller-conveyor-phase2a.md), [sorter phase2a layout](briefs/factory-sorter-production-layout-phase2a.md), [coater phase2](briefs/coater-parametric-phase2.md).

## Staged manufacturing-flow acceptance

1. **Rebuildable source:** verify the agreed parameter sets, measured bounds, dependent geometry/nodes/pivots and source/parameter/output provenance. Static scope remains explicitly static.
2. **Consumer mapping:** use the delivered inventory and existing contracts to identify supported state/action mappings. No claim that every equipment kind already has implemented dynamic contracts.
3. **One short replayable chain:** delivery selects and finally accepts the short chain. Before the project owner confirms the process, label it **ASSUMED TEST**; do not prescribe a complete real production order or material-field schema. Exercise normal flow plus stop/fault and recovery: upstream material handoff → this device's infeed/work-in-process/action feedback → outfeed/quality routing → downstream receipt and feedback. The chain selection, real project subjects and relations belong to delivery/project owners.
4. **Behavior evidence:** preserve pinned inputs/timestamps and expected/actual results for missing/stale data, initial/reset/seek and replay, plus LOD node/pivot fidelity where supported by the existing consumer. Record unsupported or untested cases accurately. A good screenshot or PBR appearance is useful visual evidence, not evidence of the complete flow.
5. **Project fit and expansion:** only after the relevant evidence and authorization, extend to approved project instances and additional equipment/steps. No blanket batch remake, immediate dynamic acceptance or new interface gate follows from this plan.

Use the [parametric task template](../templates/parametric-equipment-task.md) and [model task template](../templates/model-task.md). A deliberately static parameter-source demonstration is valid within its agreed scope while runtime contracts remain pending.
