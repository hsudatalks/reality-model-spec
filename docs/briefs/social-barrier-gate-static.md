# SOCIAL-GATE：通用车辆单杆道闸静态母版

P2，Server，任务 `SOCIAL-GATE/generic-barrier-gate-master`。已明确 ACK，随后作者交付目录；当前 **author_delivered_receipt_pending**，排队未启动下载，未实收或独验 PASS。本原创合成 brief 允许公开传播及本项目制作；资产来源与权利沿作者真实声明，不新增 CC0/MIT 或跨客户许可。

## 静态范围

闭杆完整尺寸 X=4.5m、Y=1.2m、Z=0.45m，synthetic/assumed。cabinet在bar一端、arm沿+X；`base`、`cabinet`、`arm`、`hinge`、`light_cover` 分别独立、ASCII语义名，允许记录作者实际语义映射。候选 hinge local +Z，记录实际 pivot 与 rest TRS，不假定机械限位。

GLB单位米、+Y up、+Z front/车道方向，完整 AABB 底面中心、Ymin=0。中性 PBR，无logo、文字、状态色或场景光影烘焙。无控制、检测、安全功能、socket、动画、LOD 或压缩；静态模型不等于实际通行/安全或消费认证。母版不设 runtime 面数门槛。

## 交付与证据边界

作者 DRAFT 身份 `server-generic-barrier-gate@0.1.0`，不是 Library ref。kind未知，不造消费字符串。无embedded ABI允许本静态scope；若作者提供，须使用合法player1.1声明，静态 `states`/`drives`/`sockets` 显式空数组，不混用旧12键。参见[元数据与交付](../metadata-and-delivery.md)。

沿Server既有授权目录，新task/version/DRAFT交无损 blend/GLB、可重建 source/dependencies、README/meta/manifest、逐文件bytes/SHA及实际GLB绑定的官方0 error报告；轻量核对范围/报告/尺寸/原点/分件，不追加重复渲染重建门槛、不覆盖旧资产。

作者报告31项name/size回读，实际下载GLB SHA `ff8e1883cb70e7e3000658e9b7732fb57a4e419aa78521cd224f59999b28ec1b`，官方0/0、rebuild一致；尺寸4.500000089×1.199999942×0.449999988m、origin residual 4.47e-8m均仅作者报告。浮点残差不是额外返工项，这些报告不是主管实收或独验。
