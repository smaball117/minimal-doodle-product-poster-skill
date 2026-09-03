# Minimal Doodle Product Poster Skill

**真实产品摄影 × 极简留白 × 无脸微缩小人 × 稚拙细线中文** 的可复用 AI 生图 Skill。

> 这套视觉常被口语化称为“喜茶风”。本项目使用更中性的描述：**Minimal Product Photography + Doodle Micro-Storytelling**。目标不是复刻某个品牌，而是提炼一套可迁移、可测试、可迭代的视觉方法。

## What It Does

给一张真实产品、食物、饮品或日常物件照片，Skill 会把它转译成：

```text
大面积白色留白
+ 真实摄影主体
+ 黑色极简微缩小人
+ 与产品特征相关的动作故事
+ 稚拙、松散、细黑线中文
```

核心原则只有一句：**摄影主体负责“是什么”，小人负责“它有什么特点”。**

## Generation Modes

### Quick Mode

适合第一次探索。主体、小人和文字一次生成，用最快速度建立完整海报。

### Fidelity Mode

适合已经知道“哪里必须更准”的情况。一次只解决一个高保真问题：

```yaml
mode: fidelity
fidelity_focus: subject_identity | dominant_element | lettering
```

| Focus | 适用场景 | 目标 |
|---|---|---|
| `subject_identity` | 主体不能变、必须保持原物 | 锁定类别、轮廓、材质和关键细节 |
| `dominant_element` | 强调最大或最强元素 | 建立明确第一视觉中心 |
| `lettering` | 只修标题、字体不像 | 冻结海报底图，只重做手写文字 |

Fidelity Mode 使用三层锁定：

```text
Subject Lock = 它是什么？
Scene Lock   = 原场景靠什么被认出来？
Focus Lock   = 这一轮最需要强调什么？
```

## Example · Apple Tea「心态放苹」

| Original | Quick Mode | Fidelity Mode |
|---|---|---|
| <img src="assets/examples/apple-tea/source.jpg" width="220" alt="Original apple tea photo" /> | <img src="assets/examples/apple-tea/quick-mode.jpg" width="220" alt="Apple tea Quick Mode" /> | <img src="assets/examples/apple-tea/fidelity-mode.jpg" width="220" alt="Apple tea Fidelity Mode" /> |
| 输入基准：苹果冰茶、苹果切片、冰块与饮品渐变。 | 一次建立摄影主体、小人故事与标题。 | 在已成立的海报基础上，对指定 Focus 做单项强化。 |

[查看完整测试记录 →](examples/apple-tea-test.md)

## 3-Case Experiment · Original × Quick × Fidelity

3 组实验覆盖复杂展陈、复合餐品与单一甜品，用来观察 **Quick Mode** 与 **Fidelity Mode · `dominant_element`** 的视觉差异。

<img src="assets/examples/three-case-comparison.jpg" width="900" alt="Three-case Original Quick Fidelity comparison" />

| Case | Quick Mode | Fidelity · `dominant_element` |
|---|---|---|
| 蔬菜农场 | 保留更多场景关系，故事更丰富。 | 锁定巨型红番茄为第一视觉中心。 |
| 海鲜汤 | 保留整碗食材丰富度。 | 强化中央黄色造型食材。 |
| 焦糖饼干冰淇淋 | 饼干、冰淇淋与焦糖共同叙事。 | 强化焦糖饼干这一最强形状锚点。 |

[查看完整 3 组实验记录 →](examples/three-case-comparison.md)

## Workflow

```text
上传照片
→ Subject Lock
→ 必要时 Scene Lock
→ 提炼 2–4 个真实产品特征
→ 转译为 3–5 个微缩工作动作
→ Quick / Fidelity
→ Fidelity 选择单一 Focus
→ 生成
→ Evaluation 验收
```

## Non-Negotiable Rules

1. **Subject Lock**：先确认“它是什么”，再做创意。感官概念不能覆盖产品身份。
2. **Photography First**：产品始终保持真实摄影材质，不做全图卡通化。
3. **Scene Lock**：复杂照片只保留 1–3 个有识别价值的场景线索。
4. **Worker ≠ Decoration**：每个小人必须对应一个产品特征和一个清晰动作。
5. **Fixed Figure System**：圆头、无五官、无表情、无发型、无服饰、无标签，只靠姿态和工具表达。
6. **Lettering Is a System**：稚拙、松散、细黑线、结构略歪，不使用标准字体、工整书法或圆润可爱字体。
7. **One Fidelity Focus per Pass**：主体、焦点、字体分别修，不在一轮里同时推翻所有已接受结果。

## Recommended Input

只给一张照片也可以。需要更明确控制时，可补充：

```yaml
subject: 巨型红番茄
feature: 饱满、巨大、红色、农场感
caption: 大番茄 大满足
worker_count: 4
color_palette: 红、绿、白、黑
mode: fidelity
fidelity_focus: dominant_element
```

## Repository Structure

```text
minimal-doodle-product-poster-skill/
├── README.md
├── SKILL.md
├── ASSET-NOTICE.md
├── references/
│   ├── style-guide.md
│   ├── subject-fidelity.md
│   ├── micro-worker-guide.md
│   ├── lettering-guide.md
│   ├── fidelity-focus.md
│   └── evaluation.md
├── prompts/
│   ├── quick-prompt.md
│   ├── poster-base.md
│   └── lettering-layer.md
├── evals/
│   └── evals.json
├── assets/examples/
│   ├── apple-tea/
│   └── three-case-comparison.jpg
└── examples/
    ├── watermelon.md
    ├── blue-pudding.md
    ├── apple-tea-test.md
    └── three-case-comparison.md
```

## Current Learnings

- 西瓜案例验证了“产品特征 → 微缩工作”的叙事逻辑。
- 蓝色布丁案例修复了“感官概念覆盖主体身份”的 Subject Drift。
- 固定小人系统已经明确：圆头、无脸、无表情、无服饰。
- 中文标题不能只靠“手写感”形容词，需要独立控制字形骨架、间距、倾斜与笔画长度。
- 3 组实验验证：Quick Mode 更擅长快速建立完整故事；Fidelity Mode 在指定 `dominant_element` 后更容易建立明确视觉中心。

## Asset & Brand Notice

项目不默认包含官方品牌 Logo、吉祥物、包装标识或未经授权的第三方素材。测试展示素材应确保具有相应使用权限。详细说明见 [`ASSET-NOTICE.md`](ASSET-NOTICE.md)。

## Version

**v0.4 — Fidelity Focus System**