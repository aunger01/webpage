# webpage — 安杰主页 / 网址转发仓库

> Web Forwarding Warehouse · 纯静态站点，由 GitHub Pages 托管

线上地址：<https://l1n2.com>（CNAME 绑定，详见根目录 `CNAME` 文件）

## 仓库结构（按三分类归置）

### ① 主页本体（根目录）

| 目录/文件 | 用途 |
|---|---|
| `index.html` | 主页（安杰主页，含导航入口、联系方式、公众号二维码） |
| `index1.html` | 站点目录树（全站文件结构一览，含 GitHub 匿名 API 同步按钮，已 noindex） |
| `css/` | 主页样式（`main.css` 为 normalize，`style.css` 为页面样式） |
| `assets/` | 主页静态资源：`apple-ico.png` / `logo@2x.png` / `gzh.jpg`（二维码）/ `mark.webp`（移动端印记图，桌面端背景为纯 CSS 渐变） |
| `favicon.ico` | 站点图标（按浏览器惯例置于根目录） |
| `CNAME` / `robots.txt` / `404.html` / `.gitignore` | 部署配置 |

### ② 源码子站（`app/`）

| 目录 | 用途 | 访问地址 |
|---|---|---|
| `app/help/` | 「你不会百度吗」恶搞子站（Baidu / Bing / Google 三套皮肤） | <https://l1n2.com/app/help> |
| `app/xjj/` | 随机视频子站 | <https://l1n2.com/app/xjj> |
| `app/mp4/` | 离线视频格式重封装工具（remux，不重新编码） | <https://l1n2.com/app/mp4> |

### ③ 跳转页（根目录一级短链目录）

| 目录 | 跳转目标 |
|---|---|
| `github/` | https://github.testing.ccwu.cc/ |
| `github-top/` | https://10000101.xyz/GitHub-Chinese-Top-Charts/ |
| `google/` | https://10000101.xyz/android-google-play-store/ |
| `gpt/` | https://cc.ai55.cc/ |
| `md/` | https://editor.10000101.xyz/examples/ |
| `my/` | https://1.10000101.xyz/bookmark |
| `pi/` | http://www.subidiom.com/pi/piday.asp |
| `resume/` | https://dnd-resume.com/editor |
| `sbti/` | https://10000101.xyz/SBTI/ |
| `puabook/`（含 `book/`） | https://10000101.xyz/pua-books · https://chriszheng.science/pua-books/ |
| `univ/`（含 `189/`、`carplay/`） | 大学资料网盘等三条转发 |

> `help/`、`mp4/` 在根目录留有 noindex 兜底跳转页，转发至 `app/` 下新地址，旧链接不失效。（`xjj/` 兜底页已按需移除）

## 跳转页约定

每个子目录一个 `index.html`（meta refresh + canonical + 兜底链接，`noindex`）。修改跳转目标时只需改该文件里的目标 URL。新增跳转页时复制 `github/index.html` 模板。

## 开发与部署

- 推送到 `master` 分支后 GitHub Pages 自动发布。
- 主页背景为纯 CSS 渐变 + 流光光晕（`css/style.css` 的 `.page-body`），如需换回图片背景，在 `.page-body` 的 `background` 中将渐变替换为 `url(图片路径)` 即可。
