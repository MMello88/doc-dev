# Laravel Tips

## Artisan

### Criação das controllers

```sh
# php artisan make:controller Pasta/TesteController --resource or --api --model=User
```

>note: --resource é opçional. È utilizado para deixar definido as funções dentro da controller no padrão das routes

>note: --model=User é opcional. Utiliza para fazer a injeção de dependencia. Portanto este parametro indica qual insejão de dependencia vc quer realizar. neste caso quero usar a modelo User. Exemplo: Na controller UserController tem a função "public function show(User $user)" e que ao realizar o method get na url do show passando o id do usuário ele já me trás automaticamente a Modelo dele.

### Criação das modelos

```sh
# php artisan make:model Pasta/Test [-m] [-c]
```

>note: -c é uma opção já para criar a Controller (não usar quando tiver uma pasta) e -m é uma opção para já criar a Migration

### Criação das migrations

#### Criar

```sh
# php artisan make:migration create_atividade_table --create=atividades --table=atividades
```

>note: create_atividade_table pela nomenclatura o laravel identifica o que vc quer fazer, portanto o create ele já entende que vc quer fazer uma criação de tabela

>note: parametro --create passa o nome da tabela que quer criar e o parametro --table passa tbm o nome da tabela que ira alterar.

#### aplicar migração

```sh
# php artisan migrate
```

>note: Aplica todos as migration criadas

#### voltar migraçao

```sh
# php artisan migrate:rollback
```

>Note: Voltar as operações recentes

```sh
# php artisan migrate:rollback --step=1
```

>Note: Voltar 1 operação. Pode colocar quantas quiser

```sh
# php artisan migrate:reset
```

>Note: Reverterá todas as migrações do seu aplicativo

#### Recarregar o banco todos mais os dados

```sh
# php artisan migrate:refresh --seed
```

### Criação de Seeders

```sh
# php artisan make:seeder UserSeeder
```

### Executar Seeders

Executando seed unitária

```sh
# php artisan db:seed --class=UserSeeder
```

Executando em conjunto.

>Note: Primeiro vc deve acidionar a sua nova classe na `DatabaseSeeder::run`

```sh
# php artisan db:seed
```

### Criação das Request Custom

```sh
# php artisan make:request StoreUpdateAtividadeRequest
```

>Note: Store e Update no nome para identificar os methods que irei utilizar. Este Request é utilizado para validar os parametros 

#### usando a classe

```
public function store(StoreUpdateAtividadeRequest $request)
public function update(StoreUpdateAtividadeRequest $request, Atividade $atividade)
```

>Note: Usando a classe Request fazendo injection no request



### Testar retorno

1 - Campo nulo

Modelo de retorno json

```json
{
    "message": "The given data was invalid.",
    "errors": {
        "email": [
            "The email is mula"
        ]
    }
}
```

2 - Id não existe

Status 404 retorno

```json
{
    "message": "No query results for model [App\\Models\\User] 5",
}
```

3 - Não autenticado

Retorno

```json
{
    "message": "Unauthenticated."
}
```