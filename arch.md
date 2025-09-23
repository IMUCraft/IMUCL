# 项目架构文档

## 1. 项目概述
本项目是一个基于 Next.js 和 Tauri 的现代化应用，旨在提供高性能的前端界面和轻量级的本地应用支持。项目结合了 Web 技术和本地应用的优势，适用于跨平台部署。

## 2. 技术栈
- **前端框架**: Next.js (React)
- **本地应用框架**: Tauri (Rust)
- **状态管理**: 内置 React 状态管理或 Context API
- **样式**: CSS Modules 或 Tailwind CSS
- **国际化**: Next.js i18n
- **构建工具**: npm/yarn

## 3. 目录结构
- **src/**: 前端源代码
  - **components/**: 可复用的 UI 组件
  - **pages/**: Next.js 页面路由
  - **services/**: API 服务层
  - **utils/**: 工具函数
- **src-tauri/**: Tauri 本地应用配置和 Rust 代码
- **public/**: 静态资源
- **docs/**: 项目文档

## 4. 核心模块
- **前端模块**: 基于 Next.js 的页面渲染和交互逻辑。
- **本地模块**: 通过 Tauri 提供的本地能力（如文件系统访问）。
- **API 模块**: 与后端服务交互的逻辑。

## 5. 数据流
- 前端通过 `services/` 调用 API 获取数据。
- 本地功能通过 Tauri 的 Rust 后端实现。
- 状态管理通过 React 的 Context 或状态库实现。

## 6. 部署架构
- **Web 部署**: 通过 Vercel 或其他静态托管服务部署 Next.js 应用。
- **本地应用**: 通过 Tauri 打包为跨平台桌面应用。