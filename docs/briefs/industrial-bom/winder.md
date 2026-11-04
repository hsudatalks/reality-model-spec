<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Cell winder / 电芯卷绕机

Wind electrode and separator webs into a cell core.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: feed electrode and separator rolls, control alignment/tension, wind onto a mandrel, cut and secure the tail, then unload the core. The supplied references are sparse line/enclosure evidence; internal mandrel count and indexing architecture are design assumptions.

**Master scope.** Cell winding machine or short multi-station line.

**Typical design envelope (m, width × height × flow length):** 2–6 × 2–5 × 4–18. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `winder-01`, `winder-02`. References are for visual context only; physical units remain unverified.

**Merged evidence.** Two references have near-identical long envelopes and sparse visible internal detail. Their agreement supports a shared outer master, not an observed count of winding heads. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 2–6 × 0.1–0.6 × 4–18 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 2–6 × 1–5 × 4–18 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Guard enclosure and panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 2–16 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 2–12 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Electrode reel stands / 极片放卷架 | Feeds the electrode webs. | 2–4 | 0.5–2 × 0.8–2.5 × 0.5–2 | upstream side | revolute | running, idle, fault; quality result as configured | electrode-in | L: functional placeholder |
| B10 | Separator reel stands / 隔膜放卷架 | Feeds one or more separator webs. | 1–4 | 0.5–2 × 0.8–2.5 × 0.5–2 | adjacent upstream side | revolute | running, idle, fault; quality result as configured | separator-in | L: functional placeholder |
| B11 | Tension and alignment rollers / 张力纠偏辊 | Guides separate webs toward winding. | 4–20 | 0.2–1 × 0.1–0.4 × 0.1–0.4 | feed path | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B12 | Winding spindle or mandrel / 卷绕轴或卷针 | Principal core-winding axis. | 1–4 | 0.1–0.6 × 0.1–0.6 × 0.2–1 | central process bay | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B13 | Web clamps and cutters / 夹带切刀 | Clamps and separates the webs. | 2–6 | 0.1–0.8 × 0.1–0.5 × 0.1–0.8 | near winding head | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B14 | Tail-securing module / 收尾固定模块 | Optional generic tape or securing head. | 0–2 | 0.2–1 × 0.2–1 × 0.2–1 | after winding head | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B15 | Core unload slide / 卷芯下料滑台 | Transfers the wound core to the outlet. | 1–2 | 0.3–1.5 × 0.2–1 × 0.5–2 | downstream bay | prismatic | running, idle, fault; quality result as configured | core-out | L: functional placeholder |
| B16 | Optional indexing turret / 可选分度转盘 | Illustrates a selectable multi-head configuration. | 0–1 | 0.5–2 × 0.2–1.5 × 0.5–2 | central process bay | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |

## Variant rules

- Select the module scope and optional rows before authoring the default master.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B09` Electrode reel stands: revolute; demonstration joint motion; not measured kinematics.
- `B10` Separator reel stands: revolute; demonstration joint motion; not measured kinematics.
- `B11` Tension and alignment rollers: revolute; demonstration joint motion; not measured kinematics.
- `B12` Winding spindle or mandrel: revolute; demonstration joint motion; not measured kinematics.
- `B13` Web clamps and cutters: prismatic; demonstration joint motion; not measured kinematics.
- `B14` Tail-securing module: prismatic; demonstration joint motion; not measured kinematics.
- `B15` Core unload slide: prismatic; demonstration joint motion; not measured kinematics.
- `B16` Optional indexing turret: revolute; demonstration joint motion; not measured kinematics.

## State slots

These are application visualization slots, not controller logic or a validated operating procedure. `NG-reject` changes routing only on variants with an explicitly authored reject route. Do not animate service leaves during a running cycle.

- `idle`: Ready/inactive illustration; no process motion.
- `running`: Generic process demonstration. No real cycle time or controller logic.
- `fault`: Illustrative fault indication; hold process joints.
- `NG-reject`: Optional failed-quality result; route only where the configured variant has a reject mechanism.
- `maintenance`: Demonstration access pose, disconnected from process motion.
- `loading`: Generic incoming material handoff.
- `unloading`: Generic outgoing material handoff.
- `winding`: ASSUMED generic winding visualization slot; no measured timing or recipe.
- `core-unload`: ASSUMED generic core-unload visualization slot; no measured timing or recipe.

## Sockets

Attachment nodes are authored from the generic envelope. No source positions, connector standards, pipe bores, voltage ratings or exact mating geometry are supplied. Default material flow is +Z with +Y up; +X is the service/operator side. Re-map any imported prototype axes explicitly.

| Socket | Type / direction | Generic location |
|---|---|---|
| `air-in` | utility / in | service face |
| `core-out` | material / out | exit boundary |
| `data` | utility / service | service face |
| `electrode-in` | material / in | entry boundary |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |
| `separator-in` | material / in | entry boundary |

## Modelling notes

Use a restrained enclosure as the default. Add internal winding motion only as a clearly assumed demonstration. A duplicate export must not double installed quantities.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.

