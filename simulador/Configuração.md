# Configuração inicial

## Sincronizar Projeto

Vamos inciar trazendo o projeto do repositório Github

```sh
# git remote add origin https://github.com/MattMello88/simulador.git
# git pull origin main
```

## Instalar as Dependencias do Projeto

As dependencias elas não vão para o repositório. Existe o arquivo package.json que contém toda a informação do projeto incluindo as dependencias e qual a versão ela foi usada.

### Remover configuração de Dependencias

```sh
# rm -rf node_modules/
# rm -rf package-lock.json
```

### Comando para atualizar as Dependencias

```sh
# npm install
```

### Atualizando Dependencia storybook

```sh
# npx sb init
```

# Rodar projeto

## Iniciar o storybok

```sh
# npm run storybook
```

## Iniciar o projeto

```sh
# npm start
```

## Iniciar test

```sh
# npm test
# npm run cover
```

> Note: package.json está o comando completo do cover

# Upgrade dos components

## Caso queira atualizar seus componentes para a versão mais recente

```sh
# npm upgrade --latest
```
