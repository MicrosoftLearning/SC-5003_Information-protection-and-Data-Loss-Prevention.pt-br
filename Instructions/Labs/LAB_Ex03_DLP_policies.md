---
lab:
  task: Create a data loss prevention (DLP) policy
  exercise: Exercise 3 - Create a data loss prevention (DLP) policy
---

# Tarefas de qualificação

**Tarefas:**

1. Criar uma política DLP no modo de simulação
1. Modificar uma política DLP
1. Criar uma política DLP no PowerShell
1. Ativar uma política no modo de simulação

## Tarefa 1 – Criar uma política DLP no modo de simulação

Neste exercício, você criará uma política DLP (de prevenção contra perda de dados) para proteger dados confidenciais de serem compartilhados pelos usuários. A política DLP que você criar informará aos usuários se eles desejam compartilhar conteúdo que contenha informações de cartão de crédito e permitirá que eles forneçam uma justificativa para o envio dessas informações. A política será implementada no modo de simulação porque você não quer que a ação de bloqueio afete seus usuários ainda.

1. No **Microsoft Edge**, navegue até **`https://purview.microsoft.com`** e faça logon no portal do Microsoft Purview como o usuário escolhido para ter direitos de **Administrador de conformidade**.

1. Escolha **Soluções** na barra lateral à esquerda e, em seguida, **Prevenção contra perda de dados**.

1. Escolha **Políticas** na barra lateral à esquerda.

1. Na página **Políticas**, escolha **+ Criar política** para iniciar a configuração para criar uma nova política de prevenção contra perda de dados.

1. Na página **Iniciar com um modelo ou criar uma política personalizada**, escolha **Personalizada** como a categoria e, em seguida, **Política personalizada** em **Regulamentos**.

1. Selecione **Avançar**.

1. Na página **Nomear a sua política de DLP**, insira:

   - **Nome**: `Credit Card DLP Policy`
   - **Descrição**: `Protect credit card numbers from being shared`

1. Selecione **Avançar**.

1. Na página **Atribuir unidades de administração**, clique em **Avançar**.

1. Na página **Escolher locais para aplicar a política**, habilite o local somente para **Mensagens de chat e canal do Teams**. Se outros locais estiverem selecionados, desmarque-os.

1. Selecione **Avançar**.

1. Na página **Definir configurações de política**, selecione **Criar ou personalizar regras avançadas de DLP** e selecione **Avançar**.

1. Na página **Personalizar regras avançadas de DLP**, escolha **+ Criar regra**.

1. Na página do submenu **Criar regra**, insira `Credit card information` como nome no campo **Nome**.

1. Em **Condições**, escolha **+ Adicionar condição** e **O conteúdo contém**.

1. Na nova área **O conteúdo contém**, clique em **Adicionar** e escolha **Tipos de informações confidenciais**.

1. Na página **Tipos de informações confidenciais**, escolha **Número do cartão de crédito** e, em seguida, clique em **Adicionar**.

1. Clique em **+ Adicionar condição** e, em seguida, **O conteúdo é compartilhado do Microsoft 365**.

1. Na nova seção **O conteúdo é compartilhado do Microsoft 365**, escolha a opção **somente com pessoas dentro da minha organização**.

1. Em **Ações**, clique em **+ Adicionar uma ação** e, em seguida, em **Restringir acesso ou criptografar o conteúdo em locais do Microsoft 365**.

1. Na nova área **Restringir acesso ou criptografar o conteúdo em locais do Microsoft 365**, clique em **Bloquear todo mundo**.

1. Em **Notificações do usuário**, **Ative** a opção **Usar notificações para informar seus usuários e ajudar a educá-los sobre o uso adequado de informações confidenciais** e, em seguida, marque a caixa de seleção para **Notificar usuários no serviço do Office 365 com uma dica de política**.

1. Em **Substituições do usuário**, marque a caixa de seleção **Permitir que os usuários substituam as restrições de política do Fabric (incluindo Power BI), Exchange, SharePoint, OneDrive e Teams.**

1. Marque a caixa de seleção para **Exigir que uma justificativa comercial seja substituída**.

1. Em **Relatórios de incidentes**, na lista suspensa **Usar este nível de severidade em alertas e relatórios de administrador**, escolha **Baixo**.

1. Na parte inferior do painel de submenu **Criar regra**, clique em **Salvar**.

1. De volta à página **Personalizar regras avançadas de DLP**, clique em **Avançar**.

1. Na página **Modo de política**, escolha **Executar a política no modo de simulação** e marque a caixa de seleção **Mostrar dicas de política no modo de simulação**.

1. Selecione **Avançar**.

1. Na página **Revisar e concluir**, revise as configurações e clique em **Enviar**.

1. Na página **Nova política criada**, selecione **Concluído**.

Agora você criou uma política DLP que verifica números de cartão de crédito em chats e canais do Microsoft Teams, permitindo que os usuários forneçam uma justificativa comercial para substituir a política.

## Tarefa 2 – Modificar uma política de DLP

Nesta tarefa, você modificará a política DLP existente criada na tarefa anterior para também verificar emails em busca de informações de cartão de crédito. Essa modificação garante que os dados confidenciais sejam protegidos em mais canais de comunicação.

1. Você ainda deve estar conectado ao Microsoft 365 como o usuário escolhido para ser seu **Administrador de conformidade**.

1. Você ainda deve estar na página **Políticas** do Microsoft Purview. Se não estiver, abra o **Microsoft Edge** e navegue até `https://purview.microsoft.com`. Clique em **Soluções** > **Prevenção contra perda de dados** > **Políticas**.

1. Na página **Políticas**, marque a caixa de seleção da **Política DLP de Cartão de Crédito** criada recentemente e clique em **Editar política** para abrir a configuração da política.

1. Na página **Nomear política DLP**, clique em **Avançar**.

1. Na página **Atribuir unidades de administração**, clique em **Avançar**.

1. Na página **Escolher locais para aplicar a política**, marque a caixa de seleção **Email do Exchange** para adicionar esse local à sua política DLP.

1. Clique em **Avançar** até chegar à página **Revisar e concluir**.

1. Clique em **Enviar** na página **Revisar e concluir** para aplicar a alteração feita na política.

1. Depois que a política for atualizada, clique em **Concluído** na página **Política atualizada**.

Você modificou a política DLP para incluir a verificação de email, aumentando a proteção de informações confidenciais.

## Tarefa 3 – Criar uma política DLP no PowerShell

Nesta tarefa, você usará o PowerShell para criar uma política DLP para proteger as IDs de funcionários da Contoso e impedir que elas sejam compartilhadas por meio do Exchange. Essa política notificará os usuários que tentarem compartilhar esses dados confidenciais e bloqueará o e-mail se ele contiver IDs de funcionário.

1. Na área de trabalho, abra uma janela do PowerShell com privilégios elevados clicando com o botão direito do mouse no botão Windows na barra de tarefas e escolha **Terminal (Admin)**.

1. Execute o cmdlet **Install Module** para instalar a versão mais recente do módulo do **PowerShell do Exchange Online**:

    ```powershell
    Install-Module ExchangeOnlineManagement
    ```

1. Confirme a caixa de diálogo Segurança do repositório não confiável com **S** para Sim e pressione **Enter**.  Esse processo pode levar algum tempo para ser concluído.

1. Execute o cmdlet **Connect-IPPSSession** para se conectar ao PowerShell de Segurança e Conformidade:

   ```powershell
   Connect-IPPSSession
   ```

1. Entre como o usuário que você escolheu como **Administrador de conformidade** na janela pop-up **Entrar na conta**.

1. Execute o **cmdlet New-DlpCompliancePolicy** para criar uma política DLP que verifica todas as caixas de correio do Exchange:

   ```powershell
   New-DlpCompliancePolicy -Name "EmployeeID DLP Policy" -Comment "This policy blocks sharing of Employee IDs" -ExchangeLocation All
   ```

1. Execute o cmdlet **New-DlpComplianceRule** para adicionar uma regra DLP à política DLP criada na etapa anterior:

   ```powershell
   New-DlpComplianceRule -Name "EmployeeID DLP rule" -Policy "EmployeeID DLP Policy" -BlockAccess $true -ContentContainsSensitiveInformation @{Name="Contoso Employee IDs"}
   ```

1. Execute o cmdlet **Get-DLPComplianceRule** para examinar a **Regra DLP EmployeeID**:

   ```powershell
   Get-DLPComplianceRule -Identity "EmployeeID DLP rule"
   ```

Você criou uma política DLP usando o PowerShell que verifica se há IDs de funcionários da Contoso no Exchange.

## Tarefa 4 – Ativar uma política no modo de simulação

Nesta tarefa, você ativará a **Política DLP de Cartão de Crédito** criada no modo de simulação para que ela imponha suas ações de proteção.

1. Você ainda precisa estar conectado ao Microsoft 365 como o usuário escolhido como **Administrador de conformidade**.

1. No **Microsoft Edge**, navegue até as políticas DLP acessando `https://purview.microsoft.com` > **Soluções** > **Prevenção contra perda de dados** e clique em **Políticas** na barra lateral à esquerda.

1. Na página **Políticas**, marque a caixa de seleção da **Política DLP de Cartão de Crédito** e clique em **Editar política** para abrir a configuração da política.

1. Clique em **Avançar** até chegar à página **Modo de política** e clique em **Ativar a política imediatamente**.

1. Na página **Revisar e concluir**, clique em **Enviar**.

1. Na página **Política atualizada**, selecione **Concluído**.

Você ativou a política DLP, garantindo que todas as tentativas de compartilhar informações de cartão de crédito sejam bloqueadas e exijam uma justificativa comercial.
