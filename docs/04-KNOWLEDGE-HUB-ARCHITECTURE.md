# 04 — Knowledge Hub Architecture (Locktool)

> 项目：Locktool · Locksmith Tools 国际独立站生态
> 文档用途：Phase 1 交付物之一。定义 Knowledge Hub 生态的结构、子站/目录划分、各 Hub 定位与内部建站标准。
> 状态：DRAFT v0.1
> 核心原则：不为 SEO 建 Hub；每个 Hub 必须有独立 Purpose / Entity / Topic Cluster / Internal Linking / Content Model。拒绝薄内容、重复文章、关键词堆积、伪百科。

---

## 0. 架构总览

```
                 ┌──────────────────────┐
                 │   COMMERCIAL SITE    │   locktool.com（主站）
                 │     Money Site       │
                 └──────────┬───────────┘
                            │
        ┌───────────────┬───┴──────────┬────────────────┐
        │               │              │                │
        ▼               ▼              ▼                ▼
  Knowledge Hub   Technical Hub  Training Hub    Comparison Hub
        │               │              │                │
        └───────┬───────┴──────┬───────┴────────┬───────┘
                │              │                │
                ▼              ▼                ▼
          Entity Graph    Topic Graph     AI/Search Layer
```

**主站** = commercial intent；**子站** = informational / technical / educational / comparison / entity intent。

---

## 1. Hub 划分决策（哪些 Hub 建、哪些不建）

方案第 4/5 节给出 8 个候选 Hub。经竞品盲区分析（02 文档），我做如下取舍：

| Hub | 是否建 | 理由 | 承载形式 |
|---|---|---|---|
| HUB 01 Locksmith Knowledge（行业知识库） | ⭕ 有条件 | 规模大、术语/锁型/工作流需求真实，但**术语部分已与 Wikipedia 红海冲突** | 主站 `/knowledge/` 目录（规模中等，先不拆子域） |
| HUB 02 Lock Technology（锁技术百科） | ✅ 建 | 信息型查询海量，且是"技术原理科普"（安全，非攻击） | 子域 `technology.locktool.com` 或主站目录（见 §4） |
| HUB 03 Locksmith Tools Knowledge（工具知识） | ✅ 建 | 与商业站天然衔接，是 funnel 核心 | 主站 `/resources/tools/` |
| HUB 04 Automotive Locksmith Tech（汽车锁匠技术） | ✅ 建（高风险隔离） | 搜索需求强但合规风险高，须单独隔离 + 合规定位 | 子域或独立目录，强制 C 类审核门槛 |
| HUB 05 Locksmith Training（培训） | ✅ 建 | E-E-A-T + trust 杠杆最大，且市场零散无权威源 | 子域 `training.locktool.com` |
| HUB 06 Tools Comparison（对比/决策引擎） | ✅ 建 | 是"信息增益"核心，区别于软文对比 | 主站 `/resources/compare/` 或 Comparison Hub |
| HUB 07 Glossary / Dictionary（术语实体库） | ✅ 建 | 差异化在于**用 DefinedTerm 结构化**，而非与 Wikipedia 拼文本 | 主站 `/glossary/`（Entity Graph 载体） |
| HUB 08 Standards & Compliance（合规参考） | ✅ 建 | Blue Ocean 盲区 C，E-E-A-T + 安全红线的双重价值 | 主站 `/compliance/` + 索引 |

> 结论：**8 个方向都值得做，但不是 8 个子域**。优先用主站目录承载，只有规模足够、有独立实体、能持续产生内容且能反向反哺主站的，才拆子域（见 §4 阈值）。

---

## 2. 各 Hub 内容模型（Content Model）

每个 Hub 一个独立模板，禁止跨 Hub 套用同一模板（方案第 12 节）。

### HUB 02 — Lock Technology Hub（锁技术百科）
- 内容：pin tumbler / wafer / dimple / tubular / disc detainer / lever / padlock / smart lock 的原理、机制、材料、抗性
- 红线：解释原理 ≠ 教授攻击；禁止逐步绕过教学
- 模板 TYPE B（Technical Explanation）+ TYPE C（Comparison）
- 原创价值层：工程参数对比表（借鉴 firgelliauto 但扩展到全机制）

### HUB 03 — Locksmith Tools Knowledge Hub
- 内容：Tool Category → Function → Professional Use → Selection Criteria → Maintenance → Related Products
- 模板 TYPE D（Buying Guide）+ TYPE I（Product Knowledge）
- 红线：B 类工具（pick/tension/decoding）必须合规定位 + 受众区隔

### HUB 04 — Automotive Locksmith Tech Hub
- 内容：transponder 概念、immobilizer 原理、OEM vs aftermarket、key identification、诊断概念、设备选型
- 红线：禁止具体车型盗窃/绕过教程；强调 authorized locksmith / owner / dealer / technician
- 分级：任何绕过/破解内容 = C 类人工审核

### HUB 05 — Locksmith Training Hub
- 内容：beginner concepts、术语、工具选择、专业工作流、安全、ethics、business、continuing ed、certification 概览、jurisdiction 考量
- 模板 TYPE E（Professional Guide）+ TYPE G（Compliance）
- 原创价值层：ALOA 16 认证全景层级图 + 分州认证/持证决策树

### HUB 06 — Tools Comparison Hub
- 内容：Need → Application → Skill Level → Lock Type → Tool Type → Constraints → Selection
- 模板 TYPE C（Comparison）
- 原创价值层：兼容矩阵（Lock Type × Tool Type）、决策树、工程参数表

### HUB 07 — Glossary / Dictionary
- 每个术语：Definition / Alternative Names / Category / Related Concepts / Professional Context / Common Misunderstanding / Related Tools / Related Lock Types / Sources
- 模板 TYPE H（Glossary）
- 差异化：Schema `DefinedTerm` / `DefinedTermSet` + 稳定 @id，服务 AI 检索

### HUB 08 — Standards & Compliance Hub
- 内容：regional regulations、import、licensing、standards、restrictions、responsible use、safety
- 红线：法律信息必须官方来源 + 来源日期 + jurisdiction + 明确免责声明，不做法律意见
- 模板 TYPE G（Compliance）

---

## 3. 子域 vs 目录决策（阈值）

**只有当主题同时满足以下全部条件才拆子域：**
1. 规模足够大（预期 30+ 页可独立成站）
2. 有独立搜索需求
3. 有独立实体（不是主站实体的附属）
4. 能持续产生内容
5. 能反向反哺商业主站

**否则用主站目录**：

| 当前决策 | 形式 | 理由 |
|---|---|---|
| Lock Technology | 目录 `/technology/`（先不拆子域） | 初期规模未达 30+ 独立页阈值，先目录验证 |
| Automotive Tech | 目录 `/automotive/`（高风险隔离，但先目录） | 与主站同实体，拆子域无增益 |
| Training | 📌 候选子域 `training.locktool.com` | 有独立实体/受众（培训 vs 采购），E-E-A-T 价值高 |
| Comparison | 目录 `/resources/compare/` | 与主站商品强相关，不拆 |
| Glossary | 目录 `/glossary/` | Entity Graph 载体，必须与主站同域共享 @id |

> 子域拆分是**后续**决策，Phase 1 先定骨架，不急于拆。

---

## 4. 内部链接架构（Internal Linking Map 骨架）

```
Knowledge → Knowledge（同 Hub 内递进）
Knowledge → Entity（术语/概念 → 实体）
Entity → Knowledge（实体 → 相关文章）
Knowledge → Product Category（工具知识 → 商品分类）
Product Category → Product（分类 → SKU）
Product → Knowledge（SKU → 相关原理/选型）
```

**约束**：商业链接必须自然（如"专业锁匠选 tension tool 时应考虑…"再链到分类）；禁止每篇硬塞 10 个 Buy Now；禁止子站间大量交叉链、footer 全站互链、人为 backlink network。

---

## 5. 与主站的差异化承诺

- 主站 = Commerce-first 的克制商业层
- Knowledge Hub = Knowledge-first 的信息/技术/教育/对比层
- 二者通过 Entity Graph + 自然内链连接，形成 "Knowledge → Trust → Commercial Intent → Main Site" 的漏斗。

---

## 6. 待确认决策

1. 子域品牌：Confirmed 用 `locktool.com`，子域前缀（training./technology.）待最终拍板。
2. Training Hub 是否作为首个"独立子域"试点（我建议是，因它 E-E-A-T 杠杆最大且竞品最空白）。

> 下一步（Phase 1 内）：05-ENTITY-GRAPH.md（实体图，连接 04 的所有 Hub）。
