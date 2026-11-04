<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Vertical carrier lift / 载具提升机

Move cell trays or carriers between material-handling elevations.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: receive a carrier at a landing, locate it on a lift deck, move vertically to another landing and transfer it onward. Drive type, travel, landing count and interlock logic are configurable assumptions.

**Master scope.** One lift tower with configurable travel and landings.

**Typical design envelope (m, width × height × flow length):** 1–4 × 2.5–8 × 1–5. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `vertical-lift-01`, `vertical-lift-02`, `vertical-lift-03`, `vertical-lift-04`. References are for visual context only; physical units remain unverified.

**Merged evidence.** Four assembled references support paired vertical structures and transport decks, with two repeated envelope families. Internal drive mechanisms and installed landing counts are not verified. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 1–4 × 0.1–0.6 × 1–5 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 1–4 × 1.25–8 × 1–5 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Local guards and service panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 0–12 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 0–8 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Lift mast frame / 提升立柱机架 | Defines the main tower structure. | 2–4 | 0.1–0.5 × 2.5–8 × 0.1–0.5 | tower sides | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B10 | Guide rails / 升降导轨 | Guides the vertical carriage. | 2–4 | 0.03–0.15 × 2–7 × 0.03–0.15 | inside mast | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B11 | Lift carriage / 升降滑架 | Carries the transport deck. | 1–1 | 0.5–2.5 × 0.2–1.5 × 0.5–3 | between mast rails | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B12 | Carrier transport deck / 载具输送台 | Receives and discharges carriers. | 1–1 | 0.5–2.5 × 0.1–0.8 × 0.8–3 | on carriage | revolute | running, idle, fault; quality result as configured | lower-in, upper-out | M: external form; function assumed |
| B13 | Drive head placeholder / 提升驱动占位件 | Selectable belt/chain/screw drive housing. | 1–2 | 0.2–1.2 × 0.2–1.2 × 0.2–1.2 | tower top or side | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B14 | Landing transfer collar / 层间接驳口 | Defines configurable handoff at each landing. | 2–4 | 0.5–2.5 × 0.2–1.5 × 0.2–1 | landing faces | fixed | running, idle, fault; quality result as configured | lower-in, upper-out | L: functional placeholder |
| B15 | Carrier stop and locator / 载具挡停定位器 | Locates the carrier before lift movement. | 1–2 | 0.05–0.4 × 0.05–0.5 × 0.05–0.4 | on transport deck | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |

## Variant rules

- Select the module scope and optional rows before authoring the default master.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B11` Lift carriage: prismatic; demonstration joint motion; not measured kinematics.
- `B12` Carrier transport deck: revolute; demonstration joint motion; not measured kinematics.
- `B13` Drive head placeholder: revolute; demonstration joint motion; not measured kinematics.
- `B15` Carrier stop and locator: prismatic; demonstration joint motion; not measured kinematics.

## State slots

These are application visualization slots, not controller logic or a validated operating procedure. `NG-reject` changes routing only on variants with an explicitly authored reject route. Do not animate service leaves during a running cycle.

- `idle`: Ready/inactive illustration; no process motion.
- `running`: Generic process demonstration. No real cycle time or controller logic.
- `fault`: Illustrative fault indication; hold process joints.
- `NG-reject`: Optional failed-quality result; route only where the configured variant has a reject mechanism.
- `maintenance`: Demonstration access pose, disconnected from process motion.
- `loading`: Generic incoming material handoff.
- `unloading`: Generic outgoing material handoff.
- `at-lower`: ASSUMED generic at-lower visualization slot; no measured timing or recipe.
- `lifting`: ASSUMED generic lifting visualization slot; no measured timing or recipe.
- `at-upper`: ASSUMED generic at-upper visualization slot; no measured timing or recipe.

## Sockets

Attachment nodes are authored from the generic envelope. No source positions, connector standards, pipe bores, voltage ratings or exact mating geometry are supplied. Default material flow is +Z with +Y up; +X is the service/operator side. Re-map any imported prototype axes explicitly.

| Socket | Type / direction | Generic location |
|---|---|---|
| `air-in` | utility / in | service face |
| `data` | utility / service | service face |
| `lower-in` | material / in | lower landing |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |
| `upper-out` | material / out | upper landing |

## Modelling notes

Lift tower, guide rails and independently moving deck are the identity. Use a generic travel range; do not infer exact building levels from the export.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.
