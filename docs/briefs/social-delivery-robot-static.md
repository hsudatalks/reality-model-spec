# 通用室内配送机器人静态母版 brief

本 brief 是原创通用合成设计规范，允许公开传播，并据此为本项目原创建模、修改和交付；不含客户参考，不将其他资产或整个仓库改授 CC0/MIT。

合成假设完整 AABB X/Y/Z = 0.65×1.1×0.8 m，米、+Y up、+Z front，底面中心为原点、Ymin=0。原创无品牌室内轮式配送机器人，具有清晰载货舱及单扇独立前舱门，与紧凑 AMR 区分；`chassis`、`cargo_body`、`cargo_door`、四轮及 `status_light_cover` 独立。轮心 pivot 局部 X 为候选轮轴，前门铰链侧局部 Y 为候选铰链轴。记录尺寸和枢轴；仅静态外观，不做动画、LOD、压缩、导航、开锁或实际承载性能，不猜正式状态或 sockets。

交付无损 blend 与 GLB、可重建源依赖、manifest/meta、制作文档、逐文件 bytes/SHA256、绑定实际输入的官方 Validator 0 error 报告及真实来源许可。干净几何、少量共享中性 PBR，ASCII 对象及 mesh 名；无烘焙场景光影、状态色和文字。纯色可无纹理，使用纹理须合法且 GLB 内自包含。母版无固定面数上限，平台负责运行时派生；正式状态和 sockets 待消费方契约。
