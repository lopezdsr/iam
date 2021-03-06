---

copyright:

  years: 2015, 2019
lastupdated: "2019-05-01"

keywords: service ID, service ID access, managing access for service IDs

subcollection: iam

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# 管理服务标识访问策略
{: #serviceidpolicy}

创建服务标识时，可以为该服务标识分配服务策略，以控制允许用于向服务进行认证的访问级别。您可以随时通过更改现有策略，删除策略或指定新策略来更新这些已分配的访问策略。
{:shortdesc}

如果删除或编辑当前正在使用的服务标识的现有策略，那么可能会导致服务中断。
{: note}

## 分配新访问权
{: #access_new}

要分配对资源组中所有资源的访问权，或分配仅对资源组中一项服务的访问权，请完成以下步骤：

1. 在菜单栏中，单击**管理** &gt; **访问权 (IAM)**，然后选择**服务标识**。
2. 从表中选择要为其分配服务策略的服务标识。
3. 单击**访问策略**。
4. 单击**分配访问权**。
5. 选择**按资源组分配**。
6. 选择资源组。
7. 为**分配对资源组的访问权**字段选择角色。此选项支持用户在自己的资源列表上查看资源组，编辑资源组名称或管理用户对资源组的访问权。如果希望用户仅有权访问您指定的资源，而无权访问资源所分配到的组，那么可以选择**无访问权**。
8. 选择资源组中的服务，或选择提供对所选组中所有服务的访问权。
9. 选择任意角色组合来为用户分配所需的访问权。此访问权仅适用于为策略选择的资源。它并不授予对实际容器（即资源组）的访问权。
10. 选择**分配**。

要分配对帐户中单个资源的访问权，请完成以下步骤：

1. 在菜单栏中，单击**管理** &gt; **访问权 (IAM)**，然后选择**服务标识**。
2. 从表中选择要为其分配服务策略的服务标识。
3. 单击**访问策略**。
4. 单击**分配访问权**。
5. 选择**按资源分配**。
6. 选择服务。
7. 选择**所有当前区域**或特定区域（如果系统提示选择）。
8. 选择**所有当前服务实例**或选择特定服务实例。
9. 根据所选择的服务，可能会看到以下字段。如果您未输入这些字段的值，那么会在服务实例级别而非存储区级别来分配策略。
    * **资源类型**：输入**存储区**。
    * **资源标识**：输入存储区的名称。
10. 选择任意角色组合来为用户分配所需的访问权。
11. 选择**分配**。

要分配对单个帐户管理服务或所有帐户管理服务的访问权，请完成以下步骤：

1. 在菜单栏中，单击**管理** &gt; **访问权 (IAM)**，然后选择**服务标识**。
2. 从表中选择要为其分配服务策略的服务标识。
3. 单击**访问策略**。
4. 单击**分配访问权**。
5. 选择分配对**帐户管理服务**的访问权。
6. 选择**所有帐户管理服务**，或选择特定的帐户管理服务。
7. 选择任意角色组合来分配所需的访问权。

您可能会收到一条消息，指示某个现有策略的详细信息与您所选择的详细信息相同。如果正在创建的策略与现有策略的详细信息和角色完全相同，那么系统会提示您更改新策略，因为不允许有重复的策略。如果正在创建的策略与现有策略的详细信息相同，但角色分配不同，那么系统会提示您查看和更新现有策略，使其具有您要指定的角色分配。
{: tip}

## 编辑现有访问权
{: #access_edit}

要编辑现有策略，请执行以下操作：

1. 在菜单栏中，单击**管理** &gt; **访问权 (IAM)**，然后选择**服务标识**。
2. 从表中选择要编辑其服务策略的服务标识。
3. 单击**访问策略**。
4. 确定要编辑的策略所在的行，然后从**操作** ![“操作列表”图标](../icons/action-menu-icon.svg) 菜单中，选择**编辑策略**。
5. 进行更改，然后保存策略。

要使用 CLI 更新服务策略，可以使用 [ibmcloud iam service-policy-update](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_iam#ibmcloud_iam_service_policy_update) 命令。
```
ibmcloud iam service-policy-update SERVICE_ID POLICY_ID [-v, --version VERSION] {--file JSON_FILE | [-r, --roles ROLE_NAME1,ROLE_NAME2...] [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]} [-f, --force]",
```
{: codeblock}

编辑服务标识的访问权时，您可能会收到有关不允许重复策略的消息。如果您编辑的是现有策略，而且所执行的更改与已分配的访问权相冲突，那么可以选择更改当前正在编辑的策略以提供不同的访问权，也可以转至现有冲突的策略来进行查看，并视需要进行更改。如果有满足您需求的重复策略存在，那么您可能需要删除正在编辑的策略。
{: tip}

## 除去访问权
{: #access_remove}

要除去现有策略，请执行以下操作：

1. 在菜单栏中，单击**管理** &gt; **访问权 (IAM)**，然后选择**服务标识**。
2. 从表中选择要删除其服务策略的服务标识。
3. 单击**访问策略**。
4. 确定要删除的策略所在的行，然后从**操作** ![“操作列表”图标](../icons/action-menu-icon.svg) 菜单中，选择**除去**。
5. 复查即将除去的策略的详细信息，然后通过单击**除去**进行确认。

要使用 CLI 删除服务策略，可以使用 [ibmcloud iam service-policy-delete](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_iam#ibmcloud_iam_service_policy_delete) 命令。
```
ibmcloud iam service-policy-delete SERVICE_ID POLICY_ID [-f, --force]
```
{: codeblock}
