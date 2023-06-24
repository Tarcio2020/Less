Vamos começar instalando o pacote LESS <br>

    npm install -g less

Agora iniciatemos o less com

    npm init

*Teremos algumas perguntas, daremos enter em todas. <br>

Vamos instalar a dependencia do projeto. <br>

    npm install --save-dev less

*Criou se as pastas package e node_modules <br>
*Criaremos a pasta .gitignore <br>
*Criaremos a pasta src>styles <br>
*Criaremos dentro da pasta styles o arquivo main.less <br>

Iremos em package.json
em:

  "scripts": {
                    //caminho                   destino
    "less": "lessc ./src/styles/main.less ./build/styles/main.css",
    "test": "echo \"Error: no test specified\" && exit 1"
  },

Em seguida damos o comando

    npm run less

*A pasta build será criada
___________________________________________________________________

o less não possui a função do watch, então precisaremos baixar um plugin

    npm install -global less-watch-compiler

agora fazemos a instação no projeto 

    npm install --save-dev less-watch-compiler


Agora alteramos o package:

      "scripts": {
    "less": "less-watch-compiler ./src/styles ./build/styles",
    "test": "echo \"Error: no test specified\" && exit 1"
  },


Damos o comando 

    npm run less



Colocando o arquivo main.less como principal
Aqui passamos um terceiro parametro

  "scripts": {
    "less": "less-watch-compiler ./src/styles ./build/styles main.less",
    "test": "echo \"Error: no test specified\" && exit 1"
  },




_________________________Comentários no Less________________________

/**/ ou // como no js 




