---
title: 在不构建报表的情况下显示营销活动见解
description: 使用CX Enterprise MCP Gateway以简单的语言询问Customer Journey Analytics性能问题，无需浏览Report Builder即可获得答案。
last-substantial-update: 2026-06-02T00:00:00Z
index: false
source-git-commit: 270aed67540f7347850aece70cebddc9b40b9de8
workflow-type: tm+mt
source-wordcount: '1031'
ht-degree: 0%

---


# 在不构建报表的情况下显示营销活动见解

<!-- last-modified: 2026-06-02 -->

![AI客户端显示改善营销活动性能的建议后续步骤](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png)

以前，营销活动分析需要在单独的工具中构建报表，但现在该对话了。 此演练展示了如何将AI客户端连接到Customer Journey Analytics (CJA)，并以简单的语言询问性能问题。 这样可以加快到insight的时间，而无需手动构建报表。

| | |
| --- | --- |
| CX企业级应用程序 | Customer Journey Analytics (CJA) |
| 代理工具 | CX Enterprise MCP网关 |
| 受众 | 分析员、营销活动经理 |
| 先决条件 | 与MCP兼容的AI客户端、CJA访问 |

每个步骤显示一个代表性提示和一个AI响应示例。 您还可完成&#x200B;**更多**&#x200B;部分，以供在同一会话中进行其他探索。

## 开始之前

>[!BEGINTABS]

>[!TAB 克劳德.ai]

将CX Enterprise MCP Gateway作为自定义连接器连接以访问Customer Journey Analytics工具。

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
>出现提示时，请使用您的Adobe ID登录，然后选择链接到您的CJA数据视图的IMS组织。 选择错误的组织是身份验证错误最常见的来源。
>
>在首次连接时，您的AI客户端可能会要求您选择IMS组织或指定沙盒。 设置该上下文后，MCP服务器会将其用于会话的其余部分。
>
>某些工具在执行之前会提示您审批。 查看请求并批准或拒绝 — 未经您的确认不会采取任何操作。

## 步骤1：发现可用的数据视图

首先，请您的AI客户端列出您的CJA帐户中可用的数据视图。 这告知您可在运行任何报表之前查询哪些数据集。

```
What data views are available in my CJA account?
```

+++查看示例响应

![AI客户端列出可用的CJA数据视图](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step1-data-views.png)

+++


## 步骤2：提取营销活动效果数据

识别数据视图后，按收入和转化率要求营销活动效果。 AI会从数据视图解析量度和维度名称，而无需技术ID。

```
For '[data view name]', show me the top campaigns by revenue and conversion rate for the last 30 days.
```

+++查看示例响应

![AI客户端，按Omni-Channel — 多行业数据视图中的收入和转化率显示热门促销活动](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step2.gif)

+++


>[!NOTE]
>
>将`[data view name]`替换为步骤1中数据视图的名称。 在与利益相关者共享之前，在Analysis Workspace中使用相同的数据视图和日期范围交叉检查结果。

## 步骤3：确定性能提升的原因

请让您的AI客户解释各个营销活动组之间性能差异的推动因素。 这会从标题数字转移到下面的变量。

```
What factors are driving the results for these campaign groups?
```

+++查看示例响应

![AI客户端说明驱动营销活动组性能的因素](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step3.gif)

+++


## 步骤4：深入了解特定促销活动类型

通过请求区段级别划分来跟进特定发现。 这揭示了哪些客户类型正在提升营销活动类型的性能。

```
Break down Promotional Email Campaigns by Customer Segment and explain what's driving the high conversion rate.
```

+++查看示例响应

![AI客户端按客户区段划分促销电子邮件促销活动效果](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step4-segment-breakdown.png)

+++


## 步骤5：对所找到的内容执行操作

根据会议中展示的所有内容，要求优先推荐。 请求业务价值评估可帮助您决定首先在何处采取行动。

```
Based on these findings, recommend the highest-impact actions to increase revenue and conversion rates. Prioritize recommendations by expected business value and estimate the potential uplift.
```

+++查看示例响应

![AI客户端推荐具有估计业务值的优先级操作](../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5.gif)

+++


>[!NOTE]
>
>通过CX Enterprise MCP Gateway访问的CJA工具可以在同一会话中在CJA中创建区段、计算量度和Workspace项目。 要更新其他应用程序中的促销活动、历程或内容，请连接相关的MCP服务器或直接转到应用程序。

## 您完成了哪些工作

您在五个提示中将AI客户端连接到Customer Journey Analytics并从数据视图发现移至优先的业务推荐。 您通过收入和转化率确定了热门促销活动，揭示了提升各促销活动组性能的因素，深入挖掘了特定促销活动类型的区段级别详细信息，并收到了具有预计提升度的排名推荐。 这种方法将报告构建替换为直接对话，从而减少了业务问题与基于数据的行动计划之间的时间。

## 您可以完成更多任务

CX Enterprise MCP Gateway可呈现的Customer Journey Analytics见解远多于演练所涵盖的内容。 展开下面的方案以查看可在同一会话中尝试的提示。

+++查找有效内容和无效内容

快速了解正在投放哪些营销活动以及没有投放哪些营销活动可帮助您在查看任何详细报告之前集中精力。 这些提示会在一个会话中为您提供该图片。

**提示**

```
Which campaigns are driving the most revenue and conversions?
```

```
Show me the campaigns that need attention this month.
```

```
What channels are outperforming expectations?
```

```
Identify the biggest performance changes compared to last month.
```

```
Show me conversion performance by traffic source.
```

+++

+++了解促成结果的因素

标题指标告诉您发生了什么。 这些提示可帮助您了解为什么会出现这种情况 — 数字背后是哪些区段、渠道和接触点。

**提示**

```
What factors are driving revenue growth?
```

```
Explain why conversion rates changed this quarter.
```

```
Break down campaign performance by customer segment.
```

```
Which customer segments are growing fastest?
```

```
Which touchpoints contribute most to conversions?
```

+++

+++发现增长机会

知道哪里表现强劲只是事情的一半。 这些提示可帮助您确定可在何处投入更多资金、哪些受众具有余地以及哪些营销活动可以扩展。

**提示**

```
Where should we invest more marketing budget?
```

```
Which audiences have the greatest growth potential?
```

```
Which campaigns should we scale?
```

```
What would have the biggest impact on revenue?
```

+++

+++将见解转化为行动

通过CX Enterprise MCP Gateway访问的CJA工具可以直接在CJA中创建区段、受众、计算量度和Workspace项目，而无需离开您的AI会话。 使用这些提示根据您的发现执行操作。

**提示**

```
Create a segment for high-value customers.
```

```
Build an audience from recent purchasers.
```

```
Create a calculated metric for conversion efficiency.
```

```
Save this analysis as a Workspace project for executive reporting.
```

+++


## 更多信息

| 资源 | 您将找到什么 |
| --- | --- |
| [CJA MCP Server文档](https://developer.adobe.com/analytics-mcp/docs/cja/) | 完整的工具参考和设置指南 |
| [CJA MCP使用指南](https://developer.adobe.com/analytics-mcp/docs/guides/) | 详细使用指南 |
| AI注册表中的[CJA MCP服务器](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | CJA MCP服务器工具和可用性 |
| [Customer Journey Analytics文档](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing) | 完整的CJA应用程序文档 |
