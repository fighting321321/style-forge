# 架构说明

## 当前状态

StyleForge 仍处于 Phase 0，本文件记录初始概念架构，不代表最终技术方案。

## 核心对象

### Reference

一个用于学习的真实 UI 案例。

可能包含：

- 来源；
- URL；
- 产品类型；
- 页面类型；
- 截图；
- 作者 / 团队；
- 时间；
- 标签。

### Observation

对 Reference 的相对客观观察。

例如：

- 字体大小；
- 字重；
- 页面宽度；
- Grid；
- 间距；
- 色值；
- Radius；
- Shadow；
- 动效时间。

### Interpretation

对设计语言的解释。

例如：

- Minimal；
- Editorial；
- Swiss；
- Brutalist；
- Dense；
- Playful。

Interpretation 可以存在，但应与 Observation 分开。

### Preference

个人主观判断，例如：

- 喜欢；
- 不喜欢；
- 希望复用；
- 只适用于某些场景；
- 不希望 AI 默认使用。

### Style Profile

从多个 Reference 与 Preference 中提炼出的个人风格规则。

### Compiler

把 Style Profile 转换成具体下游格式：

```text
Style Profile
   ├─ Prompt
   ├─ Design Tokens
   ├─ CSS Variables
   ├─ Tailwind Config
   ├─ Agent Context
   └─ Component Guidelines
```

### Evaluation

记录 Style 被实际执行后的效果。

可能包括：

- 是否遵守 Typography；
- 是否遵守 Color；
- 是否出现默认 AI Pattern；
- 哪些规则无效；
- 哪些规则过度限制；
- 人工评价。

## 初始数据流

```text
Reference
   ↓
Analyze
   ↓
Observation + Interpretation
   ↓
Human Preference
   ↓
Style Profile
   ↓
Compile
   ↓
AI Frontend Generation
   ↓
Evaluation
   ↓
Style Profile Update
```

## 关键架构原则

### 事实与评价分离

尽量避免：

```text
style: very premium and modern
```

优先变成更明确的信息：

```text
layout:
  density: low
  section_spacing: large

surface:
  radius: small
  shadow: none

color:
  accent_count: 1
```

然后另行记录：

```text
preference:
  liked: true
  reason: "克制、信息层级清晰"
```

### Style 不等于 Prompt

Prompt 是 Style 的一种输出格式。

核心数据模型不应该被某个 LLM 的 Prompt 格式绑定。

### Schema 可演进

早期不要追求覆盖全部 UI 设计维度。

如果一个字段无法：

- 帮助比较案例；
- 帮助形成个人规则；
- 或帮助 AI 更稳定执行，

就不一定值得进入核心 Schema。

### 第三方内容边界

Reference Library 应优先保存：

- URL；
- 元数据；
- 自己的分析；
- 必要的低风险参考信息。

不要把项目变成未经许可的第三方设计资产镜像库。

## 当前开放问题

- Style 数据采用 YAML、JSON 还是其他格式？
- Screenshot 如何管理？
- 是否需要自动采集网站信息？
- 是否需要浏览器扩展？
- Style Profile 是否支持继承？
- 不同产品类型是否需要不同 Schema？
- Evaluation 如何量化？
- 是否需要多模型对比？

这些问题应通过实际案例逐步决定。
