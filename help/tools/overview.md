---
title: 代理工具
description: 比较MCP服务器、代理技能和Builders的API ，并为Adobe CX Enterprise工作流选择合适的代理工具。
last-substantial-update: 2026-06-08T00:00:00Z
index: false
source-git-commit: 76a2dc291781d0555e0b128eb6c0e226759f5cc8
workflow-type: tm+mt
source-wordcount: '839'
ht-degree: 0%

---


# 代理工具

<!-- last-modified: 2026-06-08 -->

并非每个代理工具都满足同样的需求。 探索每个报表包的用途、使用时间以及如何入门，以便您选择适合自己情况的正确起点。

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
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="MCP Servers">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="mcp-servers.md" title="MCP服务器">
                        <img class="is-bordered-r-small" src="../assets/mcp-servers-card.png" alt="MCP服务器"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="mcp-servers.md" title="MCP服务器">MCP服务器</a>
                    </p>
                    <p class="is-size-6">将任何兼容的AI客户端连接到Adobe CX Enterprise数据和工作流。 无需编码。</p>
                </div>
                <a href="mcp-servers.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">浏览MCP服务器</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="agent-skills.md" title="座席技能">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="座席技能"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="agent-skills.md" title="座席技能">代理技能</a>
                    </p>
                    <p class="is-size-6">由Adobe策划的工作流说明，可指导代理始终如一地完成CX Enterprise任务。</p>
                </div>
                <a href="agent-skills.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">探索代理技能</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="apis.md" title="用于构建器的API">
                        <img class="is-bordered-r-small" src="../assets/apis-card.png" alt="用于构建器的API"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        生成器的<a href="apis.md" title="用于构建器的API">API</a>
                    </p>
                    <p class="is-size-6">使用支持Adobe产品的相同API构建自定义应用程序和集成。</p>
                </div>
                <a href="apis.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">浏览生成器的API</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->


## 比较代理工具

| | MCP服务器 | 座席技能 | 用于构建器的API |
| --- | --- | --- | --- |
| 最适合 | CX Enterprise应用程序用户 | CX企业应用程序用户和开发人员 | 开发者 |
| 需要编码 | 否 | 否 | 是 |
| 设置时间 | Minutes | Minutes | 小时到天 |
| 您获得的内容 | 从您的AI客户端访问CX企业应用程序 | 引导式可重复工作流 | 完全程序化控制 |

## 不确定从哪里开始？

- 要使用AI与CX Enterprise应用程序进行交互（执行操作、查询数据以及让AI通过自然对话发现下一步要做什么），[MCP服务器](mcp-servers.md)是最灵活的起点。
- 为了使代理始终遵循CX企业工作流的Adobe最佳实践而不进行即兴操作，[代理技能](agent-skills.md)在可重用说明中对域专业知识进行编码。
- 为了构建一个能够简化或自动化用户的特定CX Enterprise工作流的重点应用程序，[Builders的API](apis.md)为您提供了直接、可编程的控制功能，让您能够控制实际发生的情况。

>[!BEGINTABS]

>[!TAB MCP服务器]

将MCP服务器视为AI客户端与CX企业应用程序之间的实时线路。 只需连接一次，您的AI就可以查询营销活动、拉取受众、检查历程状态等，所有这些操作都使用纯语言，无需代码。

**在以下情况下使用MCP服务器：**

- 您希望将AI直接集成到CX Enterprise工作流中
- 您希望CX Enterprise数据位于已使用的AI客户端中
- 您正在执行探索性分析或临时数据检索
- 您希望快速获得结果，而不使项目变得繁琐

[浏览MCP服务器](mcp-servers.md)

>[!TAB 代理技能]

“代理技能”是Adobe的域专业知识，按照您的代理可遵循的说明进行编码。 与其希望您的代理能够指出正确的步骤，不如用一种技能准确地告诉您应该做什么，而且这一技能可靠、可重复而且已经针对CX Enterprise工作流进行了调整。

**在以下情况下使用代理技能：**

- 当您通过AI客户端在CX Enterprise应用程序中执行工作时，希望遵循Adobe最佳实践
- 您每次都希望以相同的方式完成相同的任务
- 您正在运行可重复的内容或媒体生产工作流

[浏览座席技能](agent-skills.md)

>生成器的[!TAB API]

API是构建块。 借助这些功能，开发人员可以使用支持Adobe自身产品的相同API，以编程方式直接访问Adobe数据和操作。 使用它们构建集中的自定义体验，通过组织需求的护栏简化特定业务工作流。

**在以下情况下使用API：**

- 您正在为特定的业务用例构建自定义应用程序或集成
- 您需要使用特定的护栏和控制来优化或自动化工作流
- 您正在使用Claude代码或光标生成完整的应用程序
- 您需要将CX Enterprise数据集成到另一个系统中

[浏览用于构建器的API](apis.md)

>[!ENDTABS]

## 将它们一起使用

这些工具旨在协同工作。 将它们组合在一起可让您充分利用Adobe AI。 代理技能可以指导AI客户端如何使用MCP服务器，使代理在CX Enterprise工作流程中保持正确跟踪。 技能还可以指导如何以及何时调用API，将Adobe最佳实践护栏添加到自定义自动化。 你不必只选一个。

## 正在使用的代理工具

请参见这些应用于实际CX Enterprise工作流的工具。

<!--
CARDS

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use CX Enterprise MCP to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Try with MCP}

* https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development
  {title = Develop AEM components with AI}
  {description = Use Claude Code or Cursor with Agent Skills to scaffold, code, and refine AEM components guided by Adobe best practices.}
  {cta = Try with Agent Skills}
  {image = ../assets/agent-skills-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app
  {title = Invoke AEM APIs from a web app}
  {description = Build a web application that authenticates users and calls AEM OpenAPIs using OAuth to deliver governed, programmatic access.}
  {cta = Try with APIs}
  {image = ../assets/using-api-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Query audiences">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="查询受众">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="查询受众"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" title="查询受众">查询受众</a>
                    </p>
                    <p class="is-size-6">使用CX Enterprise MCP通过纯语言提示查询Real-Time CDP受众和目标数据。</p>
                </div>
                <a href="../use-cases/query-audiences.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">尝试使用MCP</span>
                </a>
            </div>
        </div>
    </div>
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
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Invoke AEM APIs from a web app">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" title="从Web应用程序调用AEM API" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/using-api-card.png" alt="从Web应用程序调用AEM API"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" target="_blank" rel="referrer" title="从Web应用程序调用AEM API">从Web应用调用AEM API</a>
                    </p>
                    <p class="is-size-6">使用OAuth构建可验证用户身份并调用AEM OpenAPIs的Web应用程序，以提供受控制的编程访问。</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">尝试使用API</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
