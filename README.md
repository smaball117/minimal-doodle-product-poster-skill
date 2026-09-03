# Minimal Doodle Product Poster Skill

极简留白 × 真实产品摄影 × 无脸微缩小人 × 稚拙细线中文的可复用 AI 生图 Skill。

> 这套视觉常被口语化称为“喜茶风”，但本项目使用中性的可迁移语言描述它：**Minimal Product Photography + Doodle Micro-Storytelling**。目标不是复刻某个品牌，而是提炼一种可复用的视觉方法。

## v0.3 核心升级

从“一个很长的 Prompt”升级为“工作流 + 专项规则 + 评估测试”。

```text
上传照片
→ 锁定真实主体
→ 提炼产品特征
→ 生成微缩工作动作
→ 选择 Quick / Fidelity 模式
→ 生成海报
→ 按 Evaluation 规则验收
```

## 风格公式

```text
70%–80% 白色留白
+ 单一真实摄影主体
+ 居中偏下构图
+ 黑色稚拙线稿
+ 4–5 个无脸圆头微缩小人
+ 产品相关动作叙事
+ 稚拙、松散、细黑线中文
= 安静、清爽、治愈、有故事感的产品海报
```

## 两种生成模式

### Quick Mode

适合快速测试。主体、小人和文字一次生成。

### Fidelity Mode

当用户强调主体还原或字体像参考时使用：

1. 先生成无文字 Poster Base；
2. 单独生成 Lettering Layer；
3. 最后合成。

这样修改字体时，不会重新洗掉主体、小人和构图。

## 最重要的 5 条规则

1. **Subject Lock**：先确认“它是什么”，再做创意。布丁不能因为“蓝色 + 清凉”被改成刨冰。
2. **Photography First**：真实产品摄影永远是第一视觉锚点，不做全图卡通化。
3. **Worker ≠ Decoration**：每个小人必须有产品相关工作，不能为了热闹随机加人。
4. **Fixed Figure System**：圆头、无五官、无表情、无发型、无服饰、无标签，只靠动作表达。
5. **Lettering Is a System**：目标不是“手写字体贴图”，而是稚拙字形骨架 + 细黑线笔画 + 松散构图。

## 推荐输入

只给一张照片也可以。更稳定时可补充：

```yaml
subject: 蓝色布丁
feature: 清凉、Q弹、奶油、樱桃
caption: 清甜下午茶
worker_count: 4
color_palette: 浅蓝、奶油白、樱桃红、黑、白
mode: quick | fidelity
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
│   ├── micro-worker-guide.md
│   ├── lettering-guide.md
│   └── evaluation.md
├── prompts/
│   ├── quick-prompt.md
│   ├── poster-base.md
│   └── lettering-layer.md
├── evals/
│   └── evals.json
└── examples/
    ├── watermelon.md
    └── blue-pudding.md
```

## 当前测试结论

- 西瓜案例验证了“产品特征 → 微缩工作”的叙事逻辑。
- 蓝色布丁案例暴露并修复了“主体漂移”：布丁曾被错误转成刨冰。
- 蓝色布丁第二轮验证了固定小人系统：圆头、无脸、无服饰。
- “清甜下午茶”测试暴露了字体需要独立控制字形骨架，而不能只堆“手写感”形容词。

## 发布边界

仓库不默认包含官方品牌 Logo、吉祥物、包装标识或第三方参考图。第三方素材仅用于视觉研究，具体见 `ASSET-NOTICE.md`。

## 当前版本

**v0.3 — Modular Workflow**

下一阶段目标：继续用不同品类实拍图做回归测试，并把失败案例沉淀进 `evals/evals.json`。