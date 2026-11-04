# 通用固定式摄像头及简单支架静态母版 brief

本 brief 是原创通用合成设计规范，允许公开传播，并据此为本项目原创建模、修改和交付；不替第三方数据、模型、贴图或依赖授予许可，也不把其他资产或仓库改授CC0/MIT。

合成假设：X0.20/Y0.18/Z0.35m；mount_base、bracket、camera_body、lens_cover独立，镜头朝+Z；记录候选安装面，标准AABB底中心不冒充墙安装锚点或socket。镜头可用深色材质。不做PTZ、视频采集/识别/覆盖视锥/联网能力、动画。

米、+Y up、+Z front，完整AABB底中心原点Ymin=0；中性共享PBR、ASCII语义nodes，无烘焙光影、状态色或文字。母版不设额外面数硬阈值。交付静态无损blend与GLB、可重建source依赖、meta/manifest/制作文档、逐文件bytes/SHA256和绑定实际GLB的必要官方Validator 0 error报告。平台负责runtime LOD与压缩。

来源是既有通用模型需求，具体项目subject/relation与动态消费契约由消费方提供；本brief不声明已绑定任何场景。
