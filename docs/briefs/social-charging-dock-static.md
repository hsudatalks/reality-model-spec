# 通用充电坞静态母版 brief

本 brief 是原创通用合成设计规范，允许公开传播，并据此为本项目原创建模、修改和交付；不含客户参考，不将其他资产或整个仓库改授 CC0/MIT。

合成假设完整 AABB X/Y/Z = 0.8×0.6×0.5 m，米、+Y up、+Z front，底面中心为原点、Ymin=0。原创无品牌落地充电柱/坞，与紧凑 AMR 配套；`base`、`post`、`contact_pad`、`status_light_cover` 独立。候选对接面朝 +Z，记录可视触点中心坐标；不是正式 socket 或电气功能。只做静态外观，不做动画、LOD或压缩；dock-allocation 的机器人本体复用 AMR。

交付无损 blend 与 GLB、可重建源依赖、manifest/meta、制作文档、逐文件 bytes/SHA256、绑定实际输入的官方 Validator 0 error 报告及真实来源许可。干净几何、少量共享中性 PBR，ASCII 对象及 mesh 名；无烘焙场景光影、状态色和文字。纯色可无纹理，使用纹理须合法且 GLB 内自包含。母版无固定面数上限，平台负责运行时派生；正式状态和 sockets 待消费方契约。
