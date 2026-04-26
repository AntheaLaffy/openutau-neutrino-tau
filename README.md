# Neutrino Tau for TuneLab

> 其他语言版本：[日本語](README_ja.md)

> [!WARNING]
> 本项目是为了赶上 ボカコレ 截止日期而仓促完成的，代码较为粗糙，无法保证正常运行。仅供参考。

Neutrino Tau for TuneLab 是一个用于在 [TuneLab](https://github.com/LiuYunPlayer/TuneLab) 中使用 Neutrino 的插件。

## 安装

1. 下载并安装 [Neutrino](https://studio-neutrino.com/)（**含调声辅助工具版本**）的最新版本。
2. 下载并安装 [TuneLab](https://github.com/LiuYunPlayer/TuneLab) 的最新版本。
3. 从 [Releases](https://github.com/sevenc-nanashi/tunelab-neutrino-tau/releases) 下载最新的 `tunelab-neutrino-tau-x.x.x.tlx`。
4. 在 `Extensions` 中选择 `Install/Update...`，然后选择下载的 `.tlx` 文件进行安装。

## 部分属性

### `styleShift`

- 类型: number（整数）
- 默认值: `0`
- 范围: `-24` ～ `24`（半音）
- 若指定为小数，将四舍五入处理。

`styleShift` 是在内部推理时以半音为单位移动音符、改变音色倾向的参数。  
该参数应用于音调推理，同时也反映在最终波形合成的基准调上。

### `waveformStyleShift`

- 类型: number（整数）
- 默认值: `0`
- 范围: `-24` ～ `24`（半音）
- 若指定为小数，将四舍五入处理。

`waveformStyleShift` 是仅在最终波形合成阶段额外应用的半音偏移。  
可在 `styleShift` 的基础上，单独在波形阶段进一步调整偏移量。

### `pitchShiftCents`

- 类型: number
- 默认值: `0`
- 范围: `-2400` ～ `2400`（音分）

`pitchShiftCents` 是以音分（cent）为单位应用于最终 F0 的音调偏移。  
与 `styleShift` / `waveformStyleShift` 相互独立，可用于更精细的音调微调。
