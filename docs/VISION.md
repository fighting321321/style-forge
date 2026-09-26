# 项目愿景

## 背景

AI 已经能够快速完成大量前端开发工作，但“能生成页面”和“能形成具有个人特点的视觉语言”是两个不同的问题。

在实际课程项目中，AI 生成的前端通常具备：

- 完整布局；
- 合理的信息层级；
- 基本可用的交互；
- 看起来“现代”的视觉效果。

但当多个项目都依赖类似的默认生成方式后，很容易出现明显的风格趋同。

常见表现包括：

- 大标题 + 副标题 + CTA 的标准 Hero；
- 大量圆角卡片；
- 柔和渐变；
- 统一的阴影；
- 类似的留白策略；
- 类似的 SaaS Dashboard 或 Landing Page 审美。

这些设计单独看不一定差，但大量重复后会失去作者性。

## 问题

真正的问题不是：

> “怎样让 AI 生成更漂亮的 UI？”

而是：

> “怎样让 AI 生成的 UI 更稳定地体现我自己的审美选择？”

如果只依赖自然语言 Prompt，例如：

- 更高级；
- 更现代；
- 更极简；
- 更有设计感；

这些描述通常过于模糊，AI 最终仍会回到高频默认设计模式。

因此，需要建立比 Prompt 更底层、更稳定的设计知识表示。

## 灵感

Bilibili 视频 **BV1TNaP6MEUJ** 提供了重要启发：

```text
收集优秀案例
→ AI 分析
→ 提取设计规律
→ 建立知识
→ 再让 AI 使用这些知识生成
```

StyleForge 对这条路径做进一步扩展。

项目不希望停留在“学习并模仿优秀网站”，而希望把大量案例当作设计学习资料，通过长期筛选与归纳形成：

> **Personal UI Style System**

## 核心思想

一个完整闭环应当是：

```text
Reference
   ↓
Observation
   ↓
Structured Style Data
   ↓
Human Curation
   ↓
Personal Style Profile
   ↓
Prompt / Tokens / Rules
   ↓
AI Implementation
   ↓
Visual Evaluation
   ↓
Knowledge Update
```

这里每一步承担不同职责。

### Reference

提供真实优秀案例，而不是凭空描述风格。

### Observation

尽量客观记录：

- 字体；
- 尺寸；
- 间距；
- 对齐；
- 色彩；
- 密度；
- 组件；
- 动效。

### Structured Style Data

把观察结果转换成可以比较、筛选和复用的数据。

### Human Curation

决定：

- 哪些部分值得学习；
- 哪些不适合自己；
- 哪些规则可以组合；
- 哪些设计只适用于特定场景。

### AI Implementation

AI 根据已经明确的规则完成实现，而不是自己寻找一个“默认好看”的方案。

## 需要区分的三类信息

StyleForge 应特别区分：

### 1. Objective Observation

例如：

- 页面最大宽度约 1200 px；
- 标题字号明显大于正文；
- 卡片几乎没有阴影；
- 主色只有一种。

### 2. Interpretation

例如：

- 整体偏 Swiss；
- 信息密度较低；
- 视觉节奏克制。

### 3. Personal Preference

例如：

- 我喜欢这种大面积留白；
- 我不希望使用这种强渐变；
- 我希望保留这种细边框策略。

三者混在一起，会导致 Style Library 很难真正服务个人设计。

## 最终目标

StyleForge 最终希望让一个新的前端项目可以从如下过程开始：

1. 选择产品类型；
2. 选择一个或多个 Style Profile；
3. 根据需要调整 Typography、Color、Layout 等规则；
4. 自动生成 AI Coding Context；
5. 由 Codex / Claude / GPT 实现；
6. 对生成结果进行视觉评价；
7. 将新的经验反馈到 Style Library。

长期来看，它可能输出：

- Prompt；
- Design Tokens；
- CSS Variables；
- Tailwind Theme；
- Component Guidelines；
- Motion Guidelines；
- Agent Skill；
- 前端实现约束。

但这些都是 Style Knowledge 的下游产物，而不是项目本体。
