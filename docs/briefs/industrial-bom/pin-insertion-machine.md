<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Cell pin insertion machine / 电芯插钉机

Insert a temporary or process pin into a located cell opening.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: locate a cell, present a pin, align an insertion head, insert, check an illustrative result and release. Pin material, seal function and whether the operation is temporary are not verified.

**Master scope.** Guarded cell pin insertion station.

**Typical design envelope (m, width × height × flow length):** 1–3 × 1.5–4 × 1.5–5. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `pin-insertion-machine-01`. References are for visual context only; physical units remain unverified.

**Merged evidence.** The reference shows a compact enclosed station with a vertically organised process volume. The actual insertion tool and feeder mechanism are not isolated from the geometry. Duplicate or mirrored files do not establish installed quantity.

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
| B09 | Cell locating nest / 电芯定位治具 | Holds the cell beneath the tool. | 1–4 | 0.2–0.8 × 0.05–0.5 × 0.2–0.8 | central process deck | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B10 | Insertion head / 插钉头 | Represents the vertical insertion tool. | 1–4 | 0.1–0.6 × 0.2–1 × 0.1–0.6 | above cell nest | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B11 | Pin feed module / 供钉模块 | Selectable feeder placeholder. | 1–2 | 0.3–1.2 × 0.3–1.5 × 0.3–1.2 | side of tool bay | fixed | running, idle, fault; quality result as configured | pins-in | L: functional placeholder |
| B12 | Alignment guide / 插钉导向组件 | Illustrates final tool alignment. | 1–4 | 0.05–0.3 × 0.05–0.4 × 0.05–0.3 | tool tip | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B13 | Cell transfer shuttle / 电芯移载台 | Moves cells into and out of the fixture. | 1–2 | 0.3–1.5 × 0.1–0.6 × 0.5–2 | lower process plane | prismatic | running, idle, fault; quality result as configured | cell-in, cell-out | L: functional placeholder |
| B14 | Check sensor placeholder / 插钉检测占位件 | Represents a generic presence/check function. | 1–2 | 0.03–0.2 × 0.03–0.3 × 0.03–0.2 | near tool/cell | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |

## Variant rules

- Select the module scope and optional rows before authoring the default master.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B10` Insertion head: prismatic; demonstration joint motion; not measured kinematics.
- `B12` Alignment guide: prismatic; demonstration joint motion; not measured kinematics.
- `B13` Cell transfer shuttle: prismatic; demonstration joint motion; not measured kinematics.

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
| `operator` | operator / service | service face |
| `pins-in` | material / in | entry boundary |
| `power-in` | utility / in | service face |

## Modelling notes

Show the cell nest and short vertical tool motion in cutaway mode. Feeder type is optional; do not assert a specific pin or product.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.
