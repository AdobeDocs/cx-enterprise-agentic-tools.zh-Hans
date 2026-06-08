---
title: 座席技能
description: 由Adobe策划的工作流和说明，可引导AI代理始终如一地完成CX Enterprise任务。
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 2%

---


# 座席技能

<!-- last-modified: 2026-05-19 -->

Adobe CX Enterprise的![代理技能](../assets/hero-agent-skills.png)

“代理技能”是Adobe策划的工作流，可为AI代理提供分步说明，以便可靠地完成Adobe CX Enterprise任务。 每个Agent Skill都编码域专业知识和最佳实践，这样Agent便可以生成一致、经过验证的结果，而无需即兴发挥。 当您希望跨对话进行可重复、引导式行为时，“座席技能”很有意义，特别是对于每次都需要详细提示的任务。 它们补充了MCP服务器和API：代理技能定义代理的工作方式；MCP服务器和API提供底层访问。

所有代理技能都保留在[Adobe Skills GitHub存储库](https://github.com/adobe/skills)中，它是代理技能文档、安装和实施详细信息的主要来源。

## Adobe CX企业代理技能

所有代理技能都保留在[Adobe Skills GitHub存储库](https://github.com/adobe/skills)中。 选择下面的功能区域以探索该工作流的技能。

### Adobe应用程序

<!--
CARDS

* https://github.com/adobe/skills/tree/main/plugins/aem
  {title = Adobe Experience Manager}
  {description = Agent Skills for Experience Manager development, content, design, and project management across AEM as a Cloud Service, Edge Delivery Services, and AEM 6.5 LTS.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-aem-card.png}

* https://github.com/adobe/skills/tree/main/plugins/adobe-analytics
  {title = Adobe Analytics}
  {description = Agent Skills for KPI monitoring, funnel analysis, and executive reporting workflows in Adobe Analytics.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-analytics-card.png}

* https://github.com/adobe/skills/tree/main/plugins/adobe-cja
  {title = Customer Journey Analytics}
  {description = Agent Skills for performance comparison, dimension analysis, and workspace authoring in Customer Journey Analytics.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-cja-card.png}

* https://github.com/adobe/skills/tree/main/plugins/app-builder
  {title = Adobe App Builder}
  {description = Agent Skills for scaffolding, testing, and deploying custom applications with Adobe App Builder.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-cxenterprise-card.png}

* https://github.com/adobe/skills/tree/main/plugins/creative-cloud
  {title = Creative Cloud}
  {description = Agent Skills for batch photo editing, design from templates, video editing, and social media variants with Creative Cloud.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-creative-cloud.png}

-->

有关完整技能详细信息、安装方法和源代码，请参阅[Adobe Skills GitHub存储库](https://github.com/adobe/skills)。

## 座席技能的工作方式

![座席技能的工作方式](../assets/hero-connect-agent-skills.gif)

座席技能是一组指令，用于告知AI座席如何使用Adobe座席工具完成任务。 当代理加载技能时，它会遵循该工作流，而不是即兴操作。

- 座席每次都以相同的方式完成任务
- 域专业知识编码一次，并在对话中重用
- 技能可以将多个代理工具和操作链接到单个工作流中

## 快速入门

代理技能是根据您使用的AI客户端安装的。 某些客户端支持从命令行直接安装：

- **克劳德代码**： `/plugin install adobe/skills`
- **节点环境**： `npx skills add adobe/skills`
- **GitHub CLI**： `gh upskill adobe/skills`

其他客户端要求您下载技能文件并将其直接添加到您的AI客户端。 有关客户端的完整安装说明，请参阅GitHub](https://github.com/adobe/skills#installation)上的[Adobe技能自述文件。

### 查找座席技能

浏览[Adobe Skills GitHub存储库](https://github.com/adobe/skills)中可用技能的完整列表。 每个座席技能都包含一个`SKILL.md`文件，其中包含详细的指导、参考和示例。

安装或添加`adobe/skills`包后，某些AI客户端允许您直接列出所有可用技能：

- **克劳德代码**： `claude /plugin list`
- **节点环境**： `npx skills list`
- **GitHub CLI**： `gh upskill list`

## 代理技能vs MCP服务器vs API for Builder

| | 座席技能 | MCP服务器 | 用于构建器的API |
| --- | --- | --- | --- |
| 用途 | 引导式工作流和最佳实践 | Adobe数据和工作流访问 | 直接系统集成 |
| 编码域专业知识 | 是 | 否 | 否 |
| 需要编码 | 否 | 否 | 是 |
| 最适合 | 可重复、引导式任务 | 数据查询和工作流操作 | 自定义应用程序开发 |
