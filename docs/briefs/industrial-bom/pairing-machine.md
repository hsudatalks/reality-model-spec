<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Cell pairing machine / 电芯配对机

Arrange cells into matched groups according to upstream measurements.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: identify incoming cells, look up a configurable grouping result, buffer them, select compatible cells and transfer a group onward. Matching rules and any on-machine measurement are unverified.

**Master scope.** Cell buffering and grouping line.

**Typical design envelope (m, width × height × flow length):** 2–8 × 2–5 × 4–20. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `pairing-machine-01`, `pairing-machine-02`, `pairing-machine-03`. References are for visual context only; physical units remain unverified.

**Merged evidence.** Three references support elongated enclosures with a side buffer/service projection and mirrored or alternate arrangements. Internal grouping logic and buffer capacity are not geometry-derived. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 2–8 × 0.1–0.6 × 4–20 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 2–8 × 1–5 × 4–20 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Guard enclosure and panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 2–16 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 2–12 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Infeed lane / 上料输送道 | Receives individual cells. | 1–2 | 0.3–1.5 × 0.1–0.6 × 1–4 | entry | revolute | running, idle, fault; quality result as configured | cell-in | L: functional placeholder |
| B10 | Identification station / 身份识别工位 | Represents generic identity reading. | 1–2 | 0.1–0.5 × 0.1–0.8 × 0.1–0.5 | near entry | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B11 | Buffer lane modules / 缓存通道模块 | Holds cells for grouping. | 2–8 | 0.3–1.5 × 0.1–0.8 × 1–4 | central/side buffer zone | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B12 | Selector transfer carriage / 分组选取滑台 | Transfers selected cells between buffer and group lane. | 1–3 | 0.3–2 × 0.2–1.5 × 0.5–3 | over buffer | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B13 | Cell gripper / 电芯夹爪 | Represents generic picking of a cell. | 1–4 | 0.1–0.5 × 0.1–0.6 × 0.1–0.5 | on selector carriage | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B14 | Grouping fixture / 配对组合治具 | Holds a configurable output group. | 1–4 | 0.3–1.5 × 0.1–0.6 × 0.3–1.5 | exit bay | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B15 | Group outfeed / 组合下料通道 | Transfers completed groups downstream. | 1–2 | 0.3–1.5 × 0.1–0.6 × 1–4 | exit | revolute | running, idle, fault; quality result as configured | group-out | L: functional placeholder |

## Variant rules

- Select the module scope and optional rows before authoring the default master.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B09` Infeed lane: revolute; demonstration joint motion; not measured kinematics.
- `B12` Selector transfer carriage: prismatic; demonstration joint motion; not measured kinematics.
- `B13` Cell gripper: prismatic; demonstration joint motion; not measured kinematics.
- `B15` Group outfeed: revolute; demonstration joint motion; not measured kinematics.

## State slots

These are application visualization slots, not controller logic or a validated operating procedure. `NG-reject` changes routing only on variants with an explicitly authored reject route. Do not animate service leaves during a running cycle.

- `idle`: Ready/inactive illustration; no process motion.
- `running`: Generic process demonstration. No real cycle time or controller logic.
- `fault`: Illustrative fault indication; hold process joints.
- `NG-reject`: Optional failed-quality result; route only where the configured variant has a reject mechanism.
- `maintenance`: Demonstration access pose, disconnected from process motion.
- `loading`: Generic incoming material handoff.
- `unloading`: Generic outgoing material handoff.
- `buffering`: ASSUMED generic buffering visualization slot; no measured timing or recipe.
- `group-ready`: ASSUMED generic group-ready visualization slot; no measured timing or recipe.

## Sockets

Attachment nodes are authored from the generic envelope. No source positions, connector standards, pipe bores, voltage ratings or exact mating geometry are supplied. Default material flow is +Z with +Y up; +X is the service/operator side. Re-map any imported prototype axes explicitly.

| Socket | Type / direction | Generic location |
|---|---|---|
| `air-in` | utility / in | service face |
| `cell-in` | material / in | entry boundary |
| `data` | utility / service | service face |
| `group-out` | material / out | exit boundary |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |

## Modelling notes

Make buffer volume and cross-transfer motion visible. Mirrored layouts should be configuration options. Group size is a parameter and must not be claimed as detected capacity.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.
