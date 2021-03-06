---

copyright:

  years: 2017, 2019

lastupdated: "2019-02-21"

keywords: authorizations, service to service access, access between services

subcollection: iam

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}


# 서비스 간 액세스 부여
{: #serviceauth}

{{site.data.keyword.Bluemix_notm}} Identity and Access Management(IAM) 시스템의 많은 기능이 {{site.data.keyword.Bluemix_notm}} 리소스에 대한 사용자와 해당 애플리케이션의 액세스를 관리하고 적용하는 데 초점이 맞춰져 있습니다. 하지만 한 서비스의 사용자 리소스에 대한 액세스를 다른 서비스에 제공해야 하는 다른 시나리오가 있을 수 있습니다. 계정의 모든 사용자는 권한을 작성할 수 있지만 관리자 역할의 사용자만 권한을 삭제할 수 있습니다. **권한** 페이지에서 사용자 계정 내의 권한을 설정하고 볼 수 있습니다.
{:shortdesc}

## 권한 작성
{: #create-auth}

대상 서비스의 사용자로서 보유하고 있는 액세스 레벨만 부여할 수 있습니다. 예를 들어, 액세스할 서비스에 대해 뷰어 액세스 권한만 있는 경우 권한에 뷰어 역할만 지정할 수 있습니다.

1. 메뉴 표시줄에서 **관리** &gt; **액세스(IAM)**를 클릭하고 **권한**을 선택하십시오.
2. **작성**을 클릭하십시오.
3. 권한의 소스 및 대상 서비스를 선택하십시오. 소스 서비스에는 선택한 대상 서비스에 대한 액세스가 지정됩니다.
4. 대상 서비스에 액세스하는 소스 서비스에 액세스를 지정할 역할을 선택하십시오.
5. **권한 부여**를 클릭하십시오.

이 유형의 액세스를 부여할 수 있도록 하는 서비스만 옵션으로 사용 가능합니다.
{: note}

## 권한 제거
{: #remove-auth}

1. 메뉴 표시줄에서 **관리** &gt; **액세스(IAM)**를 클릭하고 **권한**을 선택하십시오.
2. 계정에서 제거하려는 권한에 대한 행을 식별하십시오.
3. **조치** ![조치 목록 아이콘](../icons/action-menu-icon.svg) 메뉴에서 **제거**를 선택하십시오.
5. **제거**를 선택하십시오.
