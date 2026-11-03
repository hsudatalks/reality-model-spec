# 官方工具与本地使用

本目录提供可公开工具的统一索引与使用说明。本版不分发第三方二进制，也不提供自制检查脚本；使用官方工具和系统自带文件校验即可。工具辅助制作与检查，不替代平台确定性入库或消费者验收。

## Blender：制作、保存与导出

从 [Blender 官方下载页](https://www.blender.org/download/)选择任务确认的版本和操作系统发行包，按发行包说明安装或解压运行。生产任务固定确切版本，不以“最新版”作为交付记录；需要旧版时从[官方历史发行目录](https://download.blender.org/release/)获取。

基本流程：保存 `.blend` 母版，整理依赖，在 File → Export → glTF 2.0 中选择 GLB 导出，保留任务要求的几何、材质和动作能力。具体选项按对应版本的 [Blender glTF 导出手册](https://docs.blender.org/manual/en/5.0/addons/import_export/scene_gltf2.html)核对；该链接是版本化参考，不要求所有作者使用这个版本。任务记录实际导出设置，关闭 runtime 减面/压缩步骤；最后检查导出 GLB 的米制、轴、尺寸及顶层 ABI，不能假定普通节点自定义属性会自动生成顶层 `extras.modelABI`。

在 About Blender 查看版本/build 信息，或在已配置 Blender 命令的终端使用：

```sh
blender --version
```

随交付记录完整 Blender 版本、build/commit（可取得时）、导出器/插件版本和导出设置，以及重建所需依赖。仅提供截图或 `.blend` 文件不能替代约定的无损 GLB。

## Khronos glTF Validator：官方格式检查

从 [Khronos 官方 releases](https://github.com/KhronosGroup/glTF-Validator/releases)选择固定版本、适合本机系统的 CLI 发行包，解压后按包内说明运行；记录所用 release tag，不能只记下载日期。命令行及源码构建方式以[官方 README](https://github.com/KhronosGroup/glTF-Validator)为准。需要从源码构建时固定官方源码 commit，并遵循该版本的构建说明；不在本仓库另造构建链。

以下仅演示检查一个虚构名称的本地文件；假设 CLI 已加入终端命令搜索路径：

```sh
gltf_validator example.glb
```

工具默认写出 `example.glb.report.json`，有格式错误时返回非零退出码。保留原始 JSON 报告，核对 0 error，并据实记录 warning 和输入 SHA-256；本规范不要求批量遍历或反复重跑。不要关闭资源检查来掩盖错误。

随交付记录确切 release tag/源码 commit、发行包或可执行文件 SHA-256、实际命令/选项、输入文件 SHA-256；报告若给出工具版本也一并保留。通用格式检查不会验证本规范的完整 ABI、尺寸真值、许可或动画消费语义。

## 本地 bytes 与 SHA-256

这些命令只读取指定本地文件，不上传模型。`example.glb` 为虚构文件名示意。

Linux：

```sh
sha256sum -- example.glb
wc -c < example.glb
```

macOS：

```sh
shasum -a 256 example.glb
wc -c < example.glb
```

Windows PowerShell：

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath .\example.glb
(Get-Item -LiteralPath .\example.glb).Length
```

每个实际交付文件均记录准确字节数与完整 SHA-256，绑定作者版本和本批范围。哈希只证明字节身份，不证明 GLB 格式、几何或权利合格。

## 记录与公开边界

工具版本、输入 SHA 和报告随资产交付保存；真实资产报告可能含私有名称或路径，不直接提交到本公开仓库。公共工具说明只使用虚构相对文件名。不得在工具、配置或示例中加入密钥、账号配置、私有地址或平台私有实现；新增本地 helper 应无网络、无密钥，说明能力边界，并用一个小样本验证。完整要求见[贡献约定](../docs/contributing.md)和[元数据交付](../docs/metadata-and-delivery.md)。
