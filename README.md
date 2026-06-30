# HTML Reader

一个高级简约的网页版 HTML 阅读器，采用苹果风格设计，支持书架管理、分类、搜索、阅读进度记忆以及自动 GitHub 同步。

## 特性

- 📚 **书架浏览**：网格化展示所有 HTML 电子书
- 📥 **导入 HTML**：拖拽或点击上传，自动同步到 GitHub 公开仓库
- 🔍 **实时搜索**：按书名、分类快速查找
- 🏷️ **分类管理**：自定义分类，支持新建和删除
- 📖 **阅读进度**：自动记录滚动位置和阅读百分比，并同步到 GitHub
- ☁️ **自动 GitHub 同步**：导入、删除、分类变更、阅读进度都会自动同步到仓库

## 在线访问

本仓库已启用 GitHub Pages，直接访问：

https://AHH20250507.github.io/html-reader

## 使用说明

1. 打开上面的链接，进入 HTML Reader。
2. 点击左侧 **同步设置**，输入你的 GitHub Personal Access Token（需要 `repo` 权限）。Token 只会保存在当前浏览器中。
3. 点击右上角 **导入 HTML**，选择或拖拽 HTML 文件。
4. 导入成功后，书籍会自动上传到 GitHub 仓库的 `books/` 目录，并出现在书架上。
5. 点击书籍封面即可阅读；阅读进度会自动保存并同步。
6. 删除书籍后，GitHub 仓库中的对应文件也会自动删除。

## 目录结构

```
html-reader/
├── index.html           # 单页应用（阅读器）
├── README.md            # 说明文档
└── books/               # 存放 HTML 文档
    └── (your books)
```

书架分类和阅读进度通过仓库根目录的 `reader-metadata.json` 同步。

## 技术栈

- 原生 HTML5 / CSS3 / JavaScript
- IndexedDB（本地缓存）
- GitHub REST API（云端同步）

## 本地预览

```bash
python -m http.server 8080
```

然后打开 http://localhost:8080。
