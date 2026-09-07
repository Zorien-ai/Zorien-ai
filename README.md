<div align="center">

<svg width="900" height="220" viewBox="0 0 900 220" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="ZZQ3208 - AI Agent Tooling and Automation">
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#0b1026"/>
      <stop offset="52%" stop-color="#1b2a6b"/>
      <stop offset="100%" stop-color="#6d28d9"/>
    </linearGradient>
    <linearGradient id="accent" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#22d3ee"/>
      <stop offset="100%" stop-color="#a78bfa"/>
    </linearGradient>
    <radialGradient id="glow" cx="0.82" cy="0.15" r="0.65">
      <stop offset="0%" stop-color="#22d3ee" stop-opacity="0.38"/>
      <stop offset="100%" stop-color="#22d3ee" stop-opacity="0"/>
    </radialGradient>
  </defs>

  <rect width="900" height="220" fill="url(#bg)"/>
  <rect width="900" height="220" fill="url(#glow)"/>

  <g stroke="#ffffff" stroke-opacity="0.06" stroke-width="1">
    <path d="M120 0 V220 M240 0 V220 M360 0 V220 M480 0 V220 M600 0 V220 M720 0 V220 M840 0 V220"/>
    <path d="M0 60 H900 M0 120 H900 M0 180 H900"/>
  </g>

  <rect x="0" y="0" width="6" height="220" fill="url(#accent)"/>

  <text x="60" y="108" font-family="'Segoe UI','PingFang SC','Microsoft YaHei',Helvetica,Arial,sans-serif" font-size="62" font-weight="700" fill="#ffffff" letter-spacing="2">ZZQ3208</text>

  <text x="62" y="150" font-family="'Segoe UI','PingFang SC','Microsoft YaHei',Helvetica,Arial,sans-serif" font-size="19" font-weight="400" fill="#a5b4fc" letter-spacing="1">AI Agent Tooling · Automation · Developer Experience</text>

  <rect x="60" y="172" width="300" height="4" rx="2" fill="url(#accent)"/>

  <text x="62" y="204" font-family="'Segoe UI','PingFang SC','Microsoft YaHei',Helvetica,Arial,sans-serif" font-size="14" font-weight="400" fill="#7c8db5" letter-spacing="0.5">Building small tools that make agents easier to live with.</text>
</svg>

</div>

## 👋 关于我

中文技术开发者，关注 **AI Agent 生态与编码代理工具链**，喜欢做那种「小而完整、装完就能用」的工具。

- 🔭 **正在做**：GitHub 日榜每日自动归档 —— 每天 09:00 抓榜 → AI 逐仓库简评 → 归档进仓库并推送 → 邮件送达
- 🛠 **常用技术栈**：JavaScript / Node.js · C# / .NET 8 · YAML（Agent 预设与 Skills）
- 🤖 **关注方向**：编码代理（Codex / Claude Code 等）的技能与 harness 编排、Agent 记忆与长期档案机制
- 🌱 **在折腾**：把重复的信息整理工作交给自动化，让每天只处理「值得判断」的部分
- 📫 **联系方式**：747055153@qq.com

---

## 🚀 项目

### [github-trending-chat](https://github.com/q93304989-bit/github-trending-chat)

![Node.js](https://img.shields.io/badge/Node.js-%E2%89%A520-339933?style=flat-square&logo=node.js&logoColor=white)
![Zero Dependencies](https://img.shields.io/badge/dependencies-0-44cc11?style=flat-square)
![Tests](https://img.shields.io/badge/tests-31%20passing-brightgreen?style=flat-square)

**把 GitHub Trending 装进一台复古 CRT 终端。**

零依赖实现 —— 只用 Node 内置模块和原生 HTML / CSS / JS，没有构建步骤，克隆下来直接跑。前端是磷光绿扫描线 + 瀑布入场动效的终端界面，支持 `daily / weekly / monthly` 切换和 vim 式 `J / K / Enter / C` 键盘导航；后端在缓存上下了不少功夫：ETag / 304 协商缓存、single-flight 合并并发请求、SWR 过期先回旧数据、失败后 30s→5min 指数冷却，不会把 GitHub 打疼。

配套一条每日自动化流水线：抓取榜单 → 解析 → 生成 markdown → AI 给每个仓库写一句中文简评 → 按 `年 / 月 / 日` 归档 → 推送 GitHub → 发邮件通知。

> 📁 归档成果： [历史github日榜汇总](https://github.com/q93304989-bit/github-trending-chat/tree/main/%E5%8E%86%E5%8F%B2github%E6%97%A5%E6%A6%9C%E6%B1%87%E6%80%BB)

---

### [codex-skill-manager](https://github.com/q93304989-bit/codex-skill-manager)

![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white)
![.NET 8](https://img.shields.io/badge/.NET-8.0-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Platform](https://img.shields.io/badge/platform-Windows-0078D6?style=flat-square&logo=windows&logoColor=white)

**一个双击即用、不用装任何环境的 Windows 小工具，管理 Codex 技能在哪里生效。**

技能散落在全局目录和各个项目目录里，手动搬来搬去既麻烦又容易出错。这个工具把三列 —— 全局技能、系统内置（锁定）、项目技能 —— 摊开在一个窗口里，选中就能双向搬：项目 → 全局、全局 → 项目，或者停用 / 启用。

几个设计上的坚持：系统内置技能（`.system`）和原生插件目录**只读锁定，绝不触碰**；每个动作执行前都弹窗确认；「停用」只是把 `SKILL.md` 改名成 `SKILL.md.disabled`（Codex 会递归扫描，单纯移动文件夹并不能让它失效），随时能改回来。界面中英文可切换。

---

### [dsh-super-learning-architect](https://github.com/q93304989-bit/dsh-super-learning-architect)

![Agent Preset](https://img.shields.io/badge/DSH-Agent%20Preset-4D6BFE?style=flat-square)
![Skills](https://img.shields.io/badge/skills-2-orange?style=flat-square)

**超级学习架构师 —— 一个把大模型从「一次性倒完课的讲师」改造成苏格拉底式私教的 Agent 预设。**

针对八个常见痛点做了针对性设计：讲完立刻追问而不是一屏塞完、按「识记 → 理解 → 应用」三层出题并且判卷讲错因、用长期记忆存学生档案实现跨会话不健忘、用待办到期做近似间隔复习、每个术语都配一个「10 岁孩子也能懂」的比喻，以及 —— 图表用 matplotlib 生成真实图形后**直接显示在对话里**，而不是丢一个文件路径。

预设层基于 DSH 标准工具集，只替换 persona 人设；技能层是两本可加载的操作手册：`socratic-tutor`（诊断话术、判卷量表、避坑清单）与 `socratic-charts`（配色规范、中文字体、对话内嵌图）。纯文件安装，复制即可，无需重启。

---

## ⚡ 每日自动化

把「看趋势」这件事整个交给了流水线，每天 09:00（GMT+8）自动跑一遍：

```text
09:00  抓取 GitHub Trending (since=daily)
         │  失败自动重试 3 次
         ▼
       解析 → 生成 markdown
         ▼
       AI 为每个仓库写一句中文简评 → 写回归档文件
         ▼
       git commit → push 到 GitHub
         ▼
       发送日报邮件（Top 5 增速 + 看点速览 + 完整榜单链接）
```

设计上几个刻意的取舍：时区锁死 `Asia/Shanghai`，避免跨时区机器把 09:00 的榜归档到前一天；内容与已归档文件一致时跳过提交，不制造空提交；归档与简评合并成一个 commit，不留碎提交。

---

## 📊 GitHub 数据

<p>
  <img src="https://img.shields.io/github/followers/q93304989-bit?style=for-the-badge&color=1b2a6b&labelColor=0b1026&logo=github&logoColor=22d3ee" alt="Followers" />
  <img src="https://img.shields.io/github/stars/q93304989-bit/github-trending-chat?style=for-the-badge&label=github-trending-chat&color=1b2a6b&labelColor=0b1026&logo=github&logoColor=22d3ee" alt="github-trending-chat stars" />
  <img src="https://img.shields.io/github/stars/q93304989-bit/codex-skill-manager?style=for-the-badge&label=codex-skill-manager&color=1b2a6b&labelColor=0b1026&logo=github&logoColor=22d3ee" alt="codex-skill-manager stars" />
  <img src="https://img.shields.io/github/stars/q93304989-bit/dsh-super-learning-architect?style=for-the-badge&label=dsh-super-learning-architect&color=1b2a6b&labelColor=0b1026&logo=github&logoColor=22d3ee" alt="dsh stars" />
</p>

<p>
  <img src="https://img.shields.io/github/last-commit/q93304989-bit/github-trending-chat?style=for-the-badge&label=last%20commit&color=6d28d9&labelColor=0b1026&logo=github&logoColor=a78bfa" alt="Last Commit" />
  <img src="https://img.shields.io/github/repo-size/q93304989-bit/github-trending-chat?style=for-the-badge&color=6d28d9&labelColor=0b1026&logo=github&logoColor=a78bfa" alt="Repo Size" />
</p>

### 提交贡献图

<div align="center">
  <img src="https://ghchart.rshah.org/7c3aed/q93304989-bit" alt="Contribution Graph" width="840" />
</div>

---

## 🧰 技术栈

<p>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white" alt="C#" />
  <img src="https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt=".NET" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/YAML-CB171E?style=for-the-badge&logo=yaml&logoColor=white" alt="YAML" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
</p>

---

<div align="center">

由 [github-trending-chat](https://github.com/q93304989-bit/github-trending-chat) 的每日归档流水线持续更新 · 最后更新 2026-09-07

</div>
