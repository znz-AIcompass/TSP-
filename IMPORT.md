# 上游源码导入说明

`tick-stock-panel/` 是官方仓库 [shy3130/tick-stock-panel](https://github.com/shy3130/tick-stock-panel) 标签 **v0.3.37** 的完整 Git 树，内容未改。

| 项目 | 值 |
| --- | --- |
| 标签 | `v0.3.37` |
| 附注标签对象 | `40a967d50aca42de76fb163207fd1ee5b3c3fb9f` |
| 对应提交 | `f9cb383c5918c6a88a412f3ce43d59fe81b94ccc` |
| 提交说明 | `chore(release): prepare v0.3.37` |
| 发布状态 | 正式版（非 draft、非 prerelease），发布于 2026-11-12 |
| 许可证 | MIT，版权 2026 tick-stock-panel contributors |
| 可追溯历史 | 导入提交的第二父提交就是上述上游提交，其祖先历史一并保留 |

根目录已有用户文件 `README.md`（内容为 `# TSP-`）。该路径与上游 `README.md` 冲突，因此没有覆盖或删除它。完整源码放在 `tick-stock-panel/`，其中的 `README.md`、`LICENSE` 与其余文件均保持上游原样。根目录 `LICENSE` 是同一份 MIT 许可证的副本，便于识别许可，不是上游文件的修改。

上游工作流仍位于 `tick-stock-panel/.github/workflows/`，没有放到仓库根的 `.github/workflows/`，因此本次推送和拉取请求不会启用 CI、镜像发布或桌面安装包发布。这些工作流在上游的触发方式是：

- `ci.yml`、`dco.yml`：对 `main` 的 push 或 pull request 会安装依赖并运行检查
- `docker.yml`：对 `main` 的 push、`v*` 标签或手动运行会构建并推送容器镜像
- `release.yml`：仅手动运行，会构建桌面安装包并创建 GitHub Release

请不要把上述工作流移动到仓库根目录，也不要推送 `v*` 标签，除非另行确认。本次没有下载官方桌面安装包，没有安装依赖，没有运行应用，也没有加入密钥或交易账户。
