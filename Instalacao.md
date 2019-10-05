# Instalação

### Windows

[https://git-scm.com/](https://git-scm.com/)

ou

[https://gitforwindows.org/](https://gitforwindows.org/)

Para testar se a instalação foi realizada com sucesso:

- Abrir o Git Bash:
- `$git --version`

### Linux

`$ sudo apt-get install git`

Para testar se a instalação foi realizada com sucesso:

- Abrir o terminal:
- `$ git --version`

### Mac

[https://sourceforge.net/projects/git-osx-installer/](https://sourceforge.net/projects/git-osx-installer/)

Se possuir o MacPorts:  
`$sudo port install git-core +svn +doc +bash completation +gitweb`

Para testar se a instalação foi realizada com sucesso:

- Abrir o terminal:
- `$ git --version`

## Configuração Básica

- `$git config --global user.name ”Seu Nome"`
- `$git config –global user.email ”Seu email"`

  - De preferência, o email cadastrado no github/gitlab

- `$git config –global color.ui true`
  - Opcional - Utilizado para facilitar o entendimento visual dos comandos

Para a criação de um repositório, precisamos vincular o git a uma pasta.
Para facilitar, vamos executar os seguintes comandos no Git Bash:

- `$mkdir teste //Cria a pasta`
- `$cd teste //Acessa a pasta`
- `$git init //Inicializa o git`

Ao rodar o último comando, o git irá gerar uma pasta oculta com o nome
de ”.git” . Dentro dela ficarão os arquivos internos do git, e não é necessário modifica-la. Para visualizá-la `$ls -la`

### Para realizar um commit, existem três estágios:

- Primeiro estágio - **Untracked files**;
  - O primeiro estágio é quando os arquivos são criados na pasta, mas como o
    arquivo é novo, ele se encontra no estágio de Untracked Files, ou seja, ele é desconhecido pelo git.  
     Para verificar o status digite `$git status` no terminal  
     Este comando irá listar todos os arquivos que estão na pasta e o git
    desconhece, assim como todos os arquivos que sofreram modificações
    desde o último commit.
- Segundo estágio - **Changes to be committed**;
  - Ao adicionar criar um novo arquivo no diretório em que o git está rodando, e o adicionando com o comando `$git add arquivo.txt`  
    Nosso arquivo está no segundo estágio, que é conhecido como **_Changes
    to be committed_**, ou seja, os arquivos que estiverem neste estágio, estão
    prontos para serem commitados.
- Terceiro estágio - **Committed**.

  - Para realizar o commit:
    `$git commit -m ”Meu primeiro commit!”`  
     Note que a flag ”-m” é utilizada para atribuir uma descrição ao commit.
    Ela deve ser muito explicativa, para quem ler, saber o que realmente foi
    feito naquele commit.

- Para acessar o histórico de commits realizados no repositório, utilizamos o
  comando:
  - `$git log`

### **_.gitgnore_** para que serve:

- quando estamos desenvolvendo algum projeto, geralmento temos arquivos, de dependências ou que se são gerados ao executar o programa, e não queremos que estes arquivos subam para o diretório remoto, então adicionamos um aquivos com o nome **_".gitgnore"_** na raiz do projeto, onde dentro deste arquivos iremos por todas as extensões ou pastas que queremos que o git ignore.
  - Ex: `*.exe` irá ignorar todos os arquivos com a Extensão .exe, ou se quiseremos ignorar uma pasta, é só por o nome da pasta entre aspas duplas.

## Configurando Repositório Remoto Github/Gitlab

- Entre em sua conta em Profile - Settings - SSH Keys
- Para gerar sua chave SSH, vá no terminal e digite os seguintes comandos: 
  - `$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
    - pressionar enter nos passos a seguir até gerar.
  - `$ eval "$(ssh-agent -s)"`
  -  `$ ssh-add ~/.ssh/id_rsa`
- Para Copiar sua chave SSH para ser adicionado na sua conta do github/gitlab:
  - No **Linux**:
    - `cat ~/.ssh/id_rsa.pub`
  - No **Windows**:
    - `$ clip < ~/.ssh/id_rsa.pub`
  - No **Mac**:
    - `$ pbcopy < ~/.ssh/id_rsa.pub`  
- Agora só colar sua chave em sua conta remota.