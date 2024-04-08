---
lab:
  task: Create and assign an auto-labeling policy
  exercise: Exercise 3 - Create and assign an auto-labeling policy
---

# Tarefas de habilidades

Sua tarefa é criar e publicar rótulos de confidencialidade em sua organização que classifiquem e protejam dados confidenciais de acordo com seu nível de confidencialidade e os controles de acesso necessários.

- **Crie um rótulo de confidencialidade** para categorizar dados.
- **Configurar o rótulo para rotulagem automática** para arquivos e emails.
- **Configurar uma política de rotulagem automática** para classificar automaticamente os dados no SharePoint e no OneDrive.
- **Publicar a política de rotulagem automática** para implantar o rótulo em sua organização, automatizando a classificação para segurança e conformidade aprimoradas.

**Objetivo**: Crie e publique uma política de rotulagem automática para o departamento de Finanças. Sua tarefa é configurar um rótulo de confidencialidade que aplica automaticamente rótulos a arquivos e emails com base em dados financeiros. Você também precisa criar uma política de rotulagem automática que aplique automaticamente esses rótulos ao conteúdo no SharePoint e no OneDrive.

## Tarefa 1 – Criar um rótulo de confidencialidade

1. Navegue até o portal de conformidade do Microsoft Purview.
1. Expanda **Proteção de informações** e selecione **Rótulos**.
1. Nos **Rótulos**, selecione **+ Criar um rótulo**.
1. Em **Fornecer detalhes básicos para esse rótulo**, insira as seguintes informações:

    - **Nome**: `Protected Financial Records`
    - **Nome de exibição**: `Protected Financial Records`
    - **Descrição para usuários**: `Use for documents with sensitive financial data.`
    - **Descrição para administradores**: `Applies encryption and access controls to financial documents.`

1. Selecione **Avançar**.
1. Na página **Definir o escopo deste rótulo**, selecione **Itens**, depois selecione **Arquivos** e **Emails** e, por fim, selecione **Avançar**.
1. Na página **Escolher configurações de proteção para os tipos de itens selecionados**, selecione **Avançar**.
1. Em **Rotulagem automática para arquivos e emails**:
   - Habilite a **Rotulagem automática para arquivos e emails**
   - Em **Detectar conteúdo que corresponda a essas condições** selecione **+ Adicionar condição** > **O conteúdo contém**.
   - Em **O conteúdo contém**, selecione **Adicionar** > **Tipos de informações confidenciais**.
   - Na página **Tipos de informações confidenciais**, pesquise e adicione o tipo de informações confidenciais para `Credit Card Number`, `U.S. Bank Account Number` e `ABA Routing Number`. **Adicione** para adicionar os três tipos de informações confidenciais e selecione **Salvar**.
   - Em **Quando o conteúdo corresponder a essas condições**, selecione **Aplicar o rótulo automaticamente**.
   - Deixe o opcional **Exibir esta mensagem aos usuários quando o rótulo for aplicado** em branco.
1. Selecione **Avançar** e aceite os padrões até chegar à página **Examinar suas configurações e concluir** e, então, selecione **Criar rótulo**.
1. Na página **Seu rótulo de confidencialidade foi criado**, selecione **Não criar uma política ainda** e selecione **Concluído**.

## Tarefa 2 – Criar uma política de rotulagem automática

1. Na página **Rótulos**, marque a caixa de seleção ao lado do rótulo **Registros Financeiros Protegidos** recém-criado e selecione **Criar política de rotulagem automática**.
1. Na página **Nomeie sua política de rotulagem automática**, insira as seguintes informações:

   - **Nome**: `Finance Auto-Label Policy`
   - **Insira uma descrição para sua política de rótulo de confidencialidade**: `Automates the labeling of financial documents.`
1. Selecione **Próximo** até chegar à página **Definir regras para conteúdo em todos os locais**.
1. Em **Definir regras para conteúdo em todos os locais**, selecione **Nova regra**.
1. Na página **Nova regra**:
   - Insira `Financial data` como **Nome**.
   - Em **Condições**, selecione **+ Adicionar condição** > **O conteúdo contém**.
   - Em **O conteúdo contém**, selecione **Adicionar** > **Tipo de informação confidencial**.
   - Na página **Tipos de informações confidenciais**, pesquise e adicione o tipo de informações confidenciais para `Credit Card Number`, `U.S. Bank Account Number` e `ABA Routing Number`. **Adicione** para adicionar os três tipos de informações confidenciais e selecione **Salvar**.
1. Selecione **Próximo** até chegar à página **Decidir se deseja testar a política agora ou depois**.
1. Na página **Decidir se deseja testar a política agora ou depois**, selecione **Executar política no modo de simulação** e selecione **Próximo**.
1. Na página **Examinar e concluir**, selecione **Criar política**.
1. Na página **Sua política de rotulagem automática foi criada**, selecione **Concluído**.

Agora você criou com êxito um rótulo de confidencialidade para classificar os dados financeiros para o departamento Financeiro.
