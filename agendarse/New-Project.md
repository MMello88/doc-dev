# Iniciar um novo projeto reactjs

> Considero ter lido a documentação [Install.md](Install-tools.md)

## Create Project

Documentação completa online [https://pt-br.reactjs.org/docs/create-a-new-react-app.html](https://pt-br.reactjs.org/docs/create-a-new-react-app.html)

```sh
# npx create-react-app my-project
```

## Startar Projeto

```sh
# npm start
ou
# yarn start
```

> Se utilizar o yarn remove o package-lock.json para dar o start

As dependencias elas não vão para o repositório. Existe o arquivo package.json que contém toda a informação do projeto incluindo as dependencias e qual a versão ela foi usada.

```sh
# rm -rf node_modules/
# rm -rf package-lock.json
```

# Instalando componentes

## Create storybook

```sh
# npx sb init
```

### Iniciando storybook

```sh
# yarn run storybook
```

## prettier.io

```sh
# npm install --save-dev --save-exact prettier
# yarn add --dev --exact prettier
```

## editorconfig.org

Colocar este comando abaixo dentro do arquivo que ira criar na pasta raiz chamdo .editorconfig

```
# EditorConfig is awesome: https://EditorConfig.org

# top-most EditorConfig file
root = true

# Unix-style newlines with a newline ending every file
[*]
end_of_line = lf
insert_final_newline = true

# Matches multiple files with brace expansion notation
# Set default charset
[*.{js}]
charset = utf-8
```

## styled-componentes

```sh
# npm install --save styled-components
```

## addon-viewport - component para storybook

```sh
# npm install @storybook/addon-viewport
# yarn add @storybook/addon-viewport
```

> Note: No projeto tem a pasta .storybook incluir no _main.js_ na tag _addon_ o comando **"@storybook/addon-viewport"**

## prop-types

```sh
# npm install --save prop-types
```

## addon-knobs - component para storybook

```sh
# npm install @storybook/addon-knobs
# yarn add @storybook/addon-knobs
```

> Note: No projeto tem a pasta .storybook incluir no _main.js_ na tag _addon_ o comando **"@storybook/addon-knobs"**


## react-router-dom

```sh
# yarn add history react-router-dom@next
```
> Note: Estou utilizando um release que ainda não saiu, por isso é desta maneira a sua instalação. Versão 6.1.0-beta.0

Para instalação tradicional, lembre-se de pegar a versão v6 ou maior

```sh
# yarn add react-router-dom
```

## react-helmet

```sh
# npm install --save react-helmet
# yarn add react-helmet
```

## react-icons

```sh
# npm install --save react-icons
# yarn add react-icons
```

## materil-iu

```sh
# npm install @material-ui/core
# yarn add @material-ui/core
```


```sh
# npm install @material-ui/icons
# yarn add @material-ui/icons
```