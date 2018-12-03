# Trilha sobre Git

**Git** é um sistema de controle de versão de arquivos, com ele podemos desenvolver projetos e compartilhar nossos códigos com diversas pessoas, mantendo o histórico das alterações dos arquivos.

## Instalação
**Windows**
  - Donwload da ultima versão disponível [aqui](https://gitforwindows.org/).
  - A instalação é simples, padrão em todas as instalações em aplicações na plataforma **Windows**.
  - A instalação vem com o **Git Bash**, que permite que seja executado linhas de comandos do **Git no Windows**.
  
**Mac**
  - Download da ultima versão disponível [aqui](https://git-scm.com/download/mac).
  - Utiliza o terminal padrão do **Mac**.

**Linux**
- Distribuição baseada em **Debian**, execute o comando em seu terminal:
  ```bash
    $ sudo apt-get install git
  ```
- [Outras distribuições Linux](http://git-scm.com/download/linux)
- Utiliza o terminal padrão do **Linux**.

## Configuração inicial

- É preciso informar para o **Git**, seu **nome** e **e-mail**, execute o comando em seu terminal:
```git
$ git config --global user.name "MEU NOME VAI AQUI"
$ git config --global user.email "MEU E-MAIL VAI AQUI"
```
- Verificando qual **nome** está configurado no Git, execute o comando em seu terminal:
```git
$ git config --global user.name
```
- Verificando qual **e-mail** está configurado no Git, execute o comando em seu terminal:
```git
$ git config --global user.email
```
## Criando um repositório
  - Iniciando o Git em um diretório já existente, transformando em um repositório, execute o comando em seu terminal:
```git
$ git init
```
  - Iniciando o Git em um diretório que não existe.
```git
$ git init nome-diretorio
```
  - Confirmação de sucesso da criação do repositório deve retornar uma mensagem dessa forma:
```git
Initialized empty Git repository in CAMINHO RAIZ DE ONDE FOI EXECUTADO O git init
```
  - Essa mensagem informa que foi inicializado um repositório Git vazio.
  
## Verificando alterações
  - Verificando a situação dos arquivos no repositório com o comando:
```git
$ git status
```
  - **git status** informa em uma lista, caso tenha alterado, adicionado ou removido um arquivo. 
  
## Adicionando o arquivo no rastreamento 
  - Adicionando o arquivo no rastreamento e preparando ele para commitar.
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
  - Sempre vincule cada commit a um issue.

## Verificando alterações, log de commits
  - Para ver o log das alterações no repositório, execute o comando em seu terminal:
```git
$ git log
```
  - Limitando a visualização de logs, mostrando os ultimos dois commits.

```git
$ git log -n 2  
```
## Configurando um repositório remoto
  - Para adicionar um repositório remoto, execute o comando em seu terminal: 
```git
$ git remote add origin https://caminho-do-repositorio-remoto
```
## Enviando as alterações pro repositório remoto
 - Enviando os commits pro repositório remoto
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
  - Caso não queira comitar certos arquivos toda vez, basta criarmos um arquivo chamdo .gitignore no diretório principal e colocar os nomes de arquivos e pastas dentro do mesmo.
  - [Exemplos de .gitignore](https://github.com/github/gitignore)

## git add & git commit 
  - Podemos fazer **git add** com **git commit** em apenas um comando dessa forma:
```git
$ git commit -a -m "Descrição do commit"
```
ou
```git
$ git commit -am "Descrição do commit"
```
  
