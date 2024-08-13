![logo](static/logo.svg)

# Astronaut

Astronaut 是一个简约、漂亮且功能丰富的 Hugo 博客主题。

> 该主题源自于 [Gabriele Musco](https://gabmus.org/) 的 [hugo-ficurinia](https://gitlab.com/gabmus/hugo-ficurinia) 主题，Astronaut 是在其基础上优化和改进而来的。在此非常感谢 Gabriele Musco 对其主题的精心打磨。

## 站点配置

在Hugo站点配置文件 `hugo.toml` 中，添加下面的参数可以定制 Astronaut 的一些功能。

```toml
# 站点的根URL
baseURL = "https://example.com/"

# 主题
theme = "hugo-astronaut"

# 标题
title = "My Blog"

# 站点的语言标识码
languageCode = "en"

# 站点内容默认语言
# 可以控制内容中i18n词条展示对应语言的翻译
defaultContentLanguage = "en"

# 版权信息
# 这个内容将展示在页脚当前站点构建年份后：2024 © copyright
# 版权信息支持 Markdown 语法
copyright = "Some copyright notice - [my license](https://example.com/license)"

# 单页文章个数
paginate = 5

# 文章摘要字数
summaryLength = 70


[params]

    # Meta信息（SEO优化）
    author = "Kanghua He" # 文章作者
    description = "A description for my website" # 站点描述信息


    # 文章内容目录
    posts = "posts" # 首页文章将从这个目录中获取，默认值: "posts" "post"
    

    # 首页配置
    # 是否将一个特殊的单页面作为首页展示，用来替换传统的文章列表首页
    # 开启此参数需要配置首页路径 “homeSinglePage”
    showSinglePageAsHome = false # 默认值: false
    homeSinglePage = "/home"

    # 站点图标（最好将图标放在自己站点的 "static" 目录中）
    logo = "/logo.svg"
    favicon = "/favicon.png"  # 32x32
    faviconIco = "/favicon.ico"  # 32x32
    appletouch = "/apple-touch-icon.png"  # 180x180
    svgicon = "/logo.svg"
    icon512 = "/icon512.png"  # 512x512

    # 图标在标题右侧展示
    logoRightOfTitle = false  # 默认值: false

    # 展示RSS图标
    showRss = true # 默认值: true

    # 图片在文章预览页面中展示
    imageInArticlePreview = false # 默认值: false

    # 调整图片大小以适配文章预览（非裁剪）
    fitImageInArticlePreview = false # 默认值: false

    # 文章预览页面展示文章摘要
    articleSummary = true # 默认值: true
    
    # 字体
    fontFamily = "JetBrains Mono" # 默认值: "JetBrains Mono"
    titleFontFamily = "JetBrains Mono"  # 标题和头部字体 默认值: "JetBrains Mono"
    monospaceFontFamily = "JetBrains Mono"  # 代码块字体 默认值: "JetBrains Mono"

    # 字体大小（放大或缩小倍数）
    titleFontSizeMultiplier = 1.0 # 标题字体大小
    mainFontSizeMultiplier = 1.0 # 页面内容字体大小
    monoFontSizeMultiplier = 1.0 # 代码字体大小

    # 文章内容宽度
    contentWidth = "1200px"

    # 卡片风格展示文章列表
    paperCards = false # 默认值: false

    # 卡片风格中使用网格布局展示文章列表
    gridView = false # 默认值: false

    # 按钮风格展示文章内容中的标签
    buttonTags = false # 默认值: false

    # 文章预览页面展示文章的标签
    tagsInArticlePreview = true # 默认值: true

    # 文章内容页面是否展示大标题
    bigArticleTitle = false # 默认值: false

    # 分页按钮样式
    navtype = "standard" # 可用样式: "standard", "circles" 默认值: "standard"
    
    # 菜单栏样式
    menuStyle = "standard" # 可用样式: "standard", "buttons" 默认值: "standard"
    
    # 输入框样式
    inputStyle = "standard" # 可用样式: "standard", "buttons" 默认值: "standard"

    # 展示阴影样式
    enableShadow = false # 默认值: false

    # 开启搜索
    enableSearch = true # 默认值: true

    # 任何页面都展示搜索框
    searchbarEverywhere = true # 默认值: true

    # 小屏幕浏览时使用汉堡菜单风格
    mobileHamburgerNav = false # 默认值: false

    # 在文章预览页面采用特殊视图展示文章（对应文章的frontmatter中要配置featured: true）
    enableFeatured = false # 默认值: false

    # 文章标题显示下划线
    underlineTitleLinks = false # 默认值: false

    # 使用Umami进行网站分析（需要在Umami网站上获取下面的配置信息）
    umamiScriptUrl = "https://something.com/..."
    umamiWebsiteId = "example-tracking-code"

    # 文章内容页面中TOC内容在图片之前
    tocBeforeImage = false # 默认值: false

    # 侧边栏布局
    enableSidebarLayout = false # 默认值: false

    # TOC在侧边栏显示
    tocInSidebar = false # 需要开启 enableSidebarLayout = true 默认值: false

    # 强制重定向
    forceRedirect = false

    # 无限滚动
    infiniteScrolling = false  # 无限滚动模式替换分页模式（需要在[outputs]中配置输出JSON格式）

    # 页脚信息栏（后文有详细描述）
    enableFooterColumns = false  # 默认值: false

    # 巨幕（后文有详细描述）
    enableJumbotron = false  # 默认值: false

    # 展示相关文章
    enableRelatedArticles = false
    # 相关文章数量
    relatedArticlesNum = 2 # 默认值: 2
    # 随机展示相关文章顺序
    randomRelated = false # 按时间随机排序 默认值: false

# 导航栏菜单
# 菜单固定展示(Home, Posts, Categories, Tags, About)
[menu]
    # 图标菜单
    [[menu.icons]]
        identifier = "gitlab"
        name = "GitLab"
        url = "https://gitlab.com/gabmus"
        weight = 10
    [[menu.icons]]
        identifier = "gnome"
        name = "GNOME GitLab"
        url = "https://gitlab.gnome.org/gabmus"
        weight = 20

# 开启了无限滚动的话必须配置JSON输出
# 这样就可以通过JavaScript访问JSON格式的文章内容
[outputs]
    home = ["HTML", "JSON"]     
```

### 支持的图标
主题中为`[[menu.icons]]`图标菜单内置了一些图标，可以通过identifier匹配对应图标。下面是一些支持的图标标识：
- discord
- email
- facebook
- github
- gitlab
- gnome
- instagram
- linkedin
- mastodon
- matrix
- peertube
- phone
- pleroma
- rss
- steam
- telegram
- twitter
- xmpp
- youtube

## 主题颜色

主题的颜色可以完全自定义配置。在主题的[`data/colors.yml`](data/colors.yml)中定义的颜色的配置。只需要将该文件复制到
你的站点下的`data/colors.yml`文件中，然后通过修改该文件既可自定义主题颜色。

## 页脚信息栏

如果需要在页脚展示一些链接信息，那么可以在你的站点中新建`data/footer_columns.yml`配置文件，然后按照下面的示例配置需要展示的链接信息即可。

```yaml
- title: My other projects
  links:
    - title: Project1
      link: https://project1.com
    - title: Project2
      link: https://project2.com
- title: About me
  links:
    - title: My personal website
      link: https://mysite.com
    - title: My GitHub
      link: https://github.com/mygithubxxx
```

## 巨幕
可以通过在你的站点的`data/jumbotron.yml`文件来配置添加一个在首页开始前的巨幕。下面是示例配置：

```yaml
title: My awesome website
hugeTitle: false
subtitle: Some fancy subtitle
image: /jumbotron_image.svg
imagePosition: left  # values: left, right, top, bottom
background: /img/jumbotron_bg.png
backgroundVideo: /jumbotron_video.mp4  # 可替换background
# 最好同时提供mp4和web源以达到更好的适配效果
backgroundVideoMp4: /jumbotron_video.mp4
backgroundVideoWebm: /jumbotron_video.webm
videoOpacity: 1.0
textShadow: false
fullscreen: false
downArrow: false
whiteText: false  # 巨幕中强制显示白色文本
links:
  - title: About me
    link: /about
  - title: Read my blog
    link: /posts
```

# 文章参数
每个文章都会包含一些参数在frontmatter中，下面是一些参数的示例：

- `title`: 文章标题
- `date`: 日期时间，通常是创建文件时自动生成
- `description`: 文章描述（SEO优化）
- `tags`: 文章标签（数组类型）
- `image`: 文章图片（在阅览和精选时会展示）
- `alt`: 图片不存在时展示的文本
- `imageCaption`: 图片下方的标题（MarkDown格式渲染）
- `featured`: boolean, 标注文章是否为精选
- `comments`: boolean, 是否开启文章评论(默认使用Disqus)
- `showDate`: boolean, 是否展示日期（适用于非文章页面）
- `showTitle`: boolean, default: true, 是否隐藏标题
- `norss`: boolean, 是否添加到RSS
- `nosearch`: boolean, 是否可搜索
- `toc`: boolean, 是否展示文章内容目录

## 文章内容目录
可以在站点的配置文件`hugo.toml`中配置文章内容目录的展示格式。

```toml
[markup]
  [markup.tableOfContents]
    endLevel = 5
    ordered = false
    startLevel = 1
```