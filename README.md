# Claude Code 源码思想解读

本书从 Claude Code 源码解释系统提示词怎样装配，工具描述怎样约束调用，权限怎样判定，上下文怎样压缩与记忆。全书 16 章，面向熟悉软件工程的读者。

在线阅读：[monadrome.github.io/cc-sourcebook](https://monadrome.github.io/cc-sourcebook/)。离线阅读：下载公开版后打开 `index.html`，无需联网。

## 阅读约定

论述附源码路径与行号，【作者推断】另作标记。引文保留英文原文；省略标记注明省去的行号，完整上下文可到下列固定镜像核对。源码注释中的实验结果按注释引用，不当作本书实测。

## 信源与法律状态

信源是 2026-03-31 经 npm sourcemap 意外公开的源码快照，不代表当前发行产品行为。代码中的特性开关或实验分支也不意味着已经发布。

首选：[Usamaliaquat123/Claude-Code-Source](https://github.com/Usamaliaquat123/Claude-Code-Source/tree/9955b25de0ca3ad6ff97757045006143de73db73)，路径与书中引注一致。固定提交：`9955b25de0ca3ad6ff97757045006143de73db73`。

备选：[sleeplessai/claude-code-leaked-source](https://github.com/sleeplessai/claude-code-leaked-source/tree/5a774a2b62d7949c1d94e0b726281554d7893cfd)，核对时在书中路径前加 `src/`。固定提交：`5a774a2b62d7949c1d94e0b726281554d7893cfd`。

本书是独立的技术研究与评论，分析为原创内容，仅保留佐证所需的最小引文。引文版权归原作者，本书不主张对引文的任何权利；未获得原厂商授权，也不代表其立场。

作者：monadrome。勘误与联系渠道：[Issues](https://github.com/monadrome/cc-sourcebook/issues)。
