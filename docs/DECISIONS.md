# 设计决策记录

## D-001：StyleForge 不是 Prompt Library

**状态：** 已接受

### 决定

Prompt 是 StyleForge 的下游输出之一，而不是核心资产。

核心资产是：

- Reference；
- Structured Observation；
- Personal Preference；
- Style Profile；
- Evaluation Result。

### 原因

如果项目以 Prompt 为核心，会被特定模型和当前 Prompt 技巧绑定，也无法真正沉淀长期设计知识。

---

## D-002：AI 作为 Analyzer 与 Executor

**状态：** 已接受

### 决定

AI 主要负责：

- 分析优秀案例；
- 结构化信息；
- 根据 Style 执行前端生成。

最终审美判断由人完成。

### 原因

StyleForge 的目标是形成个人风格，而不是寻找一个新的“AI 默认审美”。

---

## D-003：Observation、Interpretation、Preference 分离

**状态：** 已接受

### 决定

对于同一个 Reference，尽量分别保存：

1. 相对客观的 Observation；
2. 对风格的 Interpretation；
3. 个人的 Preference。

### 原因

如果三者混合，后续很难判断一个规则究竟来自原始设计、AI 推断，还是个人喜好。

---

## D-004：早期不优先开发完整 Web App

**状态：** 已接受

### 决定

Phase 0～2 优先验证 Style Representation 与工作流。

### 原因

如果知识结构本身没有验证，先做复杂 Web UI、数据库和后台只会增加维护成本。

---

## D-005：项目文档以中文为主

**状态：** 已接受

### 决定

README、设计文档与 Codex 上下文以中文为主。

项目名、代码标识、技术术语以及更适合保留原文的概念使用英文。

### 原因

方便长期个人维护和 Codex 协作，同时避免为翻译而翻译。

---

## D-006：尊重第三方设计资产版权

**状态：** 已接受

### 决定

StyleForge 优先保存：

- 来源；
- 元数据；
- 自己的分析；
- 风格规则；
- 必要引用。

不默认重新分发第三方网站的完整截图、字体、图片或其他受保护素材。

### 原因

项目目的是学习设计知识，而不是建立第三方资产镜像。
