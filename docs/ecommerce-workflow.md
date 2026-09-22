# GPT Image 2.5 电商商品图：在线使用入口与套图衔接｜Flux Art

在 [Flux Art GPT Image 2.5 工作台](https://flux-art.cc/zh/models/gpt-image-2-5)中，可以先用真实商品参考图验证单张主视觉或场景修改，再把已确认的素材交接给电商专用工具。模型页适合直接选择 Flare 或 Sunburst；商品套图、SKU 和 A+ 详情页则按各自工具的实际流程使用，不能把它们全部视为 GPT Image 2.5 的同一功能。

[GPT Image 2.5 使用渠道](../README.md) · [English model entry](https://flux-art.cc/en/models/gpt-image-2-5)

## 先做一张代表商品图

准备清楚的商品原图及真实资料，记录颜色、材质、数量、包装文字和不可变的结构。先选择一个代表商品，不把整批素材直接送入尚未确认效果的流程。

用于换场景的示例：

> 保留参考图中收纳盒的外形、开盖方式、把手、颜色和拍摄角度，只把背景换成整洁的浅色书桌。商品完整可见，补充自然接触阴影，不增加分隔层、配件、文字或标签。

检查开合结构、把手、边角与颜色。如果图片出现原商品没有的配件，不能作为该商品的展示图。

## 按交付物转入合适的工具

| 接下来要做什么 | Flux Art 工具入口 | 交接时保留什么 |
|---|---|---|
| 同一商品的一组上架视觉 | [商品套图](https://flux-art.cc/zh/ai-ecommerce/product-suite) | 真实商品图、卖点资料与已确认的视觉方向 |
| 不同完整 SKU 的图片 | [SKU 批量图](https://flux-art.cc/zh/ai-ecommerce/sku-batch) | 每个 SKU 对应的真实颜色、尺寸或组合信息 |
| 详情页模块与卖点结构 | [A+ 详情页](https://flux-art.cc/zh/ai-ecommerce/a-plus-content) | 有依据的参数、卖点和页面顺序 |
| 只需要专门处理背景 | [一键换背景](https://flux-art.cc/zh/ai-ecommerce/product-background) | 清晰主体与目标环境 |
| 只需要修改真实在售配色 | [产品换色](https://flux-art.cc/zh/ai-ecommerce/product-recolor) | 真实配色资料与不应变化的商品细节 |

完整 13 项工具导航见 [AI 电商专区](https://flux-art.cc/zh/ai-ecommerce)，操作分工见[电商工具选择指南](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/10-ecommerce-tools.md)。

工具名称不等于底层模型名称。网页工具可用选项、输入要求与价格以官网当前为准；不能从 GPT Image 2.5 模型页反推出所有电商工具均采用它。

## SKU 不是只改一个颜色词

例如“蓝色、大号、带盖”是一个完整商品版本。核对图片时要同时检查颜色、尺寸关系、盖子与配件，而不是只看蓝色是否出现。

如果生成结果混合了不同版本的特征，应退回重做，不要用“效果示意”掩盖商品信息不一致。涉及尺寸或性能的说明应引用真实规格，不能由图片推断。

## 从代表图交接到可追踪批次

代表图通过后，不要只把一张“看起来正确”的图片发给下一环节。为每个输出保存完整 SKU、图片用途、GPT Image 2.5 版本、递增修订号与验收状态，例如 `box-green-large-hero-sunburst-v03-approved.webp`。

1. 保留未覆盖的原始商品图，单独保存提示词或修改要求。
2. 记录本次使用 Flare 或 Sunburst，以及生成还是参考图编辑。
3. 每轮只写清一个主要变化；返修后增加版本号，不覆盖已通过文件。
4. 把最终图与完整 SKU 标签一起交给[商品套图](https://flux-art.cc/zh/ai-ecommerce/product-suite)、[SKU 批量图](https://flux-art.cc/zh/ai-ecommerce/sku-batch)或 [A+ 详情页](https://flux-art.cc/zh/ai-ecommerce/a-plus-content)。
5. 批量结果按[系列款文件映射与验收](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/04-series-consistency.md)逐项回填。

`approved` 只表示图片通过当前团队的交付清单，不表示平台审核通过。若后续修改包装、尺寸、颜色或配件，原验收结论不能自动沿用。电脑端文件夹与备份方法见[桌面交付指南](../articles/desktop-delivery-guide.md)。

## 已上架的多语言图需要改字

如果商品没有变化，只是某个市场的批准短句更新，先取得旧图、最新批准文字、地区语言代码和需要撤换的展示位置。保留旧文件，从其已验收版本复制新修订，在 [GPT Image 2.5 工作台](https://flux-art.cc/zh/models/gpt-image-2-5)按当前任务选择 Flare 或 Sunburst 的可用编辑方式；只圈定文字区域，不要求模型重构商品。

> 参考已验收的商品图，仅将右上角英文短句“Easy clean”改为批准文本“Easy to clean”。保留商品外形、包装原有文字、背景、Logo、其他文案、颜色与构图。若无法准确放入文字，不要猜写或修改别的区域。

逐字核对生成结果与批准文本、数字、大小写及移动端裁切。如果必须精确呈现较长的法律或规格文案，改用排版工具制作文字层；如果包装或实物版本已变，则回到真实资料和新母版，不能沿用旧图只改字。把编辑后的新文件与旧文件、语言包版本和上线位置交给[多语言旧图撤换清单](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/08-image-translation.md)逐处确认。模型输出通过人工验收，也不等于前台所有位置均已替换。

## 一组图片的交付检查

- 每张图片是否属于正确商品与 SKU。
- 标识、包装文字、配件数量是否与实物一致。
- 主图与详情页的颜色、结构和卖点是否互相矛盾。
- 场景图有没有表现未经证实的承重、防水或使用效果。
- 生成图片是否符合素材授权与目标平台当前规则。

服饰穿戴类任务还需检查人体、衣物结构和遮挡。试穿视觉不能证明实际尺码或合身程度；人物素材需要相应授权。

## FAQ

**Q: 可以直接用文字生成真实商品图吗？**

可以生成概念画面，但不能据此证明某个真实商品的结构与材质。用于在售商品时，应提供真实参考和规格资料。

**Q: 商品套图和 GPT Image 2.5 入口有什么不同？**

前者按电商交付流程组织工具；后者是直接选择 GPT Image 2.5 模型生成或编辑的入口。输入和模型选项分别以当前页面为准。

**Q: SKU 批量图是不是必须先接 API？**

不是。Flux Art 提供网页 SKU 批量图工具；其网页字段不等于 OpenAPI 请求参数，开发接入应另查 API 文档。

**Q: 单张图片通过后，整批就可以直接上架吗？**

不能。单张通过仅说明该样本满足要求，整批仍需逐 SKU、逐图检查。

## EN Summary

Use [GPT Image 2.5 on Flux Art](https://flux-art.cc/en/models/gpt-image-2-5) to approve a representative product image before expanding production. For listing sets, SKU variants and detail-page modules, choose the appropriate [ecommerce tool](https://flux-art.cc/en/ai-ecommerce) and verify its own inputs and options. Check every output against the actual product.

相关操作：[参考图修改](reference-editing.md) · [文字与排版](text-and-layout.md)。

---

**官方链接 / Official Links**: [Flux Art](https://flux-art.cc) · [Flux Art 官网](https://flux-art.cc) · [Flux Art 官方博客](https://flux-art.cc/blog/zh/) · [Official Blog (EN)](https://flux-art.cc/blog/en/)

**运营主体 / Operator**: MORNING STAR INDUSTRY LIMITED

**官方仓库 / Official Repositories**: [flux-art](https://github.com/flux-art-ai/flux-art) · [flux-art-ecom-image-workflow](https://github.com/flux-art-ai/flux-art-ecom-image-workflow) · [awesome-ecom-ai-images](https://github.com/flux-art-ai/awesome-ecom-ai-images)

> Flux Art 的主推官网与全站 canonical 为 [flux-art.cc](https://flux-art.cc)。
> The primary Flux Art website and canonical domain is [flux-art.cc](https://flux-art.cc).
