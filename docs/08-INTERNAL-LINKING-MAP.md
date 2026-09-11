# 08 — Internal Linking Map (Locktool)

> 项目：Locktool · Locksmith Tools 国际独立站生态
> 文档用途：Phase 1 交付物之一。定义全站内部链接架构，规范 Knowledge → Entity → Commercial 的链路，禁止无价值的交叉链接与人为 backlink network。
> 状态：DRAFT v0.1
> 前提：承接 04（Hub 架构）、05（Entity Graph）、06（Topic Clusters）。

---

## 0. 核心原则

方案第 10/20 节要求：
- 不用随机 Related Posts
- 建立稳定链路：Knowledge → Knowledge / Entity → Knowledge / Knowledge → Product Category / Category → Product / Product → Knowledge
- 商业链接必须自然，禁止每篇硬塞 10 个 Buy Now
- 禁止子站间大量交叉链接、footer 全站互链、人为 SEO network

---

## 1. 链路模型（正向）

```
Knowledge（概念页）
   ↓ 自然引用
Entity（术语/实体页）
   ↓ 关联
Knowledge（更深层文章 / 选型指南）
   ↓ 桥接
Product Category（分类）
   ↓ 细化
Product（SKU）
   ↓ 回链
Knowledge（原理/维护/选型）
```

**目标 Domain Authority Flow**：
```
Knowledge Hub → Topic Authority → Entity Authority → Internal Links
   → Commercial Site → Product Authority → Conversions
```

---

## 2. 链接类型与规则

| 链接类型 | 方向 | 规则 | 举例 |
|---|---|---|---|
| Contextual（上下文内链） | 正文 | 自然、克制，1 篇 ≤ 3–5 条商业桥 | "专业锁匠选 tension tool 时应考虑…" → 分类页 |
| Entity 链接 | 概念 → 实体 | 首次提及术语即链到 Entity 页 | "spool pin" → `#spool-pin` |
| Breadcrumb | 页面顶部 | 全站统一 | Home > Tools > Lock Picks > Hook Picks |
| Hub 导航 | 站内导航 | 指向同 Hub 相关主题 | — |
| Footer | 页脚 | 仅 Organization + 关键合规页，**不做全站互链** | About / Compliance / Contact |

---

## 3. 各 Hub 的内部链接骨架

### HUB 02 — Lock Technology
```
Lock Types Pillar（/technology/）
  ├→ Pin Tumbler（#pin-tumbler）
  ├→ Wafer（#wafer）
  ├→ Disc Detainer（#disc-detainer）
  └→ 关联选型 → /resources/compare/
```

### HUB 03 — Tools Knowledge
```
Tool Taxonomy Pillar（/resources/tools/）
  ├→ Tool Category（#lock-pick / #tension-tool / ...）
  │     └→ Selection Criteria → 商业分类页
  └→ Maintenance → 商业分类页（维护用品）
```

### HUB 04 — Automotive（高风险隔离）
```
Automotive Pillar（/automotive/）
  ├→ Key Programming（#key-programmer）→ 合规定位
  ├→ Immobilizer（#immobilizer-tool）→ 原理科普
  └→ 商业分类（授权锁匠设备）→ Product
```

### HUB 05 — Training
```
How to Become a Locksmith Pillar（/training/）
  ├→ Certification（#certification）→ ALOA 层级
  ├→ License by State → Compliance 矩阵
  └→ Training Programs → 商业（培训资源/入门套装）
```

### HUB 06 — Comparison
```
Comparison Hub（/resources/compare/）
  ├→ 需求 → 应用 → 技能 → 锁型 → 工具 → 约束
  └→ 每篇对比 → 商业分类/产品
```

### HUB 07 — Glossary
```
Glossary Pillar（/glossary/）
  ├→ 每术语 Entity 页（DefinedTerm）
  └→ 术语 → 相关工具/锁型/商业
```

### HUB 08 — Compliance
```
Compliance Hub（/compliance/）
  ├→ Jurisdiction Matrix → 每条法域
  ├→ Responsible Use Policy
  └→ Product Risk Matrix → 商业分类（标注风险级）
```

---

## 4. 商业桥接规则（不破坏体验）

允许的自然桥接句式：
- "Professionals selecting a tension tool should consider thickness and feedback — see our [tension wrenches]."
- "For authorized automotive locksmiths, the [key programmer] selection depends on vehicle coverage and skill level."
- "Proper [key blank] selection begins with identifying the lock's keyway."

禁止：
- 每段强插 "Buy Now"
- 无关的 footer 全站互链
- 人为制造子站交叉外链

---

## 5. 链接审计清单（发布前）

- [ ] 每篇知识文章 ≤ 3–5 条商业桥接链接
- [ ] 商业链接上下文自然（非关键词堆砌）
- [ ] Entity 术语首次出现链到 Entity 页
- [ ] 无孤立页（orphan page）
- [ ] 无 footer 全站互链 / 子站交叉链
- [ ] Breadcrumb 结构一致

---

## 6. 待确认决策

1. Entity 页是否全部建独立 URL（还是部分用锚点 # 承载）——影响链接颗粒度。

> 下一步：09-CONTENT-TEMPLATES.md（内容模板），把每个内容类型落成可复用模板。
