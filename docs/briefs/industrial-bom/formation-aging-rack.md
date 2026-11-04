<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Formation and aging rack / 化成老化货架

Hold cell trays during electrical formation, testing or controlled dwell.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: load a tray into a bay, engage contacts for formation or capacity testing when required, hold or cycle cells, release contacts and unload. Passive aging and active electrical bays must be separate configuration modes; actual recipe and current channels are unverified.

**Master scope.** One repeatable rack bay. Compose 2-12 bays; generic assembled-row length 4-20 m.

**Typical design envelope (m, width × height × flow length):** 1–4 × 2–5 × 1–3. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `formation-aging-rack-01`, `formation-aging-rack-02`, `formation-aging-rack-03`. References are for visual context only; physical units remain unverified.

**Merged evidence.** Three references support repeated rectangular bay divisions and distinct service volumes. Some exports represent a whole process block. Visible bay rhythm does not establish cell channel counts or installed racks. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 1–4 × 0.1–0.6 × 1–3 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 1–4 × 1–5 × 1–3 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Local guards and service panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 0–12 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 0–8 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Rack bay uprights / 货架立柱 | Defines a repeatable storage/process bay. | 4–8 | 0.05–0.2 × 2–5 × 0.05–0.2 | bay corners | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B10 | Tray support rails / 托盘支承导轨 | Supports removable trays at selectable levels. | 4–24 | 0.05–0.2 × 0.03–0.15 × 0.8–2.5 | bay levels | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B11 | Cell tray / 电芯托盘 | Generic cell carrier for loading and visualization. | 2–12 | 0.5–1.8 × 0.05–0.3 × 0.5–1.8 | rack levels | prismatic | running, idle, fault; quality result as configured | tray-in, tray-out | L: functional placeholder |
| B12 | Electrical contact bank / 电接触探针组 | Optional active formation/test interface. | 0–12 | 0.3–1.5 × 0.1–0.5 × 0.3–1.5 | above/beside tray level | prismatic | running, idle, fault; quality result as configured | dc-power | L: functional placeholder |
| B13 | Power electronics cabinet / 功率电源柜 | Optional active-bay electrical service cabinet. | 0–2 | 0.5–1.5 × 1–2.5 × 0.4–1.2 | rear/side service zone | fixed | running, idle, fault; quality result as configured | power-in, dc-power | L: functional placeholder |
| B14 | Airflow plenum / 通风均流箱 | Represents optional bay cooling or conditioned airflow. | 0–2 | 0.5–2 × 0.2–2 × 0.2–1 | rear/upper rack | fixed | running, idle, fault; quality result as configured | cooling-in, exhaust-out | L: functional placeholder |
| B15 | Bay transfer interface / 货位移载接口 | Defines attachment to external handling equipment. | 1–2 | 0.3–1.5 × 0.1–0.8 × 0.5–2 | aisle face | fixed | running, idle, fault; quality result as configured | tray-in, tray-out | L: functional placeholder |
| B16 | Bay status indicator / 货位状态灯 | Makes occupancy and fault state legible. | 1–4 | 0.03–0.2 × 0.03–0.2 × 0.02–0.1 | aisle-side upright | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |

## Variant rules

- Select active electrical formation/capacity bay or passive aging bay. Passive bays disable electrical contact and power module rows.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B11` Cell tray: prismatic; demonstration joint motion; not measured kinematics.
- `B12` Electrical contact bank: prismatic; demonstration joint motion; not measured kinematics.

## State slots

These are application visualization slots, not controller logic or a validated operating procedure. `NG-reject` changes routing only on variants with an explicitly authored reject route. Do not animate service leaves during a running cycle.

- `idle`: Ready/inactive illustration; no process motion.
- `running`: Generic process demonstration. No real cycle time or controller logic.
- `fault`: Illustrative fault indication; hold process joints.
- `NG-reject`: Optional failed-quality result; route only where the configured variant has a reject mechanism.
- `maintenance`: Demonstration access pose, disconnected from process motion.
- `loading`: Generic incoming material handoff.
- `unloading`: Generic outgoing material handoff.
- `empty`: ASSUMED generic empty visualization slot; no measured timing or recipe.
- `occupied`: ASSUMED generic occupied visualization slot; no measured timing or recipe.
- `cycling`: ASSUMED generic cycling visualization slot; no measured timing or recipe.
- `aging`: ASSUMED generic aging visualization slot; no measured timing or recipe.

## Sockets

Attachment nodes are authored from the generic envelope. No source positions, connector standards, pipe bores, voltage ratings or exact mating geometry are supplied. Default material flow is +Z with +Y up; +X is the service/operator side. Re-map any imported prototype axes explicitly.

| Socket | Type / direction | Generic location |
|---|---|---|
| `air-in` | utility / in | service face |
| `cooling-in` | utility / in | service face |
| `data` | utility / service | service face |
| `dc-power` | utility / service | service face |
| `exhaust-out` | gas/duct / out | upper/service collar |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |
| `tray-in` | material / in | entry boundary |
| `tray-out` | material / out | exit boundary |

## Modelling notes

Build a repeatable bay with independent occupancy. Distinguish passive dwell from active contacted bays. Avoid copied bay counts, rack rows, tray populations or electrical ratings.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.

