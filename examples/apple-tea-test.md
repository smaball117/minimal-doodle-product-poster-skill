# Apple Tea Test — 心态放苹

使用同一张苹果冰茶实拍素材，验证 Skill 的标准海报结构与两种生成路径。

## Visual Comparison

| Original | Quick Mode | Fidelity Mode |
|---|---|---|
| ![Original apple tea photo](../assets/examples/apple-tea/source.jpg) | ![Apple tea Quick Mode](../assets/examples/apple-tea/quick-mode.jpg) | ![Apple tea Fidelity Mode](../assets/examples/apple-tea/fidelity-mode.jpg) |
| **输入基准**：苹果冰茶、苹果切片、冰块与黄橙红渐变饮品。 | **快速路径**：主体、微缩小人与标题一次生成，用于快速建立完整视觉。 | **高保真路径**：在保留主体和版式的基础上，针对指定 Focus 做单项强化。 |

## Test Input

```yaml
subject: 苹果冰茶
caption: 心态放苹
worker_system: blank round head, faceless, expressionless, no clothing
mode: quick | fidelity
```

## What This Case Tests

1. **Subject Lock**：从真实场景中提取苹果冰茶作为摄影主角，去除咖啡店环境干扰，同时保留杯体、冰块、苹果切片和饮品渐变等识别信息。
2. **Quick Mode**：验证“真实摄影主体 + 黑色微缩小人 + 稚拙手写标题”能否一次建立完整海报。
3. **Fidelity Mode**：验证已经成立的海报能否在不推翻整体结构的情况下，对单一目标继续强化。
4. **Worker Contract**：小人保持圆头、无五官、无表情、无服饰，叙事只通过姿态、工具与主体接触关系完成。
5. **Lettering**：标题 `心态放苹` 必须保持短、松散、细黑线手写，并让“苹”与苹果视觉线索形成语义联系。

## Evaluation

- [ ] 主体仍然明确是苹果冰茶，而不是泛化的橙色饮料。
- [ ] 摄影主体保持真实材质，不被整体卡通化。
- [ ] 白色留白占主导，海报没有被装饰元素填满。
- [ ] 每个小人都与产品特征发生实际关系。
- [ ] 小人没有五官、表情、服装、帽子或角色标签。
- [ ] 标题没有变成标准电脑字体或工整书法。

> **Asset QA note**：当前重新提供的两张生成结果文件内容一致，因此本案例不把这两张文件本身作为 Quick / Fidelity 差异的视觉证据。后续只需替换 `fidelity-mode` 资产即可继续保留同一测试结构。