<div align="center">

<h1>赵子强</h1>

<p><b>AI 大模型应用与 Agent 工程</b></p>

<p>把系统做成可评测、可恢复、带约束，而不是只调 Prompt。</p>

<p>
  <a href="https://github.com/Zorien-ai"><img src="https://img.shields.io/badge/GitHub-Zorien--ai-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub" /></a>
  <img src="https://img.shields.io/badge/Open%20to-AI%20大模型工程师%20/%20Agent%20开发-6d28d9?style=flat-square" alt="Open to AI 大模型工程师 / Agent 开发" />
  <img src="https://img.shields.io/badge/期望城市-一线%20/%20新一线-0b1026?style=flat-square" alt="期望城市：一线 / 新一线" />
</p>

<p>
  <a href="#-关于我">关于我</a> ·
  <a href="#-精选项目">项目</a> ·
  <a href="#-技术栈">技术栈</a> ·
  <a href="#-联系">联系</a>
</p>

</div>

---

## 👋 关于我

面向大模型应用与 Agent 工程。主项目是开源的 [千客引擎](https://github.com/Zorien-ai/qianke-engine)：入口路由、可恢复 Agent Runtime、Text2SQL 安全约束和评测闭环都在这个仓库里。

| | |
| :-- | :-- |
| 🔭 **正在做** | **[千客引擎](https://github.com/Zorien-ai/qianke-engine)**：评测口径、多商家场景与工程化迭代 |
| 🤖 **关注方向** | Agent Runtime 与 HITL、RAG / Text2SQL、评测与安全约束 |
| 🧰 **主力技术栈** | Python · FastAPI · Vue 3 · LangGraph · pgvector · pytest · GitHub Actions |
| 🌱 **求职意向** | AI 大模型工程师 / Agent 开发工程师 · 一线 / 新一线均可 · 可随时到岗 |

> 能用评测和约束写清楚的，就不要只靠模型发挥。

---

## 🚀 精选项目

### 01 · 千客引擎

[![GitHub](https://img.shields.io/badge/GitHub-qianke--engine-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Zorien-ai/qianke-engine)
![Apache-2.0](https://img.shields.io/badge/license-Apache--2.0-blue?style=flat-square)
![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=flat-square&logo=python&logoColor=white)
![Bilibili](https://img.shields.io/badge/宣传片-79s-FF6699?style=flat-square&logo=bilibili&logoColor=white)

[![千客引擎宣传片 · 79 秒](https://raw.githubusercontent.com/Zorien-ai/qianke-engine/main/docs/assets/promo-cover.jpg)](https://www.bilibili.com/video/BV1g9nJ6hEZ9)

独立开发的开源 AI 电商平台，分管理端、B 端和 C 端。底座是 RAG 与 NL2SQL 用户画像查询；C 端做陪伴和导购 Agent（长短期记忆、日记、帮用户砍价），B 端店铺助手复用同一套引擎，抽取画像、给出经营策略和营销话术，并按 SOP 处理优惠。

为把这条链路跑稳：入口由大模型分类改为微调 BERT，路由准确率 0.61 → 0.99；Text2SQL 有只读、白名单和超时约束，再用 answer_guard 拦截预测类幻觉；Runtime 可恢复，高风险动作走企业微信人工审批。

- 黄金集 33 题，覆盖 4 类角色及边界用例、共 13 种题型。最新全量通过率 **90.9%**（30/33，2026-11-11，多商家改造后）；此前 10 月 20 日快照为 93.9%，10 月 18 日单轮历史最佳为 97.0%。33 题里差 1 题约 3 个百分点，所以以最新全量为准，不把历史高点当成当前成绩。
- **751** 个 pytest 接入 GitHub Actions。
- 演示：[B 站 79 秒宣传片](https://www.bilibili.com/video/BV1g9nJ6hEZ9)

`Python` `FastAPI` `Vue 3` `LangGraph` `pgvector` `RAG` `Text2SQL` `LLM-as-a-Judge`

---

### 02 · Stillroom

[![GitHub](https://img.shields.io/badge/GitHub-stillroom-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Zorien-ai/stillroom)
![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)
![PySide6](https://img.shields.io/badge/GUI-PySide6%20%2B%20Qt%20Quick-41CD52?style=flat-square&logo=qt&logoColor=white)

判断优先的本地多模态生成工作台。你说一句需求，代码跑完六步流水线（理解需求 → 找参考 → 生成 → 评估 → 精修 → 交付），模型只回答窄问题；流程顺序、回修上限和通过条件写在代码里，数据留在本机。

`Python` `PySide6` `Local-first`

---

### 03 · dsh-jev-highlight

[![GitHub](https://img.shields.io/badge/GitHub-dsh--jev--highlight-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Zorien-ai/dsh-jev-highlight)
![MIT](https://img.shields.io/badge/license-MIT-97CA00?style=flat-square)

给 AI 长回答画重点的 DeepSeek Harness 插件：不改模型输出，只用决策模型和 CSS Custom Highlight API 在阅读时标出该看的部分。

`TypeScript` `DeepSeek Harness`

---

### 04 · github-trending-chat

[![GitHub](https://img.shields.io/badge/GitHub-github--trending--chat-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Zorien-ai/github-trending-chat)

把 GitHub Trending 装进复古 CRT 终端。零依赖 Node.js；每天 09:00（Asia/Shanghai）自动抓榜、写中文简评并归档。

`Node.js` `Automation`

<details>
<summary><b>更多项目</b></summary>

<br />

| 项目 | 一句话 |
| :-- | :-- |
| **[codex-skill-manager](https://github.com/Zorien-ai/codex-skill-manager)** | 双击即用的 Windows 小工具：查看并搬移 Codex 技能 |
| **[dsh-super-learning-architect](https://github.com/Zorien-ai/dsh-super-learning-architect)** | 把大模型从「倒课讲师」改造成苏格拉底式私教的 Agent 预设 |
| **[jev-lab](https://github.com/Zorien-ai/jev-lab)** | 最简 Jev 调用演示器：单页看清请求、概率分布、耗时与 token |
| **[codex-canvas-format-mismatch](https://github.com/Zorien-ai/codex-canvas-format-mismatch)** | Codex 渲染不了 `.canvas.tsx` 的实测取证报告 |
| **[AgnesStudio](https://github.com/Zorien-ai/AgnesStudio)** | Stillroom 的早期版本（历史归档，不再作为代表作） |

</details>

---

## 🛠 技术栈

| 方向 | 具体能力 |
| :-- | :-- |
| **大模型应用** | RAG（解析 / 切分 / 混合检索 / 精排 / 引用溯源）· Text2SQL（只读约束、白名单、超时）· 幻觉拦截 · LLM-as-a-Judge 评测 |
| **Agent 工程** | LangGraph 编排 · 可恢复 Runtime（checkpoint / interrupt / retry / 预算）· HITL 审批 · 多租户与权限隔离 |
| **工程与评测** | pytest 与 GitHub Actions 门禁 · 黄金集回归 · 评测快照留档，不以历史高点代替最新结果 |
| **其他** | Vue 3 · FastAPI · pgvector · 本地桌面工具（PySide6）· 自动化流水线 |

---

## 📬 联系

- **GitHub**：[@Zorien-ai](https://github.com/Zorien-ai)
- **邮箱**：q93304989@gmail.com · 747055153@qq.com
- **求职方向**：AI 大模型工程师 / Agent 开发工程师。欢迎 issue 或邮件。

---

<div align="center">

<sub>最后整理于 2026-11-12</sub>

</div>
