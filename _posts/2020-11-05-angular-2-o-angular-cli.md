---
layout: post
title:  "Angular #2 - O Angular CLI"
date:   2020-11-05 08:20:26 -0300
categories: angular desenvolvimento cli frameworks
---

Vamos falar desse cara incrível, o Angular CLI, salvador de muitas vidas.

Antes dessas frameworks, como Angular, React, Vue e outras parecidas ficarem famosas e cheias de funcionalidades, você tinha que configurar tudo á mão. Você tinha que pensar em:

- **Módulos**: Como trabalhar os módulos do "novo Javascript" (Ecma Script 6), visto que era um ganho grande de produtividade para os desenvolvedores. Utilizando libs como CommonJS, Babel, Webpack;
- **Transpiladores**: Se fossemos usar Typescript além dos módulos, devido a todo o seu ganho produtivo, deveriamos usar um transpilador, que torna o código legível para todos os browsers, transpilando para versões anteriores de javascript, o mesmo aconteceria com o item acima também, então era quase um "2 em 1";
- **Minificadores**: Precisamos compactar toda aquela massa de código gerada, para gerar mais performance e reduzir o tempo de carga do site/aplicação;
- **Compatibilização de navegadores**: Precisávamos lembrar que tínhamos (ainda temos) vários navegadores, com certos padrões em comum, outros não;
- **Acompanhamento de detecção de alterações:** Visto que basicamente era uma "Single Page Application", era necessário que não houvesse reloads/refreshs aparentes na tela, daqueles que "piscam", carregam, e tal. Então tinhamos que achar uma lib, como zone.js por exemplo, que nos ajudasse com esse trabalho;

> Que dor de cabeça, meus amigues! Era uma semana pra sair do zero, e iniciar o projeto efetivamente, com chance de erros ainda.

## Durante o beta do Angular 2

Durante o beta dessa framework, a partir da versão 2, tinhamos uma grande "dor". A dor de criar tudo do zero, com todos os seus pacotes, bundlers, regras, linters, configuração de webpack (ou similares), transpilação, QUANTA COISA!!! Cheguei até a cogitar desistir das frameworks, por ter que criar um projeto do zero. Pouco depois, as facilidades vieram a nós, com elas, o Angular CLI, conjunto com equivalentes das outras frameworks.

## Facilidades do Angular CLI

Esse lindo do Angular CLI trás várias funcionalidades através da interface de comando de lia (vulgo **CLI**) . Dentre as funcionalidades, podemos:

- Criar **módulos**
- Criar **components**
- Criar **projetos**
- Criar **bibliotecas**
- Crar **testes**
- Criar um projeto com tudo estruturado, de forma minificada ou não, com scss ou less, com testes ou sem testes;

Todos esses itens acima, entre outros que não citei, tem opções para escolher se quer que venham com complementos para X ou para Y. É simplesmente maravilhoso.

### O uso no dia-a-dia

Eu não uso o CLI hoje em dia, pois gosto de entender toda a geração, gosto de fazer minha estruturação para namming dos arquivos do projeto, mas pra quem tá começando, ou para certos tipos de projetos e certos tipos de uso, ele vai ajudar de mais. 

Sem contar que ele é o "criador do projeto". Quando damos um `ng new *projeto'* ele já vai nos dar a primeira força.

Então, queria agradecer os lindes criadores e mantenedores desse projeto e dos similares, pois eles nos salvam todos os dias, o dia todo.

Dá uma olhada na documentação do Angular CLI, entenda melhor sobre esse carinha,  e veja como ele vai te ajudar durante os projetos:

[https://angular.io/cli](https://angular.io/cli)

**Por hoje é só, até e até a próxima!!!**