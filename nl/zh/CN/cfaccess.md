---

copyright:

  years: 2017, 2019

lastupdated: "2019-04-02"

keywords: Cloud Foundry roles, Cloud Foundry access, auditor, manager, developer, billing manager

subcollection: iam

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# Cloud Foundry 访问权
{: #cfaccess}

目前，并非所有服务都可以使用 Cloud IAM 进行管理。您可以继续使用 Cloud Foundry 角色来访问这些服务实例。用户将添加到实例所属的组织和空间，并分配 Cloud Foundry 角色。
{:shortdesc}

下图概述了帐户中的 Cloud Foundry 组织、空间和角色是如何关联的。一个帐户可以具有多个用户、组织和空间。可以根据需要将每个用户分配给任意数量的组织和空间，将用户分配给组织和空间后，就可以通过分配 Cloud Foundry 角色来设置要在每个组织和空间中使用的访问级别。


![使用帐户中的 Cloud Foundry 组织和空间进行访问](images/cf-diagram.svg "如何使用 Cloud Foundry 组织、空间和角色使帐户中的访问权生效")



## Cloud Foundry 角色
{: #cfroles}

Cloud Foundry 角色授予对帐户内组织和空间的访问权。Cloud Foundry 角色不会授予用户在帐户的服务上下文中完成操作的许可权。

通过将用户添加到组织和空间，然后为其分配组织角色和空间角色，从而分配 Cloud Foundry 访问权。根据分配的角色类型，该用户可以对添加到特定空间的服务实例完成特定操作。

![Cloud Foundry 访问权](images/CF.svg "为用户分配对 Cloud Foundry 组织和空间的访问权")

可以在组织级别分配以下角色：

|组织角色|许可权|
|-------------------|-------------|
|管理者|组织管理者可以创建、查看、编辑或删除组织内的空间，查看组织的使用情况和配额，邀请用户加入组织，管理谁有权访问组织及其在组织中的角色，以及管理组织的定制域。|
|记帐管理者|记帐管理者可以在“使用情况”页面上查看组织的运行时和服务使用情况信息。|
|审计员|组织审计员可以查看组织中的应用程序和服务内容。审计员还可以查看组织中的用户及其分配的角色，以及组织的配额。|
{:caption="表 1. 组织角色和许可权" caption-side="top"}

可以在空间级别分配以下角色：

|空间角色|许可权|
|------------|-------------|
|管理者|空间管理者可以添加现有用户，并管理空间内的角色。空间管理者还可以查看空间中每个应用程序的实例数、服务绑定和资源使用情况。|
|开发者|空间开发者可以创建、删除和管理空间内的应用程序和服务。某些管理任务包括部署应用程序，启动或停止应用程序，重命名应用程序，删除应用程序，重命名空间，将服务绑定到应用程序或从应用程序取消绑定服务，以及查看空间中每个应用程序的实例数、服务绑定和资源使用情况。此外，空间开发者还可以将内部或外部 URL 与空间中的应用程序相关联。|
|审计员|空间审计员具有对有关空间的所有信息的只读访问权，例如有关空间中每个应用程序的实例数、服务绑定和资源使用情况的信息。|
{:caption="表 2. 空间角色和许可权" caption-side="top"}

分配有管理者或开发者空间角色的用户可以访问 VCAP_SERVICES 环境变量。但是，分配有审计员角色的用户无法访问 VCAP_SERVICES。
{: note}
