---
title: MCP服务器
description: 使用模型上下文协议服务器将任何与MCP兼容的AI客户端连接到Adobe CX Enterprise工作流。
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1601'
ht-degree: 2%

---


# MCP服务器

<!-- last-modified: 2026-05-19 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491320/?learn=on&enablevpops)

Adobe CX Enterprise MCP服务器允许任何兼容的AI客户端直接、受管地访问Adobe数据和工作流。 连接一次，您就可以查询营销活动效果、激活受众、查看历程、管理内容等，所有这些操作都以纯语言进行，而无需离开您的AI环境。 由于MCP服务器位于AI客户端和Adobe的基础系统之间，因此您可以在组织保持有效的访问控制和数据治理的同时获得自然语言的灵活性。

Adobe MCP服务器遵循开放的模型上下文协议标准。 任何与MCP兼容的AI客户端都连接到任何Adobe MCP服务器。

## CX Enterprise MCP网关

![CX Enterprise MCP Gateway将您的AI客户端连接到整个Adobe CX Enterprise套件中的MCP工具](../assets/mcp-gateway-hero.gif)

**一个终结点。 每个Adobe CX Enterprise MCP服务器。**

CX Enterprise Gateway将您的AI客户端路由到跨Analytics、Campaigns、Content和Data的工具，而无需为每个应用程序建立单独的连接。 连接一次，网关将根据您的Adobe权限，仅显示您的组织获得许可的工具。

>[!BEGINTABS]

>[!TAB CX Enterprise应用程序]

根据您组织的Adobe许可证，可以使用每个应用程序的工具。

| 应用程序 | 您可以做什么 |
| --- | --- |
| Adobe Journey Optimizer | [查看历程、营销活动和渠道配置](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) |
| Customer Journey Analytics | [查询报告、发现数据视图、作者工作区](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) |
| Real-Time CDP | [检查目标、激活状态和数据流运行状况](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) （已关闭测试版） |

>[!TAB 连接]

只要您想使用特定于应用程序的MCP端点，就使用CX Enterprise Gateway端点。

```
https://cx-enterprise.adobe.io/mcp
```

>[!NOTE]
>对于AEM，使用直接AEM端点 — AEM不通过CX Enterprise MCP网关路由。

出现提示时，请使用您的Adobe ID登录，然后选择链接到您的Adobe应用程序的IMS组织。 选择错误的组织是缺少工具或身份验证错误的最常见来源。

有关完整设置说明，请参阅下面的[连接到您的AI客户端](#connect-to-your-ai-client)。

>[!ENDTABS]

## Adobe CX Enterprise MCP服务器

下面列出的服务器直接连接，不通过CX Enterprise MCP Gateway路由。 要访问AJO、Customer Journey Analytics和Real-Time CDP，请使用上面的[CX Enterprise MCP Gateway](#cx-enterprise-mcp-gateway)。

<!--
CARDS

* #cx-enterprise-mcp-gateway
  {title = CX Enterprise MCP Gateway}
  {description = One connection to AJO, CJA, and Real-Time CDP tools. The gateway surfaces only the tools your organization is licensed for.}
  {cta = Connect}
  {image = ../assets/mcp-cxenterprise-card.png}

* https://developer.adobe.com/analytics-mcp/docs/aa/
  {title = Adobe Analytics}
  {description = Tools for report suite discovery, dimension and metric analysis, segment authoring, and workspace creation in Adobe Analytics.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-analytics-card.png}

* https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service
  {title = AEM Content}
  {description = Tools for managing pages, content fragments, assets, and launches in Adobe Experience Manager as a Cloud Service using natural language.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service
  {title = AEM Content (Read-Only)}
  {description = Tools for discovering and querying pages, content fragments, and launches in AEM as a Cloud Service. No write access.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://experienceleague.adobe.com/zh-hans/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager
  {title = AEM Cloud Manager}
  {description = Tools for managing Cloud Manager programs, environments, pipelines, and repositories from your IDE using natural language.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

-->

### MCP服务器端点

| Server | 终结点 | 工具 |
| --- | --- | --- |
| [CX Enterprise MCP网关](#cx-enterprise-mcp-gateway) | `https://cx-enterprise.adobe.io/mcp` | · [Adobe Journey Optimizer tools](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server)<br>· [Customer Journey Analytics tools](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp)<br>· [Real-Time CDP tools](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) |
| [Adobe Analytics](https://developer.adobe.com/analytics-mcp/docs/aa/) | `https://aa-mcp.adobe.io/mcp` | [查看工具](https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp) |
| [AEM Cloud Manager](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | [查看工具](https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp) |
| [AEM内容](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | [查看工具](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) |
| [AEM内容（只读）](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | [查看工具](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly) |

## 连接到您的AI客户端

所有Adobe MCP服务器都将OAuth与Adobe Identity Management服务(IMS)结合使用。 出现提示时，选择正确的IMS组织。 选择错误是身份验证错误最常见的来源。

在手动配置之前，请检查[Adobe AI注册表](https://developer.adobe.com/ai-registry/?type=connector)以获取AI客户端和Adobe应用程序的托管连接器。 受管连接器会自动处理身份验证。 如果某个连接器可用于您的客户端和应用程序，请使用该连接器，而不是执行以下手动步骤。

![连接到Adobe MCP服务器的AI代理](../assets/hero-connect-mcp-servers.gif)

>[!BEGINTABS]

>[!TAB 克劳德.ai]

### ![推荐](../assets/badge-recommended.svg)使用托管连接器

转到[Adobe AI注册表](https://developer.adobe.com/ai-registry/?type=connector)并搜索Adobe应用程序。 如果列出了Claude连接器（例如[Adobe Experience Manager连接器](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector)），请按照其设置说明进行操作，而不是执行以下步骤。

### 使用自定义连接器连接

Claude.ai通过帐户设置中的自定义连接器支持远程MCP服务器。

1. 转到&#x200B;**设置>集成**。
2. 单击&#x200B;**添加自定义连接器**。
3. 输入`https://cx-enterprise.adobe.io/mcp`作为URL和显示名称，如`Adobe CX Enterprise`。
4. 单击&#x200B;**连接**&#x200B;并使用您的Adobe ID登录。 选择正确的IMS组织。

完整设置： [Claude.ai自定义连接器文档](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB 克劳德代码]

### 使用CLI

运行`claude mcp add`注册CX Enterprise MCP网关。 通过一个连接，您可以根据组织的许可证访问AJO、CJA和Real-Time CDP工具。

```bash
claude mcp add --transport http adobe-cx-enterprise https://cx-enterprise.adobe.io/mcp
```

### 编辑您的设置文件

将服务器添加到项目根目录（项目级别）中的`~/.claude.json` （全局）或`.mcp.json`：

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

将CX Enterprise MCP网关添加到您的Cursor `mcp.json`配置文件中，然后通过&#x200B;**设置> MCP**&#x200B;连接。

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

一个网关条目允许您根据组织的许可证访问AJO、CJA和Real-Time CDP。

添加后，MCP服务器将显示在“光标设置”的&#x200B;**安装的MCP服务器**&#x200B;下。 选择任何显示&#x200B;**需要身份验证**&#x200B;的服务器旁边的&#x200B;**连接**，然后使用您的Adobe ID登录。 选择有权访问应用程序的IMS组织。

![Cursor MCP服务器配置显示已安装的Adobe MCP服务器和mcp.json](../assets/screenshots/cursor-mcp-server-configuration.jpg)

完整设置： [Cursor MCP文档](https://cursor.com/docs/mcp)

>[!TAB ChatGPT]

### ![推荐](../assets/badge-recommended.svg)使用托管连接器

转到[Adobe AI注册表](https://developer.adobe.com/ai-registry/?type=connector)并搜索Adobe应用程序。 如果列出了ChatGPT连接器，请按照其设置说明进行操作，而不是执行以下步骤。

### 使用远程MCP服务器连接

ChatGPT通过Pro、Plus、Business、Enterprise和Education计划提供的[开发人员模式](https://developers.openai.com/api/docs/guides/developer-mode)支持远程MCP服务器。

1. 在&#x200B;**ChatGPT设置**&#x200B;中启用开发人员模式。
2. 转到&#x200B;**设置>集成**。
3. 单击&#x200B;**添加自定义连接器**&#x200B;并选择&#x200B;**远程MCP服务器**。
4. 输入`https://cx-enterprise.adobe.io/mcp`作为URL，`Adobe CX Enterprise`作为名称。
5. 将身份验证设置为&#x200B;**OAuth**。
6. 单击&#x200B;**连接**&#x200B;并使用您的Adobe ID登录。 选择正确的IMS组织。

完整设置： [ChatGPT MCP文档](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB OpenAI代码CLI]

OpenAI Codex CLI支持通过TOML配置进行远程MCP服务器。

**配置文件位置：**

- **用户级别（所有项目）：** `~/.codex/config.toml`
- 项目根中的&#x200B;**项目作用域：** `.codex/config.toml`

添加CX Enterprise MCP网关：

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
4. 在MCP载入向导中，输入：
   - **服务器名称：** `Adobe CX Enterprise`
   - **服务器URL：** `https://cx-enterprise.adobe.io/mcp`
5. 将身份验证设置为&#x200B;**OAuth 2.0**，并使用Adobe IMS授权和令牌URL进行配置。
6. 选择&#x200B;**创建**，然后选择&#x200B;**添加到代理**。

>[!NOTE]
>
>Copilot Studio中的MCP服务器连接通过Power Platform。 贵组织的数据丢失防护(DLP)策略适用。

完整设置： [Copilot Studio MCP文档](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## 故障排除

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

## 正在使用的代理工具

请参阅应用于实际业务工作流的Adobe CX Enterprise MCP服务器。

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use the CX Enterprise MCP Gateway to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use the CX Enterprise MCP Gateway to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* ../use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use the CX Enterprise MCP Gateway to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* ../use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine the CX Enterprise MCP Gateway and AEM Content MCP Server to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* ../use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Use the CX Enterprise MCP Gateway for a unified view of AJO, CJA, and Real-Time CDP campaign health in one AI session.}
  {cta = Start walkthrough}
-->
