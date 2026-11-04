<!-- generic-briefs-research-v1 -->
> **Review boundary:** Generic design ranges and confidence are unchanged. Reference units are unverified; do not apply a blanket scale. Joints, states and sockets are conceptual candidates, not a runtime ABI, implemented capability or binding contract. Delivery and 85 must define the actual schema. LOD triangle ranges below are visual planning guidance for platform-derived runtime assets, not requirements on lossless author masters.

# Cell wrapping machine / 电芯包膜机

Apply an insulating film or wrap to a cell assembly.

**Status:** ASSUMED functional assembly brief for a generic master. Quantities, internal parts, joints and process behaviour require review; this is not a manufacturing BOM.

**Generic process.** ASSUMED generic process: present film, locate the cell, cut or pick a film piece, fold/wrap it around the cell, press the wrap and unload. Adhesive, heat sealing and film cut patterns are selectable assumptions.

**Master scope.** Guarded wrapping station or short multi-module line.

**Typical design envelope (m, width × height × flow length):** 2–10 × 2–5 × 4–22. These are broad design priors, not measured source dimensions or inferred production limits.

**Released reference ids:** `wrapping-machine-01`, `wrapping-machine-03`. References are for visual context only; physical units remain unverified.

**Merged evidence.** The released references show distinct rectangular line/enclosure forms, including a broad layout and a long narrow one. Film feed, folding tools and exact wrap architecture are not directly recovered. Duplicate or mirrored files do not establish installed quantity.

## Assembly BOM

All dimension entries are ranges in metres (local X × Y × Z before final module orientation). Quantity ranges are configurable generic counts; optional rows can be omitted. “M” means medium confidence in broad external form only; “L” means an assumed functional module. Neither validates part count, dimensions or motion.

| Id | Assembly (EN / 中文) | Function | Qty range | Approx. dimensions (m) | Location | Joint | States | Sockets | Confidence / evidence |
|---|---|---|---:|---|---|---|---|---|---|
| B01 | Base support assembly / 底部支承组件 | Supports the generic master and establishes its ground contact. | 1–1 | 2–10 × 0.1–0.6 × 4–22 | base | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B02 | Leveling feet or base pads / 调平支脚或底垫 | Provides configurable ground contact; count is a design choice. | 4–16 | 0.04–0.2 × 0.04–0.3 × 0.04–0.2 | base corners/supports | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B03 | Structural frame / 主体骨架 | Supports the visible panels or process modules. | 1–1 | 2–10 × 1–5 × 4–22 | main structural envelope | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B04 | Guard enclosure and panels / 防护及检修面板 | Defines protection/access surfaces; optional coverage on open structures. | 2–16 | 0.3–1.5 × 0.4–2.5 × 0.02–0.15 | outer/service faces | fixed | running, idle, fault; quality result as configured | — | M: external form; function assumed |
| B05 | Hinged access leaves / 铰接检修门 | Demonstration service access; actual hinges are unverified. | 2–12 | 0.3–1.2 × 0.5–2.2 × 0.03–0.15 | service face | revolute | maintenance | — | L: functional placeholder |
| B06 | Operator interface console / 操作面板 | Provides generic status and manual-control graphics. | 1–2 | 0.15–0.6 × 0.15–0.6 × 0.03–0.3 | operator/service face | fixed | running, idle, fault; quality result as configured | operator | L: functional placeholder |
| B07 | Status indicator / 状态指示灯 | Displays application running/idle/fault state. | 1–2 | 0.03–0.15 × 0.1–0.5 × 0.03–0.15 | visible upper service face | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B08 | Control and utility cabinet / 控制及公用工程柜 | Represents generic control/service volume without detailed wiring. | 1–2 | 0.3–1.5 × 0.5–2.5 × 0.2–1 | rear/service side | fixed | running, idle, fault; quality result as configured | power-in, air-in, data | L: functional placeholder |
| B09 | Film reel stand / 薄膜放卷架 | Presents a generic insulating film supply. | 1–2 | 0.4–1.5 × 0.5–2 × 0.4–1.5 | feed side | revolute | running, idle, fault; quality result as configured | film-in | L: functional placeholder |
| B10 | Film feed roller bank / 薄膜送料辊组 | Guides film to a cutting or pickup position. | 2–8 | 0.3–1.5 × 0.1–0.4 × 0.1–0.4 | film route | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B11 | Film cutting head / 薄膜切断机构 | Illustrates a generic cut action. | 1–2 | 0.2–1 × 0.1–0.6 × 0.2–1 | film preparation bay | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B12 | Cell locating nest / 电芯定位治具 | Holds the cell during wrapping. | 1–4 | 0.2–1.2 × 0.1–0.6 × 0.2–1.2 | central process bay | fixed | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B13 | Film pickup carriage / 薄膜取放滑台 | Transfers a film piece in a selected variant. | 0–2 | 0.3–1.5 × 0.2–1.5 × 0.3–2 | over fixture | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B14 | Folding paddle set / 包膜折边机构 | Represents a generic fold/wrap motion. | 2–8 | 0.1–0.6 × 0.05–0.4 × 0.1–0.8 | around cell nest | revolute | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B15 | Wrap pressing module / 包膜压合组件 | Illustrates final film contact. | 1–4 | 0.2–1 × 0.1–0.8 × 0.2–1 | after fold position | prismatic | running, idle, fault; quality result as configured | — | L: functional placeholder |
| B16 | Cell transfer shuttle / 电芯移载台 | Moves cells through the wrapping sequence. | 1–2 | 0.5–2 × 0.1–0.8 × 1–4 | lower line | prismatic | running, idle, fault; quality result as configured | cell-in, cell-out | L: functional placeholder |
| B17 | Film waste collector / 废膜收集组件 | Optional trim/waste handoff. | 0–1 | 0.2–1 × 0.2–1.5 × 0.2–1 | film preparation side | fixed | running, idle, fault; quality result as configured | film-waste-out | L: functional placeholder |

## Variant rules

- Select the module scope and optional rows before authoring the default master.

## Moving parts

Use separate groups and pivots for the following assumed motions. Stroke, axis, angle, speed and cycle timing are authored parameters; they are not recovered kinematics.

- `B05` Hinged access leaves: revolute; service pose only.
- `B09` Film reel stand: revolute; demonstration joint motion; not measured kinematics.
- `B10` Film feed roller bank: revolute; demonstration joint motion; not measured kinematics.
- `B11` Film cutting head: prismatic; demonstration joint motion; not measured kinematics.
- `B13` Film pickup carriage: prismatic; demonstration joint motion; not measured kinematics.
- `B14` Folding paddle set: revolute; demonstration joint motion; not measured kinematics.
- `B15` Wrap pressing module: prismatic; demonstration joint motion; not measured kinematics.
- `B16` Cell transfer shuttle: prismatic; demonstration joint motion; not measured kinematics.

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
| `film-in` | material / in | entry boundary |
| `film-waste-out` | material / out | exit boundary |
| `operator` | operator / service | service face |
| `power-in` | utility / in | service face |

## Modelling notes

Film reel, cell nest and folding paddles communicate the process. Keep the film geometry thin and simple, with selectable opaque/translucent materials. Do not reproduce actual die-cut patterns.

- LOD0: 8k-50k triangles per core module; readable working parts, principal rails, hinges and service collars; only demonstrated internals.
- LOD1: 2k-12k triangles per core module; retain silhouette, main bays, reel/roller rhythm, process opening, sockets and animated group pivots.
- LOD2: 200-1500 triangles per core module; envelope and dominant process volumes, simple material/status regions, major ports; no hidden internals.
- Author new primitives, surfaces and textures. Keep only one LOD visible, instance repeated modules, preserve sockets and animation pivots, and avoid hidden detail at distance.
- Use generic materials and symbols. Omit brand marks, plant labels, real tags, file-path metadata and source textures. Do not include source geometry.
- Review the selected process variant and optional modules before promoting the draft to a reusable master. Original triangle counts and component candidates are not generic assembly quantities.

