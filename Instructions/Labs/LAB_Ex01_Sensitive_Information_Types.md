---
lab:
  task: Create a custom sensitive information type
  exercise: Exercise 1 - Create a custom sensitive information type
---

# Tarefa de habilidades

Sua tarefa é criar e publicar rótulos de confidencialidade em sua organização que classifiquem e protejam dados confidenciais de acordo com seu nível de confidencialidade e os controles de acesso necessários.

**Tarefa**:

- Criar um tipo de informação confidencial personalizada

## Tarefa – Criar um tipo de informações confidenciais personalizado

Nesta tarefa, você criará um novo tipo de informações confidenciais personalizado que reconhece o padrão de IDs de funcionário perto das palavras-chave "Funcionário" e "ID".

1. No **Microsoft Edge**, navegue até **`https://purview.microsoft.com`** e faça logon no portal do Microsoft Purview como o usuário definido como ** Administrador de conformidade** em uma tarefa anterior.

1. Na barra lateral esquerda, escolha **Soluções** e, em seguida, **Proteção de informações**.

1. Na barra lateral à esquerda, expanda **Classificadores** e escolha **Tipos de informações confidenciais**.

1. Na página **Tipos de informações confidenciais**, escolha **+ Criar tipo de informações confidenciais** para iniciar a configuração do tipo de informações confidenciais.

1. Na página **Nomear seu tipo de informações confidenciais**, insira:

    - **Nome**: `Contoso Employee IDs`
    - **Descrição**: `Pattern for Contoso employee IDs.`

1. Selecione **Avançar**.

1. Na página **Definir padrões para este tipo de informação confidencial**, selecione**Criar padrão**.

1. No painel do submenu **Novo padrão** à direita, escolha **+ Adicionar elemento primário** > **Expressão regular**.

1. No painel do submenu **+ Adicionar uma expressão regular** à direita, insira:

    - **ID**: `Contoso IDs`
    - **Expressão regular**: `[A-Z]{3}[0-9]{6}`
    - Clique no botão de opção para *Correspondência de cadeia de caracteres*

1. Clique em **Concluído** na parte inferior do painel de submenu.

1. De volta ao painel do submenu **Novo padrão**, em **Elementos de suporte**, clique no menu suspenso **+ Adicionar elementos de suporte ou grupo de elementos** e escolha **Lista de palavras-chave**.

1. No painel de submenu **Adicionar uma lista de palavras-chave** à direita, insira:

    - **ID**: `Employee ID keywords`
    - **Não diferencia maiúsculas de minúsculas**:

       ```text
       Employee
       ID
       ```

    - Clique no botão de opção para *Correspondência de palavras*

1. Clique em **Concluído** na parte inferior do painel de submenu.

1. De volta ao painel do submenu **Novo padrão**, em **Proximidade de caracteres**, diminua o valor **Detectar elementos primários E de suporte** para `100` caracteres.

1. Clique no botão **Criar** na parte inferior do painel de submenu.

1. De volta à página **Definir padrões para este tipo de informações confidenciais**, clique em **Avançar**.

1. Na página **Escolher o nível de confiança recomendado para mostrar nas políticas de conformidade**, use o valor padrão e clique em **Avançar**.

1. Na página **Revisar configurações e concluir**, revise as configurações e selecione **Criar**. Quando a criação tiver êxito, selecione **Concluído**.

Você criou um novo tipo de informação confidencial para identificar IDs de funcionários no padrão de três caracteres maiúsculos, seis números e as palavras-chave "Funcionário" ou "IDs" dentro de um intervalo de 100 caracteres.
