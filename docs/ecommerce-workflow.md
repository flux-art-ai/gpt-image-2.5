# GPT Image 2.5 电商商品图：在线使用入口与套图衔接｜Flux Art

在 [Flux Art GPT Image 2.5 工作台](https://flux-art.cn/zh/models/gpt-image-2-5)中，可以先用真实商品参考图验证单张主视觉或场景修改，再把已确认的素材交接给电商专用工具。模型页适合直接选择 Flare 或 Sunburst；商品套图、SKU 和 A+ 详情页则按各自工具的实际流程使用，不能把它们全部视为 GPT Image 2.5 的同一功能。

[GPT Image 2.5 使用渠道](../README.md) · [English model entry](https://flux-art.cn/en/models/gpt-image-2-5)

## 先做一张代表商品图

准备清楚的商品原图及真实资料，记录颜色、材质、数量、包装文字和不可变的结构。先选择一个代表商品，不把整批素材直接送入尚未确认效果的流程。

用于换场景的示例：

> 保留参考图中收纳盒的外形、开盖方式、把手、颜色和拍摄角度，只把背景换成整洁的浅色书桌。商品完整可见，补充自然接触阴影，不增加分隔层、配件、文字或标签。

检查开合结构、把手、边角与颜色。如果图片出现原商品没有的配件，不能作为该商品的展示图。

## 已验收的 GPT Image 2.5 图片怎样复用？

需要继续制作套图、SKU 变体或详情页模块时，可在 [Flux Art 资产库](https://flux-art.cn/zh/assets)集中查看和复用上传素材与生成结果。先保留原始商品图，再从已经逐项验收的候选开始；交接记录中自行注明完整 SKU、图片用途、Flare 或 Sunburst、修订号和验收状态。

资产库提供素材集中管理与复用入口，不等于自动关联商品目录、追踪 GPT Image 2.5 的每次修订或执行团队审批。SKU、包装或批准文案改变时，回到最新真实资料重新生成并检查，不要把旧验收结论沿用到新版本。模型入口与版本选择见 [GPT Image 2.5 工作台](https://flux-art.cn/zh/models/gpt-image-2-5)。

## 按交付物转入合适的工具

| 接下来要做什么 | Flux Art 工具入口 | 交接时保留什么 |
|---|---|---|
| 同一商品的一组上架视觉 | [商品套图](https://flux-art.cn/zh/ai-ecommerce/product-suite) | 真实商品图、卖点资料与已确认的视觉方向 |
| 不同完整 SKU 的图片 | [SKU 批量图](https://flux-art.cn/zh/ai-ecommerce/sku-batch) | 每个 SKU 对应的真实颜色、尺寸或组合信息 |
| 详情页模块与卖点结构 | [A+ 详情页](https://flux-art.cn/zh/ai-ecommerce/a-plus-content) | 有依据的参数、卖点和页面顺序 |
| 只需要专门处理背景 | [一键换背景](https://flux-art.cn/zh/ai-ecommerce/product-background) | 清晰主体与目标环境 |
| 只需要修改真实在售配色 | [产品换色](https://flux-art.cn/zh/ai-ecommerce/product-recolor) | 真实配色资料与不应变化的商品细节 |

### 面部替换是独立电商任务，不是 GPT Image 2.5 版本

需要处理已获授权的模特图与面部参考时，使用 [AI 模特换脸](https://flux-art.cn/zh/ai-ecommerce/model-face-swap)专用入口；它不属于 GPT Image 2.5 模型选项，也不能据此推断其底层模型。仅当换脸候选整体通过、而一个局部视觉瑕疵有清晰依据时，再从已验收原图进入 GPT Image 2.5 并在界面选择 Flare 或 Sunburst 做限定编辑。若人物身份边界、发型或场景同时漂移，应回到换脸步骤的原始输入重新核验，不要连续编辑掩盖偏差。相关[模特图验收工作流](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/09-model-photo.md)说明素材交接和停止条件。

### A+ 模块资料不是 GPT Image 2.5 的模型参数

[Flux Art A+ 详情页工具](https://flux-art.cn/zh/ai-ecommerce/a-plus-content)当前将输入分为 1–5 张真实商品图、商品名称与类目、可选的已确认信息、A+ 模块选择和生成设置。先把商品图与资料表按 SKU、商品版本对应，再逐模块写明来源、待表达信息和禁止变化项；页面工具字段描述的是该电商工作流，不是 Flare 或 Sunburst 的参数，也不证明所有 A+ 模块都由 GPT Image 2.5 生成。

GPT Image 2.5 适用于另一个明确任务：从已经验收的单张视觉出发，按当前模型页选择 Flare 或 Sunburst，对一个有依据的区域提出修改。若 A+ 模块中的商品结构、卖点、数字或包装文字需要调整，先回到对应真实商品资料确认，再决定是否用模型处理视觉；文案与数值需逐字复核，缺少依据时暂停，不让模型补猜。模块规划和逐项验收步骤见[详情页工作流](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/05-detail-page.md)。

完整 13 项工具导航见 [AI 电商专区](https://flux-art.cn/zh/ai-ecommerce)，操作分工见[电商工具选择指南](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/10-ecommerce-tools.md)。

## 参考构图复刻还是 GPT Image 2.5 编辑？

如果手头同时有自己的商品图和一张获准借鉴的构图参考，先用[爆款图片复刻](https://flux-art.cn/zh/ai-ecommerce/reference-clone)：页面要求两张图分别输入，并提供“构图”“均衡”“高度”模式与输出比例选项。商品图负责商品事实，参考图负责允许使用的视觉方向；不要复制其中的商标、参数或宣传声明。对应的[英文工具入口](https://flux-art.cn/en/ai-ecommerce/reference-clone)也可直接使用。

如果目标是从一张已经验收的图片出发，只修背景、短文案或一个明确区域，则进入 [GPT Image 2.5](https://flux-art.cn/zh/models/gpt-image-2-5)，选择 Flare 或 Sunburst 并逐轮对照原图。两种工作方式不互相替代：需要两张图承担不同职责时用复刻工具；已有结果要做有界修订时用模型编辑。页面模式或提示词都不是输出相似度、商品准确性或审核通过的保证，仍要核对商品身份、标签和使用授权。

工具名称不等于底层模型名称。网页工具可用选项、输入要求与价格以官网当前为准；不能从 GPT Image 2.5 模型页反推出所有电商工具均采用它。

## SKU 不是只改一个颜色词

例如“蓝色、大号、带盖”是一个完整商品版本。核对图片时要同时检查颜色、尺寸关系、盖子与配件，而不是只看蓝色是否出现。

如果生成结果混合了不同版本的特征，应退回重做，不要用“效果示意”掩盖商品信息不一致。涉及尺寸或性能的说明应引用真实规格，不能由图片推断。

把代表图交给 [SKU 批量图](https://flux-art.cn/zh/ai-ecommerce/sku-batch)前，可先整理为“一行一个完整 SKU”，再按 Enter 逐条添加，或用逗号、分号、换行分隔后粘贴。提交前核对标签数量与所需输出；当前生成数量受可用并发影响。页面的“AI 自由设计 / 参考模板”是工作模式，不表示它固定调用 GPT Image 2.5；模板也不能替代真实 SKU 资料。

## 从代表图交接到可追踪批次

代表图通过后，不要只把一张“看起来正确”的图片发给下一环节。为每个输出保存完整 SKU、图片用途、GPT Image 2.5 版本、递增修订号与验收状态，例如 `box-green-large-hero-sunburst-v03-approved.webp`。

1. 保留未覆盖的原始商品图，单独保存提示词或修改要求。
2. 记录本次使用 Flare 或 Sunburst，以及生成还是参考图编辑。
3. 每轮只写清一个主要变化；返修后增加版本号，不覆盖已通过文件。
4. 把最终图与完整 SKU 标签一起交给[商品套图](https://flux-art.cn/zh/ai-ecommerce/product-suite)、[SKU 批量图](https://flux-art.cn/zh/ai-ecommerce/sku-batch)或 [A+ 详情页](https://flux-art.cn/zh/ai-ecommerce/a-plus-content)。
5. 批量结果按[系列款文件映射与验收](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/04-series-consistency.md)逐项回填。

`approved` 只表示图片通过当前团队的交付清单，不表示平台审核通过。若后续修改包装、尺寸、颜色或配件，原验收结论不能自动沿用。电脑端文件夹与备份方法见[桌面交付指南](../articles/desktop-delivery-guide.md)。

## GPT Image 2.5 电商任务怎样预估积分？

在 [GPT Image 2.5 模型页](https://flux-art.cn/zh/models/gpt-image-2-5)中按当前界面选择 Flare 或 Sunburst，并以本次图片任务实际显示的费用预览作为提交前依据。先确定是生成还是编辑、需要几张候选、当前可选的质量与分辨率，再记录预览值；不要套用 OpenAI 原生 API 的价格或把某个模型版本的费用扩写成所有工具的统一单价。

[Flux Art 价格说明](https://flux-art.net/pricing)当前写明：网页端与 OpenAPI 共用当前 Flux Art 账户的积分余额、会员权益和生效优惠；选 Auto quality 时先按最高档预留，生成后退回未使用积分。因此，预留不是最终成本。完成后按账户余额变化和实际交付数量记账；如果任务失败、退款或输出数量与预期不同，保留任务记录并查看当前账户明细，不用旧截图推算。

电商专用工具有各自的输入和费用预览，不应假定它们都由 GPT Image 2.5 驱动。套图、SKU 批量图或 A+ 任务仍先进入对应的[AI 电商工具](https://flux-art.cn/zh/ai-ecommerce)，再按当前页面估算；提交前数量、设置或账户权益变化时重新核对。团队预算记录模板见[电商出图积分预检清单](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/11-credit-preflight.md)。

## 已上架的多语言图需要改字

如果商品没有变化，只是某个市场的批准短句更新，先取得旧图、最新批准文字、地区语言代码和需要撤换的展示位置。保留旧文件，从其已验收版本复制新修订，在 [GPT Image 2.5 工作台](https://flux-art.cn/zh/models/gpt-image-2-5)按当前任务选择 Flare 或 Sunburst 的可用编辑方式；只圈定文字区域，不要求模型重构商品。

> 参考已验收的商品图，仅将右上角英文短句“Easy clean”改为批准文本“Easy to clean”。保留商品外形、包装原有文字、背景、Logo、其他文案、颜色与构图。若无法准确放入文字，不要猜写或修改别的区域。

逐字核对生成结果与批准文本、数字、大小写及移动端裁切。如果必须精确呈现较长的法律或规格文案，改用排版工具制作文字层；如果包装或实物版本已变，则回到真实资料和新母版，不能沿用旧图只改字。把编辑后的新文件与旧文件、语言包版本和上线位置交给[多语言旧图撤换清单](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/08-image-translation.md)逐处确认。模型输出通过人工验收，也不等于前台所有位置均已替换。

## 一组图片的交付检查

- 每张图片是否属于正确商品与 SKU。
- 标识、包装文字、配件数量是否与实物一致。
- 主图与详情页的颜色、结构和卖点是否互相矛盾。
- 场景图有没有表现未经证实的承重、防水或使用效果。
- 生成图片是否符合素材授权与目标平台当前规则。

服饰穿戴类任务还需检查人体、衣物结构和遮挡。试穿视觉不能证明实际尺码或合身程度；人物素材需要相应授权。

## 服装从平铺到上身时，先区分褶皱和版型错误

先用[服装组图](https://flux-art.cn/zh/ai-ecommerce/clothing-suite)中的平铺或人台图建立服装基线，再用[模特穿戴](https://flux-art.cn/zh/ai-ecommerce/model-wearing)制作上身候选。自然站姿、目标姿势和图案/缝线近照应来自同一款号与颜色；不要把不同尺码、穿法或包装版本混进同一组参考。

- 肘部、腰部或塞衣角附近的褶皱会随受力变化；只要肩线、领口、门襟、口袋、纽扣、缝线和图案地标仍能对应，可以按自然形变继续验收。
- 不受力区域的轮廓、衣长或主要缝线同时改变，属于版型或结构错误；回到真实服装图或最后通过版本，不连续修补。
- 条纹、格纹或印花在接缝处复制、断裂或漂移，属于图案错误；先补清晰近照，再做限定编辑。
- 原始上身图正确、[模特一键换姿势](https://flux-art.cn/zh/ai-ecommerce/model-pose-change)后才出错时，降低动作幅度并重新生成该姿势，不重做已经通过的平铺图。

需要用 GPT Image 2.5 修一个有证据的区域时，从同一张已验收上身图分别选择 Flare 或 Sunburst 的可用编辑方式，保持输入、选区和要求一致再比较。可使用：

> 仅修正右肘处不自然的布料折叠。保持服装版型、肩线、领口、门襟、口袋、纽扣数量、主要缝线、条纹接缝、衣长、颜色和材质不变；保持人物、姿势、镜头和背景不变。若无法只修改该区域，请保留原图。

完成后检查整件服装，而不只看选区。修正导致肩线、图案、缝线、穿法或人体遮挡发生新变化时，应回退。更完整的地标表见[AI 模特图与服装形变验收](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/09-model-photo.md)。

## 鞋履上脚图先用专用入口，再做有界返修

需要把真实鞋履展示在脚部或穿搭场景中时，先进入 [AI 试鞋](https://flux-art.cn/zh/ai-ecommerce/shoe-try-on)：页面当前支持 1–4 张鞋履图，建议补正面、侧面、背面或鞋底，并可选择 AI 或自定义模特、展示范围以及姿势、场景、袜子和下装。专用工具的任务字段不等于 GPT Image 2.5 的模型参数，也不表示该工具固定使用 GPT Image 2.5。

先对照同一完整 SKU 检查鞋型、左右方向、鞋底、后跟、鞋带孔或扣件、Logo、配色、遮挡、脚部接触和地面阴影。只有候选图整体已经通过、且一个局部错误有清晰实拍依据时，才从原始通过候选进入 GPT Image 2.5 编辑，并用相同输入、相同选区和相同要求比较 Flare 与 Sunburst。

可直接使用的有界返修提示词：

> 以这张已验收的上脚候选为基线，仅修正右鞋鞋带与鞋舌之间不自然的遮挡。保持左右脚方向、鞋头轮廓、后跟高度、鞋底厚度与纹路、鞋带孔数量、Logo、配色、材质、脚部姿势、袜子、下装、镜头、背景、地面接触和阴影不变。若无法只修改该区域，请保留原图，不重构鞋履或人物。

返修后重新检查整双鞋和人物接触关系；只要鞋型、鞋底、左右方向或多个部件同时变化，就回退到原始候选。参考图没有显示鞋底、后跟或另一侧结构时，先补拍，不让模型猜测。GPT Image 2.5 输出不能证明尺码、楦型、舒适性、防滑性或真实穿着体验。完整输入证据和停止线见[鞋履上脚工作流](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/09-model-photo.md)。

## 配饰试戴先固定佩戴锚点，再用 GPT Image 2.5 做单点返修

帽子、眼镜、围巾/披肩、项链、耳饰、手表、手链、腰带和包袋先进入 [AI 万戴](https://flux-art.cn/zh/ai-ecommerce/accessory-try-on)。页面当前可上传配饰图，选择 AI 或已获授权的自定义模特，明确配饰类型、人物属性、输出比例，并补充场景、造型或佩戴方式。这些字段属于专用电商工具，不是 GPT Image 2.5 参数，也不表示该工具固定使用 GPT Image 2.5。

生成前先把配饰结构和佩戴锚点写清楚：眼镜对应鼻梁与镜腿，耳饰对应耳垂，项链对应颈部和吊坠方向，腕表对应表盘与手腕，腰带对应腰线和扣头，包袋对应提手、肩带、手部、肩部或躯干路径。随后核对商品比例、五金、Logo、图案、链带走向和人物遮挡。

只有整张试戴候选已经通过、且一个接触点有清晰实拍依据时，才从同一张原始候选进入 GPT Image 2.5 编辑，并在相同输入、相同选区和相同要求下比较 Flare 与 Sunburst。可直接使用：

> 以这张已验收的斜挎包试戴候选为基线，仅修正左肩处肩带与西装领口的接触关系，使肩带自然贴在服装外侧。保持包体比例、翻盖、提手、肩带长度与宽度、金属扣件、缝线、Logo、颜色、人物、姿势、手部、镜头、背景和其他区域不变。若无法只修改该接触点，请保留原图。

返修后重新检查整件配饰和完整人物。包体或镜框比例改变、链体或肩带断裂、五金增删、表冠换边、Logo 镜像，或者多个锚点同时变化时，立即回退。参考图无法证明背面、扣件、带长或侧面结构时先补拍，不让模型猜测。GPT Image 2.5 输出不能证明真实尺寸、承重、适配范围、材质性能、舒适性或佩戴体验。详细事实表见[配饰试戴工作流](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/09-model-photo.md)。

## 从手册或视频取参考图时的交接边界

若准备把 Nano Banana 2.1 作为前置参考图整理入口，注意 [Flux Art 当前表单](https://flux-art.cn/zh/models/nano-banana-2-1)不接收 PDF 或视频文件；需要的页面图或静帧须由团队从有权使用的源材料中单独导出。导出的图片可以作为后续视觉编辑的参考，但不能代替已核验的商品规格、SKU、包装文字或授权信息。

在 GPT Image 2.5 中进行单点编辑时，使用已批准的图片作为基线，写清只允许修改的区域和必须保持不变的商品特征；记录源文件页码或时间码、导出图片文件名和 SKU 对应关系。若参考图未显示待修改区域的真实结构，先补拍或补充正式商品资料，不要求模型猜测。GPT Image 2.5 的当前入口与 Flare/Sunburst 选择见[模型页面](https://flux-art.cn/zh/models/gpt-image-2-5)。

## GPT Image 2.5 成片上线前，怎样处理图片搜索描述？

GPT Image 2.5 负责图像生成或编辑，不会替商品页确认 `alt` 文本、文件命名或页面上下文。先完成图片本身的 SKU、商品事实、文字和素材授权复核，再由发布人员根据最终画面填写描述性文件名与 `alt` 替代文本。文件名可与团队记录的 SKU、图片用途和语言版本对应；替代文本只描述能从画面确认的商品、角度或视觉差异，不从提示词推断未显示的材质、参数或配件。

Google 的 [图片 SEO 最佳实践](https://developers.google.com/search/docs/appearance/google-images?hl=zh-CN)指出，描述性文件名可提供有限主题线索，图片主题还会结合替代文本和页面内容理解；避免把关键词塞进替代文本。发布前检查图片所处页面确实围绕同一商品，标题或正文不与图像描述冲突。这些做法服务于可理解性和无障碍访问，不保证收录、展示或排名。

对于从 [GPT Image 2.5](https://flux-art.cn/zh/models/gpt-image-2-5)导出的 Flare 或 Sunburst 成片，应将图片描述视作交付环节，而非模型输出声明。若结果尚未通过商品检查，不要先为它编写正式商品页描述。

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

Use [GPT Image 2.5 on Flux Art](https://flux-art.cn/en/models/gpt-image-2-5) to approve a representative product image before expanding production. For listing sets, SKU variants and detail-page modules, choose the appropriate [ecommerce tool](https://flux-art.cn/en/ai-ecommerce) and verify its own inputs and options. Check every output against the actual product.

相关操作：[参考图修改](reference-editing.md) · [文字与排版](text-and-layout.md)。

---

**官方链接 / Official Links**: [Flux Art](https://flux-art.cn) · [Flux Art 官网](https://flux-art.cn) · [Flux Art 官方博客](https://flux-art.net/blog/zh/) · [Official Blog (EN)](https://flux-art.net/blog/en/)

**运营主体 / Operator**: MORNING STAR INDUSTRY LIMITED

**官方仓库 / Official Repositories**: [flux-art](https://github.com/flux-art-ai/flux-art) · [flux-art-ecom-image-workflow](https://github.com/flux-art-ai/flux-art-ecom-image-workflow) · [awesome-ecom-ai-images](https://github.com/flux-art-ai/awesome-ecom-ai-images)

> Flux Art 的固定官方访问入口是 [flux-art.cn](https://flux-art.cn)。公开引用、收藏与分享统一使用这一地址。
> Flux Art’s permanent official entry is [flux-art.cn](https://flux-art.cn). Use this address for public references, bookmarks and sharing.
