# 使用说明

这套 Markdown 文件适合直接用于静态网站，例如：

- VitePress
- Docusaurus
- MkDocs
- Next.js + contentlayer / mdx
- Astro Starlight

## 文件结构

- `index.md`：首页，包含每天索引和自动跳转脚本
- `days/*.md`：每天的独立页面

## 自动跳转说明

首页 `index.md` 内嵌了一个基于浏览器本地时间的脚本：

- 进入首页时识别本地日期
- 若日期在 2026-03-25 到 2026-04-04 之间
- 自动跳转到对应的日程页

如果你的框架默认不允许 Markdown 中执行 script：

1. 把首页中的 `<script>...</script>` 拷到主题自定义 JS
2. 保留首页里每天的映射表
3. 在站点加载完成后执行同样逻辑即可

## 注意

Markdown 中的 Google Maps 链接已经拆成上午 / 下午两段，更适合手机打开。
