# 77 的技术美术实战

把 UE 制作中的问题、工具与流程讲清楚。面向游戏美术、技术美术和独立开发者，用真实工程和对照实验讲操作步骤、判断依据与适用边界。

## 从手头的任务开始

### 排查 Niagara 性能｜TA 实践手记 05

适合在排查粒子覆盖、透明阶段或 GPU 耗时的同学。先读两个尺寸条件下的三个采样窗口，再比较透明阶段与整帧 GPU 的读数。

自查：保持 88 个粒子和相同材质，只改尺寸时，哪些读数变化？这些读数能支持什么结论？

[打开在线读数练习](https://qiqideqi.github.io/ta05-niagara-gpu-timing-companion/#reading-exercise) · [下载离线伴读与原始数据](https://github.com/QIQIdeqi/ta05-niagara-gpu-timing-companion/releases/tag/v1.0.4)

### 做 UE 编辑器批量工具｜UE 工具蓝图实战 02

适合已经会用基础蓝图，正在做批量重命名或资产编辑工具的同学。先走一遍预览、重名检查和执行前复检。

自查：先生成改名预览，再改动一条资源或让目标名称被占用。旧预览还能直接执行吗？

<details>
<summary>用两条资源做一次预览复检</summary>

先用两个演示资源生成改名预览。保持命名规则不变，在内容浏览器中把其中一个目标名称占掉。返回工具执行前重新检查该目标。预期结果是冲突项被拦住，界面显示原因；解除占用并重新预览后再执行。记录预览行、最终资源名及跳过原因。

</details>

[阅读 UE02 完整教程](https://zhuanlan.zhihu.com/p/2095285265053004093) · [只读预览练习与反馈](https://zhuanlan.zhihu.com/p/2095979973278437632)

### 梳理过场审核与交接｜过场制作实践 01

适合在整理过场材料、版本、审核意见与进度的同学。从一次审核和一次交接入手，梳理材料、负责人和最新状态。

自查：任选一条审核意见，能否同时写出对应 Sequence、材料版本、处理人和下一步？

<details>
<summary>用两条审核意见练一次交接</summary>

下面是教学例子。先写下参考版本、修改范围、当前状态和接手人下一步，再展开核对。

| 审核记录 | 交接时怎么处理 |
|---|---|
| SH010 的交付文件是 v002，参考 v001。按 24 fps 对照第 48–71 帧，帧区间两端都包含。 | 标为「待验收」。接收方先对照 v001 / v002 的同一段，并记录结果。第 60 帧对应 00:00:02:12，本例从第 0 帧计。 |
| 只收到「再柔一点」，没有参考版本、帧率、区间或预期变化。 | 标为「待澄清」。先补齐条件，再安排修改或验收。 |

</details>

[阅读过场制作实践 01](https://zhuanlan.zhihu.com/p/2094879283684578260) · [阅读 02：审核意见与交接](https://zhuanlan.zhihu.com/p/2096324332645507394)

[打开完整系列导读](https://zhuanlan.zhihu.com/p/2095704359396971810)

---

**English** · The [TA05 illustrated guide](https://qiqideqi.github.io/ta05-niagara-gpu-timing-companion/measurement-notes.html) walks through a measured Unreal Engine Niagara timing comparison. It includes the capture conditions, raw data and a reading exercise.
