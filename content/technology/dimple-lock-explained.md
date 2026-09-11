# Dimple Lock Explained: How Side-Pinned Pin Tumblers Work and Where They Sit on the Security Ladder

> 项目：Locktool · Content
> 类型：Technical Explanation Cluster（模板 B）
> 所属 Hub：Lock Technology Hub（/technology/）
> 主实体：`#dimple-lock`、`#lock`
> 状态：DRAFT
> 研究日期：2026-09-11

---

## Direct Answer

Dimple lock（点孔锁 / 珠窝锁）本质上是**弹子锁的一个变种**——它用的还是弹簧销钉 + 剪切线，区别在于**销钉从钥匙的"平面"进入，而不是从边缘进入**。

钥匙插入后转 90°，用**钥匙叶片的平面**（而非边缘齿）作为驱动面，充满凸起/凹陷的牙花顶着销钉。因为牙花分布在平面上，可以做得更密集、支撑侧销（side pin）和更多维度，所以整体**抗撬性高于普通边缘弹子锁**，安全上限落在"中等到高"区间。

它最常见的应用场景是**欧洲 Euro cylinder（欧标锁芯）**和高安保挂锁。

---

## 机制：从"边缘齿"到"平面牙花"

普通弹子锁：钥匙是扁平刀刃，**边缘齿**顶起销钉，销钉沿钥匙边缘方向排列。

Dimple lock：钥匙同样是扁平的，但**牙花打在平面（flat face）上**——凸起或凹陷的小圆点/槽，插入后旋转 90° 让这些牙花去顶侧向布置的销钉。

因为平面可以承载的牙花数量更多、排列更自由，dimple lock 通常能容纳：
- 更多销钉（高端 Euro cylinder 可到 11 pin）
- 侧销（side pins）/侧杆（sidebar），增加二维防护
- 更复杂的 keyway，限制工具进入角度

所以 dimple lock 往往比同销钉数的边缘弹子锁更难撬，且需要**专用 dimple pick**，普通 hook/rake 不适用。

---

## 安全等级 & 星级体系（Euro Cylinder 语境）

Dimple lock 大量用于 Euro cylinder，而 Euro cylinder 有一套由 **DHF（Door & Hardware Federation）与 Glass & Glazing Federation** 制定的 **1–3 星评级**：

| 星级 | 典型配置 | 抗攻能力 |
|---|---|---|
| 1 星 | 6 pin | 基础防撬，但易受 bump / snap（锁芯折断）攻击 |
| 3 星 | 11 pin + 抗 snap/抗 bump/抗钻 | 抗撬、抗钻、抗拔、抗 bump、抗 snap，Secure by Design 认证 |

**关键提醒**：Euro cylinder（欧标锁芯）的**最大弱点不在销钉机制，而在"锁芯折断（lock snapping）"**——通过暴力掰断锁芯暴露内部机构。这是 1 星低安全 Euro cylinder 最常见的被攻击方式，3 星 cylinder 通过抗 snap 设计解决。

---

## The Author's Take

**我的判断：dimple lock 是"弹子锁家族的进阶分支"，它的价值在于用平面牙花换来了更高的销钉密度和侧销维度，但它不是一种全新的安全范式。** 如果你要的是"比普通门锁更抗撬、但还在弹子锁体系内"，dimple 是合适的选择；但它仍受 bump / snap 等攻击的威胁，需要靠星级体系里的抗 snap/抗 bump 设计来补足，而不是靠"它是 dimple"本身。

所以选 Euro cylinder 时，**看星级（1 星 vs 3 星）比看"是不是 dimple"更重要**——星级直接对应了抗 snap/bump/drill 的具体能力。

（以上是基于机制分析 + DHF 评级体系的专业判断，非我方实测。）

---

## FAQ

**Dimple lock 和普通弹子锁有什么区别？**
同机制（弹簧销钉 + 剪切线），但销钉从钥匙平面进入，可容纳更多销钉和侧销，抗撬性更高，需要专用工具。

**Dimple lock 更安全吗？**
在弹子锁体系内，是。但仍受 bump/snap 威胁，安全性取决于星级和抗攻设计，而非"dimple"这个名词。

**什么是 Euro cylinder 的 1 星和 3 星？**
DHF + Glass & Glazing Federation 制定的评级。1 星基础防撬；3 星抗撬/钻/拔/bump/snap，Secure by Design 认证。

---

## Sources

- Master Key Systems — Euro Cylinder Locks Explained（dimple 机制、11-pin 3 星 vs 6-pin 1 星）
- LockPickWorld — Pin Tumbler Locks Explained（dimple 对照表、安全评级 3/5）
- Coastal Group（DHF/GGF 1 vs 3 星体系）
- Wikipedia — Pin tumbler lock（引 dimple 侧销）

---

## 关联

- → Pillar：Pin Tumbler vs Wafer vs Disc Detainer
- → Pin Tumbler Lock Explained
- → Entity：`#dimple-lock` / `#lock`
