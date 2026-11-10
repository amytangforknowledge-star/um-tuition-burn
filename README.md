<div align="center">

# 🔥 UM Tuition Burn
### 澳门大学学费燃烧计时器 · University of Macau Tuition Countdown

**今天这节课，究竟值多少钱？**  
*How much does a minute in class cost — hypothetically?*

把学费按照排定的课堂时间折算成每秒金额；上课时，看着数字实时跳动。

[**🌐 在线体验 / Live Demo**](https://is.gd/UMMoneyBurn26) · [**直接打开网站**](https://amytangforknowledge-star.github.io/um-tuition-burn/) · [**反馈 Issues**](https://github.com/amytangforknowledge-star/um-tuition-burn/issues)

**开源免费 · 无需登录 · 手机电脑都能用**

</div>

> [!IMPORTANT]
> **非官方独立趣味项目。** 本站与澳门大学（University of Macau）无官方隶属、认证、授权或合作关系。所谓“学费燃烧”只是按课堂时间分摊学费的**数学模拟**，不代表学校按秒收费、真实教学成本、财务账单或退款依据。金额和课程安排因人而异，请谨慎填写、解读和传播。设计或功能如与其他作品相似，**如有雷同，纯属巧合**；但该声明不替代应有的知识产权授权。

![UM Tuition Burn 网站桌面预览](assets/preview.png)

## ✨ 功能 · Features

| 功能 | 说明 |
| --- | --- |
| ⏳ **下课倒计时** | 上课中显示距离下课的剩余时间；不在课堂时显示下一节课倒计时 |
| 💸 **实时学费滚动** | 只在有效授课时段累计折算金额，下课自动暂停 |
| 📚 **自定义课表** | 第一、第二学期分别配置每周课程数（1–16 节）、星期与开始时间 |
| 💰 **自行输入学费** | 修改第一学年学费与两学期分配比例，默认金额仅为参考示例 |
| 📅 **假期识别** | 按 2026/27 预置校历排除部分假期，并支持输入个人停课日 |
| ⚡ **10 倍速演示** | 未上课也能模拟金额跳动，演示模式有明确标记 |
| 🔗 **保存与分享** | 浏览器本地保存配置，支持生成带个人配置的分享链接 |
| 📱 **手机与桌面端** | 响应式布局，使用澳门时区 Asia/Macau |

**特别说明：** 当前澳大版本每节课固定 **170 分钟（2 小时 50 分钟）**，**尚不能单独修改某一节课的时长**；学期起止日期也固定为 2026/27，未自动更新至其他学年。它不是适合所有专业的统一课时模板。

## 🚀 如何使用 · Quick Start

1. 打开 **[UM Tuition Burn → https://is.gd/UMMoneyBurn26](https://is.gd/UMMoneyBurn26)**。
2. 输入你的**实际第一学年学费**，配置第一与第二学期的每周课数、星期和开课时间；必要时补充停课日期。
3. 保存设置，返回首页查看**实时等效学费、每秒速率与课堂倒计时**；点击「课堂演示」可以提前预览效果。

**分享注意：** 只分享上方基础网址，其他人会自行设置；使用页面内的「分享」功能生成个人配置链接时，你填写的学费、课程名称、课表等会通过 URL 片段传给收件人。**不要在分享配置里填隐私信息。**

## 🧮 计算口径 · Methodology

本项目使用“学费按有效课堂时间分摊”的娱乐性口径，而不是实际成本会计：

- 每学期排定的有效课次数 × **170 × 60 秒** = 该学期有效授课秒数。
- 分配到该学期的学费 ÷ 该学期有效授课秒数 = **该学期每秒等效金额**。
- 两学期分别计算后，将已经发生的有效上课秒数对应金额累计；非上课时间不增长。
- 预置的部分假期和用户添加的停课日从课程次数中排除；实际补课、实习、考试等需由使用者自行核对。

由于两学期课程总量可能不同，**每秒费率不一定相同**。

当前默认 **MOP 87,000/第一学年**，仅作为开发时参考的 **2026/27 普通两年制非本地硕士**情景，并非全校统一学费。请以个人实际费用通知与所属课程安排为准。本模型不实际核算图书馆、研究设施、GPU 或其他学校支出。

## 🗓 校历与参考资料 · References

- [澳门大学 2026/27 暂定校历 / University Almanac](https://reg.um.edu.mo/download/pub-doc/Almanac/University%20Almanac_AY2627.pdf)
- [澳门大学 2026/27 研究生学费文件 / Postgraduate Tuition Fees](https://grs.um.edu.mo/wp-content/uploads/Postgraduate-Tuition-Fees-26-27-EN.pdf)

**提醒：** 校历可能发生修订，不同学位、专业或课程可能有例外。本网站不会自动连接澳大教务系统更新排课与假期；请以学校最新公告为准。

## 🔐 隐私与使用费用 · Privacy

- **纯前端静态网页**：计时与金额计算在访问者自己的浏览器内完成，无付费 AI Token、GPU 计算或业务后端。
- **无需账号**：设置保存在浏览器的 `localStorage` 中，清理网站数据可能导致设置丢失。
- **无专用个人数据收集服务器**：项目本身未接入数据库、用户画像或广告跟踪；GitHub Pages 和短链接提供方仍可能按各自政策记录访问日志。
- **没有实际扣款**：金额跳动不涉及付款、收取学费或银行交易。

## 💻 本地运行与开源协作 · Development

下载源码后打开 `index.html`，或在项目文件夹运行：

```bash
python3 -m http.server 8000
```

然后在浏览器访问 `http://localhost:8000/`。无需 Node.js、数据库、API 密钥或安装依赖。

```text
um-tuition-burn/
├── index.html           # 页面结构
├── assets/
│   ├── app.js           # 课程、校历和实时计算
│   ├── style.css        # UI 与响应式样式
│   ├── favicon.svg      # 网站图标
│   └── preview.png      # 项目预览
├── README.md
└── LICENSE              # MIT
```

欢迎通过 [GitHub Issues](https://github.com/amytangforknowledge-star/um-tuition-burn/issues) 反馈错误，或提交 Pull Request。建议重点改善**自定义课时、校历维护、补课与课程异动**；涉及学费与学校日期的修改，请附官方来源。

## ⚖️ License & Disclaimer

项目使用 **MIT License** 开源，可在遵守许可条款并保留相应声明的前提下使用、修改及再分发。不使用澳大官方徽标。**“如有雷同，纯属巧合”并不能免除著作权、商标等相关法律义务。**

**本工具旨在娱乐、时间管理与计算可视化，不用于学费决策、收费争议或财务凭证。**

---

<div align="center"><sub>Made for curious students · 学费在跳，知识也要涨 📚</sub></div>
