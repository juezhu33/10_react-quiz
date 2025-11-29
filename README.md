# React Quiz Application

一个基于 React 构建的交互式测验应用程序，用于测试用户对 React 知识的掌握程度。

## 项目简介

这是一个完整的 React 测验应用程序，具有现代化的 UI 设计和流畅的用户体验。用户可以回答有关 React 框架的各种问题，并获得实时反馈和最终成绩评估。

该应用程序展示了 React 开发中的多种重要概念和最佳实践，包括：

- 组件化开发
- 状态管理和 useReducer Hook 的使用
- useEffect 进行副作用处理
- 自定义组件的创建和组合

## 功能特点

- 📝 **问答测验**: 回答关于 React 框架的多项选择题
- ⏱️ **倒计时**: 每个测验都有时间限制，增加挑战性
- 🏆 **得分系统**: 根据正确答案计算分数，并保存最高分记录
- 🎨 **响应式设计**: 在不同设备尺寸上都能良好显示
- 🔄 **重新开始**: 测验结束后可以选择重新开始
- 📊 **进度追踪**: 显示当前答题进度和累计得分

## 技术栈

- [React](https://reactjs.org/) (v19.2.0)
- [Create React App](https://create-react-app.dev/) 构建工具
- [JSON Server](https://github.com/typicode/json-server) 用于模拟 REST API
- Vanilla CSS (无额外 CSS 框架)

## 项目结构

```
src/
├── components/     # React 组件
├── data/           # 测验问题数据
├── index.css       # 全局样式
└── index.js        # 应用入口文件
```

## 安装与运行

### 前提条件

确保你的系统已经安装了 [Node.js](https://nodejs.org/) 和 npm。

### 安装步骤

1. 克隆或下载此仓库
2. 安装依赖包：

```bash
npm install
```

### 运行应用

此应用需要同时运行前端和模拟服务器：

1. 启动模拟服务器 (端口 9000)：

```bash
npm run server
```

2. 在另一个终端中启动前端开发服务器 (端口 3000)：

```bash
npm start
```

应用将在浏览器中自动打开，地址为 http://localhost:3000

### 构建生产版本

要创建生产优化版本，请运行：

```bash
npm run build
```

构建文件将位于 `build/` 目录中。

## 测验数据

测验问题存储在 [src/data/questions.json](src/data/questions.json) 文件中，采用以下格式：

```json
{
  "questions": [
    {
      "question": "问题文本",
      "options": ["选项1", "选项2", "选项3", "选项4"],
      "correctOption": 1, // 正确选项的索引 (从0开始)
      "points": 10 // 该问题的分数
    }
  ]
}
```

你可以轻松地修改此文件来添加更多问题或更改现有问题。

## 可用脚本

在项目目录中，你可以运行以下命令：

- `npm start`: 启动开发服务器
- `npm run server`: 启动 JSON Server 来提供测验数据
- `npm test`: 启动测试运行器（处于监听模式）
- `npm run build`: 构建生产版本
- `npm run eject`: 弹出配置（注意：此操作不可逆！）

## 学习要点

通过研究此项目源码，你可以学习到：

1. 如何使用 useReducer 管理复杂的状态逻辑
2. 如何组织大型 React 应用的组件结构
3. 如何实现计时器功能并与应用状态集成
4. 如何处理异步数据获取
5. 如何创建可重用和可组合的 React 组件
