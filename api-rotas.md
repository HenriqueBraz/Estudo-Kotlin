### SUPPLIER
GET /supplier/all

POST /supplier/
````javascript
{
    name: {type: String, required: true},
    phone: {type: String, required: true},
}
````


POST /user/
````javascript
{
    name: {type: String, required: true},
    email: {type: String, required: true, unique: true}, 
    password: {type: String, required: true }
}
````



