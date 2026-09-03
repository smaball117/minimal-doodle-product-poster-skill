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
reference_image: "【可选】"
```

If `feature`, `caption`, or worker actions are missing, infer them from the subject before writing the final prompt.

If a reference image is provided, first lock the exact product identity. Preserve category, silhouette, color, surface material, topping/garnish, and plate/container relationship when important. Do not transform one food type into another.

---

## Step 1 — Base visual and composition

```text
请设计一张极简治愈系产品海报，整体气质高级、安静、有呼吸感，采用国际品牌产品广告式的大面积留白，而不是传统插画海报。

背景为纯白色，约 70%–80% 为干净留白。画面只保留一个真实摄影质感的核心主体【subject】，主体居中偏下，整体构图简洁克制。若提供参考照片，必须还原参考图中主体的真实品类、外形轮廓、主色、表面材质、顶部装饰和关键比例，不擅自把主体改成其他食物或物品。主体采用专业商业静物摄影质感，摄影棚大面积柔光，高键、低反差，材质、表面纹理和细节真实清晰，主体下方只有轻柔自然的接触阴影。

在真实摄影主体周围加入少量黑色手绘线稿。线条像黑色马克笔或签字笔随手画出，略微不规则、稚拙、松弛、有童趣，但保持简洁，不做精致插画。线稿可包含微缩小人、梯子、箭头、波浪线、云朵及与主体特性相关的简单工具。

微缩小人为统一角色系统：圆头、无五官、无表情、无发型、无帽子、无服饰细节、无标签、无 Logo、无身体装饰，只保留极简黑色单线轮廓。动作通过身体姿势和工具表达，不依靠表情和服装。微缩小人的动作必须围绕主体展开，像一群人在认真工作。每一个动作都要直接表达【feature】，把主体变成一个巨大的微缩工作现场，而不是在周围随机摆放可爱角色。
```

---

## Step 2 — Style controls and exclusions

```text
整体风格保持克制、留白充足、真实摄影高级、安静治愈，并带有轻微幽默和微缩故事感。真实摄影主体是第一视觉重点，黑色线稿只是叙事层，不能抢过主体。

字体采用稚拙、松散、细黑线手写感。不要标准字体，不要书法，不要圆润可爱字体，不要工整排版。字形允许轻微歪斜、大小不一、横画偶尔拉长、结构松散、字距不均，但保持可辨认。文字要参与构图，不必像正式标题一样端正。文案根据主体特点生成，可以带一点轻松感、谐音或产品灵感，字数尽量短以减少错字风险。

颜色只使用【color_palette】，除主体本身颜色外不增加额外装饰色。画面保持纯白背景、黑色单线手绘与真实摄影材质之间的强对比。

不要品牌 Logo，不要边框，不要复杂排版，不要价格标签，不要大段广告文案，不要彩色插画，不要精致矢量人物，不要有表情的小人，不要服装化角色，不要 3D 卡通，不要动漫漫画感，不要复杂场景，不要多主体拼贴，不要把真实主体画成插画或塑料感 3D 模型，不要明显 AI 绘画质感。
```

---

## Step 3 — Subject-specific scene

```text
主体是【subject】。

若有参考照片，主体必须保持参考照片中的真实品类和基本外观，不改变成其他物体。主体摄影细节：
【用 1–3 句描述最能强化 subject 材质、温度、状态、表面纹理和食欲/触感的真实摄影细节】

画面里有【worker_count】个黑色单线稿微缩小人。所有小人均为圆头、空白脸、无五官、无表情、无服饰、无标签的极简人形，他们分别在做与【feature】直接相关的工作：
1. 【动作 1】
2. 【动作 2】
3. 【动作 3】
4. 【动作 4】
5. 【动作 5，可选】

这些动作必须形成一个完整的微缩工作现场，并且每个动作都能让人联想到主体的一项真实特征。工具可以出现，但人物本身不做职业服装或角色装扮。

画面左上或左侧空白区域，用稚拙、松散、细黑线的随手写字体写：【caption】。字形可以轻微歪斜、大小不一、横画拉长、结构松散，避免标准字体感。旁边画一条松弛的手绘弯箭头指向主体。文字不是正式标题，而是构图的一部分。

最终颜色严格控制为【color_palette】。整体画面清爽、安静、留白巨大，主体摄影真实高级，线稿轻巧幽默。
```

---

# Automatic idea generation

When only a subject is provided, generate the missing variables in this order:

## 1. Lock the object category

If the user provides a reference image, state internally what the object is before generating metaphors. Preserve its category, shape, main color, topping, and material.

Example:

```text
blue molded pudding ≠ shaved ice
pudding remains pudding
```

## 2. Find the strongest sensory features

Choose 2–4 from:

- taste;
- temperature;
- texture;
- moisture;
- bubbles;
- softness;
- jiggle/bounce;
- creaminess;
- ripeness;
- transparency;
- weight;
- seeds/pulp/peel;
- emotional association.

Prefer features that can be physically staged.

## 3. Turn each feature into a job

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
soft pudding → tasting/testing → using a tiny spoon
```

## 4. Generate the caption

The caption should usually be 2–6 Chinese characters and connect to the strongest feature.

The writing style is more important than formal typography:

```text
thin black strokes
naive and loose
slightly tilted
uneven size
irregular spacing
occasionally elongated horizontal strokes
```

Useful content structures:

```text
【状态】中
正在【动作】
今天有点【感受】
请勿【动作】
【感受】下午茶
```

Light wordplay or a gentle homophone is acceptable when natural. Do not force it.

---

# Prompt writing rules

1. Use concrete visual descriptions instead of abstract praise.
2. If there is a source photo, preserve the product identity before adding style.
3. State the photographic material details explicitly.
4. Keep the negative prompt short enough that it does not drown out the desired image.
5. Do not add unrelated props merely to make the picture “richer”.
6. Do not create more than one hero photographic subject.
7. Doodle people must remain secondary and much smaller than the subject.
8. Every doodle person must be round-headed, blank-faced, expressionless, unclothed in appearance, and free of labels or decorative body details.
9. Handwritten text must feel loose and imperfect, never like a standard font.
10. Preserve the three-step output structure in the final response.