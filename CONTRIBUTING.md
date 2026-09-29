# 贡献指南 / Contributing Guide

感谢你愿意为 Scintela 贡献!社区的贡献主要有三类:基准数据、教程、翻译。
Thanks for contributing! There are three main ways: benchmark data, tutorials, and translations.

## 1. 贡献基准数据(最需要!)/ Benchmark data (most needed!)

在 [`Scintela/matrix`](https://github.com/Scintela/matrix) 仓库:

1. Fork 仓库,在 `bench/` 下按 `bench/<硬件>-<模型>-<你的ID>/` 建目录,记录:
   - 硬件与环境快照:板卡型号与固件、runtime 及版本、量化工具版本、室温
   - 完整的运行命令
   - 原始输出(日志或截图)
2. 把结果加一行到 `data/matrix.csv`(字段定义见 `data/schema.md`)
3. 提交 PR,标题格式:`data: <hardware>/<model>`

**冷启动期门槛从宽**:暂不强制一键复现脚本,但环境与命令必须写清。数据被合并后,矩阵页面将**永久署名**;后续有人按你的环境复现成功,该行会升级为「已验证 ✓」。

During cold start we keep the bar low: a one-click repro script is not yet mandatory, but environment and commands must be complete. Merged rows are **permanently credited**; rows independently reproduced by others are upgraded to "Verified ✓".

## 2. 贡献教程 / Tutorials

我们想要的是端到端、真踩坑、可照做的教程,而不是营销稿。欢迎先开 Issue 或写信到 hello@scintela.dev 讨论选题。

We want end-to-end, warts-and-all, follow-along tutorials — not marketing posts. Open an issue or write to hello@scintela.dev to discuss topics first.

## 3. 贡献翻译 / Translations

中文是内容源头,英文翻译在 `/en/` 目录同步,翻译 PR 一律欢迎。
Chinese is the source of truth; English lives under `/en/`. Translation PRs are always welcome.

## 通用规则 / Ground rules

- 提 PR 前请阅读[行为准则](./CODE_OF_CONDUCT.md) / Please read the [Code of Conduct](./CODE_OF_CONDUCT.md) first.
- 引用他人数据须注明出处;使用他人模型请确认其许可证允许你的用途 / Cite sources; make sure model licenses permit your use.
- 不接受无来源的跑分数据(厂商宣传页数据不收,除非可独立复现)/ Unsourced benchmark numbers are not accepted (vendor marketing slides don't count unless independently reproducible).
