# INF221
Repositório do Trabalho Prático de INF221 - Engenharia de Software

## Dependências

* [Bootstrap v4](https://getbootstrap.com/docs/4.1/getting-started/introduction/)
* [Laravel 5.6](https://laravel.com/docs/5.6)

## API

### Execução

Para rodar a API, basta executar os seguintes comandos:

```bash

$ cd API

$ composer install

$ npm install

$ php artisan serve

```

### Migrações

Para criar as tabelas, execute o seguinte comando:

```bash
$ php artisan migrate
```

Caso queira fazer a migração novamente, apagando as tabelas já existentes, execute o comando abaixo:

```bash
$ php artisan migrate:refresh
```

### Seeds

Para preencher as tabelas automaticamente, execute:

```bash
$ php artisan db:seed
```

Caso apresente algum erro de `class SeuSeeder does not exist`, execute o comando abaixo:

```bash
$ composer dump-autoload
```

### Rotas

Rotas disponíveis:


### ```GET /api/disciplinas ```

Retorna todas as disciplinas cadastradas

### ``` POST /api/disciplinas ```

Parâmetros:

```javascript
{
    "codigo": String,
    "nome": String,
    "semestre": int, // 1 ou 2
    "departamento": String
}
```

### ```GET /api/avaliacoes ```

Retorna todas as avaliações cadastradas

### ``` POST /api/avaliacoes ```

Parâmetros:

```javascript
{
    "disciplina": String ou null,
    "avaliador": String,
    "descricao": String,
    "professor": String,
    "nota": double,
    "facilidade": double,
    "utilidade": double,
    "recomendacao": bool
}
```