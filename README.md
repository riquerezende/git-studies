# Estudando Git
## Aprendendo Git com linha de comando
## Ferramentas utilizadas
- [Git](https://git-scm.com/ "Git")
- [Cmder](https://cmder.net/ "Cmder")

## Lista de comandos

`mkdir <nome-do-projeto>`

`cd <nome-do-projeto>`


`git init`

`touch <nome-do-arquivo>`

`git status`

`git add .`

`git add <nome-do-arquivo>`

`git commit -m "<mensagem-de-commit>"`

`git remote add origin <endereço-do-repositório-remoto>`

`git push -u origin master`

## Criando um repositório local 
Para criar um repositório git no computador, é necessário criar uma pasta para inicializar o git e colocar os nossos arquivos de código dentro dela. O código a seguir cria uma pasta com o nome projeto-git no computador.

`mkdir projeto-git`

Após criar a pasta, devemos entrar nela usando o comando:

`cd projeto-git`

Após entrar na pasta, inicializamos o repositório usando o comando:

`git init`

Após inicializar o repositório, criamos um arquivo README.md usando o comando:

`touch README.md`

Se digitarmos o comando `git status` nos será mostrado:

![](https://i.imgur.com/jTT9qgh.png)

Essa saída nos mostra que o arquivo README.md não está sendo rastreado (untracked) pelo git. Para rastrear arquivos devemos adicioná-los digitando o comando:

`git add .`

Esse comando adiciona todos os arquivos que não estão sendo rastreados. Nesse caso só existe um arquivo para adicionar. Se houvessem mais arquivos não rastreados, todos seriam adicionados usando esse comando. Se quisermos adicionar apenas um arquivo, devemos digitar o comando:

`git add README.md`

Após a adição do arquivo no git, vamos ver o que o comando `git status` nos retorna:

![](https://i.imgur.com/7g4bdym.png)

Podemos ver que o arquivo já foi adicionado e que as mudanças estão esperando commit. Para fazer commit executamos o seguinte comando:

`git commit -m "Adicionando arquivo README.md"`

A mensagem do commit deve mostrar de forma resumida quais mudanças ele representa. Nesse caso o commit representa a adição do arquivo README.md ao nosso repositório.

## Enviando o repositório local para um repositório remoto

O repositório está armazenado no computador, mas não está armazenado em um repositório remoto. Para adicioná-lo em um repositório remoto, necessitamos de uma conta em site como o GitHub. Após criar uma conta no GitHub e criar um repositório nele, é necessário pegar o link do repositório criado. Para concluir o processo, devemos executar o comando:

`git remote add origin https://github.com/riquerezende/git-studies.git`

Agora o repositório tem uma origem remota, mas o repositório local ainda não foi enviado para o GitHub. Para enviar os arquivos para o servidor remoto, devemos executar o comando:

`git push -u origin master`
