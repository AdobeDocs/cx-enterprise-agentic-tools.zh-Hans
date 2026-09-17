---
title: 在旅程问题影响客户之前对其进行捕获
description: 使用Adobe Journey Optimizer MCP服务器可在活动中的AJO历程到达受众之前，监控其运行情况、审查营销活动配置和表面操作问题。
last-substantial-update: 2026-09-16
source-git-commit: a70eede6e0efe0d1dbdc00c5d9de5aeb3b5d75de
workflow-type: tm+mt
source-wordcount: '1071'
ht-degree: 4%
---

# 在旅程问题影响客户之前对其进行捕获
<!-- last-modified: 2026-06-08 -->

![AI客户端使用执行摘要总结活动和历程策略](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png){zoomable="yes"}

*选择缩放。*

未检测到的历程问题可在任何人注意到之前联系客户。 本演练展示了如何通过检查活动的AJO历程、查看Campaign配置和通过AI客户端显示操作问题、使用Adobe Journey Optimizer MCP服务器以纯语言获取答案而不打开Adobe Journey Optimizer，保持其领先地位。

| 方案详细信息 | |
| --- | --- |
| CX企业级应用程序 | [Adobe Journey Optimizer (AJO)](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/ajo-home) |
| 代理式工具 | [CX Enterprise Coworker](https://experienceleague.adobe.com/zh-hans/docs/cx-enterprise-coworker/content/home)或[Adobe Journey Optimizer MCP服务器](../tools/mcp-servers.md) |
| 受众 | 营销活动经理、营销人员 |
| 先决条件 | 与MCP兼容的AI客户端、AJO访问 |

每个步骤显示一个代表性提示和一个AI响应示例。 您还可完成&#x200B;**更多**&#x200B;部分，以供在同一会话中进行其他探索。


## 开始之前

>[!BEGINTABS]

>[!TAB CX Enterprise Coworker]

获得这些答案的最快方法是CX Enterprise Coworker，它不需要服务器设置或AI客户端配置。 [尝试CX Enterprise Coworker](https://experienceleague.adobe.com/zh-hans/docs/cx-enterprise-coworker/content/home)

如果您希望将自己的AI客户端直接连接到Adobe Journey Optimizer，请参阅以下选项卡。

>[!TAB 克劳德.ai]

将Adobe Journey Optimizer MCP服务器作为自定义连接器连接。

1. 转到Claude.ai中的&#x200B;**设置>集成**。
2. 选择&#x200B;**添加自定义连接器**&#x200B;并输入服务器URL： `https://ajo-mcp.adobe.io/mcp`
3. 选择&#x200B;**连接**&#x200B;并使用您的Adobe ID登录。

完整设置： [Claude.ai自定义连接器文档](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

使用ChatGPT Developer Mode（需要专业、Plus、商业、企业或教育计划）连接Adobe Journey Optimizer MCP服务器。

1. 在&#x200B;**ChatGPT设置**&#x200B;中启用&#x200B;**开发人员模式**。
2. 转到&#x200B;**设置>集成**，然后选择&#x200B;**添加自定义连接器>远程MCP服务器**。
3. 输入服务器URL： `https://ajo-mcp.adobe.io/mcp`
4. 选择&#x200B;**连接**&#x200B;并使用您的Adobe ID登录。

完整设置： [ChatGPT MCP文档](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB 其他AI客户端]

使用Gemini、Microsoft Copilot、Cursor、Claude Code或其他与MCP兼容的环境？ 使用以下端点连接到Adobe Journey Optimizer MCP服务器：

```
https://ajo-mcp.adobe.io/mcp
```

所有受支持客户端的完整设置说明： [连接到您的AI客户端](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>出现提示时，请使用您的Adobe ID登录，然后选择链接到您的AJO环境的IMS组织。 选择错误的组织是身份验证错误最常见的来源。
>
>在首次连接时，您的AI客户端可能会要求您选择IMS组织或指定沙盒。 设置该上下文后，MCP服务器会将其用于会话的其余部分。
>
>某些工具在执行之前会提示您审批。 查看请求并批准或拒绝。 未经确认，不执行任何操作。


## 步骤1：发现活动历程及其用途

首先，请求提供活动历程及其背后的业务目标的清单。 这可提供您在任何特定旅程中的完整情况。

```
What customer journeys are currently available and what business objectives do they support?
```

+++查看示例响应

![AI客户端列出可用的客户历程及其业务目标](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step1.gif){zoomable="yes"}

*选择缩放。*

+++



## 步骤2：查看历程的步骤和客户体验

查看历程列表后，请让您的AI客户浏览特定历程的步骤，并解释客户在每个阶段的体验。

```
Walk me through the [journey name] journey and explain the customer experience.
```

+++查看示例响应

![AI客户端正在经历欢迎新客户历程步骤和客户体验](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step2-welcome-journey.png){zoomable="yes"}

*选择缩放。*

+++


>[!NOTE]
>
>将`[journey name]`替换为步骤1结果中的历程名称。


## 步骤3：查看营销活动、受众和目标

从历程转移到营销活动。 要求您总结一下哪些营销活动处于活跃状态、以哪些人为目标，以及它们旨在推动什么结果。

```
Show me our campaigns, the audiences they target, and the outcomes they're designed to drive.
```

+++查看示例响应

![AI客户端列出了活动营销活动及其受众定位和预期结果](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step3.gif){zoomable="yes"}

*选择缩放。*

+++



## 步骤4：了解营销活动和历程如何关联

要求您的AI客户将营销活动和历程之间的圆点连接起来，并解释他们如何共同努力实现共享参与目标。

```
How do our campaigns and journeys work together to improve customer engagement?
```

+++查看示例响应

![AI客户端，用于说明营销活动与历程之间的关系](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step4-connection.png){zoomable="yes"}

*选择缩放。*

+++



## 步骤5：获取优先推荐

从生命周期营销经理的角度出发，要求优先推荐后续要关注的内容。 这揭示了会话中审查的所有内容中最具影响力的差距和机会。

```
If you were our lifecycle marketing manager, what would you prioritize next and why?
```

+++查看示例响应

![提供优先级生命周期营销建议的AI客户端](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5.gif){zoomable="yes"}

*选择缩放。*

+++


>[!NOTE]
>
>AJO MCP服务器可显示历程和营销活动信息，但无法修改历程、营销活动或内容。 要实施推荐，请直接转到AJO应用程序，或连接AEM Content MCP Server以查看同一会话中的内容更改。


## 您完成了哪些工作

您将AI客户端连接到Adobe Journey Optimizer，并通过五个提示全面了解您的旅程和活动组合。 您清点活动历程及其业务目标，审查特定历程的分步客户体验，将活动营销活动映射到其受众和预期结果，了解营销活动和历程如何协作，并收到关于下一步重点位置的优先级建议。 这样无需打开AJO界面，即可让生命周期营销和营销活动经理从战略上了解情况。


## 您可以完成更多任务

Adobe Journey Optimizer MCP服务器可以显示各种AJO历程和营销活动详细信息。 展开下面的方案以查看可在同一会话中尝试的提示。

+++在进行更改之前了解实时内容

在不知道还有什么正在运行的情况下改变旅程是有风险的。 这些提示会为您提供活动的内容、最近修改的内容以及营销活动的配置方式的当前清单。

**提示**

```
Show me all journeys modified in the last 7 days.
```

```
Show me all journeys that use SMS as a channel.
```

```
Which campaigns are scheduled to end this week?
```

```
What loyalty challenges are currently active?
```

+++

+++深入了解特定历程的详细信息

当您需要审阅、批准或交付历程时，无需打开AJO即可将完整的逻辑呈现在您面前，从而节省时间。 这些提示会根据需要提示表面条件、计划和区段规则。

**提示**

```
What is the entry condition for the [journey name] journey?
```

```
What are the exit conditions and timeout rules for the [journey name] journey?
```

```
What messages and wait conditions are in the [journey name] journey?
```

```
Which segment does the [journey name] journey target?
```

+++

+++深入了解特定营销活动的详细信息

如果您需要在批准、分发或更改活动之前查看活动的完整配置，这些操作会提示显示受众规则、渠道设置和计划详细信息，而不需要打开AJO。

**提示**

```
Walk me through the full configuration of the [campaign name] campaign.
```

```
What audience does the [campaign name] campaign target and how large is that segment?
```

```
What frequency cap and send schedule apply to the [campaign name] campaign?
```

```
Are any campaigns targeting overlapping audiences?
```

```
What channel configurations are set up in our AJO environment?
```

+++



## 更多信息

| 资源 | 您将找到什么 |
| --- | --- |
| AI注册表中的[AJO MCP服务器](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server){target="_blank"} | AJO MCP服务器工具和可用性 |
| [AJO文档](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/ajo-home){target="_blank"} | 完整的AJO应用程序文档 |
