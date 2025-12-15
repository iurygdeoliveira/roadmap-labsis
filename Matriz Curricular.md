# **Matriz Curricular**

## **1. Introdução e Filosofia Pedagógica**

Esta matriz apresenta uma especificação curricular exaustiva para  estudantes autodidatas de informática, com foco na arquitetura de aplicações web modernas. A estrutura pedagógica foi desenhada para transcender a mera transmissão de sintaxe, focando no desenvolvimento de competências de engenharia através da metodologia *Project-Based Learning* (PBL). Esta matriz adota a stack tecnológica **TALL** (Tailwind, Alpine, Laravel, Livewire) e o ecossistema **FilamentPHP**, refletindo as demandas contemporâneas por Desenvolvimento Rápido de Aplicações (RAD) sem sacrificar a escalabilidade ou a qualidade do código.

A premissa central é o "Projeto Autoral". Ao contrário de abordagens tradicionais que utilizam exercícios fragmentados, este plano exige que o aluno desenvolva, desde a primeira hora, um sistema funcional (como um pequeno ERP, ou Micro SaaS de nicho). O currículo é segmentado em 24 entregas funcionais obrigatórias — uma a cada 10 horas de estudo — simulando ciclos de *sprints* ágeis e garantindo a consolidação contínua do conhecimento. A progressão tecnológica segue uma curva de abstração ascendente: inicia-se com as fundações brutas da web (HTML/CSS/JS) para garantir a compreensão dos mecanismos subjacentes, avança para a engenharia de backend robusta com Laravel, introduz a reatividade moderna com Livewire/Alpine, e culmina na automação administrativa com Filament.

## 2. Metodologia: O Ciclo de Aprendizagem Orientado a Entregas

Esta matriz foi desenhada para combater os principais riscos do autodidatismo: a falta de estrutura, a "paralisia por análise" e a lacuna entre teoria e prática. A estrutura de 240 horas, dividida em 160 aulas de 1h30, impõe um ritmo estudo progressivo.

### **2.1 A Estrutura do Projeto Autoral**

O aluno deve definir, na Aula 1, o escopo de um projeto que resolva um problema real. Sugere-se evitar to-do lists ou blogs simples. Projetos recomendados incluem:

* **Sistema de Gestão Imobiliária:** Gestão de propriedades, inquilinos, contratos e pagamentos recorrentes.  
* **Plataforma de Telemedicina:** Agendamento, prontuário eletrônico e gestão financeira de consultórios.  
* **ERP para Pequenas Indústrias:** Controle de estoque, ordens de produção e faturamento.

### **2.2 O Protocolo de Entrega (10h Sprints)**

A cada bloco de 10 horas, o aluno deve atingir um marco funcional (Milestone). Não se trata apenas de "assistir aulas", mas de produzir um artefato de software testável.

| Milestone | Foco da Entrega | Critério de Aceite |
| :---- | :---- | :---- |
| **Arquitetura** | Código Fonte | O código deve seguir padrões PSR (PHP) e boas práticas de semântica (HTML). |
| **Funcionalidade** | Feature Set | A funcionalidade deve estar completa (ex: o formulário salva e valida, não apenas "parece" funcionar). |
| **Documentação** | Readme/Logs | Registro das dificuldades técnicas e decisões de design tomadas no período.5 |

## 3. Fase 1: Fundações da Engenharia Web e Prototipagem (0h \- 60h)

A primeira fase é dedicada à compreensão profunda da plataforma Web. Antes de utilizar frameworks que abstraem a complexidade, o engenheiro deve dominar os blocos construtivos fundamentais: HTML5, CSS3 e JavaScript (ES6+). Esta base garante que o aluno não se torne refém das ferramentas, mas sim um mestre capaz de manipulá-las.

### **Bloco 1 (0h \- 10h): Arquitetura Semântica e Estruturação de Documentos**

O objetivo deste bloco é erradicar vícios de marcação e estabelecer uma compreensão profissional da semântica web e acessibilidade. O aluno inicia a construção das interfaces estáticas do Projeto Autoral.

**Currículo Detalhado:**

* **Teoria da Web (2h):** O modelo Cliente-Servidor, o protocolo HTTP (Verbos, Status Codes, Headers) e o funcionamento do DNS. Como o navegador renderiza uma página (DOM Tree, Render Tree).  
* **HTML5 Semântico (3h):** A importância de \<main\>, \<nav\>, \<article\>, \<section\>, \<aside\> para SEO e leitores de tela. Diferença entre elementos de bloco e linha.  
* **Formulários Avançados (3h):** Inputs tipados (date, email, number), validação nativa do navegador (required, pattern), e a importância dos atributos name e id para o backend futuro.  
* **Acessibilidade (ARIA) (2h):** Introdução aos atributos aria-\* e boas práticas de contraste e navegação por teclado.

Aplicação no Projeto Autoral:  
O aluno deve criar a estrutura de arquivos do projeto (index.html, dashboard.html, login.html). Deve desenhar o esqueleto HTML de pelo menos 3 telas principais do sistema escolhido (ex: Tela de Login, Dashboard Inicial e Listagem de Registros), utilizando apenas HTML semântico, sem CSS.  

Entrega Funcional 01 (10h): Wireframe Semântico.  
Um conjunto de arquivos HTML navegáveis (via links) que representam a hierarquia de informação do sistema. O código deve passar 100% no validador W3C.

### **Bloco 2 (10h \- 20h): Estilização e Design Systems com CSS3**

O foco é o domínio do CSS "puro". O aluno deve aprender a gerenciar o layout, a tipografia e as cores sem depender de frameworks utilitários (como Tailwind) neste momento, para compreender o problema que eles resolvem posteriormente.

**Currículo Detalhado:**

* **A Cascata e Especificidade (2h):** Como o navegador decide qual estilo aplicar. O Box Model (margin, border, padding, content) e o box-sizing: border-box.  
* **Layout Moderno (Flexbox) (3h):** Eixos principais e transversais, alinhamento, distribuição de espaço (justify-content, align-items). Construção de menus e barras de navegação.  
* **Layout Bidimensional (Grid) (3h):** Criação de grids complexos para dashboards (grid-template-areas), gap e responsividade intrínseca.  
* **Variáveis CSS e Temas (2h):** Uso de Custom Properties (--primary-color) para definir o Design System do projeto.

Aplicação no Projeto Autoral:  
Estilização completa das telas HTML criadas no Bloco 1\. Implementação de um layout de Dashboard clássico (Sidebar fixa, Header fixo, Conteúdo rolável) usando CSS Grid e Flexbox. Definição da paleta de cores e tipografia do projeto.  
Entrega Funcional 02 (20h): Interface Estática Fiel.  
As telas do sistema devem ter aparência profissional, com hover states em botões e inputs estilizados. O layout deve ser fluido, mas ainda não necessariamente adaptado para mobile (responsividade fina).

### **Bloco 3 (20h \- 30h): Design Responsivo e Metodologias CSS**

Refinamento da interface para múltiplos dispositivos e organização do código CSS para escalabilidade.

**Currículo Detalhado:**

* **Media Queries e Breakpoints (3h):** Estratégia Mobile-First vs Desktop-First. Definição de breakpoints lógicos para o projeto (Mobile, Tablet, Desktop).  
* **Tipografia Responsiva (2h):** Unidades relativas (rem, em, vw, vh) versus unidades absolutas (px). Acessibilidade no redimensionamento de fontes.  
* **Metodologias de Organização (3h):** Introdução ao BEM (Block, Element, Modifier). Importância de não aninhar seletores excessivamente.  
* **Animações e Transições (2h):** Uso de transition e @keyframes para micro-interações (ex: fade-in de modais, feedback de clique).

Aplicação no Projeto Autoral:  
Tornar todas as telas do projeto autoral responsivas. O menu lateral deve colapsar em um menu "hambúrguer" no mobile. As tabelas de dados devem ter barra de rolagem horizontal ou transformar-se em cards em telas pequenas.  
Entrega Funcional 03 (30h): Protótipo Responsivo Navegável.  
O projeto deve ser acessível via celular e desktop, com adaptação fluida de layout. O código CSS deve estar organizado e comentado, utilizando variáveis para cores e espaçamentos.

### **Bloco 4 (30h \- 40h): Lógica de Programação com JavaScript (ES6+)**

Introdução à lógica computacional. O JavaScript é apresentado não como uma ferramenta de "efeitos", mas como uma linguagem de programação completa para manipulação de dados.6

**Currículo Detalhado:**

* **Sintaxe Moderna (3h):** let vs const vs var. Tipos de dados primitivos e objetos. Template Strings.  
* **Controle de Fluxo e Lógica (3h):** Condicionais (if, switch, ternários), Laços (for, while) e tratamento de erros (try/catch).  
* **Funções e Escopo (2h):** Arrow functions, funções anônimas, escopo léxico e closures.  
* **Manipulação de Arrays e Objetos (2h):** Métodos de alta ordem (map, filter, reduce, find) para manipulação de dados complexos.10

Aplicação no Projeto Autoral:  
Criação de scripts para manipular dados fictícios (mock data) do projeto. Exemplo: Criar um array de objetos JSON representando "Clientes" e escrever funções para filtrar clientes ativos, calcular a idade média ou ordenar por nome.  
Entrega Funcional 04 (40h): Módulo de Lógica de Negócios (Console).  
Um arquivo .js contendo funções puras que implementam regras de negócio do projeto (ex: calcularTotalPedido(itens), validarCPF(cpf)). Estas funções devem ser testadas no console do navegador.

### **Bloco 5 (40h \- 50h): O DOM e Interatividade**

Conectando a lógica JavaScript à interface HTML/CSS criada anteriormente.

**Currículo Detalhado:**

* **A Árvore DOM (3h):** Seleção de elementos (querySelector, getElementById). Navegação no DOM (pais, filhos, irmãos).  
* **Manipulação do DOM (3h):** Criar elementos (createElement), modificar classes (classList), alterar atributos e conteúdo dinamicamente.  
* **Eventos (2h):** addEventListener, o objeto Event, propagação de eventos (Bubbling vs Capturing). Delegação de eventos.  
* **Validação de Formulários (Client-Side) (2h):** Interceptar o submit, validar campos via JS e exibir mensagens de erro no DOM.

Aplicação no Projeto Autoral:  
Tornar os formulários estáticos funcionais no frontend. Ao clicar em "Salvar", o JS deve validar os dados e adicionar uma nova linha na tabela HTML (visualmente). Implementar a funcionalidade de "Excluir" linha da tabela e abrir/fechar modais via JS.  
Entrega Funcional 05 (50h): Interface Dinâmica (Client-Side).  
O sistema permite interações básicas: adicionar itens a uma lista, validar formulários e navegar entre abas ou modais sem recarregar a página (simulação de SPA).

### **Bloco 6 (50h \- 60h): Assincronismo e APIs**

Compreensão de como o frontend se comunica com o mundo exterior, preparando o terreno para o Livewire e consumo de dados.

**Currículo Detalhado:**

* **Assincronismo no JS (3h):** Callbacks, Promises e a sintaxe async/await. O Event Loop.  
* **Fetch API e JSON (3h):** Realizar requisições HTTP (GET, POST) via JS. Tratamento de respostas JSON.  
* **Armazenamento Local (2h):** localStorage e sessionStorage para persistir dados simples no navegador.  
* **Modularização (2h):** ES Modules (import/export) para organizar o código em múltiplos arquivos.

Aplicação no Projeto Autoral:  
Persistir os dados cadastrados no localStorage para que não sumam ao recarregar a página. Opcional: Consumir uma API pública (como ViaCEP) para preencher endereços automaticamente no cadastro de clientes.  
Entrega Funcional 06 (60h): Protótipo Funcional Persistente (Local).  
O "Frontend" do sistema está completo. É possível cadastrar, listar e excluir registros (usando LocalStorage). O código JS está modularizado e utiliza recursos modernos do ES6+.

## 4. Fase 2: Engenharia de Backend com Laravel (60h \- 120h)**

Nesta fase, o aluno transita do navegador para o servidor. O foco não é apenas aprender o framework Laravel, mas compreender a arquitetura MVC, modelagem de banco de dados e segurança. O Laravel é a fundação sobre a qual a TALL stack e o Filament são construídos.

### **Bloco 7 (60h \- 70h): PHP Moderno e Orientação a Objetos**

Antes do framework, o aluno deve dominar a linguagem PHP na versão 8.5+, focando em OOP, que é a base do Laravel

**Currículo Detalhado:**

* **Ambiente de Desenvolvimento (2h):** Setup do PHP, Composer e Servidor Local (Docker/Sail).  
* **Sintaxe PHP 8.5+ (3h):** Tipagem forte (string, int, void), Union Types, Named Arguments, Nullsafe Operator.  
* **Orientação a Objetos Avançada (3h):** Classes, Herança, Interfaces, Classes Abstratas. Injeção de Dependência (conceito).  
* **Traits e Enums (2h):** Uso de Traits para reutilização de código e Enums para tipar estados (ex: Status::ATIVO).

Aplicação no Projeto Autoral:  
Refatoração da lógica de negócio (antes em JS) para classes PHP. Criação de classes que representam as entidades do projeto (ex: class Cliente, class Pedido) com métodos para calcular totais ou formatar dados.  
Entrega Funcional 07 (70h): Biblioteca de Domínio PHP.  
Um conjunto de classes PHP testáveis (via script simples) que encapsulam a lógica do negócio, sem interface visual, apenas processamento de dados.

### **Bloco 8 (70h \- 80h): Arquitetura MVC e Rotas no Laravel**

Introdução ao Laravel 12\. Estrutura de diretórios, ciclo de vida da requisição e sistema de roteamento.

**Currículo Detalhado:**

* **Instalação e Estrutura (2h):** Análise do composer.json, .env, pasta app, config e routes. O Artisan CLI.  
* **Roteamento (3h):** Verbos HTTP, parâmetros de rota, rotas nomeadas, grupos de rotas e prefixos.  
* **Controllers (3h):** Criação de controllers, injeção de dependência básica, retorno de views e JSON.  
* **Request e Response (2h):** A classe Illuminate\\Http\\Request, captura de input, validação básica.

Aplicação no Projeto Autoral:  
Instalação do Laravel. Migração dos arquivos HTML da Fase 1 para Views Blade. Configuração das rotas para todas as telas do sistema. Criação dos Controllers para gerenciar a navegação.  
Entrega Funcional 08 (80h): Aplicação Laravel "Stateless".  
O projeto agora roda em Laravel. A navegação entre páginas funciona através de Rotas e Controllers. Formulários enviam dados para Controllers que os validam (mas ainda não salvam em banco).

### **Bloco 9 (80h \- 90h): Banco de Dados Relacional e Migrations**

Engenharia de dados. Transformar requisitos de negócio em um esquema de banco de dados sólido.

**Currículo Detalhado:**

* **Modelagem de Dados (3h):** Tabelas, Chaves Primárias, Chaves Estrangeiras, Normalização (1FN, 2FN, 3FN). Desenho do DER do projeto.  
* **Migrations (3h):** Criação e alteração de tabelas via código. Tipos de colunas (string, text, decimal, json).20  
* **Seeders e Factories (2h):** Geração de dados fictícios em massa para testes de carga e layout.  
* **Query Builder (2h):** Consultas diretas ao banco sem ORM para entendimento do SQL gerado.

Aplicação no Projeto Autoral:  
Criação das migrations para todas as entidades do sistema (ex: users, clients, products, orders, order\_items). Criação de Factories para popular o banco com 100 clientes e 500 pedidos fictícios.  
Entrega Funcional 09 (90h): Schema de Dados Versionado.  
O banco de dados do projeto pode ser recriado do zero com um único comando (php artisan migrate:fresh \--seed), populando o sistema com dados de teste consistentes.

### **Bloco 10 (90h \- 100h): Eloquent ORM e Relacionamentos**

O poder do Eloquent para abstrair operações de banco de dados e gerenciar relações complexas.

**Currículo Detalhado:**

* **Eloquent Models (3h):** Convenções, Mass Assignment ($fillable), Accessors e Mutators.  
* **Relacionamentos (4h):** hasOne, hasMany, belongsTo, belongsToMany (Pivot tables). Como definir e consultar relações.  
* **CRUD Completo (3h):** Implementar Create, Read, Update, Delete usando Eloquent nos Controllers.

Aplicação no Projeto Autoral:  
Conectar as Views e Controllers ao Banco de Dados. As listagens agora mostram dados reais do banco. Os formulários criam registros no banco. Implementar a visualização de detalhes (ex: ver um Pedido e seus Itens relacionados).  
Entrega Funcional 10 (100h): CRUD Relacional Funcional.  
O sistema permite gerenciar as principais entidades. As relações são salvas corretamente (ex: salvar um pedido cria registros na tabela de pedidos e na tabela de itens).

### **Bloco 11 (100h \- 110h): Blade Templating e Frontend Assets**

Refinamento da camada de visualização e integração de assets.11

**Currículo Detalhado:**

* **Blade Avançado (3h):** Herança de layouts (@extends), Componentes Blade (\<x-alert /\>), Diretivas de controle (@if, @foreach, @auth).  
* **Vite no Laravel (3h):** Compilação de assets (CSS/JS). Importação de imagens e fontes.  
* **Componentização (4h):** Criar componentes reutilizáveis para Cards, Modais, Tabelas e Botões usando Blade.

Aplicação no Projeto Autoral:  
Refatoração das Views para usar um Layout Mestre. Criação de componentes Blade para elementos repetitivos. Garantir que o design (CSS da Fase 1\) esteja perfeitamente integrado.  
Entrega Funcional 11 (110h): Interface Modularizada.  
O código frontend está limpo e modular. Alterar o Layout Mestre reflete em todas as páginas. O sistema visualmente está polido.

### **Bloco 12 (110h \- 120h): Autenticação, Autorização e Segurança**

Protegendo a aplicação e definindo quem pode fazer o que.

**Currículo Detalhado:**

* **Autenticação (3h):** Laravel Breeze ou implementação manual. Login, Registro, Reset de Senha.  
* **Middleware (2h):** Proteção de rotas. Criar middlewares customizados (ex: CheckAdmin).  
* **Autorização (3h):** Gates e Policies. Controlar acesso a recursos específicos (ex: usuário só edita o próprio perfil).  
* **Segurança (2h):** Proteção CSRF, XSS, SQL Injection (como o Eloquent protege).

Aplicação no Projeto Autoral:  
Implementar sistema de login. Criar níveis de acesso (ex: Admin vs Usuário Comum). Proteger as rotas administrativas. Garantir que usuários não possam ver ou editar dados uns dos outros (se aplicável).  
Entrega Funcional 12 (120h): Sistema Seguro e Multi-Usuário.  
O projeto tem controle de acesso robusto. Tentar acessar uma URL protegida sem logar redireciona para o login. Tentar editar dados alheios retorna erro 403\.

## 5. Fase 3: A Stack TALL e a Reatividade Moderna (120h \- 180h)

Com o backend sólido, o curso entra na especialização da stack TALL. O objetivo é substituir o desenvolvimento tradicional (recarregamento de página) por interfaces reativas modernas sem a complexidade de SPAs baseadas em API (como React/Vue).

### **Bloco 13 (120h \- 130h): Tailwind CSS \- A Revolução Utilitária**

Adoção do Tailwind para acelerar a estilização e padronização visual.24

**Currículo Detalhado:**

* **Filosofia Utility-First (3h):** Por que usar classes utilitárias? Configuração do tailwind.config.js. O compilador JIT.  
* **Core Concepts (4h):** Espaçamento, Cores, Tipografia, Flexbox e Grid com Tailwind. Estados (hover, focus, active).  
* **Responsividade e Dark Mode (3h):** Modificadores responsivos (md:, lg:). Implementação de tema escuro (dark:).

Aplicação no Projeto Autoral:  
Migração completa do CSS "vanilla" da Fase 1 para Tailwind CSS. Refatoração das Views Blade para usar classes utilitárias. Implementação de um toggle Dark/Light mode funcional.  
Entrega Funcional 13 (130h): UI Refatorada com Tailwind.  
O projeto deve ter o código CSS limpo (quase inexistente, substituído por classes Tailwind). A interface deve ser idêntica ou superior à anterior, com suporte nativo a modo escuro.

### **Bloco 14 (130h \- 140h): Alpine.js \- Interatividade Declarativa**

Adição de comportamento JavaScript leve diretamente no HTML, substituindo scripts manuais.22

**Currículo Detalhado:**

* **Fundamentos (3h):** x-data, x-bind, x-on. Estado local do componente.  
* **Controle de Visibilidade (3h):** x-show, x-if, x-transition. Animações suaves de entrada e saída.  
* **Manipulação de Dados (4h):** x-model (Two-way binding), x-for (Listas). Fetching de dados com Alpine.

Aplicação no Projeto Autoral:  
Substituir lógicas JS manuais (como abrir modal, dropdowns, tabs) por componentes Alpine. Criar componentes interativos como "Dropdown de Notificações" ou "Modal de Confirmação" usando Alpine.  
Entrega Funcional 14 (140h): Frontend Reativo com Alpine.  
A interface responde instantaneamente a interações do usuário. Modais e menus têm animações fluidas. Código JS "spaghetti" foi removido.

### **Bloco 15 (140h \- 150h): Introdução ao Livewire 3**

O componente central da TALL stack. Conectando o Frontend ao Backend sem escrever APIs.28

**Currículo Detalhado:**

* **Arquitetura Livewire (3h):** Como funciona o ciclo de roundtrip AJAX. Hydration e Dehydration. Instalação do Livewire 3\.  
* **Componentes (3h):** Criação de componentes (php artisan make:livewire). Propriedades públicas e data binding (wire:model).  
* **Ações e Eventos (4h):** Disparar métodos PHP via frontend (wire:click). Passagem de parâmetros. Lifecycle Hooks (mount, render).

Aplicação no Projeto Autoral:  
Converter os formulários de cadastro (antes Controllers padrão) para Componentes Livewire. Implementar validação em tempo real ("Real-time validation") nos formulários.  
Entrega Funcional 15 (150h): Formulários Reativos.  
Os formulários principais do sistema validam e salvam dados sem recarregar a página. Feedback visual de erros é instantâneo.

### **Bloco 16 (150h \- 160h): Livewire Avançado e Tabelas**

Dominando listagens de dados dinâmicas e funcionalidades complexas.

**Currículo Detalhado:**

* **Paginação e Filtros (3h):** Implementar busca e filtros (por data, status) em tempo real usando Livewire e Query Strings.  
* **Loading States (2h):** Feedback visual de carregamento (wire:loading). Desabilitar botões durante o processamento.  
* **Comunicação entre Componentes (3h):** Eventos globais ($dispatch), Nesting de componentes (Pai/Filho) e listeners.  
* **Upload de Arquivos (2h):** Traits de upload do Livewire. Preview de imagem temporária.

Aplicação no Projeto Autoral:  
Criar uma listagem de registros poderosa: com barra de busca, filtros por categoria e ordenação, tudo atualizando via AJAX. Implementar upload de arquivos (avatar do usuário ou documentos) via Livewire.  
Entrega Funcional 16 (160h): Datatables Dinâmicas.  
O sistema possui listagens ricas e rápidas. A experiência de usuário é de uma SPA. Uploads funcionam com barra de progresso e preview.

### **Bloco 17 (160h \- 170h): Integração Alpine \+ Livewire e Otimização**

O poder combinado das ferramentas e a "cola" da stack.

**Currículo Detalhado:**

* **Entangle (3h):** Sincronizando estado entre Alpine e Livewire (@entangle). Criar componentes híbridos complexos.  
* **Wire Navigate (2h):** Transformando a aplicação em SPA real com wire:navigate (feature do Livewire 3).  
* **Modularização com Blade Components (3h):** Criar inputs, modais e botões altamente reutilizáveis que aceitam atributos Livewire.  
* **Performance (2h):** wire:key para evitar problemas de DOM diffing. Lazy Loading de componentes pesados.

Aplicação no Projeto Autoral:  
Refinamento da UX. Implementar navegação SPA completa. Criar componentes de UI (ex: Datepicker customizado) que usa Alpine para a interface e Livewire para os dados.  
Entrega Funcional 17 (170h): Aplicação SPA (Single Page Application).  
Navegação instantânea entre páginas. Estado da interface é mantido. Componentes complexos funcionam sem bugs de sincronia.

## 6. Fase 4: Desenvolvimento Acelerado com FilamentPHP (170h \- 230h)

A fase final foca na produtividade extrema. Tendo aprendido a construir tudo manualmente nas fases anteriores, o aluno agora utiliza o **Filament** para gerar painéis administrativos complexos em uma fração do tempo. O Filament é construído sobre a TALL stack, então todo o conhecimento anterior é aproveitado.35

### **Bloco 18 (170h \- 180h): Fundamentos do Filament Panel**

Instalação e criação dos primeiros recursos administrativos.

**Currículo Detalhado:**

* **Instalação e Configuração (2h):** Instalando o pacote, criando um User Admin. Configuração do tema e branding (logo, cores).  
* **Resources (4h):** O conceito de Resource. Gerando CRUDs automáticos (make:filament-resource). Estrutura de pastas do Filament.  
* **Form Builder Básico (4h):** Definição de esquemas de formulário (TextInput, Select, Toggle, DatePicker). Validação automática.

Aplicação no Projeto Autoral:  
Gerar um Painel Administrativo (/admin) para o projeto. Criar Resources para as entidades principais (Clientes, Produtos, etc.). Recriar os formulários manuais da Fase 3 usando o Form Builder do Filament.  
Entrega Funcional 18 (180h): Painel Administrativo Básico.  
Um backend administrativo funcional onde é possível criar, editar e excluir registros. O design já é profissional e responsivo por padrão.

### **Bloco 19 (180h \- 190h): Tabelas e Listagens Avançadas no Filament**

Dominando o Table Builder para exibição de dados.35

**Currículo Detalhado:**

* **Colunas (3h):** Tipos de colunas (TextColumn, ImageColumn, IconColumn, ColorColumn). Formatação de dados (moeda, data).  
* **Filtros e Buscas (3h):** Filter, SelectFilter, TernaryFilter. Configuração de busca global e busca por coluna.  
* **Ações de Tabela (4h):** EditAction, DeleteAction, BulkActions (ações em massa). Criar ações customizadas na linha da tabela.

Aplicação no Projeto Autoral:  
Configurar as listagens do painel. Adicionar filtros relevantes (ex: "Mostrar apenas pedidos pendentes"). Configurar colunas com badges coloridos para status. Implementar exportação de dados (se necessário).  
Entrega Funcional 19 (190h): Gestão de Dados Avançada.  
O administrador consegue visualizar, filtrar e manipular os dados com eficiência. As tabelas apresentam informações ricas (imagens, status coloridos).

### **Bloco 20 (190h \- 200h): Relacionamentos e Formulários Complexos**

Gerenciando estruturas de dados complexas e aninhadas.37

**Currículo Detalhado:**

* **Relation Managers (4h):** Gerenciar registros filhos dentro da página do pai (ex: Listar "Itens" dentro da edição de "Pedido").  
* **Componentes de Layout (3h):** Grid, Section, Wizard, Tabs. Organizar formulários longos.  
* **Componentes Complexos (3h):** Repeater (para linhas dinâmicas de itens), Builder (para conteúdo flexível). Lógica condicional em campos.

Aplicação no Projeto Autoral:  
Implementar o formulário de "Criação de Pedido" (ou similar complexo) no Filament. Usar Repeater para adicionar itens ao pedido dinamicamente. Usar Wizard para dividir um cadastro longo em passos.  
Entrega Funcional 20 (200h): Formulários Mestre-Detalhe.  
O sistema suporta entrada de dados complexos e relacionais em uma única interface intuitiva.

### **Bloco 21 (200h \- 210h): Dashboards, Widgets e Infolists**

Transformando dados em informação gerencial.39

**Currículo Detalhado:**

* **Widgets de Estatísticas (3h):** Criar cards de KPI (Total Vendas, Novos Usuários).  
* **Gráficos (4h):** Chart Widgets (Linha, Barra, Pizza). Alimentar gráficos com dados do Eloquent. Filtros em gráficos.  
* **Infolists (3h):** Criar páginas de visualização ("Read-only") detalhadas, separadas dos formulários de edição.35

Aplicação no Projeto Autoral:  
Criar um Dashboard inicial rico. Gráficos mostrando a evolução mensal de métricas do projeto. Cards com totais e tendências.  
Entrega Funcional 21 (210h): Dashboard de Business Intelligence.  
A página inicial do painel oferece uma visão macro do negócio. Os gráficos são reais e interativos.

### **Bloco 22 (210h \- 220h): Customização Extrema e Plugins**

Indo além do padrão do Filament.42

**Currículo Detalhado:**

* **Custom Pages (3h):** Criar páginas inteiras customizadas dentro do painel (sem ser Resource).  
* **Custom Actions (3h):** Modais com lógica de negócio específica (ex: "Aprovar Orçamento" com campo de observação).  
* **Plugins (4h):** Instalação de plugins da comunidade (ex: Spatie Medialibrary, Activity Log, Shield para permissões).

Aplicação no Projeto Autoral:  
Implementar funcionalidades específicas que o CRUD padrão não cobre. Instalar plugin de Permissões (Shield) para criar papéis de "Admin" e "Editor". Personalizar o CSS do painel.  
Entrega Funcional 22 (220h): Sistema Extensível e Personalizado.  
O Filament não parece um "admin genérico", mas sim uma aplicação sob medida. Controle de permissões (ACL) está ativo.

### **Bloco 23 (220h \- 230h): Deploy, Produção e Carreira**

Preparação para o lançamento e para o mercado de trabalho.

**Currículo Detalhado:**

* **Otimização e Cache (3h):** Cache de rotas, config e views. Otimização do Autoloader.  
* **Deploy (4h):** Provisionamento de servidor (VPS), configuração de Nginx/Apache, SSL, Supervisor (para filas). Uso de Laravel Forge ou Ploi (conceito).  
* **CI/CD (3h):** GitHub Actions para rodar testes antes do deploy.

Aplicação no Projeto Autoral:  
Colocar o projeto em produção (em uma VPS real ou PaaS como Railway). Configurar domínio e HTTPS.  
Entrega Final (230h): Projeto em Produção.  
O "Projeto Autoral" está acessível publicamente. O aluno possui um portfólio com código fonte no GitHub e a aplicação rodando.

## ---

**Conclusão e Perspectivas**

Este plano de curso de 230 horas oferece um roteiro rigoroso e estruturado para a formação de um desenvolvedor Full Stack especializado na stack TALL e Filament. Ao obrigar o aluno a passar pelas camadas fundamentais (HTML/JS) antes de chegar às abstrações (Filament), garante-se a formação de um profissional capaz de resolver problemas complexos, e não apenas de configurar ferramentas. A metodologia de entregas a cada 10 horas assegura ritmo, consistência e a construção de um portfólio robusto, diferenciando o autodidata no mercado de trabalho competitivo.

#### **Referências citadas**

1. Gold Standard PBL: Essential Project Design Elements \- PBLWorks, acessado em dezembro 2, 2025, [https://www.pblworks.org/what-is-pbl/gold-standard-project-design](https://www.pblworks.org/what-is-pbl/gold-standard-project-design)  
2. Project based learning. TLDR | by Manuel Miglioranza \- Medium, acessado em dezembro 2, 2025, [https://medium.com/@mmiglioranza22/project-based-learning-d2f09b7e6996](https://medium.com/@mmiglioranza22/project-based-learning-d2f09b7e6996)  
3. 8 Essential Milestones to Minimize Software Development Project Risks \- soltech, acessado em dezembro 2, 2025, [https://soltech.net/essential-milestones-to-minimize-software-development-project-risks/](https://soltech.net/essential-milestones-to-minimize-software-development-project-risks/)  
4. Managing Milestones and Web development Project \- Stack Overflow, acessado em dezembro 2, 2025, [https://stackoverflow.com/questions/714663/managing-milestones-and-web-development-project](https://stackoverflow.com/questions/714663/managing-milestones-and-web-development-project)  
5. File Structure : Broad Institute of MIT and Harvard, acessado em dezembro 2, 2025, [https://mitcommlab.mit.edu/broad/commkit/file-structure/](https://mitcommlab.mit.edu/broad/commkit/file-structure/)  
6. Web Development Syllabus 2025 | HTML, CSS, JavaScript & Frameworks \- Uncodemy, acessado em dezembro 2, 2025, [https://uncodemy.com/web-development-syllabus](https://uncodemy.com/web-development-syllabus)  
7. Learn web development | MDN, acessado em dezembro 2, 2025, [https://developer.mozilla.org/en-US/docs/Learn\_web\_development](https://developer.mozilla.org/en-US/docs/Learn_web_development)  
8. Introduction to HTML, CSS, & JavaScript \- Coursera, acessado em dezembro 2, 2025, [https://www.coursera.org/learn/introduction-html-css-javascript](https://www.coursera.org/learn/introduction-html-css-javascript)  
9. Styling with utility classes \- Core concepts \- Tailwind CSS, acessado em dezembro 2, 2025, [https://tailwindcss.com/docs/styling-with-utility-classes](https://tailwindcss.com/docs/styling-with-utility-classes)  
10. JavaScript Essentials for PHP Developers \- Laracasts, acessado em dezembro 2, 2025, [https://laracasts.com/series/javascript-essentials-for-php-developers](https://laracasts.com/series/javascript-essentials-for-php-developers)  
11. Full Stack Web Development for Beginners (Full Course on HTML, CSS, JavaScript, Node.js, MongoDB) \- YouTube, acessado em dezembro 2, 2025, [https://www.youtube.com/watch?v=nu\_pCVPKzTk](https://www.youtube.com/watch?v=nu_pCVPKzTk)  
12. 30 Days to Learn Laravel \- Laracasts, acessado em dezembro 2, 2025, [https://laracasts.com/series/30-days-to-learn-laravel-11](https://laracasts.com/series/30-days-to-learn-laravel-11)  
13. Laravel 11 \- The Complete Beginner's Guide\! \- YouTube, acessado em dezembro 2, 2025, [https://www.youtube.com/watch?v=YC2VuowVkYc](https://www.youtube.com/watch?v=YC2VuowVkYc)  
14. PHP Full Course 2025 \- Learn PHP from Scratch | PHP Tutorial for Beginners \- YouTube, acessado em dezembro 2, 2025, [https://www.youtube.com/watch?v=l4\_Vn-sTBL8](https://www.youtube.com/watch?v=l4_Vn-sTBL8)  
15. Learn Object Oriented PHP for Beginners \- OOP PHP Tutorial from Dani Krossing, acessado em dezembro 2, 2025, [https://www.classcentral.com/course/youtube-learn-object-oriented-php-for-beginners-with-examples-to-help-you-understand-oop-php-tutorial-204721](https://www.classcentral.com/course/youtube-learn-object-oriented-php-for-beginners-with-examples-to-help-you-understand-oop-php-tutorial-204721)  
16. What's New in PHP 8.3 \- InstaWP, acessado em dezembro 2, 2025, [https://instawp.com/php-8-3-update-for-wordpress-sites/](https://instawp.com/php-8-3-update-for-wordpress-sites/)  
17. Front Line PHP: Building modern web applications with PHP 8.3, acessado em dezembro 2, 2025, [https://front-line-php.com/](https://front-line-php.com/)  
18. Traits \- Manual \- PHP, acessado em dezembro 2, 2025, [https://www.php.net/manual/en/language.oop5.traits.php](https://www.php.net/manual/en/language.oop5.traits.php)  
19. acessado em dezembro 31, 1969, [https://laravel.com/docs/11.x/readme](https://laravel.com/docs/11.x/readme)  
20. Database: Migrations \- Laravel 12.x \- The PHP Framework For Web ..., acessado em dezembro 2, 2025, [https://laravel.com/docs/11.x/migrations](https://laravel.com/docs/11.x/migrations)  
21. Eloquent: Relationships \- Laravel 12.x \- The PHP Framework For ..., acessado em dezembro 2, 2025, [https://laravel.com/docs/11.x/eloquent-relationships](https://laravel.com/docs/11.x/eloquent-relationships)  
22. Leveraging Alpine.js with Livewire 3.0 for Advanced Interactivity \- Wontonee, acessado em dezembro 2, 2025, [https://wontonee.com/leveraging-alpine-js-with-livewire-3-0-for-advanced-interactivity/](https://wontonee.com/leveraging-alpine-js-with-livewire-3-0-for-advanced-interactivity/)  
23. Advanced Laravel Livewire, acessado em dezembro 2, 2025, [https://laraveldaily.com/course/livewire-advanced](https://laraveldaily.com/course/livewire-advanced)  
24. Tailwind CSS \- Rapidly build modern websites without ever leaving your HTML., acessado em dezembro 2, 2025, [https://tailwindcss.com/](https://tailwindcss.com/)  
25. Getting Started With TailwindCSS. Tailwind is a utility-based css… | by Matt Burgess, acessado em dezembro 2, 2025, [https://mattburgess.medium.com/getting-started-with-tailwindcss-3190def35361](https://mattburgess.medium.com/getting-started-with-tailwindcss-3190def35361)  
26. My Journey from BootstrapCSS to TailwindCSS: A Backend Developer's Perspective, acessado em dezembro 2, 2025, [https://dev.to/msulaimanmisri/my-journey-from-bootstrapcss-to-tailwindcss-a-backend-developers-perspective-2n1c](https://dev.to/msulaimanmisri/my-journey-from-bootstrapcss-to-tailwindcss-a-backend-developers-perspective-2n1c)  
27. Alpine.js, acessado em dezembro 2, 2025, [https://alpinejs.dev/](https://alpinejs.dev/)  
28. Alpine \- Laravel Livewire, acessado em dezembro 2, 2025, [https://livewire.laravel.com/docs/3.x/alpine](https://livewire.laravel.com/docs/3.x/alpine)  
29. Laravel Modal Using Alpine JS \+ Livewire 3 \- YouTube, acessado em dezembro 2, 2025, [https://www.youtube.com/watch?v=ZQJhabcophk](https://www.youtube.com/watch?v=ZQJhabcophk)  
30. Laravel Livewire: An In-Depth Exploration of Empowering Interactive Web Applications, acessado em dezembro 2, 2025, [https://pbcmedia.medium.com/laravel-livewire-an-in-depth-exploration-of-empowering-interactive-web-applications-7eb6d485492](https://pbcmedia.medium.com/laravel-livewire-an-in-depth-exploration-of-empowering-interactive-web-applications-7eb6d485492)  
31. Livewire Best Practices \- Heiko Klingele, acessado em dezembro 2, 2025, [https://heikoklingele.de/blog/livewire-best-practices](https://heikoklingele.de/blog/livewire-best-practices)  
32. Laravel Livewire Crash Course \#3 \- Actions \- YouTube, acessado em dezembro 2, 2025, [https://www.youtube.com/watch?v=AL85KWfJRP8](https://www.youtube.com/watch?v=AL85KWfJRP8)  
33. AlpineJS | Laravel Livewire, acessado em dezembro 2, 2025, [https://laravel-livewire.com/docs/2.x/alpine-js](https://laravel-livewire.com/docs/2.x/alpine-js)  
34. JavaScript | Laravel Livewire, acessado em dezembro 2, 2025, [https://livewire.laravel.com/docs/3.x/javascript](https://livewire.laravel.com/docs/3.x/javascript)  
35. Getting started \- Panels \- Filament, acessado em dezembro 2, 2025, [https://filamentphp.com/docs/3.x/panels/getting-started](https://filamentphp.com/docs/3.x/panels/getting-started)  
36. All Classes | Filament API, acessado em dezembro 2, 2025, [https://filamentphp.com/api/2.x/classes.html](https://filamentphp.com/api/2.x/classes.html)  
37. Nested resources \- Filament, acessado em dezembro 2, 2025, [https://filamentphp.com/docs/4.x/resources/nesting/](https://filamentphp.com/docs/4.x/resources/nesting/)  
38. Managing relationships \- Panels \- Filament, acessado em dezembro 2, 2025, [https://filamentphp.com/docs/3.x/panels/resources/relation-managers](https://filamentphp.com/docs/3.x/panels/resources/relation-managers)  
39. Overview \- Widgets \- Filament, acessado em dezembro 2, 2025, [https://filamentphp.com/docs/4.x/widgets/overview/](https://filamentphp.com/docs/4.x/widgets/overview/)  
40. Dashboard \- Panels \- Filament, acessado em dezembro 2, 2025, [https://filamentphp.com/docs/3.x/panels/dashboard](https://filamentphp.com/docs/3.x/panels/dashboard)  
41. Widgets \- Panels \- Filament, acessado em dezembro 2, 2025, [https://filamentphp.com/docs/3.x/panels/resources/widgets](https://filamentphp.com/docs/3.x/panels/resources/widgets)  
42. Advanced forms \- Forms \- Filament, acessado em dezembro 2, 2025, [https://filamentphp.com/docs/3.x/forms/advanced](https://filamentphp.com/docs/3.x/forms/advanced)  
43. Custom components \- Schemas \- Filament, acessado em dezembro 2, 2025, [https://filamentphp.com/docs/4.x/schemas/custom-components/](https://filamentphp.com/docs/4.x/schemas/custom-components/)