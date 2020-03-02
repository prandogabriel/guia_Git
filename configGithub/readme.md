## Configurando Repositório Remoto Github

> Para gitlab o procedimento é o mesmo.



- Entre em sua conta em Profile - Settings - SSH Keys

- Para gerar sua chave SSH, vá no terminal e digite os seguintes comandos: 

  ```shell
  $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
  ```

  > pressionar enter nos passos a seguir até gerar.

  ```shell
  $ eval "$(ssh-agent -s)"
  ```

  ```shell
  $ ssh-add ~/.ssh/id_rsa
  ```

  

- Para Copiar sua chave SSH para ser adicionado na sua conta do github/gitlab:

  - No **Linux** :purple_heart::100::

    - ```shell
      cat ~/.ssh/id_rsa.pub
      ```

      

  - No **Windows**:

    - ```shell
      $ clip < ~/.ssh/id_rsa.pub
      ```

      

  - No **Mac**:

    - ```shell
      $ pbcopy < ~/.ssh/id_rsa.pub
      ```

      

- Agora só colar sua chave em sua conta remota.