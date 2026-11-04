# 静态任务所需的 Player ModelABI 1.1 子集

参考日期：2026-11-04。本页是这次静态任务可访问的声明参考，包含实际读取的类型原文摘录和完整静态声明例。它不是全 ABI schema、独立可编译的 types 模块或新造接口，也不证明平台 intake 或消费测试通过。

来源：`hsudatalks/univers-aip-lib-ts-scene-player`，`packages/types/src/model.ts`，resolved commit `bb7b89c42d06fef98a0ae72ccca1eb6e03eeb2ea`，完整源文件 SHA256 `5d18f190ac82eecee88d4d8896a878edcc0ac98fc2c3670df64655ab9136c265`。models通过既有授权 gh API 实际读取该固定版本。作者反馈该源仓库 raw 链接返回404；源链接并非作者可访问前提，本公库文档提供必要摘录，不改变源repo权限，也未复制其他源代码或私有项目数据。下列静态JSON及kingpin声明亦已由delivery确认。

## SocketDecl 原文（82–92行）

```typescript
export interface SocketDecl {
  readonly name: SocketName;
  /** glTF node name that carries the socket frame. */
  readonly node: string;
  /**
   * ABI 1.1 (7.1 V0): declared mating tolerance, used by the offline invariant
   * gate. The expected orientation IS this socket node's authored frame.
   * Absent = checked at float32 precision only, reported as undeclared.
   */
  readonly tolerance?: { readonly metres: number; readonly radians: number };
}
```

`SocketName` 在源模块从 `./ids.js` 导入，本页不重定义它；本次任务名称 `kingpin` 已由消费者确认。位置/朝向使用 glTF node 的 authored TRS，处于 unscaled model root frame；SocketDecl 不新增 xyz、position、rotation 属性。tolerance 缺省只按float32检查并标undeclared；本次明确声明 metres .01 / radians .0175，不省略。

## ModelABI 原文（95–110行）

```typescript
export interface ModelABI {
  readonly version: `1.${number}`;
  readonly units: 'm';
  readonly up: 'Y';
  readonly forward: '+Z';
  readonly states: readonly StateDecl[];
  readonly drives: readonly DriveDecl[];
  readonly sockets: readonly SocketDecl[];
  /** Socket used as the first-person eye (+Y forward, +Z up in socket frame). */
  readonly eye?: SocketName;
  /** ABI 1.1 display remains separate from pose and attachment state. */
  readonly display?: DisplayDecl;
  readonly textSlots?: readonly TextSlotDecl[];
  /** Descending fractions of viewport height separating geometry LODs. */
  readonly lodThresholds?: readonly number[];
}
```

原文七个必需属性就是 version、units、up、forward、states、drives、sockets，没有超出下例的其他必需属性。`eye/display/textSlots/lodThresholds` 是可选项，本静态任务不填写；相关引用类型不在此摘录中扩展。本任务只使用空states/drives，因此无需伪造StateDecl或DriveDecl。对未来非空state，已实读StateDecl要求 name、clip、loop、clock（scene/entry），appearance可选；没有phase-source字段，真实clip/业务动作须另有消费合同。

## 本次完整静态 modelABI 声明

以下JSON是GLB顶层 `extras.modelABI` 的完整值，不是整个GLB文件；不得放进节点extras替代顶层声明。实际GLB中须存在唯一命名的socket_kingpin节点，并按本任务已确认的root-unscaled TRS另存；不移动asset root、geometry或pivots。

```json
{
  "version": "1.1",
  "units": "m",
  "up": "Y",
  "forward": "+Z",
  "states": [],
  "drives": [],
  "sockets": [
    {
      "name": "kingpin",
      "node": "socket_kingpin",
      "tolerance": {"metres": 0.01, "radians": 0.0175}
    }
  ]
}
```

本次消费声明不额外补 id/kind/anchor/contact/gauge 等旧static12字段。资产身份与kind继续按作者真实声明放在外部meta；旧数据中存在的扩展字段由新修订的作者按来源处理，本页不授权改旧原件或猜schema优先级。**资产版本0.1.2与ABI版本1.1是两种版本**，不能混写。

外部meta的frame片段也应如实声明1.1，不为满足旧工具而填写1.0：

```json
{"abi":{"version":"1.1","units":"m","up":"Y","forward":"+Z"}}
```

这只是外部meta的abi片段，不是完整meta；id/version/kind、作者/许可/reuse/source/provenance等保留各自真实身份及原权利边界，新资产修订同步新SHA。不在GLB消费ABI里加资产版本字段。

## 平台兼容与当前任务边界

[元数据与交付](metadata-and-delivery.md)下方旧12键/ABI1.0仅历史platform静态/ISO输入口径，不能当成player1.1必填，也不能证明消费通过。当前intake/preflight是否接受此1.1及外部abi.version1.1，待c4正式声明/命令，本轮未实测；不称支持或拒绝，不让作者填1.0凑检查。无ABI静态fallback仍由delivery修复，尚无ready pin。

本静态修订仅在已确认scope内本地另存，保留旧版本；不含状态动画、coupling、物理/碰撞、工程功能或LOD压缩。成包后交真实SHA给消费方按固定types准入，尚未通过。静态源格式PASS与consumer NEEDS_FIX可同时成立；taxonomy stage不改GLB/ABI，也不解除consumer问题。
