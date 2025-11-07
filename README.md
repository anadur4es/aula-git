# 1. Introdução e Conceitos

#### P: Por que o Git é considerado um sistema de controle de versão distribuído?
R: Porque cada desenvolvedor possui uma cópia completa do repositório (com histórico e versões) em sua máquina, sem depender de um servidor central para operar.

#### P: Qual a diferença entre working directory, staging area e repository?
R: -Working directory: onde os arquivos são editados.  
-Staging area: onde ficam os arquivos prontos para serem confirmados (commit).  
-Repository: onde ficam armazenadas as versões confirmadas do projeto.

#### P: Para que serve o comando git clone?
R: Serve para copiar um repositório remoto completo (com histórico e arquivos) para a máquina local.

#### P: ​​Onde estão implementados fisicamente working directory, staging area e repository?
R: -Working directory: na pasta do projeto.  
-Staging area: dentro da pasta .git/index.  
-Repository: dentro da pasta .git/.

#### P: Quais os estados de um arquivo no repositório do Git?
R: Untracked, modified, staged e committed.

#### P: Explique as possíveis transições de estado de um arquivo no repositório do Git.
R: Um arquivo começa como untracked (não rastreado), pode ser editado (modified), depois adicionado à staging area (staged) e, ao fazer o commit, passa para o estado committed (salvo no repositório).

# 2. Prática Usando Git Local

## Etapa 1 – Criar o repositório
#### P: Qual foi a mensagem exibida após o comando git init e o que ela significa na prática?
R: A mensagem foi “Initialized empty Git repository in .../.git/”, indicando que um novo repositório Git vazio foi criado e inicializado na pasta .git, onde serão guardados todos os dados de controle de versão do projeto.

## Etapa 2 – Adicionar arquivo e fazer commit
#### P: Qual o estado do arquivo antes e depois do git add?
R: Antes era untracked (não rastreado), depois foi para staged (pronto para commit).

#### P: O que significa o estado untracked e tracked?
R: -Untracked: arquivo ainda não monitorado pelo Git.  
-Tracked: arquivo já monitorado e com histórico de mudanças.

#### P: Qual o objetivo do git commit?
R: Salvar as alterações da staging area no repositório, criando uma nova versão do projeto.

#### P: Qual o estado do arquivo após o git commit?
R: Committed (armazenado no repositório e sem modificações pendentes).

## Etapa 3 – Histórico e alterações
#### P: O que o comando git diff mostra?
R: Ele mostra as diferenças entre o conteúdo atual dos arquivos modificados e a última versão confirmada (commit).

#### P: Qual commit está atualmente apontado por HEAD?
R: O último commit realizado, ou seja, o commit mais recente no qual o repositório está baseado.

## Etapa 4 – Trabalhando com Branches
#### P: Como verificar em qual branch você está?
R: Usando o comando git branch, que lista todas as branches e marca com * a branch atual.

#### P: O que acontece se você rodar git merge nova-feature estando na branch principal?
R: As alterações feitas na branch nova-feature serão unidas (mescladas) à branch principal, integrando o trabalho das duas.

# 3. Conectando ao GitHub

#### P: O que significa o -u no comando git push -u origin main?
R: O -u define a branch remota como padrão, vinculando a branch local à remota para que futuros git push e git pull possam ser feitos sem precisar especificar o nome da origem e da branch.

# 4. Encerramento e Discussão


#### P: Como verificar os remotes configurados no repositório?
R: Usando o comando git remote -v, que lista os repositórios remotos associados e suas URLs.

#### P: Qual etapa foi mais difícil?
R: A parte de entender as transições entre working directory, staging area e repository, pois exige compreender bem o fluxo interno do Git.

#### P: Como o Git ajuda na colaboração?
R: Permite que várias pessoas trabalhem no mesmo projeto ao mesmo tempo, mantendo histórico de versões e facilitando o controle e a integração das mudanças.

#### P: Que diferença faz ter um repositório remoto?
R: O repositório remoto centraliza o código na nuvem, permitindo backup, acesso de qualquer lugar e colaboração entre desenvolvedores.
