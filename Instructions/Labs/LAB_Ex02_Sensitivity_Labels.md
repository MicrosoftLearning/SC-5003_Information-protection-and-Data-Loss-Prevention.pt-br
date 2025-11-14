---
lab:
  task: Create and publish a sensitivity label
  exercise: Exercise 2 - Create and publish a sensitivity label
---

# Tarefas de qualificação

Sua tarefa é criar e publicar rótulos de confidencialidade em sua organização que classifiquem e protejam dados confidenciais de acordo com seu nível de confidencialidade e os controles de acesso necessários.

**Tarefas:**

1. Habilitar o suporte para rótulos de confidencialidade  
1. Criar um grupo de rótulos  
1. Criar um rótulo filho  
1. Publicar rótulos  
1. Configurar a rotulagem automática  

## Tarefa 1 - Habilitar o suporte para rótulos de confidencialidade no SharePoint e no OneDrive

Nesta tarefa, você habilitará a coautoria para rótulos de confidencialidade, o que também habilita rótulos de confidencialidade para arquivos no SharePoint e no OneDrive.

1. Abra o **Microsoft Edge** e nague até `https://purview.microsoft.com`.

1. Na navegação à esquerda, selecione **Configurações** > **Proteção de informações**.

1. Nas configurações** de **Proteção de Informações, verifique se você está na **guia Coautoria para arquivos com rótulos** de confidencialidade.

1. Selecione a caixa de seleção **Ativar coautoria para arquivos com rótulos de confidencialidade**.

1. Selecione **Aplicar** na parte inferior da tela.

Você habilitou com sucesso o suporte a rótulos de confidencialidade para arquivos no SharePoint e no OneDrive.

<!--

## Task 2 – Create sensitivity labels

In this task, your HR department has requested a sensitivity label to apply to HR employee documents. You'll create a sensitivity label for internal documents and a sublabel for the HR department.

1. Open **Microsoft Edge** and navigate to **`https://purview.microsoft.com`**. Log into Microsoft Purview as the user you selected as the **Compliance Administrator**.

1. In the Microsoft Purview portal, select **Solutions** from the left sidebar, then select **Information Protection**.

1. On the **Microsoft Information Protection** page, on the left sidebar, select **Sensitivity labels**.

1. On the **Sensitivity labels** page select **+ Create a label**.

1. The **New sensitivity label** configuration will start. On the **Provide basic details for this label**, enter:

    - **Name**: `Internal`
    - **Display name**: `Internal`
    - **Description for users**: `Internal sensitivity label.`
    - **Description for admins**: `Internal sensitivity label for Contoso.`

1. Select **Next**.

1. On the **Define the scope for this label** page, select **Items**, then select **Files** and **Emails**. If the checkbox for **Meetings** is selected, make sure it's deselected.

   > [!NOTE]
   > When **Meetings** is selected, you can't create a sublabel for the sensitivity label.

1. Select **Next**.

1. On the **Choose protection settings for labeled items** page, select **Next**.

1. On the **Auto-labeling for files and emails** page, select **Next**.

1. On the **Define protection settings for groups and sites** page, select **Next**.

1. On the **Auto-labeling for schematized data assets (preview)** page, select **Next**.

1. On the **Review your settings and finish** page, select **Create label**.

1. On the **Your sensitivity label was created** page, select **Don't create a policy yet**, then select **Done**.

1. On the **Sensitivity labels** page, find the newly created **Internal** sensitivity label. Select the vertical ellipsis (**...**) next to it, then select **+ Create sublabel** from the dropdown menu.

    ![Screenshot showing the Action menu to create a sublabel for a sensitivity label.](../Media/create-sublabel-button.png)

1. The **New sensitivity label** wizard will start. On the **Provide basic details for this label** page enter:

   - **Name**: `Employee data (HR)`
   - **Display name**: `Employee data (HR)`
   - **Description for users**: `This HR label is the default label for all specified documents in the HR Department.`
   - **Description for admins**: `This label was created with input from the Head of HR. Contact the HR department for any changes to the label settings.`

1. Select **Next**.

1. On the **Define the scope for this label** page, select **Items**, then select **Files**, **Emails**, and **Meetings**.

1. Select **Next**.

1. On the **Choose protection settings for labeled items** page, select the **Control access** option, then select **Next**.

1. On the **Access control** page, select **Configure access control settings**.

1. Configure the encryption settings with these options:

   - **Assign permissions now or let users decide?**: Assign permissions now
   - **User access to content expires**: Never
   - **Allow offline access**: Only for a number of days
   - **Users have offline access to the content for this many days**: 15
   - Select the **Assign permissions** link. On the **Assign permissions** flyout panel, select the **+ Add any authenticated users**, then select **Save** to apply this setting.

1. On the **Access control** page, select **Next**.

1. On the **Auto-labeling for files and emails** page, select **Next**.

1. On the **Define protection settings for groups and sites** page, select **Next**.

1. On the **Auto-labeling for schematized data assets (preview)** page, select **Next**.

1. On the **Review your settings and finish** page, select **Create label**.

1. On the **Your sensitivity label was created** page, select **Don't create a policy yet**, then select **Done**.

You have successfully created a sensitivity label for your organizations internal policies and a sensitivity sublabel for the Human Resources (HR) department.

## Task 3 – Publish sensitivity labels

You will now publish the Internal and HR sensitivity label so that the published sensitivity labels will be available for the HR users to apply to their HR documents.

1. In **Microsoft Edge**, the Microsoft Purview portal tab should still be open. If not, navigate to **`https://purview.microsoft.com`** > **Solutions** > **Information Protection** > **Sensitivity labels**.

1. On the **Sensitivity labels** page select **Publish labels**.

1. The publish sensitivity labels configuration will start.

1. On the **Choose sensitivity labels to publish** page, select the **Choose sensitivity labels to publish** link.

1. On the **Sensitivity labels to publish** flyout panel, select the **Internal** and **Internal/Employee Data (HR)** checkboxes, then select **Add** at the bottom of the flyout panel.

1. Back on the **Choose sensitivity labels to publish** page, select **Next**.

1. On the **Assign admin units** page, select **Next**

1. On the **Publish to users and groups** page, select **Next**.

1. On the **Policy settings** page, select **Next**.

1. On the **Default settings for documents** page, select **Next**.

1. On the **Default settings for emails** page, select **Next**.

1. On the **Default settings for meetings and calendar events** page, select **Next**.

1. On the **Default settings for Fabric and Power BI content** page, select **Next**.

1. On the **Name your policy** page, enter:

   - **Name**: `Internal HR employee data`
   - **Enter a description for your sensitivity label policy**: `This HR label is to be applied to internal HR employee data.`

1. Select **Next**.

1. On the **Review and finish** page, select **Submit**.

1. On the **New policy created**, select **Done** to finish publishing your label policy.

You have successfully published the Internal and HR sensitivity labels. Note that it can take up to 24 hours for changes to replicate to all users and services.

## Task 4 – Create a client-side auto labeling policy

In this task, you'll create a client-side auto-labeling policy. Client-side auto-labels apply automatically to files and emails based on their content, ensuring that sensitive information is classified and protected before it leaves the user's device.

1. You should still be on the **Sensitivity labels** page in the Microsoft Purview portal. If not, navigate to **`https://purview.microsoft.com`** > **Solutions** > **Information Protection** > **Sensitivity labels**.

1. On the **Sensitivity labels** page, find the newly created **Internal** sensitivity label. Select the vertical ellipsis (**...**) next to it, then select **+ Create sublabel** from the dropdown menu.

1. The **New sensitivity label** configuration will start. On the **Provide basic details for this label** page, enter:

   - **Name**: `Confidential Research Data`
   - **Display name**: `Confidential Research Data`
   - **Description for users**: `This document or email contains sensitive research or development data that is proprietary to the organization.`
   - **Description for admins**: `This label is auto-applied to documents and emails containing information related to research, prototypes, or internal projects.`

1. Select **Next**.

1. On the **Define the scope for this label** page, select **Items**, then select **Files**, **Emails**, and **Meetings**.

1. Select **Next**.

1. On the **Choose protection settings for labeled items** page, select **Apply content marking**, then select **Next**.

1. Select **Next**.

1. On the **Content marking** page, select the toggle to enable content marking.

1. If the checkbox for **Add a footer** is selected, deselect it, and select the checkbox for **Add a watermark**, then select **Customize text**.

1. In the **Customize watermark text** flyout pane, enter `Confidential - R&D Data` as **Watermark text**. Increase the **Font size** to `40`, then select **Save** at the bottom of the panel.

1. Back on the **Content marking** page, if other content marking options are enabled, disable them to ensure **Add a watermark** is the only option enabled.

1. Select **Next**.

1. On the **Auto-labeling for files and emails** page, set the **Auto-labeling for files and emails** to enabled.

1. In the **Detect content that matches these conditions** section, select **+ Add condition** > **Content contains**.

1. In **Content contains** section select the **Add** > **Trainable classifiers**.

1. In the **Trainable classifiers** flyout panel, add these trainable classifiers:

   - `Source code`
   - `Project documents`
   - `Software Product Development Files`

1. Select **Add** at the bottom of the panel to add these trainable classifiers.

1. Back on the **Auto-labeling for files and emails** page, select **Next**.

1. On the **Define protection settings for groups and sites** page, select **Next**.

1. On the **Auto-labeling for schematized data assets (preview)** page, select **Next**.

1. On the **Review your settings and finish** page, select **Create label**.

1. On the **Your sensitivity label was created** page, select **Publish label to users' apps**, then select **Done**.

1. On the **Publish label** flyout panel, select **Create new label policy**.

1. On the **Choose sensitivity labels to publish** page, select the **Choose sensitivity labels to publish** link.

1. Select the parent **Internal** label and the **Confidential Research Data** label that was just created, then select **Add**.

1. Back on the **Choose sensitivity labels to publish** page, select **Next**.

1. On the **Assign admin units** page, select **Next**.

1. On the **Publish to users and groups** page, select **Next**.

1. On the **Policy settings** page, select the checkbox for **Users must provide a justification to remove a label or lower its classification**, then select **Next**.

1. On the **Default settings for documents** page, select **Next** until you reach the **Name your policy** page.

1. On the **Name your policy** page, enter:

   - **Name**: `R&D Confidential Data Policy`
   - **Enter a description for your sensitivity label policy**: `Automatically applies labels to source code, project documents, and development files to protect sensitive R&D data.`

1. Select **Next**.

1. On the **Review and finish** page, select **Submit**.

1. On the **New policy created** page, select **Done**.

You have successfully created a client-side auto-labeling policy that will automatically apply the **Confidential Research Data** label to files and emails containing research and development data. It might take up to 24 hours for the policy to take full effect.

## Task 5 – Create a service-side auto labeling policy

In this task, you'll create a service-side auto-labeling policy. Service-side auto-labels are applied by cloud services like SharePoint, Exchange, and OneDrive after content is uploaded or received, ensuring that sensitive data is protected even if users don't manually classify it.

1. You should still be on the **Sensitivity labels** page in the Microsoft Purview portal. If not, navigate to **`https://purview.microsoft.com`** > **Solutions** > **Information Protection** > **Sensitivity labels**.

1. Expand the **Internal** label, then select the `Confidential Research Data` sublabel you created in a previous task.

1. In the **Confidential Research Data** flyout panel, you'll see the properties for the auto-label you created in a previous task. In this panel, select **Create auto-labeling policy**.

    ![Screenshot showing the option to create an auto-labeling policy.](../Media/create-auto-labeling-policy.png)

1. On the **Name your policy** page, enter:

   - **Name**: `R&D Confidential Data Container Policy`
   - **Enter a description for your sensitivity label policy**: `Automatically applies the Confidential Research Data label to content in SharePoint, Exchange, and OneDrive.`

1. Select **Next**.

1. On the **Assign admin units** page, select **Next**.

1. On the **Choose locations where you want to apply the label** page, leave **Exchange email**, **SharePoint sites**, and **OneDrive accounts** selected, then select **Next**.

1. On the **Set up common or advanced rules** page, leave **Common rules** selected, then select **Next**.

1. On the **Define rules for content in all locations** page, edit the **Confidential Research Data rule**.

    ![Screenshot where to edit the rule for a service-side auto-labeling policy.](../Media/auto-apply-labels-edit-rule.png)

1. In the **New rule** flyout panel, under **Conditions** > **Content contains** select the dropdown for **Add**, then select **Trainable classifiers**.

1. In the **Trainable classifiers** flyout panel, add these trainable classifiers:

   - `Source code`
   - `Project documents`
   - `Software Product Development Files`

   This ensures consistent protection between client-side and service-side labels.

1. Select **Add** at the bottom of the panel to add these trainable classifiers.

1. Back on the **Define rules for content in all locations** page, select **Next**.

1. On the **Choose a label to auto-apply**, leave the **Internal/Confidential Research Data** chosen, then select **Next**.

1. On the **Decide if you want to test out the policy now or later** page, select **Run policy in simulation mode**, and select the checkbox for **Automatically turn on policy if not modified after 7 days in simulation**, then select **Next**.

1. On the **Review and finish** page, select **Create policy**.

1. On the **Your auto-labeling policy was created** page, select **Done**.

You have successfully created a service-side auto-labeling policy that will automatically apply the **Confidential Research Data** label to content stored or shared in SharePoint, Exchange, and OneDrive. It might take up to 24 hours for the policy to take effect.

-->
## Tarefa 2 – Criar um grupo de rótulos

Nesta tarefa, você criará um grupo de rótulos para organizar os rótulos de confidencialidade internos. Os grupos de rótulos funcionam como contêineres para rótulos relacionados, como classificações de departamento ou unidade de negócios.

1. Você ainda deve estar conectado ao portal do Microsoft Purview como Administrador de conformidade.

1. No **Microsoft Edge**, navegue até `https://purview.microsoft.com`.

1. No portal do Microsoft Purview, selecione **Soluções** na barra lateral esquerda e clique em **Proteção de Informações**.

1. Na página **Proteção de informações da Microsoft**, na barra lateral esquerda, escolha **Rótulos de confidencialidade**.

1. Na página **Rótulos de confidencialidade**, selecione **+ Criar** > **Grupo de rótulos**.

1. A configuração **Novo grupo de rótulos** será iniciada. Em **Fornecer detalhes básicos para este grupo de rótulos**, insira:

    - **Nome**: `Internal`
    - **Nome de exibição**: `Internal`
    - **Descrição para usuários**: `Internal sensitivity label.`
    - **Descrição para administradores**: `Internal sensitivity label group for Contoso.`

1. Selecione **Avançar**.

1. Na página **Revisar suas configurações e concluir**, selecione **Criar grupo de rótulos**.

1. Na página **Seu grupo de rótulos foi criado com êxito**, selecione **Não criar um rótulo agora** e, em seguida, selecione **Concluído**.

Você criou um grupo de rótulos para uso interno. Esse grupo ajuda você a gerenciar rótulos relacionados a departamentos específicos ou categorias de dados.

## Tarefa 3 – Criar um rótulo filho

Agora que você criou um grupo de rótulos, adicionará um rótulo filho para conteúdo relacionado a RH. Esse rótulo filho aplica criptografia e marcas de conteúdo para proteger os dados de RH contra acesso não autorizado.

1. Na página **Rótulos de confidencialidade**, localize o grupo de rótulos de confidencialidade **Interno**. Selecione a elipse vertical (**...**) ao lado dele e, no menu suspenso, selecione **+ Criar rótulo no grupo**.

    ![Captura de tela mostrando o menu Ação para criar um rótulo no grupo de um rótulo de confidencialidade.](../Media/create-label-in-group.png)

1. O assistente **Novo rótulo de confidencialidade** será iniciado. Na página **Fornecer detalhes básicos para este rótulo**, insira:

   - **Nome**: `Employee data (HR)`
   - **Nome de exibição**: `Employee data (HR)`
   - **Descrição para usuários**: `This HR label is the default label for all specified documents in the HR Department.`
   - **Descrição para administradores**: `This label is created in consultation with Ms. Jones (Head of the HR department). Contact her if you need to change the label settings.`

1. Selecione **Avançar**.

1. Na página **Definir o escopo para este rótulo**, selecione **Arquivos** e **E-mails**. Se a caixa de seleção de **Reuniões** estiver marcada, desmarque-a.

1. Selecione **Avançar**.

1. Na página **Escolher configurações de proteção para itens rotulados**, selecione as opções **Controlar acesso** e **Aplicar marcação de conteúdo** e, em seguida, selecione **Avançar**.

1. Na página **Controle de acesso**, clique em **Definir configurações de controle de acesso**.

1. Defina as configurações de criptografia com estas opções:

   - **Atribuir permissões agora ou permitir que os usuários decidam?,**: Atribuir permissões agora
   - **O acesso do usuário ao conteúdo expira**: Nunca
   - **Permitir acesso offline**: Apenas por um número de dias
   - **Os usuários têm acesso offline ao conteúdo por este número de dias**: 15
   - Clique no link **Atribuir permissões**. No painel do submenu **Atribuir permissões**, clique em **+ Adicionar qualquer usuário autenticado** e, em seguida, em **Salvar** para a aplicar esta configuração.

1. Na página **Controle de acesso**, clique em **Avançar**.

1. Na página **Marcação de conteúdo**, selecione a opção para habilitar **Marcação de conteúdo**.

1. Para cada um dos seguintes tipos de marcação, marque a caixa de seleção e selecione o ícone de edição para inserir o texto:

   |Tipo de marcação|Texto|
   |:---|:---|
   |Adicionar uma marca d’água|`INTERNAL USE ONLY`|
   |Adicionar um cabeçalho|`Internal Document`|
   |Adicionar um rodapé|`Contoso Confidential`|

1. Selecione **Avançar**.

1. Na página **Rotulagem automática para arquivos e emails**, clique em **Avançar**.

1. Na página **Definir configurações de proteção para grupos e sites**, clique em **Avançar**.

1. Na página **Examinar suas configurações e concluir**, selecione **Criar rótulo**.

1. Na página **Seu rótulo de confidencialidade foi criado**, selecione **Não criar uma política ainda** e selecione **Concluído**.

Você criou um rótulo filho dentro do grupo de rótulos Interno. O rótulo aplica criptografia e marcas de conteúdo aos documentos de RH, tornando os dados confidenciais fáceis de identificar e protegidos por política.

## Tarefa 4 – Publicar rótulos

Em seguida, você publicará o rótulo de RH do grupo de rótulos Interno para que os usuários do departamento de RH possam aplicá-lo aos seus documentos.

1. Você ainda deve estar conectado ao portal do Microsoft Purview como Administrador de conformidade.

1. No **Microsoft Edge**, a guia do portal do Microsoft Purview ainda deve estar aberta. Se não estiver, navegue até **`https://purview.microsoft.com`** > **Soluções** > **Proteção de Informações** > **Rótulos de confidencialidade**.

1. Na página **Rótulos de confidencialidade**, clique em **Publicar rótulos**.

1. A configuração de publicação dos rótulos de confidencialidade será iniciada.

1. Na página **Escolher rótulos de confidencialidade a serem publicados**, clique no link **Escolher rótulos de confidencialidade para publicar**.

1. No painel **Rótulos de confidencialidade a serem publicados**, selecione a caixa de seleção **Interno/Dados de funcionários (RH)** e, em seguida, selecione **Adicionar** na parte inferior da página do painel.

1. De volta à página **Escolher rótulos de confidencialidade a serem publicados**, clique em **Avançar**.

1. Na página **Atribuir unidades administrativas**, clique em **Avançar**

1. Na página **Publicar para usuários e grupos**, clique em **Avançar**.

1. Na página **Configurações de política**, clique em **Avançar**.

1. Em **Configurações padrão para documentos**, selecione **Avançar**.

1. Em **Configurações padrão para e-mails**, selecione **Avançar**.

1. Em **Configurações padrão para reuniões e eventos do calendário**, selecione **Avançar**.

1. Na página **Configurações padrão para conteúdo do Fabric e do Power BI**, clique em **Avançar**.

1. Na página **Nomear política**, insira:

   - **Nome**: `Internal HR employee data`

   - **Insira uma descrição para sua política de rótulo de confidencialidade**: `This HR label is to be applied to internal HR employee data.`

1. Selecione **Avançar**.

1. Na página **Revisar e concluir**, clique em **Enviar**.

1. Na página **Nova política criada**, selecione **Concluído** para concluir a publicação da sua política de rótulos.

Você publicou o grupo de rótulos Interno e seu rótulo de RH para que os usuários possam aplicá-los a documentos de RH. Pode levar até 24 horas para que a política seja propagada pelos serviços.

## Tarefa 5 – Configurar a rotulagem automática

Agora você criará um rótulo filho para dados financeiros e o configurará para ser aplicado automaticamente a conteúdo que contenha identificadores financeiros, como números de cartão de crédito ou de roteamento bancário.

1. Você ainda deve estar conectado ao portal do Microsoft Purview como Administrador de conformidade.

1. No **Microsoft Edge**, navegue até `https://purview.microsoft.com` e entre no portal do Microsoft Purview como Administrador de conformidade.

1. No portal do Microsoft Purview, selecione **Soluções** > **Proteção de informações** > **Rótulos de confidencialidade**.

1. Na página **Rótulos de confidencialidade**, localize o rótulo de confidencialidade **Interno**. Selecione a elipse vertical (**...**) e, no menu suspenso, selecione **+ Criar rótulo no grupo**.

1. Na página **Fornecer detalhes básicos para este rótulo**, insira:

   |Detalhes|Texto|
   |---|---|
   |**Nome**|`Financial Data`|
   |**Nome de exibição**|`Financial Data`|
   |**Descrição para usuários**|`This content contains financial data that must be labeled and protected.`|
   |**Descrição para administradores**|`This label is used for content that includes sensitive financial identifiers.`|

1. Selecione **Avançar**.

1. Na página **Definir o escopo para este rótulo**, selecione **Arquivos** e **E-mails**. Se a caixa de seleção de **Reuniões** estiver marcada, desmarque-a.

1. Selecione **Avançar**.

1. Na página **Escolher configurações de proteção para os itens rotulados**, clique em **Avançar**.

1. Na página **Rotulagem automática de arquivos e emails**, habilite a **Rotulagem automática de arquivos e emails **.

1. Em **Detectar conteúdo que corresponda a essas condições** clique em **+ Adicionar condição** > **O conteúdo contém**.

1. Na seção **O conteúdo contém**, selecione **Adicionar** > **Tipos de informações confidenciais**.

1. Na página do submenu **Tipos de informações confidenciais**, procure e selecione estes tipos de informações confidenciais:

   - `Credit Card Number`
   - `ABA Routing Number`
   - `SWIFT Code`

1. Selecione **Adicionar**.

1. De volta à página **Rotulagem automática para arquivos e emails**, clique em **Avançar**.

1. Na página **Definir configurações de proteção para grupos e sites**, clique em **Avançar**.

1. Na página **Examinar suas configurações e concluir**, selecione **Criar rótulo**.

1. Na página **Seu rótulo de confidencialidade foi criado**, selecione **Aplicar rótulo automaticamente ao conteúdo confidencial** e, em seguida, selecione **Concluído**.

1. Na página do submenu **Criar política de rotulagem automática**, selecione **Revisar política**.

1. Na página **Nomear sua política de rotulagem automática**, deixe o padrão e selecione **Avançar**.

1. Na página **Escolher um rótulo para aplicar automaticamente**, verifique se o rótulo _Dados internos/financeiros_ está selecionado e selecione **Próximo**.

1. Na página **Atribuir unidades administrativas**, clique em **Avançar**.

1. Na página **Escolha os locais onde deseja aplicar o rótulo**, selecione as opções para:

   - Email do Exchange
   - Sites do SharePoint
   - Contas do OneDrive

1. Selecione **Avançar**.

1. Na página **Configurar regras comuns ou avançadas**, deixe a opção padrão **Regras comuns** selecionada e selecione **Avançar**.

1. Na página **Definir regras para conteúdo em todos os locais**, expanda as regras para _Regra de dados financeiros_ para garantir que as regras esperadas estejam definidas e selecione **Avançar**.

1. Na página **Configurações adicionais para e-mail**, selecione **Avançar**.

1. Na página **Decida se deseja testar a política agora ou mais tarde**, selecione **Executar política no modo de simulação** e marque a caixa de seleção **Ativar automaticamente a política se não for modificada após 7 dias na simulação.**

1. Selecione **Avançar**.

1. Na página **Revisar e concluir**, clique em **Criar política**.

1. Na página **Sua política de rotulagem automática foi criada**, selecione **Concluído**.

Você organizou os rótulos em um grupo, publicou-os para os usuários e habilitou a rotulagem automática para que o conteúdo confidencial seja protegido sem depender dos usuários.
