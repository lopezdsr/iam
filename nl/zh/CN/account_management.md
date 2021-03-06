---

copyright:

  years: 2019

lastupdated: "2019-04-03"

keywords: account management, access, access policy, account administrator

subcollection: iam

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# 分配对帐户管理服务的访问权
{: #account-services}

作为帐户所有者或帐户管理服务的管理员，您可以使用帐户管理服务向帐户中的用户授予访问权，使其能够邀请用户加入帐户、跟踪计费和使用情况以及处理支持案例。具有访问权的用户还可以管理服务标识、访问策略、目录条目和访问组。

## 为帐户管理服务访问创建策略
{: #account-management-access}

要分配对单个或所有帐户管理服务的访问权，请完成以下步骤：

1. 在菜单栏中，单击**管理** &gt; **访问权 (IAM)**，然后选择**用户**。
2. 在要为其分配访问权的用户所在的行中，选择**操作** ![“操作列表”图标](../icons/action-menu-icon.svg) 菜单，然后单击**分配访问权**。
3. 选择分配对**帐户管理服务**的访问权。
4. 选择**所有帐户管理服务**，或选择特定的帐户管理服务。
5. 选择任意角色组合来分配所需的访问权。

要为另一个用户授予对帐户的完全访问权，以便管理用户访问权和所有帐户资源，您必须分配两个策略。
通过选择**所有启用“身份和访问权”的服务**并分配**管理员**和**管理者**角色来设置其中一个策略，以授予用户对帐户中所有资源的访问权。此外，通过选择**所有帐户管理服务**并分配**管理员**角色来设置另一个策略，以授予用户对帐户中所有帐户管理服务的访问权。
{: tip}

## 帐户管理服务的角色映射操作
{: #account-management-actions-roles}

下表概述了为用户分配每个帐户管理服务的特定角色后，用户可以执行的操作。请查看相关信息以确保为用户分配的是正确访问级别。

|角色|操作|
|:-------|----------|
|查看者|查看访问组和成员|
|操作员|不适用 |
|编辑者|查看、创建、编辑和删除组<br><br> 在组中添加或除去用户|
|管理员|查看、创建、编辑和删除组<br><br> 添加或除去用户<br><br> 将访问权分配给组<br><br> 管理访问权以使用访问组|
{: caption="表 1. 访问组服务的角色和示例操作" caption-side="top"}

|角色|操作|
|:-------|----------|
|查看者|查看帐户中的用户<br><br> 查看用户概要文件设置|
|操作员|查看帐户中的用户<br><br> 查看用户概要文件设置|
|编辑者|查看、邀请、除去和更新帐户中的用户<br><br> 查看和更新用户概要文件设置|
|管理员|查看、邀请、除去和更新帐户中的用户<br><br> 查看和更新用户概要文件设置|
{: caption="表 2. 用户管理服务的角色和示例操作" caption-side="top"}

|角色|操作|
|:-------|----------|
|查看者|查看案例<br><br> 搜索案例|
|操作员|不适用 |
|编辑者|查看案例<br><br> 搜索案例<br><br> 更新案例<br><br> 创建案例|
|管理员|查看案例<br><br> 搜索案例<br><br> 更新案例<br><br> 创建案例|
{: caption="表 3. 支持中心服务的角色和示例操作" caption-side="top"}

{: #billing-acct-mgmt}
|角色|操作|
|:-------|----------|
|查看者|查看帐户功能设置<br><br> 查看帐户中的订阅<br><br> 查看帐户名称<br><br> 查看资源组|
|操作员|查看帐户功能设置<br><br> 查看帐户中的订阅<br><br> 查看和更改帐户名称<br><br> 查看和更新资源组|
|编辑者|查看和更新帐户功能设置<br><br> 查看帐户中的订阅<br><br> 查看帐户中的商品<br><br> 查看和应用特征代码<br><br> 查看和更改帐户名称<br><br> 查看和更新开支限制<br><br> 查看、创建和更新资源组|
|管理员|查看和更新帐户功能设置<br><br> 查看帐户中的订阅<br><br> 查看帐户中的商品<br><br> 查看和应用特征代码<br><br> 查看和更改帐户名称<br><br> 查看和更新开支限制<br><br> 查看预订余额并跟踪使用情况<br><br> 查看、创建、更新和分配用于管理资源组的访问权|
{: caption="表 4. 计费服务的角色和示例操作" caption-side="top"}

|角色|操作|
|:-------|----------|
|查看者|查看标识|
|操作员|创建和删除标识及 API 密钥|
|编辑者|创建、更新和删除标识及 API 密钥|
|管理员|创建、更新和删除标识及 API 密钥<br><br> 将访问策略分配给标识|
{: caption="表 5. IAM 身份服务的角色和示例操作" caption-side="top"}
{: #identity-service-acct-mgmt}

对于 IAM 身份服务，这些操作适用于用户未创建的帐户内的服务标识。所有用户都可以创建服务标识。他们是这些标识的管理员，可以创建关联的 API 密钥和访问策略。但是，此帐户管理服务适用于其他用户对帐户中创建的服务标识进行查看、删除以及分配访问权的能力。
{: note}

|角色|操作|
|:-------|----------|
|查看者|查看私有服务|
|操作员|不适用 |
|编辑者|更改对象元数据，但不能更改私有服务的可视性|
|管理员|更改对象元数据或私有服务的可视性，并限制公共服务的可视性|
{: caption="表 6. 全局目录服务的角色和示例操作" caption-side="top"}

|角色|操作|
|:-------|----------|
|查看者| 帐户管理服务的所有查看者角色操作 |
|操作员| 帐户管理服务的所有操作员角色操作 |
|编辑者| 帐户管理服务的所有编辑者角色操作 |
|管理员| 帐户管理服务的所有管理员角色操作|
{: caption="表 7. 应用于所有身份和访问权服务的策略的角色和示例操作" caption-side="top"}
