# Factory 三族：从静态母版接续到动作候选

本 brief 是 proposed / awaiting_ack 计划，不是派工或开工。1 主任务加 1–2 明确有序后续，逐项 ACK 后才认领；无明确后续时不填满任务包。采用作者自己的无损母版与 Book / Studio 中性风格，不新堆静态设备。米、+Y up、+Z front；业务流程、逐颗 custody、OK/NG、数值绑定和实例控制由消费方实现，producer 负责 GLB/节点及获确认的动作能力。

已发布语义：`factory.conveyor.speed` 是 m/s、occupancy 是整数；`factory.inspection-machine.headStroke` 是 signed m、cycleTime 是 s；`factory.sorter.diverterAngle` 是 rad、flow 是 1/h；lane occupancy/capacity 为整数且 occupancy≤capacity，cell serial 是文本、quality 是 uninspected/OK/NG。硬件极限、数值 channel/index、source field 和正式节点绑定仍需 owner 明确，不把 kind/单位全部写成未知，也不复用旧 production-line.speed 的 % 或把局部 field82 当 MODEL_STATE。

## 可先 ACK 的主任务：辊子归一化旋转

建议 Hidden 接 `FACTORY-CONVEYOR/normalized-roller-clip-phase2b`。复用已交两档 L=3/4m、X=1.2m、Y=.8m、半径名义 .05m 的 source；保持 rest geometry、材质、节点名字与位置。L3 为 roller_01..14，L4 为 roller_01..19；它们各自在辊心，local +X 正转使辊顶趋向 +Z。只转 roller tube，不移动机架、不把未声明绑定的端盖强行 parent 或跟转。

候选 clip 名 `roller_transport_cycle`：**1s 归一化一周**，每个目标绕自身 local +X 一周，至少 0/.25/.5/.75/1s 五个季度采样以避免 0/2π 同四元数导致不转或插值反向；采用 glTF 合法 LINEAR 旋转采样，首尾同姿态、保持 rest translation/scale。不添加 skin/morph 或新的设备几何。1s 是动作参数化基准，不是工艺 RPM。

作者交每档新无损 blend/GLB、新未占版本、source/dependency/invocation、实际 node→clip channel 表、rest/axis/radius 依据、duration/interpolation、逐文件 bytes/SHA 与绑定新 GLB SHA 的必要 official 报告；只检查新动作必要目标/端点，不重复旧静态审查或多视图渲染。旧 GLB/source 保留，原许可与交付入口不变，不要求作者 LOD/压缩。

速度→phase 的消费绑定由 delivery+85 按现有合同决定；`omega = v/r`（无滑移假设）只供核量纲，不在 GLB 或新自定义接口中写 mapper，不把 occupancy 当旋转量。正式 slot/index、clock(scene/entry)、stop/hold/seek/reset 选定前，不伪造 ModelABI state/drive 或新服务字段。有序后续仅在 delivery+85 给出上述最小绑定和 socket frame/tolerance、平台确认动态保真后，再另 ACK：将同一 clip 接入既有 ABI、为正式 draft 提供 source→output 证据；未确认后续不算生产任务。

## Inspection：先明确真实检测头

既有两档 W=2/2.4、H=2.4、L=2m 是静态光学外观候选。`camera_head` / camera_body 是相机外观，不能将其平移冒充电测头，也不能把 maintenance door 当 headStroke。电测方案需要真实 head/nest、接触原点、轴、rest 和机械范围；这些数值尚未确定，不指定假位移、不编 `head` 节点已存在。

可执行的候选前置为在作者自己的已交源上列出实际 head/nest 有无、可复用节点及缺口，并回报有限的头部/夹具 geometry 提案；不制作未知硬件。delivery 选择电测构型与 cell/nest/contact envelope、轴/零位和行程上下限后，producer 另 ACK 才补真实独立 head 及对应新无损动态母版。指定的 3300-tri 原型源资格与干净 generic 参数包需 owner/平台确认，不默认其已复用或获公开许可。

## Sorter：先完成已 ACK 生产布局，再对角位移

保持已有 phase2a 顺序：X/Y/Z=3/2/5m，S 仅1.2/1.6m，入口[0,.8,-2.5]、出口[±S/2,.8,2.5]，pivot[0,.8,0] localY、zero朝+Z。ref_infeed/ref_lane_a/ref_lane_b 仅 geometry。phase1 的2.4/1.2/3m紧凑箱不能替代此构型。

未来动作候选只针对真实 diverter 节点绕真实枢轴的 rad 角位移。生产版实际节点/rest/SHA、几何可达角域和净空由 producer 报告，delivery+85 确认合法角限、零位/插值与 lane index/socket tolerance 后再 ACK 新动态范围；不先写 ±π/4、占位 drive range 或 OK/NG 映射。

## 完成链

真实 source/参数/SHA → 新动态无损母版 → 原件收件及双份备份核验 → 平台正式支持的 preflight/不可变 draft（不激活） → delivery 以精确 Library version+digest 接入并给截图/replay → 批准后正式 activate 与消费可引用证据。动画/节点跨 LOD 保真是平台另行核验能力，静态 derive ready 不代表支持动画。当前 brief 不声称任何这些阶段已完成。
