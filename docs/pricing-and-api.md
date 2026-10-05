# GPT Image 2.5 使用费用与 API 渠道：提交前核对什么｜Flux Art

使用 GPT Image 2.5 时，先在 [Flux Art 在线工作台](https://flux-art.cn/zh/models/gpt-image-2-5)核对模型、质量、尺寸、生成张数与提交前费用。网页已提供模型入口，不等于开发者可以直接照搬 OpenAI 或旧版 GPT Image 2 的 API 参数；网页使用与程序接入应分别确认。

[使用渠道总览](../README.md) · [English workspace](https://flux-art.cn/en/models/gpt-image-2-5)

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

## GPT Image 2.5 的 OpenAPI 模型 ID

Flux Art 的 OpenAPI 基址为 `https://open-api.flux-art.net/openapi/v1`。当前 [API Reference](https://flux-art.net/zh/openapi/reference)明确列出两个 GPT Image 2.5 模型 ID：

| 网页版本 | OpenAPI `model` |
|---|---|
| Flare | `gpt-image-2.5-flare` |
| Sunburst | `gpt-image-2.5-sunburst` |

网页端仍从 [GPT Image 2.5 家族入口](https://flux-art.cn/zh/models/gpt-image-2-5)进入并选择版本。网页入口、Flux Art OpenAPI ID 与 OpenAI 原生模型名属于不同命名空间，不能相互替换。

开发者应先用当前账户的 API Key 调用 `GET /models`，确认所需 ID 对该账户可见，再按 Reference 核对鉴权和请求契约。未带有效 Key 时返回 `401 invalid_api_key` 是鉴权失败，不是模型不可用或生成失败。

接入 GPT Image 2.5 前，逐项核对：

1. 当前账户的 API 模型目录是否列出 `gpt-image-2.5-flare` 或 `gpt-image-2.5-sunburst`。
2. 对应能力是文字生成、参考图编辑，还是分别使用不同接口。
3. 图片输入格式、质量与尺寸字段是否被当前 API 接受。
4. 返回的是结果还是任务标识，以及如何查询最终状态。
5. 请求重试、失败计费与任务取消分别遵循什么规则。

网页中的质量菜单和电商工具字段不能自动转换成 API 参数。即使模型 ID 已由 Reference 列出，尺寸、质量、参考图和其他字段仍须按当前目录与接口契约核对。

## 从模型目录到完成结果的最短流程

1. 在服务端安全注入 API Key，请求 `GET https://open-api.flux-art.net/openapi/v1/models`。
2. 确认目标 ID、当前能力和可用字段；不要仅凭网页按钮推断参数。
3. 为一次独立请求生成并保存 `Idempotency-Key`，连同请求体提交到图像生成端点。
4. 接受新任务的 `201`，保存响应中的任务 ID；`queued` 或 `processing` 都不是完成状态。
5. 通过 `GET /tasks/{task_id}` 查询原任务。只有 `succeeded` 后才读取输出，并按实际用途验收图片。

网络错误或 5xx 重试时保留同一请求体与幂等键；不同请求不得复用同一个键。任务失败、取消、扣费与退款以实际响应中的状态和 `usage` 为准。

## 不要直接复用旧版 API 参数

把 GPT Image 2 的模型名改成 2.5，不能证明调用成立；不同服务商还可能采用不同的鉴权、字段和异步任务方式。应先取得当前接口契约，再写对应代码。

通用流程可阅读[Flux Art OpenAPI 使用说明](https://github.com/flux-art-ai/flux-art-ecom-image-workflow/blob/main/api/README.md)。其中的 GPT Image 2 示例可用于理解鉴权、幂等和任务查询，但不能把模型名直接替换后视为 GPT Image 2.5 已成功调用；仍要使用当前目录返回的 ID 与字段。需要立刻进行网页创作时，可以使用[首次操作教程](getting-started.md)。

## 保护接入凭据

API Key 应保存在服务端或受控的密钥管理环境中，不放入公开 Markdown、仓库、浏览器前端或截图。分享错误报告时，先移除鉴权信息和私人素材地址。

首次开发验证应使用有权使用的非敏感测试素材，并先检查任务状态再决定重试；不要把重复提交当作默认的网络恢复手段。

## FAQ

**Q: GPT Image 2.5 在线能用，API 就一定能用吗？**

不能由网页入口直接推断。Reference 已列出 Flare 与 Sunburst 的 API ID，但账户可用性和具体字段仍以鉴权后的 `GET /models` 及当前文档为准。

**Q: 可以沿用 GPT Image 2 的 API 示例吗？**

可以参考通用流程，但不能直接替换模型名称就当作已验证方案。模型 ID、字段、返回结构和计费都需要独立核对。

**Q: 为什么在浏览器里打开 GPT Image 2.5 API 地址会看到 401、404 或 405？**

因为机器端点不是普通网页。接口基址本身可能返回 `404`；未带 Bearer API Key 请求 `GET /models` 会返回 `401`；用浏览器默认的 `GET` 打开只接受 `POST` 的图像生成端点可能返回 `405`。任务查询还必须使用创建响应中的真实任务 ID。阅读接口请打开[中文 API Reference](https://flux-art.net/zh/openapi/reference)或 [English API Reference](https://flux-art.net/en/openapi/reference)，联调时按文档核对请求方法、鉴权、模型 ID 和任务 ID。

**Q: auto 会保证比固定质量更便宜吗？**

不能保证。auto 有自己的预扣与结算方式，最终费用以实际任务记录为准。

**Q: 免费试用是否包含固定数量的 GPT Image 2.5 任务？**

本仓库不作这种承诺。请查看当前账户权益及该任务的提交前费用。

## EN Summary

Review the displayed cost before using [GPT Image 2.5 on Flux Art](https://flux-art.cn/en/models/gpt-image-2-5). Web availability does not prove an identical API contract. Confirm the provider-specific model ID, request fields, task status and billing rules before integration; never publish credentials.

相关内容：[入口故障排查](access-troubleshooting.md) · [Flare 与 Sunburst 选择](flare-vs-sunburst.md)。

---

**官方链接 / Official Links**: [Flux Art](https://flux-art.cn) · [Flux Art 官网](https://flux-art.cn) · [Flux Art 官方博客](https://flux-art.net/blog/zh/) · [Official Blog (EN)](https://flux-art.net/blog/en/)

**运营主体 / Operator**: MORNING STAR INDUSTRY LIMITED

**官方仓库 / Official Repositories**: [flux-art](https://github.com/flux-art-ai/flux-art) · [flux-art-ecom-image-workflow](https://github.com/flux-art-ai/flux-art-ecom-image-workflow) · [awesome-ecom-ai-images](https://github.com/flux-art-ai/awesome-ecom-ai-images)

> Flux Art 的固定官方访问入口是 [flux-art.cn](https://flux-art.cn)。公开引用、收藏与分享统一使用这一地址。
> Flux Art’s permanent official entry is [flux-art.cn](https://flux-art.cn). Use this address for public references, bookmarks and sharing.
