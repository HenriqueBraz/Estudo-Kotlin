# API

### Estrura
-index.js (define os routers)   
........    ->routers (define o service a ser utilizado)     
................          ->services (onde a rota deve ser executada e retornar o *resposta*)
Imagem da arquitetura: 
![alt text][logo]

[logo]: https://ibb.co/bv3t0S "Logo Title Text 2"
      
[captura_Arq_Porj](https://ibb.co/bv3t0S)
https://ibb.co/bv3t0S

#### Parâmetro do Request
queryparameter (*o do get*)        
........ex: url/rota?id=10203        
........`let id = req.params.id`         

recuperar body      
........ex: Post para rota X com body = {id: 12345}        
........`let id = req.body.id`           

### Convenções do Projeto
1.  Camelcase (ex: 'chaveDaApi')
1.  Lógica presente apenas nos 'SERVICES'
1.  Router apenas chama o Service
1.  Tentar manter código legível com nomenclaturas significativas
1.  Comentar código sempre que possível de mandeira direta e clara

### POSTMAN
*  Utilizar postman para 'testar' api (durante desenvolvimento


### DOCUMENTAÇÂO RECOMENDADA    
*  [MONGOOSE](http://mongoosejs.com/docs/models.html) 
*  [NODE](https://nodejs.org/en/docs/) 
*  [Express](http://expressjs.com/pt-br/) 
*  [BODY-PARSER](https://github.com/expressjs/body-parser) 
*  [NPM](https://www.npmjs.com/) 

### Instalando projeto
1.  Baixar projeto do git*
1.  Ir para pasta 
>> ./api 
1.  Rodar na linha de comando`npm install` (Rodar sempre que novas dependências forem instaladas)
1.  Rodar em outra linha de comando `mongod` se ouver erro preça ajuda para cássio para criar pasta *data*
1.  Rondar na linha de comando `npm start` ou `npm run dev` (perguntar diferença)

### Salvando novas dependências
*SALVANDO NO PROJETO DEV E PROD*    
`npm install --save` nome-do-pacote     
*SALVANDO EM DESENVOLVIMENTO*       
`npm install --save-dev` nome-do-pacote      
*Para Desinstalar*     
`npm uninstall --save` nome-do-pacote (ou --save-dev)     


### Editores VS IDE's
*  Preferencialmente utizar Visual Studio Code, ou Atom, ou Sublime ****Não Há Necessidade de utilizar IDE****!



