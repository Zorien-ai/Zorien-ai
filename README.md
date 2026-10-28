<div align="center">

<h1>Zorien Zhao</h1>

<p><b>AI Agent 工具链 · 多模态本地应用 · 自动化</b></p>

<p>
  <a href="https://github.com/Zorien-ai"><img src="https://img.shields.io/badge/GitHub-Zorien--ai-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
  <img src="https://img.shields.io/badge/Shenzhen-China-0b1026?style=for-the-badge&logo=googlemaps&logoColor=22d3ee" alt="Shenzhen, China" />
  <img src="https://img.shields.io/badge/Open%20to-AI%20%2F%20LLM%20roles-6d28d9?style=for-the-badge" alt="Open to AI / LLM roles" />
</p>

<p>
  <b>简体中文</b> ·
  <a href="#-关于我">关于我</a> ·
  <a href="#-精选项目">项目</a> ·
  <a href="#-技术栈">技术栈</a> ·
  <a href="#-每日自动化">自动化</a> ·
  <a href="#-联系">联系</a>
</p>

</div>

---

## 👋 关于我

中文技术开发者，长期关注 **AI Agent 生态与多模态应用**。偏好做「小而完整、装完就能用」的本地工具——不需要 GPU、不需要服务器、不需要注册账号，双击就能跑起来。

| | |
| :-- | :-- |
| 🔭 **正在做** | **[dsh-jev-highlight](https://github.com/Zorien-ai/dsh-jev-highlight)** —— 给 AI 的长回答画重点的 DSH 插件 · **[Stillroom](https://github.com/Zorien-ai/stillroom)** —— 判断优先的本地多模态生成工作台 |
| 🤖 **关注方向** | 编码代理的 Skill 与 harness 编排 · Agent 记忆与长期档案机制 · 多模态生成 API 的工程化封装 |
| 🧰 **主力技术栈** | Python · JavaScript / Node.js · C# / .NET 8 · YAML（Agent 预设与 Skills） |
| 🌱 **在折腾** | 把重复的信息整理交给自动化流水线，人只处理「值得判断」的那部分 |
| 📍 **坐标** | 深圳 Shenzhen · 开放 AI / LLM 方向机会 |

> 一句话概括我的偏好：**能用代码写死的流程，就不要交给模型猜。**

---

## 🚀 精选项目

### 01 · dsh-jev-highlight

[![GitHub](https://img.shields.io/badge/GitHub-dsh--jev--highlight-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Zorien-ai/dsh-jev-highlight)
![MIT](https://img.shields.io/badge/license-MIT-97CA00?style=flat-square)
![Node.js](https://img.shields.io/badge/Node.js-%E2%89%A520-339933?style=flat-square&logo=node.js&logoColor=white)

**给 AI 的长回答画重点。** 一个运行在 DeepSeek Harness 里的开源插件：它不修改 AI 的输出，只在阅读时把回答里「最该看的部分」高亮出来。

[![dsh-jev-highlight 高亮效果](https://raw.githubusercontent.com/Zorien-ai/dsh-jev-highlight/main/docs/assets/demo-highlights.png)](https://github.com/Zorien-ai/dsh-jev-highlight)

- 用 **StartLux / Jev** 决策模型判断段落、列表、代码块、表格行的重要程度；
- 用 **CSS Custom Highlight API** 上色，页面节点一个都不动；
- 支持设置页配置 Key、思考模式与三档阈值；
- MIT 开源，从想法到可用版只花了不到两周。

`DeepSeek Harness` `StartLux` `TypeScript` `CSS Custom Highlight API`

---

### 02 · Stillroom

[![GitHub](https://img.shields.io/badge/GitHub-stillroom-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Zorien-ai/stillroom)
![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
![PySide6](https://img.shields.io/badge/GUI-PySide6%20%2B%20Qt%20Quick-41CD52?style=flat-square&logo=qt&logoColor=white)
![Local First](https://img.shields.io/badge/data-100%25%20local-44cc11?style=flat-square)

**判断优先的本地多模态生成工作台。** 你只说一句需求，代码跑完六步流水线，模型只回答窄问题。

```text
理解需求 → 找参考 → 生成 → 评估 → 精修 → 交付
   ↑                    ↑      ↑
   └ 判断链（Jev）      └ 预算 / 白名单 / 审批 / 限流都在这一层强制生效
```

流程顺序、回修上限、通过条件都写死在代码里；参考来源分三层（历史作品 / 用户知识库 / 联网兜底）；数据留在本机 SQLite，密钥不进云端。

`Python` `PySide6` `Local-first` `MCP`

---

### 03 · 千客引擎

[![GitHub](https://img.shields.io/badge/GitHub-qianke--engine-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Zorien-ai/qianke-engine)
![Apache-2.0](https://img.shields.io/badge/license-Apache--2.0-blue?style=flat-square)
![Bilibili](https://img.shields.io/badge/%E5%AE%A3%E4%BC%A0%E7%89%87-79s-FF6699?style=flat-square&logo=bilibili&logoColor=white)

[![千客引擎宣传片 · 79 秒](https://raw.githubusercontent.com/Zorien-ai/qianke-engine/main/docs/assets/promo-cover.jpg)](https://www.bilibili.com/video/BV1g9nJ6hEZ9)

**面向电商的「数据 + 知识」双轨问答引擎。** 把订单 CSV 和业务规则 Markdown 拖进来，系统自动清洗、识别字段、构建用户画像与文档索引；业务人员用一句中文提问，就能拿到**带引用来源**的答案。

- 意图路由：知识问答走混合检索，统计问题走 Text2SQL；
- 画像池与文档池分池召回，关键结论必须带 `[来源N]`；
- 多租户 + 私有化部署，33 道业务黄金题、LLM-as-a-Judge 通过率 **97.0%**。

`Python` `FastAPI` `Vue 3` `pgvector` `RAG`

---

### 04 · github-trending-chat

[![GitHub](https://img.shields.io/badge/GitHub-github--trending--chat-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Zorien-ai/github-trending-chat)
![Node.js](https://img.shields.io/badge/Node.js-%E2%89%A520-339933?style=flat-square&logo=node.js&logoColor=white)
![Zero Dependencies](https://img.shields.io/badge/dependencies-0-44cc11?style=flat-square)

**把 GitHub Trending 装进一台复古 CRT 终端。** 零依赖 Node.js，磷光绿扫描线 + 瀑布入场动效；支持 `daily / weekly / monthly` 切换与 vim 式键盘导航。后端做了 ETag / 304、single-flight、SWR 和失败冷却。

每天 09:00（GMT+8）自动抓取、生成中文简评并归档到仓库。

`Node.js` `Vanilla JS` `Automation`

---

<details>
<summary><b>更多项目</b></summary>

<br />

| 项目 | 一句话 |
| :-- | :-- |
| **[codex-skill-manager](https://github.com/Zorien-ai/codex-skill-manager)** | 双击即用的 Windows 小工具：三列查看并双向搬移 Codex 技能 |
| **[dsh-super-learning-architect](https://github.com/Zorien-ai/dsh-super-learning-architect)** | 把大模型从「倒课讲师」改造成苏格拉底式私教的 Agent 预设 |
| **[jev-lab](https://github.com/Zorien-ai/jev-lab)** | 最简 Jev 调用演示器：单页看清请求、概率分布、耗时与 token |
| **[codex-canvas-format-mismatch](https://github.com/Zorien-ai/codex-canvas-format-mismatch)** | Codex 渲染不了 `.canvas.tsx` 的实测取证报告 |
| **[AgnesStudio](https://github.com/Zorien-ai/AgnesStudio)** | Stillroom 的早期版本（历史归档） |

</details>

---

## 🛠 技术栈

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white" alt="C#" />
  <img src="https://img.shields.io/badge/.NET%208-512BD4?style=flat-square&logo=dotnet&logoColor=white" alt=".NET 8" />
  <img src="https://img.shields.io/badge/PySide6-41CD52?style=flat-square&logo=qt&logoColor=white" alt="PySide6" />
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite" />
  <img src="https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white" alt="PowerShell" />
  <img src="https://img.shields.io/badge/YAML-CB171E?style=flat-square&logo=yaml&logoColor=white" alt="YAML" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git" />
</p>

| 方向 | 具体能力 |
| :-- | :-- |
| **AI / Agent 工程** | 多模态生成 API 封装 · MCP 工具协议 · Skill 与 Agent 预设编排 · 长期记忆 · 本地 RAG · 提示词评测与版本化 |
| **桌面应用** | PySide6 + Qt Quick · CustomTkinter · PyInstaller 单文件 / onedir 打包 |
| **工程与自动化** | 零依赖 Node 服务 · 定时流水线（抓取 → AI 加工 → 归档 → 通知）· SQLite 存储与检索 · ETag / single-flight / SWR |
| **跨栈经验** | Windows 原生工具链（GDI / 注册表 / ctypes）· Git 仓库治理 · 中英文技术文档 |

---

## ⚡ 每日自动化

把「看趋势」这件事交给流水线，每天 09:00（GMT+8）自动运行：

<details>
<summary><b>展开流水线细节</b></summary>

<br />

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

几个刻意的取舍：

- **时区锁死 `Asia/Shanghai`**：避免跨时区机器把 09:00 的榜归档到前一天；
- **内容与已归档文件一致时跳过提交**：不制造空 commit；
- **归档与简评合并成一个 commit**：不留碎提交。

归档成果：[历史 GitHub 日榜汇总](https://github.com/Zorien-ai/github-trending-chat/tree/main/%E5%8E%86%E5%8F%B2github%E6%97%A5%E6%A6%9C%E6%B1%87%E6%80%BB)。

</details>

---

## 📬 联系

- **GitHub**：[@Zorien-ai](https://github.com/Zorien-ai)
- **邮箱**：q93304989@gmail.com（推荐）· 747055153@qq.com
- **合作方向**：AI Agent 工具链 · 多模态应用工程化 · 桌面端 AI 工具 · 本地优先的自动化流程。欢迎 issue 或邮件。

---

<div align="center">

<sub>最后整理于 2026-10-28 · 由每日 GitHub Trending 流水线维护的部分见上方归档</sub>

</div>
