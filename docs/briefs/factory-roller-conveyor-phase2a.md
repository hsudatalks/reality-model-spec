# FACTORY-CONVEYOR：phase2a 接口与动作准备清单

P1，Hidden，任务 `FACTORY-CONVEYOR/phase2a-interface-motion-inventory`。已明确 ACK，随后作者报告交付；当前 **author_delivered_receipt_pending**，不是独立实收或 PASS。本公开 brief 允许传播及本项目原创制作；不新增模型公开、跨客户复用或 CC0/MIT 许可。

本期只新增独立 Markdown/CSV 补充。保留一期 L3/L4 的 GLB、blend、源码及原23文件，不改几何、不重传、不重渲、不重复验证，也不制作 clip。

## 节点与接口记录

- 按 L3/L4 分组、各组按实际 Z 排序，覆盖实际全部33辊（14+19）。逐辊记录现有 node 名、parent、rest TRS、centre、local X 轴及半径0.05m；保留现有名字，不为符合示例重命名。
- 最终 GLB 单位米、+Y up、+Z flow。候选 `carrier-in`/`carrier-out` 为 `[0,0.8,-L/2]` / `[0,0.8,+L/2]`，quaternion xyzw `[0,0,0,1]`、contactY=0.8。全部标 **ASSUMED 几何候选，非正式 socket**；tolerance/index 未定，保留待确认，不编造值。
- 只记录候选 `roller_transport_cycle` 和绕 local +X 正转时辊顶趋向 +Z 的动作准备。速度、slot、限位及正式 ABI 映射未知，不填写假值，不创建动作或宣称动态通过。
- 实际不存在的 stop、door、side-out 明列 absent；endcaps 未 parent 的事实保留，不强绑层级。

## 交付

六份文档：`README.md`、`roller_nodes.csv`、`interface_candidates.csv`、`motion_preparation.csv`、`absent_features.csv`、`SHA256SUMS`。更新作者已有文档并关联原件身份/SHA；CSV 记录实际值及候选/未知边界。此补充不改变一期静态 PASS，也不是动态 G4/G5 或消费绑定验收。

参见[参数化设备与消费契约通知](../parametric-equipment.md)。该通知不替本清单定义 wire schema、速度、硬件限位或正式 socket。
