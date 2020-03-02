# Mac

> Instalação no Mac.

[Download ](https://sourceforge.net/projects/git-osx-installer/)

Se possuir o MacPorts:

```shell
$ sudo port install git-core +svn +doc +bash completation +gitweb
```

> Para testar se a instalação foi realizada com sucesso

```shell
$ git --version
```

> Deve retornar a versão do git que está instalada em sua máquina.



## Configuração Básica

> No terminal ...

```shell
$ git config --global user.name ”Seu Nome"
```

```shell
$ git config --global user.email ”Seu Nome"
```

- > Seu email do github de preferência

```shell
$ git config --global color.ui true
```

- > Opcional - Utilizado para facilitar o entendimento visual dos comandos