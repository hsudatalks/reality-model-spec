# SOCIAL-EDGE-GATEWAY：通用工业边缘网关静态母版

本公开 brief 允许用于本项目原创制作和交付；不授予第三方资料许可，不把资产改授 CC0/MIT。用途是 Apps SOCIAL P2 通用设备可视化，不是厂家型号或已部署设备。

- 合成尺寸 X宽0.30 × Y高0.25 × Z深0.12 m，包含两根直立天线，truth=synthetic/assumed。尺寸参数写入制作源码；本次不要求多组参数验证。
- 米制，GLB +Y上、+Z前；完整可见几何 AABB 底面中心为原点，Ymin=0。
- 独立语义节点：body、front_panel、heat_sink、mount_base 或 mount_bracket、antenna_left、antenna_right、port_panel、status_light_cover。端口采用可视凹槽或几何盖板，非真实电气接口。
- 散热和端口轮廓在概览与近看均可辨；中性 PBR、语义材质名、ASCII 语义节点名。无品牌、网格文字、状态色或场景光影烘焙。不加母版面数硬门槛。
- 只记录候选安装面。不声明正式 socket、网络/无线/计算能力、可动轴、状态映射、动画或 rig；不制作 LOD 或压缩运行时。

交无损 .blend 与 GLB、可重建源码及依赖说明、README/meta/manifest、预览、逐文件 bytes/SHA256、绑定实际 GLB 的必要官方 Validator 0 error 报告。验收只作来源/哈希、报告绑定及尺寸/原点/必要分件的轻量核对，不增加重复渲染或重建门槛。平台负责运行时派生。

作者 DRAFT 身份 `mini-generic-edge-gateway@0.1.0`，不是 Library 引用。kind 的消费字符串未定，不自行创造；公开/跨客户复用权保持 pending，不将 brief 许可当成资产开源。动态契约未定不阻塞静态制作；不要盲填旧12键 ABI，不把不同版本契约混写。
