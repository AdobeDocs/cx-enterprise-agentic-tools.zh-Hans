---
title: 座席技能
description: 由Adobe策划的工作流和说明，可引导AI代理始终如一地完成CX Enterprise任务。
last-substantial-update: 2026-05-19T00:00:00Z
index: false
source-git-commit: f7ace53bd5988b5902659c89c6da16448398e0c0
workflow-type: tm+mt
source-wordcount: '574'
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

其他客户端要求您下载技能文件并将其直接添加到您的AI客户端。 有关客户端的完整安装说明，请参阅GitHub[&#128279;](https://github.com/adobe/skills#installation)上的Adobe技能自述文件。

### 查找座席技能

浏览[Adobe Skills GitHub存储库](https://github.com/adobe/skills)中可用技能的完整列表。 每个座席技能都包含一个`SKILL.md`文件，其中包含详细的指导、参考和示例。

安装或添加`adobe/skills`包后，某些AI客户端允许您直接列出所有可用技能：

- **克劳德代码**： `claude /plugin list`
- **节点环境**： `npx skills list`
- **GitHub CLI**： `gh upskill list`

## 座席操作技能

“代理技能”可让Adobe的域专业知识在您的AI客户端中起作用，因此代理遵循经过验证的工作流而不是即兴创作。 下面的每个演练都显示了以Adobe最佳实践为指导，从头到尾以可靠的方式完成的特定业务任务。

<!--
CARDS

* https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development
  {title = Develop AEM components with AI}
  {description = Use Claude Code or Cursor with Agent Skills to scaffold, code, and refine AEM components guided by Adobe best practices.}
  {cta = Try with Agent Skills}
  {image = ../assets/agent-skills-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Develop AEM components with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" title="使用AI开发AEM组件" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="使用AI开发AEM组件"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" title="使用AI开发AEM组件">使用AI开发AEM组件</a>
                    </p>
                    <p class="is-size-6">使用具有代理技能的克劳德代码或光标建立、编码和优化AEM组件，以Adobe最佳实践为指导。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">尝试使用代理技能</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
