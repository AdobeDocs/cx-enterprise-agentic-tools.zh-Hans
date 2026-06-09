---
title: 座席技能
description: 由Adobe策划的工作流和说明，可引导AI代理始终如一地完成CX Enterprise任务。
last-substantial-update: 2026-05-19T00:00:00Z
index: false
source-git-commit: 8f499ad7baf1b5d08dfac90511d0c76e8372c08b
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 1%

---


# 座席技能

<!-- last-modified: 2026-05-19 -->

Adobe CX Enterprise的![代理技能](../assets/hero-agent-skills.png)

“代理技能”是Adobe策划的工作流，可为AI代理提供分步说明，以便可靠地完成Adobe CX Enterprise任务。 每个Agent Skill都编码域专业知识和最佳实践，这样Agent便可以生成一致、经过验证的结果，而无需即兴发挥。 当您希望跨对话进行可重复、引导式行为时，“座席技能”很有意义，特别是对于每次都需要详细提示的任务。 它们补充了MCP服务器和API：代理技能定义代理的工作方式；MCP服务器和API提供底层访问。

## Adobe CX Enterprise代理技能

选择下面的功能区域以探索该工作流的技能。

>[!BEGINTABS]

>[!TAB Adobe Experience Manager]

适用于AEM as a Cloud Service、Edge Delivery Services和AEM 6.5 LTS中的Experience Manager开发、内容、设计和项目管理的代理技能。

[查看座席技能](https://github.com/adobe/skills/tree/main/plugins/aem)

>[!TAB Adobe Analytics]

适用于Adobe Analytics中KPI监控、funnel分析和执行报告工作流的代理技能。

[查看座席技能](https://github.com/adobe/skills/tree/main/plugins/adobe-analytics)

>[!TAB Customer Journey Analytics]

在Customer Journey Analytics中进行性能比较、维度分析和工作区创作的代理技能。

[查看座席技能](https://github.com/adobe/skills/tree/main/plugins/adobe-cja)

>[!TAB Adobe App Builder]

适用于基架、测试和部署自定义应用程序与Adobe App Builder的代理技能。

[查看座席技能](https://github.com/adobe/skills/tree/main/plugins/app-builder)

>[!TAB Creative Cloud]

通过Creative Cloud批量编辑照片、从模板进行设计、编辑视频和设计社交媒体变体的代理技能。

[查看座席技能](https://github.com/adobe/skills/tree/main/plugins/creative-cloud)

>[!ENDTABS]

## 添加座席技能

![座席技能的工作方式](../assets/hero-connect-agent-skills.gif)

座席技能是一组指令，用于告知AI座席如何使用Adobe座席工具完成任务。 当代理加载技能时，它会遵循该工作流，而不是即兴操作。

### 安装代理技能

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
