# Vim 命令速查表 · Vim Cheatsheet

[![Stars](https://img.shields.io/github/stars/Ezra-Zhao/vim-cheatsheet?style=social)](https://github.com/Ezra-Zhao/vim-cheatsheet/stargazers) [![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE) ![Languages](https://img.shields.io/badge/languages-3-blue)

> 🌍 [Español](README.es.md) · [Português](README.pt.md)

一份**一页纸**的 Vim 速查表：30 条真实可用的 Vim 用法——退出与保存、快速移动、操作符+文本对象、查找替换、可视模式、宏与寄存器。每个条目只讲三件事——**它是干什么的、一段能直接照着敲的键位、适用场景标签**。不编造命令：绝大多数条目都在本机 Vim 9.1（vim-tiny）里无头实测、核对过改后文件；tiny 版跑不了的少数条目（系统剪贴板、`:nohlsearch`、持久撤销、sudo 保存）按 Vim 的编译特性与官方行为注明核实方式。

## 面向谁

刚被 Vim"怎么退出都退不出去"劝退的新手，以及用了几年还只会 `i` 和 `:wq` 的老用户。如果查找替换、可视块编辑、宏这几件事总让你现查，这张表能让你一次记牢。

## 怎么用

1. 直接看 **[CHEATSHEET.md](CHEATSHEET.md)** ——速查表正文，英文说明全球开发者都无压力。
2. 本地要有 Vim：Linux / macOS 自带，Windows 用 WSL 或 gVim；随便拿一个文本文件就能练。
3. 按"退出保存 → 移动 → 编辑 → 查找替换 → 可视 → 宏"的顺序，每个条目亲手敲一遍，一小时就顺手了。

## 先跑起来（30 秒验证环境）

```bash
vim --version | head -1            # 打印版本（如 VIM - Vi IMproved 9.1），说明 Vim 在
vim --version | grep clipboard     # +clipboard 才有系统剪贴板（"+y），-clipboard 就是没有
vimtutor                           # 官方自带 30 分钟交互教程，练完这张表就全熟了
```

## 一份能直接用的 ~/.vimrc

```vim
set number relativenumber   " 行号：当前行绝对行号，周围相对行号（跳行时心里有数）
set expandtab shiftwidth=2  " Tab 换成空格，一级缩进 2 格
set ignorecase smartcase    " 搜索忽略大小写，但模式里带大写字母时自动敏感
set undofile                " 撤销历史存进文件，关掉 Vim 重开还能接着撤销
```

存进 `~/.vimrc` 后重新打开 Vim 就生效——行号、缩进、搜索手感一次到位。

## 收录了什么

| 分类 | 内容 |
|---|---|
| 🚪 退出与保存 | :w/:q/:wq 与 ZZ / :q! 与 ZQ / :x 与 :wq 的差别 / sudo 保存 / 在指定行或搜索处打开（5 条） |
| 🧭 移动 | hjkl 与 w b e（及 W B E）/ 0 ^ $ 与 gg G / f F t T 与 ; , / % 与 { } / Ctrl-d/u/f/b 与 H M L / gj gk 显示行（6 条） |
| ✏️ 编辑 | i a I A o O / x dd yy p P 与数字前缀 / u Ctrl-r 与 . / 操作符+移动 / 文本对象 / r ~ 与缩进 / J 与 :m（7 条） |
| 🔍 查找替换 | / ? n N 与 * # / :s 与 g c 旗标 / :%s 与区间替换 / 搜索设置与 :noh / :g 与 :v（5 条） |
| 👁 可视模式 | v V Ctrl-v 三种可视 / 块插入与块尾追加 / gv 与 o（3 条） |
| 🎙 宏与进阶 | 宏录制与回放（完整示例）/ 寄存器与系统剪贴板 / :! 与 :r ! / ~/.vimrc 生存设置（4 条） |

官方文档只链 https://www.vim.org/docs.php，所有命令均以 Vim 9.1 为准核实：能在本机 vim-tiny 里跑的全部无头实测过，tiny 版缺编译特性的条目（+clipboard、+persistent_undo、+extra_search）在正文里如实注明。

## 为什么是这 30 条

- **退出/保存排第一**：`:q!` 丢什么、`:x` 和 `:wq` 差在哪（无改动时不重写文件、不动 mtime），先讲清才敢放心用。
- **操作符+移动是语法**：学会 `d/c/y + 移动` 和文本对象，几百个组合自动解锁，不用逐条死记。
- **宏给完整示例**：录宏时把 `j` 一起录进去，回放自己会往下走——`qa` 录一次、`9@a` 刷完十行，这是宏真正省时间的地方。
- **危险动作先警告**：`:%s` 全文替换和 `:q!` 都标了 ⚠️，并给了 `c` 确认旗标和 `u` 撤销的退路。

## 欢迎 PR

发现命令写错了、说法过时了、翻译不到位——欢迎提 Pull Request。新增条目请保持统一格式（一句话说明 / 代码块 / 标签），**只收真实可用的命令，不确定的宁可不收**。

## 📚 更多速查表

同一作者的其他速查表，同样有中/西/葡三语版本：

- [FFmpeg 命令速查表](https://github.com/Ezra-Zhao/ffmpeg-cheatsheet) — 28 条音视频处理命令
- [Git 实战速查表](https://github.com/Ezra-Zhao/git-cheatsheet) — 30 条日常+救命命令
- [Docker 命令速查表](https://github.com/Ezra-Zhao/docker-cheatsheet) — 28 条容器命令
- [curl 命令速查表](https://github.com/Ezra-Zhao/curl-cheatsheet) — 29 条 API 调试命令
- [正则表达式速查表](https://github.com/Ezra-Zhao/regex-cheatsheet) — 30 条实战正则模式
- [jq 命令速查表](https://github.com/Ezra-Zhao/jq-cheatsheet) — 30 条 JSON 处理 filter
- [终端神器速查表](https://github.com/Ezra-Zhao/terminal-superpowers-cheatsheet) — 14 个终端效率工具
- [Adobe 免费替代速查表](https://github.com/Ezra-Zhao/adobe-free-alternatives-cheatsheet) — 16 个 Adobe 免费替代品
- [退订省钱速查表](https://github.com/Ezra-Zhao/desubscribe-cheatsheet) — 10 组退订替代，年省约 $1,260
- [kubectl 命令速查表](https://github.com/Ezra-Zhao/kubectl-cheatsheet) — Kubernetes 常用命令速查
- [SQL 查询速查表](https://github.com/Ezra-Zhao/sql-cheatsheet) — 常用 SQL 查询与函数速查
- [SSH 命令速查表](https://github.com/Ezra-Zhao/ssh-cheatsheet) — 28 条 SSH 连接、密钥与隧道命令

## License

MIT © 2026 Guangyi Zhao，详见 [LICENSE](LICENSE)。
