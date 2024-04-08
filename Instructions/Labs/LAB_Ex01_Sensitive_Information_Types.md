---
lab:
  task: Create a custom sensitive information type
  exercise: Exercise 1 - Create a custom sensitive information type
---

## Locatários do WWL – Termos de uso

Se você estiver recebendo um locatário como parte de uma entrega de treinamento com instrutor, observe que o locatário é disponibilizado com a finalidade de dar suporte aos laboratórios práticos no treinamento com instrutor.

Os locatários não devem ser compartilhados ou usados para fins fora dos laboratórios práticos. O locatário usado neste curso é um locatário de avaliação e não pode ser usado ou acessado após o fim da aula e não está qualificado para extensão.

Os locatários não podem ser convertidos em uma assinatura paga. Os locatários obtidos como parte deste curso permanecem a propriedade da Microsoft Corporation e reservamos o direito de obter acesso e a qualquer momento.

# Tarefas de habilidades

Sua tarefa é criar um tipo de informação confidencial (SIT) personalizado que atenda aos critérios necessários:

- **Padrão regex personalizado para a ID de funcionário**: inclua um padrão regex que identifique a configuração de ID exclusiva de funcionário da sua organização, que é composta por 9 caracteres: 3 dígitos, um hífen, seguido por 5 letras (por exemplo, 123-abcde).
- **Lista de palavras-chave associadas a IDs de funcionário**: incorpore uma lista de palavras-chave que são comumente associadas a IDs de funcionários para aprimorar a exatidão da detecção.

## Tarefa 1: criar um tipo de informação confidencial

1. Navegue até o portal de conformidade do Microsoft Purview.
1. Expanda a **Classificação de dados** e selecione **Classificadores**.
1. Selecione **Tipos de informações confidenciais** e, em seguida, selecione **+ Criar de tipo de informação confidencial**.
1. Na página **Nomear o tipo de informação confidencial**, dê ao seu tipo de informação confidencial um **Nome** **Descrição** significativos para o seu tipo de informação confidencial e selecione**Próximo**.
1. Na página **Definir padrões para este tipo de informação confidencial**, selecione**Criar padrão**.
1. Na página **Novo padrão**, selecione **+ Adicionar elemento primário** > **Expressão regular**.
1. Na página **Adicionar uma expressão regular**, atribua à expressão regular um nome significativo para **ID** e insira `\d{3}-[a-zA-Z]{5}` no campo **Expressão regular** para atender às exigências da organização. Selecione **Concluído** quando terminar.
1. De volta à página **Novo padrão**, em **Elementos de suporte**, selecione **+ Adicionar elementos de suporte ou grupo de elementos** > **Lista de palavras-chave**.
1. Na página **Adicionar uma lista de palavras-chave**, dê à sua lista de palavras-chave uma **ID** significativa. Em **Grupo de palavras-chave nº1**, na seção **Sem distinção entre maiúsculas e minúsculas**, insira:
   - `Employee ID`
   - `Staff number`
   - `Work ID`
1. Selecione **Concluído** quando terminar.
1. De volta à página **Novo padrão**, selecione **Criar**.
1. Selecione **Próximo** na página **Definir padrões para este tipo de informação confidencial**.
1. Na página **Escolher o nível de confiança recomendado para mostrar nas políticas de conformidade**, deixe a seleção padrão e selecione **Próximo**.
1. Examine as configurações e selecione **Criar**.
1. Na página **Seu tipo de informação confidencial foi criado**, selecione **Concluído**.

Você criou com sucesso um tipo de informação confidencial (SIT) personalizado para melhorar a segurança e o gerenciamento dos números das IDs exclusivas dos funcionários da sua empresa.
