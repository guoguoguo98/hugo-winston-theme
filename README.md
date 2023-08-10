# Hugo Winston 主题

Hugo Winston 是一个大胆的简约博客主题。

[在线演示](https://hugo-winston.netlify.app/) |
[Zerostatic 主题](https://www.zerostatic.io/)

![Hugo Winston 主题截图](https://www.zerostatic.io/theme/hugo-winston/hugo-winston-screenshot.png)

## 主题特点

- 文章（Markdown格式）
- 基础页面（Markdown格式）
- SCSS（Hugo Pipelines）
- 响应式设计
- 100/100 Google Lighthouse 速度评分
- 100/100 Google Lighthouse SEO评分
- 100/100 Google Lighthouse 可访问性评分
- 在 `config.toml` 中配置的 Google 分析
- 使用环境变量 HUGO_GOOGLE_ANALYTICS_ID 配置 GID，与 Netlify 兼容。
- 每个页面自动生成的标题、元描述和元标签
- 适用于 Facebook 和 Twitter 的 OG 元数据
- 语义化的 HTML 文档结构

## 安装

**1. 安装 Hugo**

要使用此主题，首先需要安装 Hugo。请按照官方[安装指南](https://gohugo.io/getting-started/installing/)

> ⚠️ **注意:** 检查您的 Hugo 版本 - 需要 **Hugo Extended** 版本！

此主题使用 [Hugo Pipes](https://gohugo.io/hugo-pipes/scss-sass/) 来编译 SCSS 和压缩资源，这意味着如果您没有使用 Hugo extended 版本，此主题将无法工作。要检查您的 Hugo 版本，请运行 `hugo version`。确保您看到版本号后的 **/extended**，例如 _Hugo Static Site Generator v0.51/extended darwin/amd64 BuildDate: unknown_。您不需要特定使用版本 v0.51，只需要有 _/extended_ 部分。

**2. 创建一个新的 Hugo 网站**

这将在文件夹 `mynewsite` 中创建一个全新的 Hugo 网站。

```
hugo new site mynewsite
```

**3. 安装主题**

下载或 git 克隆此主题到网站的主题文件夹 `mynewsite/themes`。您应该得到以下文件夹结构 `mynewsite/themes/hugo-winston-theme`

```
cd mynewsite
git clone https://github.com/guoguoguo98/hugo-winston-theme.git themes/hugo-winston-theme
```

**4. 复制示例内容**

将 `mynewsite/themes/hugo-winston-theme/exampleSite/` 文件夹的所有内容复制到您的 Hugo 网站的根文件夹，即 `mynewsite/`。要使用终端复制文件，请确保您仍在项目的根目录，即 `mynewsite` 文件夹。

```
cp -a themes/hugo-winston-theme/exampleSite/. .
```

**6. 运行 Hugo**

首次安装主题后，生成 Hugo 网站。

从您的 Hugo 网站的根文件夹运行此命令，即 `mynewsite`

```
hugo
```

对于本地开发，运行 Hugo 的内置本地服务器。

```
hugo server
```

现在在浏览器的地址栏中输入 [`localhost:1313`](http://localhost:1313)。

# 配置

### 配置选项

```toml
# hugo.toml
[params]
  google_analytics_id = ""
  twitter_handle = "@zerostaticio"
  showAuthorOnHomepage = true
  showAuthorOnPosts = false
  showIntroContentOnHomepage = true
  showPostsOnHomepage = true
  usePaginationOnHomepage = false
  limitPostsOnHomepage = 3 # 只在 usePaginationOnHomepage 为 false 时使用
  sortPostsByDateOldestFirst = false
  addDot = true
  addFrame = true
  highlightColor = '#7b16ff'
  baseColor = "#ffffff"
  baseOffsetColor = "#eaeaea"
  headingColor = "#1c1b1d"
  textColor = "#4e5157"
  dotColor = "#7b16ff"
  enableGoogleFonts = true
  googleFontsUrl = "https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap"
  fontFamilyHeading = "Poppins"
  fontFamilyParagraph = "Helvetica"
  fontFamilyMonospace = "monospace"
```

### Google 分析

在 `hugo.toml` 中添加您的 google 分析 ID。

```toml
# hugo.toml
[params]
  google_analytics_id="UA-132398315-1"
```

### Plausible 分析

在 `config.toml` 中添加您的 plausible 分析域。这是您的[跟踪脚本代码](https://plausible.io/docs/plausible-script)中的 `data-domain`。

```toml
# config.toml
[params]
  plausible_analytics_domain = "example.com"
```