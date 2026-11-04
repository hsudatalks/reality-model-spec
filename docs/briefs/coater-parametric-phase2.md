# P1-A1：涂布机参数源 phase2

P2，edge-01，任务 `P1-A1/parametric-source-phase2`。已明确 ACK，随后作者报告本地完成；**local-only / 未上传 / 未收件 / 未独立验收**。本原创合成 brief 可公开，不授予模型 CC0/MIT、公开或跨客户复用许可。

## 有限参数范围

只新增 X/Y/Z 两组 **(3.6,3,6)m**、**(3,3.3,6)m**。连同一期 (3,3,6)、(3,3,7.2)，总共四个离散演示集，不是连续参数域。旧两组和原55文件不动。

复用作者自己的 source/material，实际按 W/H 联动生成 frame、enclosure、support 及 roller，不能用 root 非均匀缩放替代。最终 GLB 为米、+Y up、+Z front，完整 AABB 底面中心；两辊中心为 `(0,0.45*H,±0.43*L)`，候选转轴 local X。保持圆截面，作者自检节点 unit scale，记录实际节点/parent/rest TRS、辊心与轴，不造 slot、速度、限位、socket 或 ABI 映射。

## 输出与权限

沿旧 source 的真实稳定 ID，不猜新 ID；新作者输出版本0.2.0，不覆盖原件。交新增两组无损 blend/GLB、可重建 source/params/dependencies、README/meta/manifest、尺寸与节点联动记录、逐文件 bytes/SHA 和绑定输出 SHA 的必要官方0 error报告。无 state/clip/drive、LOD 或压缩要求；不以未来消费合同阻塞静态演示。此 coater 不是 battery-chain1 的第四族，factory 契约不能直接套用。

作者报告33项 SHA及两份官方0 errors/0 warnings，宽样例 GLB SHA256 `15e70d91f98a26cf347e94d1c07bb2969e78591e9e9a1304b7b73b728ed977b8`，高样例 `0b33d8eb80ecf45ceac6f896fee164b59d75d68ac4198adcf15ad89461476886`。这些是作者证据，不是独验 PASS。

原11件、coater两 phase 和 trailer0.1.2 全部保留既有本地限制：无建云目录、上传、重试或改权限授权。本地完成不增加已实收资产数。参见[一期 brief](coater-parametric-phase1.md)及[参数化设备](../parametric-equipment.md)。
