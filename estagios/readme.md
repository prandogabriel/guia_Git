### Para realizar um commit, existem três estágios:

- Primeiro estágio - **Untracked files**;

  - O primeiro estágio é quando os arquivos são criados na pasta, mas como o
    arquivo é novo, ele se encontra no estágio de Untracked Files, ou seja, ele é desconhecido pelo git.  
     Para verificar o status digite 

    ```shell
    $ git status
    ```

     Este comando irá listar todos os arquivos que estão na pasta e o git
    desconhece, assim como todos os arquivos que sofreram modificações
    desde o último commit.

- Segundo estágio - **Changes to be committed**;

  - Ao adicionar criar um novo arquivo no diretório em que o git está rodando, e o adicionando com o comando 

    ```shell
    $ git add arquivo.txt
    ```


    Nosso arquivo está no segundo estágio, que é conhecido como **_Changes
    to be committed_**, ou seja, os arquivos que estiverem neste estágio, estão
    prontos para serem commitados.

- Terceiro estágio - **Committed**.

  - Para realizar o commit:

    ```shell
    $ git commit -m ”Meu primeiro commit!
    ```

     Note que a flag ”-m” é utilizada para atribuir uma descrição ao commit.
    Ela deve ser muito explicativa, para quem ler, saber o que realmente foi
    feito naquele commit.

- Para acessar o histórico de commits realizados no repositório, utilizamos o
  comando:

  ```shell
  $ git log
  ```

  