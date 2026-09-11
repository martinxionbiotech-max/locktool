# 12 — Content Quality Gate (Locktool)

> 项目：Locktool · Locksmith Tools 国际独立站生态
> 文档用途：Phase 1 交付物之一。定义发布前的内容质量门槛：9 项检查 + 7 维打分 + 一票否决项。
> 状态：DRAFT v0.1
> 引用：方案第 22 节。所有内容（含 AI 生成后）发布前必须过此门。

---

## 0. 核心规则

- 七维打分各 1–10 分，满分 **70**。总分 < 56（即均值 < 8 分）→ **不发布**
- Legal Safety < 9 → **人工审核**（无论总分）
- 任何一票否决项触发 → **STOP，回退人工**

---

## 1. 一票否决项（Red Flags）

以下任一命中，直接不发布：

1. 出现 01 文档 §1 的禁止语汇（"bypass immobilizer" / "defeat security" / "break into" / "undetectable entry" 等）
2. 提供绕过防盗/锁具/报警的具体攻击步骤或逐步操作
3. 虚构 locksmith license / 专家 / 测试 / 实验室 / 客户 / 数据
4. 法律结论无官方来源 / jurisdiction / 日期，或编造法律结论
5. 面向盗窃/未授权进入/规避安防的定位
6. 薄内容（仅替换城市/车型/关键词的伪程序化页面）

---

## 2. 九项发布前检查

| # | 检查项 | 说明 |
|---|---|---|
| 1 | FACT CHECK | 事实核对，数据有来源 |
| 2 | LEGAL CHECK | 合规，无危险语汇/攻击步骤 |
| 3 | DUPLICATION CHECK | 无重复/无 AI 改写堆砌 |
| 4 | SEARCH INTENT CHECK | 页面匹配用户搜索意图 |
| 5 | ENTITY CHECK | 实体挂靠正确、@id 一致 |
| 6 | INTERNAL LINK CHECK | 内链自然、无孤立、无堆砌 |
| 7 | SOURCE CHECK | 来源权威、带日期 |
| 8 | AI CITATION CHECK | 有 Quick Answer / 定义块 / 表格可被 AI 抽取 |
| 9 | COMMERCIAL RELEVANCE CHECK | 商业桥接自然、不过度 |

---

## 3. 七维打分卡

每维 1–10 分，总分 70 为满分；总分 < 56（即均值 < 8 分）不发布。

| 维度 | 权重说明 | 打分锚点 |
|---|---|---|
| Legal Safety | 一票关键，<9 即人工 | 是否触红线 |
| Originality /10 | 原创价值层 | 有无原创对比/分类/框架/数据 |
| Information Value /10 | 信息增益 | 是否回答真实问题 |
| SEO /10 | 关键词/结构 | 意图匹配 + 技术规范 |
| AIO /10 | AI 可引用性 | 定义块/表格/引用/实体 |
| EEAT /10 | 权威可信 | 作者/来源/专业考量 |
| Commercial Relevance /10 | 商业价值 | 是否自然导向主站 |

---

## 4. 打分流程

1. 作者（Agent）产出初稿
2. 过九项检查，任一否决项 → 停
3. 七维打分
4. 总分 ≥ 56 且 Legal Safety ≥ 9 → 可发布
5. 任一不达标 → 回修或人工审核

---

## 5. 记录模板（每篇内容）

```
页面: {URL}
类型: {A-J}
Legal Safety: /10
Originality: /10
Information Value: /10
SEO: /10
AIO: /10
EEAT: /10
Commercial Relevance: /10
总分: /70
结论: PUBLISH / REVISE / MANUAL REVIEW / STOP
```

---

## 6. 首批 19 篇自检记录（2026-09-11）

> 注：以下为 Agent 自评，Legal Safety 均 ≥9，无一篇触发一票否决。评分按 §3 七维（各 1–10，满分 70）。

### 技术 Hub（/technology/，7 篇）

| 页面 | 总分 | 结论 |
|---|---|---|
| pin-tumbler-vs-wafer-vs-disc-detainer（Pillar） | 61 | PUBLISH |
| pin-tumbler-lock-explained | 57 | PUBLISH |
| wafer-vs-pin-tumbler | 56 | PUBLISH |
| disc-detainer-locks-explained | 56 | PUBLISH |
| dimple-lock-explained | 56 | PUBLISH |
| tubular-lock-explained | 56 | PUBLISH |
| lever-tumbler-lock-explained | 56 | PUBLISH |

### 工具 Hub（/tools/，6 篇）

| 页面 | 总分 | 结论 |
|---|---|---|
| locksmith-tool-taxonomy（Pillar） | 60 | PUBLISH |
| lock-pick-types-explained | 58 | PUBLISH |
| key-cutting-machines-explained | 58 | PUBLISH |
| automotive-key-programmers-explained | 58 | PUBLISH |
| lishi-tools-explained | 59 | PUBLISH |
| lock-pick-gun-explained | 58 | PUBLISH |

### 认证 Hub（/certification/，3 篇）

| 页面 | 总分 | 结论 |
|---|---|---|
| how-to-become-a-locksmith（Pillar） | 59 | PUBLISH |
| aloa-certification-levels | 59 | PUBLISH |
| locksmith-license-by-state | 59 | PUBLISH |

### 标准 Hub（/standards/，3 篇）

| 页面 | 总分 | 结论 |
|---|---|---|
| lock-security-standards-explained（Pillar） | 61 | PUBLISH |
| en-1303-decoded | 60 | PUBLISH |
| ansi-bhma-grades-decoded | 60 | PUBLISH |

---

## 7. 待确认决策

1. 打分是否要人工复核，还是先 Agent 自评 + 抽查。

> Phase 1 的 12 个交付物全部完成（DRAFT v0.1）；首批 19 篇内容已过质量门（v0.2 更新）。
