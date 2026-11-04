<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Actual consumer owners must confirm the existing contract path and commit; historical message aliases do not establish an owner. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Electrode slurry mixing system / 极片制浆系统

Combine powder, binder and liquid into a process slurry.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: feed powders and liquid to one or more vessels, mix/disperse, optionally condition or de-air, then transfer slurry through generic service modules. Order of addition, chemistry, batch size and mixer internals are not inferred.

**Master scope.** Single mixing skid or tower module. Large installation arrays are layout context, not one equipment master.

**Typical design envelope (m, width × height × flow length):** 2–10 × 3–12 × 2–12. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `slurry-mixer-01`, `slurry-mixer-02`, `slurry-mixer-03`, `slurry-mixer-04`, `slurry-mixer-05`, `slurry-mixer-06`, `slurry-mixer-07`. References are for visual context only; physical units remain unverified.

**Merged evidence.** Seven references span isolated tank/skid forms, twin-vessel arrangements and very large repeated installation arrays. Circular vessel silhouettes, upper drives and repeated supports are visible; the arrays must not determine generic vessel quantities. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 2–10 × 0.1–0.6 × 2–12 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 2–10 × 1.5–12 × 2–12 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Local guards and service panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 0–12 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 0–8 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Mixing vessel / 搅拌罐 | Defines a generic principal process vessel. | 1–3 | 1–4 × 1.5–5 × 1–4 | main skid/tower | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B10 | Upper drive housing / 顶部驱动箱 | Represents a generic mixer drive. | 1–3 | 0.3–1.5 × 0.3–2 × 0.3–1.5 | above vessel | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B11 | Agitator shaft placeholder / 搅拌轴占位件 | Optional illustrative internal mixing axis. | 1–3 | 0.05–0.3 × 0.5–3 × 0.05–0.3 | inside vessel | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B12 | Powder feed hopper / 粉料投料斗 | Represents a generic powder interface. | 1–3 | 0.5–2.5 × 0.5–3 × 0.5–2.5 | above/adjacent vessel | fixed | running, idle, fault; quality result as configured | powder-in | L: functional placeholder |
| B13 | Liquid service manifold / 液体服务歧管 | Represents generic liquid feed. | 1–2 | 0.2–1.5 × 0.2–1.5 × 0.2–1.5 | vessel service side | fixed | running, idle, fault; quality result as configured | liquid-in | L: functional placeholder |
| B14 | Transfer pump/filter skid / 输送过滤模块 | Represents downstream slurry transfer. | 1–2 | 0.5–2.5 × 0.5–2 × 0.5–3 | lower side | fixed | running, idle, fault; quality result as configured | slurry-out, drain-out | L: functional placeholder |
| B15 | Optional de-airing vessel / 可选脱泡罐 | Selectable conditioning stage. | 0–2 | 0.5–2.5 × 1–3 × 0.5–2.5 | adjacent process bay | fixed | running, idle, fault; quality result as configured | vacuum-out | L: functional placeholder |
| B16 | Service platform and ladder / 检修平台爬梯 | Optional access for a tall mixer tower. | 0–2 | 1–6 × 1–10 × 1–6 | around upper vessel | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |

## Variant rules

- Select isolated vessel, twin-vessel skid or tower module. Compose arrays with separate instances; do not stretch one master to an installation envelope.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B11` Agitator shaft placeholder: revolute; demonstration joint motion; not measured kinematics.

## State slots

These are application visualization slots, not controller logic or a validated operating procedure. `NG-reject` changes routing only on variants with an explicitly authored reject route. Do not animate service leaves during a running cycle.

- `idle`: Ready/inactive illustration; no process motion.
- `running`: Generic process demonstration. No real cycle time or controller logic.
- `fault`: Illustrative fault indication; hold process joints.
- `NG-reject`: Optional failed-quality result; route only where the configured variant has a reject mechanism.
- `maintenance`: Demonstration access pose, disconnected from process motion.
- `loading`: Generic incoming material handoff.
- `unloading`: Generic outgoing material handoff.
- `mixing`: ASSUMED generic mixing visualization slot; no measured timing or recipe.
- `transferring`: ASSUMED generic transferring visualization slot; no measured timing or recipe.

## Sockets

Attachment nodes are authored from the generic envelope. No source positions, connector standards, pipe bores, voltage ratings or exact mating geometry are supplied. Default material flow is +Z with +Y up; +X is the service/operator side. Re-map any imported prototype axes explicitly.

| Socket | Type / direction | Generic location |
|---|---|---|
| `air-in` | utility / in | service face |
| `data` | utility / service | service face |
| `drain-out` | fluid / out | service face |
| `liquid-in` | fluid / in | service face |
| `operator` | operator / service | service face |
| `powder-in` | material / in | entry boundary |
| `power-in` | utility / in | service face |
| `slurry-out` | fluid / out | service face |
| `vacuum-out` | gas/duct / out | upper/service collar |

## Modelling notes

Offer single-vessel, twin-vessel and tower variants. Tanks, top drives and support levels are the key silhouette. Pipe routes and large array spacing must be newly designed, not traced.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.

## Supplementary visual classification (ASSUMED)

`unknown-03` → slurry-mixer feed/dosing station **subassembly**, visual classification confidence **0.5**: two platform levels, conical hoppers/dosing vessels and separate tank units. This does not prove a complete mixer or a specific real process.

Source: delivery's neutral-grey, edge and scale-bar visual inspection, provisionally accepted by the coordinator; no independent re-review here. The initial unknown classification at 0.25 is retained as history. Units and dimension confidence remain **unverified**, separately from the visual confidence above. This text does not alter safe IDs, source GLB SHA, filenames, original index, geometry, Library tags or rights. See the [release directory note](../../reference-exports/industrial-20261104.md).
