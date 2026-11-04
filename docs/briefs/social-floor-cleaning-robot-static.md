# SOCIAL-CLEANING-ROBOT：通用室内双圆盘洗地机器人静态母版

P2，mini，任务 `SOCIAL-CLEANING-ROBOT/generic-floor-cleaner-master`。已明确 ACK，随后作者交ZIP；当前 **author_delivered_receipt_pending**，指定收件队列第四项，未实收或独验 PASS。本原创合成 brief 允许公开传播及本项目制作；沿原project-only授权，公开/跨客户pending，不新增 CC0/MIT 许可。

## 静态几何

完整尺寸 X=0.65m、Y=0.70m、Z=0.90m，包含brush和rear squeegee，synthetic/assumed。下列语义部件分别独立：chassis、upper body、tank cover、wheel L/R、front caster、brush L/R、rear squeegee、sensor cover、light cover；使用ASCII节点名并记录作者实际映射。brush在前+Z，rear在−Z，wheel centre候选local X轴，brush centre候选local Y轴，记录实际pivot/rest TRS。

米、+Y up、+Z front，完整 AABB 底面中心、Ymin=0；中性PBR，无logo、文字、状态色或场景光影烘焙。静态brush 11mm、squeegee 4.5mm间隙主管接受，不强制归零。无真实清洁、导航、状态动作、动画、socket、LOD或压缩声明，母版无runtime面数门槛。

## 交付与身份

作者 DRAFT `mini-generic-floor-cleaning-robot@0.1.0`，非 Library ref。kind未知；no embedded ABI不构成本scope返工。若作者提供ABI，按[当前适用合同](../metadata-and-delivery.md)如实声明，不盲填旧12键。

沿mini已授权目录新任务/version/DRAFT交无损blend/GLB、可重建source/dependencies、README/meta/manifest、逐文件bytes/SHA、实际GLB绑定的必要官方0 error报告。轻量核对，不追加重复渲染重建，不覆盖旧原件或改权限。

作者交付ZIP声明5,233,562B、SHA256 `44ed49c056cec406d2c550ca95352b0379f05343ecca0384ce919f2a0c2e0839`，GLB SHA `a77f0c125f7f2f257cd1f7d12b2ae3d35cf761097613342ac163d5d659c8f592`；官方0/0和readback QA均自报，未独立核验。
