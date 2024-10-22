# <a> Metas, Operadores, Métodos e Regras de Seleção (GOMS) </a>

## <a> Introdução </a>

GOMS (Goals, Operators, Methods, and Selection Rules — Objetivos, Operadores, Métodos e Regras de Seleção) é um método derivado da interação humano-computador (IHC), que em resumo, caracteriza o conhecimento procedimental de uma pessoa ao realizar tarefas num determinado dispositivo (Kieras, 2001). O nível de granulidade variará de acordo com as necessidades da análise.

## <a> Termos do GOMS </a>

### <a> Objetivos </a>
Representam o que o usuário quer realizar utilizando o software (editar um texto, por exemplo).

### <a> Operadores </a>
São primitivas internas (cognitivas) ou externas (as ações concretas que o software permite que os usuários façam, tal como um comando e seus parâmetros digitados num teclado; a seleção de menus; o clique de um botão, são exemplos de operadores). 

### <a> Métodos </a>
São sequências bem conhecidas de subobjetivos e operadores que permitem atingir um objetivo maior. 

### <a> Regras de Seleção </a>
Quando há mais do que um método para atingir um mesmo objetivo, são necessárias regras de seleção, que representam tomadas de decisão dos usuários sobre qual método utilizar numa determinada situação. 

## <a> Técnicas ou modelos </a>

### <a> KLM (Keystroke-Level Method) </a>
O KLM é a técnica mais simples da família GOMS, limitada a um conjunto predefinido de operadores primitivos: K para pressionar uma tecla ou botão; P para apontar com o mouse um alvo num dispositivo visual; H para mover as mãos para o teclado ou outro dispositivo; D para desenhar um segmento de reta em um grid; M para se preparar mentalmente para realizar uma ação ou uma série de ações primitivas fortemente relacionadas entre si; e R para o tempo de resposta do sistema, durante o qual o usuário precisa esperar.

O KLM também inclui um conjunto de heurísticas sobre como posicionar operadores mentais durante a preparação. A estimativa de tempos de execução pode ser utilizada para comparar ideias em tarefas de benchmark, fazer uma avaliação paramétrica para explorar o espaço definido por importantes variáveis (e.g., o tamanho de nomes de arquivos em uma linguagem de comando) e fazer análises sobre as suposições feitas (e.g., velocidade de digitação do usuário) (John, 2003).

### <a> CMN-GOMS </a>
O CMN-GOMS se refere à proposta original de GOMS, elaborada por Card et al. (1983). No CMN-GOMS, há uma hierarquia estrita de objetivos, os operadores são executados estritamente em ordem sequencial, e os métodos são representados numa notação semelhante a um pseudocódigo, que inclui submétodos e condicionais.

Quantitativamente, os modelos CMN-GOMS permitem prever a sequência de operadores e o tempo de execução. Qualitativamente, eles focam métodos para alcançar objetivos: métodos semelhantes são facilmente identificados, métodos atipicamente curtos ou longos se destacam e podem disparar ideias de design, como, por exemplo, a inclusão de teclas de atalho para comandos frequentes e pontos de feedback para o usuário.

Uma diferença importante entre os modelos KLM e CMN-GOMS é que o CMN-GOMS é representado na forma de programa, e, portanto, a análise é geral e executável. Qualquer instância de classe de tarefas descrita pode ser realizada ou simulada seguindo os passos do modelo que podem passar por caminhos diferentes dependendo da situação específica da tarefa (John, 2003).

### <a> CPM-GOMS </a>
O CPM-GOMS foi assim designado por dois motivos: por representar operadores cognitivos, perceptivos e motores, e por seguir a abordagem de Critical Path Method (técnica de análise do caminho crítico). CPM-GOMS é uma versão do GOMS baseada diretamente no modelo de estágios paralelos do processamento humano de informações. Isso significa que o CPM-GOMS não supõe que os operadores são executados sequencialmente.

A construção de um modelo CPM-GOMS inicia com a construção do modelo CMN-GOMS, cujos operadores são em seguida classificados em operadores cognitivos, perceptivos e motores do MHP. Atribuímos então uma duração estimada a cada operador e calculamos o tempo de execução previsto para a tarefa. É possível ainda efetuar uma análise qualitativa da relação entre aspectos do design e o tempo de execução, bem como fazer simulações de designs alternativos e ajudar a identificar por que um terá um desempenho melhor do que o outro.

Em geral, o CPM-GOMS assume que o usuário é extremamente experiente e executa as tarefas tão rápido quanto a arquitetura MHP permite. Isso significa que o usuário sabe exatamente onde procurar visualmente um determinado item, e que não há atividades cognitivas substanciais associadas à seleção de métodos ou decisões complexas. Portanto, os modelos CPM-GOMS devem ser utilizados apenas para tarefas nas quais a seleção do método se baseia em dicas óbvias do ambiente ou envolve decisões triviais (John, 2003).

### <a> CTT (ConcurTaskTrees) </a>

O modelo de árvores de tarefas concorrentes (ConcurTaskTrees – CTT) foi criado para auxiliar a avaliação e o design e avaliação de IHC (Paterno, 1999). Nesse modelo, existem quatro tipos de tarefas:
* Tarefas do usuário, realizadas fora do sistema;
* Tarefas do sistema, em que o sistema realiza um processamento sem interagir com o usuário;
* Tarefas interativas, em que ocorrem os diálogos usuário–sistema; e
* Tarefas abstratas, que não são tarefas em si, mas sim uma representação de uma composição de tarefas
que auxilie a decomposição.

Dentre as vantagens do CTT com relação a outros modelos de tarefas, destacamos a possibilidade do registro explícito das relações entre as tarefas. Observamos que, uma vez que há tarefas interativas, do sistema e do usuário, o CTT vai além da análise de tarefas tradicional para representar uma solução de design da interação. Uma desvantagem com relação a modelos especificamente projetados para a interação é a ausência de elementos destinados à representação de mecanismos de prevenção e tratamento de erros na interação usuário–sistema.

## <a> Análise de Tarefas - GOMS </a> 

### <a> 1. Submissão de Problema </a> 

**Objetivo Geral:** Submeter uma solução para um problema de programação.

```
GOAL 0: Submeter solução para um problema de programação
    GOAL 1: Selecionar problema
        OP 1.1: Escolher problema da lista
        OP 1.2: Visualizar detalhes do problema
    GOAL 2: Escrever código
        OP 2.1: Digitar código no editor integrado
        OP 2.2: Utilizar realce de sintaxe e visualizar erros em tempo real
    GOAL 3: Testar código
        OP 3.1: Executar testes locais
        OP 3.2: Observar resultados dos testes
    GOAL 4: Submeter solução
        OP 4.1: Clicar em 'Submeter'
        OP 4.2: Aguardar envio e processamento
    GOAL 5: Receber feedback
        OP 5.1: Receber e analisar resultados da avaliação
```

### <a> 2. Tutorial de Resolução de Questões Pós-Contest </a> 

**Objetivo Geral:** Aprender a resolver problemas apresentados após o término de um contest.

```
GOAL 0: Aprender resolução de problemas pós-contest
    GOAL 1: Selecionar contest encerrado
        OP 1.1: Acessar lista de contests encerrados
        OP 1.2: Escolher contest específico
    GOAL 2: Escolher problema para revisão
        OP 2.1: Visualizar detalhes do problema
        OP 2.2: Acessar soluções passo a passo
    GOAL 3: Estudar solução detalhadamente
        OP 3.1: Seguir tutorial explicativo
        OP 3.2: Compreender técnicas e lógica utilizadas
    GOAL 4: Participar de discussões
        OP 4.1: Acessar fóruns ou seções de comentários
        OP 4.2: Interagir com outros usuários para aprofundamento
```
### <a> 3. Verificação de Submissões </a> 

**Objetivo Geral:** Verificar e analisar os resultados das submissões realizadas durante um contest.

```
GOAL 0: Verificar submissões de um contest
    GOAL 1: Acessar lista de submissões
        OP 1.1: Navegar até a lista de submissões do contest
        OP 1.2: Visualizar lista completa de submissões
    GOAL 2: Analisar resultado de uma submissão específica
        OP 2.1: Selecionar submissão específica
        OP 2.2: Analisar detalhes do resultado (correto, erro, tempo excedido)
    GOAL 3: Verificar logs de execução
        OP 3.1: Acessar logs de execução
        OP 3.2: Diagnosticar erros com base nos logs
```
### <a> 4. Ranking de Contest </a> 

**Objetivo Geral:** Calcular e exibir o ranking dos participantes de um contest.

```
GOAL 0: Exibir ranking de Contest
    GOAL 1: Calcular pontos das submissões
        OP 1.1: Processar resultados das submissões
        OP 1.2: Aplicar critérios de pontuação
    GOAL 2: Ordenar resultados
        OP 2.1: Aplicar critérios de ordenação
        OP 2.2: Atualizar ranking exibido
    GOAL 3: Acessar detalhes de performance
        OP 3.1: Clicar em participante para detalhes
        OP 3.2: Visualizar informações detalhadas
    GOAL 4: Atualizar ranking em tempo real
        OP 4.1: Receber novas submissões
        OP 4.2: Recalcular e atualizar ranking
```
### <a> 5. Criação de Problema (Administrador) </a> 

**Objetivo Geral:** Criar e configurar novos problemas de programação.

```
GOAL 0: Criar novo problema de programação
    GOAL 1: Escrever enunciado do problema
        OP 1.1: Digitar o texto do enunciado
        OP 1.2: Revisar o enunciado
    GOAL 2: Configurar testes
        OP 2.1: Definir entradas e saídas esperadas
        OP 2.2: Salvar testes
    GOAL 3: Definir restrições técnicas
        OP 3.1: Estabelecer limites de tempo e memória
        OP 3.2: Salvar restrições
    GOAL 4: Publicar problema
        OP 4.1: Revisar todas as configurações
        OP 4.2: Publicar problema para usuários
```

### <a> 6. Criação de Contest (Administrador) </a> 

**Objetivo Geral:** Organizar e configurar uma competição de programação.

```
GOAL 0: Organizar uma nova competição de programação
    GOAL 1: Definir informações básicas do contest
        OP 1.1: Inserir nome, duração, e tipo de acesso
        OP 1.2: Registrar informações
    GOAL 2: Selecionar problemas
        OP 2.1: Escolher problemas existentes ou criar novos
        OP 2.2: Adicionar problemas ao contest
    GOAL 3: Configurar participantes
        OP 3.1: Definir acesso aberto ou restrito
        OP 3.2: Salvar configurações de participantes
    GOAL 4: Definir regras de pontuação
        OP 4.1: Estabelecer critérios de pontuação e penalidades
        OP 4.2: Salvar regras de pontuação
    GOAL 5: Publicar contest
        OP 5.1: Verificar configurações finais
        OP 5.2: Publicar contest
```

## <a> Bibliografia </a>
> <a id="REF1" href="#anchor_1">1. </a> Barbosa, S. D. J.; Silva, B. S. da; Silveira, M. S.; Gasparini, I.; Darin, T.; Barbosa, G. D. J. (2021) Interação Humano-Computador e Experiência do usuário.
>
> <a id="REF2" href="#anchor_2">2. </a> Stanton N, Salmon P, Walker G, et al. Task analysis methods. Human factors methods: a practical guide for engineering and design. Great Britain: Ashgate; 2005. p. 45-76.

## <a> Histórico de Versão </a>

| Versão | Data | Data Prevista de Revisão | Descrição  | Autor(es)  | Revisor(es) |
| ------- | ------ | ------ | ------- | -------- | -------- |
| `1.0` | 06/05/2024 | 06/05/2024 | Criação da página de Metas, Operadores, Métodos e Regras de Seleção.| [Luiz Gustavo](https://github.com/LuizGust4vo) | [João Artur](https://github.com/joao-artl) |
| `1.1` | 10/05/2024 | 11/05/2024 | Adicionando análise de tarefas usando o método GOMS | [João Artur](https://github.com/joao-artl) | [Luiz Gustavo](https://github.com/LuizGust4vo)|