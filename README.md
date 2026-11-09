# UM Tuition Burn · 学费燃烧计时器

一个免费的、开源的 **澳门大学 2026/27 学年学费倒计时网页**。根据实际授课时间，将学期学费折算为每秒课堂成本，展示实时「学费燃烧」金额与距离下课的倒计时。

> **非官方学生趣味项目**：不隶属于澳门大学。学费按课堂时间折算仅是娱乐性估算，**不代表学校按秒计费**，亦不代表学费仅用于课堂教学。2026/27 校历为暂定版，遇校历变化需更新源代码。

![桌面截图](assets/preview.png)

## 在线体验

将此仓库公开并启用 GitHub Pages 后，网站会出现在：

`https://<你的 GitHub 用户名>.github.io/<仓库名>/`

如果仓库名为 `um-tuition-burn`，且用户名为 `amytangforknowledge-star`，预期地址为：

`https://amytangforknowledge-star.github.io/um-tuition-burn/`

**以上是预期地址，需要部署成功后才生效。**

## 功能

- 上课期间实时累计等效学费，其他时段停止；支持 10× 课堂演示（明确标注模拟）
- 距离下课或下一节课的动态倒计时
- 默认单节 170 分钟（2 小时 50 分钟）
- 自定义第一学年学费、第一学期比例、两个学期每周节数、星期与开始时间
- 默认过滤 2026/27 校历列出的部分假期；可另行输入个人停课日
- 课表保存在浏览器本地；可通过包含配置的 URL 片段分享
- 按澳门时区 Asia/Macau 计时；响应式设计，支持手机

## 0 成本发布到 GitHub Pages

1. 登录 GitHub，创建一个新的仓库，建议名称为 **`um-tuition-burn`**。
2. 选择 **Public**（公开）。GitHub Free 对公开仓库提供 Pages 托管。
3. 打开仓库主页，使用 **Add file → Upload files**，将本仓库**解压后**的 `index.html`、`assets/`、`README.md`、`LICENSE`、`.nojekyll` 上传到仓库根目录（不是再包一层文件夹）。注意：浏览器上传有时不显示隐藏文件 `.nojekyll`，该文件对本项目不是强制的，可跳过。
4. 点击 **Commit changes**。
5. 进入 **Settings → Pages → Build and deployment**，将 **Source** 选为 `Deploy from a branch`，**Branch** 选 `main`，**Folder** 选 `/(root)`，点击 **Save**。
6. 部署完成后进入 **Settings → Pages → Visit site** 查看公开网址。初次部署可能需等待数分钟。

官方说明：[GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site) · [发布来源设置](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

### 更简单的方式：单文件发布

如果你不想上传多个文件，也可以使用单文件版本 `UM_Tuition_Burn_2026-27_正式版.html`，在 GitHub 创建名为 `index.html` 的新文件，粘贴全部内容即可。**本仓库采用分离 HTML/CSS/JS 的结构，更适合开源协作和维护。**

## 本地运行

直接打开 `index.html`，或者在本目录执行：

```bash
python3 -m http.server 8000
```

然后访问 http://localhost:8000 。无需 Node、npm、数据库、服务器或 API 密钥。

## 文件结构

```text
um-tuition-burn/
├── index.html            # HTML 页面结构
├── assets/
│   ├── app.js            # 计时与学费计算、课表和本地分享
│   ├── style.css         # 桌面与手机布局样式
│   ├── favicon.svg       # 网站图标
│   └── preview.png       # 项目预览图
├── .nojekyll             # 直接静态发布
├── LICENSE               # MIT 开源许可证
└── README.md             # 说明、部署方法
```

## 计算逻辑

每学期有效授课总时长：

`该学期每节课 10,200 秒 × 该学期排定的有效课程数`

每秒等效学费：

`该学期分配的学费 ÷ 该学期有效授课总秒数`

只对已发生的有效授课秒数计价；实时累计为两个学期分别计算后的总和。课表日期、开始时间和假期名单由浏览器端 JavaScript 计算。

计算结果取决于课表真实性、停课安排、实践活动及个人收费标准。它不是财务账单、学校学分收费规则或实际教学成本评估。

## 数据隐私

- **无后端、无账户、无埋点和广告代码**。课表数据保存在你自己的浏览器 `localStorage` 中。
- 点击「分享」时，课表和学费会被序列化到网址 `#p=...` 中。**任何拿到分享链接的人都能看到这些参数**，不要在课程名称里填写私人敏感信息。
- 不使用大学的官方标志。本项目名称提及 University of Macau 仅用于说明所参考的大学及学年。

## 参考来源

- [澳门大学 2026/27 暂定校历](https://reg.um.edu.mo/download/pub-doc/Almanac/University%20Almanac_AY2627.pdf)
- [澳门大学 2026/27 研究生学费标准](https://grs.um.edu.mo/wp-content/uploads/Postgraduate-Tuition-Fees-26-27-EN.pdf)

## 许可

MIT License — 允许保留版权及许可声明的情况下自由使用、修改与再分发。欢迎通过 GitHub Issues / Pull Requests 提交更新。
