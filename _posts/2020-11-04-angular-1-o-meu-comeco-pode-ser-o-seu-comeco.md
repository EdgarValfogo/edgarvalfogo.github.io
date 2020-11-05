---
layout: post
title:  "Angular #1 - O meu começo pode ser o seu começo"
date:   2020-11-04 22:10:26 -0300
categories: angular desenvolvimento
---

**OLHA O BONITÃO AI!**

Eu quero falar sobre **Angular**, não só isso. EU QUERO ENSINAR ALGO PRA ALGUÉM!!!

>**Antes de mais nada**, para o que está escrito abaixo, deduzo que você já conhece bastante coisa sobre desenvolvimento, principalmente para web. Que tenha boas noções de HTML, CSS e Javascript.
>Caso não tenha, tem uma galera ai que pode te ajudar no **Youtube**, o pessoal da [**Rocketseat**](https://rocketseat.com.br/) tem uns cursos incríveis, de graça. [**Alura**](https://www.alura.com.br/), [**Devmedia**](https://www.devmedia.com.br/), [**Origamid**](https://www.origamid.com/), dentre opções pagas. Entre muitas outras por aí, que não lembro agora. Em breve devo fazer algo para ajudar as pessoas a entrarem nesse mundo também. Se precisarem de umas dicas, podem me chamar também, em!

Vou lhes dizer que, na pirâmide do aprendizado, ensinar é o que mais te faz aprender, e eu estou em uma trilha intensa de "Tentando ser um mestre de **Angular**". Se você também tem esse objetivo, ótimo! Eu espero que possamos trocar informações, e que vocês possam me ajudar a conduzir essa jornada comigo. Caso ainda não tenha esse objetivo, mas está curioso sobre **Angular**, também vai ser muito bom tê-lo por aqui. Vamos trocar idéias!

Vou começar a contar minha experência pessoal e o meu inicio com Angular, para, quem sabe, isso ser compatível com mais pessoas. Lembrando que é totalmente "pulável", e vocês podem ir direto ao ponto pulando o tópico **Como eu comecei com Angular** e indo diretamente para **O que é o Angular?**.

```<!-- Inicio da parte ignorável -->```
## Como eu comecei com Angular

### Meetups - Você deveria ir em alguns, assim que possível

Há muito tempo que fui em um **meetup**, que ainda era pequeno na época, chamado **.Net Coders**. Lá conheci uma galera legal, e também era um dos primeiros meetups que eu fui até então, mas foi neste meetup que conheci realmente o **Angular**.

Eu já somava alguns anos de desenvolvedor web, e curioso em desenvolvimento de jogos e aplicações ERP também. Eu tinha, na época, uma grande aplicação comercial em desenvolvimento, que consistia em ter várias e várias telas, alinhava sistemas de montagem para variadas situações, centros de custos de forma que tudo ficasse bem fragmentado, mas inteligente. Jobs e mais jobs, tudo utilizando algo acessível na época, para mim: PHP, MySQL, HTML, JS e CSS.

### A promessa do Angular

Angular na época era uma das ferramentas que prometia pra mim mais performance, dentre outras que eu havia lido sobre, e algo mais parecido com uma SPA (Single Page Aplicação aka Aplicação de uma página), daquelas que não dao "refresh" na tela. Nessa época, eu fazia esse trabalho já focado em SPA, porém utilizando o **Ajax** através de **Javascript** puro. Vocês nem imaginam o *trampo* que dava dar manutenção para o sistema.

Desde esse meetup, **Angular** faz parte da minha vida, desde a versão inicial, que hoje é conhecida como **AngularJS**, da qual eu já abandonei para seguir para as versões atuais, conhecidas simplesmente como **Angular**. Eu sei, eu sei, é complicado. Mas entenda que **AngularJS** é o antigo, e **Angular** é o novo, o atual, e o que seguirá sendo como qualquer versão vinda de **Angular 2+**.

Trabalho em aplicações de larga escala, ajudando milhares de pessoas com o objetivo de facilitar acesso a ERPs, melhorar suas comunicações com um portal de colaboradores, trazer escalabiliadade para soluções e sistemas grandes (e complicados) e viabilizar muitos tipos de aplicações via web, em formato de **SPA**s ou **PWA**s.

### Hoje muito do meu trabalho é em volta de Angular

Com o tempo fui migrando as aplicações para **microsserviços**, utilizando **Python**, **C#**, **PHP**, **Javascript**, todas containerizadas ou não, mas sempre sendo porta de comunicação para interfaces feitas com **Angular**. Então hoje eu posso dizer que: **Angular faz parte da minha vida, a pelo menos 7 anos**.

```<!-- Fim da parte ignorável -->```

## O que é o Angular?

O **Angular** (2+) é uma framework bem completa. Vem com uma interface de comandos para te auxiliar (Angular CLI), vem pronto para fazer aplicações de todos os tamanhos, com ou sem testes, com ou sem pré-processadores de CSS, construído com **Typescript**, com o **Webpack** como seu *bundler* e uma comunidade bem grande.

### Ele é bom para todos os tipos de projeto?

Sim, mas com alguns poréns: 
* Se você for fazer uma aplicação que tenha todo um trabalho em torno de conteúdos e todo o trabalho com SEO, você vai ter algumas tarefas a serem feitas, como o Server Side Rendering, para que o conteúdo dinâmico seja renderizado antes de ser exibido, para que haja uma leitura melhor através das *Search Engines* (Google, Yahoo, Bing, etc...).
* Ele não faz tanto barulho quanto outras libs no momento, como React e Vue, pois ele tem uma curva de entrada pouco maior. Mas todos que trabalham com essas outras frameworks/libs, já vão entender mais rapidamente Angular.
* Se você for fazer uma pequena aplicação, que não parece que irá escalar, pode parecer muito "verboso". Mas pra mim, esse argumento não é bom.

Então se você me perguntar: *Mas e então, Eddy, devo usar Angular no meu próximo projeto?*

Eu digo: **Sim, mas com calma. Caso seja seu primeiro projeto com Angular, você fará cagadas, grandes cagadas**.

### Como evitar as grandes cagadas com Angular?

* Saiba o minimo de **Git** pois como estaremos em crescimento, um controle de versão é bom para poder reverter as cagadas. Não só isso, hoje é e sempre foi de extrema importância que todos os projetos tivessem seu controle de versão;
* Entenda como funciona **Typescript**, é incrível e gostoso trabalhar com ele depois que se aprende mais sobre. Tudo que no começo pode parecer chato (Caso você não tenha experiência com outras langs fortemente tipadas), vai parecer uma espécie de escudo contra bugs;
* Aprenda a conviver com **ESLint**/**TSLint**. Eles vão te ajudar a fazer as coisas de forma mais padronizada. Se um dia você for trabalhar em equipe, um desses vai salvar muito o tempo de todos na hora de um olhar para o código do outro. Este também se torna um escudo contra bugs;
* Leia o básico da documentação, se possível faça o **Tour of Heroes**. Não é lá dos mais empolgantes, mas dá uma boa noção sobre quase todos os assuntos.
* Aprenda sobre formulários reativos (Form Builder, Form Group, Form Array);
* Aprenda sobre Feature Modules, Modules, Core Modules, Shared Modules, Lazy Loading e Routing no **Angular**;
* Aprenda sobre estruturação de Angular com projetos de larga escala;
* Aprenda sobre Observables e Promisses. São como ouro!;
* Crie algumas aplicações como por exemplo:
    * Listas de compras;
    * Uma mini rede social;
    * Uma calculadora;
    * Uma pokedex (brincando mas falando sério);

Com esses tópicos/aprendizados, acho que qualquer um estaria pronto para dar um passo "maior", iniciando com uma grande aplicação.

Nos posts seguintes, vou falar um pouco mais sobre esses tópicos, e coisas que considero importante para o seu crescimento como um desenvolvedor que trabalha com **Angular**, e todas as outras similares.

Vou deixar aqui alguns links para vocês iniciarem seus estudos:
* [Instalação do Git](https://git-scm.com/)
* [Github para os seus repositórios](https://github.com/), observação de que não tem só esse. Mas é um dos mais famosinhos!
* [Tutorial para iniciar com o Git e o Github](http://devfuria.com.br/git/tutorial-iniciando-git/)
* [Documentação do Typescript: Typescript for the New Programmer](https://www.typescriptlang.org/docs/handbook/typescript-from-scratch.html)
* [ESLint](https://eslint.org/)
* [TSLint](https://palantir.github.io/tslint/)
* [Angular](https://angular.io/)
* [Documentação Angular](https://angular.io/docs)
* [Documentação Angular: Tour of Heroes](https://angular.io/tutorial)

Espero que tenha ajudado alguém a se interessar mais pelo meu amado **Angular**. Gostaria de deixar bem claro que também gosto muito de **React** e **Vue**, e já trabalhei com eles, porém **Angular** sempre foi o mais presente pra mim, em todos os meus projetos, e me sinto mais confortável com ele.

E, por hora é isso. Até a próxima!!!