# Claude Code 控制面

作者：GitHub 账号 monadrome。仓库名为 `cc-sourcebook`，公开链接预定为 https://monadrome.github.io/cc-sourcebook/ 。目前只准备本地产物，尚未发布。

## 信源与法律状态

源码于 2026-03-31 经 npm 包 sourcemap 意外公开。本书从该事件的备份树独立取证，不借用其他源码分析。公开版用以下镜像核对完整原文，commit 固定到 40 位，不以浮动 HEAD 为准。

首选镜像：https://github.com/Usamaliaquat123/Claude-Code-Source ，commit：`9955b25de0ca3ad6ff97757045006143de73db73`。其路径布局与本书引注一致，源码页固定在 https://github.com/Usamaliaquat123/Claude-Code-Source/tree/9955b25de0ca3ad6ff97757045006143de73db73 。负责人已抽验 8/8 行号命中，并确认完整 hash。

备选镜像：https://github.com/sleeplessai/claude-code-leaked-source ，commit：`5a774a2b62d7949c1d94e0b726281554d7893cfd`。核对时必须在书中相对路径前加 `src/`，固定源码页为 https://github.com/sleeplessai/claude-code-leaked-source/tree/5a774a2b62d7949c1d94e0b726281554d7893cfd 。负责人同样抽验了 8/8 行号。

原 kuberwastaken/claude-code 已改名 Kuberwastaken/claurst，当前 HEAD 是 Rust 项目，已无这份原始 TS 源码，不能用其当前 hash 代替本书信源。以上镜像验证用于钉版，不用于借鉴分析内容。

本书是独立的技术研究与评论，分析为原创内容；公开版仅保留支撑评论所需的最小引文，其余原文由路径、行号与固定镜像索引。引文版权归原作者所有，本书不主张对引文的任何权利。

本书描述该快照的静态代码行为，不代表当前发行产品行为。构建特性和远端开关的存在不证明它们在任何发行版启用；构建宏不能确定这份源码的产品版本号（`constants/system.ts:73-95`）。

本书未获得原厂商授权，不声称与其存在隶属或背书关系。勘误与联系渠道：[Issues](https://github.com/monadrome/cc-sourcebook/issues)。Issues 是本书的勘误与联系入口，作者为 monadrome；没有另列邮箱。

## 阅读约定

公开版保留中文分析、完整源码区间与承重短引。保留行逐字来自原文，英文、标点、空白及内部标识不改写。`// … 省略 N 行（path:Lx-Ly）` 是本书新增的省略标记，说明省去的精确范围；最多两处。保留行与标记顺序合起来覆盖标题的整个区间，标记不算源码行。

只作存在性旁证的块换成 `（原文见 path:La-Lb，共 N 行，略）`。需要完整上下文时，按首选镜像的固定 commit 加路径与行号核对；使用备选时加 `src/`。镜像若失效，应在此标明核验链中断并暂停引流，不恢复大段转载。

源码事实由附近的路径行号支持；【作者推断】明确标出解释。源码注释里的效果、原因和实验记录按注释归属，不当成本次实测。逐字专有引文仍未获授权，缩小体量不等于已取得引用权，也不提供法律结论。

## 本地产物

`python3 build.py` 生成完整版 `site/`；`python3 build.py --public` 生成公开版 `site-public/`。构建只用 Python 3 标准库，页面无 CDN、外部字体或运行时网络依赖，直接打开 `index.html` 即可离线阅读。

唯一可发布目录为 `site-public/`。它只包含阅读 HTML、本地 CSS、本 README 和 `.nojekyll`；不包含取证库、源码备份、完整版书稿或构建工具。本地研究仓库不能整体公开。当前任务不创建公开仓库、不推送、不启用 Pages。
