---
title: Github Data
description:
imageHeader: "/images/github-data-project-logo.jpg"
cover: "/images/github-data-project-logo.jpg"
date: 2017-03-20 16:30
modifiedDate:
channel: Devs
category: Pessoal
tags:
  - Projeto pessoal
layout: landscape-layout
filter: filter-burn
typography:
draft: false
authors:
  - name: Julian Silva da Cunha
    quote:
gallery:
---

Recentemente, ao ler alguns artigos, vi um projeto em que um desenvolvedor utilizava a API do GitHub para pesquisar por um nome de usuário e exibir informações básicas sobre ele. Inspirado por isso, decidi criar minha própria versão dessa aplicação, buscando incluir mais informações detalhadas sobre o usuário.

Para desenvolver essa aplicação, utilizei algumas tecnologias atuais, entre elas:

- **Svelte/SvelteKit**: já tinha testado o Svelte anteriormente e sempre tive interesse em criar um projeto completo com ele. Acho o Svelte similar ao Vue, meu primeiro framework e com o qual trabalhei profissionalmente.
- **Octokit e GitHub API**: para acessar dados do GitHub, usei o Octokit, que facilita as buscas e permite um número maior de requisições com autenticação.
- **@tanstack/query**: essencial para gerenciar melhor as buscas e o cache dos dados obtidos.
- **Shadcn-svelte**: como gosto de usar o ShadcnUI com React/Next.js, optei por uma versão compatível com Svelte, com componentes fáceis de usar e estilizar com TailwindCSS.
- **Vercel**: usei para deploy. Normalmente, crio sites estáticos com GitHub Pages, mas, neste caso, a aplicação requer buscas dinâmicas de dados, então a Vercel foi mais adequada.
- **v0**: usei essa IA como base para criar o componente de exibição de contribuições e para configurar queries de contribuições e repositórios fixados em GraphQL. Como v0 é voltado para React, tive que ajustar o componente para que funcionasse corretamente em Svelte.
- **Lucide Icons, Phosphor Icons e fonte Inter**: escolhi essas bibliotecas de ícones e a fonte Inter para a tipografia geral da aplicação.

A aplicação está disponível em [https://githubdata.ultimatemercer.com/](https://githubdata.ultimatemercer.com/?un=ultimatemercer).

Você também pode acessá-la com um nome de usuário pré-definido, por exemplo: [https://githubdata.ultimatemercer.com/?un=ultimatemercer](https://githubdata.ultimatemercer.com/?un=ultimatemercer). Assim, ao carregar o site, ele já exibe os dados do usuário.

Realizei um teste de desempenho com o Lighthouse para verificar performance, acessibilidade, boas práticas e SEO, e obtive resultados excelentes. Embora haja uma leve oscilação na performance, os resultados iniciais foram melhores do que eu esperava, dado que não foquei tanto em otimização de performance.

![Performance Lighthouse](../../../../images/github-data-project-performance.jpg)

### Algumas capturas de tela da aplicação:

![Captura 1](../../../../images/github-data-project-1.jpg)

![Captura 2](../../../../images/github-data-project-2.jpg)

![Captura 3](../../../../images/github-data-project-3.jpg)

Desenvolver esse projeto foi uma experiência valiosa, tanto em termos de aprendizado quanto no uso de ferramentas. Um ponto de melhoria seria a fase de planejamento, já que precisei refatorar a estrutura para integrar o @tanstack/query.

### Próximos Passos

Ainda quero melhorar alguns pontos no projeto (dei uma pausa no momento). Os principais pontos a trabalhar são:

- Adicionar testes unitários;
- Aperfeiçoar o carregamento de dados com um nome de usuário pré-definido;
- Ajustar alguns detalhes de design.

Atenciosamente,  
Julian Silva da Cunha
