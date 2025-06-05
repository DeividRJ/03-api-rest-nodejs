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

* SQLITE BANCO DE DADOS

// O SQLite é um banco de dados embutido, leve e autônomo que armazena dados em um único arquivo local, sem necessidade de servidor. É amplamente usado em aplicações mobile (Android/iOS), desktop e sistemas embarcados.
✅ Vantagens
Zero Configuração:

Não requer instalação ou servidor separado.

Leve e Rápido:

Consome poucos recursos (ideal para dispositivos com limitações).

Armazenamento em Arquivo Único:

Dados ficam em um arquivo .db ou .sqlite, facilitando backup e portabilidade.

Sem Dependências:

Funciona offline e é integrado a linguagens como Python, JavaScript e C.

Compatível com SQL Padrão:

Suporta comandos SQL como CREATE, INSERT, SELECT, etc.

⚠️ Limitações
Não suporta concorrência alta (não é ideal para sistemas multi-usuário pesados).

Falta recursos avançados como stored procedures e usuários/permissões.

📌 Quando Usar?
Aplicativos mobile (WhatsApp, Discord usam SQLite).

Prototipagem e projetos pequenos.

Sistemas locais que precisam de armazenamento simples.


* Querybuilders

// O Knex.js - é um query builder para Node.js que permite interagir com bancos de dados (como SQLite, PostgreSQL, MySQL) usando JavaScript em vez de SQL puro. Ele simplifica a construção de consultas, migrations e seeds, tornando o desenvolvimento mais rápido e legível.

// Migrations - controle de versão dentro do código, um histórico de todas as mudanças que foram feitas dentro de um banco de dados.
