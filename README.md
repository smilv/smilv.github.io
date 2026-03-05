# smilv.github.io

一个基于 Nuxt 3 的个人博客/作品展示项目，采用现代化的前端技术栈，包含静态资源和历史项目归档。

## 技术栈

- **框架**: [Nuxt 3](https://nuxt.com/) (v3.15.1)
- **UI 框架**: [Vue 3](https://vuejs.org/)
- **路由**: [Vue Router](https://router.vuejs.org/)
- **样式**: 
  - [Tailwind CSS](https://tailwindcss.com/) (v6.13.1)
  - [Sass](https://sass-lang.com/) (v1.83.4)
- **语言**: [TypeScript](https://www.typescript.org/)
- **包管理**: pnpm（推荐）

## 项目结构

```
├── app.vue                 # 主应用入口
├── nuxt.config.ts         # Nuxt 配置文件
├── tailwind.config.ts      # Tailwind CSS 配置
├── tsconfig.json           # TypeScript 配置
├── .github/
│   └── workflows/
│       └── nuxtjs.yml      # GitHub Actions CI/CD 部署工作流
├── pages/                  # 页面路由目录
│   └── index.vue          # 首页
├── assets/                # 静态资源
│   └── css/
│       └── parallax.scss   # 视差效果样式
├── public/                # 公共资源
│   ├── robots.txt
│   ├── images/            # 图片资源
│   ├── infancy/           # 历史项目归档
│   └── storybook-static/  # Storybook 静态输出
└── server/                # 服务器端配置
```

## 核心功能

- ✨ 现代化的 Nuxt 3 应用
- 🎨 Tailwind CSS 样式框架
- 📱 响应式设计
- 📦 历史项目归档和展示
- 🔍 搜索引擎友好


## 部署

### GitHub Pages + GitHub Actions 自动部署

本项目采用 GitHub Actions 进行 CI/CD 自动构建和部署。每次提交代码到主分支时，GitHub Actions 将自动：
1. 安装项目依赖
2. 构建静态网站
3. 部署到 GitHub Pages

#### 部署流程说明

```
Git Push → GitHub Actions 触发
    ↓
安装依赖 (pnpm install)
    ↓
构建项目 (pnpm generate)
    ↓
生成 dist 文件夹
    ↓
部署到 GitHub Pages
    ↓
网站自动更新至 https://smilv.github.io
```

## 快速开始

### 环境要求

- Node.js >= 18+
- pnpm >= 8+ (推荐)

### 安装依赖

```bash
# 使用 pnpm
pnpm install
```

### 开发服务器

启动开发服务器，访问 `http://localhost:3000`:

```bash
# pnpm (推荐)
pnpm dev
```

### 生产构建

构建生产版本：

```bash
# pnpm
pnpm build
```

### 预览生产构建

```bash
# pnpm
pnpm preview
```

### 静态生成

生成静态网站文件（用于部署到 GitHub Pages）：

```bash
# pnpm
pnpm generate
```

## 资源和文档

- [Nuxt 3 文档](https://nuxt.com/docs)
- [Vue 3 文档](https://vuejs.org/)
- [Tailwind CSS 文档](https://tailwindcss.com/)
- [Nuxt Tailwind 模块](https://tailwindcss.nuxtjs.org/)
- [GitHub Actions 文档](https://docs.github.com/en/actions)
- [GitHub Pages 文档](https://docs.github.com/en/pages)
