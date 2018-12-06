# Trilha sobre Git 

<p align="center">
  <a href="https://git-scm.com/"><img src="img/logo-git.png" height="200" width="200"></a>
 
</p>

**Git** é um sistema de controle de versão de arquivos, com ele podemos desenvolver projetos e compartilhar nossos códigos com diversas pessoas, mantendo o histórico das alterações.

## Instalação
**Windows**
  - Donwload da última versão disponível [aqui](https://gitforwindows.org/).
  - A instalação é simples, padrão em todas as instalações na plataforma **Windows**.
  - A instalação vem com o **Git Bash**, que permite que seja executado linhas de comandos do **Git no Windows**.
  
**Mac**
  - Download da última versão disponível [aqui](https://git-scm.com/download/mac).
  - Utiliza o terminal padrão do **Mac**.

**Linux**
- Distribuições baseadas em **Debian**, execute o comando em seu terminal:
  ```bash
    $ sudo apt-get install git
  ```
- [Donwload para outras distribuições Linux](http://git-scm.com/download/linux)
- Utiliza o terminal padrão do **Linux**.

## Configuração inicial

- É preciso informar para o **Git**, seu **nome** e **e-mail**, execute o comando em seu terminal:
```git
$ git config --global user.name "MEU NOME"
$ git config --global user.email "MEU E-MAIL"
```
- Verificando qual **nome** está configurado no **Git**, execute o comando em seu terminal:
```git
$ git config --global user.name
```
- Verificando qual **e-mail** está configurado no **Git**, execute o comando em seu terminal:
```git
$ git config --global user.email
```

## Criando um repositório Local
- Iniciando o **Git** em um diretório já existente, transformando em um repositório, execute o comando em seu terminal:
```git
$ git init
```
- Iniciando o **Git** em um diretório que não existe, execute o comando em seu terminal:
```gitProtocolos suportados pelo Git
$ git init nome-diretorio
```
- Confirmação de sucesso da criação do repositório deve retornar uma mensagem dessa forma:
```git
Initialized empty Git repository in CAMINHO RAIZ DE ONDE FOI EXECUTADO O git init
```
- Essa mensagem informa que foi inicializado um repositório **Git** vazio.
  
## Verificando alterações
  - Verificando as situações dos arquivos no repositório, execute o comando em seu terminal:
```git
$ git status
```
  - **git status** informa em uma lista, caso tenha alterado, adicionado ou removido um arquivo. 
  
## Adicionando o arquivo no rastreamento 
  - Adicionando o arquivo no rastreamento e preparando ele para commitar, execute o comando em seu terminal:
```git
$ git add nome-do-arquivo-alterado
```
  - Temos o **git add .** ele permite rastrear todos os arquivos modificados e prepará-los para commitar.
  
## Gravando e criando um commit
  - Para criar um commit e gravar as mudanças no repositório, execute o comando em seu terminal:
```git
$ git commit -m "Aqui vai a explicação da sua alteração"
```
  
## Boas praticas para escrever um commit
  - Deve-se comitar uma funcionalidade por vez, facilita a reverter uma mudança em caso de problemas.
  - Informe uma explicação em alto nível com poucas palavras do que foi feito.
  - Não faça grandes explicações em comentários de commits.
  - Sempre vincule cada commit a um **issue**.

## Verificando alterações, log de commits
  - Para ver o **log** das alterações no repositório, execute o comando em seu terminal:
```git
$ git log
```
  - Limitando a visualização de **logs**, mostrando os ultimos dois commits, execute o comando em seu terminal:

```git
$ git log -n 2   git clone file:// url-do-repositorio 
```
  - Trazendo um resumo reduzido dos commits, execute o comando em seu terminal:
```git
$ git log --oneline
```
- Mostrando resumo dos arquivos com o número de linhas adicionadas e removidas, execute o comando em seu terminal:
```git
$ git log --stat
```

## Configurando um repositório remoto
  - Para adicionar um repositório remoto, execute o comando em seu terminal: 
```git
$ git remote add origin https://caminho-do-repositorio-remoto
```

## Enviando as alterações pro repositório remoto
 - Enviando os commits pro repositório remoto, execute o comando em seu terminal: 
```git
$ git push origin master 
```

## Obtendo um repositório já existente
  - Para obter o código do repositório desejado, execute o comando em seu terminal:
```git
$ git clone https://caminho-do-repositorio
```
  - Pode ser **http**, **https** e **ssh**.
  
## Ignorar arquivos
  - Caso não queira comitar certos arquivos toda git remote add servidor
file://192.168.1.1/opt/repositorios/moveis-ecologicos.gitvez, basta criarmos um arquivo chamdo .gitignore no diretório principal e colocar os nomes de arquivos e pastas dentro do mesmo.
  - [Exemplos de .gitignore](https://github.com/github/gitignore)

## git add & git commit 
  - Podemos fazer **git add** com **git commit** em apenas um comando dessa forma:
```git
$ git commit -a -m "Descrição do commit"
```
ou execute o comando em seu terminal: 
```git
$ git commit -am "Descrição do commit"
```

## Verificando alterações
$ git remote -v
- Conseguimos ver as alterações feitas com o comando:
```git
$ git diff
```$ git remote -v
- Apenas em programas que não foram rastreados através do **git add**.
  
- Mostrando diferença dos arquivos na área de stage e a última versão de commit do arquivo:
```git
$ git diff -staged
```
- É possível ver o **diff** do commit pelo seu código, conforme exemplo:
```git
$ git diff 123abcd..848998
```
- Os dois pontos (..) significa do commit inicial no caso **123abcd** até o commit **848998**.

- Mostrando as mudanças do commit 123abcd em relação aos dois commits anteriores
```git
$ git diff 123abcd~2
```

## Removendo um arquivo
- Removendo um arquivo pelo git, pelo comando:
```git
$ git rm nome-do-arquivo
```
- Essa ação remove por completo o arquivo.
 execute o comando em seu terminal: 
## Renomeando um arquivo
- É possível renomear um arquivo dessa forma:
```git
$ git mv nome-arquivo-atual.js nome-do-novo-arquivo.js
```
## Movendo um arquivo
- É possível mover um arquivo dessa forma:
```git
$ git mv meu-arquivo.js js/meu-arquivo.js
```
## Desfazendo mudanças
- É possível desfazer dessa forma:
```git
$ git checkout -- index.html
```
- O comando git checkout desfaz as alterações ainda não adicionas ao stage.

## Removendo arquivo do stage
- Podemos apenas remover da área de stege, mantendo as alterações no arquivo dessa forma:
- É possível desfazer dessa forma:
```git
$ git reset -- app.js
```
## Removendo arquivo do stage e as alterações
- Podemos remover os arquivos da área de stage e desfazer as alterações dessa forma: execute o comando em seu terminal: 
```git
$ git reset --hard
```
## Desfazendo mudanças já comitadas
- Podemos desfazer mudanças já commitadas dessa forma:
```git
$ git revert --no-edit codigo-do-commit
```
- O comando **--no-edit** diz para não abrir um editor de texto para modificar a mensagem do novo commit.
- Caso não queira passar o código do commit, podemos usar o **HEAD**, apontando para o último commit.

## Voltando a commits anteriores
- Podemos voltar a commits anteriores dessa forma:
```git
$ git reset --hard 1158799
```
- Dessa forma é descartado os commits.

## Criando um repositório remoto

- Para criar um repositório remoto devemos usar o comando **git init**, porém passando o parâmetro **--bare**, dessa forma:
```git 
$ git init --bare nome-projeto.git
```
- O parâmetro **--bare** serve para informar ao Git que não deve criar um **working tree** (diretório de trabalho), impedindo que commits sejam efetuados diretamente no servidor.

## Adicionando o repositório remoto
- Para enviar os commits realizado no respositório local para o repositório remoto, precisamos indicar ao Git onde está localizado o repositório remoto.

- Podemos utilizar o comando **$ git remote add** passando o endereço do repositório remoto.
```git
$ git remote add nome-repositorio-remoto nome-da-url
```
  Outro exemplo:
```git
$ git remote add meu-app file://192.168.1.1/opt/repositorios/meu-app.git
```
## Listando repositórios remotos
- Para mostrar todos os repositórios remotos adicionados, podemos usar o comando:
```git
$ git remote
```
- Para mostrar a **url** devemos adicionar o parâmetro **-v**, dessa forma:
```git
$ git remote -v
```
## Alterando o nome do repositório remoto
- Podemos alterar o nome do repositório dessa forma: 
```git
$ git remote rename nome-atual novo-nome
```
## Alterando a URL do repositório remoto
- Podemos alterar a URL do repositório dessa forma:
```git execute o comando em seu terminal: 
$ git remote set-url nome-repositorio url-nova
```
## Enviando commits ao repositório remoto
- Para enviar os commits feito no repositório local para o remoto, podemos usar o comando:
```git execute o comando em seu terminal: 
$ git push nome-repositorio nome-branch
```
## Clonando o repositório remoto
- Para clonar um repositório remoto, podemos fazer dessa forma:
```git
$ git clone file://192.168.1.1/opt/repositorios/meu-projeto.git
```
## Sincronizando o repositório local
- Para sincronizar o repositório local com o servidor podemos utilizar o comando **git pull**, execute o comando em seu terminal:
```git
$ git pull servidor master
```
## Protocolos suportados pelo Git
- O Git suporta quatro protocolos para comunicação e transferência de dados:
  - **Protocolo local**
    - Pode ser usando caso o remoto está no mesmo computador ou em outro computador que esteja conectado na mesma rede.
    - Necessita usar o prefixo **file://** na URL ao ser clonado.
      ```git
      $ git clone file:// url-do-repositorio
      ```
    - Podemos omitir o **file://** na url, informando apenas o caminho do repositório.
      ```git
      $ git clone url-do-repositorio
      ```
  - **SSH**
    - O uso do protocolo SSH é feito com a URL seguindo o padrão **usuario@servidor:/caminho/repositorio.git**
      ```git
      $ git clone root@192.168.1.1:/opt/repositorios/meu-projeto.git
      ```
  - **Git**
    - Git possui um protocolo próprio, similar ao SSH, não contém autenticação, e sendo apenas leitura.
    - Para clonar um repositório utlizando o protocolo, usamos o prefixo **git://:**
      ```git
      $ git clone git://192.168.1.1/opt/repositorios/meu-projeto.git
      ```
  - **HTTP/HTTPS**
    - Para clonar um repositório utilizando o protocolo HTTP ou HTTPS, a URL deve possuir o prefixo http://: ou https://
      ```git
      $ git clone http://192.168.1.1/opt/repositorios/moveis-ecologicos.git
      ```
