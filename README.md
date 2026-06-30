# HTML Reader

一个高级简约的网页版 HTML 阅读器，采用苹果风格设计，支持书架管理、分类、搜索、阅读进度记忆以及 GitHub 同步。

## 特性

- 📚 **书架浏览**：网格化展示所有 HTML 电子书
- 📥 **导入 HTML**：支持拖拽上传和文件选择
- 🔍 **实时搜索**：按书名、分类快速查找
- 🏷️ **分类管理**：自定义分类，给书籍归类
- 📖 **阅读进度**：自动记录滚动位置和阅读百分比
- ☁️ **GitHub 同步**：阅读器应用部署在公开仓库，HTML 文档存放在仓库内，通过 GitHub API 读取

## 在线访问

本仓库已启用 GitHub Pages，直接访问：

https://AHH20250507.github.io/html-reader

## 使用说明

1. 打开上面的链接，进入 HTML Reader。
2. 点击右上角 **导入 HTML**，选择或拖拽 HTML 文件到书架。
3. 在左侧可以创建分类、筛选书籍。
4. 点击书籍封面即可开始阅读，阅读进度会自动保存到浏览器本地。
5. 如需跨设备同步，在 **设置** 中填写本仓库的 GitHub Token（需要 `repo` 权限）并开启自动同步。

## 目录结构

```
html-reader/
├── index.html           # 单页应用（阅读器）
├── README.md            # 说明文档
└── books/               # 存放 HTML 文档
    └── (your books)
```

书架元数据和阅读进度默认保存在浏览器 IndexedDB 中。开启 GitHub 同步后，阅读器会在本仓库创建 `reader-metadata.json` 来同步进度。

## 技术栈

- 原生 HTML5 / CSS3 / JavaScript
- IndexedDB（本地存储）
- GitHub REST API（云端同步）

## 本地预览

```bash
python -m http.server 8080
```

然后打开 http://localhost:8080。
