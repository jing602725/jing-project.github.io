# 个人博客创建计划

基于您提供的两个参考博客，我为您制定了以下详细的博客创建计划。

## 一、参考博客分析

### 1. Areay's Blog (https://areay-blog.pages.dev/)
- **技术栈**: Hexo + Anzhiyu主题
- **部署平台**: Cloudflare Pages
- **设计风格**: 现代简洁、科技感、细节丰富
- **主要功能**:
  - 文章分类（技术、量化、生活）
  - 标签云
  - 深色/浅色模式切换
  - 音乐播放器
  - 微信/支付宝打赏
  - 随机文章跳转
  - 增强右键菜单
  - 站内搜索

### 2. 部署指南博客 (https://blog.oneiseven.top/)
- **内容**: Hexo博客从GitHub Pages迁移到Cloudflare Pages的完整指南
- **核心优势**: Cloudflare Pages国内访问更快，自动部署（git push即部署）

## 二、技术选型

### 核心技术栈
- **静态网站生成器**: Hexo (v7+)
- **博客主题**: Anzhiyu (与参考博客一致)
- **版本控制**: Git
- **代码托管**: GitHub (使用您提供的账户: 1946914722decade)

### 部署方案选择

我为您准备了两个部署方案，请根据需求选择：

#### 方案A: GitHub Pages (简单快捷)
**优点**:
- 设置简单，无需额外账户
- 与GitHub仓库直接集成
- 完全免费

**缺点**:
- 国内访问速度较慢
- 需要手动部署（`hexo deploy`）或配置GitHub Actions

**适用场景**: 主要面向海外用户，或对访问速度要求不高

#### 方案B: Cloudflare Pages (推荐)
**优点**:
- 国内访问速度快（全球CDN）
- 自动部署（git push即部署）
- 免费额度充足（每月500次构建）
- 可绑定自定义域名

**缺点**:
- 需要Cloudflare账户
- 设置步骤稍多

**适用场景**: 主要面向国内用户，追求访问速度和自动化

## 三、实施步骤

### 第一阶段：环境准备 (预计时间: 30分钟)

1. **安装Node.js环境**
   - 确保Node.js版本 ≥ 20
   - 安装npm包管理器

2. **安装Hexo CLI**
   ```bash
   npm install -g hexo-cli
   ```

3. **初始化Hexo项目**
   ```bash
   hexo init blog
   cd blog
   npm install
   ```

### 第二阶段：主题配置 (预计时间: 1-2小时)

1. **安装Anzhiyu主题**
   ```bash
   git clone https://github.com/anzhiyu-c/hexo-theme-anzhiyu themes/anzhiyu
   ```

2. **配置主题**
   - 修改 `_config.yml` 启用Anzhiyu主题
   - 配置主题参数（菜单、侧边栏、样式等）
   - 添加示例文章和页面

3. **自定义调整**
   - 根据参考博客调整布局和样式
   - 配置音乐播放器、打赏功能等

### 第三阶段：GitHub仓库设置 (预计时间: 30分钟)

1. **创建GitHub仓库**
   - 使用您的GitHub账户创建新仓库
   - 仓库名建议: `blog` 或 `1946914722decade.github.io`

2. **推送代码到GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/1946914722decade/blog.git
   git push -u origin main
   ```

### 第四阶段：部署配置 (根据选择方案)

#### 方案A: GitHub Pages部署
1. 在GitHub仓库设置中启用GitHub Pages
2. 选择部署分支（通常是`main`或`gh-pages`）
3. 配置自定义域名（可选）

#### 方案B: Cloudflare Pages部署
1. 注册Cloudflare账户
2. 连接GitHub仓库
3. 配置构建设置：
   - 构建命令: `npx hexo generate`
   - 输出目录: `public`
   - 环境变量: `NODE_VERSION=20`

### 第五阶段：内容完善 (持续进行)

1. **添加个人内容**
   - 编写"关于"页面
   - 添加个人介绍、联系方式
   - 配置社交链接

2. **发布文章**
   - 创建新文章: `hexo new "文章标题"`
   - 编写Markdown内容
   - 推送到GitHub自动部署

## 四、项目结构预览

```
blog/
├── _config.yml          # Hexo主配置文件
├── package.json         # 项目依赖
├── scaffolds/           # 文章模板
├── source/              # 源文件目录
│   ├── _posts/          # 文章目录
│   ├── about/           # 关于页面
│   └── categories/      # 分类页面
├── themes/              # 主题目录
│   └── anzhiyu/         # Anzhiyu主题
└── public/              # 生成的静态文件
```

## 五、时间安排

1. **第1天**: 环境准备、项目初始化、主题安装配置
2. **第2天**: GitHub仓库设置、部署配置
3. **第3天**: 内容完善、自定义调整
4. **后续**: 持续发布文章、优化博客

## 六、需要您确认的事项

1. **部署方案选择**: GitHub Pages 还是 Cloudflare Pages？
2. **仓库命名**: 使用`blog`还是`1946914722decade.github.io`？
3. **博客语言**: 主要使用中文还是英文？
4. **特殊需求**: 是否需要参考博客中的特定功能（如音乐播放器、打赏等）？

请确认以上计划，我将根据您的选择开始实施。