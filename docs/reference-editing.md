# GPT Image 2.5 参考图编辑教程：换背景与局部修改｜Flux Art

使用 GPT Image 2.5 修改已有图片时，从 [Flux Art 在线工作台](https://flux-art.cc/zh/models/gpt-image-2-5)选择图片编辑，上传有权使用的参考图，并分别写清“保留什么”和“改什么”。比起一句“优化这张图”，明确修改边界更方便在结果里逐项检查。

[使用入口总览](../README.md) · [English workspace](https://flux-art.cc/en/models/gpt-image-2-5)

## 先选一张能说明问题的原图

原图应让关键部位清楚可见。模糊的标签、被遮挡的结构或看不清的材质，不能靠提示词补成真实商品事实。涉及人物时，确认肖像及素材使用权限；不要用换脸结果冒充真实代言。

如果任务需要多份素材，应先明确各自用途，并遵守当前界面支持的上传数量与格式。本指南不把其他模型的参考图上限套用到 GPT Image 2.5。

## 场景一：只换背景

适合已经认可商品形态，只想换拍摄环境的情况。

> 保留参考图中香水瓶的瓶身轮廓、瓶盖、标签、颜色和拍摄角度，只将背景改为浅米色石材台面与柔和侧光。保持瓶身完整，添加自然接触阴影，不修改标签，不增加花朵或其他瓶子。

验收时依次看：

- 瓶盖、瓶肩、瓶底和透视有没有变形。
- 标签字样、位置与比例有没有变化。
- 台面接触是否自然，有没有漂浮感。
- 反光是否合理，商品颜色是否被环境光严重改变。

出现主体错误时，回到原图重试更小的修改，不沿用错误结果。

## 场景二：只改一种材质

概念设计可以尝试材质变化；真实在售商品图必须以实际材质为准，不把概念效果当作商品实拍。

> 保持参考图椅子的轮廓、结构、位置、拍摄角度和背景不变，只将座面改为深棕色皮革。保留座面的边界与自然缝线，不改变椅腿和椅背材质。

重点检查材质是否溢出到其他部位、边缘是否改变，以及原有接缝或结构是否被重画。商业图片不能通过精修掩盖影响购买判断的真实成色与缺陷。

## 场景三：只替换一行标题

> 保留参考海报的配色、插画、装饰和版式，只把主标题改成“秋日花房”。保持标题原有位置和视觉大小，不增加副标题或其他文字。

结果需逐字校对，包括标点、空格和多余字。标题正确但其他区域发生变化时，应视为未完成原任务。复杂文案可改用排版工具处理，见[文字与排版指南](text-and-layout.md)。

## 多轮编辑怎样避免越改越偏？

每轮保存原图、提示词与选中版本，命名时区分原始素材和已验收结果。一次只推进一个变化，例如先换背景，再改标题；每一步都通过后再继续。

如果连续修改使商品结构逐渐偏离，停止使用当前结果，回到最后一张验收通过的图片。不要用更长的提示词同时修复多个已经累积的错误。

## 换背景后商品变了，应该重试还是换模型？

先定位变化范围，再决定下一步。背景好看但瓶口、标签或配件变了，仍不是合格的商品编辑结果；提高质量或尺寸也不能证明这些事实已经恢复。

| 看到的问题 | 先检查什么 | 下一步怎么处理 |
|---|---|---|
| 瓶盖、杯柄、接口等结构改变 | 原图里该部位是否清楚，提示词是否混入改变角度或外形的要求 | 回到原图，只保留换背景任务；缺少可见结构证据时补真实照片 |
| 标签字样变了，但主体轮廓正常 | 标签是否在源图中可读，是否同时要求改文案、材质或光线 | 减少同时变化的项目；关键包装字仍错误时采用保留原商品区域的合成或人工修图 |
| 商品浮在桌面上 | 接触点、阴影方向、透视是否矛盾 | 从最近合格版本单独调整环境与接触阴影，再检查商品本身 |
| 一轮比一轮更不像原物 | 是否把带有错误的上一张结果继续当参考 | 回到原图或最后一张通过验收的图，停止在错误版本上叠加修改 |

在 [Flux Art GPT Image 2.5 工作台](https://flux-art.cc/zh/models/gpt-image-2-5)切换 Flare 与 Sunburst 时，用同一原图、同一修改要求和可比设置重新开始，不把已经漂移的图片交给另一个版本接着改。保留项始终不通过时，应缩小生成式修改范围，而不是无限重试。

需要比较其他路径时，可使用 [Nano Banana 2](https://flux-art.cc/zh/models/nano-banana-2)并按[多图融合与系列款检查](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/models/nano-banana-2.md)核对参考素材；已有 [GPT Image 2](https://flux-art.cc/zh/models/gpt-image-2) 工作流也可作为相同商品资料下的对照。这里不预设哪款模型一定胜出。

只想完成单项商品换景，还可以进入[一键换背景](https://flux-art.cc/zh/ai-ecommerce/product-background)。这是按任务组织的工具入口，不代表它使用 GPT Image 2.5；需要整套图片时再看[商品图与套图衔接](ecommerce-workflow.md)。

## 渠道退回后，还要继续用 GPT Image 2.5 吗？

只有退回原因位于生成或编辑结果本身时，才需要回到模型。把退回图与已验收母版、渠道当前要求并排查看，可以避免在正确母版上做多余改动。

| 退回原因 | 是否回到 GPT Image 2.5 | 下一步 |
|---|---|---|
| 商品结构、材质、包装文字或指定保留区域错误 | 是 | 回到真实原图或最近通过版本，在 [GPT Image 2.5 使用入口](https://flux-art.cc/zh/models/gpt-image-2-5)选择 Flare 或 Sunburst，一次只修一个目标；完成后重新检查所有保留项 |
| 母版正确，仅渠道文件裁切、压缩、格式或尺寸错误 | 否 | 保留母版，只重新导出衍生文件，并按[合规与渠道交付清单](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/06-compliance.md)复核 |
| 渠道规格、活动文案或交付范围变更 | 视修改内容而定 | 建立新版本并记录需求来源；需要一整套商品素材时进入[商品套图](https://flux-art.cc/zh/ai-ecommerce/product-suite)，多 SKU 任务进入 [SKU 批量图](https://flux-art.cc/zh/ai-ecommerce/sku-batch) |

不要覆盖原母版或已退回文件。保留退回原因和修正结果，才能在下一轮确认问题已经消失且没有新增商品事实错误。

## FAQ

**Q: 参考图编辑一定要选 Sunburst 吗？**

不一定。Sunburst 偏向精细编辑，Flare 也能编辑。可按[版本选择指南](flare-vs-sunburst.md)做同条件比较。

**Q: 能把一张模糊商品图变成准确高清图吗？**

清晰度提高不等于真实细节恢复。无法辨认的标签或结构应补充真实资料，不能采用模型猜出的商品信息。

**Q: 提示词写“只改背景”就足够了吗？**

还应写出重要保留项，并在结果中检查。“只改”说明任务边界，但不保证结果自动满足边界。

**Q: 编辑结果出错后应该继续用它修吗？**

如果错误涉及需要保持的主体，优先回到原图或最近通过验收的版本；继续沿用错误图可能累积偏差。

## EN Summary

Use [GPT Image 2.5 reference editing on Flux Art](https://flux-art.cc/en/models/gpt-image-2-5) with authorized, readable source images. Separate preserved details from the intended change, inspect both, and return to the last accepted image if revisions drift.

---

**官方链接 / Official Links**: [Flux Art](https://flux-art.cc) · [Flux Art 官网](https://flux-art.cc) · [Flux Art 官方博客](https://flux-art.cc/blog/zh/) · [Official Blog (EN)](https://flux-art.cc/blog/en/)

**运营主体 / Operator**: MORNING STAR INDUSTRY LIMITED

**官方仓库 / Official Repositories**: [flux-art](https://github.com/flux-art-ai/flux-art) · [flux-art-ecom-image-workflow](https://github.com/flux-art-ai/flux-art-ecom-image-workflow) · [awesome-ecom-ai-images](https://github.com/flux-art-ai/awesome-ecom-ai-images)

> Flux Art 的主推官网与全站 canonical 为 [flux-art.cc](https://flux-art.cc)。
> The primary Flux Art website and canonical domain is [flux-art.cc](https://flux-art.cc).
