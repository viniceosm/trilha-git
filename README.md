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

É preciso informar para o **Git**, seu **nome** e **e-mail**, execute o comando em seu terminal:
  ```git
    $ git config --global user.name "MEU NOME VAI AQUI"
    $ git config --global user.email "MEU E-MAIL VAI AQUI"
  ```
## Criando um repositório
  - Iniciando o Git em um diretório, transformando em um repositório, execute o comando em seu terminal:
    ```git
      git init
    ```
  - Confirmação de sucesso da criação do repositório deve retornar uma mensagem dessa forma:
    ```git
      Initialized empty Git repository in CAMINHO RAIZ DE ONDE FOI EXECUTADO O git init
    ```
  - Essa mensagem informa que o inicializado um repositório git vazio.
