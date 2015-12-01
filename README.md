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