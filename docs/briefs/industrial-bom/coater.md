<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Electrode coater / 极片涂布机

Apply a controlled slurry layer to current-collector foil before drying.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: unwind foil, guide and tension the web, meter slurry at a coating head, pass the coated web to a separate dryer, then inspect and rewind. The available head and tail references do not establish the dryer length, coating recipe, or single/double-sided arrangement.

**Master scope.** Head and tail modules; dryer is a separate linked master.

**Typical design envelope (m, width × height × flow length):** 3–7 × 2–5 × 6–18. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `coater-01`, `coater-02`. References are for visual context only; physical units remain unverified.

**Merged evidence.** Both references show elongated frames with repeated roller-like cross sections and distinct head/tail layouts. Coating die internals and web routing are not recovered. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 3–7 × 0.1–0.6 × 6–18 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 3–7 × 1–5 × 6–18 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Guard enclosure and panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 2–16 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 2–12 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Unwind stand / 放卷架 | Carries an incoming foil roll. | 1–2 | 1–3 × 1–3 × 1–3 | upstream end | revolute | running, idle, fault; quality result as configured | foil-in | L: functional placeholder |
| B10 | Coating head carriage / 涂布头滑台 | Positions a generic metering head relative to the web. | 1–2 | 0.5–2 × 0.3–1.5 × 0.5–2 | upstream process bay | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B11 | Slot-die or coating head / 涂布模头 | Represents the slurry application module; technology is optional. | 1–2 | 0.5–2.5 × 0.1–0.6 × 0.2–0.8 | above application roller | fixed | running, idle, fault; quality result as configured | slurry-in | L: functional placeholder |
| B12 | Guide and tension rollers / 导向张力辊 | Supports a continuous visible web route. | 4–16 | 0.5–2.5 × 0.1–0.5 × 0.1–0.5 | between reel and process bays | revolute | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B13 | Web guide actuator / 纠偏执行机构 | Provides a generic lateral alignment motion. | 1–2 | 0.3–1.5 × 0.1–0.5 × 0.3–1.5 | entry roller bay | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B14 | Rewind stand / 收卷架 | Collects dried electrode web. | 1–2 | 1–3 × 1–3 × 1–3 | downstream end | revolute | running, idle, fault; quality result as configured | electrode-out | L: functional placeholder |
| B15 | Slurry service skid / 浆料供给模块 | Shows generic pump/filter service connections. | 1–2 | 0.5–2 × 0.5–2 × 0.5–2 | side service bay | fixed | running, idle, fault; quality result as configured | slurry-in, drain-out | L: functional placeholder |
| B16 | Dryer connection collar / 烘箱连接口 | Defines the web handoff to a separate drying master. | 1–2 | 0.8–3 × 0.3–1.5 × 0.2–1 | module boundary | fixed | running, idle, fault; quality result as configured | web-to-dryer, web-from-dryer | L: functional placeholder |

## Variant rules

- Select head-only, tail-only or composed head/tail. Head-only enables unwind/coating/feed services; tail-only enables rewind and optional review modules. Dryer connections are ports to a separate master.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B09` Unwind stand: revolute; demonstration joint motion; not measured kinematics.
- `B10` Coating head carriage: prismatic; demonstration joint motion; not measured kinematics.
- `B12` Guide and tension rollers: revolute; demonstration joint motion; not measured kinematics.
- `B13` Web guide actuator: prismatic; demonstration joint motion; not measured kinematics.
- `B14` Rewind stand: revolute; demonstration joint motion; not measured kinematics.

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
- `coating`: ASSUMED generic coating visualization slot; no measured timing or recipe.

## Sockets

Attachment nodes are authored from the generic envelope. No source positions, connector standards, pipe bores, voltage ratings or exact mating geometry are supplied. Default material flow is +Z with +Y up; +X is the service/operator side. Re-map any imported prototype axes explicitly.

| Socket | Type / direction | Generic location |
|---|---|---|
| `air-in` | utility / in | service face |
| `data` | utility / service | service face |
| `drain-out` | fluid / out | service face |
| `electrode-out` | material / out | exit boundary |
| `foil-in` | material / in | entry boundary |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |
| `slurry-in` | fluid / in | service face |
| `web-from-dryer` | material / in | entry boundary |
| `web-to-dryer` | material / out | exit boundary |

## Modelling notes

Keep head and tail as selectable modules. Roller rhythm, reel silhouettes and web plane matter more than concealed pumps. Do not join them with a copied project-length tunnel.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.
