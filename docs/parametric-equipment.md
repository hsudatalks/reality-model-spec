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

Application inventory/contract evidence is owned by the actual consumer owner. **FACTORY-INV1** is pending: fill the repository path and commit after delivery, together with existing kinds/data, slot provenance/units/ranges/missing/stale behavior, existing node/clip contract paths and existing material flow. Unknowns retain an owner and pending status. A reported roughly two-hour research ETA is an owner estimate, not a delivery guarantee. Historical message aliases are not verified owners, threads or dependencies.

## Staged manufacturing-flow acceptance

1. **Rebuildable source:** verify the agreed parameter sets, measured bounds, dependent geometry/nodes/pivots and source/parameter/output provenance. Static scope remains explicitly static.
2. **Consumer mapping:** use the delivered inventory and existing contracts to identify supported state/action mappings. No claim that every equipment kind already has implemented dynamic contracts.
3. **One short replayable chain:** delivery selects and finally accepts the short chain. Before the project owner confirms the process, label it **ASSUMED TEST**; do not prescribe a complete real production order or material-field schema. Exercise normal flow plus stop/fault and recovery: upstream material handoff → this device's infeed/work-in-process/action feedback → outfeed/quality routing → downstream receipt and feedback. The chain selection, real project subjects and relations belong to delivery/project owners.
4. **Behavior evidence:** preserve pinned inputs/timestamps and expected/actual results for missing/stale data, initial/reset/seek and replay, plus LOD node/pivot fidelity where supported by the existing consumer. Record unsupported or untested cases accurately. A good screenshot or PBR appearance is useful visual evidence, not evidence of the complete flow.
5. **Project fit and expansion:** only after the relevant evidence and authorization, extend to approved project instances and additional equipment/steps. No blanket batch remake, immediate dynamic acceptance or new interface gate follows from this plan.

Use the [parametric task template](../templates/parametric-equipment-task.md) and [model task template](../templates/model-task.md). A deliberately static parameter-source demonstration is valid within its agreed scope while runtime contracts remain pending.
