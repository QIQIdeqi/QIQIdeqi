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

[阅读 UE02 完整教程](https://zhuanlan.zhihu.com/p/2095285265053004093)

### 梳理过场审核与交接｜过场制作实践 01

适合在整理过场材料、版本、审核意见与进度的同学。从一次审核和一次交接入手，梳理材料、负责人和最新状态。

自查：任选一条审核意见，能否同时写出对应 Sequence、材料版本、处理人和下一步？

[阅读过场制作实践 01](https://zhuanlan.zhihu.com/p/2094879283684578260)

[打开完整系列导读](https://zhuanlan.zhihu.com/p/2095704359396971810)

---

**English** · The [TA05 illustrated guide](https://qiqideqi.github.io/ta05-niagara-gpu-timing-companion/measurement-notes.html) walks through a measured Unreal Engine Niagara timing comparison. It includes the capture conditions, raw data and a reading exercise.
