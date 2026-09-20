

# Haku Fumomo - 个人主页

一个基于 Nuxt 4 + Vue 3 + Tailwind CSS 构建的现代化个人主页，支持 RSS 订阅文章功能。

[English](./docs/README.en.md) | [日本語](./docs/README.ja.md) 多语言文档更新可能不及时

## 功能特点

- 现代化设计，支持响应式布局
- 移动端友好
- RSS 文章订阅功能
- 基于 Nuxt 4，性能优秀
- TypeScript 支持
- Tailwind CSS 样式
- 友链：来自[RhenCloud](https://github.com/RhenCloud)
- 访问统计：来自[yCENzh](https://github.com/yCENzh)

## 技术栈

- **前端框架**: Nuxt 4 + Vue 3
- **样式**: Tailwind CSS v3
- **类型**: TypeScript
- **部署**: Vercel
- **RSS解析**: fast-xml-parser

## 安装和运行

### 本地开发

```bash
# 安装依赖
pnpm install

# 启动开发服务器
pnpm dev

# 访问 http://localhost:3000
```

### 构建生产版本

```bash
# 构建项目
pnpm build

# 预览构建结果
pnpm preview
```

## 部署到 Vercel

### 自动部署（推荐）

1. 将代码推送到 GitHub 仓库
2. 在 [Vercel](https://vercel.com) 导入你的 GitHub 仓库
3. Vercel 会自动检测 Nuxt 项目并进行部署
4. 部署完成后会获得一个 `.vercel.app` 域名

### 手动部署

```bash
# 安装 Vercel CLI
npm i -g vercel

# 部署
vercel --prod
```

## 配置

### RSS 订阅配置、收发邮件配置

在 `.env` 中修改相关配置



### 个人信息配置

在 `app/config/index.ts` 中修改个人信息：

```typescript
personal: {
  name: "你的名字",
  bio: "个人简介",
  avatar: "头像URL",
  social: {
    github: "https://github.com/your-username",
    email: "your-email@example.com"
  }
}
```
### 技能专长配置
前往下面这个网站获取图标Vue文件放入components/icons

https://icones.js.org/collection/logos

### GitHub热力图

只要在配置中正确填写你的Github链接即可自动生成

## 项目结构

```
fumomo-nuxt/
├── app/
│   ├── assets/
│   │   └── styles/          # 全局样式
│   ├── components/          # Vue 组件
|   |   └── icons/           # 技能专长Icons
│   ├── config/
│   │   └── index.ts         # 网站配置
│   ├── layouts/
│   │   └── default.vue      # 默认布局
│   └── pages/               # 页面路由
├── server/
│   └── api/
│       └── rss.get.ts       # RSS API 路由
├── public/                  # 静态资源
├── nuxt.config.ts           # Nuxt 配置
└── package.json
```

## 自定义配置

### 修改主题色彩

在 `app/config/index.ts` 中的 `theme` 部分：

```typescript
theme: {
  primaryColor: "#8b5a8c",      // 主色调
  secondaryColor: "#f0f9ff",    // 次要色
  accentColor: "#ffeef8",       // 强调色
  textColor: "#666",            // 文字色
  fontFamily: "'Comic Sans MS', 'XiaokeNailao', cursive, sans-serif"
}
```

### 修改导航菜单

在 `app/config/index.ts` 中的 `navigation` 部分：

```typescript
navigation: [
  { name: "首页", href: "/", key: "home"},
  { name: "文章", href: "/articles", key: "articles"},
  { name: "关于", href: "/about", key: "about"},
  // 添加更多导航项...
]
```



## Vercel 部署优化

项目已针对 Vercel 部署进行优化：

- 使用 `vercel-edge` 预设，提升性能
- 预渲染首页，提高 SEO
- 自动缓存静态资源
- 支持 Serverless Functions

## 许可证

MIT License

## 贡献

欢迎提交 Issue 和 Pull Request！

---

如果这个项目对你有帮助，请给个 Star 支持一下！
