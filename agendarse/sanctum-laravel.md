# Instalação do Sanctum Laravel api

* Instalar o XAMPP

* Instalar ro Composer

## Instalação do Sanctum Laravel

Criar o projeto laravel

```sh
# composer create-project laravel/laravel --prefer-dist nome-projeto-app
```

Adicionar o component sunctum

```sh
# composer require laravel/sanctum
```

Publicar os arquivos de configuração e migração sunctum

```sh
# php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
```

Configurar o **auth.php** dentro da pasta **Config**

> O driver do api colocar sanctum

 ```
 'guards' => [
        'web' => [
            'driver' => 'session',
            'provider' => 'users',
        ],

        'api' => [
            'driver' => 'sanctum',
            'provider' => 'users',
            'hash' => false,
        ]
    ],
 ```
