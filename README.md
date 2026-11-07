# 77 的技术美术实战

把 UE 制作中的问题、工具与流程讲清楚。面向游戏美术、技术美术和独立开发者，用真实工程和对照实验讲操作步骤、判断依据与适用边界。

## 从手头的任务开始

### 排查 Niagara 性能｜TA 实践手记 05

适合在排查粒子覆盖、透明阶段或 GPU 耗时的同学。先读两个尺寸条件下的三个采样窗口，再比较透明阶段与整帧 GPU 的读数。

自查：保持 88 个粒子和相同材质，只改尺寸时，哪些读数变化？这些读数能支持什么结论？

[打开在线读数练习](https://qiqideqi.github.io/ta05-niagara-gpu-timing-companion/#reading-exercise) · [下载离线伴读与原始数据](https://github.com/QIQIdeqi/ta05-niagara-gpu-timing-companion/releases/tag/v1.0.4)

### 做 UE 编辑器批量工具｜UE 工具蓝图实战 02

适合已经会用基础蓝图，正在做批量重命名或资产编辑工具的同学。先走一遍预览、重名检查和执行前复检。

自查：预览生成后改了规则，和生成预览时发现目标重名，界面各应怎样提示？

1. **只读练习包。** 在练习材质上用 `Old → New` 生成预览，再把替换值改成 `Other`。记录旧行是否保留、「核对当前规则」是否可用，以及重新预览后的目标名。
2. **完整版演示副本。** 在 DemoAssets 选中四个演示材质，输入 `Brick → Metal`。记录目标占用提示、阻止和可执行项数、按钮状态，以及左侧资源名称。

<details>
<summary>完成后核对结果</summary>

只读版改规则后，旧行可以保留，但「核对当前规则」禁用；重新预览才应出现 Other。完整版里 M_Old_Brick 的目标 M_Old_Metal 已存在，本例同时选中了原有目标。预览显示阻止 1 项、可执行 0 项，执行按钮禁用，四个资源名称保持原样。

</details>

[阅读 UE02 完整教程](https://zhuanlan.zhihu.com/p/2095285265053004093) · [只读预览练习与反馈](https://zhuanlan.zhihu.com/p/2095979973278437632)

### 梳理过场审核与交接｜过场制作实践 01

适合在整理过场材料、版本、审核意见与进度的同学。从一次审核和一次交接入手，梳理材料、负责人和最新状态。

自查：任选一条审核意见，能否同时写出对应 Sequence、材料版本、处理人和下一步？

[用 R001 和 R002 做一次接收方交接练习](过场交接练习.md)。先写记录，再展开参考答案。

[阅读过场制作实践 01](https://zhuanlan.zhihu.com/p/2094879283684578260) · [阅读 02：审核意见与交接](https://zhuanlan.zhihu.com/p/2096324332645507394)

[打开完整系列导读](https://zhuanlan.zhihu.com/p/2095704359396971810)

---

## English · Unreal Engine technical art practice

Choose a route based on the problem you are working on:

| Task | Start here | Try this |
| --- | --- | --- |
| Diagnose Niagara GPU cost | [TA05 illustrated guide and reading exercise](https://qiqideqi.github.io/ta05-niagara-gpu-timing-companion/measurement-notes.html) (English) | Hold particle count and material fixed. Compare translucent-pass and whole-frame GPU timings after changing sprite size. Which measurement supports your conclusion? |
| Build a safe batch-rename tool | [UE02 Editor Utility Widget tutorial](https://zhuanlan.zhihu.com/p/2095285265053004093) (Chinese) | Generate a preview, then change the rule. Can the old preview still be executed? Repeat with an occupied target name. |
| Hand off a cutscene review | [R001 / R002 handoff exercise](过场交接练习.md) (Chinese) | Given a review note, record the Sequence, reference version, owner and next action. Decide whether it is ready for review or needs clarification. |

English navigation was prepared with AI-assisted translation and checked against the original Chinese routes.
