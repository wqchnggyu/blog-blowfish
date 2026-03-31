# 项目长期记忆

## Hugo Blowfish 博客配置（newSite 项目）

- **主题**：blowfish，中文语言（zh-cn），defaultAppearance = "dark"（强制深色，autoSwitchAppearance = false 不跟随系统）
- **博主名**：Wqchnggyu，**标题**：Wqchnggyu's blogs
- **baseURL**：https://blogs.wqch.net/（自定义域名，static/CNAME 已配置）
- **背景图**：assets/background.webp（165KB，background_hu_53eef77c6a909fb9）
- **头像**：assets/avatar.jpg
- **自定义字体**：assets/css/custom.css 引用 static/LXGWNeoZhiSongPlus.ttf（霞鹜新晰黑 Plus），设为全局默认字体
- **社交链接**：在 `config/_default/languages.zh-cn.toml` 的 `[params.author] links` 数组中配置（Bilibili/GitHub/GitLab），`params.toml` 的 `[[footer.social]]` 无效（主题无对应模板）
- **社交图标**：assets/icons/bilibili.svg（Simple Icons 风格，主题无内置需自定义）
- **ICP备案预留**：params.toml 的 icp 字段；background.html 底部显示
- **unsafe HTML 渲染**：hugo.toml 中已开启 markup.goldmark.renderer.unsafe = true
- **评论系统**：Waline（serverURL: https://comment-waline.wqch.net/），服务端 v1.39.3，前端使用 @waline/client@v3，通过 layouts/partials/comments.html 集成，dark: 'html.dark' 自动跟随深浅色，含微博/bilibili 表情包，login: 'force' 强制登录，comment: true，pageview: true，params.toml 开启 showComments = true
- **访问量统计**：Waline pageview，通过 layouts/partials/extend-footer.html 全站加载（每页都执行），article.showViews = true + 覆盖 layouts/partials/meta/views.html 用 waline-pageview-count class；footer 总访问量显示已移除
- **站点分析**：Umami Analytics，通过 params.toml [umamiAnalytics] 配置，domain: umami.wqch.net，websiteid: e30a6109-4267-499c-b243-34d79e7fd0a1
- **GitHub Pages 部署**：.github/workflows/hugo.yaml（触发分支 main，Hugo v0.157.0，baseURL 由 Actions 动态注入）
- **主题管理方式**：git submodule，指向官方 `https://github.com/nunocoracao/blowfish.git`（非 fork），checkout 时需 `submodules: true`
- **go.mod**：仅保留 module 声明和 `go 1.21`，无需 hugo mod 依赖（主题通过 submodule 管理）
- **配置文件**：config/_default/{params.toml, languages.zh-cn.toml, menus.zh-cn.toml}
- **现有文章**：
  - content/posts/h3c-learningspace-crack/（H3C 学习空间破解，来自 B站文章）
  - content/posts/markdown-guide/（Markdown 语法教程，来自 astro-pure.js.org）
  - content/posts/nianwei/（年味，来自 blog.liushen.fun）
