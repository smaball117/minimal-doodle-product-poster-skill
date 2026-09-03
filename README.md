# Minimal Doodle Product Poster Skill

极简留白 × 真实产品摄影 × 黑色手绘微缩小人叙事的可复用 AI 生图 Skill。

> 这套视觉在日常交流里可以被称为“喜茶风”，但本项目使用中性、可复用的视觉语言描述它：**Minimal Product Photography + Doodle Micro-Storytelling**。目标不是复刻某个品牌，而是提炼一种可迁移的视觉方法。

## 这套 Skill 能做什么

给定一个水果、饮品、甜品或清凉物件，自动完成：

1. 提炼主体最值得被视觉化的产品特征；
2. 为主体设计 4–5 个“围绕产品认真工作”的手绘微缩小人动作；
3. 生成一句 2–6 字的情绪化手写短句；
4. 控制留白、构图、摄影质感、线稿密度与色彩范围；
5. 输出可直接用于图片生成模型的三段式完整提示词。

## 风格公式

```text
大面积白色留白
+ 单一真实摄影主体
+ 居中偏下构图
+ 黑色随手线稿
+ 微缩小人功能性动作
+ 极短手写情绪文案
= 极简、治愈、安静、有故事感的产品海报
```

## 最重要的规则

- 主体必须保持真实摄影质感，不做插画化。
- 画面约 70%–80% 为纯白留白。
- 一个画面只保留一个核心主体。
- 小人不是随机装饰，每一个动作都必须解释或放大产品特性。
- 线稿只使用黑色单线，松弛、稚拙、像马克笔随手画，不做精致漫画。
- 颜色只来自产品本身，尽量不额外引入新颜色。
- 文案短、轻、像便签，不做复杂广告排版。

## 快速使用

最少只需要告诉 Skill 一个主体：

```text
帮我做一张西瓜主题海报。
```

更稳定的输入方式：

```yaml
subject: 冰镇西瓜
feature: 多汁、清凉、夏日补水
caption: 补水中
worker_count: 5
color_palette: 红、绿、白
```

Skill 会输出三段式提示词：

```text
1. 基础视觉与构图规则
2. 风格控制与负面约束
3. 当前主体、微缩动作、文案与颜色
```

## 文件结构

```text
minimal-doodle-product-poster-skill/
├── README.md
├── SKILL.md
├── docs/
│   └── style-analysis.md
├── prompts/
│   └── prompt-template.md
└── examples/
    └── watermelon.md
```

## 文档入口

- `SKILL.md`：Skill 的执行规则，给 Agent / Codex 使用。
- `docs/style-analysis.md`：风格视觉 DNA、构图、线稿、叙事机制与常见跑偏分析。
- `prompts/prompt-template.md`：三段式提示词母版与变量说明。
- `examples/watermelon.md`：西瓜案例，从输入到最终 Prompt 的完整演示。

## 当前版本

**v0.1 — Foundation**

第一阶段先把“风格识别 + 叙事逻辑 + Prompt 输出”做稳定。后续再逐步增加参考图分析、自动生成多个创意方向、模型适配和案例库。