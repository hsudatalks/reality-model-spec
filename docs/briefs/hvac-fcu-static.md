# 通用明装风机盘管（FCU）静态母版 brief

本 brief 是原创通用合成设计规范，允许公开传播，并据此为本项目原创建模、修改和交付；不含客户参考，不将其他资产或整个仓库改授 CC0/MIT。

合成假设完整 AABB X/Y/Z = 1.2×0.6×0.3 m，米、+Y up、+Z front，底面中心为原点、Ymin=0。明装箱式风机盘管，`housing`、`front_service_panel`、`fan_rotor`、`outlet_louvers` 独立；横向长风扇局部 X 为候选旋转轴，记录枢轴位置。可参考作者自身 AHU 同族中性 PBR，不用私密客户或其他作者几何。不猜风量、冷量、工艺或管口 sockets；不做动画、LOD 或压缩。

交付无损 blend 与 GLB、可重建源依赖、manifest/meta、制作文档、逐文件 bytes/SHA256、绑定实际输入的官方 Validator 0 error 报告及真实来源许可。干净几何、少量共享中性 PBR，ASCII 对象及 mesh 名；无烘焙场景光影、状态色和文字。纯色可无纹理，使用纹理须合法且 GLB 内自包含。母版无固定面数上限，平台负责运行时派生；正式状态和 sockets 待消费方契约。具体交付权限按任务确认。
