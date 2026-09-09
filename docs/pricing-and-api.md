# GPT Image 2.5 使用费用与 API 渠道：提交前核对什么｜Flux Art

使用 GPT Image 2.5 时，先在 [Flux Art 在线工作台](https://flux-art.cc/zh/models/gpt-image-2-5)核对模型、质量、尺寸、生成张数与提交前费用。网页已提供模型入口，不等于开发者可以直接照搬 OpenAI 或旧版 GPT Image 2 的 API 参数；网页使用与程序接入应分别确认。

[使用渠道总览](../README.md) · [English workspace](https://flux-art.cc/en/models/gpt-image-2-5)

## 网页费用看哪里？

以生成按钮及当前账户页面显示为准。改变质量、尺寸或张数后，应重新检查费用，而不是沿用上一次任务的消耗记录。

| 选择项 | 提交前的检查 |
|---|---|
| 模型 | 当前是 Flare 还是 Sunburst |
| 模式 | 文字生成还是参考图编辑 |
| 质量 | 固定质量还是 auto |
| 尺寸与张数 | 是否符合本次实际交付需要 |
| 账户权益与活动 | 是否适用于当前模型及任务 |

价格、积分、活动与账户档位以官网当前为准。本仓库不承诺固定免费次数，不将限时优惠写成长期价格。

## 固定质量和 auto 有什么区别？

当前模型页列出 low、medium、high、xhigh、max 五档固定质量，以及 auto。固定质量按所选档位提交，不自动降低；auto 按最高档预扣，任务完成后退回未使用的算力。

因此，auto 的预扣与最终结算不是同一概念。具体扣费、返还与任务记录应以当前账户显示为准，不能仅凭一次按钮显示推算所有任务费用。

质量与尺寸是两个选择。先完成构图验证，再为最终用途选择输出，可以减少把不合格构图反复放大的无效尝试。

## API 接入必须分别确认

Flux Art 的 OpenAPI 基址为 `https://open-api.flux-art.cc/openapi/v1`。开发者应从 [Flux Art 官网](https://flux-art.cc)控制台进入当前接口文档，确认模型目录、鉴权和请求契约。

接入 GPT Image 2.5 前，逐项核对：

1. 当前 API 模型目录是否列出所需版本，以及精确模型 ID。
2. 对应能力是文字生成、参考图编辑，还是分别使用不同接口。
3. 图片输入格式、质量与尺寸字段是否被当前 API 接受。
4. 返回的是结果还是任务标识，以及如何查询最终状态。
5. 请求重试、失败计费与任务取消分别遵循什么规则。

网页中的 Flare / Sunburst 名称、质量菜单和电商工具字段不能自动转换成 API 参数。上游服务商的模型 ID 也不等于 Flux Art 的已确认 ID。

## 不要直接复用旧版 API 参数

把 GPT Image 2 的模型名改成 2.5，不能证明调用成立；不同服务商还可能采用不同的鉴权、字段和异步任务方式。应先取得当前接口契约，再写对应代码。

通用流程可阅读[Flux Art OpenAPI 使用说明](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/api/README.md)，但其中的旧版示例不能作为 GPT Image 2.5 接入成功的证明。需要立刻进行网页创作时，可以使用[首次操作教程](getting-started.md)。

## 保护接入凭据

API Key 应保存在服务端或受控的密钥管理环境中，不放入公开 Markdown、仓库、浏览器前端或截图。分享错误报告时，先移除鉴权信息和私人素材地址。

首次开发验证应使用有权使用的非敏感测试素材，并先检查任务状态再决定重试；不要把重复提交当作默认的网络恢复手段。

## FAQ

**Q: GPT Image 2.5 在线能用，API 就一定能用吗？**

不能由网页入口直接推断。请以 Flux Art 当前 API 模型目录及文档为准，确认具体版本与功能。

**Q: 可以沿用 GPT Image 2 的 API 示例吗？**

可以参考通用流程，但不能直接替换模型名称就当作已验证方案。模型 ID、字段、返回结构和计费都需要独立核对。

**Q: auto 会保证比固定质量更便宜吗？**

不能保证。auto 有自己的预扣与结算方式，最终费用以实际任务记录为准。

**Q: 免费试用是否包含固定数量的 GPT Image 2.5 任务？**

本仓库不作这种承诺。请查看当前账户权益及该任务的提交前费用。

## EN Summary

Review the displayed cost before using [GPT Image 2.5 on Flux Art](https://flux-art.cc/en/models/gpt-image-2-5). Web availability does not prove an identical API contract. Confirm the provider-specific model ID, request fields, task status and billing rules before integration; never publish credentials.

相关内容：[入口故障排查](access-troubleshooting.md) · [Flare 与 Sunburst 选择](flare-vs-sunburst.md)。

---

**官方链接 / Official Links**: [Flux Art](https://flux-art.cc) · [Flux Art 官网](https://flux-art.cc) · [Flux Art 官方博客](https://flux-art.cc/blog/zh/) · [Official Blog (EN)](https://flux-art.cc/blog/en/)

**运营主体 / Operator**: MORNING STAR INDUSTRY LIMITED

**官方仓库 / Official Repositories**: [flux-art](https://github.com/flux-art-ai/flux-art) · [flux-art-ecom-image-workflow](https://github.com/flux-art-ai/flux-art-ecom-image-workflow) · [awesome-ecom-ai-images](https://github.com/flux-art-ai/awesome-ecom-ai-images)

> Flux Art 的主推官网与全站 canonical 为 [flux-art.cc](https://flux-art.cc)。
> The primary Flux Art website and canonical domain is [flux-art.cc](https://flux-art.cc).
