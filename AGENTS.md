# GitHub Profile — 工程指令

本仓库 `seiya058904/seiya058904` 提供个人 GitHub Profile。`README.md` 是展示入口，`assets/` 保存已引用的 SVG/WebP 项目图片；它不是个人主页网站仓库。没有 `package.json`、应用构建或 npm 测试命令，不要为文档维护添加工具链。

## 验证与交付

- 改动前读取 README 和相关资源/链接，保留作者身份、文案及既有项目展示。
- 文档改动检查本地相对路径存在、Markdown/HTML 图片与链接及 `git diff --check`；按需检查 GitHub 的实际渲染，不把本地文本检查当作浏览器验收。
- 完成前检查 `git status --short`、限定范围 diff 和 staged 文件，只提交本任务拥有的内容。
- `main` 是正式源码分支。`.github/workflows/snake.yml` 每周定时或手动生成贡献活动 SVG，写入独立的 `output` 分支；README 从该分支读取图片。`output` 是部署生成用途，必须保留，不能按过时分支删除。
- 普通文档维护不需要运行生成工作流；不要把写入 `output` 的任务当作只读 CI 检查。本仓库目前没有 PR 验证工作流。

## 安全与边界

保留原始图片、Git 历史和用户未提交内容，不做全仓格式化、历史重写或强制推送。不要提交凭据、缓存、临时截图或 `.workbuddy/`，也不要删除用户项目数据。提交、推送、合并、工作流触发和其它外部写入必须有明确任务授权；对仓库链接所指向的其它项目，不因修改 Profile 而自动开展维护。

## Browser tool selection

- Prefer Ego Browser for exploratory navigation, visual review and interactive checks when available. Use Playwright for repeatable regression, CI, isolation, request interception or other automation requiring its APIs; combine tools when useful. If Ego is unavailable, use a suitable existing browser tool.
- Keep this repository's required browser commands, versions, profiles and safety boundaries; an exploratory check does not replace required automated tests. Do not alter real user data or production state for testing. Report the tools, coverage and any untested paths.
