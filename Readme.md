# Git - guia prático

## O que é git ?
- E um sistema de controle de versão de código livre, além de ser utilizado para rastrear modificações dos arquivos ao longo do tempo. Ele ajudar a coordenar trabalho em várias pessoas mantendo um histórico detalhado das alterações.

### Algumas característica
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

* __Desfazer Alterações__
  - Permiter reverte para uma versão anterior do projeto. Isso é util quando precisamos corrigir erro ou lidar com mudanças indesejadas.

* __Integração Contínua__
  - Com automação de fluxo de trabalho utilizando as ferramentas com GitHub Actions ou Jenkins podemos integrar automação de tarefa com teste, compilação e implantação continua.

* __Backup e Distribuição__
  - O git permite que seja hospedado os repositórios em servidor remoto, facilitando o backup e a distribuição do projeto.
 
## Com funciona o git ?

- O git funciona armazenando todos os históricos de alteração de um projeto em uma estrutura de árvore de diretório. Esta estrutura de árvore de diretório organiza os arquivos e pasta do projeto. A cada nó da árvore de diretório representa um commit que são as alterações feitas no projeto.
- O git também armazenar histórico de todas as alterações feitas no projeto. Este historio e chamado de log de commits. O log permite visualizar todas as alterações feitas no projeto ao longo do tempo.

## Fluxo de trabalho do git
-  No repositório local exitem três arvore mantida pelo git.
A primeira é a Working Diretory que contém os arquivos vigentes, na segunda é a índex que funciona como uma área temporária e a terceira é o head que aponta para o último commit que você fez. 
![This is an alt text.](/img/fluxoTrabalhoGit.PNG "This is a sample image.")

## Instalação do Git
- Precisamos instalar o git no nosso computador, abaixo segue o link para baixar e instalar.
  - [Baixe o git para OSX](https://git-scm.com/download/mac).
  - [Baixe o git para Windows](https://gitforwindows.org/).
  - [Baixe o git para Linux](https://git-scm.com/download/linux).

 
 ## Ajuda
 - Geral
    ```
      git help
    ```
- Comando específico
  ```
    git help add
    git help commit
    git help <qualquer_comando_git>
    ```

## Configuração
- Geral
  - As configurações do git são armazenads no arquivo .gitconfig localizado dentro do diretório do usuário do sistema.

- Seta usuário
    ``` 
    git config --global user.name "Nome do usuário"
    ```

- Setar email
    ``` 
    git config --global user.email EmaildoUsuario@gmail.com
    ```

- Setar arquivos a serem ignorados
    ``` 
    git config --global core.excludesfile ~/.gitignore
    ```

- Listar configurações
    ``` 
    git config --list
    ```

## Criando um novo repositório Local 
  - Primeiro precisamos criar uma pasta no computador, com o nome desejado. Depois precisamos abrir o prompt de comando (CMD) e navegar até a pasta criada e inicializar a pasta com repositório, para isso utilizamo o comando:
    ``` 
    git init
    ``` 

  ## Obtenha um repositório
  #### Local
  - Fazer clone do repositório local
    ``` 
    git clone /caminho/para/o/repositório
    ```

 - Fazer clone do repositório remoto
    - Temos duas forma de clonar um repositório remoto, que é por HTTPS e SSH. 
        ``` 
      git clone URL do repositório remoto
        ```

- Verificar se um repositório local esta vinculado ao remoto.
    ``` 
    git remote -v 
    ``` 

- Vincular repositório local ao remoto.
    ``` 
     git remote add origin "url do gitHub"
    ```

## Salvando alterações no repositório local
- Verificar o estado dos arquivos
    ``` 
    git status
    ``` 
#### adicionado os arquivos ao estado (index, stage) 
  - Podemos adicionar arquivo ou diretório especifíco
    ``` 
    git add nomeDoArquivo ou nomeDoDiretorio
    ``` 
 
  - Podemos adicionar todos os arquivo ou diretório
    ``` 
    git add .
    ``` 

#### Realizar commit
- Comitar informando mensagem 
    ``` 
    git commit -m "comentários das alterações"
    ```

#### Pasta vazia
- Quando são criados pasta e não é adicionada nenhum arquivo, ao verificar os status do arquivo, a pasta vazia não é visualizada, porque, o git status não consegue ver a pasta vazia.
Para que possamos criar uma pasta vazia e o git status consiga ver, precisamo criar um arquivo .gitkeep
 
 #### Ignorar pasta e arquivo
  - Para que o git ignore arquivo ou pasta quando for enviar o projeto para o servidor remoto, basta adiciona os mesmo na pasta .gitignore

#### Visualizar histórico
 - 
    ``` 
    git log
    ```

#### Desfazendo alterações no repositório local.
- Inicializa pasta errada
  - Quando inicializamos uma paste que deveria, precisamos apenas excluir a pasta git.

#### Restaura arquivo que estão no estado (index/stage)
- Quando for feita alteração em um arquivo que não queremos, podemos voltar ao status anterior
-  Tenha muita atenção ao usar o comando git restore, por que, este comando desfaz toda alteração que já foram feitas localmente.
    ``` 
    git restore "nome do arquivo"
    ``` 
  
#### Alterar mensagem do último commint ?
- 
    ``` 
    git commit --amend -m"nova mensagem"
    ``` 
 
 ## Desfazer o último commit.
- Git reset
  - O git reset é utilizado para desfaz as alterações que estão no índice do git, mas não altera os arquivos na árvore de trabalho. Os arquivos ainda estão nos arquivos, mas não serão rastreados pelo git.
  - O git reset possui 3 forma de ser usado, que correspondem aos argumentos soft, mixed e hard.
	 - soft
      O git soft restaura o estado do head para um commit especifico, mas não altera os arquivos na árvore de trabalho. Isso restaurará o estado do HEAD para o commit anterior
       ``` 
       git reset --soft HEAD~1      
    - mixed
      O mixed restaura o estado do HEAD para o commit especificado e, em seguida, mescla as alterações feitas após o commit especificado nos arquivos na árvore de trabalho. Isso restaurará o estado do HEAD para o commit anterior. No entanto, os arquivos na árvore de trabalho terão as alterações feitas após o commit especificado, mas apenas as alterações que ainda não foram commitadas.
      ``` 
       git reset --mixed HEAD~1
    - hard
    O hard restaura o estado do HEAD para o commit especificado e, em seguida, remove todas as alterações feitas após o commit especificado dos arquivos na árvore de trabalho.Isso restaurará o estado do HEAD para o commit anterior. No entanto, os arquivos na árvore de trabalho serão revertidos para o estado que eles tinham no commit especificado.
      ````
        git reset --hard HEAD~1 
      ````

## Conectar com o repositório remoto
  -
      ````
        git remote add origin "Nome do repositorio remoto" 
      ````