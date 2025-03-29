# Modelagem de Requisitos

## Diagramas de Casos de Uso - Requisitos Funcionais

### Usuário

O usuário pode criar, visualizar, editar e excluir tarefas. Essas ações permitem a gestão eficiente de suas atividades.

### Criar Tarefa

Fluxo:
1. O usuário acessa a opção de criar tarefa.
2. Preenche os detalhes da nova tarefa.
3. Confirma e salva a tarefa no sistema.
4. O sistema armazena os dados e exibe uma confirmação.

### Atualizar Tarefa

Fluxo:
1. O usuário seleciona uma tarefa existente.
2. Modifica as informações conforme necessário.
3. Salva as alterações.
4. O sistema confirma a atualização dos dados.

### Excluir Tarefa

Fluxo:
1. O usuário escolhe uma tarefa para remover.
2. Confirma a exclusão.
3. O sistema remove os dados da tarefa e confirma a ação.

### Visualizar Tarefas

Fluxo:
1. O usuário acessa a lista de tarefas.
2. Pode aplicar filtros e ordenar as tarefas.
3. Pode visualizar os detalhes de uma tarefa específica.

## Modelo de Domínio

### Entidades e Relacionamentos
- **Usuário**: Responsável por criar e gerenciar as tarefas.
- **Tarefa**: Contém título, descrição, data de criação, data de vencimento e status.
- **Relacionamento**: Um usuário pode possuir várias tarefas.

### Estados das Entidades
- **Tarefa**: Criada, Em andamento, Concluída, Cancelada.
- **Usuário**: Ativo, Inativo.

## Requisitos Não Funcionais

Fluxo de Criação de Tarefa:
1. O usuário inicia a criação de uma nova tarefa.
2. Preenche os dados e confirma.
3. O sistema valida as informações.
4. Caso esteja tudo correto, a tarefa é salva e uma mensagem de confirmação é exibida.
5. Se houver erro, o usuário é notificado para corrigir.

Outros requisitos:
- O sistema deve ter tempo de resposta inferior a 1 segundo para ações CRUD.
- Deve ser acessível via web e dispositivos móveis.
- Garantia de disponibilidade de 99,9%.
- Segurança: Autenticação via OAuth 2.0.

## Modelos Iniciais


Os **modelos iniciais** do Sistema de Gerenciamento de Tarefas estabelecem a estrutura básica de **usuários** e **tarefas**, facilitando a gestão eficiente do fluxo de trabalho.

- **Usuários**: Cada usuário tem atributos como **id**, **nome**, **email** e **status** (Ativo/Inativo). O sistema gerencia múltiplos usuários, com controle de acesso às tarefas.
  
- **Tarefas**: Caracterizadas por **id**, **título**, **descrição**, **data de criação**, **data de vencimento**, **status** e **prioridade**. As tarefas podem ser criadas, editadas e removidas, além de acompanhar o status e a prioridade.

- **Relacionamento entre Usuários e Tarefas**: Um usuário pode ter várias tarefas, mas cada tarefa pertence a um único usuário. Esse relacionamento "um para muitos" organiza o controle e acompanhamento de atividades.

- **Fluxos de Trabalho**: Incluem a criação, edição, visualização e exclusão de tarefas, além da capacidade de filtrar e organizar as tarefas por status e prioridade.

Esses modelos servem como base para o desenvolvimento das funcionalidades e garantem uma gestão estruturada e eficiente das atividades no sistema.

## Aplicando INVEST

### Avaliação das Histórias de Usuário

| História | Independente (I) | Negociável (N) | Valiosa (V) | Estimável (E) | Pequena (P) | Testável (T) | Total |
|----------|------------------|----------------|-------------|---------------|-------------|--------------|-------|
| **Cadastrar Tarefa** | 4 | 4 | 5 | 4 | 3 | 5 | 25 |
| **Editar Tarefa**    | 3 | 4 | 5 | 5 | 4 | 5 | 26 |
| **Excluir Tarefa**   | 3 | 4 | 4 | 4 | 3 | 5 | 23 |
| **Visualizar Tarefas** | 4 | 4 | 5 | 5 | 4 | 5 | 27 |
| **Notificações**     | 2 | 3 | 5 | 3 | 2 | 4 | 19 |

**Escala:**
- 1 a 5 (1 = mínimo / 5 = máximo)

### Priorização das Histórias

- **Visualizar Tarefas**: 27 pontos (alta prioridade)
- **Editar Tarefa**: 26 pontos (alta prioridade)
- **Cadastrar Tarefa**: 25 pontos (alta prioridade)
- **Excluir Tarefa**: 23 pontos (média prioridade)
- **Notificações**: 19 pontos (baixa prioridade)

## Priorização (INVEST)

- **Independente**: Cada funcionalidade pode ser desenvolvida sem dependências rígidas.
- **Negociável**: Pode ser ajustada conforme necessário.
- **Valiosa**: Cada história agrega valor ao usuário.
- **Estimável**: Deve ser possível estimar o esforço.
- **Pequena**: Deve ser possível concluir em poucos dias.
- **Testável**: Critérios claros de aceitação.



## Prioridades e Justificativas

As prioridades das funcionalidades foram estabelecidas com base na importância e no impacto para o usuário final, bem como na complexidade de implementação. Abaixo estão as funcionalidades priorizadas, juntamente com as justificativas que orientaram a alocação de cada uma delas.

## **Alta Prioridade**

### 1. Criar Tarefas
**Justificativa**: A criação de tarefas é a funcionalidade central do sistema. Sem a capacidade de criar novas tarefas, o sistema perde sua principal utilidade. Esta funcionalidade é essencial para o funcionamento básico da aplicação e deve ser implementada o mais cedo possível.

### 2. Visualizar Tarefas
**Justificativa**: A visualização das tarefas é fundamental para que o usuário possa acompanhar o andamento de suas atividades. Sem a capacidade de visualizar suas tarefas, o usuário não teria controle sobre o que precisa ser feito. Esta funcionalidade proporciona a transparência necessária para o gerenciamento eficiente.

## **Média Prioridade**

### 3. Atualizar Tarefas
**Justificativa**: A capacidade de editar tarefas é importante, mas é menos urgente do que criar ou visualizar tarefas. Essa funcionalidade permite que os usuários façam ajustes nas tarefas conforme a necessidade, mas não é tão crítica quanto a criação ou visualização, pois a tarefa pode ser executada de forma inicial sem a necessidade de ajustes constantes.

### 4. Excluir Tarefas
**Justificativa**: Excluir tarefas é uma funcionalidade útil para a limpeza e organização do sistema, mas não é essencial para o fluxo de trabalho. Ela pode ser desenvolvida após as funcionalidades mais fundamentais, uma vez que a exclusão de tarefas não é uma ação constante durante o uso diário do sistema.

## **Baixa Prioridade**

### 5. Notificações
**Justificativa**: Embora as notificações possam melhorar a experiência do usuário, elas são consideradas uma funcionalidade complementar. A principal funcionalidade do sistema gira em torno do gerenciamento de tarefas, e as notificações podem ser adicionadas em uma versão posterior, após as funcionalidades essenciais estarem completas.


## Definition of Ready (DoR)

A **Definition of Ready (DoR)** define claramente o que constitui uma história de usuário "pronta para desenvolvimento". A equipe deve garantir que todos os critérios abaixo sejam atendidos antes de iniciar o trabalho no desenvolvimento de uma funcionalidade.

## Critérios de Aceitação

1. **Descrição Clara da História**: 
   - A história de usuário deve ter uma descrição completa e precisa do que é necessário. A equipe deve entender exatamente o que se espera da funcionalidade a ser implementada.

2. **Critérios de Aceitação Definidos**:
   - Todos os critérios de aceitação para a história devem estar claramente definidos, permitindo que a equipe saiba exatamente quando a tarefa será considerada concluída e funcionando conforme o esperado.

3. **Dependências Identificadas e Resolvidas**:
   - Todas as dependências externas, internas ou de outras histórias devem ser identificadas e resolvidas antes que a história seja considerada pronta para desenvolvimento. Se houver dependências de outros times ou sistemas, estas devem ser tratadas e solucionadas.

4. **Compreensão dos Requisitos pela Equipe**:
   - A equipe deve ter uma compreensão clara dos requisitos e do que é necessário para completar a história. Todos os membros do time devem estar alinhados quanto aos detalhes técnicos e funcionais da tarefa.

## Objetivo

- Garantir que a história esteja completamente pronta para ser desenvolvida, sem ambiguidade ou obstáculos que possam impedir o progresso. 
- Facilitar um ciclo de refinamento contínuo, com revisões regulares, de modo que todas as histórias sejam claras e prontas para desenvolvimento antes de serem inseridas no backlog de sprints.

Ao atender a esses critérios, a equipe garante que o trabalho será mais eficiente, reduzindo riscos e melhorando a qualidade da entrega.



## Matriz de rastreabilidade

RF001	Criar tarefas com título, descrição, data de vencimento e prioridade.	Alta	Permitir organização eficiente das tarefas.	RF002, RF003, RF006

RF002	Exibir todas as tarefas com filtros para busca.	Alta	Facilitar a visualização e gestão de tarefas.	RF001, RF004, RF009

RF003	Editar tarefas (título, descrição, data, prioridade).	Média	Garantir flexibilidade na organização das tarefas.	RF001, RF005

RF004	Marcar tarefas como concluídas e destacá-las.	Alta	Permitir rastreamento do progresso do usuário.	RF002, RF005

RF005	Excluir tarefas com confirmação.	Média	Evitar erros e dar controle ao usuário.	RF003, RF004

RF006	Enviar lembretes para tarefas com prazo.	Alta	Ajudar o usuário a não perder prazos.	RF001, RF007

RF007	Salvar tarefas de forma persistente.	Alta	Garantir que os dados não sejam perdidos.	RF001, RF006

RF008	Ordenar tarefas por data, prioridade ou título.	Média	Facilitar a organização e busca de tarefas.	RF002, RF009

RF009	Buscar tarefas por palavras-chave.	Média	Melhorar a navegação em listas grandes.	RF002, RF008

RF010	Sincronizar tarefas entre dispositivos.	Baixa	Acessar as tarefas de qualquer lugar.	RF007
