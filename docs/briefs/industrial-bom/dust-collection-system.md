<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Industrial dust collection system / 工业除尘系统

Extract airborne process dust into a collection and filtration system.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: draw dust-laden air from local extraction points, separate or filter particulate, collect solids and discharge treated air. Filter media, explosion protection, airflow and duct sizing are not inferred.

**Master scope.** One collector skid; compose duct networks and multiple skids as separate layout objects.

**Typical design envelope (m, width × height × flow length):** 1.5–6 × 2–7 × 2–8. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `dust-collection-system-01`, `dust-collection-system-02`, `dust-collection-system-03`, `dust-collection-system-04`, `dust-collection-system-05`, `dust-collection-system-06`, `dust-collection-system-07`, `dust-collection-system-08`. References are for visual context only; physical units remain unverified.

**Merged evidence.** Eight references include cabinet/tower volumes, round duct-like branches and mixed grouped installations. Similar repeated variants inform a shared collector family; branch count and full network extents must remain configurable. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 1.5–6 × 0.1–0.6 × 2–8 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 1.5–6 × 1–7 × 2–8 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Local guards and service panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 0–12 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 0–8 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Filter housing / 过滤箱体 | Defines the principal collector volume. | 1–3 | 0.8–4 × 1–5 × 0.8–4 | main skid | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B10 | Filter cassette placeholder / 滤芯占位模块 | Optional removable internal filtration volume. | 1–12 | 0.2–1 × 0.3–2 × 0.2–1 | inside housing | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B11 | Collection hopper / 集尘灰斗 | Represents lower dust collection geometry. | 1–3 | 0.5–3 × 0.5–3 × 0.5–3 | below filter housing | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B12 | Dust collection bin / 集尘箱 | Represents removable solids collection. | 1–3 | 0.3–1.5 × 0.3–1.5 × 0.3–1.5 | hopper base | prismatic | running, idle, fault; quality result as configured | dust-bin-out | L: functional placeholder |
| B13 | Extraction fan housing / 抽风机壳 | Represents the air-moving module. | 1–2 | 0.4–2 × 0.4–2 × 0.4–2 | service side | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B14 | Duct trunk and branches / 抽风主管及支管 | Defines a generic modular air route. | 1–8 | 0.2–1.5 × 0.2–1.5 × 0.5–5 | around skid | fixed | running, idle, fault; quality result as configured | dust-air-in, clean-air-out | M: external form; function assumed |
| B15 | Service access doors / 滤箱检修门 | Provides access to generic filter modules. | 1–6 | 0.3–1.5 × 0.5–2 × 0.03–0.15 | filter housing sides | revolute | maintenance | — | L: functional placeholder |
| B16 | Pulse service manifold / 脉冲服务歧管 | Optional filter-cleaning service placeholder. | 0–2 | 0.2–1.5 × 0.2–0.8 × 0.2–1.5 | upper housing | fixed | running, idle, fault; quality result as configured | air-in | L: functional placeholder |

## Variant rules

- Select the module scope and optional rows before authoring the default master.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B12` Dust collection bin: prismatic; demonstration joint motion; not measured kinematics.
- `B13` Extraction fan housing: revolute; demonstration joint motion; not measured kinematics.
- `B15` Service access doors: revolute; service pose only.

## State slots

These are application visualization slots, not controller logic or a validated operating procedure. `NG-reject` changes routing only on variants with an explicitly authored reject route. Do not animate service leaves during a running cycle.

- `idle`: Ready/inactive illustration; no process motion.
- `running`: Generic process demonstration. No real cycle time or controller logic.
- `fault`: Illustrative fault indication; hold process joints.
- `NG-reject`: Optional failed-quality result; route only where the configured variant has a reject mechanism.
- `maintenance`: Demonstration access pose, disconnected from process motion.
- `loading`: Generic incoming material handoff.
- `unloading`: Generic outgoing material handoff.

## Sockets

Attachment nodes are authored from the generic envelope. No source positions, connector standards, pipe bores, voltage ratings or exact mating geometry are supplied. Default material flow is +Z with +Y up; +X is the service/operator side. Re-map any imported prototype axes explicitly.

| Socket | Type / direction | Generic location |
|---|---|---|
| `air-in` | utility / in | service face |
| `clean-air-out` | gas/duct / out | upper/service collar |
| `data` | utility / service | service face |
| `dust-air-in` | gas/duct / in | upper/service collar |
| `dust-bin-out` | material / out | exit boundary |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |

## Modelling notes

Silhouette depends on filter body, lower hopper, fan and a few major ducts. Avoid turning full duct networks into a single scalable collector mesh. No copied branch routing.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.

