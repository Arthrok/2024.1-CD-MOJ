## <a>Introdução</a>

Prezando pela engenharia de usabilidade Mayhew (1999) propôs um ciclo de vida que reúne e organiza diferentes atividades propostas da área de IHC para orientar o trabalho do designer, sendo as fases: análise de requisitos, design/avaliação/desenvolvimento e instalação<a id="anchor_1" href="#FRM1">^1^</a>.

Na análise de requisitos, que de acordo com o ciclo de vida desenvolvido por Mayhew é a primeira fase, são definidas as metas de usabilidade com base em alguns aspectos, incluindo inclusive as características da plataforma em que a equipe irá trabalhar, destacando suas possibilidades e limitações<a id="anchor_1" href="#FRM1">^1^</a>.

## <a>Metodologia</a>

O método de avaliação utilizado foi a *inspeção*, que envolve a análise crítica da interface por avaliadores que buscam identificar problemas potenciais ou reais que os usuários podem enfrentar. Durante a inspeção, os avaliadores se colocam no lugar de usuários com perfis específicos, levando em consideração seus conhecimentos e experiências prévias em atividades relacionadas. Este método não envolve diretamente os usuários, mas simula experiências de usuário para prever e resolver problemas de usabilidade antes que afetem os usuários reais<a id="anchor_3" href="#FRM3">^2^</a>.


## <a>Características da Plataforma</a>

Um sistema tem como principal objetivo a correspondência sobre usabilidade dos usuários e a eficiência perante ao propósito que foi desenvolvido.

O *Contest-Driven Meta Online Judge* (CD-MOJ) é um online judge direcionado a contests que despacha os códigos para outro "online judge" ao invés de executar e verificar a corretude da solução <a id="anchor_2" href="#FRM2">^3^</a>.

A plataforma possui os seguintes recursos e funcionalidades:

- Usuários Registrados: Todos os indivíduos cadastrados nos contests, incluindo alunos e professores que atuam como administradores.
- Histórico de Contests: Acesso aos contests anteriores, incluindo detalhes como o tempo de submissão de cada questão desde o início do contest e o total de submissões realizadas.
- Ranking por Contest: Um sistema de classificação que ordena os participantes com base no desempenho em cada contest.
- Acesso às Questões: As questões podem ser acessadas através de links para documentos PDF ou páginas HTML, dependendo do formato disponibilizado.
- Feedback de Submissões: O sistema retorna resultados detalhados para cada submissão, como "Time Limit Exceeded", "Runtime Error", "Accepted 100p", entre outros, permitindo aos usuários identificar possíveis erros em seus códigos.

Sobre tecnologia, o CD-MOJ é desenvolvido em *Shell Script* e baseado na especificação *CGI - Common Gateway Interface*.

## <a>Requisitos de Sistema</a>
Para garantir uma experiência de usuário consistente e segura, o sistema CD-MOJ é compatível com qualquer navegador, mas não é tão acessível por dispositivos mobile, devido a responsividade implementada.

É necessário a permissão de acesso aos arquivos do computador, pois a submissão deve ser feita a partir do upload do arquivo, com o código referente a questão.

## <a>Limites da Plataforma</a>
- O usuário, se não cadastrado por um administrador não poderá efetuar submissão de questões.
- O usuário, não tem acesso ao log das questões submetidas.
- O usuário não consegue filtrar somente o contest que ele está participando, dificultando muitas vezes a achar o mesmo.
- O usuário, tem um tempo de resposta muito grande após efetuar a submissão da questão.
- A plataforma pode não ser totalmente acessível para usuários com deficiências visuais ou outras necessidades especiais.
- Em alguns momentos, o sistema pode enfrentar problemas de escalabilidade, resultando em tempos de resposta lentos ou indisponibilidade temporária.
- A plataforma tem recorrente necessidades de manutenções regulares e atualizações de sistema/questões.

## <a>Referência Bibliográfica</a>

> <a id="FRM1" href="#anchor_1">1.</a> Barbosa, S. D. J.; Silva, B. S. da; Silveira, M. S.; Gasparini, I.; Darin, T.; Barbosa, capítulo 6 Processos de Design de IHC, tópico 6.3.3 Engenharia de Usabilidade de Mayhew, página 120, G. D. J. (2021) *Interação Humano-Computador e Experiência do usuário.* Autopublicação. ISBN: 978-65-00-19677-1.

> <a id="FRM2" href="#anchor_2">2.</a> Barbosa, S. D. J.; Silva, B. S. da; Silveira, M. S.; Gasparini, I.; Darin, T.; Barbosa, capítulo 11 Planejamento da Avaliação de IHC, tópico 11.6 Qual Tipo de Método de Avaliação Escolher?. página 272, G. D. J. (2021) *Interação Humano-Computador e Experiência do usuário.* Autopublicação. ISBN: 978-65-00-19677-1.

> <a id="FRM3" href="#anchor_3">3.</a> Ribas, Bruno. Contest-Driven Meta Online Judge. Disponível em: <https://moj.naquadah.com.br/about.shtml>. Acesso em 08/05/2024.


## <a>Histórico de versão</a>
|Versão|Data|Data Prevista de Revisão|Descrição|Autor|Revisor|
| :------: | :----------: |:-----------: | :----------------------: | :---------: |:---------: |
| `1.0` | 08/05/2024 | 09/05/2024 |Criação da documentação das Características da plataforma | [Eric Silveira](https://github.com/ericbky) | [Arthur Alves](https://github.com/Arthrok) |
| `2.0` | 16/05/2024 | 19/05/2024 | Revisão pós apresentação | [Eric Silveira](https://github.com/ericbky) | [Arthur Alves](https://github.com/Arthrok)|