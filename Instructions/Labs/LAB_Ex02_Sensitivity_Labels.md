---
lab:
  task: Create and publish a sensitivity label
  exercise: Exercise 2 - Create and publish a sensitivity label
---

# Tarefas de habilidades

Sua tarefa é criar e publicar rótulos de confidencialidade em sua organização que classifiquem e protejam dados confidenciais de acordo com seu nível de confidencialidade e os controles de acesso necessários.

- **Crie um rótulo de confidencialidade** para categorizar dados.
- **Crie um sub-rótulo** sob o rótulo pai para agrupar dados.
- **Crie uma política de rótulos** para estabelecer regras e diretrizes de gerenciamento dos rótulos de confidencialidade na organização.

**Objetivo**: Criar e publicar um rótulo de confidencialidade para melhorar a proteção de dados no departamento de RH. Sua tarefa é configurar um rótulo pai chamado _Interno_, com um sub-rótulo chamado _Dados do funcionário (RH)_.

## Tarefa 1 – Criar um rótulo de confidencialidade

1. Navegue até o portal de conformidade do Microsoft Purview.
1. Expanda **Proteção de informações** e selecione **Rótulos**.
1. Nos **Rótulos**, selecione **+ Criar um rótulo**.
1. Em **Fornecer detalhes básicos para esse rótulo**, insira as seguintes informações:

    - **Nome**: `Internal`
    - **Nome de exibição**: `Internal`
    - **Descrição para usuários**: `Internal sensitivity label.`
    - **Descrição para administradores**: `Internal sensitivity label for Contoso.`

1. Selecione **Avançar**.
1. Na página **Definir o escopo deste rótulo**, selecione **Itens**, depois selecione **Arquivos** e **Emails** e, por fim, selecione **Avançar**.
1. Na página **Escolher configurações de proteção para os tipos de itens selecionados**, selecione **Avançar**.
1. Selecione **Avançar** e aceite os padrões até chegar à página **Examinar suas configurações e concluir** e, em seguida, selecione **Criar rótulo**.
1. Na página **Seu rótulo de confidencialidade foi criado**, selecione **Não criar uma política ainda** e selecione **Concluído**.

## Tarefa 2 – Criar um rótulo de sub-rótulo

1. Na página “Proteção de informações”, realce (sem selecionar) o rótulo **Interno** recém-criado e selecione o menu vertical **...** ![Imagem do menu de pontos vertical](../Media/SensitivityLabelDotMenu.png)
1. Selecione **+ Criar sub-rótulo** no menu.
1. Em **Fornecer detalhes básicos para esse rótulo**, insira as seguintes informações:

   - **Nome**: `Employee data (HR)`
   - **Nome de exibição**: `Employee data (HR)`
   - **Descrição para usuários**: `This label is the default label for all documents in the HR Department.`
   - **Descrição para administradores**: `This label is created in consultation with the Director of HR.`
1. Selecione **Avançar**.
1. Na página **Definir o escopo deste rótulo**, selecione **Itens**, depois selecione **Arquivos** e **Emails** e, por fim, selecione **Avançar**.
1. Em **Escolher configurações de proteção para os tipos de itens selecionados**, marque a caixa de seleção **Controlar acesso** e, em seguida, selecione **Avançar**.
1. Na página **Controle de acesso**:
   - Verifique se o botão de opção para **Definir as configurações de controle de acesso** está selecionado.
   - Em **Atribuir permissões agora ou permitir que os usuários decidam?**, selecione **Atribuir permissões agora**.
   - Em **O acesso do usuário ao conteúdo expira**, selecione **Nunca**.
   - Em **Permitir acesso offline**, selecione **Apenas por um número de dias**.
   - No campo **Os usuários têm acesso offline ao conteúdo por quantos dias**, insira 14.
   - Em **Atribuir permissões a usuários e grupos específicos**, selecione o botão **Atribuir permissões**.
1. Na página **Atribuir permissões**, selecione **+ Adicionar qualquer usuário autenticado** e, em seguida, selecione **Salvar**.
1. De volta à página **Controle de acesso**, selecione **Avançar**.
1. Selecione **Avançar** e aceite os padrões até chegar à página **Examinar suas configurações e concluir** e, então, selecione **Criar rótulo**.
1. Na página **Seu rótulo de confidencialidade foi criado**, selecione **Não criar uma política ainda** e selecione **Concluído**.

## Tarefa 3 – Publicar um rótulo de confidencialidade

1. Na página **Rótulos**, marque as caixas de seleção ao lado do rótulo **Interno** e do sub-rótulo **Dados do funcionário (RH)** recém-criados.
1. Na página **Escolher rótulos de confidencialidade para publicar**, verifique se os rótulos “Interno” e “Dados do funcionário (RH)” estão exibidos sob **Rótulos de confidencialidade para publicar** e, em seguida, selecione **Avançar**.
1. Selecione **Avançar** até chegar à página **Configurações de política**.
1. Na página **Configurações de política**, marque a caixa de seleção **Os usuários devem fornecer uma justificativa para remover um rótulo ou diminuir sua classificação**.
1. Selecione **Avançar** até chegar à página **Nome da política**
1. Na página **Nome da política**, insira as seguintes informações:

   - **Nome**: `Internal HR employee data`
   - **Insira uma descrição para sua política de rótulo de confidencialidade**: `This HR label is to be applied to internal HR employee data.`

1. Selecione **Avançar**.
1. Na página **Examinar e concluir**, selecione **Enviar**.
1. Na página **Nova política criada**, selecione **Concluído**.

Agora você criou com êxito um rótulo de confidencialidade para classificar os dados dos funcionários para o departamento de RH.
