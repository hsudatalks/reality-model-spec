# Reality Model Specification

面向模型生产者的通用制作与交付规范。文档版本 **0.1.0（2026-11-04）**；当前元数据参考为 **modelABI 1.0 静态母版输入**。本文档不包含模型文件。

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

所有示例标识与数据均为虚构示意，不指向真实项目或资产。公开本文档不授予任何现有模型、贴图、参考资料或依赖的使用许可；资产权利必须逐项声明。本版暂未附文档 LICENSE，公开可读不等于授予开源许可。

版本变更见 [CHANGELOG](CHANGELOG.md)。使用本规范时记录文档版本或 commit，以及消费契约的固定版本。

## 官方格式资料

- [Khronos glTF 2.0](https://registry.khronos.org/glTF/specs/2.0/glTF-2.0.html)：坐标、节点变换、PBR 材质和动画等基础格式定义；本规范另外要求资产正面为 +Z。
- [Khronos glTF Validator](https://github.com/KhronosGroup/glTF-Validator)：格式检查工具；格式有效不等于尺寸、权利或消费行为已验收。
