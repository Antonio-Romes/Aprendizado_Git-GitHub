#Git - guia prático

## O que é git ?
- E um sistema de controle de versão de código livre, além de ser utilizado para rastrear modificações dos arquivos ao longo do tempo. Ele ajudar a coordenar trabalho em várias pessoas mantendo um histórico detalhado das alterações.

###Algumas característica
- __Repositório__
  - É o local onde é salvo os dados do projeto. O local pode ser local (no computador ) ou remoto (github, gitLab e etc).
- __Clone__
  - Criar uma cópia de um repositório que exite. Pode ser repositório local ou remoto.

- __Commit__
  - Representa uma alteração no seu projeto. Cada alteração feita possui um identificador único e um conjunto de informações associadas.
- __Branch__
  - É uma ramificação do projeto, que é utilizada para desenvolver funcionalidade isolada sem afetar a branch principal.

- __Merge__
  - São a combinação de diferente branch, normalmente é usado para unir as branch de desenvolvimento com a branch principal.

## O git serve para
* __Controla versões__
  - Controlar versão do projeto, rastrear mudança nos arquivos ao longo do tempo e identificar que fez as alterações, quando foi feita e qual alteração foi feita.

### Algumas das principais finalidades e benefícios do Git

*  __Controle de versão__
    - Permite que seja mantido um histórico completo de todas as alterações feitas no projeto. Cada alteração e registrada através do commit, que criar uma trilha clara das evoluções do projeto.

* __Coloboração__
  - Facilita o trabalho entre equipe. Cada pessoa da equipe pode criar uma cópia do projeto, realizar as alterações necessárias e mescla no projeto principal.

* __Branch e Merge__
  - Com a criação de branch é possível trabalhar em funcionalidade nova ou correção de bug sem afetar a branch principal. O merge é a combinação das branch, ou seja, é a mesclagem da branch de desenvolvimento com a branch principal.

* __Rastreamento de Mudanças__
  - Git fornecer informações detalhadas do projeto, com isso é possível saber que fez a alteração e por quê. A cada commit é associada uma mensagem descritiva, fornecendo informações das alterações feitas. Isso facilitar o entendimento do projeto para correção de problema no projeto.

* __sfazer Alterações__
  - Permiter reverte para uma versão anterior do projeto. Isso é util quando precisamos corrigir erro ou lidar com mudanças indesejadas.

* __Integração Contínua__
  - Com automação de fluxo de trabalho utilizando as ferramentas com GitHub Actions ou Jenkins podemos integrar automação de tarefa com teste, compilação e implantação continua.

* __Backup e Distribuição__
  - O git permite que seja hospedado os repositórios em servidor remoto, facilitando o backup e a distribuição do projeto.
 
## Com funciona o git ?

- O git funciona armazenando todos os históricos de alteração de um projeto em uma estrutura de árvore de diretório. Esta estrutura de árvore de diretório organiza os arquivos e pasta do projeto. A cada nó da árvore de diretório representa um commit que são as alterações feitas no projeto.
O git também armazenar histórico de todas as alterações feitas no projeto. Este historio e chamado de log de commits. O log permite visualizar todas as alterações feitas no projeto ao longo do tempo.

## Inciando um repositorio git