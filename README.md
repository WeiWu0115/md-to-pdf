# Markdown → PDF

一个纯前端的 Markdown 转 PDF 工具。打开网页、粘贴或拖入 `.md`、点「导出 PDF」即可。无需安装、无需后端、不上传任何文件——一切都在你的浏览器里完成。

**👉 在线使用:https://weiwu0115.github.io/md-to-pdf/**

## 功能

- 📄 **实时预览**——左边写 Markdown,右边即时排版,所见即所得
- 🖱️ **拖拽 / 粘贴 / 打开文件**——三种方式导入
- 🧮 **数学公式**——KaTeX,行内 `$...$`、块级 `$$...$$`
- 📊 **流程图**——Mermaid，写一个 ` ```mermaid ` 代码块即可
- 🎨 **代码高亮**——highlight.js,浅色 / 深色主题可选
- 🔖 **封面页**——可选的标题 / 作者 / 日期独立首页
- 🅰️ **字体与页边距**——无衬线 / 衬线（宋体），窄 / 标准 / 宽
- 🈶 **中文友好**——导出为矢量文字，可选中、可搜索、清晰不糊

## 导出为 PDF

点击「导出 PDF」会唤起浏览器打印对话框：

1. 目标选择 **「另存为 PDF」**
2. 想要干净页面 → 关闭 **「页眉和页脚」**
3. 想要页码 → 打开 **「页眉和页脚」**

> 用浏览器原生打印导出，PDF 是矢量文字而非截图，因此体积小、可选中、中文清晰。

## 本地运行

无需构建，直接打开即可：

```bash
git clone https://github.com/WeiWu0115/md-to-pdf.git
cd md-to-pdf
open index.html        # macOS（或在浏览器中打开 index.html）
```

## 技术栈

纯静态单文件 `index.html`，依赖通过 CDN 引入：

| 用途 | 库 |
|------|-----|
| Markdown 解析 | [marked](https://marked.js.org/) |
| 代码高亮 | [highlight.js](https://highlightjs.org/) |
| 数学公式 | [KaTeX](https://katex.org/) + marked-katex-extension |
| 流程图 | [Mermaid](https://mermaid.js.org/) |
| 转 PDF | 浏览器原生打印（矢量输出） |

## 部署

托管在 GitHub Pages。推送到 `main` 分支后自动更新：

```bash
git add -A && git commit -m "..." && git push
```

## License

MIT
