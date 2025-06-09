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


* Migrations

// Migrations - controle de versão dentro do código, um histórico de todas as mudanças que foram feitas dentro de um banco de dados.

// Dentro do arquivo migrations tem as opções UP e DOWN que servem tanto pra subir o código como derrubar ou voltar ao código anterior.


* Realizando queries com Knex

// como realizar queries simples de inserção e busca de dados.

* Variáveis ambiente

// Sabe quando você precisa utilizar um diferente valor quando está em desenvolvimento e quando está em produção? Bom, é exatamente para isso que servem as variáveis ambiente

* Zod

// com essa biblioteca é possível garantir que as variáveis ambeintes estão preenchidas e com valores corretos, é possível tratar e validar as váriaveis ambiente dos projetos.

* Requisitos funcionais, Regras de Negócio e Requisitos não funcionais.

// RF:
- [] O usuário deve poder criar uma nova transação;
- [] O usuário deve poder obter um resumo da sua conta;
- [] O usuário deve poder listar todas transações que já ocorreram
- [] O usuário deve poder vizualizar uma transação única;

// RN : 
- [] A transação pode ser do tipo crédito que somará ao valor total ou débito que subtrairá;
- [] Deve ser possível identificarmos o usuário entre as requisições;
- [] O usuário só pode vizualizar transações o qual ele criou;

// RNF:
- [] 

* Plugins do fastify

// Plugins podem ser usados para adicionar funcionalidades como autenticação, log, validação de dados, gerenciamentos de erros entre outras, sempre lembrar que ao usar um plugin do fastify em uma function é necessário que adicione o Async na function.


* Implementação de rotas 

// criação de transações e validação de dados da requisição (request.body) com o zod para garantir que as informações recebidas sejam válidas e após isso, fazer de fato a inserção no banco de dados.

//  Tipagem no Knex - intengrar o knex ao typescript para ter suporte ao autocomplete de tabelas e tipagem de dados corretos.

// Listagem das transações - implementação de uma rota pra listar todas as transações e uma específica para receber o id para uma transação única.

// Resumo de transações - criação de uma rota para calcular(somar) as transações e retornar o total.

// Utilizando cookies no Fastify - identificação do usuário que está utilizando a aplicação ao ler e escrever informações em cookies utilizando o fastify.

// Validando existência do cookie - validação do coockie do sessionId para identificar o usuário da aplicação, a busca será realizada uma função como preHandler(middleware).

// Configurando um hook global - como registrar hooks globais no fastify e em quais rotas eles vão impactar.


* Testes automatizados

// Unitários: unidade da sua aplicação

// Integração: comunicação entre duas ou mais unidades

// e2e - ponta a ponta : simulam um usuário operando na nossa aplicação

// Criando primeiro teste - como criar o primeiro arquivo de testes usando o vitest, uso da ferramenta, instalação e execução do primeiro teste.

// Testando criação de transação - Esta aula ensina como criar o primeiro teste e2e para testar a rota de criação de transação, utilizando o pacote supertest. Além disso, a aula explica o uso das funções beforeAll, beforeEach, afterAll e afterEach para realizar configurações e limpezas antes e depois dos testes e2e.

Uma breve explicação sobre esses métodos:

beforeAll

É uma função que é executada uma única vez antes de todos os testes. É útil para inicializar recursos compartilhados que serão utilizados pelos testes.

beforeEach

É uma função que é executada antes de cada teste. É útil para preparar o ambiente antes da execução de cada teste, por exemplo, inicializar variáveis ou limpar o banco de dados.

afterAll

É uma função que é executada uma única vez após todos os testes terem sido executados. É útil para limpar recursos compartilhados ou fechar conexões abertas.

afterEach

É uma função que é executada após cada teste. É útil para limpar o ambiente depois da execução de cada teste, por exemplo, limpar variáveis ou fechar conexões com o banco de dados.