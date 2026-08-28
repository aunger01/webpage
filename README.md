# webpage — 安杰主页 / 网址转发仓库

> Web Forwarding Warehouse · 纯静态站点，由 GitHub Pages 托管

线上地址：<https://l1n2.com>（CNAME 绑定，详见根目录 `CNAME` 文件）

## 仓库结构

| 目录/文件 | 用途 |
|---|---|
| `index.html` | 主页（安杰主页，含导航入口、联系方式、公众号二维码） |
| `index1.html` | 旧版地址发布页（已 noindex） |
| `css/` | 主页样式（`main.css` 为 normalize，`style.css` 为页面样式） |
| `img.webp` / `mark.webp` | 主页背景图 / 印记图 |
| `gzh.jpg` / `logo@2x.png` / `favicon.ico` / `apple-ico-2.png` | 二维码、Logo、站点图标 |
| `mp4/index.html` | 离线视频格式重封装工具（remux，不重新编码） |
| `I_help_you/` | 「你不会百度吗」恶搞子站（Baidu / Bing / Google 三套皮肤） |
| `alist/` `github/` `google/` `gpt/` `s/` 等 | 各子域跳转页（`*.l1n2.com/xxx` → 目标站） |

## 跳转页约定

每个子目录一个 `index.html`，跳转到对应服务地址。修改跳转目标时只需改该文件里的目标 URL。

## 开发与部署

- 推送到 `master` 分支后 GitHub Pages 自动发布。
- 主页背景在 `css/style.css` 的 `.page-body` 中引用 `img.webp`，更换背景直接替换该文件即可。
