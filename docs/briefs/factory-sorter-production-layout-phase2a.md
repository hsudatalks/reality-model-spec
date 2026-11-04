# FACTORY-SORTING：phase2a 生产布局参数母版

P1，任务 `FACTORY-SORTING/production-layout-phase2a`，proposed_assignee=Legion，**awaiting_ack**；没有 ACK、认领或开工事实。本公开原创合成 brief 允许传播与本项目制作，不新增资产许可。复用作者一期 source，保留一期原件及原权利。

## 两组合成布局

新完整外框 X=3m、Y=2m、Z=5m；参数 S 仍只支持1.2/1.6m两组，不声明连续工程范围。米、+Y up、+Z flow，完整 AABB 底面中心。按新尺寸实际重建 frame、enclosure、support、main transport 及两个 branches，不使用 root 缩放代替生成。

| 几何候选 | 最终 GLB 坐标/方向 |
| --- | --- |
| infeed | `[0,0.8,-2.5]` |
| lane A/B outfeed | `[-S/2,0.8,2.5]` / `[+S/2,0.8,2.5]` |
| diverter pivot | `[0,0.8,0]`，local Y，zero pose 朝 +Z |
| reference empties | `ref_infeed`、`ref_lane_a`、`ref_lane_b`，+Y up / +Z flow |

reference empties 是几何候选，不是正式 sockets；A/B 不预绑定 OK/NG。保留可追溯语义节点，记录实际 parent/rest TRS、pivot、轴和点表；tolerance、index、source field、硬件限位与正式绑定未知，不补造。

## 输出与边界

沿用作者 ID `legion-generic-battery-sorter`，新作者版本 **0.2.0**，仅项目 DRAFT、非 Library ref。交新可重建 source/dependencies、两份无损 blend 和两份无损 GLB、params、rest TRS、候选点表、README/meta/manifest、逐文件 bytes/SHA-256 及绑定输出 SHA 的必要官方 Validator 0 error 报告，warning/info 如实列出。

沿作者已授权任务/version/DRAFT目录交付，不覆盖一期 source/版本、不改权限或权利。采用作者中性 PBR、ASCII语义名，无品牌文字或状态烘焙。不制作 state、clip、drive、LOD、压缩或填硬件限位；本期不是动态 G4/G5 通过。母版无 runtime 面数门槛，平台派生与消费绑定另验。

参见[参数化设备](../parametric-equipment.md)与[一期范围](factory-sorter-parametric.md)。
