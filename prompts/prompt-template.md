# Prompt Template

This project keeps the user's preferred three-step prompt structure. Do not collapse the three sections into one paragraph.

## Input variables

```yaml
subject: "【主体】"
feature: "【主体特点】"
caption: "【情绪短句】"
worker_count: "【4–5】"
color_palette: "【主体色 + 白 + 黑】"
aspect_ratio: "【默认竖版】"
```

If `feature`, `caption`, or worker actions are missing, infer them from the subject before writing the final prompt.

---

## Step 1 — Base visual and composition

```text
请设计一张极简治愈系产品海报，整体气质高级、安静、有呼吸感，采用国际品牌产品广告式的大面积留白，而不是传统插画海报。

背景为纯白色，约 70%–80% 为干净留白。画面只保留一个真实摄影质感的核心主体【subject】，主体居中偏下，整体构图简洁克制。主体采用专业商业静物摄影质感，摄影棚大面积柔光，高键、低反差，材质、表面纹理和细节真实清晰，主体下方只有轻柔自然的接触阴影。

在真实摄影主体周围加入少量黑色手绘线稿。线条像黑色马克笔或签字笔随手画出，略微不规则、稚拙、松弛、有童趣，但保持简洁，不做精致插画。线稿可包含微缩小人、梯子、箭头、波浪线、云朵及与主体特性相关的简单工具。

微缩小人的动作必须围绕主体展开，像一群人在认真工作。每一个动作都要直接表达【feature】，把主体变成一个巨大的微缩工作现场，而不是在周围随机摆放可爱角色。
```

---

## Step 2 — Style controls and exclusions

```text
整体风格保持克制、留白充足、真实摄影高级、安静治愈，并带有轻微幽默和微缩故事感。真实摄影主体是第一视觉重点，黑色线稿只是叙事层，不能抢过主体。

颜色只使用【color_palette】，除主体本身颜色外不增加额外装饰色。画面保持纯白背景、黑色单线手绘与真实摄影材质之间的强对比。

不要品牌 Logo，不要边框，不要复杂排版，不要价格标签，不要大段广告文案，不要彩色插画，不要精致矢量人物，不要 3D 卡通，不要动漫漫画感，不要复杂场景，不要多主体拼贴，不要把真实主体画成插画或塑料感 3D 模型，不要明显 AI 绘画质感。
```

---

## Step 3 — Subject-specific scene

```text
主体是【subject】。

主体摄影细节：
【用 1–3 句描述最能强化 subject 材质、温度、状态、表面纹理和食欲/触感的真实摄影细节】

画面里有【worker_count】个黑色单线稿微缩小人，他们分别在做与【feature】直接相关的工作：
1. 【动作 1】
2. 【动作 2】
3. 【动作 3】
4. 【动作 4】
5. 【动作 5，可选】

这些动作必须形成一个完整的微缩工作现场，并且每个动作都能让人联想到主体的一项真实特征。

画面左上或左侧空白区域，用黑色随手写字体写：【caption】。旁边画一条松弛的手绘弯箭头指向主体。文字体量很小，不做正式字体排版。

最终颜色严格控制为【color_palette】。整体画面清爽、安静、留白巨大，主体摄影真实高级，线稿轻巧幽默。
```

---

# Automatic idea generation

When only a subject is provided, generate the missing variables in this order:

## 1. Find the strongest sensory features

Choose 2–4 from:

- taste;
- temperature;
- texture;
- moisture;
- bubbles;
- softness;
- ripeness;
- transparency;
- weight;
- seeds/pulp/peel;
- emotional association.

Prefer features that can be physically staged.

## 2. Turn each feature into a job

Use this conversion pattern:

```text
product feature → physical metaphor → miniature job
```

Example:

```text
juicy → water system → watering with hose
seeds → cargo → transporting seeds
cold → cooling system → running fan / measuring temperature
sweet → quality control → checking sweetness
```

## 3. Generate the caption

The caption should usually be 2–6 Chinese characters and connect to the strongest feature.

Useful structures:

```text
【状态】中
正在【动作】
今天有点【感受】
请勿【动作】
【感受】营业中
```

Do not force these structures if a more natural phrase exists.

---

# Prompt writing rules

1. Use concrete visual descriptions instead of abstract praise.
2. State the photographic material details explicitly.
3. Keep the negative prompt short enough that it does not drown out the desired image.
4. Do not add unrelated props merely to make the picture “richer”.
5. Do not create more than one hero photographic subject.
6. Doodle people must remain secondary and much smaller than the subject.
7. Preserve the three-step output structure in the final response.