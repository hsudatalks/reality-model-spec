# Reality Model Specification

模型师共享材料、工具说明与任务模板的统一公开入口。文档版本 **0.1.1（2026-11-04）**；当前元数据参考区分 **Player ModelABI 1.1** 与历史平台1.0静态输入；intake11.1已发布，本机未安装执行。需要公开分享的制作材料和工具从本仓库索引；资产交付仍按具体任务约定进行。

## 资源、工具与模板索引

| 入口 | 用途 |
| --- | --- |
| [官方工具与使用说明](tools/README.md) | Blender、Khronos Validator 的获取、基本用法、版本记录及本地文件校验 |
| [模型任务模板](templates/model-task.md) | 填写制作范围、尺寸依据、权利、消费契约与交付证据 |
| [母版制作](docs/authoring.md) | 坐标、锚点、几何、材质与可重建源 |
| [Runtime 与 LOD](docs/runtime-and-lod.md) | 平台派生职责、等级结构、预算与能力边界 |
| [参数化设备](docs/parametric-equipment.md) | 可重建参数源、几何/节点联动及分阶段工序闭环 |
| [数据驱动动画](docs/data-driven-animation.md) | 状态槽、节点映射、时间行为与输入→pose 验收表 |
| [元数据与交付](docs/metadata-and-delivery.md) | 完整 12 键 ABI、来源权利、文件 SHA 与轻量检查 |
| [贡献与公开范围](docs/contributing.md) | 哪些材料可以公开，提交范围与敏感信息约定 |
| [官方格式资料](https://registry.khronos.org/glTF/specs/2.0/glTF-2.0.html) | glTF 基础格式参考；更多工具资料见工具索引 |

## 从这里开始

1. 用[任务模板](templates/model-task.md)确定范围、尺寸依据、权利与消费场景。
2. 按[母版制作](docs/authoring.md)交付高质量 `.blend`、无损 GLB 和可重建依赖。
3. 按[元数据与交付](docs/metadata-and-delivery.md)填写 ABI、文件大小和 SHA-256。
4. 需要动作时，先填写[数据驱动动画](docs/data-driven-animation.md)的消费契约与验收表。
5. [Runtime 与 LOD](docs/runtime-and-lod.md)由平台从母版确定性派生，作者无需自行制作 runtime。

## 适用范围与状态

本版规定通用几何、坐标、材质、母版交付和 runtime 目标。运行时预算不限制质量母版；静态派生能力不代表动画、蒙皮或其他扩展已获支持。LOD、编码及动作仍须在固定版本的真实消费者中验证。

本文中的“必须”是制作或交付要求，“目标”是平台 runtime 的性能设计目标，“待确认”表示尚无可执行契约。modelABI 是应用级约定，不是 Khronos 标准扩展或完整消费语义 schema。特殊锚点、接触、轨距、挂点和数据绑定由具体消费契约确认；不得以字段存在代替语义验收。

静态草稿完成必要的文件、元数据及确定性格式检查后，即推进已授权的下一步，并向生产者反馈明确结果；正式 active 状态须经过消费者场景验收流程。草稿通过不代表正式激活。

除明确标注为草稿研究参考的最小材质参数摘要外，示例标识与数据均为虚构示意，不指向真实项目或资产。公开本文档不授予任何现有模型、贴图、参考资料或依赖的使用许可；资产权利必须逐项声明。本版暂未附文档 LICENSE，公开可读不等于授予开源许可。

版本变更见 [CHANGELOG](CHANGELOG.md)。使用本规范时记录文档版本或 commit，以及消费契约的固定版本。

## 官方格式资料

- [Khronos glTF 2.0](https://registry.khronos.org/glTF/specs/2.0/glTF-2.0.html)：坐标、节点变换、PBR 材质和动画等基础格式定义；本规范另外要求资产正面为 +Z。
- [Khronos glTF Validator](https://github.com/KhronosGroup/glTF-Validator)：格式检查工具；格式有效不等于尺寸、权利或消费行为已验收。

## 草稿设计参考

- [人物系列材质槽草稿参考](docs/reference-palettes/person-draft.md)：仅研究，未系列定版，不包含模型或素材使用授权。

- [通用冷却塔静态母版 brief](docs/briefs/hvac-cooling-tower-static.md)：原创合成视觉设计与静态部件范围，允许外发；权限仍按具体任务。

- [通用 AHU 静态母版 brief](docs/briefs/hvac-ahu-static.md)：原创合成、允许据此为本项目制作；任务权限单独确认。
- [经授权参考 GLB 发布流程](docs/reference-exports.md)：Releases 参考文件与 Library 生产资产区分；含已发布的参考清单。

- [通用室内服务机器人静态母版 brief](docs/briefs/social-service-robot-static.md)：原创合成、用于总览及点击聚焦；正式 kind/状态绑定由消费方确认。

- [紧凑通用 AMR／AGV 静态母版 brief](docs/briefs/social-agv-static.md)：原创合成、0.8×0.6×1.2m室内移动机器人；两个消费角色共用，正式载荷/状态接口待确认。

- [通用智能寄存柜静态 brief](docs/briefs/social-smart-cabinet-static.md)：原创合成静态范围。
- [通用充电坞静态 brief](docs/briefs/social-charging-dock-static.md)：原创合成静态范围。

- [通用室内配送机器人静态 brief](docs/briefs/social-delivery-robot-static.md)：原创合成静态范围。

- [通用明装风机盘管静态 brief](docs/briefs/hvac-fcu-static.md)：原创合成静态范围。

- [通用原创无品牌四旋翼巡检无人机静态 brief](docs/briefs/social-drone-static.md)：原创合成、允许公开传播及本项目制作。

- [通用合成房间外壳模块静态 brief](docs/briefs/generic-room-shell-static.md)：原创合成、允许公开传播及本项目制作。

- [通用固定式摄像头及简单支架静态 brief](docs/briefs/social-camera-static.md)：原创合成、允许公开传播及本项目制作。

- [工业设备通用 BOM brief 索引](docs/briefs/industrial-bom/INDEX.md)：24 类共 365 行，另附合成 stacker；尺寸为设计范围、参考单位未验证，动作接口为候选，非已批准消费契约。公开文档不授予母版或参考资产的额外许可。

- [通用滚筒输送机参数母版 brief](docs/briefs/factory-roller-conveyor-parametric.md)：仅3m/4m两组合成参数候选，一期静态交接已完成；phase2a文档补充已作者交付待回执。
- [通用双出口分选机参数母版 brief](docs/briefs/factory-sorter-parametric.md)：固定外框、两个出口间距参数集，一期静态交接已完成；新phase2a布局待ACK，非已实现OK/NG业务。

- [通用工业边缘网关静态 brief](docs/briefs/social-edge-gateway-static.md)：原创合成静态范围，消费 kind 待定。

- [通用传感节点静态母版 brief](docs/briefs/social-sensor-node-static.md)：原创合成紧凑外壳，非相机或网关，消费 kind 待确认。

- [滚筒输送 phase2a 接口与动作准备](docs/briefs/factory-roller-conveyor-phase2a.md)：仅文档补充，原L3/L4不变。
- [分选 phase2a 生产布局](docs/briefs/factory-sorter-production-layout-phase2a.md)：3×2×5m、两档S，awaiting_ack。
- [涂布参数源 phase2](docs/briefs/coater-parametric-phase2.md)：新增W/H两组，作者本地完成、未收件。
- [通用车辆单杆道闸静态 brief](docs/briefs/social-barrier-gate-static.md)：已作者交付待回执。
- [通用双圆盘洗地机器人静态 brief](docs/briefs/social-floor-cleaning-robot-static.md)：已作者交付待回执。

- [OPS subject exact-token style reference](docs/style/ops-subject-model-style-ref.md): Apps-authorized public mirror with three synthetic PNGs; Blender PBR remains untested.
