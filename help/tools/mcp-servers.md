---
title: MCP服务器
description: 使用模型上下文协议服务器将任何与MCP兼容的AI客户端连接到Adobe CX Enterprise工作流。
index: false
last-substantial-update: 2026-06-17T00:00:00Z
source-git-commit: 9dda1df512aea64703843cfb22603af5f239a490
workflow-type: tm+mt
source-wordcount: '2074'
ht-degree: 2%

---


# MCP服务器

<!-- last-modified: 2026-06-11 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491320/?learn=on&enablevpops)

Adobe CX Enterprise MCP服务器允许任何兼容的AI客户端直接、受管地访问Adobe数据和工作流。 连接一次，您就可以查询营销活动效果、激活受众、查看历程、管理内容等，所有这些操作都以纯语言进行，而无需离开您的AI环境。 由于MCP服务器位于AI客户端和Adobe的基础系统之间，因此您可以在组织保持有效的访问控制和数据治理的同时获得自然语言的灵活性。

Adobe MCP服务器遵循打开的[模型上下文协议](https://modelcontextprotocol.io/docs/getting-started/intro)标准。 任何与MCP兼容的AI客户端都连接到任何Adobe MCP服务器。

## CX Enterprise MCP服务器 {#cx-enterprise-mcp-servers}

>[!CONTEXTUALHELP]
>id="cx-enterprise-agentic-tools_mcp_servers_cx-enterprise"
>title="CX Enterprise MCP"
>abstract="您的CX Enterprise应用程序，可通过单个MCP端点访问。 以简明的语言向人工智能客户提问、分析和采取行动。"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/overview" text="CX Enterprise MCP文档"

![CX Enterprise MCP将您的AI客户端连接到整个Adobe CX Enterprise套件中的工具](../assets/mcp-gateway-hero.gif)

选择一个应用程序以查看端点和功能。

>[!BEGINTABS]

>[!TAB CX Enterprise MCP]

**一个终结点。 多个CX Enterprise应用程序。**

只需连接一次，您的AI客户端即可根据您组织的许可证访问CX Enterprise应用程序。 若要启用您的组织，请发送电子邮件至[cxo-mcp-feedback@adobe.com](mailto:cxo-mcp-feedback@adobe.com)以请求获取访问权限。

```
https://cx-enterprise.adobe.io/mcp
```

| CX企业级应用程序 | 您可以做什么 |
| --- | --- |
| [Adobe Analytics](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/analytics-mcp) | 报表包发现、区段创作和工作区创建 |
| [Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/aep-mcp) | 数据集发现、架构浏览和沙盒管理 |
| [Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/ajo-mcp) | 查看历程、营销活动和渠道配置 |
| Adobe Journey Optimizer B2B edition | 管理B2B历程、帐户计划、购买组和个性化 |
| [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/cja-mcp) | 查询报表、发现数据视图和创作工作区 |
| [Marketo Engage](https://experienceleague.adobe.com/zh-hans/docs/marketo-developer/marketo/mcp-server) | 管理项目、营销策划、潜在客户、智能列表、电子邮件和表单 |
| [Real-Time CDP](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) | 检查受众激活状态、目标运行状况和数据流运行状况 |

有关完整文档，请参阅[CX Enterprise MCP](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/overview)。

>[!NOTE]
>
>对每个CX Enterprise应用程序的访问取决于贵组织在Adobe Admin Console中的权利和用户权限。 要为贵组织启用CX Enterprise MCP，请发送电子邮件至[cxo-mcp-feedback@adobe.com](mailto:cxo-mcp-feedback@adobe.com)。

>[!TAB Experience Manager]

Adobe Experience Manager有多台MCP服务器用于不同的工作流。

| MCP服务器 | 终结点 | 您可以做什么 |
| --- | --- | --- |
| [AEM Cloud Manager](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | 管理项目、环境、管道和存储库 |
| [AEM内容](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | 管理页面、内容片段、资源和启动项 |
| [AEM内容（只读）](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | 探索和查询页面、内容片段以及没有写入权限的启动项 |
| [AEM体验管理](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/mcp-servers/experience-governance-mcp-server) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-governance` | 根据品牌准则和合规性规则评估内容和图像 |

>[!NOTE]
>
>对每个AEM环境的访问取决于贵组织的AEM Cloud Service权利和用户在该环境中的权限。

>[!TAB Experience Platform]

| MCP服务器 | 终结点 | 您可以做什么 |
| --- | --- | --- |
| Adobe Marketing Agent | `https://aep-ai-ama.adobe.io/mcp` | 跨AEP应用程序编排受众分析、AEP诊断和AJO B2B历程构建 |

>[!NOTE]
>
>访问取决于贵组织的Adobe Experience Platform权利和用户的权限。

>[!TAB Target]

Adobe Target MCP处于公开测试阶段。 所有当前可用的工具均为只读。 已计划正式提供写入工具。

| MCP服务器 | 终结点 | 您可以做什么 |
| --- | --- | --- |
| [Adobe Target](https://experienceleague.adobe.com/zh-hans/docs/target/using/mcp/target-mcp) | `https://targetmcp.adobe.io/mcp` | 查看活动、选件、受众、mbox和性能报表 |

>[!NOTE]
>
>访问权限取决于您的Adobe Target权利和用户的权限。

>[!TAB Workfront]

| MCP服务器 | 终结点 | 您可以做什么 |
| --- | --- | --- |
| [Adobe Workfront](https://experienceleague.adobe.com/zh-hans/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-overview) | `https://mcp.prod.us-west-2.aws.wfk8s.com/mcp/v1/workfront` | 管理工作、项目、规划记录、见解和内容审批 |

>[!NOTE]
>
>访问取决于您的Adobe Workfront许可证和用户的权限。

>[!ENDTABS]

## 连接到您的AI客户端

大多数Adobe MCP服务器都将OAuth与Adobe Identity Management服务(IMS)结合使用。 出现提示时，选择正确的IMS组织。 选择错误是身份验证错误最常见的来源。

![连接到Adobe MCP服务器的AI代理](../assets/hero-connect-mcp-servers.gif)

以下步骤使用CX Enterprise MCP端点作为示例。 同一过程适用于任何Adobe MCP服务器：交换要连接的服务器的端点URL。

>[!BEGINTABS]

>[!TAB 克劳德.ai]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="推荐">使用托管连接器

转到[Adobe AI注册表](https://developer.adobe.com/ai-registry/?type=connector)并搜索Adobe应用程序。 如果列出了Claude连接器（例如[Adobe Experience Manager连接器](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector)），请按照其设置说明进行操作，而不是执行以下步骤。

### 使用自定义连接器连接

Claude.ai通过帐户设置中的自定义连接器支持远程MCP服务器。

1. 转到&#x200B;**设置>集成**。
2. 单击&#x200B;**添加自定义连接器**。
3. 输入服务器端点，作为URL（例如，CX Enterprise MCP为`https://cx-enterprise.adobe.io/mcp`）和您选择的显示名称。
4. 单击&#x200B;**连接**&#x200B;并使用您的Adobe ID登录。 选择正确的IMS组织。

完整设置： [Claude.ai自定义连接器文档](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB 克劳德代码]

### 使用CLI

运行`claude mcp add`以注册Adobe MCP服务器。 将服务器名称和URL替换为要连接的服务器的值。 此示例使用CX Enterprise MCP ：

```bash
claude mcp add --transport http adobe-cx-enterprise https://cx-enterprise.adobe.io/mcp
```

### 编辑您的设置文件

将服务器添加到项目根目录（项目级别）中的`~/.claude.json` （全局）或`.mcp.json`。 将密钥和URL替换为要连接的服务器的值：

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

Adobe MCP服务器使用OAuth。 在首次调用工具时，克劳德代码会提示您使用Adobe ID进行身份验证。 出现提示时，选择正确的IMS组织。

完整设置： [Claude Code MCP文档](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB 游标]

将Adobe MCP服务器添加到您的Cursor `mcp.json`配置文件中，然后通过&#x200B;**设置> MCP**&#x200B;进行连接。 将密钥和URL替换为您要连接的服务器的值。 此示例使用CX Enterprise MCP ：

- **全局（所有项目）：** `~/.cursor/mcp.json`
- 项目根目录中的&#x200B;**项目级别：** `.cursor/mcp.json`

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

添加后，MCP服务器将显示在“光标设置”的&#x200B;**安装的MCP服务器**&#x200B;下。 选择任何显示&#x200B;**需要身份验证**&#x200B;的服务器旁边的&#x200B;**连接**，然后使用您的Adobe ID登录。 选择有权访问应用程序的IMS组织。

![Cursor MCP服务器配置显示已安装的Adobe MCP服务器和mcp.json](../assets/screenshots/cursor-mcp-server-configuration.jpg)

完整设置： [Cursor MCP文档](https://cursor.com/docs/mcp)

>[!TAB ChatGPT]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="推荐">使用托管连接器

转到[Adobe AI注册表](https://developer.adobe.com/ai-registry/?type=connector)并搜索Adobe应用程序。 如果列出了ChatGPT连接器，请按照其设置说明进行操作，而不是执行以下步骤。

### 使用远程MCP服务器连接

ChatGPT通过Pro、Plus、Business、Enterprise和Education计划提供的[开发人员模式](https://developers.openai.com/api/docs/guides/developer-mode)支持远程MCP服务器。

1. 在&#x200B;**ChatGPT设置**&#x200B;中启用开发人员模式。
2. 转到&#x200B;**设置>集成**。
3. 单击&#x200B;**添加自定义连接器**&#x200B;并选择&#x200B;**远程MCP服务器**。
4. 输入服务器端点，作为URL（例如，CX Enterprise MCP为`https://cx-enterprise.adobe.io/mcp`）和您选择的显示名称。
5. 将身份验证设置为&#x200B;**OAuth**。
6. 单击&#x200B;**连接**&#x200B;并使用您的Adobe ID登录。 选择正确的IMS组织。

完整设置： [ChatGPT MCP文档](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB OpenAI代码CLI]

OpenAI Codex CLI支持通过TOML配置进行远程MCP服务器。

**配置文件位置：**

- **用户级别（所有项目）：** `~/.codex/config.toml`
- 项目根中的&#x200B;**项目作用域：** `.codex/config.toml`

将部分名称和URL替换为要连接的服务器的值。 此示例使用CX Enterprise MCP ：

```toml
[mcp_servers.adobe-cx-enterprise]
url = "https://cx-enterprise.adobe.io/mcp"
enabled = true
```

Adobe MCP服务器使用OAuth。 Codex CLI在首次使用时自动处理OAuth流程。 出现提示时，选择正确的IMS组织。

完整设置： [OpenAI Codex CLI MCP文档](https://developers.openai.com/codex/mcp)

>[!TAB Copilot Studio]

Microsoft Copilot Studio使用“MCP载入向导”连接到远程MCP服务器，该向导会自动创建Power Platform自定义连接器。

1. 在Copilot Studio中打开您的代理。
2. 转到&#x200B;**工具**&#x200B;页面。
3. 选择&#x200B;**添加工具>新建工具>模型上下文协议**。
4. 在MCP载入向导中，输入服务器详细信息。 例如，对于CX Enterprise MCP ：
   - **服务器名称：** `Adobe CX Enterprise`
   - **服务器URL：** `https://cx-enterprise.adobe.io/mcp`
5. 将身份验证设置为&#x200B;**OAuth 2.0**，并使用Adobe IMS授权和令牌URL进行配置。
6. 选择&#x200B;**创建**，然后选择&#x200B;**添加到代理**。

>[!NOTE]
>
>Copilot Studio中的MCP服务器连接通过Power Platform。 贵组织的数据丢失防护(DLP)策略适用。

完整设置： [Copilot Studio MCP文档](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## 正在运行的MCP服务器

请参见Adobe CX Enterprise MCP Server来解决实际业务问题。 每次演练都从真正的操作挑战开始，并显示AI客户端如何以简单的语言解决它，而无需切换工具或编写代码。

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Campaign insights without reports}
  {description = Ask performance questions in plain language and get answers from Customer Journey Analytics, without building a single report.}
  {cta = Surface campaign insights}

* ../use-cases/query-audiences.md
  {title = Audience activation at a glance}
  {description = See which audiences are live, where they are flowing, and whether destinations are healthy, without navigating Real-Time CDP.}
  {cta = Check audience activation}

* ../use-cases/manage-ajo-journeys.md
  {title = Catch journey issues early}
  {description = Monitor active journeys and surface operational issues before they reach your audience.}
  {cta = Monitor your journeys}

* ../use-cases/manage-aem-content.md
  {title = Ship content updates faster}
  {description = Find, update, and publish AEM pages and content fragments faster, without switching to the AEM interface.}
  {cta = Ship content faster}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Close content performance gaps}
  {description = Surface conversion gaps in CJA, trace them to underperforming content in AEM, and apply the fix in a single AI session.}
  {cta = Close performance gaps}
-->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Campaign insights without reports">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/analyze-campaign-performance.md" title="不带报表的营销活动洞察">
                        <img class="is-bordered-r-small" src="../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="不带报表的营销活动洞察"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/analyze-campaign-performance.md" title="不带报表的营销活动洞察">没有报表的营销活动分析</a>
                    </p>
                    <p class="is-size-6">使用简单的语言提出性能问题并从Customer Journey Analytics获得答案，而无需构建单个报表。</p>
                </div>
                <a href="../use-cases/analyze-campaign-performance.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">表面营销活动分析</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Audience activation at a glance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="Audience Activation概览">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="Audience Activation概览"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" title="Audience Activation概览">Audience Activation概览</a>
                    </p>
                    <p class="is-size-6">无需导航Real-Time CDP，即可查看哪些受众处于实时状态、流量在哪里，以及目标是否健康。</p>
                </div>
                <a href="../use-cases/query-audiences.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">检查受众激活</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Catch journey issues early">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-ajo-journeys.md" title="及早发现历程问题">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png" alt="及早发现历程问题"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-ajo-journeys.md" title="及早发现历程问题">提早发现历程问题</a>
                    </p>
                    <p class="is-size-6">在活动历程和表面操作问题影响受众之前，对其进行监控。</p>
                </div>
                <a href="../use-cases/manage-ajo-journeys.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">监视您的历程</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Ship content updates faster">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-aem-content.md" title="更快地发送内容更新">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="更快地发送内容更新"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-aem-content.md" title="更快地发送内容更新">更快地发送内容更新</a>
                    </p>
                    <p class="is-size-6">无需切换到AEM界面，即可更快地查找、更新和发布AEM页面和内容片段。</p>
                </div>
                <a href="../use-cases/manage-aem-content.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">更快地发送内容</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Close content performance gaps">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/optimize-content-with-performance-data.md" title="弥补内容性能差距">
                        <img class="is-bordered-r-small" src="../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5-03-page-compare.png" alt="弥补内容性能差距"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/optimize-content-with-performance-data.md" title="弥补内容性能差距">弥补内容性能差距</a>
                    </p>
                    <p class="is-size-6">在CJA中显示转化差距，跟踪它们以发现AEM中的内容性能不佳，并在单个AI会话中应用修复。</p>
                </div>
                <a href="../use-cases/optimize-content-with-performance-data.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">弥补性能差距</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## 需要更多帮助？

MCP连接涉及身份验证、组织选择和应用程序级别的权限。 如果某些组件无法按预期工作，这些步骤会涵盖最常见的原因。

+++切换Adobe组织

如果您的Adobe用户属于多个IMS组织，并且您看到错误的组织的工具或数据，请断开MCP服务器的连接，在浏览器中注销Adobe会话，然后重新连接。 在登录过程中，系统将提示您选择组织。

Adobe CX Enterprise MCP服务器一次只能向一个IMS组织进行身份验证，即使您的用户帐户有权访问多个组织也是如此。

+++

+++指定沙盒、报表包、环境或其他会话资源

某些Adobe CX Enterprise MCP服务器在返回结果之前需要您指定资源。 根据应用程序，这可能是一个沙盒、程序、环境、报表包或数据视图。

如果不确定您有权访问哪些资源，请咨询AI客户端。 例如：“列出可用的沙盒”或“我有权访问哪些报表包？” Adobe CX Enterprise MCP服务器通常可以返回用户可用的资源的完整列表。

设置会话资源后，您可以随时通过通知AI客户端要使用哪个会话资源来切换该资源。

+++

+++权限和访问错误

AI客户端使用OAuth代表您的Adobe用户帐户。 当您登录到Adobe应用程序时应用的权限和访问控制在您使用MCP服务器时同样适用。

如果操作失败或未返回任何结果，请检查您的用户是否在Adobe Admin Console和相关CX Enterprise应用程序中拥有所需的权限。 如果您需要调整访问权限，请联系您的Adobe系统管理员。

+++

+++丢失会话后重新进行身份验证

Adobe CX Enterprise MCP服务器使用OAuth来验证您的Adobe用户帐户。 如果身份验证状态丢失，则在您重新进行身份验证之前，将不再成功调用工具。

要重新进行身份验证：打开AI客户端的MCP服务器配置，选择Adobe CX Enterprise MCP服务器条目，然后重新连接。 系统将提示您再次使用Adobe ID登录。

+++
