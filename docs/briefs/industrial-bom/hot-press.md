<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Cell hot press / 电芯热压机

Apply heat and compression to a cell core or stack.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: load a core into a nest, close a guarded press, bring heated platens together, dwell, release and unload. The line references do not establish press force, dwell, temperature or number of independent press stations.

**Master scope.** Single press module; compose a line from 2-8 modules rather than stretching one press. Generic composed-line length range: 8-35 m.

**Typical design envelope (m, width × height × flow length):** 1.5–5 × 2–5 × 2–6. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `hot-press-01`, `hot-press-02`. References are for visual context only; physical units remain unverified.

**Merged evidence.** The two references share a long rectangular envelope and sparse process details. Use the line shell as context only; platen and actuator identification remain assumed. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 1.5–5 × 0.1–0.6 × 2–6 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 1.5–5 × 1–5 × 2–6 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Guard enclosure and panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 2–16 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 2–12 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Press reaction frame / 压力机架 | Carries compressive loads in the generic design. | 1–1 | 1–4 × 1.5–4 × 1–4 | central press bay | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B10 | Fixed heated platen / 固定热压板 | Provides a stationary process face. | 1–2 | 0.3–1.5 × 0.05–0.3 × 0.3–1.5 | press bed | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B11 | Moving heated platen / 活动热压板 | Provides illustrative closing motion. | 1–2 | 0.3–1.5 × 0.05–0.3 × 0.3–1.5 | above process nest | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B12 | Press drive actuator / 热压驱动机构 | Moves the upper platen; drive type selectable. | 1–2 | 0.2–1 × 0.5–2 × 0.2–1 | above press frame | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B13 | Cell locating nest / 电芯定位治具 | Positions a core during pressing. | 1–4 | 0.2–1 × 0.05–0.3 × 0.2–1 | between platens | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B14 | Load and unload shuttle / 上下料移载台 | Moves a nest into and out of the guarded bay. | 1–2 | 0.5–2 × 0.1–0.8 × 0.5–2 | entry/exit of press bay | prismatic | running, idle, fault; quality result as configured | cell-in, cell-out | L: functional placeholder |
| B15 | Thermal service unit / 温控服务模块 | Represents generic heater/cooling connections. | 1–1 | 0.4–1.5 × 0.5–2 × 0.4–1.5 | rear service side | fixed | running, idle, fault; quality result as configured | thermal-service | L: functional placeholder |

## Variant rules

- Select the module scope and optional rows before authoring the default master.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B11` Moving heated platen: prismatic; demonstration joint motion; not measured kinematics.
- `B12` Press drive actuator: prismatic; demonstration joint motion; not measured kinematics.
- `B14` Load and unload shuttle: prismatic; demonstration joint motion; not measured kinematics.

## State slots

These are application visualization slots, not controller logic or a validated operating procedure. `NG-reject` changes routing only on variants with an explicitly authored reject route. Do not animate service leaves during a running cycle.

- `idle`: Ready/inactive illustration; no process motion.
- `running`: Generic process demonstration. No real cycle time or controller logic.
- `fault`: Illustrative fault indication; hold process joints.
- `NG-reject`: Optional failed-quality result; route only where the configured variant has a reject mechanism.
- `maintenance`: Demonstration access pose, disconnected from process motion.
- `loading`: Generic incoming material handoff.
- `unloading`: Generic outgoing material handoff.
- `pressing`: ASSUMED generic pressing visualization slot; no measured timing or recipe.
- `heating`: ASSUMED generic heating visualization slot; no measured timing or recipe.
- `cooling`: ASSUMED generic cooling visualization slot; no measured timing or recipe.

## Sockets

Attachment nodes are authored from the generic envelope. No source positions, connector standards, pipe bores, voltage ratings or exact mating geometry are supplied. Default material flow is +Z with +Y up; +X is the service/operator side. Re-map any imported prototype axes explicitly.

| Socket | Type / direction | Generic location |
|---|---|---|
| `air-in` | utility / in | service face |
| `cell-in` | material / in | entry boundary |
| `cell-out` | material / out | exit boundary |
| `data` | utility / service | service face |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |
| `thermal-service` | utility / service | service face |

## Modelling notes

The C-frame or four-post frame and opposed platens carry the identity. Choose one configurable frame style; keep the protective shell separate. Do not copy the reference line station spacing.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.

