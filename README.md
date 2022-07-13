# Treinando markdow
### Treinando markdow e construindo documentação para APIs

##### Endepoints:

#### GET /games
---------------------------------------------------------------------------------------------
  ##### Retorno ► retorna a listagem de todos os games cadastrados
  ##### Parâmetros ► não recebe
  ##### Respostas ► OK! 200 (sucesso), 401 (Falha na autenticação - usuário, senha ou token) 
#### ▼ Exemplo de resposta (200)
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
#### ▼ Exemplo de resposta (401)
```
{
    "message": "Invalid token"
}
```
