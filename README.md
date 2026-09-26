# StyleForge

**一个用于沉淀个人 UI 审美、提炼设计规则，并将其应用到 AI 辅助前端开发中的风格知识系统。**

StyleForge 的目标不是再做一个 Prompt Collection，也不是简单收集“好看的网站”。

它希望建立一套长期可维护的个人 UI 风格知识库：从优秀案例中提取结构化设计规律，由人进行筛选、归纳与组合，再把这些规则交给 Codex、GPT、Claude 等 AI 执行，让 AI 生成的界面逐渐摆脱默认、趋同的“AI 味”，形成更稳定、更有个人特点的视觉语言。

## 项目动机

这个项目来自一个很具体的问题。

在之前使用 AI 完成课程项目前端时，我发现 AI 生成的界面虽然通常结构完整、视觉上也不算差，但不同项目之间越来越容易出现相似的风格：

- 类似的 Hero Section；
- 类似的圆角卡片；
- 类似的渐变与阴影；
- 类似的留白与排版；
- 类似的 SaaS / Landing Page 视觉语言。

结果是：页面“看起来像一个合格的 AI 生成页面”，但缺少自己的设计特点，也容易产生审美疲劳。

后来看到 Bilibili 视频 **BV1TNaP6MEUJ**，其中“收集优秀网站 → 分析设计 → 提取规律 → 建立知识 → 再用于 AI 生成”的思路给了我直接启发。

StyleForge 在此基础上进一步扩展：

> 不只是模仿已有优秀案例，而是把案例当作学习材料，逐步提炼出属于自己的设计语言。

## 核心思想

StyleForge 中，AI 应该承担两类角色：

1. **Analyzer**：帮助拆解优秀设计，提取可复用规律；
2. **Executor**：根据已经明确的风格规则生成界面。

但最终的审美判断仍然由人完成。

也就是说：

```text
优秀案例
   ↓
结构化分析
   ↓
Style Knowledge
   ↓
人工筛选 / 修改 / 组合
   ↓
Personal Style
   ↓
Prompt / Design Tokens / Rules
   ↓
AI 生成前端
   ↓
人工评价
   ↓
反向更新 Style Library
```

## 核心目标

- 建立可持续积累的 UI Reference Library。
- 把“这个网站很好看”转化成可描述、可比较、可复用的设计参数。
- 提炼 Typography、Color、Layout、Spacing、Component、Motion 等维度的设计规则。
- 区分“案例中的客观特征”和“我真正喜欢的部分”。
- 形成可组合的个人 Style Profile。
- 将 Style 转换为 AI 可执行的 Prompt、Design Tokens、前端约束或其他结构化输入。
- 让 AI 更像执行设计规则的工具，而不是默认审美的来源。
- 通过实际生成结果持续反向校正风格知识库。

## 当前阶段

**Phase 0 — 风格表示与知识结构探索。**

当前最重要的问题不是做 Web UI，而是先回答：

- 一个 UI 风格应该如何被结构化表示？
- 哪些维度值得记录？
- 哪些属性可以量化？
- 怎样区分“设计事实”和“主观偏好”？
- 怎样从多个优秀案例中抽象出共性？
- 怎样把抽象后的风格重新转化成 AI 能稳定执行的约束？

## 文档

- [项目愿景](docs/VISION.md)
- [开发路线](docs/ROADMAP.md)
- [架构说明](docs/ARCHITECTURE.md)
- [参考资料](docs/REFERENCES.md)
- [设计决策](docs/DECISIONS.md)
- [AGENTS.md](AGENTS.md) — Codex / AI Coding Agent 项目上下文

## License

项目代码采用 [MIT License](LICENSE)。

案例截图、第三方网站内容、字体、图片等参考素材仍属于各自原作者或权利人。StyleForge 应优先保存分析结果、元数据与引用信息，而不是未经许可重新分发第三方素材。
