# 通用合成房间外壳模块静态母版 brief

本 brief 是原创通用合成设计规范，允许公开传播，并据此为本项目原创建模、修改和交付；不替第三方数据、模型、贴图或依赖授予许可，也不把其他资产或仓库改授CC0/MIT。

合成假设：X6/Y3.4/Z8m；四墙、floor、ceiling分别节点可隐藏；墙厚0.15m、floor厚0.15m、ceiling厚0.15m；+Z前墙留净宽1m/高2.1m开口，从地板顶面起。不做门扇/家具/设备。可沿Book已有Concrete_WarmGrey同族材质，不引用他人几何。供HDB/GBB/PSA/factory/venue合成场景，非实际户型；区别于三层building-shell和concourse。不声明导航/碰撞/消防/无障碍合规/实际户型语义或动画。

米、+Y up、+Z front，完整AABB底中心原点Ymin=0；中性共享PBR、ASCII语义nodes，无烘焙光影、状态色或文字。母版不设额外面数硬阈值。交付静态无损blend与GLB、可重建source依赖、meta/manifest/制作文档、逐文件bytes/SHA256和绑定实际GLB的必要官方Validator 0 error报告。平台负责runtime LOD与压缩。

来源是既有通用模型需求，具体项目subject/relation与动态消费契约由消费方提供；本brief不声明已绑定任何场景。
