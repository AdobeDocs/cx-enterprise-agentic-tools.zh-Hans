---
title: 保持内容最新，更快地发送更新
description: 使用AEM Content MCP Server查找、查看、更新和发布AEM内容，而无需在工具之间切换。
last-substantial-update: 2026-06-10T00:00:00Z
source-git-commit: 40d93f878ba9f48c9daffd3beccb4bf829113a36
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 3%

---


# 保持内容最新，更快地发送更新

<!-- last-modified: 2026-05-22 -->

![AI客户端确认页面已发布并返回实时URL](../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png)

让网站内容保持最新状态是一项持续不断的操作压力。 本演练展示了内容团队如何使用AEM Content MCP Server通过AI客户端查找、查看、更新和发布AEM页面和内容片段，以缩短内容决策和实时更新之间的时间。

| 方案详细信息 | |
| --- | --- |
| CX企业级应用程序 | [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/overview/introduction) |
| 代理工具 | [AEM Content MCP Server](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) |
| 受众 | 内容经理、营销团队 |
| 先决条件 | 与MCP兼容的AI客户端、AEM as a Cloud Service访问 |

每个步骤显示一个代表性提示和一个AI响应示例。 您还可完成&#x200B;**更多**&#x200B;部分，以供在同一会话中进行其他探索。

## 开始之前

>[!BEGINTABS]

>[!TAB 克劳德.ai]

将AEM Content MCP Server作为自定义连接器连接。

1. 转到Claude.ai中的&#x200B;**设置>集成**。
2. 选择&#x200B;**添加自定义连接器**&#x200B;并输入服务器URL： `https://mcp.adobeaemcloud.com/adobe/mcp/content`
3. 选择&#x200B;**连接**&#x200B;并使用您的Adobe ID登录。

完整设置： [Claude.ai自定义连接器文档](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

使用ChatGPT开发人员模式（需要Pro、Plus、Business、Enterprise或Education计划）连接AEM Content MCP Server。

1. 在&#x200B;**ChatGPT设置**&#x200B;中启用&#x200B;**开发人员模式**。
2. 转到&#x200B;**设置>集成**，然后选择&#x200B;**添加自定义连接器>远程MCP服务器**。
3. 输入服务器URL： `https://mcp.adobeaemcloud.com/adobe/mcp/content`
4. 选择&#x200B;**连接**&#x200B;并使用您的Adobe ID登录。

完整设置： [ChatGPT MCP文档](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB 其他AI客户端]

使用Gemini、Microsoft Copilot、Cursor、Claude Code或其他与MCP兼容的环境？ 使用以下端点连接到AEM Content MCP Server：

```
https://mcp.adobeaemcloud.com/adobe/mcp/content
```

所有受支持客户端的完整设置说明： [连接到您的AI客户端](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>出现提示时，请使用您的Adobe ID登录，然后选择链接到您的AEM as a Cloud Service环境的IMS组织。 权限是在AEM级别强制实施的。 您的AI客户端只能执行您的帐户授权的操作。
>
>如果只需要浏览或审核内容而无需进行更改，请改用只读服务器端点： `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly`。 此页上的所有发现和查看提示都适用于两个服务器。
>
>首次连接时，AI客户端可能会要求您确认组织或AEM环境。 设置该上下文后，MCP服务器会将其用于会话的其余部分。
>
>某些工具在执行之前会提示您审批。 审查提议的行动，并批准或拒绝。 未经您的确认，不会进行任何更改。

## 步骤1：在AEM环境中查找内容

首先，请您的AI客户端发现AEM环境和搜索内容。 您可以按主题、关键词或内容类型搜索，而无需知道确切路径。

```
From WKND Dev environment, find all ski related content.
```

+++查看示例响应

![AI客户端显示来自WKND开发AEM环境的滑雪内容搜索结果](../assets/use-cases/manage-aem-content/manage-aem-content-step1-find-ski.png)

+++


## 第2步：查看特定页面

找到相关内容后，请让您的AI客户端向您显示特定页面。 您可以按名称或路径引用页面。 MCP服务器解析引用并返回内容结构。

```
Show me the US English Home Page.
```

+++查看示例响应

![AI客户端显示AEM中的美国英语主页内容结构](../assets/use-cases/manage-aem-content/manage-aem-content-step2-home-page.png)

+++


## 步骤3：改进内容

查看页面内容后，请让您的AI客户端提出改进或应用改进。 AI可以根据页面当前所显示的内容提出副本更改，并在编写任何内容之前请求确认。

```
Improve the Hero CTAs.
```

+++查看示例响应

![AI客户端在应用更改之前提出带有确认提示的改进Hero CTA副本](../assets/use-cases/manage-aem-content/manage-aem-content-step3.gif)

+++


>[!CAUTION]
>
>出现提示时确认每个更改。 AEM Content MCP Server可以创建、更新和删除内容。 在批准之前（尤其是在实时页面上）审核建议的更改。

## 步骤4：发布和共享

确认更新后，发布页面并检索可共享URL，所有这些操作都在同一对话中。

```
Publish the changes and share the URL.
```

+++查看示例响应

![AI客户端确认页面已发布并返回实时URL](../assets/use-cases/manage-aem-content/manage-aem-content-step4.gif)

+++


## 您完成了哪些工作

您使用AEM Content MCP Server查找内容、查看实时页面、应用AI建议的改进以及发布结果，而无需打开AEM界面。 通过在单个AI会话中组合进行内容发现、编辑和发布，内容团队可以从识别间隙转移到以更快的速度和更少的上下文切换发送更新。 同一工作流可以扩展到多个页面、内容片段和协调的活动启动项。

## 您可以完成更多任务

AEM Content MCP Server处理的内容远远超过演练所涵盖的范围。 展开下面的方案以查看可在同一会话中尝试的提示。

+++抢先进行网站审核或重新启动

手动执行内容审核非常耗时。 这些提示可帮助您快速显示陈旧内容、从未发货的草稿以及需要在大推之前修复的间隙。

**提示**

```
Show me everything updated in the last two weeks.
```

```
What content is sitting in draft and hasn't been published yet?
```

```
Find pages that haven't been touched in over a year.
```

```
Which pages are missing their description field?
```

```
We're reorganizing the taxonomy. Find all articles missing tags or categories.
```

+++

+++大规模修复SEO和可访问性问题

SEO和可访问性差距会在大型站点中快速复合。 这些提示可帮助您找到在审核或启动之前最重要的问题并确定其优先级。

**提示**

```
Pull a list of all pages with an empty meta description.
```

```
Which pages have thin content that's likely to underperform for SEO?
```

```
Find all images missing alt text.
```

```
Our CTAs aren't consistent. Scan the site and flag anywhere the call-to-action wording differs from "Book now."
```

```
The homepage was updated yesterday. Show me what changed compared to the version before.
```

+++

+++让您的资源库保持井然有序

中断的资源引用和未处理的上传会减慢内容生产的速度。 这些提示可帮助您在资源阻止页面更新或营销活动之前查找和管理资源。

**提示**

```
We're building a biking content series. What image assets do we already have?
```

```
Can you upload a placeholder asset from https://placehold.co/800x450/png to the wknd folder and save it as placeholder.png?
```

```
That asset was just uploaded. Is it processed and ready to use in a page?
```

```
I need to replace the hero image across the site. Which fragments are currently using it?
```

+++

+++协调跨多个页面的内容启动

启动活动通常意味着跨多个内容片段和页面协调更改。 这些提示可帮助您对更新进行分组、提升前进行审核以及整齐地发送。

**提示**

```
I need to update the surfing adventure. Show me its content and all its fields.
```

```
Create an EMEA market variation of the ski adventure fragment.
```

```
Bundle everything we changed in this session into a launch called May Updates.
```

```
What launches are open right now, and which ones are ready to promote?
```

```
Before I promote, show me exactly what changed between May Updates and what is currently live.
```

```
Promote the May Updates launch to production.
```

+++


## 更多信息

| 资源 | 您将找到什么 |
| --- | --- |
| AI注册表中的[AEM Content MCP Server](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp){target="_blank"} | 工具列表和可用性 |
| [AEM as a Cloud Service 文档](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service){target="_blank"} | 完整的AEM应用程序文档 |
