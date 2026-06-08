---
title: 根据性能数据优化内容
description: 将CJA和AEM MCP服务器一起使用，找出性能不佳的内容并进行更新，而无需在工具之间切换。
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 3%

---


# 根据性能数据优化内容

<!-- last-modified: 2026-05-21 -->

![根据性能数据优化内容](https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data)

通常情况下，关闭内容性能数据和内容更新之间的循环意味着在Analytics和CMS之间切换。 此演练展示了如何在同一AI会话中连接Customer Journey Analytics和AEM，以便您可以在不离开对话的情况下显示性能不佳的页面并更新它们。

| | |
| --- | --- |
| CX企业级应用程序 | Customer Journey Analytics、Adobe Experience Manager as a Cloud Service |
| 代理工具 | CX Enterprise MCP Gateway 、 AEM Content MCP Server |
| 受众 | 营销活动经理、内容策划师、营销运营 |
| 先决条件 | 与MCP兼容的AI客户端、CJA访问、AEM as a Cloud Service访问 |

每个步骤显示一个代表性提示和一个AI响应示例。 您还可完成&#x200B;**更多**&#x200B;部分，以供在同一会话中进行其他探索。

## 开始之前

>[!BEGINTABS]

>[!TAB 克劳德.ai]

将两个MCP服务器连接为自定义连接器。 分别添加各一个。

1. 转到Claude.ai中的&#x200B;**设置>集成**。
2. 选择&#x200B;**添加自定义连接器**，输入服务器URL，然后选择&#x200B;**连接**。
3. 使用Adobe ID登录，然后为第二台服务器重复此操作。

| Server | 终结点 |
| --- | --- |
| CX Enterprise MCP网关 | `https://cx-enterprise.adobe.io/mcp` |
| AEM Content MCP Server | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

完整设置： [Claude.ai自定义连接器文档](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

使用ChatGPT Developer Mode（Pro、Plus、Business、Enterprise或Education计划）连接两个MCP服务器。 分别添加每台服务器。

1. 在&#x200B;**ChatGPT设置**&#x200B;中启用&#x200B;**开发人员模式**。
2. 转到&#x200B;**设置>集成**，然后选择&#x200B;**添加自定义连接器>远程MCP服务器**。
3. 输入服务器URL，选择&#x200B;**连接**，然后使用您的Adobe ID登录。
4. 对第二个服务器重复此操作。

| Server | 终结点 |
| --- | --- |
| CX Enterprise MCP网关 | `https://cx-enterprise.adobe.io/mcp` |
| AEM Content MCP Server | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

完整设置： [ChatGPT MCP文档](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB 其他AI客户端]

使用Gemini、Microsoft Copilot、Cursor、Claude Code或其他与MCP兼容的环境？ 使用以下端点连接到两个MCP服务器：

| Server | 终结点 |
| --- | --- |
| CX Enterprise MCP网关 | `https://cx-enterprise.adobe.io/mcp` |
| AEM Content MCP Server | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

所有受支持客户端的完整设置说明： [连接到您的AI客户端](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>出现提示时，请使用您的Adobe ID登录，然后选择链接到您的CJA和AEM环境的IMS组织。 选择错误的组织是身份验证错误最常见的来源。
>
>在首次连接时，您的AI客户端可能会要求您选择IMS组织或指定沙盒。 设置该上下文后，MCP服务器会将其用于会话的其余部分。
>
>某些工具在执行之前会提示您审批。 查看请求并批准或拒绝 — 未经您的确认不会采取任何操作。

## 步骤1：识别性能不佳的内容

使用CX Enterprise MCP Gateway在Customer Journey Analytics中按参与和转化指标对页面进行排名。 目标是列出需要关注的内容的清晰、优先列表。

```
Show me the 10 pages with the lowest engagement rate over the last 60 days.
```

+++查看示例响应

最低参与页面（2026年3月22日至5月21日）：

| 排名 | 页面 | 参与率 | 跳出率 | 平均 页面逗留时间 |
| --- | --- | --- | --- | --- |
| 1 | /en/products/analytics | 8.2% | 74% | 0:42 |
| 2 | /en/resources/whitepapers | 9.1% | 71% | 0:38 |
| 3 | /en/solutions/retail | 10.4% | 69% | 0:51 |
| 4 | /en/blog/2025-q4-recap | 11.0% | 68% | 0:44 |
| 5-10 | ... | 12.3-14.1% | 63-67% | 0:35-1:10 |

您的网站平均参与率为34.7%。 这些页面比平均水平低2-4倍。

+++

## 步骤2：在AEM中查看内容

在不离开AI会话的情况下，从AEM中提取这些页面的当前状态。 了解内容的含义是了解要更改哪些内容的第一步。

```
Show me the current content on the /en/products/analytics page in AEM.
```

+++查看示例响应

**页：** `/en/products/analytics`
**上次修改日期：** MacMillan于2026年4月30日修改
**状态：**&#x200B;已发布

**主页部分：**
Headline： “为每一个团队制定以数据为导向的决策”
Subheadline： “Adobe Analytics为您的组织提供了采取行动的洞察力。”
CTA： /contact/demo→的“请求演示”

**正文：** 3个功能块，后跟一个客户徽标条和一个辅助CTA。 无视频或交互式元素。 21天未更新页面。

**Meta描述：** &quot;Adobe Analytics：企业团队的实时报表和AI见解。&quot;

+++

## 步骤3：进行定向更新

在考虑性能数据和当前内容的情况下，根据数据揭示的内容进行更新。

```
Update the hero headline on the analytics product page to Make faster decisions with AI-powered analytics.
```

+++查看示例响应

**提议的更改：**

| 字段 | 当前值 | 新值 |
| --- | --- | --- |
| 英雄标题 | 针对每个团队的数据驱动型决策 | 利用AI支持的分析更快地做出决策 |

页面： `/en/products/analytics`

确认此更改？ 回复“是”会将更新写入AEM。 在您明确重新发布之前，页面将保持当前发布状态。

+++

>[!CAUTION]
>
>在出现提示时确认每个内容更改。 在批准对实时页面的更新之前，请查看完整的差异部分。

## 步骤4：验证并发布

如果对更新满意，则通过确认所有更改并提升内容来关闭循环。

```
Show me a summary of all changes made in this session.
```

+++查看示例响应

**会话摘要 — 2026年5月21日：**

| 页面 | 更改 | 状态 |
| --- | --- | --- |
| /en/products/analytics | 主页标题已更新 | 已保存，已取消发布 |

已更新1页。 确认后可发布。

您的低参与度列表中剩余&#x200B;**个：** 9页在此会话中未更新。 是否要继续下一页，或创建启动项以在发布前进行批量审阅？

+++

## 您完成了哪些工作

您在单个AI会话中连接Customer Journey Analytics和AEM，并使用性能数据直接通知内容更改。 通过在不切换工具的情况下从量度移动到更新，您可以缩短Analytics insight与已发布内容之间的反馈循环。 这在营销活动规模上最为重要，因为许多页面可能需要引起注意，并且手动跨工具工作流会导致延迟。

## 您可以完成更多任务

CJA和AEM MCP服务器共同支持从识别问题到运输修复的整个周期。 展开下面的方案以查看可在同一会话中尝试的提示。

+++查找阻碍性能的内容

参与度低的高流量表示内容问题，而不是流量问题。 这些提示可帮助您在活动截止日期强制实施问题之前显示需要注意的特定页面和模式。

**提示**

```
Show me the 10 pages with the lowest conversion rate this quarter.
```

```
Which pages have a high bounce rate but also high traffic?
```

```
Compare engagement rates for blog posts versus product pages.
```

```
Find AEM pages that haven't been updated in over 60 days.
```

+++

+++修复数据告诉您修复的内容

一旦您知道哪些方面表现不佳，下一步就是进行有针对性的更改。 这些提示允许您根据性能数据显示的信息更新标题、CTA和元描述。

**提示**

```
Update the CTA on the /en/solutions/retail page to 'See how it works'.
```

```
Add a note to the hero subheadline on the analytics page: Now with AI-powered anomaly detection.
```

```
Update the meta description on all pages in /en/products/ that contain the word 'legacy'.
```

```
Which pages updated in this session still need their CTAs reviewed?
```

+++

+++下一营销活动之前的发货改进

在会话期间所做的更改可能会快速栈积。 这些提示可帮助您查看就绪的内容，将更新分组到可查看的启动项中，并在活动开始之前进行简洁的提升。

**提示**

```
Show me all pages updated in this session that are still unpublished.
```

```
Create a launch with all changes from this session for review before publishing.
```

```
Give me a summary of all changes made in this session.
```

```
Promote everything in the current launch to production.
```

+++

## 更多信息

| 资源 | 您将找到什么 |
| --- | --- |
| [Analytics MCP文档](https://developer.adobe.com/analytics-mcp/docs/) | CJA MCP设置和工具参考 |
| [AEM as a Cloud Service 文档](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service) | 完整的AEM文档 |
| AI注册表中的[CJA MCP服务器](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | CJA MCP服务器工具和可用性 |
| AI注册表中的[AEM Content MCP Server](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) | AEM Content MCP Server工具和可用性 |
| [MCP服务器](../tools/mcp-servers.md) | 将AI客户端连接到Adobe MCP服务器 |
