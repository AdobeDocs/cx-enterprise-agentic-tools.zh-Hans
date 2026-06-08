---
title: 用于构建器的API
description: 使用Adobe CX Enterprise API构建自定义应用程序和集成。
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 3%

---


# 用于构建器的API

<!-- last-modified: 2026-06-02 -->

![Adobe CX Enterprise API](../assets/hero-apis.png)

Adobe CX Enterprise API允许开发人员和人工智能辅助编码代理工具直接访问Adobe数据和工作流。 使用它们可以构建自定义应用程序、自动集成，并将Adobe功能嵌入您自己的系统中。 当您需要以编程方式全面控制系统集成，或需要在Adobe数据的基础上构建应用程序时，API是您的正确选择。 有关对Adobe工作流的代理驱动对话访问，请参阅[MCP服务器](mcp-servers.md)。

## Adobe CX Enterprise API

Adobe CX Enterprise API公开了支持Adobe Experience Platform、Journey Optimizer和Customer Journey Analytics等产品的核心数据和操作。 每个API都遵循API优先的设计，允许开发人员和人工智能辅助编码代理工具直接、可编程地访问Adobe内部使用的相同功能。 使用它们构建自定义应用程序、自动化工作流并将Adobe数据集成到您自己的系统中。

<!--
CARDS

* https://developer.adobe.com/audience-manager/
  {title = Audience Manager}
  {description = Audience management and activation workflows.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aam-card.png}

* https://developer.adobe.com/client-sdks/home/
  {title = Client SDKs}
  {description = Mobile SDKs, edge SDKs, and in-app messaging.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://developer.adobe.com/cja-apis/docs/
  {title = Customer Journey Analytics}
  {description = Analytics data access, reporting, and CJA insights workflows.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cja-card.png}

* https://developer.adobe.com/data-collection-apis/docs/
  {title = Data Collection}
  {description = Edge Network data ingestion, real-time event collection, and streaming data delivery.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/developer-console/docs/guides/
  {title = Developer Console}
  {description = API project setup, authentication, and credential management.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://developer.adobe.com/events/docs/
  {title = Events}
  {description = Event-driven integrations, webhooks, and automation triggers.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://experienceleague.adobe.com/en/docs/experience-platform/privacy/home
  {title = Privacy}
  {description = Privacy workflows, data governance, and data subject requests.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/experience-platform-apis/
  {title = Adobe Experience Platform}
  {description = CRUD operations for datasets, schemas, profiles, identities, queries, and segmentation.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/journey-optimizer-apis/
  {title = Adobe Journey Optimizer}
  {description = Journey orchestration, campaign management, content templates, and offer decisioning.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-ajo-card.png}

* https://developer.adobe.com/analytics-apis/docs/2.0/
  {title = Adobe Analytics}
  {description = Reporting, data feeds, calculated metrics, and segment management.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-analytics-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/apis-and-extensions
  {title = AEM as a Cloud Service}
  {description = Content, asset, and workflow management APIs for Adobe Experience Manager.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aem-card.png}

* https://developer.adobe.com/commerce/webapi/
  {title = Adobe Commerce}
  {description = REST and GraphQL APIs for catalog, cart, orders, customers, and promotions.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-commerce-card.png}

* https://developer.adobe.com/umapi/
  {title = User Management}
  {description = User management, identity administration, and enterprise account automation.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}
-->

## Builders与MCP服务器的API

当您需要完全控制系统集成或构建自定义应用程序时，请使用API。 当您希望AI代理直接使用Adobe工作流时，请使用MCP服务器。

| | API | MCP服务器 |
| --- | --- | --- |
| 直接系统集成 | 是 | 有时 |
| 代理友好的编排 | 有限 | 是 |
| 原始数据访问 | 是 | 通常被抽象化 |
| 自定义应用程序开发 | 主要用例 | 辅助 |
| 人工智能辅助的工作流 | 受支持 | 主要用例 |

## 开始使用面向构建器的API

![连接到Adobe CX Enterprise API的IDE](../assets/hero-connect-apis.gif)

Adobe CX Enterprise API在构建之前需要两个条件：来自Adobe Developer Console的经过身份验证的凭据，以及添加到项目中的API文档，以便编码代理可以可靠地与Adobe API一起使用。

### 在Adobe Developer Console中设置API凭据

所有Adobe CX Enterprise API访问均通过[Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)进行管理。 创建项目、添加应用程序所需的API并生成凭据。

1. 登录并在Adobe Developer Console中[创建项目](https://developer.adobe.com/developer-console/docs/guides/projects/)。
2. [为所需的Adobe CX Enterprise应用程序添加API](https://developer.adobe.com/developer-console/docs/guides/services/)。
3. 选择[身份验证类型](https://developer.adobe.com/developer-console/docs/guides/authentication/)。 将&#x200B;**OAuth服务器到服务器**&#x200B;用于自动化工作流，或将&#x200B;**OAuth Web应用程序**&#x200B;用于面向用户的应用程序。
4. 生成您的凭据。 请注意要在应用程序中使用的客户端ID、客户端密钥和令牌端点。

大多数Adobe CX Enterprise API都需要应用程序许可。 如果API在您的Developer Console项目中不可用，请联系您的Adobe代表。

### 将Adobe API上下文添加到您的项目

当您将正确的参考资料添加到项目时，AI编码代理可以可靠地发现并使用Adobe API。 这适用于发布OpenAPI规范的任何Adobe CX Enterprise API。

**1. 查找API规范**

浏览上面列出的[Adobe CX Enterprise API](#adobe-cx-enterprise-apis)，或直接转到[Adobe Developer API目录](https://developer.adobe.com/apis)。

**2. 下载OpenAPI规范**

在您的项目中创建一个`/specs`目录。 从[developer.adobe.com](https://developer.adobe.com/apis)上的API引用页面下载OpenAPI YAML并将其保存在该处。 添加`README.md`以记录源URL和下载日期。

```
/specs/README.md
/specs/aem-assets.openapi.yaml
```

>[!TIP]
>签入快照可为编码代理提供稳定、可重现的行为，并使API更改显示在Git历史记录中。

**3. 生成API索引**

将此提示粘贴到编码代理中，将`<API-SPEC-FILE>`替换为您的文件名：

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and generate /docs/<API-SPEC-FILE>.api.md.

Create a concise API index for AI coding agents. For each operation include: operationId, HTTP method, path, purpose, authentication requirements, required inputs, response shape, common error responses, pagination behavior, asynchronous behavior, and deprecation status.

Do not invent endpoints, parameters, request bodies, response fields, or behavior not present in the OpenAPI specification.
```

**4. 生成代理说明**

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and /docs/<API-SPEC-FILE>.api.md.

Generate AGENTS.md. Instructions should:
- Treat the OpenAPI specification as the source of truth.
- Use the API index as a navigation guide.
- Never invent endpoints, parameters, response fields, or status codes.
- Prefer documented operationIds.
- Avoid deprecated or experimental APIs unless explicitly requested.
- Follow authentication requirements defined in the specification.
- Use the local OpenAPI snapshot for implementation decisions.
```

**5. 验证**

要求编码代理仅使用生成的文件完成简单任务：

```
Write a function that takes an AEM asset ID and returns the asset title and description. Use only /specs/aem-assets.openapi.yaml and /docs/aem-assets.api.md.
```

如果代理程序正确完成它而没有发明行为，则设置完成。

**推荐的项目结构**

```
project/
├── specs/
│   ├── README.md
│   └── aem-assets.openapi.yaml
├── docs/
│   └── aem-assets.api.md
└── AGENTS.md
```

**保持规格为最新**

当Adobe发布新的API版本时：将新的快照下载到`/specs`中，更新`README.md`中的日期，并重新生成索引和`AGENTS.md`。
