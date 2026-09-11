# 09 — Content Templates (Locktool)

> 项目：Locktool · Locksmith Tools 国际独立站生态
> 文档用途：Phase 1 交付物之一。定义 10 类内容模板（Content Matrix），每类一个独立结构，禁止跨类套用。
> 状态：DRAFT v0.1
> 前提：承接 06（Topic Clusters）、07（Keyword Map）。每类模板都要过内容质量门（12 文档）。

---

## 0. Content Matrix（内容类型总表）

| Type | 名称 | 用途 | 模板要点 | 对应 Hub |
|---|---|---|---|---|
| A | Definition | 定义/概念 | Direct Answer → 定义 → 上下文 → 疑难 | Glossary |
| B | Technical Explanation | 技术原理 | 原理 → 机制 → 参数 → 安全边界 | Technology |
| C | Comparison | 对比 | 参数矩阵 → 场景适配 → 决策树 | Comparison |
| D | Buying Guide | 选购指南 | 需求 → 选型维度 → 推荐逻辑 | Tools Knowledge |
| E | Professional Guide | 专业指南 | 工作流 → 技能 → 工具 → 合规 | Training |
| F | Industry Research | 行业分析 | 数据 → 趋势 → 洞察 | Knowledge |
| G | Compliance | 合规参考 | 法域 → 条款 → 来源 → 免责 | Compliance |
| H | Glossary | 术语 | 定义 → 别名 → 关系 → 来源 | Glossary |
| I | Product Knowledge | 产品知识 | 规格 → 兼容 → 维护 → 商业桥 | Tools Knowledge |
| J | Case / Application | 应用案例 | 场景 → 问题 → 方案 → 结果 | Various |

---

## 1. 模板 A — Definition（定义页）

```
H1: {Term}
Quick Answer（1–2 句，可被 AI 抽取）
Definition（完整定义）
Alternative Names / Aliases
Category（所属分类）
Related Concepts（关联概念）
Professional Context（专业语境）
Common Misunderstanding（常见误解）
Related Tools / Lock Types
Sources（权威来源）
```

Schema：`DefinedTerm`（挂在 `DefinedTermSet`）。

---

## 2. 模板 B — Technical Explanation（技术原理页）

```
H1: {Technology} Explained
直接回答（What / Why）
工作原理（概念层，非攻击步骤）
关键机制 / 参数
安全边界（做什么、不做什么）
对比（与其他机制，若有）
专业考量（Professional Considerations）
相关实体 + 来源
```

Schema：`TechArticle`。
⚠️ 红线：只讲"如何工作"，不讲"如何攻击/绕过"。

---

## 3. 模板 C — Comparison（对比页）

```
H1: {A} vs {B}（或多个）
概述（何时选谁）
参数对比矩阵（表）
场景适配（决策树 / 表格）
专业考量（Skill Level / Lock Type / Tool Type / Constraints）
结论（推荐逻辑）
商业桥接（自然）
```

Schema：`Article` + `ItemList`（可选）。
原创价值层：必须含一张**工程参数表**或**决策树**，拒绝软文式"哪个更好"。

---

## 4. 模板 D — Buying Guide（选购指南）

```
H1: {Category} Selection Guide
目标受众（licensed/authorized）
选型维度（材料/规格/兼容/技能门槛/预算）
推荐逻辑（不是"best 5"，是"何时选哪种"）
对比表
合规 / 安全提示（B 类需受众区隔）
商业桥接
```

原创价值层：选型决策框架，不是 listicle。

---

## 5. 模板 E — Professional Guide（专业指南）

```
H1: {Workflow / Skill} for Locksmiths
适用对象 + 前置技能
专业工作流（步骤，合规内）
所需工具（链到商业）
安全 / ethics / 合规边界
继续教育 / 认证关联
```

原创价值层：结构化工作流，市场零散无权威源。

---

## 6. 模板 F — Industry Research（行业分析）

```
H1: {Topic} — Industry Analysis
背景 + 数据（有来源）
趋势
洞察 / 立场块（原声观点）
对专业人士的含义
来源
```

原创价值层：原创数据或原创综合（synthesis），禁止 AI 改写。

---

## 7. 模板 G — Compliance（合规页）

```
H1: {Regulation / Jurisdiction Topic}
权威声明（非法律意见）
法域 / 条款 / 限制（表格）
官方来源（URL + 日期）
免责声明（克制，集中）
相关合规页内链
```

⚠️ 红线：引用官方来源，标注 jurisdiction + 日期；不做法律意见；禁止编造结论。未确认项标 `[UNKNOWN]`。

---

## 8. 模板 H — Glossary（术语表）

```
H1: Locksmith Glossary
分组导航（按类别）
单条术语结构等同模板 A
DefinedTermSet 包裹全部引用的 DefinedTerm
```

Schema：`DefinedTermSet` + 多个 `DefinedTerm`。

---

## 9. 模板 I — Product Knowledge（产品知识页）

```
H1: {Product Category} — What It Is & How It's Used
What / Who / Why / How different
Specifications（表）
Compatibility（锁型/车型）
Professional Application
Maintenance
Safety / Compliance（风险级标注）
商业桥接（自然）
```

Schema：`Product`（如需，价格字段询价模式不填 price）。

---

## 10. 模板 J — Case / Application（应用案例）

```
H1: {Application} for {Profession}
场景 / 问题
方案（合规）
工具 / 产品（桥接）
结果 / 考量
```

原创价值层：真实应用叙事，非虚构。

---

## 11. AI Citation Design（所有 Pillar 页统一附加）

方案第 21 节要求每个 Pillar 页增加：
- Quick Answer（可引用短答）
- Key Takeaways（要点）
- Technical Summary（技术小结）
- Comparison（对比，若适用）
- Sources（来源）
- Related Concepts（相关概念）
- Professional Considerations（专业考量）

使 AI 能快速理解、提取、引用、关联实体。

---

## 12. Content Quality Gate（发布门槛）

方案第 22 节，每个内容过 9 项检查 + 打分（详见 12-CONTENT-QUALITY-GATE.md）：

Legal Safety / Originality / Information Value / SEO / AIO / EEAT / Commercial Relevance

- 总分 < 80 → 不发布
- Legal Safety < 9 → 人工审核

---

## 13. 待确认决策

1. 图文比例：是否需要为每类模板配示意结构图（锁型机制图），还是纯文字 + 表格先行。

> 下一步：10-AIO-GEO-STRATEGY.md、11-90-DAY-EXECUTION-PLAN.md、12-CONTENT-QUALITY-GATE.md。
