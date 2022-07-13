# Treinando markdow
### Treinando markdow e construindo documentação para APIs

##### Endepoints:


---------------------------------------------------------------------------------------------
### ▼ GET /games
##### Objetivo do endpoint ► retorna a listagem de todos os games cadastrados
#####   Parâmetros ► não recebe
#####   Respostas ► OK! 200 (sucesso), 401 (Falha na autenticação - usuário, senha ou token) 
####      Exemplo de resposta (200) ▼
            ```
            [
                {
                    "id": 23,
                    "title": "Call of duty MW",
                    "year": 2019,
                    "price": 60
                },
                {
                    "id": 65,
                    "title": "Sea of thieves",
                    "year": "2018",
                    "price": "45"
                }
            ]
            ```
#### Exemplo de resposta (401) ▼
```
{
    "message": "Invalid token"
}
```


---------------------------------------------------------------------------------------------
### ▼ POST /auth
##### Objetivo do endpoint ► fazer o login e gerar o token
##### Parâmetros ▼
#####     email do usuário cadastrado
#####     senha do respectivo email cadastrado para este usuário
####        Exemplo de requisição: ▼
              ```
              {
              "email": "v@email.com",
              "password": "54321"
              }
              ```
        
##### Respostas ► OK! 200 (sucesso), 404 (Falha de login - usuário e ou senha), 500 (erro interno) 
####    Exemplo de resposta (200) ▼
          ```
          {
              "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImlkIjoyLCJuYW1lIjoiVmFuZGVybGVpIiwiZW1haWwiOiJ2QGVtYWlsLmNvbSIsInBhc3N3b3JkIjoiNTQzMjEifSwiaWF0IjoxNjU3NzU2MTA0LCJleHAiOjE2NTc3NTk3MDR9.7nQ6FSc9jOxdhMQzIdUfebgvUyEYAPoPbll-D9saA9k"
          }
          ```
####     Exemplo de resposta (404) ▼
          ```
          {
              "error": "Usuário não encontrado ou credenciais inválidas"
          }
          ```
