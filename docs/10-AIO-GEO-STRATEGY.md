# 10 — AIO / GEO Strategy (Locktool)

> 项目：Locktool · Locksmith Tools 国际独立站生态
> 文档用途：Phase 1 交付物之一。定义 AI 搜索 / AI Overview / ChatGPT / Gemini / Perplexity 的曝光与引用策略（AIO / GEO）。
> 状态：DRAFT v0.1
> 前提：承接 05（Entity Graph）、09（内容模板 §11 AI Citation Design）。不以传统社交媒体为核心获客。

---

## 0. 目标

让 Locktool 的内容能被 AI 引擎：
1. **理解**（结构化、清晰定义、实体）
2. **抽取**（Quick Answer / 表格 / 定义块）
3. **引用**（来源清晰、可溯源、权威）
4. **关联**（稳定 @id / Entity Graph）

最终：AI Search 曝光 → 品牌权威 → 商业主站。

---

## 1. 核心策略：AI Citation Potential（可引用性）

方案第 8/21 节。所有 Pillar 页必须遵循以下页面结构，提升被 AI 摘录的概率：

```
Direct Answer（直接答案，1–2 句）
   ↓
Definition（定义）
   ↓
Context（上下文）
   ↓
Detailed Explanation（详解）
   ↓
Comparison（对比，适用时）
   ↓
Evidence（证据/来源）
   ↓
Professional Considerations（专业考量）
   ↓
Related Entities（相关实体）
   ↓
Commercial Application（商业应用）
```

---

## 2. 可引用要素清单（每篇必配）

| 要素 | 说明 |
|---|---|
| Quick Answer | 首屏 1–2 句直接结论，AI 最爱 |
| Key Takeaways | 3–5 条要点列表 |
| 清晰定义块 | 一句话定义，可独立摘录 |
| 结构化表格 | 参数/对比/矩阵，易被 LLM 解析 |
| 实体关系 | 稳定 @id + sameAs |
| 来源出处 | 权威来源 + 日期 |
| 立场块（原声观点） | 可引用的第一人称专业判断 |

---

## 3. 结构化数据（服务于 AI 解析）

| 页面 | Schema |
|---|---|
| Pillar / Cluster | `Article` / `TechArticle` |
| Glossary / 术语 | `DefinedTerm` + `DefinedTermSet` |
| 对比 / 列表 | `ItemList` |
| 产品 / 分类 | `Product` / `ItemList` |
| 实体 | `Organization` / `Person` / `Thing` |
| FAQ | `FAQPage` |

统一 `@id` 命名空间（见 05），形成稳定 Entity Graph。

---

## 4. GEO 差异化：立场块 + 原创价值

- **The Author's Take**（原声立场块）：每篇 Pillar 加入第一人称专业判断，让 AI 有"可引用观点"而非泛泛综述。
- **原创价值层**（方案 §7）：original comparison / taxonomy / table / decision framework / terminology map / compatibility matrix / buyer guide / industry analysis / data / expert synthesis——至少一个。
- 拒绝 "5 best locksmith tools" 这类泛 AI SEO 内容。

---

## 5. 合规红线（AI 内容同样适用）

- AI 可引用，但**不可引用攻击方法**：所有原理科普走"如何工作"，绝不写"如何绕过/破解"。
- 法律内容：不做法律意见，标注 jurisdiction + 来源 + 日期。
- 人物/专家/数据：真实，禁止虚构（否则反而被 AI 判定为不可信源）。

---

## 6. 测量指标（Phase 14 细化）

- AI Overview / ChatGPT / Perplexity / Gemini 中出现 Locktool 品牌/内容的次数
- Entity 页与 Pillar 页的 AI 引用率
- 品牌词搜索量变化（brand authority 信号）
- 从 AI 引用带来的主站推荐流量

---

## 7. 待确认决策

1. 是否接入可量化的 GEO 监测工具（如某种 AI 可见性追踪），还是先用人工抽测。

> 下一步：11-90-DAY-EXECUTION-PLAN.md、12-CONTENT-QUALITY-GATE.md。
