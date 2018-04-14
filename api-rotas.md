# SUPPLIER
### GET /supplier/all
retorna json com todos os fornecedores

### POST /supplier/
Adiciona supplier
````javascript
{
    name: {type: String, required: true},
    phone: {type: String, required: true},
}
````

# USER
### POST /user/
Adiciona user
````javascript
{
    name: {type: String, required: true},
    email: {type: String, required: true, unique: true}, 
    password: {type: String, required: true }
}
````

# LOGIN
### POST /login/
Efetua login
````javascript
{
    email: {type: String, required: true }, 
    password: {type: String, required: true }
}
````
retorna
````javascript
        return res.json({
            success: true,
            token: token,
            user: user
        });
````




#PADRÕES DE RETORNO
````
SUCESSO
   -> STATUS 200
   -> NÂO CASO ESPECIFICADO SUCESSO RETORNA {} OBJETO VAZIO

ERROS / INSUCESSOS

   -> STATUS 500 erro interno do servidor
   -> STATUS 404 ROTA NAO ENCONTRADA
````