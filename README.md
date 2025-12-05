# 🎄 手势控制 3D 粒子圣诞树

一个使用 Three.js、MediaPipe Hands 和 GSAP 构建的交互式 3D 粒子圣诞树，通过手势控制实现丰富的交互效果。

<div align="center">
  <img src="https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=three.js&logoColor=white" alt="Three.js" />
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/MediaPipe-FF6F00?style=for-the-badge&logo=google&logoColor=white" alt="MediaPipe" />
</div>

## ✨ 特性

- 🎨 **华丽的视觉效果**
  - 金色发光粒子系统
  - 多层烟花爆炸效果
  - 飘雪动画
  - 电影级光晕效果（UnrealBloomPass）
  - 树顶闪烁星星

- 🤲 **丰富的手势交互**
  - **握拳**：控制粒子聚合成树形
  - **张开**：粒子散开成星尘
  - **6DOF 控制**：握拳时移动手部旋转树
  - **1 根手指**：切换颜色主题
  - **2 根手指**：开启/关闭飘雪
  - **3 根手指**：触发烟花效果

- 🌲 **真实的树形**
  - 基于 Phyllotaxis（叶序）算法的自然树形
  - 指数轮廓，底部宽顶部尖
  - 分层结构，清晰的层次感
  - 深棕色树干

- ⚡ **高性能**
  - 5000+ 粒子流畅运行
  - 60fps 稳定帧率
  - 优化的物理模拟

## 🚀 快速开始

### 安装依赖

```bash
npm install
```

### 运行开发服务器

```bash
npm run dev
```

### 构建生产版本

```bash
npm run build
```

## 🌐 在线部署

### GitHub Pages（已配置自动部署）

项目已配置 GitHub Actions 自动部署到 GitHub Pages。

1. **启用 GitHub Pages**：
   - 进入仓库设置：https://github.com/fuguther/gesture-christmas-tree-2/settings/pages
   - Source 选择：**GitHub Actions**
   - 保存设置

2. **自动部署**：
   - 每次推送到 `main` 分支会自动触发部署
   - 部署完成后，访问：`https://fuguther.github.io/gesture-christmas-tree-2/`

3. **手动触发部署**：
   - 在 GitHub 仓库的 Actions 标签页，选择 "Deploy to GitHub Pages" workflow
   - 点击 "Run workflow" 按钮

### 其他部署选项

#### Vercel（推荐，更简单）

1. 访问 [Vercel](https://vercel.com)
2. 导入 GitHub 仓库
3. 自动检测 Vite 配置，点击部署
4. 完成！会获得一个 `*.vercel.app` 域名

#### Netlify

1. 访问 [Netlify](https://www.netlify.com)
2. 导入 GitHub 仓库
3. Build command: `npm run build`
4. Publish directory: `dist`
5. 部署完成

## 📋 使用说明

1. **允许摄像头权限**：应用需要访问摄像头进行手势识别
2. **握拳**：将手掌握成拳头，粒子会聚合成圣诞树形状
3. **张开**：张开手掌，粒子会散开成星尘
4. **旋转控制**：握拳时移动手部，可以旋转圣诞树
5. **切换主题**：伸出 1 根手指（食指）
6. **飘雪效果**：伸出 2 根手指（✌️）
7. **烟花效果**：伸出 3 根手指（🤟）

## 🛠️ 技术栈

- **Three.js** - 3D 渲染引擎
- **React** - UI 框架
- **TypeScript** - 类型安全
- **MediaPipe Hands** - 手势识别
- **GSAP** - 动画库
- **Vite** - 构建工具

## 📦 项目结构

```
gesture-christmas-tree-2/
├── components/
│   └── GestureTree.tsx    # 主组件（Three.js + MediaPipe）
├── App.tsx                 # React 应用入口
├── index.tsx               # 应用初始化
├── types.ts                # TypeScript 类型定义
├── vite.config.ts          # Vite 配置
└── package.json            # 项目依赖
```

## 🎨 视觉效果

- **粒子着色器**：自定义 GLSL 着色器实现金色发光和闪烁效果
- **后处理**：EffectComposer + UnrealBloomPass 实现电影级光晕
- **物理模拟**：基于 LERP 的重力场和爆炸力
- **多层烟花**：3 层爆炸效果，450+ 粒子，渐变色彩

## 📝 许可证

MIT License

## 🙏 致谢

- Three.js 社区
- MediaPipe 团队
- GSAP 团队
