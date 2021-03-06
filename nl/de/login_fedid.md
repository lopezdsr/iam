---

copyright:

  years: 2015，2019

lastupdated: "2019-01-28"

keywords: federated ID, enterprise SSO, single sign-on ID, API key login, one-time passcode login

subcollection: iam

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Mit föderierter ID anmelden
{: #federated_id}

Als föderierter Benutzer, der eine unternehmensweite oder Unternehmens-Single Sign-on-ID verwendet, können Sie sich bei {{site.data.keyword.Bluemix}} über die Befehlszeilenschnittstelle (CLI) anmelden, indem Sie entweder einen einmaligen Kenncode oder einen API-Schlüssel verwenden.
{: shortdesc}

## Einmaligen Kenncode verwenden
{: #onetime_passcode}

Wenn Sie die Option für den einmaligen Kenncode verwenden, um sich mit einer föderierten ID anzumelden, geben Sie den Single-Sign-on-Parameter (SSO) an, um einen einmaligen Kenncode anzufordern, den Sie dann bei der Anmeldung eingeben.

Ein einmaliger Kenncode ruft Code über die {{site.data.keyword.Bluemix_notm}}-Konsole ab. Dies hat zur Folge, dass die Verwendung einer föderierten ID in Ihrem Automationsscript fehlschlägt. Sie können dieses Problem vermeiden, indem Sie die API-Schlüssel-Option mit einem automatisierten Script verwenden.
{: tip}

### Über die {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle
{: #login_cli}
1. Geben Sie die Option `--sso` mit dem Befehl `ibmcloud login` an.
2. Folgen Sie der URL in der Eingabeaufforderung, um den einmaligen Kenncode abzurufen.
3. Verwenden den Kenncodewert in der Befehlszeilenschnittstelle per Cut-and-paste als Ihre Eingabe.

  ```
  ibmcloud login --sso
  API-Endpunkt: https://cloud.ibm.com

  Zum Fortfahren einen einmaligen Code über https://identity-2.us-south.iam.cloud.ibm.com/identity/passcode anfordern.
  URL im Standardbrowser öffnen? [J/N]>
  Einmaliger Code >
  Authentifizieren...
  OK

  ```

### Über die Cloud Foundry-Befehlszeilenschnittstelle
{: #login_cf_cli}

1. Geben sie die Option `--sso` mit dem Befehl `cf login` an.
2. Folgen Sie der URL in der Eingabeaufforderung, um den einmaligen Kenncode abzurufen.
3. Verwenden den Kenncodewert in der Befehlszeilenschnittstelle per Cut-and-paste als Ihre Eingabe.

  ```
  cf login -a  https://api.us-south.cf.cloud.ibm.com --sso

  API-Endpunkt: https://api.us-south.cf.cloud.ibm.com

  Einmaliger Code (Abruf unter https://login.us-south.cf.cloud.ibm.com/UAALoginServerWAR/passcode)>
  Authentifizieren...
  OK

  ```

## API-Schlüssel verwenden
{: #api_key}

Der erforderliche API-Schlüssel ist der {{site.data.keyword.Bluemix_notm}}-API-Schlüssel, der für die Authentifizierung bei der {{site.data.keyword.Bluemix_notm}}-Plattform verwendet wird, und nicht der API-Schlüssel für die klassische Infrastruktur oder der {{site.data.keyword.Bluemix_notm}}-Service-API-Schlüssel.

1. Erstellen Sie einen API-Schlüssel mit dem [Befehl `ibmcloud iam api-key-create`](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_iam_api_key_create#ibmcloud_iam_api_key_create). Verwenden Sie die Option `-f`, um eine API-Schlüsseldatei zu erstellen, anstatt den Schlüssel im Befehlsfenster anzuzeigen:

   ```
   ibmcloud iam api-key-create NAME [-d BESCHREIBUNG] [-f, --file DATEI]

   ```

2. Melden Sie sich mit dem API-Schlüssel an.

  Sie können den API-Schlüssel mit der {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle auf folgende Art und Weise verwenden:

    * API-Schlüssel direkt aufrufen

      ```
      ibmcloud login --apikey <api-schlüsselzeichenfolge>

      ```

    * API-Schlüssel mit der Schlüsseldatei aufrufen:

      ```
      ibmcloud login --apikey @schlüsseldateiname

      ```

    * Legen Sie eine Umgebungsvariable fest. Darüber hinaus können Sie auf Ihrem System auch eine Umgebungsvariable definieren. Beispiel: 'IBMCLOUD_API_KEY=api-schlüsselzeichenfolge', wobei `api-schlüsselzeichenfolge` der angepasste Wert des API-Schlüssels ist. Nachdem die Umgebungsvariable definiert worden ist, können Sie einfach `ibmcloud login` in der Befehlszeilenschnittstelle angeben.

  Um sich über die Cloud Foundry-Befehlszeilenschnittstelle anzumelden, geben Sie `apikey` als Benutzernamen und die API-Schlüsselzeichenfolge als Kennwort an:

    ```
    cf login -a https://api.us-south.cf.cloud.ibm.com

    API-Endpunkt: https://api.us-south.cf.cloud.ibm.com

    Email> apikey

    Password>
    Authenticating...
    OK

    ```
