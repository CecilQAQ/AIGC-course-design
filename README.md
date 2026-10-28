# NIGHTLI · AIGC 课程设计全案

一个虚拟赛车品牌的完整数字内容项目。从标志到 App 到宣传片，**六项作业串成一条完整链路**。

> 🌐 **在线预览**：[cecilqaq.github.io/AIGC-course-design](https://cecilqaq.github.io/AIGC-course-design/)
> 📦 **完整全案下载**（150 张高清原图 + 9 份文档 + 宣传片，409 MB）：[`AIGC-course-full.zip`](https://github.com/cecilqaq/AIGC-course-design/releases/download/v1.0/AIGC-course-full.zip)
> 🎨 **PSD 源文件**（10 个原始工程，718 MB）：[123 云盘](https://1816407483.share.123pan.cn/123pan/LCPqVv-F8Hkv)　免登录下载

---

## 这是什么

| | |
|---|---|
| 项目 | 虚拟 F1 车队品牌 **NIGHTLI** 的全套视觉与数字内容 |
| 内容 | LOGO 与 VI、IP 形象、文创产品、宣传物料、小程序 App、宣传片、项目报告 |
| 技术 | 小程序 Demo 用原生 HTML + CSS + JavaScript，**无框架、无构建、无依赖** |
| 体积 | 仓库约 68 MB，图片已压缩；原图与视频见 Releases |
| 来源 | AIGC 数字内容创作课程作业，AI 生成 + 人工调整 |
| 许可 | 代码 MIT；图像与文档仅作学习参考 |

## 目录

```
index.html              小程序 Demo（20 个页面，双击即开）
assets/                 Demo 用的 12 张配图 + 8 个图标
作品集/
├─ README.md            作品索引（带预览图）
├─ 01-LOGO与VI/         标志三色版本、设计提案、6 张应用展板
├─ 02-IP形象与文创/      IP 形象、文创周边、提案 PPT
├─ 03-宣传物料/         海报 6 张、线下物料 6 张、公众号 4 篇
├─ 04-视频与剧本/       品牌故事剧本全文
└─ 05-项目报告/         完整创作报告
README.md
LICENSE
```

## 六项作业

| # | 作业 | 看什么 |
|---|---|---|
| 1 | 小程序 UI 交互设计 | [根目录 `index.html`](index.html) — 20 页可交互 Demo |
| 2 | LOGO 及 VI 视觉系统 | [`作品集/01-LOGO与VI`](作品集/01-LOGO与VI) |
| 3 | IP 形象 + 文创产品 | [`作品集/02-IP形象与文创`](作品集/02-IP形象与文创) |
| 4 | 宣传物料设计 | [`作品集/03-宣传物料`](作品集/03-宣传物料) |
| 5 | 视频制作 + 品牌故事剧本 | [`作品集/04-视频与剧本`](作品集/04-视频与剧本) |
| 6 | 项目报告 | [`作品集/05-项目报告`](作品集/05-项目报告) |

---

## 小程序 Demo

一整个手机 App 的界面，全在 **一个 `index.html`** 里。下载解压，双击就能点，不用装 Node、不用装 HBuilderX、不用起本地服务器。

```
下载 → 双击 index.html → 20 个页面随便点
```

| | |
|---|---|
| 结构 | 375×812 的手机外壳，内存状态机切换 20 个页面 |
| 网络 | 无 CDN、无外链、无 fetch，**断网也能跑** |

> ⚠️ 必须**整个文件夹**一起打开。`index.html` 用相对路径引用 `assets/` 里的图片，只拷这一个 html 会满屏裂图。

### 20 个页面

| # | 页面 | 函数 | # | 页面 | 函数 |
|---|---|---|---|---|---|
| 1 | 启动页 | `splash` | 11 | 发布动态 | `publish` |
| 2 | 引导页 | `intro` | 12 | 商城 | `shop` |
| 3 | 登录 | `login` | 13 | 商品详情 | `productDetail` |
| 4 | 注册 | `register` | 14 | 购物车 | `cart` |
| 5 | 首页 | `home` | 15 | 结账 | `checkout` |
| 6 | 搜索 | `search` | 16 | 支付成功 | `paySuccess` |
| 7 | 赛事 | `race` | 17 | 个人中心 | `profile` |
| 8 | 赛道详情 | `raceDetail` | 18 | 我的订单 | `orders` |
| 9 | 社区 | `community` | 19 | 设置 | `settings` |
| 10 | 动态详情 | `postDetail` | 20 | 资讯详情 | `article` |

### 拿来改成你自己的作业

改这五处就够了，都在 `index.html` 里：

**1. 品牌名** — 全文搜索 `NIGHTLI`（34 处），全局替换成你的项目名。记得连 `<title>` 一起改。

**2. 主色** — 搜 `#f43f5e`（玫红强调色，3 处），换成你的主色。整体基调是黑 `#111` + 白 `#fff`。

**3. 图片** — `assets/images/` 里 12 张，**用同名文件覆盖**即可，不用动代码。建议宽度 800px 左右、JPG 质量 80。图标同理，`assets/icons/` 8 个 PNG，128px 以内。

**4. 文案** — 20 个 `function xxx()`，每个函数开头就是这个页面的 HTML，中文字符串直接改。

**5. 用户名** — 首页的 `Hi, Jonathan!`，换成你的名字。

### 已知限制

- **刷新回首页**。没有 `localStorage`，状态只存在内存里，加进购物车的商品刷新就没了。
- **没有深链接**。不写 `location.hash`，没法把"第 13 页"的地址发给别人。
- **登录 / 注册 / 支付全是假的**。输入框不校验，点按钮直接跳下一页。
- **图片是压缩过的展示素材**，高清原图在 Releases。

---

## 怎么用

| 你想 | 怎么做 |
|---|---|
| 看 Demo | 点上面的在线预览，或下载 ZIP 双击 `index.html` |
| 拿去做作业 | 看 [作品集 README](作品集/README.md) 里的改造建议，**务必换掉品牌名和主色** |
| 要高清原图 / 视频 | [下载 `AIGC-course-full.zip`（409 MB）](https://github.com/cecilqaq/AIGC-course-design/releases/download/v1.0/AIGC-course-full.zip) |
| 要 PSD 源文件 | [123 云盘下载](https://1816407483.share.123pan.cn/123pan/LCPqVv-F8Hkv)　718 MB，10 个 PSD/PSB 原始工程，免登录 |

## 许可证

代码部分 MIT，随意使用、修改、商用。`作品集/` 下的图片、文档、品牌设计为课程作业产出，仅作学习参考，请勿商用。
