# API de games

Esta API é destinada para a manipulação de jogos do meu sistema privado

## Enpoints

### GET /jogos
Esse Enpoint é responsavel por retornar todos os jogos do banco de dados

#### Parametros 
Nenhum

#### Respostas

##### OK! 200
Caso sua solição ocorra tudo bem

Exemplo de resposta:

```
[
    {
        "id": 1,
        "titulo": "call of duty",
        "ano": 2019,
        "preco": 50
    },
    {
        "id": 2,
        "titulo": "call of duty",
        "ano": 2019,
        "preco": 50
    }
]
```

##### Falha na autenticação! 401
Caso o solicitante não estaja autenticado no sistema
Motivos: Token inválido Token expirado

Exemplo de resposta:

```
{
    "err": "Não autorizado"
}
```

### GET /auth
Esse Enpoint é responsavel por fazer o processo de login

#### Parametros 
email: E-mail do usuario cadastrado no sistema.
senha: Senha do usuario cadastrado no sistema.

Exemplo de parametro:

```
{
    "email": "teste@gmail.com",
    "senha": "teste123"
}
```
#### Respostas

##### Falha na autenticação! 401
Caso o solicitante não estaja autenticado no sistema
Motivos: Token inválido Token expirado



##### OK! 200
Caso sua solição ocorra tudo bem

Exemplo de resposta:

```
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJqZXJmc29ubGlua0BnbWFpbC5jb20iLCJpYXQiOjE2MTYzNTAyNDQsImV4cCI6MTYxNjM2NDY0NH0._J_Ix3iZEX00nKSEExo6mcvILNxy1Wj_9vsSnSEDC8A"
}
```
