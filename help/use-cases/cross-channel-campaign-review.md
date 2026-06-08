---
title: 运行跨渠道营销活动审核
description: 在单次AI会话中使用CX Enterprise MCP网关可跨历程、受众和性能统一查看AJO、CJA和Real-Time CDP营销活动运行状况。
index: false
source-git-commit: 14488b494c454ce6d1207e2d21024749d93db669
workflow-type: tm+mt
source-wordcount: '1433'
ht-degree: 4%

---


# 运行跨渠道营销活动审核

<!-- last-modified: 2026-05-21 -->

![运行跨渠道营销活动审核](https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review)

要全面了解营销活动的运行状况，需要来自多个系统的数据：来自AJO的活动历程、来自Real-Time CDP的受众激活状态以及来自CJA的性能指标。 本演练展示了如何在单个AI会话中连接所有三个，以使您能够通过一次会话而不是通过三个单独的工具从历程状态转变为受众健康状况以及性能趋势。

| | |
| --- | --- |
| CX企业级应用程序 | Adobe Journey Optimizer、Customer Journey Analytics、Real-Time CDP |
| 代理工具 | CX Enterprise MCP网关 |
| 受众 | 营销活动经理、营销运营 |
| 先决条件 | 与MCP兼容的人工智能客户端，访问AJO、CJA和Real-Time CDP |

每个步骤显示一个代表性提示和一个AI响应示例。 您还可完成&#x200B;**更多**&#x200B;部分，以供在同一会话中进行其他探索。

## 开始之前

>[!BEGINTABS]

>[!TAB 克劳德.ai]

将CX Enterprise MCP Gateway作为自定义连接器连接。 通过一个连接，您可以访问AJO、CJA和Real-Time CDP工具。

1. 转到Claude.ai中的&#x200B;**设置>集成**。
2. 选择&#x200B;**添加自定义连接器**&#x200B;并输入服务器URL： `https://cx-enterprise.adobe.io/mcp`
3. 选择&#x200B;**连接**&#x200B;并使用您的Adobe ID登录。

完整设置： [Claude.ai自定义连接器文档](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

使用ChatGPT Developer Mode （需要Pro 、 Plus 、 Business 、 Enterprise或Education计划）连接CX Enterprise MCP Gateway。

1. 在&#x200B;**ChatGPT设置**&#x200B;中启用&#x200B;**开发人员模式**。
2. 转到&#x200B;**设置>集成**，然后选择&#x200B;**添加自定义连接器>远程MCP服务器**。
3. 输入服务器URL： `https://cx-enterprise.adobe.io/mcp`
4. 选择&#x200B;**连接**&#x200B;并使用您的Adobe ID登录。

完整设置： [ChatGPT MCP文档](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB 其他AI客户端]

使用Gemini、Microsoft Copilot、Cursor、Claude Code或其他与MCP兼容的环境？ 使用此端点连接到CX Enterprise MCP网关：

```
https://cx-enterprise.adobe.io/mcp
```

所有受支持客户端的完整设置说明： [连接到您的AI客户端](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>出现提示时，使用您的Adobe ID登录并选择链接到您的AJO、CJA和Real-Time CDP环境的IMS组织。 选择错误的组织是身份验证错误最常见的来源。
>
>在首次连接时，您的AI客户端可能会要求您选择IMS组织或指定沙盒。 设置该上下文后，MCP服务器会将其用于会话的其余部分。
>
>某些工具在执行之前会提示您审批。 查看请求并批准或拒绝 — 未经您的确认不会采取任何操作。

## 步骤1：查看活动历程和营销活动

从AJO开始建立当前正在运行的项目。 了解哪些历程处于实时状态且最近进行了修改，为审阅的其余部分奠定了基础。

```
What journeys are currently active in AJO?
```

+++查看示例响应

在您的AJO组织中找到8个活动历程：

| 历程 | 渠道 | 上次修改时间 |
| --- | --- | --- |
| 欢迎系列 — 新成员 | 电子邮件、推送 | 2026年5月18日 |
| 购买后跟进 | 电子邮件、短信 | 2026年5月14日 |
| 忠诚度重新参与 | 电子邮件 | 2026年5月20日 |
| 已放弃的购物车 — 24小时 | 电子邮件、短信 | 2026年5月10日 |
| Spring Promotion | 电子邮件、推送 | 2026年5月19日 |
| 回馈 — 90天不活动 | 电子邮件 | 2026年4月28日 |
| 生日奖励 | 电子邮件 | 2026年4月15日 |
| 重新参与 — 推送选择退出 | 短信 | 2026年5月12日 |

过去7天内修改了3个历程。 要了解其中任何一项的详细信息吗？

+++


## 步骤2：检查受众激活状态

查看历程后，验证为这些营销活动提供支持的受众是否正确流向其目标。

```
Show me the activation status for the high-value loyalty segment.
```

+++查看示例响应

**高价值忠诚度区段** — 目标之间的激活状态：

| 目标 | 状态 | 上次成功运行 | 受众规模 |
| --- | --- | --- | --- |
| Google Ads | 活动 | 2026年5月21日凌晨02:14 | 48,320 |
| Meta Ads | 活动 | 2026年5月21日上午01:58 | 48,295 |
| Salesforce Marketing Cloud | 活动 | 2026年5月20日晚上11:30 | 47,940 |
| Adobe Target | 活动 | 2026年5月21日半夜12:00 | 48,320 |

未检测到数据流错误。 过去3小时内完成的所有激活。

+++


## 步骤3：从CJA中提取性能指标

建立历程和受众上下文后，使用CJA评估这些营销活动的转化方式以及参与度的下降位置。

```
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
```

+++查看示例响应

**忠诚度重新参与活动** — 2026年4月21日至5月21日：

| 渠道 | 发送 | CTR | 转化 | 同意 评价 |
| --- | --- | --- | --- | --- |
| 电子邮件 | 48,320 | 8.4% | 1,973 | 4.1% |
| 推送 | 31,200 | 12.1% | 987 | 3.2% |

综合转化率：3.8%。 Email CTR与之前30天相比增长了1.2%。 推送转化保持不变。

+++


## 步骤4：综合营销活动运行状况摘要

请您的AI客户在所有三个来源中汇集图像，并展示任何需要关注的内容。

```
Give me a summary of our campaign health: what is running, which audiences are activated, and how performance looks against last month.
```

+++查看示例响应

以下是您当前在AJO、Real-Time CDP和CJA中的营销活动运行状况摘要：

**活动历程：** 8个已上线，3个本周修改。 忠诚度重新参与历程是最近更新的。

**受众激活：**&#x200B;所有区段都正确流动到4个目标。 未检测到数据流错误。

**绩效：**&#x200B;忠诚度促销活动中的电子邮件CTR上升。 推送转换持平。 没有渠道出现显着下降。

**要注意的标志：**

- 回溯历程（90天不活动）上次修改于23天前，最近未审查过。
- 推送转化率连续3个周期保持平稳 — 值得回顾消息传递或时间安排。

未检测到严重问题。 上述两项内容值得在下一次营销活动启动之前审查。

+++


这就是多服务器方法取得成效的地方：在一次对话中跨越历程配置、受众状态和性能数据的AI客户端原因。

## 步骤5：对所找到的内容执行操作

审查发现了两个项目。 请咨询您的AI客户端，帮助您确定每个项目的优先级并为其路由选择。

```
For each flag you identified, what should I do and where should I go to do it?
```

+++查看示例响应

以下是两种旗帜的优先行动计划：

**1. Win-Back journey — 查看重新进入条件（AJO MCP，如果需要更改，则查看AJO应用程序）**

23天内未修改回溯历程。 让我介绍一下它目前的重返条件和退出逻辑。 如果条件陈旧或不正确，则需要对旅程流进行结构性更改以打开AJO。 可在此处进行频率上限和受众更新。

**2. 3个期间的推送转换平坦 — 更新消息或测试变体**

平面转换通常表示消息疲劳或选件和受众不匹配。 两条路径：

- **立即更新推送内容(AEM MCP)：**&#x200B;如果推送通知链接到登陆页面，请添加AEM Content MCP Server并更新页面副本或CTA，而无需切换工具。
- **运行推送A/B测试（AJO应用程序）：**&#x200B;使用不同的消息创建营销活动级别的变体，以隔离该变体是内容还是目标。 这要求直接转到AJO。

您想从哪个开始？

+++


## 您完成了哪些工作

您通过将AJO、Real-Time CDP和CJA连接到单个AI会话，运行了跨渠道营销活动运行状况审查。 您无需打开三个应用程序并手动组装图片，而是在一次对话中浏览历程状态、受众激活和性能数据。 综合摘要为营销活动经理提供了一种更快的途径，使他们能够识别哪些组件在运行、哪些组件需要调整，以及下一步应在何处重点关注。

## 您可以完成更多任务

借助AJO、CJA和Real-Time CDP在同一会话中连接，您可以超越演练。 展开下面的方案以查看可以尝试的提示。

+++在启动新项目之前准确了解正在运行的项目

重叠的历程、最近修改的营销活动以及您尚未审阅的渠道都可能会影响新的启动项。 在添加任何内容之前，这些提示会为您提供清晰的当前状态图像。

**提示**

```
Which journey has the most active profiles right now?
```

```
Show me all journeys modified in the last 7 days.
```

```
Which campaigns are scheduled to end this week?
```

```
Are any journeys targeting the same segment as the campaign I'm about to launch?
```

+++

+++确保受众能够访问正确的目标

激活问题无任何提示 — 区段停止流动，您的营销活动会发送到较小的列表，而不会出现任何警告。 这些会在影响结果之前提示曲面间隙和误差。

**提示**

```
Which audiences have grown the most in the last 30 days?
```

```
Are there any dataflow errors across my active destinations?
```

```
How many records were exported to each destination in the last 7 days?
```

```
Are there any audiences with no active destinations?
```

+++

+++了解哪些功能有效，以及下一步应在何处重点关注

跨渠道的性能趋势可让您了解在哪里投资以及收回哪些投资。 这些提示可帮助您确定哪些因素在推动业绩，以及下一季度的注意力应该流向何处。

**提示**

```
Show me email performance trends for the last 90 days.
```

```
Which campaigns are underperforming against their conversion targets?
```

```
What is the average revenue per conversion this month compared to last month?
```

```
Which channel has the highest conversion rate across all active campaigns?
```

+++


## 更多信息

| 资源 | 您将找到什么 |
| --- | --- |
| [AJO文档](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/ajo-home) | 完整的AJO应用程序文档 |
| [Analytics MCP文档](https://developer.adobe.com/analytics-mcp/docs/) | CJA MCP设置和工具参考 |
| [Real-Time CDP MCP文档](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) | RTCDP MCP设置指南 |
| AI注册表中的[AJO MCP服务器](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) | AJO MCP服务器工具和可用性 |
| AI注册表中的[CJA MCP服务器](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | CJA MCP服务器工具和可用性 |
| [MCP服务器](../tools/mcp-servers.md) | 将AI客户端连接到Adobe MCP服务器 |
