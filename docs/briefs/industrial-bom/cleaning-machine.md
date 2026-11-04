<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Cell cleaning machine / 电芯清洁机

Clean a cell surface before or after another process step.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: fixture a cell, present a wipe/brush tool, clean selected surfaces, collect used media or extracted dust, and release. Cleaning medium, chemistry and contact force are unspecified.

**Master scope.** Enclosed cell wiping/cleaning station.

**Typical design envelope (m, width × height × flow length):** 1–3 × 1.5–4 × 1.5–5. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `cleaning-machine-01`. References are for visual context only; physical units remain unverified.

**Merged evidence.** The reference supports a compact vertical enclosure and lower material passage. Cleaning tool type and surface sequence remain assumptions. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 1–3 × 0.1–0.6 × 1.5–5 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 1–3 × 0.75–4 × 1.5–5 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Guard enclosure and panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 2–16 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 2–12 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Cell locating nest / 电芯定位治具 | Holds the cell in a repeatable pose. | 1–4 | 0.2–0.8 × 0.05–0.5 × 0.2–0.8 | process deck | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B10 | Cleaning tool carriage / 清洁头滑台 | Moves a selected cleaning tool across the work. | 1–4 | 0.2–1 × 0.2–1 × 0.3–1.5 | above/beside cell | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B11 | Wipe or brush head / 擦拭或刷头 | Selectable generic surface-cleaning tool. | 1–4 | 0.1–0.6 × 0.1–0.5 × 0.1–0.6 | on cleaning carriage | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B12 | Media supply/take-up / 清洁耗材收放组件 | Optional wipe-media feed. | 0–2 | 0.2–0.8 × 0.2–1 × 0.2–0.8 | tool service side | revolute | running, idle, fault; quality result as configured | media-in, waste-out | L: functional placeholder |
| B13 | Extraction collar / 抽尘接口 | Optional generic particle extraction. | 0–2 | 0.1–0.5 × 0.1–0.5 × 0.1–0.5 | near cleaning tool | fixed | running, idle, fault; quality result as configured | dust-out | L: functional placeholder |
| B14 | Cell transfer shuttle / 电芯移载台 | Moves cells through the process. | 1–2 | 0.3–1.5 × 0.1–0.6 × 0.5–2 | lower deck | prismatic | running, idle, fault; quality result as configured | cell-in, cell-out | L: functional placeholder |

## Variant rules

- Select the module scope and optional rows before authoring the default master.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B10` Cleaning tool carriage: prismatic; demonstration joint motion; not measured kinematics.
- `B11` Wipe or brush head: revolute; demonstration joint motion; not measured kinematics.
- `B12` Media supply/take-up: revolute; demonstration joint motion; not measured kinematics.
- `B14` Cell transfer shuttle: prismatic; demonstration joint motion; not measured kinematics.

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
| `cell-in` | material / in | entry boundary |
| `cell-out` | material / out | exit boundary |
| `data` | utility / service | service face |
| `dust-out` | gas/duct / out | upper/service collar |
| `media-in` | material / in | entry boundary |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |
| `waste-out` | material / out | exit boundary |

## Modelling notes

Represent one selectable cleaning technology at a time. Use subtle wipe motion and a clear process deck; avoid invented spray chemistry or residue effects.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.

