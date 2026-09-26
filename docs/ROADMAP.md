# 开发路线

## Phase 0：定义 Style Representation

目标：先解决“风格应该如何表示”。

任务：

- 选取少量优秀 UI 案例作为测试集。
- 手工拆解 Typography、Color、Layout、Spacing 等维度。
- 区分 Observation、Interpretation、Preference。
- 尝试 JSON / YAML / Markdown 等表示方式。
- 比较自由文本与结构化字段的优缺点。

产出：

- 第一版 Style Schema；
- 3～5 个完整案例分析；
- Style 分析模板。

## Phase 1：Reference Library

目标：形成可持续积累的案例库。

任务：

- 定义案例元数据；
- 保存来源 URL、作者、产品类型等信息；
- 记录案例截图或截图引用方式；
- 建立标签体系；
- 允许同一案例拥有多个视角的分析。

重点不是“收集数量”，而是保证每个案例真的能用于学习。

## Phase 2：Style Analyzer

目标：利用 AI 辅助分析案例。

可能流程：

```text
Screenshot / Website
        ↓
AI Analysis
        ↓
Structured Draft
        ↓
Human Review
        ↓
Style Knowledge
```

任务：

- 设计稳定的分析 Prompt / Agent Skill；
- 约束输出结构；
- 对比 AI 分析与人工分析；
- 标记低置信度结论；
- 避免只输出模糊形容词。

## Phase 3：Personal Style Library

目标：从“案例库”进一步形成“我的设计规则”。

任务：

- 从多个案例中提取共性；
- 建立 Style Profile；
- 支持组合不同风格元素；
- 记录喜欢 / 不喜欢的具体原因；
- 建立 Context-sensitive Rules。

例如：

- Portfolio 适合什么；
- Dashboard 适合什么；
- 学术网站适合什么；
- 游戏界面适合什么。

## Phase 4：Style Compiler

目标：把 Style Knowledge 转换成 AI 能执行的输入。

可能输出：

- Prompt；
- AGENTS.md 片段；
- Design Tokens；
- CSS Variables；
- Tailwind Theme；
- Component Guidelines；
- Motion Guidelines。

核心问题：

> 同一个 Style 能否稳定转换成不同工具都能理解的约束？

## Phase 5：Generation Evaluation

目标：真正验证 Style 是否有效。

任务：

- 对同一需求生成多个版本；
- 比较默认 AI 输出与 StyleForge 输出；
- 检查一致性；
- 记录失败案例；
- 找到哪些 Style 字段真正影响结果。

建立：

```text
Style
→ Generate
→ Compare
→ Evaluate
→ Update Style
```

的迭代闭环。

## Phase 6：工具化

当前面方法被验证后，再考虑：

- CLI；
- Web UI；
- 浏览器扩展；
- Screenshot Analyzer；
- Style Browser；
- Prompt Exporter；
- Codex / Claude Skill；
- 自动前端实验环境。

工具形态应服务已经验证的方法，而不是反过来驱动项目方向。
