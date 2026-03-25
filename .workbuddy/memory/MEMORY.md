# 项目长期记忆

## Hugo Blowfish 博客配置（newSite 项目）

- **主题**：blowfish，中文语言（zh-cn）
- **博主名**：Wqchnggyu，**标题**：Wqchnggyu's blogs
- **baseURL**：https://wqchnggyu.github.io/（GitHub Pages 部署地址）
- **背景图**：assets/background.webp（165KB，background_hu_53eef77c6a909fb9）
- **头像**：assets/avatar.jpg
- **自定义字体**：assets/css/custom.css 引用 static/LXGWNeoZhiSongPlus.ttf（霞鹜新晰黑 Plus），设为全局默认字体
- **社交图标**：assets/icons/bilibili.svg（Simple Icons 风格），GitHub/GitLab 图标由 Blowfish 内置提供
- **社交链接**：params.toml 的 [[footer.social]]，Bilibili/GitHub/GitLab 三个链接
- **ICP备案预留**：params.toml 的 icp 字段；background.html 底部显示
- **unsafe HTML 渲染**：hugo.toml 中已开启 markup.goldmark.renderer.unsafe = true
- **评论系统**：Giscus（repo: wqchnggyu/Comments），通过 layouts/partials/comments.html 集成，支持深浅色自动切换，params.toml 开启 showComments = true
- **GitHub Pages 部署**：.github/workflows/hugo.yaml（触发分支 master，Hugo v0.157.0，baseURL 由 Actions 动态注入）
- **配置文件**：config/_default/{params.toml, languages.zh-cn.toml, menus.zh-cn.toml}
- **现有文章**：
  - content/posts/h3c-learningspace-crack/（H3C 学习空间破解，来自 B站文章）
  - content/posts/markdown-guide/（Markdown 语法教程，来自 astro-pure.js.org）
  - content/posts/nianwei/（年味，来自 blog.liushen.fun）
