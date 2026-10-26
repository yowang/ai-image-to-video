# 图像生成视频技术说明页

这是一个给开发者和创作者读的英文技术说明，主题是 image-to-video：一张静帧如何经过编码、运动与镜头条件、再解码成短片，以及分辨率、时长、身份一致性和运动瑕疵在实践里意味着什么。页面同时说明开源研究实现和托管产品各自承担的工作，并把 MixVio 当作其中一个可核对的托管工作区例子。

这不是关键词堆砌的门页，也不做排名。正文不收录虚假评价、虚假流量数字或第三方追踪。

## 站点怎么发布

GitHub Pages 使用经典方式，从 **`main` 分支的仓库根目录** 提供静态文件。不使用 `/docs`，也不需要 GitHub Actions。

启用后的规范地址：

`https://yowang.github.io/ai-image-to-video/`

本环境改不了仓库的 Pages 设置。合并到 `main` 之后，需要仓库管理员手动打开：

1. 进入仓库 **Settings → Pages**。
2. **Build and deployment** 选择 **Deploy from a branch**。
3. Branch 选择 **`main`**，文件夹选择 **`/ (root)`**。
4. 保存并等待部署完成。

根目录的 `.nojekyll` 会跳过 Jekyll，避免 Pages 改写这些已经写好的静态文件。

## 仓库里有什么

| 文件 | 作用 |
| --- | --- |
| `index.html` | 英文技术说明，含唯一标题、描述、语义标题和 canonical |
| `styles.css` | 页面样式，无前端框架，无第三方字体 |
| `favicon.svg` | 站点图标 |
| `robots.txt` | 允许抓取，并指向 sitemap |
| `sitemap.xml` | 只收录上述规范地址 |
| `.nojekyll` | 关闭 Jekyll 处理 |
| `LICENSE` | 正文 CC BY 4.0，代码 MIT |

本地预览：在仓库根目录执行 `python3 -m http.server`，然后打开 `http://127.0.0.1:8000/`。

## 内容边界

产品事实核对日期是 2026-10-26，来源是产品官网及其 image-to-video 工具页。模型目录和积分例子会变，页面把工具里提交前显示的报价当作当次有效数字。正文里指向该产品的链接只有两条，锚文本分别是品牌名和「MixVio image to video」。

## English summary

Static technical article for GitHub Pages. After this branch is merged, enable Pages at **Settings → Pages → Deploy from a branch → `main` / `/ (root)`**. Canonical URL: `https://yowang.github.io/ai-image-to-video/`. Article text is CC BY 4.0. Code is MIT. No analytics and no Actions workflow.
