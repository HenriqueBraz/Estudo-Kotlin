### SUPPLIER
GET /supplier/all
retorna json com todos os fornecedores

POST /supplier/
````javascript
{
    name: {type: String, required: true},
    phone: {type: String, required: true},
}
````

### USER
POST /user/
````javascript
{
    name: {type: String, required: true},
    email: {type: String, required: true, unique: true}, 
    password: {type: String, required: true }
}
````

### LOGIN
POST /login/
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