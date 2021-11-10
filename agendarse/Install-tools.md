# Guia de Instalação

## Instalação Node

[Documentation install online](https://github.com/nodesource/distributions/blob/master/README.md#debinstall)

```sh
https://github.com/nodesource/distributions/blob/master/README.md
# curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
# sudo apt-get install -y nodejs
```

## Instalação Yarn

```sh
# curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
# curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
# sudo apt update && sudo apt install yarn
```

## Instalação Git

```sh
# apt-get install git
# add-apt-repository ppa:git-core/ppa # apt update; apt install git
```

### Configuração inicial

```sh
# git config --global user.name "MattMello88"
# git config --global user.email "matheusnarciso@hotmail.com"
```
