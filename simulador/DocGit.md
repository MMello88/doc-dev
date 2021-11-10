# Branche

## Criação de Brance

```sh
# git checkout -b nome-da-branche
```

## Remover de Brance

### `Local`

```sh
# git branch -d nome-da-branch

# -D // force o delete
```

### `Remoto`

```sh
# git push origin --delete nome-da-branch
```

Ao fazer o checkout de uma nova branche automaticamente o projeto já esta direcionando para esta branche.

> Nota: **# git status** vc pode verificar sua nova branche configurada

## Adicionar

Adicionar tudo de uma unica vez

```sh
# git add .
```

**ou**

Adicionar por arquivos selecionados

```sh
# git add -A -- /diretório/arquivo.text
```

## Commit

```sh
# git commit -m "msg"
```

### Nota

> Nota: Após realizar os commits na primeira vez que fizer o **# git push** para o repositório online deve-se criar esta brenche lá e trocar para receber nesta branche criada.

## Criando Branche Repositório online

Comando para mudar e criar a branche da sua origem

```sh
# git push --set-upstream origin correcoes-home
```


# Entendendo o Pull Request

Pull requesta só é possível fazer pelo repositório do Github na branche que estamos trabalhando para a branche master.

![](./assets/pull-request-parte-1.png)

> Nota: Na imagem mostra a branche *correcoes-home* selecionada e na janelinha duas opções de *Compare* e *Open pull request*. Nesta mesma janalinha mostra o informativo que houve 7 commits a frante da principal branche.

## Iniciar o Pull Request - Requisição para subir

Ao clicar no **Open pull request** teremos a seguinte tela abaixo.

![](./assets/pull-request-parte-2.png)

* No topo superior mostrar a direção do merge, onde os fontes vão sair da branche *correcoes-home* para branche *main* (default).
* do lado direito da tela mostra algumas opções como: Reviewers, uma pessoa especifica do projeto liderada para revisar todo o código fonte. Assignees, são cessionários, ou pessoas envolvidas no problema, ou testers que podem adiquirir esta pull request e atribuir a devida solução.
* A parte central irá informar um titulo e/ou deixar um comentário, este comentário tem formato de Markedown igual ao ``README.md``.

> Nota: Ao criar o **Pull Request** os deployers já vão disponibilizar um ambiente online ou para testar ou para uma prévia para seu cliente analisar.

### Deploye

O depolye irá recompilar seu projeto, refazer os test criado, e se o deployers que estiver usando precise que também faça em seu site para uma revisão. Tudo isso vai fazer parte do check list. Enquanto os check list não estiver aprovador o merge não se habilitá para submeter na sua brenche principal.

> Deployer Chromatic do storybook obriga revisar component por component criado para ser aprovado.


## Reviews

Após o Pull Request ser criado seu código fonte passar por um processo de analise. Alguém ou vocês mesmo pode revisar seu código podendo adicionar comentários, aprovar ou negar o seu pull request.


## O Merge

O Pull Request esta aprovado e os check list também. Uiiiii! \
Seu código fonte esta pronto para ser submetido para o projeto principal.



# Deploy

## https://vercel.com/

O vercel vamos utilizar para fazer o deploy de nossa aplicação e deixar nosso site online.


## https://www.chromatic.com/

O chromatic vamos utilizar para fazer deploy do storybook e deixar online nosso storybook como uma documentação para nosso cliente analisar ponto a ponto

## Atualizando a brech main

Vamos trocar a origin que esta com *correcoes-home* para *main* utilizando o seguinte comando

```sh
# git checkout main
```

Assim q trocamos ele nos mostra que existem submissões a serem feitas e para isso usamos o comando

```sh
# git pull
```

Pronto o seu github na branche main esta atulizada igual ao do seu repositório online.

## Criando uma Release

A release uma braço da branche *main* que é identificado com **tag** que vai conter o seu sistema completo e finalizado. Permitindo avançar com o sistema com novas features. Em caso de necessidade voltar uma versão, é pela release que saberá que seu sistema vai está estável.

Em seu repositório com sua branche *main* selecionado, ao lado direito vai em Release

![](./assets/release-parte-1.png)

Informe a versão no padrão iniciando com a letra v e o numero da versão a ser liberada. Para saber mais [semver](https://semver.org/lang/pt-BR/). De um titulo e uma descrição e está pronto para publicar a realease

![](./assets/release-parte-2.png)

A release fica zipada e pode ser distribuida.

![](./assets/release-parte-3.png)
