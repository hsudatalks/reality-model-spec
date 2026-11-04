# Book：静态母版 ABI 1.1 元数据修订与经验页

本 brief 为既有任务的执行说明；是否 ACK/交付以主管账本为准。顺序为一项主任务加一项后续，逐项明确 ACK 才可认领；作者估时不是承诺。沿 Book / Studio 已认可中性风格，无新模型几何任务。

主任务：从作者自己的 RMG 与 walking 原件分别另存新作者资产版本 **0.1.1**（若已占用先报告，不覆盖），只修元数据。最终 GLB 顶层 `extras.modelABI` 使用以下七字段；外部 meta 的 `abi.version` 同步为 `1.1`，资产版本与 ABI 版本分开。

```json
{"version":"1.1","units":"m","up":"Y","forward":"+Z","states":[],"drives":[],"sockets":[]}
```

遵循[固定 player 1.1 类型说明](../static-player11-task-contract.md)。不添加旧 12 字段或把未实现动作写成 state/drive。RMG 保持 30m gauge；walking 保持左支撑脚原点。geometry、材质、root、节点、几何 JSON 与 BIN 保持原样，权利不扩；只在新 source/blend 与新 GLB 中同步必要元数据，主管不得代改原件。给出新旧 BIN 与 geometry JSON 摘要及 SHA 比对，说明允许的 metadata 差异。若导出器改变几何或 BIN，先报告阻塞，不为凑检查重建几何。

交新无损 blend、GLB、meta/manifest、每文件 bytes/SHA，以及绑定新 GLB SHA 的必要 official 格式报告；保留旧版本。只用原已授权交付入口及原许可，不恢复任何历史受限上传。完成的是作者修订，正式 preflight、草稿及消费准入由主管/平台/消费方继续办理。

有序后续：主任务交付后，交 **一页 Markdown + 同内容 PDF**，用既有房间和站厅两例总结比例、分件、材质与可重建交付心得。复用作者已有 README/manifest/制作文档，不新做模型或渲染、不补场景状态逻辑；逐条标明可复用经验与未验证项。此页不扩大两个例子的公开或跨客户权利。

本任务不要求 runtime/LOD/压缩。Library 精确版本+digest 且消费可引用，才计最终成果；source PASS 或作者完成不能替代。
