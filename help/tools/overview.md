---
title: 代理工具
description: 比较MCP服务器、代理技能和Builders的API ，并为Adobe CX Enterprise工作流选择合适的代理工具。
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 1%

---


# 代理工具

<!-- last-modified: 2026-05-08 -->

并非每一种仿造工具方法都满足同样的需求。 通过MCP服务器，您可以从任何兼容的AI客户端以自然语言立即访问Adobe数据，而无需编码。 代理技能将Adobe域专业知识编码为可重复的代理工作流，以便任务每次都以一致的方式运行。 API为开发人员提供了完全的编程控制，以便构建自定义应用程序和集成。 本页将介绍权衡，以便您选择适合自己情况的正确起点。

<!--
CARDS

* mcp-servers.md
  {title = MCP Servers}
  {description = Connect any compatible AI client to Adobe CX Enterprise data and workflows. No coding required.}
  {cta = Explore MCP Servers}
  {image = ../assets/mcp-servers-card.png}

* agent-skills.md
  {title = Agent Skills}
  {description = Adobe-curated workflow instructions that guide agents through CX Enterprise tasks consistently.}
  {cta = Explore Agent Skills}
  {image = ../assets/agent-skills-card.png}

* apis.md
  {title = APIs for Builders}
  {description = Build custom applications and integrations using the same APIs that power Adobe products.}
  {cta = Explore APIs for Builders}
  {image = ../assets/apis-card.png}

-->

## 比较代理工具

| | MCP服务器 | 座席技能 | 用于构建器的API |
| --- | --- | --- | --- |
| 最适合 | AI客户端用户 | 所有用户 | 开发者 |
| 需要编码 | 否 | 否 | 是 |
| 设置时间 | Minutes | Minutes | 小时到天 |
| 您获得的内容 | 从AI工具访问Adobe | 引导式可重复工作流 | 完全程序化控制 |
| 需要AI客户端 | 是 | 是 | 可选 |

## 不确定从哪里开始？

- 要使用AI与Adobe CX Enterprise应用程序进行交互（执行操作、查询数据以及让AI通过自然对话发现下一步要做什么），[MCP服务器](mcp-servers.md)是最灵活的起点。
- 为了让代理始终如一地遵循Adobe本机工作流而不进行即兴操作，[代理技能](agent-skills.md)在可重用说明中对域专业知识进行编码。
- 要构建可简化或自动执行用户特定Adobe工作流的重点应用程序，[Builders的API](apis.md)可让您直接、可编程地控制所发生的情况。

>[!BEGINTABS]

>[!TAB MCP服务器]

可将MCP服务器视为连接您的AI工具与Adobe的实时连接线。 连接一次，您的AI可以查询营销活动、拉取受众、检查历程状态等。 全部使用纯语言，无需代码。

**在以下情况下使用MCP服务器：**

- 您希望Adobe数据位于已使用的AI工具中
- 您正在执行探索性分析或临时数据检索
- 您希望快速获得结果，而不使项目变得繁琐

**尝试：**&#x200B;请让Claude总结您的活动历程。 从ChatGPT中提取Real-Time CDP受众大小。 在不打开功能板的情况下查看CJA促销活动量度。

[浏览MCP服务器](mcp-servers.md)

>[!TAB 代理技能]

“代理技能”是Adobe的域专业知识，按照您的代理可遵循的说明进行编码。 与其希望你的经纪人能找出正确的步骤，不如用技能告诉它该怎么做。 可靠、可重复，并且已针对Adobe工作流进行了调整。

**在以下情况下使用代理技能：**

- 您每次都希望以相同的方式完成相同的任务
- 您正在运行可重复的内容或媒体生产工作流
- 你需要一个认识Adobe的探员，而你不需要解释

**试用：**&#x200B;批量编辑照片集以使其具有凝聚力。 从一个源资产生成适用于平台的社交变体。 在几个提示中从Adobe Express模板进行设计。

[浏览座席技能](agent-skills.md)

>[!TAB 生成器的 API]

API是构建块。 借助这些功能，开发人员可以使用支持Adobe自身产品的相同API，以编程方式直接访问Adobe数据和操作。 使用它们构建按您的计划、条款和栈栈运行的项目。

**在以下情况下使用API：**

- 您正在构建自定义应用程序或功能板
- 您需要将Adobe数据集成到另一个系统中
- 您正在使用Claude代码或光标生成完整的应用程序
- 您需要完全创建、更新或删除控件

**尝试：**&#x200B;生成自定义营销活动仪表板。 自动化数据管道。 使用Claude代码生成可读取和写入Adobe Experience Platform的应用程序。

[浏览用于构建器的API](apis.md)

>[!ENDTABS]

## 将它们一起使用

MCP服务器、代理技能和API是互补的。 许多工作流将这三者结合在一起：

- 座席技能定义工作流并指导座席
- MCP服务器在工作流中向代理授予对Adobe数据的读取权限
- API处理需要直接系统写入或自定义应用程序逻辑的操作
