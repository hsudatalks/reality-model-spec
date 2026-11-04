<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Electrode slitter / 极片分切机

Convert wide coated electrode rolls to narrower webs.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: unwind electrode, align and tension it, cut longitudinally with a configurable knife station, extract edge trim and rewind the slit webs. No blade spacing, speed, tension or scrap routing is inferred from the reference.

**Master scope.** Standalone web slitting line.

**Typical design envelope (m, width × height × flow length):** 2–6 × 1.5–4 × 4–20. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `slitter-01`, `slitter-02`. References are for visual context only; physical units remain unverified.

**Merged evidence.** Two references show elongated process envelopes; the detailed reference has repeated circular/reel features while the second is an enclosed variant. Exact station equivalence is unverified. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 2–6 × 0.1–0.6 × 4–20 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 2–6 × 0.75–4 × 4–20 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Guard enclosure and panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 2–16 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 2–12 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Unwind reel stand / 放卷架 | Receives a wide electrode roll. | 1–2 | 1–3 × 1–3 × 1–3 | entry | revolute | running, idle, fault; quality result as configured | web-in | L: functional placeholder |
| B10 | Guide roller bank / 导辊组 | Carries the visible electrode web. | 4–16 | 0.5–2.5 × 0.1–0.5 × 0.1–0.5 | web path | revolute | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B11 | Web alignment carriage / 纠偏滑台 | Illustrates transverse web correction. | 1–2 | 0.5–2 × 0.2–0.8 × 0.5–2 | entry process bay | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B12 | Knife shaft cassette / 刀轴组件 | Represents adjustable longitudinal slitting. | 1–2 | 0.8–3 × 0.3–1.2 × 0.3–1.2 | central guarded bay | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B13 | Knife discs / 分切刀片 | Configurable blade set on a common shaft. | 2–24 | 0.01–0.05 × 0.1–0.4 × 0.1–0.4 | knife cassette | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B14 | Rewind spindle modules / 收卷轴模块 | Collects narrow slit rolls. | 1–4 | 1–3 × 1–3 × 1–3 | exit | revolute | running, idle, fault; quality result as configured | web-out | L: functional placeholder |
| B15 | Edge-trim collector / 边料收集组件 | Routes edge scrap to collection. | 1–2 | 0.3–1.5 × 0.3–2 × 0.3–1.5 | side of knife bay | fixed | running, idle, fault; quality result as configured | scrap-out, dust-out | L: functional placeholder |
| B16 | Web splice table / 接带台 | Provides a generic service surface for reel change. | 0–1 | 0.8–2.5 × 0.5–1.2 × 0.5–1.5 | entry service area | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |

## Variant rules

- Select the module scope and optional rows before authoring the default master.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B09` Unwind reel stand: revolute; demonstration joint motion; not measured kinematics.
- `B10` Guide roller bank: revolute; demonstration joint motion; not measured kinematics.
- `B11` Web alignment carriage: prismatic; demonstration joint motion; not measured kinematics.
- `B12` Knife shaft cassette: revolute; demonstration joint motion; not measured kinematics.
- `B13` Knife discs: revolute; demonstration joint motion; not measured kinematics.
- `B14` Rewind spindle modules: revolute; demonstration joint motion; not measured kinematics.

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
- `reel-change`: ASSUMED generic reel-change visualization slot; no measured timing or recipe.

## Sockets

Attachment nodes are authored from the generic envelope. No source positions, connector standards, pipe bores, voltage ratings or exact mating geometry are supplied. Default material flow is +Z with +Y up; +X is the service/operator side. Re-map any imported prototype axes explicitly.

| Socket | Type / direction | Generic location |
|---|---|---|
| `air-in` | utility / in | service face |
| `data` | utility / service | service face |
| `dust-out` | gas/duct / out | upper/service collar |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |
| `scrap-out` | material / out | exit boundary |
| `web-in` | material / in | entry boundary |
| `web-out` | material / out | exit boundary |

## Modelling notes

Make reel hubs, knife bay, guide rollers and web plane readable at medium distance. Hide individual thin blades at distant LOD; do not invent a fixed production strip count.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.

