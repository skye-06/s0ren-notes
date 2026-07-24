# S0ren 学习知识库

基于 [Quartz v5](https://quartz.jzhao.xyz/) 的纯静态 Markdown 知识库，用于整理测绘、导航与空间智能方向的学习笔记。站点保留 Quartz 官方搜索、Explorer、目录、内部链接、暗色模式、代码高亮、KaTeX 与表格能力，不包含分析、评论、加密页面、登录或后端服务。

## 本地运行

需要 Node.js 22 和 npm。

```bash
npm ci
npx quartz plugin install
npx quartz build --serve
```

浏览器访问终端显示的本地地址。仅构建静态文件：

```bash
npx quartz build
```

构建结果位于 `public/`。

## 内容维护

- 根入口：`content/index.md`
- 分类笔记：在 `content/` 的对应目录中新建 Markdown 文件
- 本地图片：建议放在 `content/assets/`
- 站点标题、域名与个人主页入口：编辑 `quartz.config.yaml`

Markdown 文件会在构建时自动生成页面；可使用公式、表格、代码块、图片、普通链接和 `[[内部链接]]`。

## EdgeOne Makers

从 GitHub 导入本仓库，生产分支选 `v5`。仓库中的 `edgeone.json` 已配置：

- Node.js：`22.17.1`（Makers 预装且满足 Quartz v5 当前锁定依赖要求）
- 安装命令：`npm install --global npm@10.9.2 && npm ci`
- 构建命令：`npx quartz plugin install && npx quartz build`
- 输出目录：`public`

当前公开域名为 `https://notes.aisoren.top/`，`baseUrl` 和 Footer 的“个人主页”
地址均使用正式自定义域名。

## 许可

上游 Quartz 使用 MIT License，本仓库保留其许可证与署名。
