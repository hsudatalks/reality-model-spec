# 元数据与交付

## 当前消费合同：Player ModelABI 1.1（2026-11-04）

作者可直接使用本公库[静态任务子集、原文摘录与完整有效JSON](static-player11-task-contract.md)，不依赖源repo raw访问。此次消费声明只用version/units/up/forward/states/drives/sockets七字段，不额外补id/kind；identity/kind由外部meta据实声明。资产版本0.1.2与ABI版本1.1分开，外部abi.version也如实1.1，旧tool兼容性待c4，不填1.0凑检查。

已核对权威 [packages/types/src/model.ts](https://github.com/hsudatalks/univers-aip-lib-ts-scene-player/blob/bb7b89c42d06fef98a0ae72ccca1eb6e03eeb2ea/packages/types/src/model.ts)，固定 source commit `bb7b89c42d06fef98a0ae72ccca1eb6e03eeb2ea`。这是播放器的 GLB 顶层 `extras.modelABI` typed contract；外部 intake `meta.json` 是另一个平台输入合同，不能互相替代。下方保留的 static12 / ABI 1.0 是旧平台静态/ISO 输入参考，凑齐12键不等于播放器准入、动画可用或消费通过。

当前静态声明可使用合法的空 `states`、`drives` 数组。下例须确实存在唯一命名的 `socket_kingpin` glTF 节点，节点由任务约定其 authored TRS；这只是 typed 声明示例，不是任意模型的准入实测或挂接认证：

```json
{
  "modelABI": {
    "version": "1.1",
    "units": "m",
    "up": "Y",
    "forward": "+Z",
    "states": [],
    "drives": [],
    "sockets": [{
      "name": "kingpin",
      "node": "socket_kingpin",
      "tolerance": {"metres": 0.01, "radians": 0.0175}
    }]
  }
}
```

`SocketDecl`（82–92行）仅为 `name`、`node` 和可选 `tolerance:{metres,radians}`。位置和方向来自 glTF 节点在 unscaled model root frame 下的 authored TRS；不在 ABI 新增 xyz/position/rotation 字段。tolerance 缺省时按源码注释只按 float32 精度检查并报告 undeclared；上例显式声明容差不等于物理/工程配合验证。无已声明挂点的静态模型可用 `sockets:[]`。GLB 米、+Y up、+Z front 保持，播放器内部坐标转换只做一次。

非空 `StateDecl`（26–46行）必需 `name:string`、`clip:string`、`loop:boolean`、`clock:'scene'|'entry'`；可选 `appearance` 的 `color/emissive` 为三元数值、`opacity` 为数值。不存在 `phase-source` 这个属性；PHASE 是源码注释的时间语义。非空 states 必须指向真实 clip，不能用候选能力名代替。`DriveDecl`（17–25行）为 name/node/path/axis/range/default/interp，具体业务映射与插值值仍须钉版消费合同。静态无 clip/未实现驱动时正式数组留空，未来动作候选列 README，不伪造运行语义。

当前平台 intake/preflight 对上述1.1的支持声明和正式调用尚待 c4 确认，本轮未实测，不宣称接受或拒绝。旧无 ABI 的 generic 原件仍按其正式 adopt 外部声明路径保留，不自动要求每个母版改写。delivery 正修无 ABI 静态 fallback 并保留 diagnostic，尚无正式 ready pin，不能写成已发布支持。后续修改由作者另存新无损修订、同步真实资产版本/来源/新 SHA；不改原件或旧 DRAFT，也不用 retag 修改 GLB/ABI。

本页保留的历史参考日期 **2026-11-04**，下列12键是 **modelABI 1.0 内嵌声明及 ISO 派生输入参考**，位于 **GLB JSON 顶层 `extras.modelABI`**，不是节点 extras。它不是所有 generic-original adopt 路径的统一拒收条件；各路径以正式钉版工具合同为准。本参考不提供完整消费语义 schema。

## 历史平台 static12 / ABI 1.0 输入参考

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

## 人物支撑中心与几何中心

当前静态入口的 `bottom-centre` 校验要求 X/Z 几何包围盒居中；它不是任意接触点中心的通称。人物单脚实际支撑中心、双脚实际支撑面中心与几何包围盒底面中心是不同概念，不能直接视为相同的锚点或共用同一枚举。

截至 **2026-11-04**，人物单脚／双脚支撑中心目前暂无专用的已确认 ABI 枚举或消费契约；复用现有命名 socket 的映射仅为消费侧待确认提案，不是已生效的 schema。研究与交付说明应分别记录实际原点、支撑面定义和资产坐标，正式 `anchor` 写法及 `contact` 语义仍待最小消费契约及平台支持确认。

保留作者真实原点，不为通过入口移动已有母版、伪标 `bottom-centre`、自造特殊枚举或以 `null` 掩盖未知。语义待定不新增静态制作或检查门槛，也不等于已验证某个模型入库失败。standing 等人物工作仍按各自任务授权进行；本段不授予建模、上传或复用几何的权限。

## contact、gauge 与 sockets 的语义边界

字段存在不代表已满足接触、轨道运行或吊装挂接契约。具体类型、坐标点和适用条件由消费者确认，所有空间值采用最终 GLB 坐标。

静态示例中，`contact: {"plane":"Y=0"}` 仅在确有底面测量证据时表达该接触面；`gauge: null` 仅表示确实无轨距或轨距不适用；`sockets: []` 仅表示本版未声明挂点。三者不构成吊装、挂接或动画功能认证，也不是可复制到任意资产的通用默认值。

本版不规定通用 unknown 编码。未知项列在交付说明的待确认表中，不以 `null`、空数组、不适用或自造对象掩盖未知；在相关语义确认后形成相应元数据修订。已满足静态草稿范围的事实不因未来复杂动作契约待定而扩大或缩小其含义。

## 静态 ISO 箱的最小元数据修订（历史平台1.0参考）

本节保留旧平台ISO输入参考；它不能代替上方player1.1消费声明。1.1嵌入声明与外部intake meta的版本对齐及正式调用待平台确认，不将本例1.0固定值强套到新1.1修订。

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
- 外部 `abi` 参考：`{"version":"1.0","units":"m","up":"Y","forward":"+Z"}`；它是否适用及是否需要内嵌声明须按具体平台路径确认，不能替代播放器1.1合同。
- `author`、`source`、`license`、`reuse_rights`、`derivation`：实际作者、来源、许可、允许复用范围与修订/派生关系；附可核对的 provenance 和权利依据。
- 尺寸出处、测量方法及 truth/假设说明；contact、轨距、挂点与可动节点的声明和消费契约 pin。
- 源文件、GLB、原始贴图与依赖清单，制作/导出工具版本、设置及可重建步骤，实际几何/材质统计与已知限制。
- 每个交付文件的相对名称、准确字节数与完整 SHA-256；明确本次交付范围、作者版本及可交接状态。

不得冒用他人的作者身份或将未知许可写成自有作品、公共领域或任意开源许可。权利声明覆盖模型、贴图、参考资料与依赖的实际范围；本公开文档不替任何模型授权。

缺内嵌 ABI 是观察事实，不能直接当成所有路径的正式工具拒收。只有实际适用合同要求内嵌修订时，才由作者提供新的无损元数据 GLB、字节/SHA和修订说明，并保留旧原件；不得把外部声明说成已补内嵌 ABI，也不预造 runtime SHA 或派生回执。

## Generic originals：正式 adopt 的外部声明路径

已发布 `@univers/asset-intake@0.0.1-dev.utpub3.1`（source `27b0ece366ecb60bfb0a5c7eb851e7c7e225cd43`，包SHA256 `59f0266bd6e662a6e12c82058f2d06e46ede2ec303297dc549a0f7f689b7853a`）的 `package/README.md` §Explicit anchors and generic originals（249–281行）区分两条路径：ISO20/40 derive.profile沿用ISO流程；其他generic-original通过原字节自包含GLB及外部作者声明进入已有隐藏DRAFT路径。

该合同明确：给定真实explicit anchor及作者 `abi` frame 时，没有顶层 `extras.modelABI` 的静态原件可使用该外部坐标声明，无需重写母版，也不宣称完整contact/gauge/socket/消费ABI。已有embedded ABI仍检查其frame和身份；外部声明不能与之冲突。该能力不实现消费端placement或业务绑定。未声明LOD在此原件adopt路径默认为master，不据此要求作者造runtime。

因此，缺顶层ABI的generic原件先保留，登记 `formal_intake_metadata_requirements_pending_tool_check`，核具体路径所需的作者身份/kind/许可/外部frame/anchor等；没有实际适用的正式输入合同或工具拒收证据，不增GLB返工门槛、不造unknown字段。文档观察或格式报告不等于preflight通过。外部元数据确实缺少的真实作者声明仍需最小补齐，不能由管理者推造值。此处不提供新资产命令、不扩大运行/发布授权，也不要求重复adopt或发布测试。

## 轻量交付检查与反馈

1. 确认本批范围、来源、文件落地、字节数/SHA-256 和依赖清单一致，保留原字节。
2. 核对必填外部元数据和内嵌 ABI，查看尺寸、锚点与材质的已有测量证据。
3. 提供 [Khronos glTF Validator](https://github.com/KhronosGroup/glTF-Validator) 的原始报告、工具版本与输入 SHA；要求 0 error，警告按原文记录。未运行写“未运行”，不算通过。
4. 完成必要的确定性预检后，推进已授权的静态草稿步骤，不重复人工检查或为非阻塞疑问增加确认轮次。动态行为和场景性能按消费范围另验。

向生产者明确反馈精确资产引用/版本、文件 SHA-256 和预检结论；失败时给出工具原文错误和需修改的项。草稿结论明确标为草稿，不写成已 active。正式 active 由消费验收流程决定。

已发布版本不可覆盖。修订保留出处与旧版本；平台派生的母版、runtime、回执 SHA 分别记录，见 [runtime 与 LOD](runtime-and-lod.md)。
