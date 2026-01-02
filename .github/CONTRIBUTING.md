# Contribuindo com o rAthena


Tabela de Conteúdos
------------------

  * [Relatando Bugs](#relatando-bugs)
  * [Sugerindo Melhorias](#sugerindo-melhorias)
  * [Rótulos de Issues](#rótulos-de-issues)
  * [Ambiente de Desenvolvimento Local](#ambiente-de-desenvolvimento-local)
  * [Torne-se um Membro da Equipe](#torne-se-um-membro-da-equipe)

Relatando Bugs
--------------

Estas informações existem para guiá-lo no processo de criação de um relatório de bug para o rAthena!  
As Issues não servem apenas para os desenvolvedores rastrearem bugs, mas também para acompanhar melhorias e tarefas.  
Quanto mais detalhado for o seu relatório, mais fácil será para os desenvolvedores reproduzirem e resolverem o bug!

### Você encontrou um bug? :bug:

* **Certifique-se de que o bug não é causado por alguma customização** em seus arquivos!
* **Certifique-se de que o bug ainda não foi reportado**, pesquisando no GitHub em [Issues](https://github.com/rathena/rathena/issues).  
  Se a mesma issue já existir, fique à vontade para deixar um comentário informando que você também está enfrentando o problema e, se possível, adicionar informações adicionais ou ausentes!
* Caso não encontre uma issue aberta abordando o problema, [abra uma nova](#enviar-um-relatório-de-bug)!

#### Enviar um Relatório de Bug :inbox_tray:

Existem vários fatores que fazem de um relatório de bug um bom relatório!

Este é um detalhamento de uma Issue genérica:
* **Título** deve fornecer uma visão geral sobre o bug.
* **Descrição** deve fornecer mais detalhes que não podem ser explicados apenas no **Título**.
* **Rótulos (Labels)** possuem cores para representar a categoria à qual pertencem.
* **Marcos (Milestones)** são utilizados pelos desenvolvedores para agrupar tarefas e avaliar rapidamente o quão próximo o projeto está da conclusão.
* **Responsáveis (Assignees)** são os desenvolvedores diretamente ligados à resolução da issue.
* **Comentários** permitem que outros membros forneçam feedback sobre a issue.

#### Quais são bons detalhes para fornecer em um relatório de bug? :pencil2:

Ao descrever sua Issue na área de **Descrição**, é recomendável fornecer o máximo de informações possível para que a issue seja resolvida o mais rápido possível.  
Lembre-se de que você pode marcar pessoas na **Descrição** usando o recurso `@mention`.  
Você também pode referenciar outras Issues ou Pull Requests digitando `#`, o que exibirá uma lista de opções.

Você pode encontrar um guia de Markdown em:  
[Mastering Markdown](https://guides.github.com/features/mastering-markdown/)

Algumas informações importantes a considerar ao criar uma Issue:
* **Hash do GitHub**: O hash é uma string alfanumérica de 40 caracteres (normalmente reduzida aos primeiros 7) que indica a versão utilizada.  
  (**Se você estiver usando SVN em vez de Git:** informe também a data da alteração e a primeira linha da mensagem do commit ao lado do número da revisão, caso contrário não será possível localizar o hash correspondente no Git).
* **Data do Cliente**: A data do cliente fornece detalhes importantes dependendo da issue. O principal ponto é ajudar a identificar problemas relacionados a packets.
* **Modificações que podem afetar os resultados**: É sempre recomendável tentar reproduzir o problema em um rAthena limpo, especialmente se houver muitas modificações.
* **Descrição do Problema**: Descreva o problema em detalhes! Capturas de tela e vídeos ajudam bastante!  
  Forneça também crash dumps caso algum dos servidores esteja encerrando inesperadamente.
* **Como Reproduzir o Problema**: Descreva detalhadamente como reproduzir o problema. Quanto mais informações, melhor!
* **Informação Oficial**: Forneça fontes confiáveis que comprovem que se trata de um bug.  
  Não utilize links da iRO Wiki, pois há uma grande chance de não corresponder ao comportamento do kRO.

#### Atenção ao uso do recurso `@mention`! :warning:

Como o rAthena utiliza comandos personalizados com `@`, ao descrever uma issue relacionada a esses comandos, tenha em mente que isso pode conflitar com o sistema de menções do GitHub!  
Sempre coloque o comando entre crases, como ``` `@comando` ```, para evitar mencionar usuários do GitHub que não têm relação com o assunto.

Sugerindo Melhorias
------------------

### Você escreveu um patch que corrige um bug? :bookmark_tabs:

* Abra um novo Pull Request no GitHub com o patch.
* Certifique-se de que a descrição do PR descreva claramente o problema e a solução. Inclua o número da issue relacionada, se aplicável.

### Você pretende adicionar uma nova funcionalidade ou alterar uma existente? :bulb:

* Abra um novo Pull Request no GitHub com a nova funcionalidade ou alteração.
* Certifique-se de que a descrição do PR descreva claramente o objetivo da adição ou alteração. Inclua o número da issue relacionada, se aplicável.

#### Como criar Pull Requests :pencil:

1. Certifique-se de que você possui uma conta no [GitHub](https://github.com/signup/free).
2. Em seguida, faça um [fork do rAthena](https://help.github.com/articles/fork-a-repo/#fork-an-example-repository) para a sua conta.
3. Antes de realizar alterações, certifique-se de [criar um novo branch](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/) para seu trabalho.  
   Nunca utilize o branch **master**! :bangbang:
4. Após concluir as alterações, faça commit e push para o seu branch.
5. Agora você está pronto para [criar um Pull Request](https://help.github.com/articles/creating-a-pull-request/) para o rAthena!
  * Ao criar o Pull Request, certifique-se de seguir nosso [template](https://github.com/rathena/rathena/blob/master/.github/PULL_REQUEST_TEMPLATE.md) e fornecer todas as informações necessárias.
  * **OPCIONAL**: Agradecemos muito se você marcar a opção para [permitir edições pelos mantenedores](https://help.github.com/articles/allowing-changes-to-a-pull-request-branch-created-from-a-fork/), permitindo pequenos ajustes antes do merge.

Rótulos de Issues
----------------

Na maioria dos casos, como usuário, você não precisará se preocupar com **Milestone** ou **Assignee**.  
Os diferentes **Rótulos (Labels)** permitem que os desenvolvedores compreendam rapidamente a issue e facilitem buscas e organização.

:bangbang: Os usuários devem prestar atenção especial aos rótulos de **Modo (Mode)** e **Status**, pois eles podem exigir feedback! :bangbang:

#### Componente

| Nome do Rótulo | Link de Busca | Descrição |
| --- | --- | --- |
| `component:core` | [search][search-rathena-label-componentcore] | Falha localizada no núcleo principal do rAthena. |
| `component:database` | [search][search-rathena-label-componentdatabase] | Falha localizada no banco de dados do rAthena. |
| `component:documentation` | [search][search-rathena-label-componentdocumentation] | Falha localizada na documentação do rAthena. |
| `component:script` | [search][search-rathena-label-componentscript] | Falha localizada nos scripts do rAthena. |
| `component:skill` | [search][search-rathena-label-componentskill] | Falha relacionada especificamente a uma skill. |
| `component:tool` | [search][search-rathena-label-componenttool] | Falha localizada em uma ferramenta do rAthena. |

#### Ausente

| Nome do Rótulo | Link de Busca | Descrição |
| --- | --- | --- |
| `missing:clientdate` | [search][search-rathena-label-missingclientdate] | O **Título** ou **Descrição** não informa a data do cliente usada. |
| `missing:mode` | [search][search-rathena-label-missingmode] | O **Título** ou **Descrição** não informa se é modo pre-renewal ou renewal. |
| `missing:revision` | [search][search-rathena-label-missingrevision] | A **Descrição** não informa a revisão do rAthena utilizada. |

#### Modo

| Nome do Rótulo | Link de Busca | Descrição |
| --- | --- | --- |
| `mode:prerenewal` | [search][search-rathena-label-modeprerenewal] | Falha existente no modo pre-renewal. |
| `mode:renewal` | [search][search-rathena-label-moderenewal] | Falha existente no modo renewal. |

#### Prioridade

| Nome do Rótulo | Link de Busca | Descrição |
| --- | --- | --- |
| `priority:high` | [search][search-rathena-label-priorityhigh] | Falha que torna o rAthena instável ou inutilizável. |
| `priority:medium` | [search][search-rathena-label-prioritymedium] | Falha com impacto significativo, mas que não torna o rAthena inutilizável. |
| `priority:low` | [search][search-rathena-label-prioritylow] | Falha isolada que afeta apenas uma funcionalidade específica. |

#### Status

| Nome do Rótulo | Link de Busca | Descrição |
| --- | --- | --- |
| `status:code-review` | [search][search-rathena-label-statuscodereview] | Pull Request que precisa de revisão antes de ser integrado ao master. |
| `status:confirmed` | [search][search-rathena-label-statusconfirmed] | Issue confirmada por um desenvolvedor como um problema real. |
| `status:duplicate` | [search][search-rathena-label-statusduplicate] | Issue já reportada anteriormente. |
| `status:inprogress` | [search][search-rathena-label-statusinprogress] | Issue que já está sendo trabalhada por um desenvolvedor. |
| `status:invalid` | [search][search-rathena-label-statusinvalid] | Issue não oficial ou não relacionada ao rAthena. |
| `status:need more info` | [search][search-rathena-label-statusneedmoreinfo] | Issue que precisa de mais informações de uma fonte confiável. |
| `status:need user input` | [search][search-rathena-label-statusneeduserinput] | Issue que precisa de mais informações do autor. |
| `status:outdated emulator` | [search][search-rathena-label-statusoutdatedemulator] | Issue que exige atualização dos arquivos locais do autor. |
| `status:unable to reproduce` | [search][search-rathena-label-statusunabletoreproduce] | Issue que não pôde ser reproduzida. |
| `status:wontfix` | [search][search-rathena-label-statuswontfix] | Issue que não será corrigida por limitação ou comportamento intencional. |

#### Tipo

| Nome do Rótulo | Link de Busca | Descrição |
| --- | --- | --- |
| `type:bug` | [search][search-rathena-label-typebug] | Issue que representa um bug no rAthena. |
| `type:enhancement` | [search][search-rathena-label-typeenhancement] | Issue que representa uma melhoria no rAthena. |
| `type:maintenance` | [search][search-rathena-label-typemaintenance] | Issue relacionada à refatoração do rAthena. |
| `type:question` | [search][search-rathena-label-typequestion] | Issue que representa uma pergunta sobre o rAthena. |

[search-rathena-label-componentcore]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Acomponent%3Acore
[search-rathena-label-componentdatabase]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Acomponent%3Adatabase
[search-rathena-label-componentdocumentation]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Acomponent%3Adocumentation
[search-rathena-label-componentscript]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Acomponent%3Ascript
[search-rathena-label-componentskill]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Acomponent%3Askill
[search-rathena-label-componenttool]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Acomponent%3Atool
[search-rathena-label-missingclientdate]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Amissing%3Aclientdate
[search-rathena-label-missingmode]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Amissing%3Amode
[search-rathena-label-missingrevision]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Amissing%3Arevision
[search-rathena-label-modeprerenewal]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Amode%3Aprerenewal
[search-rathena-label-moderenewal]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Amode%3Arenewal
[search-rathena-label-priorityhigh]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Apriority%3Ahigh
[search-rathena-label-prioritymedium]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Apriority%3Amedium
[search-rathena-label-prioritylow]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Apriority%3Alow
[search-rathena-label-statuscodereview]: https://github.com/rathena/rathena/pulls?q=is%3Apr+is%3Aopen+label%3Astatus%3Acode-review
[search-rathena-label-statusconfirmed]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Astatus%3Aconfirmed
[search-rathena-label-statusduplicate]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Astatus%3Aduplicate
[search-rathena-label-statusinprogress]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Astatus%3Ainprogress
[search-rathena-label-statusinvalid]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Astatus%3Ainvalid
[search-rathena-label-statusneedmoreinfo]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3A"status%3Aneed+more+info"
[search-rathena-label-statusneeduserinput]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3A"status%3Aneed+user+input"
[search-rathena-label-statusoutdatedemulator]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3A"status%3Aoutdated+emulator"
[search-rathena-label-statusunabletoreproduce]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3A"status%3Aunable+to+reproduce"
[search-rathena-label-statuswontfix]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Astatus%3Awontfix
[search-rathena-label-typebug]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Atype%3Abug
[search-rathena-label-typeenhancement]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Atype%3Aenhancement
[search-rathena-label-typemaintenance]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Atype%3Amaintenance
[search-rathena-label-typequestion]: https://github.com/rathena/rathena/issues?q=is%3Aissue+is%3Aopen+label%3Atype%3Aquestion

Ambiente de Desenvolvimento Local
---------------------------------

Os desenvolvedores podem iniciar rapidamente utilizando um ambiente de desenvolvimento com Docker, que instala todas as dependências necessárias para executar e desenvolver no rAthena.  
Consulte a documentação do Docker para mais detalhes:

https://github.com/rathena/rathena/blob/master/tools/docker/README.md


Torne-se um Membro da Equipe
---------------------------

1. Antes de enviar uma candidatura para a equipe, certifique-se de que possui uma conta no rAthena:  
   https://rathena.org/board/register/
    * Se você é novo na comunidade, apresente-se aqui:  
      https://rathena.org/board/forum/89-introductions/
2. Preencha a [Aplicação para Staff](https://rathena.org/board/staffapplications/) e você será notificado em breve.

A equipe do rAthena é composta inteiramente por voluntários ([AUTHORS](https://github.com/rathena/rathena/blob/master/AUTHORS)).  
Incentivamos todos a contribuir enviando relatórios de bugs ou Pull Requests!

Obrigado!

Equipe rAthena
