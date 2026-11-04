<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Process solvent recovery system / 工艺溶剂回收系统

Collect and recover solvent from a process exhaust stream.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: accept solvent-bearing exhaust, pass it through a selectable recovery stage, collect recovered liquid and hand treated air onward. Condensation, adsorption and distillation are alternative architectures; the source does not establish which one applies.

**Master scope.** Modular recovery skid or equipment group; external duct layout authored separately.

**Typical design envelope (m, width × height × flow length):** 3–12 × 2–10 × 4–20. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `solvent-recovery-system-01`. References are for visual context only; physical units remain unverified.

**Merged evidence.** The reference shows a distributed group of service volumes with prominent round duct/pipe-like connections. The process equipment identities and recovery chemistry remain unverified. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 3–12 × 0.1–0.6 × 4–20 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 3–12 × 1–10 × 4–20 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Local guards and service panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 0–12 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 0–8 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Recovery process housing / 回收工艺箱体 | Generic selectable recovery module. | 1–3 | 1–5 × 1–5 × 1–6 | main skid | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B10 | Heat-exchange or adsorber placeholder / 换热或吸附模块占位件 | Select one generic recovery architecture. | 1–3 | 0.8–4 × 1–5 × 0.8–4 | process group | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B11 | Exhaust duct collars / 废气风管接口 | Defines process inlet/outlet handoffs. | 2–6 | 0.3–2 × 0.3–2 × 0.3–2 | group boundaries | fixed | running, idle, fault; quality result as configured | process-exhaust-in, treated-air-out | M: external form; function assumed |
| B12 | Circulation/extraction fan / 循环抽风机 | Represents a generic gas-moving stage. | 1–2 | 0.5–2.5 × 0.5–2.5 × 0.5–2.5 | gas service side | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B13 | Recovered-liquid receiver / 回收液接收罐 | Represents generic liquid collection. | 1–2 | 0.5–2.5 × 1–3 × 0.5–2.5 | lower process side | fixed | running, idle, fault; quality result as configured | recovered-liquid-out | L: functional placeholder |
| B14 | Service pump manifold / 服务泵歧管 | Defines generic utility and drain interfaces. | 1–2 | 0.3–2 × 0.3–2 × 0.3–2 | base service side | fixed | running, idle, fault; quality result as configured | cooling-in, cooling-out, drain-out | L: functional placeholder |
| B15 | Access platform / 检修平台 | Optional maintenance access for tall modules. | 0–2 | 1–5 × 1–8 × 1–5 | upper process side | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |

## Variant rules

- Select a generic recovery architecture before modelling process internals. Do not combine all alternative recovery technologies by default.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B12` Circulation/extraction fan: revolute; demonstration joint motion; not measured kinematics.

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
| `cooling-in` | utility / in | service face |
| `cooling-out` | utility / out | service face |
| `data` | utility / service | service face |
| `drain-out` | fluid / out | service face |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |
| `process-exhaust-in` | gas/duct / in | upper/service collar |
| `recovered-liquid-out` | fluid / out | service face |
| `treated-air-out` | gas/duct / out | upper/service collar |

## Modelling notes

Use a generic process group with clear duct interfaces. Do not assert a chemical species, operating temperature, recovery technology or treatment efficiency.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.

