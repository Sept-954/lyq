 # Design：个人网站
 
 ## 1. 页面区块与浏览顺序
 
 单页落地页 + 独立博客页结构：
 
 1. **首页** (`/`) —— splash 全宽布局
    - Hero：深色覆盖背景 + 站点标题（L 的个人空间）
    - About：个人简介
    - Skills：技能标签列表（待补充）
    - Projects：项目链接
    - Contact：GitHub 链接
 2. **文章列表** (`/posts/`) —— 博客文章归档，图文缩略图 + 摘要
 3. **文章详情** (`/posts/:slug/`) —— 单篇文章全文
 4. **分类 / 标签归档** (`/categories/`, `/tags/`) —— 按分类或标签筛选
 
 ## 2. 颜色、字体与整体风格
 
 - **主题皮肤**：Minimal Mistakes `air` 皮肤（淡蓝色系）
 - **Hero 背景色**：`#2c3e50`（深蓝灰）
 - **字体**：主题默认（sans-serif），正文 1.15em
 - **整体风格**：简约、偏学术、内容优先
 
 ## 3. 响应式要求
 
 - **桌面端**：双栏布局，导航在顶部，内容区居中，最大宽度 64em
 - **手机端**：导航自动折叠为汉堡菜单，内容全宽单列
 - **缩略图**：博客列表缩略图自适应，在手机上缩为小图
 
 ## 4. 关键文件分工
 
 | 文件 | 职责 |
 |---|---|
 | `_config.yml` | 站点全局配置（title/author/skin/plugins/默认布局） |
 | `Gemfile` | Ruby 依赖声明 |
 | `index.html` | 首页 splash 页面，含全部五个区块 |
 | `404.html` | 自定义 404 错误页 |
 | `_data/navigation.yml` | 主导航菜单配置 |
 | `_pages/posts.md` | 博客文章归档页面 |
 | `_pages/categories.md` | 分类归档页面 |
 | `_pages/tags.md` | 标签归档页面 |
 | `_posts/*.md` | 博客文章，每篇含 title/teaser/excerpt/正文 |
 | `assets/images/` | 图片资源（头像、缩略图占位） |
 | `docs/prd.md` | 产品需求文档 |
 | `docs/design.md` | 设计说明 |
 | `docs/checklist.md` | 验收检查清单 |
 | `report/final-report.md` | 最终报告 |
 
 ## 5. 保留与修改
 
 **保留的**：
 - 主题的布局模板（`splash`、`single`、`archive`、`home`）
 - 主题的导航栏、作者侧栏、页脚
 - 主题的响应式行为
 
 **修改的**：
 - `_config.yml` —— 替换为个人资料
 - `index.html` —— 从 `layout: home` 改为 `layout: splash`，写入五个区块
 - `_data/navigation.yml` —— 精简导航项
 - `_posts/` —— 替换为个人博客内容
 
 ## 6. 图片与外部素材
 
 - 头像、占位图均为自制 SVG
 - 主题 CSS/JS 通过 remote_theme 从 GitHub Pages 获取
 - 图标使用 Font Awesome（主题自带）
