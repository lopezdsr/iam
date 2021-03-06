---

copyright:

  years: 2018, 2019
lastupdated: "2019-03-05"

keywords: MFA, multifactor authentication, IBMid MFA, two-factor authentication, account MFA, time-based one-time passcode, TOTP

subcollection: iam

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}

# 針對帳戶中的使用者要求 MFA
{: #enablemfa}

身為 {{site.data.keyword.Bluemix}} 帳戶擁有者或計費服務的管理者，您可以選擇帳戶中的每位使用者都需要多因子鑑別 (MFA)，或是只有不使用 SSO 的非聯合 ID 使用者需要。所有具有 IBM ID 的使用者都會使用時間型一次性密碼 (TOTP) MFA 方法，而且必須啟用具有不同 ID 類型的所有使用者，才能分別使用 TOTP、安全問題或外部鑑別方法。  
{:shortdesc}

## 開始之前
{: #considerations}

請先檢閱下列考量，再啟用帳戶的 IBM ID MFA，確保知道其對您帳戶中所有使用者的影響：

* 當您啟用帳戶的 MFA 時，使用者必須在下次登入時完成 MFA 處理程序。
* 啟用 MFA 之後，使用者的 API 金鑰及服務 ID 將會繼續運作。
* 如果您需要使用 CLI 或使用者介面登入 Cloud Foundry，則在帳戶啟用 MFA 之後，您必須使用 API 金鑰或單一登入 (SSO)。
* 您帳戶的 MFA 適用於使用者的登入，但不適用於 API 呼叫。如果使用者有權對您帳戶中的資源提出 API 呼叫，則使用者不需完成 MFA 即可執行此動作。如果使用者屬於其他帳戶，則使用者可以使用不需要 MFA 之帳戶的 API 金鑰，對您帳戶中的資源提出 API 呼叫。
* 如果您的帳戶需要 MFA，而且您的帳戶中有沒有 IBM ID 的使用者，則必須在 {{site.data.keyword.Bluemix_notm}} 主控台的「使用者詳細資料」頁面中，針對該使用者啟用其中一個其他 MFA 選項。如需相關資訊，請參閱[多因子鑑別的類型](/docs/iam?topic=iam-types#types)。
* 為您帳戶中的使用者規劃通訊與支援策略：
  * 選擇您計劃啟用 MFA 的日期和時間，以期對企業造成最小的影響。
  * 啟用 MFA 之後，通知您的帳戶使用者如何[設定](/docs/iam?topic=iam-enablemfa#setupapp)的資訊。

啟用多因子鑑別帳戶設定時，會在登入時提示您帳戶中的所有 IBM ID 使用者進行 IBM ID MFA 鑑別。如果您已設定您帳戶中任何 IBM ID 使用者的其他 MFA 方法，則不再提示他們輸入這些 MFA 方法。
{: tip}

## 啟用帳戶中所有使用者的 MFA
{: #enabling}

若要啟用 MFA，您必須是帳戶擁有者或計費帳戶管理服務的管理者。啟用 MFA 並不會影響已登入的使用者，因為對帳戶強制執行 MFA 只會對新的登入生效。請確定您通知帳戶使用者已啟用 MFA，並說明使用者下次登入時對他們的影響。

1. 從功能表列按一下**管理** &gt; **存取 (IAM)**，然後選取**設定**。
2. 針對「帳戶登入設定」選取**更新**。
3. 根據您想要的鑑別類型，選取**無**、**僅限非聯合使用者**或**所有使用者**。
4. 如果您選取「僅限非聯合使用者」選項，請選取勾選框來確認您瞭解取得帳戶中使用者之 MFA 的影響。
5. 按一下**儲存**。

## 設定 TOTP
{: #setupapp}

在您啟用帳戶的 MFA 之後，必須在下次登入時，使用鑑別器應用程式來設定一次性密碼。帳戶中的所有使用者也必須在下次登入時設定一次性密碼。

請完成下列步驟，以便第一次使用鑑別器應用程式來設定一次性密碼：

1. 使用您的 IBM ID 及密碼登入。

  可能需要最多 5 分鐘，您才能夠使用 MFA 重新登入。
  {: note}

2. 在**需要驗證**畫面上選取**驗證**，以使用鑑別器應用程式設定 MFA。
3. 選取**設定您的鑑別器應用程式**，讓一次性驗證碼傳送至您的電子郵件，以繼續設定鑑別器應用程式。
4. 選取**驗證**。
5. 使用您的應用程式掃描條碼，或按一下**無法掃描條碼？**輸入提供的金鑰。
6. 按一下**繼續**來輸入您的驗證碼。
7. 輸入驗證碼並選取**驗證**。

如果您遇到錯誤訊息，指出您已設定鑑別，但驗證碼無法運作，或是您沒有驗證碼可供輸入，則必須與[服務台](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示") 聯絡，以重設您的 MFA 登記。
{: note}
{: #mfahelp}

## 停用帳戶中所有使用者的必要 MFA
{: #disablemfa}

若要停用 MFA，您必須是帳戶擁有者或帳戶管理計費服務的管理者。停用 MFA 並不會影響已登入的使用者。此動作會在所有新登入時生效。

1. 從功能表列按一下**管理** &gt; **存取 (IAM)**，然後選取**設定**。
2. 針對「帳戶登入設定」選取**編輯**。
3. 選取**無**。
4. 按一下**儲存**。

