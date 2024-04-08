---
lab:
  task: Create a data loss prevention (DLP) policy
  exercise: Exercise 4 - Create a data loss prevention (DLP) policy
---

# Tarefas de qualificação

Sua tarefa é desenvolver e impor uma política personalizada de DLP (prevenção contra perda de dados) adaptada para proteger os dados confidenciais do cliente da sua organização, ao mesmo tempo em que garante a conformidade com as regulamentações de proteção de dados.

- **Crie uma política de DLP personalizada** no modo de teste para monitorar dados sem imposição.
- **Defina uma regra de DLP avançada** direcionada a informações confidenciais específicas.
- **Ative a política de DLP** para impor proteções e conformidade ativamente.

**Objetivo**: Desenvolva e implemente uma política personalizada de DLP (prevenção contra perda de dados) para proteger dados confidenciais do cliente e garantir a conformidade regulatória. Você começará criando uma política de DLP no modo de teste para monitoramento inicial, passará a criar uma regra avançada visando tipos específicos de informações confidenciais e, por fim, ativará a política para impor a proteção de dados em email, SharePoint, OneDrive e comunicações do Teams.

## Tarefa 1 – Criar uma política personalizada de DLP (prevenção contra perda de dados)

1. Navegue até o portal de conformidade do Microsoft Purview.
1. Expanda **Prevenção contra perda de dados** e selecione **Políticas**.
1. Na página **Políticas**, selecione **+ Criar política**.
1. No assistente de política DLP, em **Começar com um modelo ou criar uma política personalizada**, selecione:
   - Categorias: **Personalizada**
   - Regulamentos: **Política personalizada**
1. Selecione **Avançar**.
1. Na página **Nomear a sua política de DLP**, insira:
   - **Nome**: `Customer interaction protection policy`
   - **Descrição**: `This DLP policy protects customer data integrity and confidentiality in the Customer Service department by preventing unauthorized access and disclosure.`
1. Selecione **Avançar** até chegar à página **Escolher onde aplicar a política**.
1. Na página **Escolher onde aplicar a política**, selecione apenas:
   - **Email do Exchange**
   - **Sites do SharePoint**
   - **Contas do OneDrive**
   - **Chat do Teams e mensagens de canal**
1. Selecione **Avançar**.
1. Na página **Definir configurações de política**, selecione **Criar ou personalizar regras avançadas de DLP** e selecione **Avançar**.
1. Na opção **Personalizar regras avançadas de DLP**, selecione **+ Criar regra**.
1. Na página **Criar regra**:
   - No campo **Nome**, insira `Customer data`.
   - Em **Condições**, selecione **+ Adicionar condição** > **O conteúdo contém**.
   - Em **O conteúdo contém**, selecione **Adicionar** > **Tipos de informações confidenciais**.
   - Na página **Classificadores treináveis** à direita, selecione os classificadores para `Customer Complaints` e `Customer Files` e, em seguida, selecione **Adicionar** na parte inferior da página para adicionar esses classificadores pré-treinados.
   > [!tip] Use a barra de pesquisa para encontrar facilmente classificadores treináveis.
   - De volta à página **Criar regra** em **O conteúdo contém**, selecione **+ Adicionar condição** > **O conteúdo é compartilhado do Microsoft365**.
   - Em **Conteúdo é compartilhado do Microsoft365** selecione **com pessoas de fora da minha organização** na lista suspensa.
   - Em **Ações**, selecione **+ Adicionar uma ação** > **Restringir ou criptografar o conteúdo em locais do Microsoft 365**.
   - Em **Restringir ou criptografar o conteúdo em locais do Microsoft 365**, verifique se o botão de opção para **Bloquear somente pessoas fora da sua organização** está selecionado.
   - Em **Notificações do usuário**, alterne as notificações para **Ativado** e selecione a caixa de seleção para **Notificar os usuários no serviço do Office 365 com uma dica de política**.
   - Em **Substituições de usuário**, selecione a caixa de seleção para **Permitir substituições dos serviços do Microsoft 365**
   - Em **Relatórios de incidentes**, defina a opção **Usar este nível de severidade em alertas e relatórios de administrador:** como **Médio**.
   - Na parte inferior de **Criar regra**, selecione **Salvar**.
1. De volta à página **Personalizar regras avançadas de DLP**, selecione **Avançar**.
1. Na **página Modo de política**, selecione **Executar a política no modo de teste** e verifique se a opção **Mostrar dicas de política enquanto estiver no modo de simulação** está habilitada, depois selecione **Avançar**.
1. Na página **Examinar e concluir**, selecione **Enviar**.
1. Na página **Nova política criada**, selecione **Concluído**.

## Tarefa 2 – Modificar uma política de DLP

1. Na página **Políticas**, marque a caixa de seleção à esquerda da **Política de proteção de interação do cliente** recém-criada e, em seguida, selecione **Editar política** na parte superior da página.
1. Uma vez no assistente de criação de política de DLP, selecione **Avançar** até chegar à página **Modo de política** e, em seguida, selecione **Ativar a política imediatamente** para impor a política de DLP.
1. Selecione **Avançar** para examinar a política de DLP e, em seguida, selecione **Enviar** depois de revisar suas alterações.
1. Na página **Política atualizada**, selecione **Concluído**.

Agora você criou com êxito uma política de DLP para proteger dados confidenciais do cliente.
