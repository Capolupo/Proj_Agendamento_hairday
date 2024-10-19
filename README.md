1 - Instalando o JSON Server
npm i json-server@1.0.0-alpha.21

2 - Adicionando o arquivo .gitignore
node_modules

3 - Adicionando scripts ao arquivo package.json:

A - Propriedades de descrição do prjeto
"name": "hairday",
"description": "Aplicação Web de agendamento para corte de cabelo",
"author": "André Capolupo",

B - Scripts
"scripts":{
  "server" : "json-server --watch server.json --port 3333"
},

4 - Criar o arquivo server.json que será onde ficara salva os agendamentos

5 - deixar criado a rota no server.json
{
  "schedules" : []
}

6 - Testar rodando 
npm run server

7 - Instalando o Webpack e criar os arquivos de configurações
npm i webpack@5.89.0 webpack-cli@5.1.4 --save-dev
A - Acrecentar no package.json "build":"webpack"

8 - Dentro da pasta src Criar o arquivo de entrada do js main.js

9 - Na raiz do projeto criar o arq webpack.config.js
*Pegar o modelo deste arquivo ja pronto

10 - Fazer a instalação do server do webpack
npm i webpack-dev-server@4.15.1 --save-dev

11 - Adicionando scripts ao arquivo package.json:
"dev":"webpack serve",

12 - Carregando o HTML no webpack
npm i html-webpack-plugin@5.6.0 --save-dev

13 - Carregando o fivIcon

14 - Instalando o style-loader
npm i style-loader@3.3.3 css-loader@6.8.1 --save-dev

15 - Ajustar o arquivo main
"use strict"
//css
import "./styles/global.css"
import "./styles/form.css"
import "./styles/schedule.css"

16 - Copiando os assets
npm i copy-webpack-plugin@11.0.0 --save-dev

17 - Instalação do Babel
npm i babel-loader@9.1.3 @babel/core@7.23.7 @babel/preset-env@7.23.7 --save-dev


//EXECUTANDO//
npm run build
npm run server
npm run dev -> em outro terminal

18 - Adicionando 
npm i dayjs@1.11.10

19 - criando a pasta libs para adicionar as bibliotecas


----------------------------------------------------------
CRIANDO E CONSUMINDO A API
1 - Criei a pasta services em src
2 - Criei o arquivo api-config.js onde ficara a URL de acesso API
3 - Criei o arquivo schedule-new.js para cadastrar novos agendamentos 
4 - Importei schedule-new.js no arquivo submit.js para utilizar a função de cadastro de agendamentos
5 - Criei a schedule-fetch-by-day.js para filtrar os agendamentos por dia
