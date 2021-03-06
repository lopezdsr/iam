---

copyright:
  years: 2015, 2019
lastupdated: "2019-04-01"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:note:.deprecated}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Resolução de problemas do IAM
{: #troubleshoot_iam}

Os problemas gerais com o uso do IAM podem incluir a necessidade de acesso a um recurso ou a uma conta para executar uma tarefa ou a identificação do tipo correto de acesso para designar aos usuários em sua conta a fim de que eles executem tarefas específicas. Em muitos casos, é possível recuperar-se desses problemas seguindo algumas etapas simples.
{:shortdesc}

## Como eu sei qual acesso está designado a mim?
{: #troubleshoot-myaccess}
{: troubleshoot}

Se você não tiver acesso para concluir uma tarefa específica, como criar uma instância de serviço e incluí-la em um grupo de recursos ou convidar outros usuários para a conta, talvez seja necessário verificar qual acesso está designado a você.

Eu não tenho certeza qual nível de acesso está designado a mim para que eu conclua ações em uma conta da qual sou um membro.
{: tsSymptoms}
   
É possível que o acesso correto não esteja designado a você.
{: tsCauses}

Para verificar a que tarefas você tem acesso e o nível de acesso, conclua as etapas a seguir. Se você precisar solicitar acesso, entre em contato com o proprietário da conta.

Acesse **Gerenciar** &gt; **Acesso (IAM)** e selecione seu nome na página **Usuários**. Em seguida, dependendo do acesso que você estiver procurando, selecione as guias diferentes:
{: tsResolve}

* Para determinar o acesso que você tem nos grupos de acesso aos quais está designado, selecione **Grupos de acesso**.
* Para ver as políticas de acesso do IAM que estão designadas a você, selecione as **Políticas de acesso**.
* Para ver o seu acesso ao Cloud Foundry para todas as organizações e os espaços, selecione **Acesso ao Cloud Foundry**.


## Como posso obter acesso para convidar usuários para a conta? 
{: #troubleshoot-invite}
{: troubleshoot}

Se você não for o proprietário da conta e o acesso correto não estiver designado a você, você não poderá convidar usuários para uma conta. 

Não posso convidar usuários para a conta.
{: tsSymptoms}
   
É possível que o acesso correto não esteja designado a você.
{: tsCauses}

Para convidar usuários e gerenciar convites pendentes, deve-se ser um proprietário da conta, um gerenciador de organização, um usuário com uma política de acesso do IAM com a função Editor ou superior no serviço de gerenciamento de conta do gerenciamento de usuário ou deve-se ter permissões de infraestrutura clássica para incluir usuários.
{: tsResolve}


## Como posso visualizar permissões de infraestrutura clássica para outros usuários?
{: #troubleshoot-classicinfra}
{: troubleshoot}

Os proprietários da conta têm acesso total à conta, portanto, eles não veem as permissões para si mesmos. Os usuários individuais não podem editar suas próprias permissões, portanto, eles veem permissões em sua página de infraestrutura clássica, mas não podem editá-las. Deve-se ter acesso específico para visualizar e editar permissões para outro usuário na conta.

Você vê uma mensagem que informa que não é possível visualizar as permissões de infraestrutura clássica de outro usuário.
{: tsSymptoms}
   
É possível que o acesso correto não esteja designado a você.
{: tsCauses}

Deve-se solicitar que o proprietário da conta designe a permissão de infraestrutura clássica **Gerenciar usuários** a você, mas deve-se também ser um antecessor do usuário dentro da hierarquia do usuário da infraestrutura clássica para visualizar e gerenciar as permissões de outro usuário.
{: tsResolve}
