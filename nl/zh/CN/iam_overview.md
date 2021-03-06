---

copyright:

  years: 2017, 2019

lastupdated: "2019-01-28"

keywords: IBM Cloud IAM, user identities, service ID, policies, access management, roles, actions

subcollection: iam


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# IAM 概念
{: #iamconcepts}

## 身份
{: #identity}

{{site.data.keyword.Bluemix_notm}} IAM 中的身份概念由以下部分组成：

<dl>
<dt>用户身份</dt>
<dd>所有用户都通过其 IBM 标识进行标识。</dd>
<dt>服务和应用程序身份</dt>
<dd>服务标识是用于为服务和应用程序提供单独身份的 Cloud IAM 功能。可以创建服务标识以供需要访问 {{site.data.keyword.Bluemix_notm}} 服务的应用程序使用，这样就不必使用个别用户的凭证。</dd>
<dt>API 密钥</dt>
<dd>通过 Cloud IAM 提供了 {{site.data.keyword.cloud_notm}} API 密钥，以供您用于通过将 API 或 CLI 用作用户或服务标识进行认证。这些 API 密钥是通过 Cloud IAM 提供的，因此通常无法用于在 IBM Cloud 之外使用 IBM 标识进行认证。用户还可以具有单个经典基础架构 API 密钥，可用于访问经典基础架构 API；但是，这不是必需的，因为您可以使用 {{site.data.keyword.cloud_notm}} API 密钥来访问相同的 API。</dd>
<dt>资源</dt>
<dd>{{site.data.keyword.Bluemix_notm}} 资源通过其云资源名称 (CRN) 进行识别。有关更多信息，请参阅[云资源名称](/docs/overview?topic=overview-crn#crn)。</dd>
</dl>

## 访问权管理
{: #am}

{{site.data.keyword.Bluemix_notm}} 中的访问权管理概念由一些相互关联的部分组成，包括用户、资源、策略、角色、操作和 Cloud IAM 控制系统，这些组成部分允许用户对帐户中的资源执行操作。

可以查看以下列表以了解有关这些 Cloud IAM 组成部分的更多信息：

<dl>
<dt>用户</dt>
<dd>帐户中的所有用户都通过其 IBM 标识进行标识。可以邀请用户加入帐户并向其授予对资源的访问权。可以分配对单个资源下至实例级别的访问权，也可以分配对组织成帐户资源组的一组资源的访问权。</dd>
<dt>访问组</dt>
<dd>一组用户和服务标识可以由帐户所有者创建，以便可以使用单个策略将相同访问权分配给组中的所有实体。</dd>
<dt>资源</dt>
<dd>帐户资源是从目录中选择的供应服务产品或是某个服务实例中的更细颗粒度资源。</dd>
<dt>策略</dt>
<dd>策略是向帐户中的用户、服务标识和访问组授予访问帐户资源的许可权的方法。策略包括主体、目标和角色。主体是要为其提供访问权的用户、服务标识或访问组。策略的目标是要提供其访问权的资源。而角色是用于定义策略目标上的访问级别或所允许操作的方法。有不同类型的策略允许访问帐户资源：资源组策略、资源实例策略、用于访问所有启用“身份和访问权”的服务的帐户范围策略，以及一个或所有帐户管理服务上的策略。根据您的选择，可能会有定制的配置选项，例如定义下至特定区域中资源的访问权，或定义具体到实例中特定于服务的粒度级别资源的访问权。</dd>
<dt>角色</dt>
<dd>Cloud IAM 访问角色允许用户对策略中定义的资源完成特定任务。有两种类型的访问角色：平台管理和服务访问。平台管理角色定义允许用于在平台级别管理资源的操作，例如用户访问权、创建服务实例。平台角色还适用于可在帐户管理服务上下文中采取的操作，例如，邀请和除去用户，管理访问组，管理服务标识和私有目录产品。此外，服务访问角色定义在使用此服务（例如调用服务 API）的上下文中允许的操作。这些角色基于策略中所选服务进行定制。</dd>
<dt>操作</dt>
<dd>操作会映射到 Cloud IAM 角色，以支持用户在分配有不同角色时仅执行特定任务。针对每个角色的允许操作可能会根据所访问的服务而有所不同，因为每个服务都会定义该角色如何映射到服务的使用。</dd>
<dt>访问管理系统</dt>
<dd>Cloud IAM 控制系统根据分配的策略，允许或拒绝用户在服务上下文中执行操作。用户尝试完成特定操作时，控制系统会使用策略中定义的属性来确定用户是否有权执行该任务。</dd>
</dl>
