# HTML Reader

一个高级简约的网页版 HTML 阅读器，采用苹果风格设计，支持书架管理、分类、搜索、阅读进度记忆以及基于 GitHub 公开仓库的书籍存储。

## 特性

- 📚 **书架浏览**：网格化展示所有 HTML 电子书
- 📥 **本地导入 HTML**：支持拖拽上传和文件选择，仅在当前浏览器可用
- 🔍 **实时搜索**：按书名、分类快速查找
- 🏷️ **分类管理**：自定义分类，给书籍归类
- 📖 **阅读进度**：自动记录滚动位置和阅读百分比
- ☁️ **GitHub 书库**：HTML 文档存放在本仓库的 `books/` 目录，阅读器启动时自动从 GitHub 加载

## 在线访问

本仓库已启用 GitHub Pages，直接访问：

https://AHH20250507.github.io/html-reader

## 使用方式

### 方式一：由助手上传（推荐）

直接把 HTML 文件发给我，我会上传到这个仓库的 `books/` 目录。阅读器打开后会自动从 GitHub 加载这些书籍，进度和分类会自动保存到浏览器本地。

### 方式二：自己上传到 GitHub

1. 把 HTML 文件上传到仓库的 `books/` 目录。
2. 打开上面的链接，阅读器会自动从仓库拉取书籍。

### 方式三：本地临时阅读

1. 打开上面的链接。
2. 点击右上角 **导入 HTML**，选择或拖拽 HTML 文件到书架。
3. 这些书籍只保存在当前浏览器，不会上传到 GitHub。

## 目录结构

```
html-reader/
├── index.html           # 单页应用（阅读器）
├── README.md            # 说明文档
└── books/               # 存放 HTML 文档（助手或用户上传）
    └── (your books).html
```

书架元数据和阅读进度默认保存在浏览器 IndexedDB 中。阅读器启动时会自动从仓库 `books/` 目录加载书籍，并尝试读取 `reader-metadata.json` 中的分类和进度信息。

## 技术栈

- 原生 HTML5 / CSS3 / JavaScript
- IndexedDB（本地存储）
- GitHub REST API（读取公开仓库书籍）

## 本地预览

```bash
python -m http.server 8080
```

然后打开 http://localhost:8080。
