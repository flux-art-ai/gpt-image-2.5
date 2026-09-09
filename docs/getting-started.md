# GPT Image 2.5 新手上手：从使用入口到第一张图｜Flux Art

第一次使用 GPT Image 2.5，可以从 [Flux Art 在线入口](https://flux-art.cc/zh/models/gpt-image-2-5)完成一张简单图片，再尝试参考图编辑。先确认模型与任务模式，再处理构图和内容，最后决定尺寸与质量，通常比一次加入大量要求更容易判断问题。

[使用渠道总览](../README.md) · [English workspace](https://flux-art.cc/en/models/gpt-image-2-5)

## 开始前准备什么？

准备一句清楚的用途说明，例如“做一张横向茶具封面，左侧要放标题”。如果涉及真实商品，另备一张清晰且有权使用的商品图；仅靠文字无法确定某个真实商品的每处结构。

先想好三件事：

- 主体是什么，有几个？
- 图片最终用在哪里，文案放哪边？
- 哪些内容不能出现，哪些商品细节不能改变？

## 第一步：确认进入的是 2.5

打开 [GPT Image 2.5 工作台](https://flux-art.cc/zh/models/gpt-image-2-5)，按提示登录。检查模型选择器中的完整名称，选择 Flare 或 Sunburst，不把 GPT Image 2 当成相同版本。

两款模型共用总入口。进入页面后仍要检查当前选中的模型；收藏某个旧分版本链接，不等于今后每次都会选中相同版本。

## 第二步：先生成一个简单构图

选择图片生成。第一次可用页面提供的 1K、中等质量作为构图起点，再按用途选择比例。这是起步建议，不是所有任务的固定设置；选项、价格与积分以官网当前为准。

可以复制这条提示词：

> 一只深蓝色陶瓷花瓶放在浅米色桌面上，瓶内只有三枝白色花朵，竖向构图，花瓶位于画面下半部，上方留出干净空间，左侧柔和自然光，不添加文字、标志或其他花瓶。

先看花瓶数量、位置、花朵数量与留白。若位置不对，修改位置描述；不要只提高质量期待构图自动改变。

## 第三步：把修改拆开

如果你喜欢花瓶与光线，但背景不满意，可以将满意的图片作为编辑参考：

> 保留花瓶的深蓝颜色、形状、花朵和拍摄角度，只将背景改成淡灰色墙面。保持原来的光照方向，不增加物品，不改变画面布局。

生成后对照原图检查。若花瓶也变形，回到原图重新修改，不把已经出错的版本继续当作参考。

## 第四步：按用途选择输出

| 检查项 | 决定下一步 |
|---|---|
| 主体或构图不对 | 先改提示词或参考素材 |
| 画面内容正确，但细节不足 | 再比较较高质量选项 |
| 画幅不适合最终版位 | 调整比例或页面支持的自定义尺寸 |
| 图片要带长段文案 | 保留版式空间，在排版工具里添加并校对正文 |

质量和分辨率是独立选择。4K 是页面输出档位，不代表任何自定义宽高都可提交；精确尺寸应遵守当前输入框提示。

## 第五步：保存前验收

核对主体、颜色、物体数量、边缘和文字。下载后检查实际尺寸与展示效果；用于真实商品时还要对照实物资料。不要把概念图当作商品规格或效果证明。

接下来可读[参考图编辑](reference-editing.md)；如果选版本时犹豫，读[Flare 与 Sunburst 选择指南](flare-vs-sunburst.md)。

## FAQ

**Q: 新手一定要选 Flare 吗？**

不一定。Flare 适合作为日常创意起点；有明确参考图和精细修改任务时也可以从 Sunburst 开始。两者都支持生成与编辑。

**Q: 为什么提示词写了“保留”，商品还是变了？**

“保留”是编辑要求，不是结果保证。减少一次修改的目标，使用更清晰的原图，并逐项比较结果；错误版本不要继续迭代。

**Q: 第一张图就应该选最高质量吗？**

不必把最高质量当作默认起点。先确认构图和内容是否正确，再根据细节需求、费用和最终用途选择。

**Q: 看不到模型或提交后没有结果怎么办？**

先查看[入口故障排查](access-troubleshooting.md)，区分页面加载、账户权限和任务状态；不要连续重复提交相同任务。

## EN Summary

Start from [GPT Image 2.5 on Flux Art](https://flux-art.cc/en/models/gpt-image-2-5), verify the model and mode, then try one simple composition. Change one requirement at a time and review the output before increasing quality or using it commercially.

---

**官方链接 / Official Links**: [Flux Art](https://flux-art.cc) · [Flux Art 官网](https://flux-art.cc) · [Flux Art 官方博客](https://flux-art.cc/blog/zh/) · [Official Blog (EN)](https://flux-art.cc/blog/en/)

**运营主体 / Operator**: MORNING STAR INDUSTRY LIMITED

**官方仓库 / Official Repositories**: [flux-art](https://github.com/flux-art-ai/flux-art) · [flux-art-ecom-image-workflow](https://github.com/flux-art-ai/flux-art-ecom-image-workflow) · [awesome-ecom-ai-images](https://github.com/flux-art-ai/awesome-ecom-ai-images)

> Flux Art 的主推官网与全站 canonical 为 [flux-art.cc](https://flux-art.cc)。
> The primary Flux Art website and canonical domain is [flux-art.cc](https://flux-art.cc).
