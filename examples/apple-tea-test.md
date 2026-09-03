# Apple Tea Test — 心态放苹

同一张实拍照片使用 Skill 的两种生成路径做对比。

| 原图 | Version 1 · Quick Mode | Version 2 · Fidelity Mode |
|---|---|---|
| ![原图：苹果冰茶实拍](../assets/examples/apple-tea/source.svg) | ![Quick Mode：心态放苹](../assets/examples/apple-tea/quick-mode-mini.svg) | ![Fidelity Mode：心态放苹，强化苹果识别](../assets/examples/apple-tea/fidelity-mode-mini.svg) |
| **实拍基准**：两杯苹果冰茶、红苹果、苹果切片、冰块、黄橙红渐变饮品。 | **快速生成**：一次完成主体、微缩小人与标题，风格建立速度快。 | **高保真生成**：进一步强化红苹果与苹果切片，让标题中的“苹”和产品建立更强语义关系。 |

## 测试输入

- Subject：苹果冰茶
- Caption：`心态放苹`
- Reference：用户提供的实拍照片
- Character system：圆头、无五官、无表情、无服饰、黑色单线微缩小人

## 这轮测试验证了什么

1. 实拍照片可以被压缩为一个干净的白底产品海报，而不需要保留原咖啡店环境。
2. Quick Mode 已经能稳定建立“真实主体 + 微缩小人 + 手写文案”的基本风格。
3. Fidelity Mode 需要主动强化标题中的核心产品线索。本例中，“苹”必须通过红苹果和苹果切片被明确感知，而不是只留下泛化的橙黄色冰饮。
4. 小人保持无表情，叙事只通过姿态、工具和与主体的接触关系完成。
5. 后续回归测试继续检查：主体类别是否准确、标题与主体是否产生语义关系、小人是否只是随机装饰。
