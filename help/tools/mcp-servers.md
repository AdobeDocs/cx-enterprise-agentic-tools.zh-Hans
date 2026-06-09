---
title: MCP服务器
description: 使用模型上下文协议服务器将任何与MCP兼容的AI客户端连接到Adobe CX Enterprise工作流。
index: false
last-substantial-update: 2026-06-09T00:00:00Z
source-git-commit: 36c10d31072f13be42e508944a3ce742818e88b4
workflow-type: tm+mt
source-wordcount: '2068'
ht-degree: 2%

---


# MCP服务器

<!-- last-modified: 2026-06-09 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491320/?learn=on&enablevpops)

Adobe CX Enterprise MCP服务器允许任何兼容的AI客户端直接、受管地访问Adobe数据和工作流。 连接一次，您就可以查询营销活动效果、激活受众、查看历程、管理内容等，所有这些操作都以纯语言进行，而无需离开您的AI环境。 由于MCP服务器位于AI客户端和Adobe的基础系统之间，因此您可以在组织保持有效的访问控制和数据治理的同时获得自然语言的灵活性。

Adobe MCP服务器遵循打开的[模型上下文协议](https://modelcontextprotocol.io/docs/getting-started/intro)标准。 任何与MCP兼容的AI客户端都连接到任何Adobe MCP服务器。

## CX Enterprise MCP

![CX Enterprise MCP将您的AI客户端连接到整个Adobe CX Enterprise套件中的工具](../assets/mcp-gateway-hero.gif)

**一个终结点。 多个CX Enterprise应用程序。**

只需连接一次，您的AI客户端即可根据您组织的许可证访问CX Enterprise应用程序。 您可用的工具自动由Adobe权限决定 — 每个应用程序无需单独的连接。

>[!BEGINTABS]

>[!TAB CX Enterprise应用程序]

根据您组织的Adobe许可证，可以使用每个应用程序的工具。

| 应用程序 | 您可以做什么 |
| --- | --- |
| Adobe Journey Optimizer | [查看历程、营销活动和渠道配置](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) |
| Customer Journey Analytics | [查询报告、发现数据视图、作者工作区](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) |
| Real-Time CDP | [检查目标、激活状态和数据流运行状况](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) （已关闭测试版） |

如果此处未列出您的应用程序，请参阅下面的[MCP服务器的完整列表](#adobe-cx-enterprise-mcp-servers)。

>[!TAB 连接]

无论您要在何处使用特定于应用程序的MCP端点，都使用CX Enterprise MCP端点。

```
https://cx-enterprise.adobe.io/mcp
```

出现提示时，请使用您的Adobe ID登录，然后选择链接到您的Adobe应用程序的IMS组织。 选择错误的组织是缺少工具或身份验证错误的最常见来源。

有关完整设置说明，请参阅下面的[连接到您的AI客户端](#connect-to-your-ai-client)。

>[!ENDTABS]

## Adobe CX Enterprise MCP服务器

下面列出的服务器直接连接。 对于AJO、Customer Journey Analytics和Real-Time CDP，请使用上面的[CX Enterprise MCP](#cx-enterprise-mcp)。

<!--
CARDS

* #cx-enterprise-mcp
  {title = CX Enterprise MCP}
  {description = One connection to AJO, CJA, and Real-Time CDP. Your AI client gets access to the applications your organization is licensed for — automatically.}
  {cta = Connect}
  {image = ../assets/mcp-cxenterprise-card.png}

* https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp
  {title = Adobe Analytics}
  {description = Tools for report suite discovery, dimension and metric analysis, segment authoring, and workspace creation in Adobe Analytics.}
  {cta = View in AI Registry}
  {target = _blank}
  {image = ../assets/mcp-analytics-card.png}

* https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp
  {title = AEM Content}
  {description = Tools for managing pages, content fragments, assets, and launches in Adobe Experience Manager as a Cloud Service using natural language.}
  {cta = View in AI Registry}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly
  {title = AEM Content (Read-Only)}
  {description = Tools for discovering and querying pages, content fragments, and launches in AEM as a Cloud Service. No write access.}
  {cta = View in AI Registry}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp
  {title = AEM Cloud Manager}
  {description = Tools for managing Cloud Manager programs, environments, pipelines, and repositories from your IDE using natural language.}
  {cta = View in AI Registry}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="CX Enterprise MCP">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="#cx-enterprise-mcp" title="CX Enterprise MCP" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-cxenterprise-card.png" alt="CX Enterprise MCP"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="#cx-enterprise-mcp" target="_blank" rel="referrer" title="CX Enterprise MCP">CX Enterprise MCP</a>
                    </p>
                    <p class="is-size-6">一个到AJO、CJA和Real-Time CDP的连接。 您的AI客户端可自动访问您的组织许可使用的应用程序。</p>
                </div>
                <a href="#cx-enterprise-mcp" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">连接</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Analytics">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp" title="Adobe Analytics" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-analytics-card.png" alt="Adobe Analytics"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp" target="_blank" rel="referrer" title="Adobe Analytics">Adobe Analytics</a>
                    </p>
                    <p class="is-size-6">Adobe Analytics中的报表包发现、维度和量度分析、区段创作和工作区创建工具。</p>
                </div>
                <a href="https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">在AI注册表中查看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="AEM Content">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp" title="AEM内容" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-aem-card.png" alt="AEM内容"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp" target="_blank" rel="referrer" title="AEM内容">AEM内容</a>
                    </p>
                    <p class="is-size-6">用于在Adobe Experience Manager as a Cloud Service中使用自然语言管理页面、内容片段、资源和启动项的工具。</p>
                </div>
                <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">在AI注册表中查看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="AEM Content (Read-Only)">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly" title="AEM内容（只读）" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-aem-card.png" alt="AEM内容（只读）"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly" target="_blank" rel="referrer" title="AEM内容（只读）">AEM内容（只读）</a>
                    </p>
                    <p class="is-size-6">用于在AEM as a Cloud Service中搜索和查询页面、内容片段和启动项的工具。 无写入权限。</p>
                </div>
                <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">在AI注册表中查看</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="AEM Cloud Manager">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp" title="AEM Cloud Manager" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-aem-card.png" alt="AEM Cloud Manager"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp" target="_blank" rel="referrer" title="AEM Cloud Manager">AEM Cloud Manager</a>
                    </p>
                    <p class="is-size-6">使用自然语言从IDE中管理Cloud Manager项目、环境、管道和存储库的工具。</p>
                </div>
                <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">在AI注册表中查看</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

### MCP服务器端点

[Adobe AI注册表](https://developer.adobe.com/ai-registry/?type=connector)中列出了所有端点。 如果您已经知道需要什么（在连接之前获取端点URL并扫描可用工具），则此表为快速参考。

| Server | 终结点 | 工具 |
| --- | --- | --- |
| [CX Enterprise MCP](#cx-enterprise-mcp) | `https://cx-enterprise.adobe.io/mcp` | · [Adobe Journey Optimizer tools](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server)<br>· [Customer Journey Analytics tools](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp)<br>· [Real-Time CDP tools](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) |
| [Adobe Analytics](https://developer.adobe.com/analytics-mcp/docs/aa/) | `https://aa-mcp.adobe.io/mcp` | [查看工具](https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp) |
| [AEM Cloud Manager](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | [查看工具](https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp) |
| [AEM内容](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | [查看工具](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) |
| [AEM内容（只读）](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | [查看工具](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly) |

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

运行`claude mcp add`注册CX Enterprise MCP。 通过一个连接，您可以根据组织的许可证访问AJO、CJA和Real-Time CDP。

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

将CX Enterprise MCP添加到您的Cursor `mcp.json`配置文件中，然后通过&#x200B;**设置> MCP**&#x200B;进行连接。

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

通过一个连接，您可以根据组织的许可证访问AJO、CJA和Real-Time CDP。

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

添加CX Enterprise MCP ：

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
  {description = Use CX Enterprise MCP to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use CX Enterprise MCP to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* ../use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use CX Enterprise MCP to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* ../use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine CX Enterprise MCP and AEM Content MCP Server to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* ../use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Use CX Enterprise MCP for a unified view of AJO, CJA, and Real-Time CDP campaign health in one AI session.}
  {cta = Start walkthrough}
-->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze campaign performance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/analyze-campaign-performance.md" title="分析营销活动效果" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Analyze+Campaign+Performance" alt="分析营销活动效果"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" title="分析营销活动效果">分析营销活动效果</a>
                    </p>
                    <p class="is-size-6">使用CX Enterprise MCP从任何AI客户端显示Customer Journey Analytics指标和见解。</p>
                </div>
                <a href="../use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">开始演练</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Query audiences">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="查询受众" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Query+Audiences" alt="查询受众"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" target="_blank" rel="referrer" title="查询受众">查询受众</a>
                    </p>
                    <p class="is-size-6">使用CX Enterprise MCP通过纯语言提示查询Real-Time CDP受众和目标数据。</p>
                </div>
                <a href="../use-cases/query-audiences.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">开始演练</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Review AJO journeys">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-ajo-journeys.md" title="查看AJO历程" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Review+AJO+Journeys" alt="查看AJO历程"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" title="查看AJO历程">查看AJO历程</a>
                    </p>
                    <p class="is-size-6">使用CX Enterprise MCP从AI客户端访问AJO历程、营销活动状态和历程条件。</p>
                </div>
                <a href="../use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">开始演练</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Manage AEM content with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-aem-content.md" title="使用AI管理AEM内容" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Manage+AEM+Content+with+AI" alt="使用AI管理AEM内容"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-aem-content.md" target="_blank" rel="referrer" title="使用AI管理AEM内容">使用AI管理AEM内容</a>
                    </p>
                    <p class="is-size-6">使用自然语言在AEM中发现、更新和发布页面和内容片段。</p>
                </div>
                <a href="../use-cases/manage-aem-content.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">开始演练</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Optimize content based on performance data">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/optimize-content-with-performance-data.md" title="根据性能数据优化内容" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data" alt="根据性能数据优化内容"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" title="根据性能数据优化内容">根据性能数据优化内容</a>
                    </p>
                    <p class="is-size-6">将CX Enterprise MCP与AEM Content MCP Server结合使用，找出性能不佳的内容并在一个会话中进行更新。</p>
                </div>
                <a href="../use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">开始演练</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Run a cross-channel campaign review">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/cross-channel-campaign-review.md" title="运行跨渠道营销活动审核" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review" alt="运行跨渠道营销活动审核"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" title="运行跨渠道营销活动审核">运行跨渠道营销活动审核</a>
                    </p>
                    <p class="is-size-6">使用CX Enterprise MCP在一个AI会话中统一查看AJO、CJA和Real-Time CDP营销活动运行状况。</p>
                </div>
                <a href="../use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">开始演练</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

