<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Cell sorting machine / 电芯分选机

Route cells into configurable output categories.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: receive and identify a cell, obtain a selected category from a demo result, index a transfer mechanism and direct the cell to a matching lane or reject outlet. Grade definitions and test functions are not inferred.

**Master scope.** Multi-lane sorting line.

**Typical design envelope (m, width × height × flow length):** 3–10 × 2–5 × 5–22. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `sorting-machine-01`. References are for visual context only; physical units remain unverified.

**Merged evidence.** The reference shows an elongated main transfer route and repeated transverse branches. The visible pattern supports configurable outlet lanes, not a verified number of grades. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 3–10 × 0.1–0.6 × 5–22 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 3–10 × 1–5 × 5–22 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Guard enclosure and panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 2–16 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 2–12 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Main transport lane / 主输送道 | Carries incoming cells through the sorter. | 1–1 | 0.4–2 × 0.1–0.8 × 2–12 | main line | revolute | running, idle, fault; quality result as configured | cell-in | L: functional placeholder |
| B10 | Identification module / 身份识别模块 | Generic cell identity pickup. | 1–2 | 0.1–0.6 × 0.1–0.8 × 0.1–0.6 | entry | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B11 | Cross-transfer carriage / 横移分选滑台 | Moves cells toward selected lanes. | 1–3 | 0.5–3 × 0.2–1.5 × 0.5–4 | over main line | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B12 | Cell divert gates / 电芯分流挡板 | Optional short-stroke route selection. | 2–8 | 0.05–0.4 × 0.05–0.5 × 0.1–0.5 | lane junctions | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B13 | Output lane modules / 分选输出通道 | Defines repeatable grade destinations. | 2–8 | 0.3–1.5 × 0.1–0.8 × 1–4 | side branches | revolute | running, idle, fault; quality result as configured | grade-out | M: external form; function assumed |
| B14 | Reject collection module / 不良收集模块 | Optional reject destination. | 0–1 | 0.3–1.5 × 0.3–1.5 × 0.3–1.5 | end or side outlet | fixed | running, idle, fault; quality result as configured | reject-out | L: functional placeholder |

## Variant rules

- Select the module scope and optional rows before authoring the default master.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B09` Main transport lane: revolute; demonstration joint motion; not measured kinematics.
- `B11` Cross-transfer carriage: prismatic; demonstration joint motion; not measured kinematics.
- `B12` Cell divert gates: revolute; demonstration joint motion; not measured kinematics.
- `B13` Output lane modules: revolute; demonstration joint motion; not measured kinematics.

## State slots

These are application visualization slots, not controller logic or a validated operating procedure. `NG-reject` changes routing only on variants with an explicitly authored reject route. Do not animate service leaves during a running cycle.

- `idle`: Ready/inactive illustration; no process motion.
- `running`: Generic process demonstration. No real cycle time or controller logic.
- `fault`: Illustrative fault indication; hold process joints.
- `NG-reject`: Optional failed-quality result; route only where the configured variant has a reject mechanism.
- `maintenance`: Demonstration access pose, disconnected from process motion.
- `loading`: Generic incoming material handoff.
- `unloading`: Generic outgoing material handoff.
- `routing`: ASSUMED generic routing visualization slot; no measured timing or recipe.

## Sockets

Attachment nodes are authored from the generic envelope. No source positions, connector standards, pipe bores, voltage ratings or exact mating geometry are supplied. Default material flow is +Z with +Y up; +X is the service/operator side. Re-map any imported prototype axes explicitly.

| Socket | Type / direction | Generic location |
|---|---|---|
| `air-in` | utility / in | service face |
| `cell-in` | material / in | entry boundary |
| `data` | utility / service | service face |
| `grade-out` | material / out | configurable side branch |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |
| `reject-out` | material / out | configurable side branch |

## Modelling notes

Keep the main spine and repeated branch rhythm. Use per-lane state/occupancy; do not bake names, grade labels or project-specific lane counts into geometry.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.
