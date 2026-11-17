# devin-qiehao-update

`devin-qiehao`（云端切号 VSCode 插件）的公开更新分发仓。

- 每次源码仓推送 `v*` tag，GitHub Actions 自动把 `.vsix` 发布到本仓 Releases
- 根目录 `version.json` 是客户端更新检查拉取的静态清单（不走 api.github.com）
- 根目录 `CHANGELOG.md` 同步自源码仓，供插件内「查看更新日志」使用

> 本仓由 CI 维护，请勿手工提交。
