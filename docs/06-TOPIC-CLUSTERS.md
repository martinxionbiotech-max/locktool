# 06 — Topic Clusters (Locktool)

> 项目：Locktool · Locksmith Tools 国际独立站生态
> 文档用途：Phase 1 交付物之一。定义主题树（Topic Tree）与 Pillar → Cluster → Supporting → Entity → Commercial 的内容层级。
> 状态：DRAFT v0.1
> 前提：承接 05-ENTITY-GRAPH.md。主题簇必须围绕实体组织，而非围绕关键词堆砌。

---

## 0. 核心原则

- 不"发现关键词 → 写文章"。而是：Search Intent → Entity → Topic → User Problem → Information Gap → Original Value → Evidence → Content → Internal Link → Commercial Relevance → AI Citation。
- Pillar 页负责 broad informational intent；Cluster 页负责 long-tail；Supporting 页负责具体问题；Entity 页负责实体定义；Commercial 页负责转化。

---

## 1. Topic Tree（主题树）

```
Locksmith（根）
├── 01 Locksmith Tools（锁匠工具）
│   ├── Tool Categories（分类学）
│   ├── Tool Selection（选型）
│   ├── Tool Materials（钢材/工艺）
│   ├── Tool Maintenance（维护）
│   └── Tool Kits（套装）
├── 02 Lock Types（锁型）
│   ├── Pin Tumbler / Wafer / Dimple / Tubular / Disc Detainer / Lever / Padlock / Smart
├── 03 Key Systems（钥匙系统）
│   ├── Key Blank / Key Cutting / Master Key / Restricted Key / Transponder
├── 04 Lock Technology（锁技术）
│   ├── Mechanisms / Anti-pick / Security Evolution
├── 05 Automotive Locksmith（汽车锁匠）
│   ├── Key Programming / Immobilizer / Diagnostics / OEM vs Aftermarket
├── 06 Locksmith Training（培训）
│   ├── Beginner / Certification / Continuing Ed / Ethics
├── 07 Locksmith Certification（认证）
│   ├── ALOA 体系 / 州持证 / 法域差异
├── 08 Tool Selection（选型）
│   ├── 需求 → 应用 → 技能 → 锁型 → 工具 → 约束
├── 09 Tool Maintenance（维护）
├── 10 Security Technology（安防技术）
├── 11 Compliance（合规）
│   ├── 法域矩阵 / 进口 / 持有 / 责任使用
└── 12 Glossary（术语）
```

---

## 2. Pillar 页定义（Top-level）

| Pillar | 对应 Entity | 目标意图 | 承接 Hub |
|---|---|---|---|
| Locksmith Tools: The Complete Taxonomy | `#locksmith-tool` | 工具分类体系，商业意图上位 | HUB 03 |
| Lock Types: Engineering Comparison | `#lock` + 锁型子实体 | informational + comparison | HUB 02 |
| Key Systems: From Blank to Transponder | `#key` 系列 | informational + technical | HUB 02/04 |
| Lock Technology: How Locks Work | `#lock` | technical explanation | HUB 02 |
| Automotive Locksmith Technology | `#automotive-locksmith` | technical + compliance | HUB 04 |
| How to Become a Locksmith | `#training` | educational + E-E-A-T | HUB 05 |
| Locksmith Certification: The Complete Map | `#certification` | educational + compliance | HUB 05/08 |
| Locksmith Tool Selection Framework | `#locksmith-tool` | commercial intent 上位 | HUB 06 |
| Locksmith Glossary | `#glossary`（DefinedTermSet） | entity intent | HUB 07 |

---

## 3. Cluster 页（中长尾）

每个 Pillar 下挂 4–8 个 Cluster，示例（Pillar 1 — Tools）：

- Hook Picks vs Rakes: When to Use Each
- Tension Wrenches: BOK vs TOK Explained
- Professional vs Beginner Lock Pick Sets
- Tool Steel & Finishes: Spring Steel vs Stainless
- Decoding Tools: What They Are & Professional Use
- Key Cutting Machines: Types & Selection
- Broken Key Extractors: Selection & Use
- Tool Kits: Building a Professional Loadout

---

## 4. Supporting 页（长尾/具体问题）

- "What is a spool pin?"（术语实体 → 关联 Cluster）
- "How many key combinations does a 5-pin lock have?"（数据点 → 关联 Lock Technology）
- "Is it legal to carry lock picks in [State]?"（合规 → 关联 Compliance）

> 注意：Supporting 页若只剩薄内容（城市/车型/关键词替换），按方案 14 节禁止生成。

---

## 5. 内容层级关系图

```
Pillar (broad)
  ├── Cluster (mid)
  │     ├── Supporting (long-tail)
  │     └── Entity (definition)
  └── Commercial (product/category/solution)
```

内链规则：
- Pillar ↔ Cluster 双向
- Cluster → Supporting / Entity
- Entity → 相关 Cluster
- Cluster/Pillar → Commercial（自然桥接）

---

## 6. 待确认决策

1. 首批 Pillar 优先级：建议先做 **Lock Types + Certification + Tool Selection**（对应用户 02 文档蓝海 C/A/B），具体排序待 07 关键词量确认。

> 下一步：07-KEYWORD-MAP.md（把主题簇映射到真实关键词与搜索意图）。
