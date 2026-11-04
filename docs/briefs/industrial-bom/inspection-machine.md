<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Cell inspection machine / 电芯检测机

Inspect a cell and route it according to a test result.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: receive and fixture a cell, execute one selected test technology, record an illustrative pass/fail result, then release to the main outlet or optional reject route. Optical appearance, radiographic, leak-test and electrical-test modules are mutually selectable variants rather than a single combined process.

**Master scope.** Compact inspection station; optional composed test-line envelope 5-15 m long and 2-8 m wide.

**Typical design envelope (m, width × height × flow length):** 1–4 × 1.2–4 × 1.5–5. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `inspection-machine-01`, `inspection-machine-02`, `inspection-machine-03`, `inspection-machine-04`, `inspection-machine-05`, `inspection-machine-06`. References are for visual context only; physical units remain unverified.

**Merged evidence.** The released references cover optical, radiographic, leak-test and electrical-test variants. The prior optical decomposition supports frames, access leaves, insert panels and pass-through openings in one reference; hidden sensors and transfer functions remain inferred. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 1–4 × 0.1–0.6 × 1.5–5 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 1–4 × 0.6–4 × 1.5–5 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Guard enclosure and panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 2–16 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 2–12 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Material pass-through frames / 物料通道框 | Defines entry and exit openings. | 2–2 | 0.2–1.2 × 0.2–1.2 × 0.02–0.2 | opposite lower sides | fixed | running, idle, fault; quality result as configured | cell-in, cell-out | M: external form; function assumed |
| B10 | Transfer conveyor or shuttle / 检测移载机构 | Moves cells between fixture and outlets. | 1–2 | 0.3–1.5 × 0.1–0.6 × 0.5–3 | lower process plane | prismatic | running, idle, fault; quality result as configured | cell-in, cell-out | L: functional placeholder |
| B11 | Cell locating nest / 电芯定位治具 | Holds the cell during a selected test. | 1–4 | 0.15–0.8 × 0.05–0.4 × 0.15–0.8 | test station | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B12 | Optical camera/light module / 外观相机光源模块 | Optional appearance-inspection technology. | 0–6 | 0.1–0.5 × 0.1–0.6 × 0.1–0.5 | around cell nest | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B13 | Radiographic test module / 射线检测模块 | Optional shielded test placeholder; no radiation-system design inferred. | 0–1 | 0.5–3 × 0.5–3 × 0.5–3 | shielded process bay | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B14 | Leak-test chamber/manifold / 检漏腔及歧管 | Optional generic sealed-test module. | 0–2 | 0.3–1.5 × 0.3–1.5 × 0.3–1.5 | test bay | prismatic | running, idle, fault; quality result as configured | test-gas-in, vacuum-out | L: functional placeholder |
| B15 | Electrical probe head / 电测探针头 | Optional contact-based measurement module. | 0–4 | 0.1–0.8 × 0.1–0.8 × 0.1–0.8 | above cell terminals | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B16 | Reject diverter / 不良分流机构 | Optional illustrative fail-route actuator. | 0–1 | 0.1–0.6 × 0.05–0.3 × 0.2–0.8 | after test station | revolute | running, idle, fault; quality result as configured | reject-out | L: functional placeholder |
| B17 | Reject chute and bin / 不良收集槽箱 | Collects visually rejected cells in a demo. | 0–1 | 0.3–1.2 × 0.3–1.2 × 0.3–1.2 | side outlet | fixed | running, idle, fault; quality result as configured | reject-out | L: functional placeholder |
| B18 | Internal support decks / 内部支承台架 | Supports selectable test modules. | 1–4 | 0.3–2 × 0.1–0.6 × 0.3–2 | within enclosure | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B19 | Roof ventilation module / 顶部通风模块 | Represents generic enclosure ventilation. | 0–2 | 0.15–0.6 × 0.1–0.4 × 0.15–0.6 | roof | fixed | running, idle, fault; quality result as configured | exhaust-out | M: external form; function assumed |

## Variant rules

- Select exactly one test technology: optical, radiographic, leak or electrical. Enable its matching module bank; hide the other technology rows. Select a single compact station or composed line scope.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B10` Transfer conveyor or shuttle: prismatic; demonstration joint motion; not measured kinematics.
- `B11` Cell locating nest: prismatic; demonstration joint motion; not measured kinematics.
- `B14` Leak-test chamber/manifold: prismatic; demonstration joint motion; not measured kinematics.
- `B15` Electrical probe head: prismatic; demonstration joint motion; not measured kinematics.
- `B16` Reject diverter: revolute; demonstration joint motion; not measured kinematics.

## State slots

These are application visualization slots, not controller logic or a validated operating procedure. `NG-reject` changes routing only on variants with an explicitly authored reject route. Do not animate service leaves during a running cycle.

- `idle`: Ready/inactive illustration; no process motion.
- `running`: Generic process demonstration. No real cycle time or controller logic.
- `fault`: Illustrative fault indication; hold process joints.
- `NG-reject`: Optional failed-quality result; route only where the configured variant has a reject mechanism.
- `maintenance`: Demonstration access pose, disconnected from process motion.
- `loading`: Generic incoming material handoff.
- `unloading`: Generic outgoing material handoff.
- `testing`: ASSUMED generic testing visualization slot; no measured timing or recipe.
- `pass`: ASSUMED generic pass visualization slot; no measured timing or recipe.
- `fail`: ASSUMED generic fail visualization slot; no measured timing or recipe.

## Sockets

Attachment nodes are authored from the generic envelope. No source positions, connector standards, pipe bores, voltage ratings or exact mating geometry are supplied. Default material flow is +Z with +Y up; +X is the service/operator side. Re-map any imported prototype axes explicitly.

| Socket | Type / direction | Generic location |
|---|---|---|
| `air-in` | utility / in | service face |
| `cell-in` | material / in | entry boundary |
| `cell-out` | material / out | exit boundary |
| `data` | utility / service | service face |
| `exhaust-out` | gas/duct / out | upper/service collar |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |
| `reject-out` | material / out | configurable side branch |
| `test-gas-in` | gas/duct / in | upper/service collar |
| `vacuum-out` | gas/duct / out | upper/service collar |

## Modelling notes

Use the common shell and interchangeable test modules. The optical decomposition is evidence for one variant only. Camera counts, reject routes, contact motion and all test internals are assumptions. Keep original component evidence ids local.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.
