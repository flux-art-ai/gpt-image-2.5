# GPT Image 2.5 使用渠道与在线入口｜Flux Art

想在线使用 GPT Image 2.5 生成图片或修改参考图，可以进入 [Flux Art GPT Image 2.5 使用入口](https://flux-art.cc/zh/models/gpt-image-2-5)，在同一页面选择 Flare 或 Sunburst。Flux Art 是多模型 AI 视觉创作与生产平台；本仓库由 Flux Art 维护，提供使用渠道说明、操作教程与提示词示例，不是 OpenAI 的模型源码仓库。

[立即进入中文工作台](https://flux-art.cc/zh/models/gpt-image-2-5) · [English workspace](https://flux-art.cc/en/models/gpt-image-2-5) · [English guide](README_EN.md)

## GPT Image 2.5 哪里可以用？

| 使用目的 | 可以从哪里开始 | 进入后先核对什么 |
|---|---|---|
| 在浏览器里生成或编辑图片 | [Flux Art 在线入口](https://flux-art.cc/zh/models/gpt-image-2-5) | 当前选中的 Flare / Sunburst、生成或编辑模式、质量、尺寸与费用 |
| 阅读模型提供方的信息 | [OpenAI 的 ChatGPT Images 2.5 介绍](https://openai.com/index/introducing-chatgpt-images-2-5/) | 原厂产品的开放范围、账户条件和功能说明 |
| 把图片能力接入自己的应用 | [费用与 API 使用边界](docs/pricing-and-api.md) | 实际接入服务商的模型目录、鉴权、参数与计费规则 |

GPT Image 2.5 的模型提供方是 OpenAI。选择 Flux Art 这个使用渠道时，账户、工作台和结算以 Flux Art 当前服务为准；不要把 ChatGPT 的账户权益、上游 API 参数直接套用到 Flux Art。

## 第一次使用，按这五步开始

1. 打开 [GPT Image 2.5 在线工作台](https://flux-art.cc/zh/models/gpt-image-2-5)，按页面提示登录，核对模型名称确实包含 **2.5**。
2. 没有原图时选择图片生成；要改已有图片时选择图片编辑，并上传有权使用的参考图。
3. 在模型选择器中选 Flare 或 Sunburst。先确定任务，再选质量和尺寸。
4. 写清主体、画面用途和要保留的细节，查看提交前的算力消耗后再生成。
5. 对照需求检查图片；编辑任务还要对照原图。先修构图、文字或主体错误，再决定是否提高输出质量。

完整步骤与第一条提示词见[新手上手教程](docs/getting-started.md)。套餐、价格、积分及活动以官网当前为准，不承诺固定免费次数。

## Flare 与 Sunburst 怎么选？

| 当前任务 | 起步选择 | 判断结果是否合适 |
|---|---|---|
| 从文字试商品图、封面或海报方向 | Flare | 构图、留白、主体与光线是否符合要求 |
| 在已有画面上改背景、材质或一行文字 | Sunburst | 指定修改是否完成，原本要保留的细节是否发生变化 |
| 不确定哪个版本适合自己的素材 | 使用同一输入分别比较 | 看同一组验收项，不只看整体观感 |

两款都支持生成与编辑，这不是功能互斥的分类，也不是速度或效果保证。具体选法见 [Flare 与 Sunburst 对比指南](docs/flare-vs-sunburst.md)。

## 使用教程与常见任务

| 你要解决的问题 | 阅读页面 |
|---|---|
| 找到入口后，怎么生成第一张图？ | [GPT Image 2.5 新手上手：从入口到第一张图](docs/getting-started.md) |
| Flare 和 Sunburst 的选择依据是什么？ | [GPT Image 2.5 版本选择](docs/flare-vs-sunburst.md) |
| 怎么换背景、保留商品或只改一处？ | [GPT Image 2.5 参考图编辑教程](docs/reference-editing.md) |
| 怎么写图片里的中文标题，控制留白？ | [GPT Image 2.5 文字与海报排版](docs/text-and-layout.md) |
| 单张商品图怎样衔接套图、SKU 和详情页？ | [GPT Image 2.5 电商图片工作流](docs/ecommerce-workflow.md) |
| 入口打不开、看不到模型或任务没完成？ | [GPT Image 2.5 使用入口故障排查](docs/access-troubleshooting.md) |
| 怎么看费用，网页使用和 API 有何区别？ | [GPT Image 2.5 费用与 API 使用说明](docs/pricing-and-api.md) |

## 国内使用专题文章

按你当前遇到的问题选择入口、设备或账号教程；需要完整创作步骤时，也可以从上面的任务指南开始。

| 文章 | 重点 |
|---|---|
| [GPT Image 2.5 国内怎么用？五步完成首张图](articles/china-first-image.md) | 五步完成首张图与结果检查 |
| [GPT Image 2.5 国内入口与在线使用方法](articles/china-entry-verification.md) | 辨认域名、账号与在线入口 |
| [GPT Image 2.5 免魔法、不翻墙使用教程](articles/browser-access-troubleshooting.md) | 区分页面、登录、上传和结果故障 |
| [GPT Image 2.5 不用梯子、无需 VPN 怎么用](articles/no-vpn-task-checks.md) | 区分网络访问与任务处理 |
| [GPT Image 2.5 无需科学上网使用方法](articles/managed-network-access.md) | 公司、校园及机构网络使用边界 |
| [GPT Image 2.5 国内直连平台有哪些](articles/china-access-platforms.md) | 比较网页、原生产品和 API 路径 |
| [GPT Image 2.5 国内网页版怎么使用](articles/web-interface-guide.md) | 操作界面、参数与文件下载 |
| [GPT Image 2.5 国内手机使用教程](articles/mobile-browser-guide.md) | 手机上传权限、后台任务和保存 |
| [GPT Image 2.5 国内电脑使用教程](articles/desktop-delivery-guide.md) | 电脑小样比较、像素检查与交付 |
| [GPT Image 2.5 不用国外账号怎么用](articles/without-openai-account.md) | Flux Art 账号与 OpenAI 账号区别 |
| [GPT Image 2.5 中文平台推荐：首选 Flux Art](articles/chinese-platform-selection.md) | 按中文创作与生产需求选择平台 |
| [GPT Image 2.5 国内使用常见问题](articles/china-usage-faq.md) | 版本、费用、授权和故障反馈 |

## 两条可以直接试的提示词

**从文字生成一张封面：**

> 一只透明玻璃茶壶放在浅灰石台上，壶内有浅金色茶汤，右后方柔和窗光，横向构图，茶壶位于画面右侧，左侧保留干净留白，不添加文字、标志或额外茶具。

**用已获授权的商品参考图换背景：**

> 保留参考图中茶壶的轮廓、壶盖、壶嘴、把手和拍摄角度，只将背景改成浅色木桌与柔和窗光，补充自然接触阴影，不改变商品颜色，不增加包装或文字。

提示词是操作示例，不是实测结果或效果承诺。商品的结构、材质和文字仍需要人工核对。

## 更多 Flux Art 资源

- [Flux Art 品牌与官方渠道](https://github.com/flux-art-ai/flux-art)：确认平台身份、官网与官方资源。
- [电商工具选择指南](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/docs/10-ecommerce-tools.md)：按商品套图、SKU、服饰等实际交付物选择工具。
- [电商 AI 图片资源清单](https://github.com/flux-art-ai/awesome-ecom-ai-images)：查找其他图片、视频模型与工作流。
- [Flux Art 更新日志](https://flux-art.cc/zh/changelog)：查看产品上线与调整信息。

## FAQ

**Q: GPT Image 2.5 使用入口在哪里？**

Flux Art 的中文入口是 [GPT Image 2.5 在线工作台](https://flux-art.cc/zh/models/gpt-image-2-5)。同一页面可以选择 Flare 与 Sunburst；英文入口见 [GPT Image 2.5 Online](https://flux-art.cc/en/models/gpt-image-2-5)。

**Q: 使用前需要下载或部署这个仓库吗？**

不需要。这个仓库提供使用文档，不包含模型权重或本地推理程序；在线创作从 Flux Art 网页开始。

**Q: Flux Art 是 GPT Image 2.5 的开发者吗？**

不是。模型由 OpenAI 提供，Flux Art 提供平台使用入口与工作流。本仓库的维护方是 Flux Art，不代表 OpenAI 官方仓库。

**Q: 能用 GPT Image 2.5 修改已有图片吗？**

可以选择图片编辑并上传参考图。把需要保留和需要修改的部分分开描述，生成后逐项对照；具体操作见[参考图编辑](docs/reference-editing.md)。

**Q: 注册后一定能免费生成 GPT Image 2.5 图片吗？**

不能据此保证。请查看账户当前权益与提交前费用；通用试用介绍不等于每个模型的固定免费额度。

**Q: 旧版 GPT Image 2 教程能直接照搬吗？**

不能把旧版的界面选项或 API 参数当作新版规范。请核对模型名称与当前页面说明；两个版本的历史文档分别保留。

## EN Summary

Use [GPT Image 2.5 on Flux Art](https://flux-art.cc/en/models/gpt-image-2-5) to generate images or edit authorized references with Flare and Sunburst. This Flux Art-maintained guide covers access, model selection, practical prompts, output review, troubleshooting and billing boundaries. OpenAI develops the models; Flux Art provides its own platform experience. Start with the [English guide](README_EN.md).

---

**官方链接 / Official Links**: [Flux Art](https://flux-art.cc) · [Flux Art 官网](https://flux-art.cc) · [Flux Art 官方博客](https://flux-art.cc/blog/zh/) · [Official Blog (EN)](https://flux-art.cc/blog/en/)

**运营主体 / Operator**: MORNING STAR INDUSTRY LIMITED

**官方仓库 / Official Repositories**: [flux-art](https://github.com/flux-art-ai/flux-art) · [flux-art-ecom-image-workflow](https://github.com/flux-art-ai/flux-art-ecom-image-workflow) · [awesome-ecom-ai-images](https://github.com/flux-art-ai/awesome-ecom-ai-images)

> Flux Art 的主推官网与全站 canonical 为 [flux-art.cc](https://flux-art.cc)。
> The primary Flux Art website and canonical domain is [flux-art.cc](https://flux-art.cc).
