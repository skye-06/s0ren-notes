# S0ren 学习知识库

本项目是基于 Quartz v5 的纯静态 Markdown 知识库，生产分支为 `v5`。

## 运行与验证

- 环境：Node.js 22、npm 10.9.2+
- 安装：`npm ci`
- 安装已配置插件：`node quartz/bootstrap-cli.mjs plugin install`
- 构建：`node quartz/bootstrap-cli.mjs build`
- 本地预览：`node quartz/bootstrap-cli.mjs build --serve`

## 技术栈与结构

- Quartz v5、TypeScript、Preact
- `content/`：知识库正文与本地资源
- `quartz.config.yaml`：站点、主题、插件与布局配置
- `quartz.lock.json`：Quartz 插件锁文件
- `public/`：构建产物，不直接编辑

## 约定

- 内容修改优先落在 `content/`，不修改生成的 `public/`
- 插件通过 Quartz CLI 和配置文件管理，不手动复制插件实现
- 新增或移除插件后同步 `quartz.config.yaml`、`quartz.lock.json` 与 README
- 不自动提交、推送或发布；发布前必须完成静态构建
- 正式域名为 `https://notes.aisoren.top/`

## 当前状态

站点为无登录、无后端的静态知识库，由 EdgeOne Makers 构建部署。

下一步：内容或配置变更后先构建验证，再按用户要求通过内容编辑器发布。
