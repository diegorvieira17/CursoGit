# CursoGit

> Vamos aprender agora como criar um respositório remoto no GitHub assim como configurá-lo no nosso computador para que possamos enviar nossos arquivos git para o servidor remoto.

> Para isso basta seguir os passos abaixo:

>>+ Para criar o respositório no GitHub, acesse seu perfil, clique na aba "Repositories" - botão "New" - escolha o nome do seu respositório e, caso julgue necessário, informe uma breve descrição de seu repositório - botão "Create Repository".

> Feito isso, seu repositório está criado. Agora iremos criar nosso primeiro arquivo, criar nosso commit e enviar para o servidor.

>>+ Para criar um arquivo podemos utilizar o comando abaixo:
>>>* *echo "# teste" >> README.md*

>>+ Agora vamos iniciar o git em nosso diretório:
>>>* *git init*

>>+ Adicionando o arquivo ao controle do git:
>>>* *git add README-md*

>>+ Criando o primeiro commit:
>>>* *git commit -m "first commit"*

>>+ Configurando o endereço do servidor remoto:
>>>* *git remote add origin https://github.com/[seu_usuario]/[seu_repositorio]*

>>+ E pra finalizar, vamos enviar nosso arquivo para o servidor do GitHub com o comando abaixo:
>>>* *git push origin master*


# Principais comandos GIT e suas funções.

> Nesse tópico iremos conhecer os principais comandos do git assim como suas funções.

>>+ git config --global user.name [seu_nome] => Inclui nas configurações do git o nome do colaborador do repositório.
>>>* Ex.: *git config --global user.nome "Diego Vieira"*

>>+ git config --global user.email [seu_email] => Inclui nas configurações do git o email do colaborador do repositório.
>>>* Ex.: *git config --global user.email "diegorvieira17@gmail.com"*

>>+ git config --global collor.ui = true => Habilita cores nas interações do git (não funciona no cmd do windows).
>>>* Ex.: *git config --global collor.ui = true*

>>+ git init => Inicia o controle do git no diretório onde o comando foi digitado.
>>>* Ex.: *git init*

>>+ git status => Mostra o status de todos os arquivos que estão no diretório. São possíveis os seguintes tipos de status. Seguem eles abaixo:
>>>>- Untracked files => Arquivos que não estão sendo controlados pelo git.
>>>>- Changes not staged to be committed => Arquivos que foram modificados mas não foram adicionados a lista de commit.
>>>>- Changes to be committed => Arquivos que estão prontos para serem comitados.
>>>>- Nothing to be committed => Não existe nenhuma informação a ser commitada. Todos os arquivos estão de acordo com o último commit.
>>>* Ex.: *git config --global "Diego Vieira"*

>>+ git add => Adicona arquivos ao controle de versão e ao pacote para ser commitado.
>>>* Ex.: *git add arquivo.txt* (Obs.: Para adicionar todos os arquivos, pode-se usar *git add .*).

>>+ git commit => Cria o commit (snapshot) dos arquivos.
>>>* Ex.: *git commit -m "first commit"*
>>>* Ex.: *git commit -a*
>>>* Ex.: *git commit -a -m "first commit"*
>>>>- -m => indica que será adicionada uma mensagem para descrever as alterações do commit. Caso o parâmetro -m seja omitido, o git abrirá o editor de texto padrão da máquina com o arquivo de mensagem para que o usuário insira a descriçao do commit.
>>>>- -a => adiciona todos os arquivos untracked e not staged ao pacote de commit e faz o commit sem precisar realizar em duas etapas como o git add e depois o git commit.

>>+ git log => Mostra todos os commits realizados no diretório.
>>>* Ex.: *git log*
>>>* Ex.: *git log -p* (todos os commits)
>>>* Ex.: *git log -p -2* (apenas os 2 últimos commits)
>>>* Ex.: *git log --stat*
>>>* Ex.: *git log --pretty=oneline*
>>>* Ex.: *git log --pretty=format:"%h - %an, %ar : %s"*
>>>* Ex.: *git log --since=2.days*
>>>>- -p => Mostra detalhadamente todos os commits realizados.
>>>>- -p -2 => Igual -p porém mostra apenas os últimos 2 commits.
>>>>- --stat => Mostra todos as estatísticas resumidas de todos os commits.
>>>>- --pretty=oneline => Mostra em apenas uma linha as informações resumidas dos commits (mostra todos).
>>>>- --pretty=format => Mostra de forma semelhante ao oneline mas formatado de acordo com a sua necessidade.
>>>>>- %h => hash do commit.
>>>>>- %an => Nome do colaborador que criou o commit.
>>>>>- %ar => Quanto tempo atrás foi criado o commit.
>>>>>- %s => Mensagem do commit.
>>>>- --since => mostra todos os commits realizados nos últimos n dias. No caso do exemplo, nos últimos 2 dias.


# Como ignorar arquivos no controle de versão do GIT.

>As vezes existem alguns arquivos que estão dentro da pasta do projeto que não queremos que faça parte do controle de versão. Algumas vezes por serem arquivos sensíveis como por exemplo arquivos de configuração de bancos de dados onde temos todos os dados de acesso assim como quando temos arquivos gerados por exemplo por uma IDE que não contribuem em nada com o projeto.
>Para que esses arquivos não fiquem aparecendo sempre pra você como untracked files, podemos usar o recurso do GIT que permit ignorar arquivos listados no arquivo .gitignore. Abaixo veremos como isso funciona.

>>+ Antes de mais nada precisamos criar o arquivo .gitignore no diretório do projeto.
>>+ Feito isso, basta incluir os arquivos que você não quer que sejam versionados pelo GIT linha a linha. Simples assim.
>>>* Ex.: *conf.php*