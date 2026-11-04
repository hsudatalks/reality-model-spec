# 外观检测柜参数化质量母版 — phase1

P1 / FACTORY-INSPECTION / parametric-master-phase1。原创合成静态无损母版，属于delivery G4第三族；当前为proposed、awaiting_ack，未认领或开工，不扩成第四类短链。沿作者中性PBR风格，不做品牌mesh文字、场景光影或状态色烘焙。

[固定公开BOM概念参考](https://github.com/hsudatalks/reality-model-spec/blob/51e37552c920ec74cd0631acc306d951b637ec79/docs/briefs/industrial-bom/inspection-machine.md)只用于分件概念，不是已完成母版、工程规格或客户拟合尺寸。不能复刻私有fit尺寸、使用客户raw。现有AIVM参数原型只是复用候选，安全generic源后续交来优先复用；当前未取得，不声称已复用，也不等待客户资料。

## 有限两组参数

唯一参数 `width_X_m ∈ {2.0,2.4}`，number、m；baseline X/Y/Z=2.0/2.4/2.0m，variant=2.4/2.4/2.0m。高度和长度固定。这仅是两组合成ASSUMED测试，不是连续工程全域或厂家真值。

米制、最终GLB +Y up、+Z为物料前进候选方向，AABB bottom-centre原点。不能用root非均匀scale替代宽向重建。

独立ASCII节点：base_frame、enclosure、service_door、infeed_deck、inspection_platform、outfeed_deck、camera_head、light_cover、support_legs。+X侧维护门localY仅候选铰链轴，pivot在实际门边缘；camera_head只表外观，不声明识别、摄影或采图能力。

宽变化联动机架、外壳和平台宽向重建；脚位X=±(W/2−.2)，门框/铰链X随+X侧壁联动。输送中心线X=0，几何入口[0,.8,−1]/出口[0,.8,1]及camera_head中心线X=0保持。进出口/轴/枢轴都是几何候选，不是formal sockets或动作接口。

## 交付与必要检查

两组参数表、可重建源、每组blend与无损GLB；附bbox、脚位、门铰链及进出口/相机中心线联动表，真实逐文件bytes/SHA、来源/许可/reuse/provenance与manifest。只验证这两组，提供必要官方格式报告且0error，warning如实记录；不fuzz参数域、不新增重渲或完整工程测试。

不含相机/采图/OKNG逻辑、clip/rig/状态绑定、LOD/压缩、真实工艺流程、碰撞或工程验收。delivery后续提供固定battery-chain1-spec再对齐；本次静态范围不声称短链已可运行。运行时派生归平台，不套母版面数门槛。

候选源id/version：studio-generic-cell-inspection@0.1.0，由作者确认未占用版本；只用作者现有授权目录FACTORY-INSPECTION/<version>/DRAFT，不扩权限或许可，不覆盖原件/旧版本。复用已有制作/交付README，交付声明给准确文件范围和路径。静态完成不等于正式Library或消费验收。
