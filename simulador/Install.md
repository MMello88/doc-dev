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
# curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | gpg --dearmor | sudo tee /usr/share/keyrings/yarnkey.gpg >/dev/null
# echo "deb [signed-by=/usr/share/keyrings/yarnkey.gpg] https://dl.yarnpkg.com/debian stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
# sudo apt-get update && sudo apt-get install yarn
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
