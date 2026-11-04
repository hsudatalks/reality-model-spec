<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Electrode calender and slitter / 极片辊压分切机

Densify coated electrode and divide it into controlled-width webs.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: unwind, guide and tension the electrode, pass it through a pressure-roll nip, optionally trim/slit, remove edge scrap and rewind. Combined-line and separate-stage variants share interfaces but need different optional modules.

**Master scope.** Roll-processing line; pressure and slitting modules independently selectable.

**Typical design envelope (m, width × height × flow length):** 2–6 × 2–5 × 6–25. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `calender-slitter-01`, `calender-slitter-02`, `calender-slitter-03`. References are for visual context only; physical units remain unverified.

**Merged evidence.** Three references support repeated reel/roller stations and long framed process bays. One open-layout variant differs from the enclosed variants; blade count, pressure mechanism and strip count are not established. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 2–6 × 0.1–0.6 × 6–25 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 2–6 × 1–5 × 6–25 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Guard enclosure and panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 2–16 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 2–12 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Unwind turret / 放卷转塔 | Supports incoming electrode roll. | 1–2 | 1–3 × 1–3 × 1–3 | entry | revolute | running, idle, fault; quality result as configured | electrode-in | L: functional placeholder |
| B10 | Pressure-roll stand / 辊压机架 | Carries the opposed calender rolls. | 1–2 | 1–3 × 1–4 × 1–3 | central process bay | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B11 | Calender roll pair / 辊压辊组 | Shows the principal compression nip. | 2–4 | 0.5–2.5 × 0.3–1 × 0.3–1 | inside pressure stand | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B12 | Nip-gap adjustment / 辊缝调节机构 | Provides illustrative pressure-gap motion. | 1–2 | 0.3–1.5 × 0.3–2 × 0.3–1.5 | above/beside roll stand | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B13 | Slitting cassette / 分切刀盒 | Optional combined-line cutting station. | 0–2 | 0.8–3 × 0.3–1.5 × 0.3–1.5 | after pressure stand | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B14 | Tension and guide rollers / 张力导向辊 | Links the web path between major modules. | 4–20 | 0.5–2.5 × 0.1–0.6 × 0.1–0.6 | web path | revolute | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B15 | Rewind spindle bank / 收卷轴组 | Collects slit or calendered webs. | 1–4 | 1–3 × 1–3 × 1–3 | exit | revolute | running, idle, fault; quality result as configured | electrode-out | L: functional placeholder |
| B16 | Edge trim extraction / 边料抽吸口 | Connects optional slitting scrap extraction. | 0–2 | 0.2–0.8 × 0.2–1 × 0.2–0.8 | slitting bay | fixed | running, idle, fault; quality result as configured | scrap-out, dust-out | L: functional placeholder |

## Variant rules

- Select the module scope and optional rows before authoring the default master.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B09` Unwind turret: revolute; demonstration joint motion; not measured kinematics.
- `B11` Calender roll pair: revolute; demonstration joint motion; not measured kinematics.
- `B12` Nip-gap adjustment: prismatic; demonstration joint motion; not measured kinematics.
- `B13` Slitting cassette: revolute; demonstration joint motion; not measured kinematics.
- `B14` Tension and guide rollers: revolute; demonstration joint motion; not measured kinematics.
- `B15` Rewind spindle bank: revolute; demonstration joint motion; not measured kinematics.

## State slots

These are application visualization slots, not controller logic or a validated operating procedure. `NG-reject` changes routing only on variants with an explicitly authored reject route. Do not animate service leaves during a running cycle.

- `idle`: Ready/inactive illustration; no process motion.
- `running`: Generic process demonstration. No real cycle time or controller logic.
- `fault`: Illustrative fault indication; hold process joints.
- `NG-reject`: Optional failed-quality result; route only where the configured variant has a reject mechanism.
- `maintenance`: Demonstration access pose, disconnected from process motion.
- `loading`: Generic incoming material handoff.
- `unloading`: Generic outgoing material handoff.
- `threading`: ASSUMED generic threading visualization slot; no measured timing or recipe.
- `nip-open`: ASSUMED generic nip-open visualization slot; no measured timing or recipe.

## Sockets

Attachment nodes are authored from the generic envelope. No source positions, connector standards, pipe bores, voltage ratings or exact mating geometry are supplied. Default material flow is +Z with +Y up; +X is the service/operator side. Re-map any imported prototype axes explicitly.

| Socket | Type / direction | Generic location |
|---|---|---|
| `air-in` | utility / in | service face |
| `data` | utility / service | service face |
| `dust-out` | gas/duct / out | upper/service collar |
| `electrode-in` | material / in | entry boundary |
| `electrode-out` | material / out | exit boundary |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |
| `scrap-out` | material / out | exit boundary |

## Modelling notes

Preserve the dominant paired roll stand and reel arrangement. Blade count is a parameter, not a detected manufacturing quantity. Keep pressure and cutting modules optional.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.

