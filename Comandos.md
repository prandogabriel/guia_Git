# Comandos Básicos :

## Clonar Repositório Remoto

- `$git clone linkrepositorio`
  - se tiver ums chave ssh adicionada em sua conta, use a opção para clonar para autenticação ssh.

## Sincronização de Arquivos

- `$git push` ou `$git push origem nomeBranch` quando temos mais de uma branch.
  - Para mandar seus arquivos locais para repositório remoto. Antes deve ter sido feito um commit.
- `$git pull`
  - Para baixar atualizações do repositório.

## Branch
- ```$git branch``` 
  - Listar braches existentes.
- `$git checkout -b funcionalidade_x`
  - Cria uma nova branch e chamado funcionalidade_x e a seleciona.
- `$git checkout nomeBranch`
  - Seleciona a branch.
- `$git branch -d funcionalidade_x`
  - Deleta a branch.
- `$git merge nomeBranch`
  - Atualiza a branch que você escreveu no comando para a master passar a ter o conteúdo do branch.

## Links Úteis

### Comandos mais utilizados disponíveis em :

[https://woliveiras.com.br/posts/comandos-mais-utilizados-no-git/](https://woliveiras.com.br/posts/comandos-mais-utilizados-no-git/)

[https://www.hostinger.com.br/tutoriais/comandos-basicos-de-git/](https://www.hostinger.com.br/tutoriais/comandos-basicos-de-git/)
