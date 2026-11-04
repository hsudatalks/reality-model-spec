<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Actual consumer owners must confirm the existing contract path and commit; historical message aliases do not establish an owner. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Cell or tray conveyor / 电芯托盘输送机

Transfer cells or carriers between process stations.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: accept a carrier, transport it along a belt/roller path, stop or locate it, and hand it to the next station. A lift-and-transfer variant may raise a short deck and transfer sideways; direction and sensor logic are configurable.

**Master scope.** Straight module or optional short lift-and-transfer module.

**Typical design envelope (m, width × height × flow length):** 0.5–2.5 × 0.5–2 × 1–12. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `conveyor-01`, `conveyor-02`. References are for visual context only; physical units remain unverified.

**Merged evidence.** Two references support distinct forms: a long open transport frame and a compact raised transfer deck. These are variants, not two mandatory sections of one conveyor. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 0.5–2.5 × 0.1–0.6 × 1–12 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 0.5–2.5 × 0.25–2 × 1–12 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Local guards and service panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 0–12 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 0–8 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Transport rails / 输送导轨 | Defines the carrier route. | 2–4 | 0.03–0.2 × 0.05–0.3 × 1–12 | top deck | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B10 | Belt or roller bed / 皮带或滚筒床 | Provides the moving transport surface. | 1–2 | 0.3–2 × 0.05–0.4 × 0.8–12 | between rails | revolute | running, idle, fault; quality result as configured | carrier-in, carrier-out | M: external form; function assumed |
| B11 | Drive and idler modules / 驱动从动组件 | Represents end drives or roller drive units. | 2–4 | 0.1–0.5 × 0.1–0.5 × 0.1–0.5 | deck ends | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B12 | Carrier stop / 载具挡停器 | Provides illustrative stopping and release. | 1–3 | 0.05–0.3 × 0.05–0.4 × 0.05–0.3 | transfer positions | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B13 | Lift deck / 顶升台 | Optional lift-and-transfer variant. | 0–1 | 0.5–2 × 0.1–0.6 × 0.5–2 | central short module | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B14 | Side-transfer belt / 横移皮带 | Optional transverse carrier handoff. | 0–2 | 0.3–1.5 × 0.05–0.3 × 0.5–2 | above lift deck | revolute | running, idle, fault; quality result as configured | side-out | L: functional placeholder |

## Variant rules

- Select straight transport or lift-and-transfer deck. Side transfer sockets exist only on the corresponding variant.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B10` Belt or roller bed: revolute; demonstration joint motion; not measured kinematics.
- `B11` Drive and idler modules: revolute; demonstration joint motion; not measured kinematics.
- `B12` Carrier stop: prismatic; demonstration joint motion; not measured kinematics.
- `B13` Lift deck: prismatic; demonstration joint motion; not measured kinematics.
- `B14` Side-transfer belt: revolute; demonstration joint motion; not measured kinematics.

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
| `carrier-in` | material / in | entry boundary |
| `carrier-out` | material / out | exit boundary |
| `data` | utility / service | service face |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |
| `side-out` | material / out | configurable side branch |

## Modelling notes

Keep transport height, direction arrows and end sockets readable. Use a material offset for belt motion; do not translate the entire conveyor indefinitely.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.

## Supplementary visual classification (ASSUMED)

`unknown-02` → conveyor, visual classification confidence **0.9**. This supports a provisional functional label, not certified geometry, motion or flow behavior.

Source: delivery's neutral-grey, edge and scale-bar visual inspection, provisionally accepted by the coordinator; no independent re-review here. The initial unknown classification at 0.25 is retained as history. Units and dimension confidence remain **unverified**, separately from the visual confidence above. This text does not alter safe IDs, source GLB SHA, filenames, original index, geometry, Library tags or rights. See the [release directory note](../../reference-exports/industrial-20261104.md).
