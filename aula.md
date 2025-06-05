//Fastify - é um microframework para criação de uma API no node.


* ENTENDENDO O TYPESCRIPT

// Typescript - é um superset com tipagem estática, é uma linguagem de programação.
// Principais diferenças entre typescript e javascript :
// typescript - verifica erros durante o desenvolvimento, erros antes de executar, ferramentas : (: type)
// javascrpit - verifica erros durante a execução, só descobre ao rodar, ferramentas: typeof e instaof.
// npx é uma função que vem junto ao npm pode ser executado no terminal para rodar scrpits locais do node_modules/.bin se um pacote está instalado localmente no projeto você pode execut-alo sem configurar scrpits no package.json
// sempre que usar o typescript no node é necessário instalar a dependência @types/node para que o node não de erros ao executar a conversão do arquivo.
//tsx - uma dependência do npm que converte e executa de forma automatizada o typescript para javascript sem "sujar o código" só recomendado para desenvolvimento, para produção é melhor a coversão do código raiz.

* ESLINT

// O código ESlint serve para padronizar o código de um projeto, dentro do script no packaje.json o parâmetro "lint": "eslint src --ext .ts --fix" ajuda a identificar "erros" sempre que um novo código subir e o fix para corrigi-los automaticamente caso for um erro simples.