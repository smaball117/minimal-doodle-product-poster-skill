# Apple Tea Test — 心态放苹

同一组苹果冰茶素材，用来验证“真实摄影主体 + 无脸微缩小人 + 手写标题”的基础结构，以及 Quick / Fidelity 两种路径的职责边界。

## Visual Comparison

| Original | Quick Mode | Fidelity Mode |
|---|---|---|
| <img src="../assets/examples/apple-tea/source-original.jpg" width="220" alt="两杯苹果冰茶、苹果切片和整颗红苹果的原始照片" /> | <img src="../assets/examples/apple-tea/quick-mode-original.png" width="220" alt="苹果冰茶 Quick Mode 海报" /> | <img src="../assets/examples/apple-tea/fidelity-mode-original.png" width="220" alt="苹果冰茶 Fidelity Mode 海报" /> |
| **输入基准**：两杯苹果冰茶、苹果切片、冰块、迷迭香与黄橙红渐变。 | **快速路径**：一轮建立主体、微缩工作与标题。 | **高保真路径**：保持已接受的主体和版式，只加强一个指定 Focus。 |

> **对照说明**：三张图现在各自对应 Original、Quick Mode 与 Fidelity Mode。对比时先确认主体身份和场景线索仍被保留，再观察 Fidelity 是否只强化了指定 Focus。

## Test Input

```yaml
subject: 两杯苹果冰茶与整颗苹果
scene_lock: 双杯、苹果切片、冰块、木桌与暖色饮品渐变
features: 清爽冰感、苹果切片、黄橙红渐变、红苹果
caption: 心态放苹
worker_system: blank round head, faceless, expressionless, no clothing
mode: quick | fidelity
fidelity_focus: dominant_element # 仅在 fidelity 时指定
```

## What This Case Tests

1. **Subject Lock**：海报主角必须仍是苹果冰茶；双杯、透明杯体、冰块、苹果切片和渐变是优先保留的识别线索。
2. **Scene Lock**：保留暖色桌面或整颗红苹果即可提示来源，不必复制完整咖啡店背景。
3. **Quick Mode**：用一次生成建立可读的产品、微缩动作和标题，优先验证整套视觉语言是否成立。
4. **Fidelity Mode**：若“苹”是语义钩子，可选择 `dominant_element`，让红苹果或苹果切片更早被看见；其余结构保持稳定。
5. **Worker Contract**：小人用姿态、工具和与冰块／苹果片的接触关系讲故事，不能带五官、服装、帽子或角色标签。
6. **Lettering**：`心态放苹` 应短、松散、细黑线、略不规则；“苹”可与苹果形成语义呼应，但不能变成标准字体。

## Evaluation

- [ ] 主体仍明确为苹果冰茶，而非泛化的橙色饮料。
- [ ] 杯体、冰块、苹果切片与黄橙红渐变至少保留大部分关键识别信息。
- [ ] 摄影主体保持真实材质，白色留白仍占主导。
- [ ] 每个小人都在执行与产品特征相关的动作，而非纯装饰。
- [ ] 小人无五官、表情、服装、帽子、标签或品牌元素。
- [ ] 标题可读，但没有变成标准电脑字体或工整书法。
- [ ] 若采用 Fidelity，只有选定 Focus 被明显加强，其他已接受结构不被无故重做。
