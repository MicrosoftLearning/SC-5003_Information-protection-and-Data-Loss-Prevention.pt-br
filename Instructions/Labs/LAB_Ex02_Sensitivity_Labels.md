---
lab:
  task: Create and publish a sensitivity label
  exercise: Exercise 2 - Create and publish a sensitivity label
---

# Tarefas de habilidades

Sua tarefa é criar e publicar rótulos de confidencialidade em sua organização que classifiquem e protejam dados confidenciais de acordo com seu nível de confidencialidade e os controles de acesso necessários.

**Tarefas:**

1. Habilitar o suporte para rótulos de confidencialidade
1. Criar rótulos de confidencialidade
1. Publicar os rótulos de confidencialidade
1. Configurar a rotulagem automática

## Tarefa 1 - Habilitar o suporte para rótulos de confidencialidade no SharePoint e no OneDrive

Nesta tarefa, você habilitará a coautoria para rótulos de confidencialidade, o que também habilita rótulos de confidencialidade para arquivos no SharePoint e no OneDrive.

1. Abra o **Microsoft Edge** e nague até `https://purview.microsoft.com`.

1. Na navegação à esquerda, selecione **Configurações** > **Proteção de informações**.

1. Nas configurações** de **Proteção de Informações, verifique se você está na **guia Coautoria para arquivos com rótulos** de confidencialidade.

1. Selecione a caixa de seleção **Ativar coautoria para arquivos com rótulos de confidencialidade**.

1. Selecione **Aplicar** na parte inferior da tela.

Você habilitou com sucesso o suporte a rótulos de confidencialidade para arquivos no SharePoint e no OneDrive.

## Tarefa 2 – Criar rótulos de confidencialidade

Nesta tarefa, seu departamento de RH solicitou um rótulo de confidencialidade para aplicar aos documentos dos funcionários de RH. Você criará um rótulo de confidencialidade para documentos internos e um sub-rótulo para o departamento de RH.

1. Abra o **Microsoft Edge** e nague até **`https://purview.microsoft.com`**. Faça logon no Microsoft Purview como o usuário que você escolheu como **Administrador de conformidade**.

1. No portal do Microsoft Purview, selecione **Soluções** na barra lateral esquerda e clique em **Proteção de Informações**.

1. Na página **Proteção de informações da Microsoft**, na barra lateral esquerda, escolha **Rótulos de confidencialidade**.

1. Na página **Rótulos de confidencialidade**, clique em **+ Criar um rótulo**.

1. A nova configuração de **Rótulo de confidencialidade** será iniciada. Em **Fornecer detalhes básicos para esse rótulo**, insira:

    - **Nome**: `Internal`
    - **Nome de exibição**: `Internal`
    - **Descrição para usuários**: `Internal sensitivity label.`
    - **Descrição para administradores**: `Internal sensitivity label for Contoso.`

1. Selecione **Avançar**.

1. Na página **Definir o escopo deste rótulo**, selecione **Itens**, **Arquivos** e, em seguida, **Emails**. Se a caixa de seleção de **Reuniões** estiver marcada, desmarque-a.

   > [!NOTE]
   > Quando **Reuniões** estiver marcado, não será possível criar um sub-rótulo para o rótulo de confidencialidade.

1. Selecione **Avançar**.

1. Na página **Escolher configurações de proteção para os itens rotulados**, clique em **Avançar**.

1. Na página **Rotulagem automática para arquivos e emails**, clique em **Avançar**.

1. Na página **Definir configurações de proteção para grupos e sites**, clique em **Avançar**.

1. Na página **Rotulagem automática para ativos de dados esquematizados (versão prévia),** clique em **Avançar**.

1. Na página **Examinar suas configurações e concluir**, selecione **Criar rótulo**.

1. Na página **Seu rótulo de confidencialidade foi criado**, selecione **Não criar uma política ainda** e selecione **Concluído**.

1. Na página **Rótulos de confidencialidade**, localize o rótulo de confidencialidade **Interno** recém-criado. Clique nas reticências verticais (**...**) ao lado do rótulo e clique em **+ Criar sub-rótulo** no menu suspenso.

    ![Captura de tela mostrando o menu Ação para criar um sub-rótulo para um rótulo de confidencialidade.](../Media/create-sublabel-button.png)

1. O assistente **Novo rótulo de confidencialidade** será iniciado. Na página **Fornecer detalhes básicos para este rótulo**, insira:

   - **Nome**: `Employee data (HR)`
   - **Nome de exibição**: `Employee data (HR)`
   - **Descrição para usuários**: `This HR label is the default label for all specified documents in the HR Department.`
   - **Descrição para administradores**: `This label was created with input from the Head of HR. Contact the HR department for any changes to the label settings.`

1. Selecione **Avançar**.

1. Na página **Definir o escopo deste rótulo**, selecione **Itens**, depois **Arquivos**, **Emails** e, por fim, **Reuniões**.

1. Selecione **Avançar**.

1. Na página **Escolher configurações de proteção para itens rotulados**, escolha a opção **Controlar acesso** e clique em **Avançar**.

1. Na página **Controle de acesso**, clique em **Definir configurações de controle de acesso**.

1. Defina as configurações de criptografia com estas opções:

   - **Atribuir permissões agora ou permitir que os usuários decidam?,**: Atribuir permissões agora
   - **O acesso do usuário ao conteúdo expira**: Nunca
   - **Permitir acesso offline**: Apenas por um número de dias
   - **Os usuários têm acesso offline ao conteúdo por este número de dias**: 15
   - Clique no link **Atribuir permissões**. No painel do submenu **Atribuir permissões**, clique em **+ Adicionar qualquer usuário autenticado** e, em seguida, em **Salvar** para a aplicar esta configuração.

1. Na página **Controle de acesso**, clique em **Avançar**.

1. Na página **Rotulagem automática para arquivos e emails**, clique em **Avançar**.

1. Na página **Definir configurações de proteção para grupos e sites**, clique em **Avançar**.

1. Na página **Rotulagem automática para ativos de dados esquematizados (versão prévia),** clique em **Avançar**.

1. Na página **Examinar suas configurações e concluir**, selecione **Criar rótulo**.

1. Na página **Seu rótulo de confidencialidade foi criado**, selecione **Não criar uma política ainda** e selecione **Concluído**.

Você criou um rótulo de confidencialidade para as políticas internas de sua organização e um sub-rótulo de confidencialidade para o departamento de RH (recursos humanos).

## Tarefa 3 – Publicar rótulos de confidencialidade

Agora você publicará o rótulo de confidencialidade interno e de RH para que os rótulos de confidencialidade publicados fiquem disponíveis para os usuários de RH aplicarem aos documentos de RH.

1. No **Microsoft Edge**, a guia do portal do Microsoft Purview ainda deve estar aberta. Se não estiver, navegue até **`https://purview.microsoft.com`** > **Soluções** > **Proteção de Informações** > **Rótulos de confidencialidade**.

1. Na página **Rótulos de confidencialidade**, clique em **Publicar rótulos**.

1. A configuração de publicação dos rótulos de confidencialidade será iniciada.

1. Na página **Escolher rótulos de confidencialidade a serem publicados**, clique no link **Escolher rótulos de confidencialidade para publicar**.

1. No painel do submenu **Rótulos de confidencialidade a serem publicados**, marque as caixas de seleção **Interno** e **Interno/Dados do Funcionário (RH)** e cliquem em **Adicionar** na parte inferior do painel do submenu.

1. De volta à página **Escolher rótulos de confidencialidade a serem publicados**, clique em **Avançar**.

1. Na página **Atribuir unidades administrativas**, clique em **Avançar**

1. Na página **Publicar para usuários e grupos**, clique em **Avançar**.

1. Na página **Configurações de política**, clique em **Avançar**.

1. Na página **Configurações padrão para documentos**, clique em **Avançar**.

1. Na página **Configurações padrão para emails**, clique em **Avançar**.

1. Na página **Configurações padrão para reuniões e eventos do calendário**, clique em **Avançar**.

1. Na página **Configurações padrão para conteúdo do Fabric e do Power BI**, clique em **Avançar**.

1. Na página **Nomear política**, insira:

   - **Nome**: `Internal HR employee data`
   - **Insira uma descrição para sua política de rótulo de confidencialidade**: `This HR label is to be applied to internal HR employee data.`

1. Selecione **Avançar**.

1. Na página **Revisar e concluir**, clique em **Enviar**.

1. Na **Nova política criada**, clique em **Concluído** para concluir a publicação da política de rótulo.

Você publicou os rótulos de confidencialidade interno e de RH. Pode levar até 24 horas para que as alterações sejam replicadas para todos os usuários e serviços.

## Tarefa 4 – Criar uma política de rotulagem automática do lado do cliente

Nesta tarefa, você criará uma política de rotulagem automática do lado do cliente. Os rótulos automáticos do lado do cliente se aplicam automaticamente a arquivos e emails com base no conteúdo dos rótulos, garantindo que as informações confidenciais sejam classificadas e protegidas antes de saírem do dispositivo do usuário.

1. Você ainda deve estar na página **Rótulos de confidencialidade** no portal do Microsoft Purview. Se não estiver, navegue até **`https://purview.microsoft.com`** > **Soluções** > **Proteção de Informações** > **Rótulos de confidencialidade**.

1. Na página **Rótulos de confidencialidade**, localize o rótulo de confidencialidade **Interno** recém-criado. Clique nas reticências verticais (**...**) ao lado do rótulo e clique em **+ Criar sub-rótulo** no menu suspenso.

1. A nova configuração de **Rótulo de confidencialidade** será iniciada. Na página **Fornecer detalhes básicos para este rótulo**, insira:

   - **Nome**: `Confidential Research Data`
   - **Nome de exibição**: `Confidential Research Data`
   - **Descrição para usuários**: `This document or email contains sensitive research or development data that is proprietary to the organization.`
   - **Descrição para administradores**: `This label is auto-applied to documents and emails containing information related to research, prototypes, or internal projects.`

1. Selecione **Avançar**.

1. Na página **Definir o escopo deste rótulo**, selecione **Itens**, depois **Arquivos**, **Emails** e, por fim, **Reuniões**.

1. Selecione **Avançar**.

1. Na página **Escolher configurações de proteção para itens rotulados**, marque **Aplicar marcação de conteúdo** e clique em **Avançar**.

1. Selecione **Avançar**.

1. Na página **Marcação de conteúdo**, ative a opção Marcação de conteúdo.

1. Se a caixa de seleção **Adicionar um rodapé** estiver marcada, desmarque-a e marque a caixa de seleção **Adicionar uma marca d'água** e clique em **Personalizar texto**.

1. No painel do submenu **Personalizar texto da marca d'água**, insira `Confidential - R&D Data` como **Texto da marca d'água**. Aumente o **Tamanho da fonte** para `40` e clique em **Salvar** na parte inferior do painel.

1. De volta à página **Marcação de conteúdo**, se outras opções de marcação de conteúdo estiverem habilitadas, desabilite-as para garantir que **Adicionar uma marca d'água** seja a única opção habilitada.

1. Selecione **Avançar**.

1. Na página **Rotulagem automática de arquivos e emails**, habilite a **Rotulagem automática de arquivos e emails **.

1. Em **Detectar conteúdo que corresponda a essas condições** clique em **+ Adicionar condição** > **O conteúdo contém**.

1. Na seção **O conteúdo contém**, clique em **Adicionar** > **Classificadores treináveis**.

1. No painel do submenu **Classificadores treináveis**, adicione estes classificadores treináveis:

   - `Source code`
   - `Project documents`
   - `Software Product Development Files`

1. Clique em **Adicionar** na parte inferior do painel para adicionar esses classificadores treináveis.

1. De volta à página **Rotulagem automática para arquivos e emails**, clique em **Avançar**.

1. Na página **Definir configurações de proteção para grupos e sites**, clique em **Avançar**.

1. Na página **Rotulagem automática para ativos de dados esquematizados (versão prévia),** clique em **Avançar**.

1. Na página **Examinar suas configurações e concluir**, selecione **Criar rótulo**.

1. Na página **Seu rótulo de confidencialidade foi criado**, clique em **Publicar rótulo nos aplicativos dos usuários** e, em seguida, em **Concluído**.

1. No painel do submenu **Publicar rótulo**, clique em **Criar nova política de rótulo**.

1. Na página **Escolher rótulos de confidencialidade a serem publicados**, clique no link **Escolher rótulos de confidencialidade para publicar**.

1. Selecione o rótulo pai **Interno**e o rótulo **Dados de pesquisa confidenciais** que acabou de ser criado e clique em **Adicionar**.

1. De volta à página **Escolher rótulos de confidencialidade a serem publicados**, clique em **Avançar**.

1. Na página **Atribuir unidades administrativas**, clique em **Avançar**.

1. Na página **Publicar para usuários e grupos**, clique em **Avançar**.

1. Na página **Configurações de política**, marque a caixa de seleção **Os usuários devem fornecer uma justificativa para remover um rótulo ou diminuir sua classificação** e clique em **Avançar**.

1. Na página **Configurações padrão para documentos**, clique em **Avançar** até chegar à página **Nomear política**.

1. Na página **Nomear política**, insira:

   - **Nome**: `R&D Confidential Data Policy`
   - **Insira uma descrição para sua política de rótulo de confidencialidade**: `Automatically applies labels to source code, project documents, and development files to protect sensitive R&D data.`

1. Selecione **Avançar**.

1. Na página **Revisar e concluir**, clique em **Enviar**.

1. Na página **Nova política criada**, selecione **Concluído**.

Você criou uma política de rotulagem automática do lado do cliente que aplicará automaticamente o rótulo **Dados de pesquisa confidenciais** a arquivos e emails que contêm dados de pesquisa e desenvolvimento. Pode demorar até 24 horas para a política entrar totalmente em vigor.

## Tarefa 5 – Criar uma política de rotulagem automática do lado do serviço

Nesta tarefa, você criará uma política de rotulagem automática do lado do serviço. Os rótulos automáticos do lado do serviço são aplicados por serviços de nuvem como SharePoint, Exchange e OneDrive depois que o conteúdo é carregado ou recebido, garantindo que os dados confidenciais sejam protegidos mesmo que os usuários não os classifiquem manualmente.

1. Você ainda deve estar na página **Rótulos de confidencialidade** no portal do Microsoft Purview. Se não estiver, navegue até **`https://purview.microsoft.com`** > **Soluções** > **Proteção de Informações** > **Rótulos de confidencialidade**.

1. Expanda o rótulo **Interno** e selecione o sub-rótulo `Confidential Research Data` que você criou em uma tarefa anterior.

1. No painel do submenu **Dados de Pesquisa Confidenciais**, você verá as propriedades do rótulo automático criado em uma tarefa anterior. Neste painel, clique em **Criar política de rotulagem automática**.

    ![Captura de tela mostrando a opção de criar uma política de rotulagem automática.](../Media/create-auto-labeling-policy.png)

1. Na página **Nomear política**, insira:

   - **Nome**: `R&D Confidential Data Container Policy`
   - **Insira uma descrição para sua política de rótulo de confidencialidade**: `Automatically applies the Confidential Research Data label to content in SharePoint, Exchange, and OneDrive.`

1. Selecione **Avançar**.

1. Na página **Atribuir unidades administrativas**, clique em **Avançar**.

1. Na página **Escolher locais onde você quer aplicar o rótulo**, deixe **Email do Exchange**, **Sites do SharePoint** e **Contas do OneDrive** selecionados e clique em **Avançar**.

1. Na página **Configurar regras comuns ou avançadas**, deixe **Regras comuns** selecionado e clique em **Avançar**.

1. Na página **Definir regras para conteúdo em todos os locais**, edite a **regra Dados de Pesquisa Confidenciais**.

    ![Captura de tela de onde editar a regra para uma política de rotulagem automática do lado do serviço.](../Media/auto-apply-labels-edit-rule.png)

1. No painel do submenu **Nova regra**, em **Condições** > **O conteúdo contém**, clique na lista suspensa para **Adicionar** e, em seguida, clique em **Classificadores treináveis**.

1. No painel do submenu **Classificadores treináveis**, adicione estes classificadores treináveis:

   - `Source code`
   - `Project documents`
   - `Software Product Development Files`

   Isso garante uma proteção consistente entre os rótulos do lado do cliente e do lado do serviço.

1. Clique em **Adicionar** na parte inferior do painel para adicionar esses classificadores treináveis.

1. De volta à página **Definir regras para conteúdo em todos os locais**, clique em **Avançar**.

1. Em **Escolher um rótulo para aplicar automaticamente**, deixe os **Dados de pesquisa internos/confidenciais** escolhidos e clique em **Avançar**.

1. Na página **Decidir se você quer testar a política agora ou mais tarde**, clique em **Executar política no modo de simulação** e marque a caixa de seleção **Ativar automaticamente a política se não for modificada após 7 dias em simulação** e clique em **Avançar**.

1. Na página **Revisar e concluir**, clique em **Criar política**.

1. Na página **Sua política de rotulagem automática foi criada**, selecione **Concluído**.

Você criou uma política de rotulagem automática do lado do serviço que aplicará automaticamente o rótulo **Dados de pesquisa confidenciais** ao conteúdo armazenado ou compartilhado no SharePoint, Exchange e OneDrive. Pode demorar até 24 horas para a política entrar em vigor.
