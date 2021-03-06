---

copyright:

  years: 2017, 2019

lastupdated: "2019-01-28"

keywords: Cloud Foundry access, assign access, add user to organization, Cloud Foundry roles

subcollection: iam

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# 管理 Cloud Foundry 存取權
{: #mngcf}

若要管理帳戶組織及空間的存取權，您必須是帳戶擁有者、組織管理員或空間管理員。
{:shortdesc}

## 更新 Cloud Foundry 存取權
{: #update_cf_access}

1. 從功能表列按一下**管理** &gt; **存取 (IAM)**，然後選取**使用者**。
2. 從您要指派存取權的使用者列中，選取**動作** ![「動作清單」圖示](../icons/action-menu-icon.svg) 功能表，然後按一下**指派存取權**。
3. 選取**使用 Cloud Foundry 指派**。
4. 展開獲指派使用者的組織列，以檢視使用者的空間存取權及其在這些空間中的角色。
5. 從 Cloud Foundry 區段的**動作** ![「動作清單」圖示](../icons/action-menu-icon.svg) 功能表中，您可以執行下列動作：

  * 移除組織中的使用者
  * 編輯組織角色
  * 編輯空間角色

## 將使用者新增至組織
{: #add_to_org}

如果使用者還不是您所管理之組織的成員，請將使用者指派給該組織。

1. 從功能表列按一下**管理** &gt; **存取 (IAM)**，然後選取**使用者**。
2. 從您要指派存取權的使用者列中，選取**動作** ![「動作清單」圖示](../icons/action-menu-icon.svg) 功能表，然後按一下**指派存取權**。
3. 選取**使用 Cloud Foundry 指派**。
4. 選取**指派組織**。
5. 指派使用者存取權：
   * 選擇要新增使用者的組織
   * 指派組織角色
   * 選擇地區
   * 選擇空間
   * 指派空間角色
7. 按一下**指派**。

## 檢閱已指派的存取權
{: #review_my_access}

如果您需要檢閱您在已加入之帳戶中的獲指派存取權，請完成下列步驟：

1. 從功能表列按一下**管理** &gt; **存取 (IAM)**，然後選取**使用者**。
2. 選取名稱。
3. 按一下 **Cloud Foundry 存取權**。
3. 展開組織列，並檢閱指派的角色。

如果您需要其他存取權，則必須與組織管理員或帳戶擁有者聯絡，以更新已指派的 Cloud Foundry 角色。
