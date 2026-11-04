# 元数据与交付

本页参考日期 **2026-11-04**，适用于 **modelABI 1.0 当前静态母版输入**。12 个必需键位于 **GLB JSON 顶层 `extras.modelABI`**，不是节点 extras。外部元数据保持一致，但不能代替 GLB 内嵌 ABI；此参考不提供完整消费语义 schema。

## 完整 12 键 ABI 参考

| 键 | 当前参考要求 |
| --- | --- |
| `id` | 字符串，作者确认的资产引用 `assetId@assetVersion` |
| `version` | 字符串 `"1.0"`，指 ABI 版本，不是资产版本 |
| `units` | 字符串 `"m"` |
| `up` | 字符串 `"Y"` |
| `forward` | 字符串 `"+Z"` |
| `kind` | 已声明的资产类别字符串，与外部 `kind` 一致 |
| `nominalDimensions` | 3 个有限正数，按 GLB 资产坐标 X 宽/Y 高/Z 长排列，单位米 |
| `anchor` | 当前静态输入参考为字符串 `"bottom-centre"`；特殊锚点需另行确认支持 |
| `contact` | 必须存在；具体结构与语义由消费契约确认 |
| `gauge` | 必须存在；具体结构与语义由消费契约确认 |
| `sockets` | 必须存在；具体结构与语义由消费契约确认 |
| `licence` | 真实许可声明字符串，与外部美式拼写 `license` 的值一致 |

例如，虚构引用 `example-crate@0.1.0` 中的 `0.1.0` 是资产版本；`extras.modelABI.version` 仍为 `"1.0"`。本仓库文档版本 `0.1.1` 又是另一项版本，三者不能混用。

可选 `extras.lodThresholds` 是与 `modelABI` 并列的独立字段，不是上述第 13 个必需键。阈值由消费场景实测；不为凑字段填写未经验证的数值。

轨道设备等特殊锚点应保留任务明确的实际原点；`bottom-centre` 参考不能冒充与其不同的轨道接触中点。当前静态入口仍有底部中心约束，尚未提供该特殊锚点的准确 ABI 写法；不要自造枚举、用未知占位或为通过检查移动母版。可继续几何与源母版草稿，在说明中记录实际原点定义和资产坐标接触候选点，正式 ABI 声明待最小消费契约及平台支持确认。

## contact、gauge 与 sockets 的语义边界

字段存在不代表已满足接触、轨道运行或吊装挂接契约。具体类型、坐标点和适用条件由消费者确认，所有空间值采用最终 GLB 坐标。

静态示例中，`contact: {"plane":"Y=0"}` 仅在确有底面测量证据时表达该接触面；`gauge: null` 仅表示确实无轨距或轨距不适用；`sockets: []` 仅表示本版未声明挂点。三者不构成吊装、挂接或动画功能认证，也不是可复制到任意资产的通用默认值。

本版不规定通用 unknown 编码。未知项列在交付说明的待确认表中，不以 `null`、空数组、不适用或自造对象掩盖未知；在相关语义确认后形成相应元数据修订。已满足静态草稿范围的事实不因未来复杂动作契约待定而扩大或缩小其含义。

## 静态 ISO 箱的最小元数据修订

普通静态 ISO20/40 箱可按上述事实声明进入仅存在性检查的草稿流程，无需等待未来完整吊装或动画契约。前提是作者已有底面 Y=0 的证据、该资产确实不适用轨距、此版确实没有声明挂点。不要为此重建几何、制作 LOD 或压缩母版。

在 GLB 顶层 `extras` 下写入以下对象；尖括号项必须由作者用真实声明替换，**不是可直接提交的完整实例**：

```json
{
  "modelABI": {
    "id": "<assetId>@<newAssetVersion>",
    "version": "1.0",
    "units": "m",
    "up": "Y",
    "forward": "+Z",
    "kind": "<author-declared-kind>",
    "nominalDimensions": [2.438, 2.591, 6.058],
    "anchor": "bottom-centre",
    "contact": {"plane": "Y=0"},
    "gauge": null,
    "sockets": [],
    "licence": "<same exact statement as external license>"
  }
}
```

这是 ISO20 的 X/Y/Z 尺寸；ISO40 的 Z 改为 `12.192`。这份声明不代表开门、标准角件配合、吊装、挂接或消费者验收。未知接触面不能复制示例冒充已测。

外部 `meta.json` 的必需字段为 `id`、`version`、`kind`、`author`、`license`、`reuse_rights`、`source`、`derivation`、`tags`、`abi`。其中 `tags` 是字符串数组，`id/version/kind/author/license/reuse_rights/source/derivation` 是非空字符串；`abi` 固定为 `{"version":"1.0","units":"m","up":"Y","forward":"+Z"}`。ISO 派生输入另写 `derive:{"profile":"iso20"}` 或 `iso40`；这是平台派生配置，不是要求作者交 runtime。`asset_id` 不能替代所需的 `id`；描述性 `axes`/`unit` 不能替代 `abi`。源件不需要填写 runtime 的 `lod`、runtime SHA 或派生回执。

沿用作者真实身份和既有权利限制，采用新的资产版本，外部 `id/version/kind/license` 与内嵌值一致。`source` 可复用已有原创来源说明；`derivation` 记本次元数据修订与旧母版出处。仅补充发生变化的无损 GLB、对应 meta、字节/SHA 和必要格式报告，更新已有可重建源记录；保留原稿，不重复上传未改的整批文件，不为元数据修订新增渲染或重建门槛。

## 外部说明、来源与权利

随包提供 manifest、制作/导出说明和外部元数据，复用并更新生产者已有文档。至少包括：

- 作者确认的单资产 `id`、资产 `version`、`kind`、平面 `tags` 列表，以及与 ABI 一致的坐标、尺寸和锚点信息。
- 外部 `abi` 参考：`{"version":"1.0","units":"m","up":"Y","forward":"+Z"}`；它不替代完整内嵌 12 键。
- `author`、`source`、`license`、`reuse_rights`、`derivation`：实际作者、来源、许可、允许复用范围与修订/派生关系；附可核对的 provenance 和权利依据。
- 尺寸出处、测量方法及 truth/假设说明；contact、轨距、挂点与可动节点的声明和消费契约 pin。
- 源文件、GLB、原始贴图与依赖清单，制作/导出工具版本、设置及可重建步骤，实际几何/材质统计与已知限制。
- 每个交付文件的相对名称、准确字节数与完整 SHA-256；明确本次交付范围、作者版本及可交接状态。

不得冒用他人的作者身份或将未知许可写成自有作品、公共领域或任意开源许可。权利声明覆盖模型、贴图、参考资料与依赖的实际范围；本公开文档不替任何模型授权。

缺内嵌 ABI 时由作者提供新的无损元数据修订 GLB，附新字节数、SHA-256、修订身份和变更说明，保留旧原件。不能用 sidecar 或消费端 adapter 冒充已补齐内嵌 ABI，也不预造尚未生成的 runtime SHA 或派生回执。

## 轻量交付检查与反馈

1. 确认本批范围、来源、文件落地、字节数/SHA-256 和依赖清单一致，保留原字节。
2. 核对必填外部元数据和内嵌 ABI，查看尺寸、锚点与材质的已有测量证据。
3. 提供 [Khronos glTF Validator](https://github.com/KhronosGroup/glTF-Validator) 的原始报告、工具版本与输入 SHA；要求 0 error，警告按原文记录。未运行写“未运行”，不算通过。
4. 完成必要的确定性预检后，推进已授权的静态草稿步骤，不重复人工检查或为非阻塞疑问增加确认轮次。动态行为和场景性能按消费范围另验。

向生产者明确反馈精确资产引用/版本、文件 SHA-256 和预检结论；失败时给出工具原文错误和需修改的项。草稿结论明确标为草稿，不写成已 active。正式 active 由消费验收流程决定。

已发布版本不可覆盖。修订保留出处与旧版本；平台派生的母版、runtime、回执 SHA 分别记录，见 [runtime 与 LOD](runtime-and-lod.md)。
