## 更新 (v2.3.3)

- 添加：云端自更新升级为点击「立即更新」一键自动下载并安装 VSIX，带实时进度条、可取消操作与安装后一键重载窗口；严格校验 ZIP 文件头、大小与 SHA-256，校验通过才自动安装
- 优化：云端更新下载与清单检测同时兼容本地直连网络（自动切换 jsDelivr CDN 与国内 GitHub 加速镜像）以及代理网络（`vwdevin.proxy` / `http.proxy` / 环境变量 / Windows 系统代理，自动代理拒连时回退直连）
- 修复：更新清单 `raw.githubusercontent.com/.../refs/heads/main/...` 转换为 jsDelivr 地址时路径拼错导致回退失效的问题

## 更新 (v2.3.2)

- 添加：双模式安全接续桥接（`vwdevin.bridgeMode` 默认未选择），支持「官网原生桥接（免 cloudflared · Local Hands + 本机 MCP）」与「传统隧道桥接（Cloudflare / localhost.run）」二选一，支持互斥切换、一键启停与换号后一键续接
- 添加：侧边栏内嵌「本源观照」与「破甲 · 提示词/技能库」卡片，支持原生「☁ 云端直发」（复用插件账号与代理，无需外置服务）、Devin Local 官方生命周期 hooks 注入开关，以及进程级隔离终端会话池命令
- 添加：Windows 系统代理自动识别与代理隧道支持（代理留空时自动跟随系统代理或本机直连）
- 优化：ACP 配置支持 `windsurf.acp.*` 与 `devin.acp.*` 双命名空间独立合并写入，适配新版 Devin Desktop
- 优化：更新插件图标，隐藏高级 GitHub 折叠卡并合并侧边栏视图消除底栏留白
- 修复：部分网络环境下邮箱直登 `windsurf.com` 偶发 `ETIMEDOUT` 连接超时的问题

## 更新 (v2.2.7)

- 添加：插件云端自更新——推送 `v*` tag 由 GitHub Actions 自动打包正式 vsix 并发布到公开分发仓 [devin-qiehao-update](https://github.com/libai6666/devin-qiehao-update)；IDE 启动/重载窗口后自动检测新版本并提示（仅提示，手动下载），面板顶部新增「检查更新」入口，命令面板可执行 `Devin\windsurf 云端切号: 检查更新`
- 添加：`vwdevin.updateAutoCheck` 配置项，可关闭启动自检

**完整更新日志:** [v2.3.3](https://github.com/libai6666/devin-qiehao/releases/tag/v2.3.3)
