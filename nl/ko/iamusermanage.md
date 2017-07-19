---

copyright:

  years: 2015, 2017

lastupdated: "2017-05-30"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# 사용자 및 액세스 관리
{: #iamusermanage}

관리할 권한이 부여된 액세스 옵션에 따라 계정 또는 조직 전체의 사용자를 보고 관리할 수 있습니다. 계정 소유자로서, 현재 계정에서 사용자에게 액세스 권한이 지정되었으며 직접 관리 중인 액세스 옵션에서 사용자를 관리할 수 있습니다.
{:shortdesc}

계정의 사용자를 관리하려면 다음 단계를 완료하십시오. 

1. 메뉴 표시줄에서 **관리** &gt; **계정** &gt; **사용자**를 클릭하십시오. 사용자 창은 현재 선택된 계정의 사용자 목록 및 해당 이메일 주소를 표시합니다.  
2. 사용자 이름을 선택하거나 **조치** 메뉴에서 **사용자 관리**를 클릭하십시오.  
3. 그리고 관리 가능한 액세스 권한에 따라, 서비스 정책 또는 Cloud Foundry 역할 섹션에서 사용자에 대한 액세스 권한을 업데이트하거나 인프라 액세스 지정 페이지에 액세스하기 위한 링크를 클릭하십시오. 

각 액세스 유형의 관리에 대한 추가 정보를 보려면 다음 절을 검토하십시오. 

추가된 계정에서 지정된 액세스 권한을 검토해야 하는 경우에는 다음 단계를 완료하십시오. 

1. 메뉴 표시줄에서 **관리** &gt; **보안** &gt; **ID 및 액세스** &gt; **사용자**를 클릭하십시오.  
2. 이름을 선택하십시오. 
3. 지정된 역할을 검토하십시오. 

추가 권한이 필요한 경우에는 조직 관리자 또는 계정 소유자에게 문의하여 Cloud Foundry 역할을 업데이트하거나, 서비스 또는 서비스 인스턴스의 관리자에게 문의하여 서비스 정책을 업데이트해야 합니다. 

계정, 조직 및 영역을 관리하는 데 사용되는 CLI 명령의 세부사항은 [계정, 조직 및 역할 관리를 위한 명령](https://console.stage1.bluemix.net/docs/cli/reference/bluemix_cli/bx_cli.html#bx_commands_acctorg)을 참조하십시오. 

## Cloud Foundry 액세스
{: #iammancfser}

계정 조직 및 영역에 대한 액세스 권한을 관리하려면 계정 소유자, 조직 관리자 또는 영역 관리자여야 합니다. 

1. 메뉴 표시줄에서 **관리** &gt; **보안** &gt; **ID 및 액세스** &gt; **사용자**를 클릭하십시오.  
2. 해당 역할을 편집할 사용자 이름을 선택하십시오. 
3. Cloud Foundry 섹션의 **조치** 메뉴에서 다음을 수행할 수 있습니다. 

  * 조직에서 사용자 제거
  * 조직 역할 편집
  * 영역 역할 편집

사용자가 아직 구성원이 아닌 조직의 관리자인 경우에는 **조직 지정**을 클릭하여 다른 조직에 사용자를 추가할 수도 있습니다.  


## ID 및 액세스 사용 서비스
{: #iammanidaccser}

서비스 정책을 관리하거나 사용자에 대해 새 서비스 정책을 지정하려면 특정 서비스 또는 서비스 인스턴스에 대한 지정 관리자 또는 계정 액세스 관리자여야 합니다. 

1. 메뉴 표시줄에서 **관리** &gt; **보안** &gt; **ID 및 액세스** &gt; **사용자**를 클릭하십시오.  
2. 서비스 정책이 지정될 사용자 이름을 선택하십시오. 
3. **서비스 정책 지정**을 선택하여 새 서비스 정책을 작성하거나, 서비스 정책 섹션의 **조치** 메뉴에서 다음을 수행할 수 있습니다. 
  
  * 정책 편집
  * 정책 제거

서비스 정책 및 역할에 대한 자세한 정보는 [ID 및 액세스 관리 정책 및 역할](/docs/iam/users_roles.html#iamusermanpol)을 참조하십시오. 

## 인프라 서비스

인프라 권한을 지정하거나 업데이트하려면 **인프라 액세스 지정** 링크를 클릭하십시오. 