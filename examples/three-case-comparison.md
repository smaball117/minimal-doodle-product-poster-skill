# Three-Case Comparison — Original × Quick × Fidelity

3 组实验覆盖复杂展陈、复合餐品与单一甜品三种不同输入，用于观察 **Quick Mode** 与 **Fidelity Mode · `dominant_element`** 的差异。

![Three-case Original × Quick × Fidelity comparison](../assets/examples/three-case-comparison.jpg)

## Experiment Matrix

| Case | Original | Quick Mode | Fidelity · `dominant_element` |
|---|---|---|---|
| **01 · 蔬菜农场** | 多主体展陈场景，巨型红番茄、粉色角色与绿色蔬菜同时形成强视觉信息。 | 保留较多场景关系，把多个元素共同转译为白底微缩工作世界，故事密度更高。 | 锁定巨型红番茄为第一视觉信号，仅保留少量蔬菜作为 Scene Lock 辅助线索。 |
| **02 · 海鲜汤** | 一整碗深色汤底包含虾、玉米、丸子等多种配料，中央黄色造型食材最具形状识别度。 | 保留整碗的丰富度，小人分散在不同配料周围工作，强调完整餐品故事。 | 放大并居中强化黄色造型食材，让它先于汤底与其他配料被识别。 |
| **03 · 焦糖饼干冰淇淋** | 金属碗、冰淇淋球、焦糖酱与竖直饼干共同组成主体，饼干是最强形状锚点。 | 保留饼干、冰淇淋与焦糖之间的完整关系，整体信息更均衡。 | 进一步强化焦糖饼干的尺度与位置，让它成为第一视觉中心，冰淇淋与焦糖退居第二层。 |

## What This Comparison Shows

### Quick Mode

更适合第一次探索。它倾向于保留更多输入信息，并快速建立：

```text
摄影主体
+ 微缩小人
+ 产品动作故事
+ 手写标题
```

优势是故事完整、生成速度快；风险是复杂原图容易保留过多元素，第一视觉中心可能不够明确。

### Fidelity Mode · `dominant_element`

适合已经知道“哪一个元素必须最先被看到”的情况。

```text
Subject Lock
→ Scene Lock
→ Focus Lock: dominant_element
→ 削弱次要元素
→ 小人优先服务于核心元素
```

它不是把画面任意简化成一个新物体，而是在保持原始类别、材质与关键结构的前提下，重新建立视觉层级。

## Key Findings

1. **最大的元素必须是最大的“有意义元素”。** 背景建筑、桌面或墙面即使占据更多像素，也不应被选作 Fidelity Focus。
2. **复杂照片需要 Scene Lock。** 保留 1–3 个最关键的场景线索，比完整复制原图更有利于白底海报成立。
3. **Quick 与 Fidelity 的差异首先是视觉优先级，而不是精细度。** Quick 建立完整故事，Fidelity 解决明确的单项问题。
4. **小人必须继续保持辅助地位。** 产品摄影是第一视觉主角，小人负责解释和放大产品特征。
5. **文字与小人仍需单独验收。** 如果字体或角色系统单独失控，应进入对应 Fidelity Focus，而不是重新生成全部内容。

## Regression Targets

下一轮优先继续测试：

- 非食品类单品，例如护肤品、香水、鞋或包；
- 极简单主体照片，检查模型是否会为了“热闹”过度增加小人；
- 带包装文字的产品，检查是否误生成 Logo、标签或伪文字；
- 同一输入分别运行 `subject_identity`、`dominant_element`、`lettering` 三种 Fidelity Focus。