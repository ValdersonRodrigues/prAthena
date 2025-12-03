# Contribuindo para o rAthena

Tabela de Conteúdos
-------------------

  * [Reportando Bugs](#reportando-bugs)
  * [Sugerindo Melhorias](#sugerindo-melhorias)
  * [Rótulos de Issues](#rótulos-de-issues)
  * [Ambiente de Desenvolvimento Local](#ambiente-de-desenvolvimento-local)
  * [Torne-se um Membro da Equipe](#torne-se-um-membro-da-equipe)

Reportando Bugs
----------------

Este conjunto de informações existe para guiá-lo durante o processo de criação de um relatório de bug para o rAthena! Issues não servem apenas para desenvolvedores rastrearem bugs — elas também rastreiam melhorias e tarefas. Quanto mais detalhado for seu relatório, mais fácil será para os desenvolvedores reproduzirem e resolverem o bug!

### Você encontrou um bug? :bug:

* **Garanta que o bug não esteja vindo de uma customização** em seus arquivos!
* **Garanta que o bug ainda não foi relatado**, buscando no GitHub em [Issues](https://github.com/rathena/rathena/issues).  
  Se a mesma issue já existir, sinta-se livre para comentar dizendo que você também está enfrentando o problema e, se possível, adicionar informações adicionais ou faltantes!
* Se você não conseguir encontrar uma issue aberta que trate do problema, [abra uma nova](#submit-a-bug-report)!

#### Enviar um Relatório de Bug :inbox_tray:

Existem várias coisas que tornam um bom relatório de bug!

Aqui está a estrutura geral de uma Issue:

* **Título** deve fornecer uma ideia geral sobre o que o bug trata.
* **Descrição** deve dar mais detalhes sobre o bug que não podem ser explicados apenas no **Título**.
* **Labels (Rótulos)** são coloridos para representar a categoria a que pertencem.
* **Milestones** são usados pelos desenvolvedores para agrupar tarefas e avaliar o quão perto o projeto está da conclusão.
* **Assignees** são desenvolvedores diretamente associados à resolução da issue.
* **Comentários** permitem que outros membros deem feedback sobre a issue.

#### Quais são alguns bons detalhes para fornecer em um relatório de bug? :pencil2:

Ao descrever seu problema na área de **Descrição**, recomenda-se fornecer o máximo de informações possível, para permitir uma resolução mais rápida.  
Lembre-se de que você pode marcar pessoas na **Descrição** usando o recurso `@mention`.  
Também é possível marcar outras Issues ou Pull Requests digitando `#`, que exibirá uma lista de issues.  
Você pode encontrar um guia de markdown em [Mastering Markdown](https://guides.github.com/features/mastering-markdown/).

Informações importantes para incluir ao criar uma Issue:

* **GitHub Hash**: Hash é uma string alfanumérica de 40 caracteres (pode ser reduzida para os 7 primeiros) indicando a versão em que você está.  
  (**Se estiver usando SVN em vez de Git:** forneça a data da alteração e a primeira linha da mensagem do commit ao lado do número da revisão, ou não poderemos encontrar o hash correspondente.)
* **Data do Cliente**: Ajuda a identificar problemas relacionados a pacotes.
* **Modificações que possam afetar os resultados**: Sempre teste sua issue em um rAthena limpo se você tiver muitas modificações.
* **Descrição do Problema**: Detalhe tudo! Capturas de tela e vídeos ajudam muito! Inclua também crash dumps se algum servidor estiver caindo.
* **Como Reproduzir o Problema**: Descreva o passo a passo! Quanto mais detalhado, melhor!
* **Informações Oficiais**: Forneça fontes confiáveis para provar que é um bug.  
  *Evite links do iRO Wiki, pois muitas vezes não representam o comportamento oficial do kRO.*

#### Tome cuidado com o recurso `@mention`! :warning:

Como o rAthena utiliza comandos `@comandos` personalizados, ao descrever uma issue envolvendo esses comandos, lembre-se de que isso pode conflitar com o sistema de menções do GitHub!  
Sempre coloque o texto entre crases ao mencionar um ``` `@comando` ``` (como isso), para evitar marcar usuários do GitHub por engano!

Sugerindo Melhorias
-------------------

### Você escreveu um patch que corrige um bug? :bookmark_tabs:

* Abra um novo Pull Request no GitHub com o patch.
* Certifique-se de que a descrição do PR descreva claramente o problema e a solução.  
  Inclua o número da issue relacionada, se aplicável.

### Você deseja adicionar um novo recurso ou alterar um já existente? :bulb:

* Abra um novo Pull Request no GitHub com a adição ou mudança.
* Certifique-se de que a descrição do PR explique claramente o propósito da mudança.  
  Inclua o número da issue relacionada, se existir.

#### Como criar Pull Requests :pencil:

1. Certifique-se de ter uma [conta no GitHub](https://github.com/signup/free).
2. Depois, você precisará [fazer um fork do rAthena](https://help.github.com/articles/fork-a-repo/#fork-an-example-repository).
3. Antes de fazer mudanças, [crie um novo branch](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/).  
   Nunca use o branch **master**! :bangbang:
4. Após concluir suas alterações, faça commit e push para seu branch.
5. Agora você está pronto para [criar um Pull Request](https://help.github.com/articles/creating-a-pull-request/) para o rAthena!
   * Ao criar o Pull Request, lembre-se de seguir o nosso [template](https://github.com/rathena/rathena/blob/master/.github/PULL_REQUEST_TEMPLATE.md).
   * **Opcional:** Agradecemos quem marca a opção para [permitir edições por mantenedores](https://help.github.com/articles/allowing-changes-to-a-pull-request-branch-created-from-a-fork/).  
     Isso facilita pequenos ajustes antes do merge!

Rótulos de Issues
-----------------

Na maioria das vezes, como usuário você não precisará se preocupar com **Milestones** ou **Assignees**.  
Os diferentes **Labels** ajudam os desenvolvedores a entender rapidamente cada issue e auxiliam buscas e organização.

:bangbang: Usuários devem prestar atenção aos Labels de **Mode** (Modo) e **Status**, pois eles às vezes exigem feedback! :bangbang:

#### Componente

| Nome do Rótulo | Link de Busca | Descrição |
| --- | --- | --- |
| `component:core` | [search][search-rathena-label-componentcore] | Falha que está no framework principal do rAthena. |
| `component:database` | [search][search-rathena-label-componentdatabase] | Falha que está no banco de dados do rAthena. |
| `component:documentation` | [search][search-rathena-label-componentdocumentation] | Falha encontrada na documentação do rAthena. |
| `component:script` | [search][search-rathena-label-componentscript] | Falha nos scripts do rAthena. |
| `component:skill` | [search][search-rathena-label-componentskill] | Falha relacionada especificamente a uma skill. |
| `component:tool` | [search][search-rathena-label-componenttool] | Falha em alguma ferramenta do rAthena. |

#### Missing (Faltando)

| Nome do Rótulo | Link de Busca | Descrição |
| --- | --- | --- |
| `missing:clientdate` | [search][search-rathena-label-missingclientdate] | Título ou descrição não informa a data do cliente usado no bug. |
| `missing:mode` | [search][search-rathena-label-missingmode] | Título ou descrição não informa se é pre-renewal ou renewal. |
| `missing:revision` | [search][search-rathena-label-missingrevision] | Descrição não informa a revisão do rAthena usada quando o bug ocorreu. |

#### Mode (Modo)

| Nome do Rótulo | Link de Busca | Descrição |
| --- | --- | --- |
| `mode:prerenewal` | [search][search-rathena-label-modeprerenewal] | Falha existente no modo pre-renewal. |
| `mode:renewal` | [search][search-rathena-label-moderenewal] | Falha existente no modo renewal. |

#### Priority (Prioridade)

| Nome do Rótulo | Link de Busca | Descrição |
| --- | --- | --- |
| `priority:high` | [search][search-rathena-label-priorityhigh] | Falha que torna o rAthena instável ou inutilizável. |
| `priority:medium` | [search][search-rathena-label-prioritymedium] | Falha com impactos significativos, mas não torna o rAthena inutilizável. |
| `priority:low` | [search][search-rathena-label-prioritylow] | Falha localizada em uma funcionalidade específica. |

#### Status

| Nome do Rótulo | Link de Busca | Descrição |
| --- | --- | --- |
| `status:code-review` | [search][search-rathena-label-statuscodereview] | PR que precisa ser revisado antes do merge. |
| `status:confirmed` | [search][search-rathena-label-statusconfirmed] | Issue confirmada por um desenvolvedor. |
| `status:duplicate` | [search][search-rathena-label-statusduplicate] | Issue já relatada anteriormente. |
| `status:inprogress` | [search][search-rathena-label-statusinprogress] | Issue que já está sendo trabalhada. |
| `status:invalid` | [search][search-rathena-label-statusinvalid] | Issue que não é oficial ou não está relacionada ao rAthena. |
| `status:need more info` | [search][search-rathena-label-statusneedmoreinfo] | É necessário mais informação de fontes confiáveis. |
| `status:need user input` | [search][search-rathena-label-statusneeduserinput] | É necessário mais informação do criador da issue. |
| `status:outdated emulator` | [search][search-rathena-label-statusoutdatedemulator] | Criador precisa atualizar os arquivos locais. |
| `status:unable to reproduce` | [search][search-rathena-label-statusunabletoreproduce] | Não foi possível reproduzir o problema no rAthena. |
| `status:wontfix` | [search][search-rathena-label-statuswontfix] | Problema não pode ser corrigido ou é comportamento pretendido. |

#### Type (Tipo)

| Nome do Rótulo | Link de Busca | Descrição |
| --- | --- | --- |
| `type:bug` | [search][search-rathena-label-typebug] | Issue que é um bug no rAthena. |
| `type:enhancement` | [search][search-rathena-label-typeenhancement] | Issue que é uma melhoria para o rAthena. |
| `type:maintenance` | [search][search-rathena-label-typemaintenance] | Issue destinada à refatoração. |
| `type:question` | [search][search-rathena-label-typequestion] | Issue que é uma pergunta sobre o rAthena. |

(As URLs foram mantidas exatamente como no original.)

Ambiente de Desenvolvimento Local
---------------------------------

Desenvolvedores podem iniciar rapidamente com um ambiente Docker que instala todas as dependências necessárias para rodar e desenvolver no rAthena.  
Veja a [documentação do Docker](https://github.com/rathena/rathena/blob/master/tools/docker/README.md) para mais detalhes.

Torne-se um Membro da Equipe
----------------------------

1. Antes de enviar uma aplicação para a equipe, certifique-se de ter uma [conta no rAthena](https://rathena.org/board/register/).
    * Se você é novo na comunidade, aproveite para [se apresentar](https://rathena.org/board/forum/89-introductions/)!
2. Preencha o formulário de [Aplicação para Staff](https://rathena.org/board/staffapplications/) e você será notificado em breve.

A equipe do rAthena é composta inteiramente por voluntários ([AUTHORS](https://github.com/rathena/rathena/blob/master/AUTHORS)).  
Nós encorajamos você a contribuir enviando relatórios de bugs ou Pull Requests!

Obrigado!

Equipe rAthena
