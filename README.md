# ChisFlash-MBCX

> 一块面向 Game Boy / Game Boy Color 的单卡方案。通过烧录不同的 CPLD 固件，可在 `MBC3 RTC` 与 `MBC5 震动` 两种模式之间切换。

简体中文 | [English](README_EN.md)

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](LICENSE)
![Platform: GB/GBC](https://img.shields.io/badge/Platform-GB%20%2F%20GBC-4f8bff.svg)
[![Open Source Hardware](https://img.shields.io/badge/OSHWHub-Project-orange.svg)](https://oshwhub.com/morinaka/chisflash-cqz)

![ChisFlash_MBCX](picture/ChisFlash_MBCX.png)

## 项目简介

`ChisFlash-MBCX` 是 ChisFlash 系列中的单卡项目，主要用于实现：

- `MBC3 RTC` 时钟单卡
- `MBC5` 震动单卡

项目由 `兜鬼巨神兵（CQZ）` 开发，由 `mori` 代为整理与发布。根据仓库现有说明，这块板通过刷写不同的固件即可在两种用途之间切换；其中 RTC 版本对 MBC3 时钟寄存器做了还原，并通过了 RTC 相关测试。

## 项目亮点

- 一套 PCB，支持两种常用方案切换
- 提供 `Gerber`、`PCB 工程`、`CPLD 固件` 与 `MCU 固件`
- 适合复古游戏卡带爱好者自制、研究与二次开发
- 提供嘉立创开源页面，便于查看焊接辅助与 BOM 信息

## 快速导航

- 嘉立创开源页面：[oshwhub.com/morinaka/chisflash-cqz](https://oshwhub.com/morinaka/chisflash-cqz)
- PCB 图片：[picture/ChisFlash_MBCX.png](picture/ChisFlash_MBCX.png)
- Gerber 文件：[gerber/Gerber_ChisFlash-MBCX-CQZ_2025-11-29.zip](gerber/Gerber_ChisFlash-MBCX-CQZ_2025-11-29.zip)
- PCB 工程：[pcb/ProDoc_ChisFlash-MBCX-CQZ_2025-11-29.epro](pcb/ProDoc_ChisFlash-MBCX-CQZ_2025-11-29.epro)
- RTC 版 CPLD 固件：[pof/CPLD_ChisFlash_MBCX_RTC.pof](pof/CPLD_ChisFlash_MBCX_RTC.pof)
- 震动版 CPLD 固件：[pof/CPLD_ChisFlash_MBCX_Motor.pof](pof/CPLD_ChisFlash_MBCX_Motor.pof)
- RTC 版 MCU 固件：[mcu/MCU_ChisFlashRTC.hex](mcu/MCU_ChisFlashRTC.hex)

## 仓库结构

| 路径 | 内容 |
| --- | --- |
| `gerber/` | 生产用 Gerber 压缩包 |
| `pcb/` | PCB 原始工程文件 |
| `pof/` | CPLD 固件，分别对应 RTC / 震动版本 |
| `mcu/` | RTC 版本使用的 MCU 固件 |
| `picture/` | 项目图片与展示素材 |

## 模式说明

| 模式 | 对应文件 | 是否需要 MCU / 时钟芯片 | 说明 |
| --- | --- | --- | --- |
| `MBC3 RTC` 时钟单卡 | `pof/CPLD_ChisFlash_MBCX_RTC.pof` + `mcu/MCU_ChisFlashRTC.hex` | 需要 | 用于 RTC 功能卡带 |
| `MBC5` 震动单卡 | `pof/CPLD_ChisFlash_MBCX_Motor.pof` | 不需要 | 可不焊 MCU 和时钟芯片，以减少不必要耗电 |

## 自制流程

1. 按照嘉立创开源页面中的焊接辅助 / BOM 准备材料并完成焊接。
2. 烧录对应的 CPLD 固件，在 `RTC` 与 `震动` 两种模式中二选一。
3. 如果制作 RTC 版本，还需要焊接单片机与时钟芯片，并通过 `SWD` 或 `TTL` 烧录 MCU 固件。
4. 如果制作震动版本，可以不焊接单片机和时钟芯片，避免额外耗电。
5. 注意电池左下方的电阻需要焊接，否则电池不会供电。

> 建议使用插件晶振，温漂更小，时间精度更稳定。

## 2025-11-18 更新

- 新增一颗 `0Ω` 电阻，用于铁电改装
- 使用 `SRAM` 时，焊接 `0Ω`
- 使用铁电时，不焊接 `0Ω`，改为短接二极管和电阻焊盘

## 项目背景

<details>
<summary>点击展开项目缘起</summary>

这个项目最初的出发点很简单：想做一张真正适合 GBC 中文化《宝可梦 金 / 银》体验的时钟卡。

早年的一些盗版卡方案，可能会依赖 ROM 补丁，用步数代替 RTC；但在新的汉化 ROM 场景里，这种方式并不总是成立。于是，围绕 ChisFlash 这条已经逐渐成熟的路线，我们把 `MBC3 RTC` 这块拼图补了上去。

这也是 ChisFlash 系列自然延伸出来的一步。从最早的烧录器，到后来逐渐出现的时钟卡、震动卡、合卡以及更多复古社区的自制方案，这个项目更像是大家一起把一撮小火苗养成篝火的过程。

</details>

## 开源与授权

- 本项目开放 `PCB` 与固件下载，欢迎个人制作、学习研究和社区交流。
- 仓库当前附带许可证文件：[GPL-3.0](LICENSE)
- 根据原说明，个人卖家售卖时请保留以下鸣谢字样：

```text
感谢兜鬼巨神兵（CQZ）的开发并开源，感谢 chis 团队贡献。
```

- 如需商业化，请先联系 `兜鬼巨神兵（CQZ）` 获取授权。

## 社群与相关链接

- QQ 交流群：`771688226`
- 嘉立创开源页面：[oshwhub.com/morinaka/chisflash-cqz](https://oshwhub.com/morinaka/chisflash-cqz)
- CQZ Bilibili：[space.bilibili.com/371016269](https://space.bilibili.com/371016269)
- chisbread 作品页：[oshwhub.com/chisbread/works](https://oshwhub.com/chisbread/works)
- chisbread Bilibili：[space.bilibili.com/811896](https://space.bilibili.com/811896)
- mori 作品页：[oshwhub.com/morinaka/works](https://oshwhub.com/morinaka/works)
- mori Bilibili：[space.bilibili.com/1825944](https://space.bilibili.com/1825944)

## 鸣谢

- `兜鬼巨神兵（CQZ）`：项目开发与开源
- `林面包（chisbread）`：ChisFlash 相关协作与社区贡献
- `mori`：项目整理、代发与资料归档
