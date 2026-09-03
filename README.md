# Minimal Doodle Product Poster Skill

极简留白 × 真实产品摄影 × 无脸微缩小人 × 稚拙细线中文的可复用 AI 生图 Skill。

> 这套视觉常被口语化称为“喜茶风”，但本项目使用中性的可迁移语言描述它：**Minimal Product Photography + Doodle Micro-Storytelling**。目标不是复刻某个品牌，而是提炼一种可复用的视觉方法。

## v0.4 核心升级：Fidelity Focus System

Fidelity Mode 不再等于“整体更精细”，而是一次只解决一个高保真问题。

```yaml
mode: fidelity
fidelity_focus: subject_identity | dominant_element | lettering
```

三种 Focus：

| Focus | 什么时候用 | 核心目标 |
|---|---|---|
| `subject_identity` | “主体不要变”“保持原物” | 锁死产品类别、轮廓、材质和关键细节 |
| `dominant_element` | “强调最大的元素”“突出番茄/饼干” | 让最强的有意义元素成为第一视觉信号 |
| `lettering` | “字体不像”“只改标题” | 冻结海报底图，只重做手写文字 |

同时引入三层锁定逻辑：

```text
Subject Lock = 它是什么？
Scene Lock   = 原场景靠什么被认出来？
Focus Lock   = 这一轮最需要强调什么？
```

这样复杂原图也不用在“完全还原”和“只留一个主体”之间二选一。

## 工作流

```text
上传照片
→ Subject Lock
→ 必要时 Scene Lock
→ 提炼产品特征
→ 生成微缩工作动作
→ Quick / Fidelity
→ Fidelity 时选择单一 Focus
→ 生成海报
→ Evaluation 验收
```

## 风格公式

```text
大面积白色留白
+ 单一真实摄影主角
+ 黑色稚拙线稿
+ 4–5 个无脸圆头微缩小人
+ 产品相关动作叙事
+ 稚拙、松散、细黑线中文
= 安静、清爽、治愈、有故事感的产品海报
```

## 两种生成模式

### Quick Mode

适合第一次探索和快速测试。主体、小人和文字一次完成。

### Fidelity Mode

适合已经知道“哪里必须更准”的情况。

- `subject_identity`：先保主体准确
- `dominant_element`：先保视觉焦点准确
- `lettering`：先保字体准确，其他全部冻结

如果几个问题同时存在，分轮解决，不要一张图里同时大改主体、焦点、字体和小人。

## 实测对比｜苹果冰茶「心态放苹」

| 原图 | Version 1 · Quick Mode | Version 2 · Fidelity Mode |
|---|---|---|
| ![原图：苹果冰茶实拍](assets/examples/apple-tea/source.svg) | ![Quick Mode：心态放苹](assets/examples/apple-tea/quick-mode-mini.svg) | ![Fidelity Mode：心态放苹](assets/examples/apple-tea/fidelity-mode-mini.svg) |
| 实拍照片作为 Subject Lock 基准。 | 一次完成海报，验证整体风格能否快速成立。 | 强化红苹果与苹果切片，让标题中的“苹”与主体关系更直接。 |

完整测试记录见 [`examples/apple-tea-test.md`](examples/apple-tea-test.md)。

## 实测对比｜3 组本人实拍照片

本轮继续测试不同复杂度的真实照片，并为 Fidelity Mode 指定统一目标：**`dominant_element`，强调画面中最大的有意义元素**。

![三组 Original / Quick / Fidelity 对比](assets/examples/three-case-comparison.svg)

| Case | Quick Mode | Fidelity · dominant_element |
|---|---|---|
| 蔬菜农场 | 保留多个角色与蔬菜关系，故事更丰富。 | 锁定巨型红番茄为第一视觉中心。 |
| 米奇海鲜汤 | 保留整碗食材丰富度。 | 强化中央黄色造型食材。 |
| 焦糖饼干冰淇淋 | 饼干、冰淇淋、焦糖共同叙事。 | 放大焦糖饼干作为最强形状锚点。 |

完整测试记录见 [`examples/three-case-comparison.md`](examples/three-case-comparison.md)。

## 最重要的 6 条规则

1. **Subject Lock**：先确认“它是什么”，再做创意。
2. **Scene Lock**：复杂照片只留 1–3 个有识别价值的场景线索，不把全部元素搬进白底海报。
3. **Focus Lock**：Fidelity 每轮只有一个主目标。
4. **Photography First**：真实产品摄影永远是第一视觉锚点，不做全图卡通化。
5. **Worker ≠ Decoration**：每个小人必须有产品相关工作。
6. **Fixed Figure System**：圆头、无五官、无表情、无发型、无服饰、无标签，只靠动作表达。

## 推荐输入

最简单只给照片也可以。更稳定时建议：

```yaml
subject: 巨型红番茄
feature: 饱满、巨大、红色、农场感
caption: 大番茄 大满足
worker_count: 4
color_palette: 红、绿、白、黑
mode: fidelity
fidelity_focus: dominant_element
```

如果是字体修复：

```yaml
mode: fidelity
fidelity_focus: lettering
caption: 清甜下午茶
```

## 文件结构

```text
minimal-doodle-product-poster-skill/
├── README.md
├── SKILL.md
├── ASSET-NOTICE.md
├── references/
│   ├── style-guide.md
│   ├── subject-fidelity.md
│   ├── fidelity-focus.md
│   ├── micro-worker-guide.md
│   ├── lettering-guide.md
│   └── evaluation.md
├── prompts/
│   ├── quick-prompt.md
│   ├── poster-base.md
│   └── lettering-layer.md
├── evals/
│   └── evals.json
├── assets/examples/
│   ├── apple-tea/
│   └── three-case-comparison.svg
└── examples/
    ├── watermelon.md
    ├── blue-pudding.md
    ├── apple-tea-test.md
    └── three-case-comparison.md
```

## 当前测试结论

- 西瓜案例验证了“产品特征 → 微缩工作”的叙事逻辑。
- 蓝色布丁案例修复了主体漂移：布丁不能因为“蓝色 + 清凉”变成刨冰。
- 蓝色布丁第二轮锁定了无脸、无服饰的小人系统。
- “清甜下午茶”证明字体需要独立控制字形骨架，而不是继续堆“手写感”形容词。
- 苹果冰茶证明 Fidelity 可以服务于产品语义强化。
- 三组本人实拍证明 `dominant_element` 能显著拉开 Quick 与 Fidelity 的视觉层级。
- 新增回归规则：多张照片要求分别生成时，不能自动混成一张拼图或对比板。

## 发布边界

仓库不默认包含官方品牌 Logo、吉祥物、包装标识或未经授权的第三方参考图。本人拍摄并明确允许用于测试展示的素材可作为回归案例保留。具体见 `ASSET-NOTICE.md`。

## 当前版本

**v0.4 — Fidelity Focus System**

下一阶段目标：验证 `subject_identity / dominant_element / lettering` 三条 Fidelity 分支在不同品类照片上的稳定性。