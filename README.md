# Portfólio de QA — Ingrid Matos

Portfólio de testes manuais e automatizados desenvolvido no bootcamp de **Analista de QA da TripleTen**, com oito projetos que cobrem teste funcional, design de teste, teste web cross-browser, teste de API REST, teste mobile, análise de logs com SQL, automação de testes web com Python e Selenium e um projeto final que integra testes web, mobile e de API.

Cada repositório traz os artefatos em Markdown, legíveis direto no navegador: casos de teste, checklists, classes de equivalência e relatórios de defeito com passos de reprodução.

## Visão geral

| Sprint | Foco | Verificações | Defeitos | Repositório |
|---|---|---|---|---|
| 1 | Testes funcionais (Urban Routes) | 37 casos de teste | 5 | [Ver projeto](https://github.com/ingridmatosn/Qa-Sprint1-Testes-Funcionais) |
| 2 | Design de teste: BVA e partição de equivalência | 44 classes, 14 casos | 1 crítico documentado | [Ver projeto](https://github.com/ingridmatosn/QA-Sprint2-Design-de-Testes) |
| 3 | Web cross-browser e layout | 104 verificações | 32 | [Ver projeto](https://github.com/ingridmatosn/Qa-Sprint3-Testes-Web) |
| 4 | API REST (Postman) | 70 casos de teste | 44 | [Ver projeto](https://github.com/ingridmatosn/QA-Sprint4-Testes-API) |
| 5 | Mobile end-to-end (Urban Lunch) | 36 verificações | 6 | [Ver projeto](https://github.com/ingridmatosn/QA-Sprint5-Testes-Mobile) |
| 6 | Terminal e banco de dados | 6 tarefas práticas | — | [Ver projeto](https://github.com/ingridmatosn/QA-Sprint6-Terminal-Database) |
| 7 e 8 | Automação E2E (Python, Selenium, Pytest, POM) | 8 testes automatizados | — | [Ver projeto](https://github.com/ingridmatosn/QA-Brazil_Python_Automation) |
| 9 | Projeto final: web, mobile e API (Urban Scooter) | 105 casos de teste | 41 | [Ver projeto](https://github.com/ingridmatosn/QA-Projeto-Final-Urban-Scooter) |

**Totais:** nos sprints 1 a 6, 261 verificações registradas e **87 defeitos com identificador rastreável** no Jira (BR-001 a BR-005 e KAN-1 a KAN-83). No projeto final, mais **105 casos de teste e 41 defeitos** (KAN-84 a KAN-124).

## Projetos em destaque

### Projeto final: web, mobile e API — 105 casos, 41 defeitos, projeto aprovado
[QA-Projeto-Final-Urban-Scooter](https://github.com/ingridmatosn/QA-Projeto-Final-Urban-Scooter)

Testes do serviço Urban Scooter em três frentes: formulário web em Chrome e Opera (52 casos), aplicativo mobile do entregador no emulador Android, incluindo notificações e falha de conexão (17 casos), e API do backend para criar e excluir entregadores (36 casos). Os destaques foram a API respondendo **201 Created** para dados que deveriam ser rejeitados, um **500 Internal Server Error** no DELETE com id inválido e a exclusão de entregador que **não apaga os pedidos vinculados**.

### Automação de testes E2E — 8 testes, projeto aprovado
[QA-Brazil_Python_Automation](https://github.com/ingridmatosn/QA-Brazil_Python_Automation)

Automação do fluxo completo de pedido de táxi do app web Urban Routes com Python, Selenium WebDriver e Pytest, no padrão **Page Object Model**. Os testes cobrem rota, tarifa, cadastro de telefone com código SMS, cartão, comentário para o motorista, itens extras e o modal de busca de carro, usando esperas explícitas no lugar de pausas fixas.

### Testes de API REST — 70 casos, 44 defeitos
[QA-Sprint4-Testes-API](https://github.com/ingridmatosn/QA-Sprint4-Testes-API)

Testes de dois endpoints REST no Postman. O achado principal não foi um defeito isolado, e sim um padrão: a API respondia **500 Internal Server Error** em cenários que exigiam **400 Bad Request** — erro do cliente devolvido como falha do servidor. Isso impede o cliente de se corrigir, polui o monitoramento e desvia a investigação de produção. Recomendação registrada: bloquear a release até a correção do tratamento de erros.

### Design de testes com BVA e partição de equivalência — 44 classes
[QA-Sprint2-Design-de-Testes](https://github.com/ingridmatosn/QA-Sprint2-Design-de-Testes)

Casos desenhados antes da execução, com partição de equivalência e análise de valor limite em um formulário de cadastro. A classe "29 de fevereiro em ano não bissexto" expôs o defeito mais grave: o sistema aceitou **29/02/2005**, data que não existe. A validação de fevereiro existia, mas ignorava a regra de ano bissexto.

### Testes web cross-browser — 104 verificações, 32 defeitos
[Qa-Sprint3-Testes-Web](https://github.com/ingridmatosn/Qa-Sprint3-Testes-Web)

Layout comparado ao design e validações do formulário de pagamento, em Chrome 800x600 e Firefox 1920x1080. Ao fim do sprint, **não recomendei o lançamento do produto**, pela quantidade e gravidade dos defeitos, incluindo uma falha crítica que impedia o cancelamento de corridas.

## Competências demonstradas

**Técnicas de teste:** partição de equivalência, análise de valor limite, teste funcional, teste de regressão, teste exploratório de layout, teste end-to-end.

**Automação:** Python, Selenium WebDriver, Pytest e Page Object Model (POM).

**Tipos de aplicação:** web, mobile e APIs REST.

**Documentação:** casos de teste com pré-condição, etapas e resultado esperado; checklists por seção; relatórios de defeito com passos de reprodução, resultado esperado, resultado real e prioridade.

**Ferramentas:** Jira, Postman, DevTools, emulador Android, Cygwin/Bash, PostgreSQL, Python, Selenium WebDriver, Pytest, PyCharm, Git e GitHub.

## Como este portfólio está organizado

Cada repositório de sprint tem:

- um **README** com objetivo, escopo, técnicas aplicadas, resultados, defeitos, ferramentas, aprendizados e melhorias pendentes;
- os **artefatos em Markdown**, que abrem direto no GitHub, sem download;
- a **planilha ou documento original** da entrega.

## Sobre mim

Analista de QA em formação pela TripleTen, com mais de 8 anos de experiência anterior em atendimento e suporte operacional de alta demanda — o que me acostumou a ouvir o problema do ponto de vista de quem usa o produto e a registrar cada passo do que aconteceu.

Busco a primeira oportunidade como QA Júnior, Manual QA Tester ou QA Intern, em modelo remoto ou híbrido.

---

**Ingrid Matos** — Analista de QA Júnior
Feira de Santana, Bahia, Brasil
[LinkedIn](https://www.linkedin.com/in/ingridmatosn/) · [GitHub](https://github.com/ingridmatosn) · ingridmatosyt01@gmail.com
# Portfólio de QA — Ingrid Matos

Portfólio de testes manuais e automatizados desenvolvido no bootcamp de **Analista de QA da TripleTen**, com sete projetos que cobrem teste funcional, design de teste, teste web cross-browser, teste de API REST, teste mobile, análise de logs com SQL e automação de testes web com Python e Selenium.

Cada repositório traz os artefatos em Markdown, legíveis direto no navegador: casos de teste, checklists, classes de equivalência e relatórios de defeito com passos de reprodução.

## Visão geral

| Sprint | Foco | Verificações | Defeitos | Repositório |
|---|---|---|---|---|
| 1 | Testes funcionais (Urban Routes) | 37 casos de teste | 5 | [Ver projeto](https://github.com/ingridmatosn/Qa-Sprint1-Testes-Funcionais) |
| 2 | Design de teste: BVA e partição de equivalência | 44 classes, 14 casos | 1 crítico documentado | [Ver projeto](https://github.com/ingridmatosn/QA-Sprint2-Design-de-Testes) |
| 3 | Web cross-browser e layout | 104 verificações | 32 | [Ver projeto](https://github.com/ingridmatosn/Qa-Sprint3-Testes-Web) |
| 4 | API REST (Postman) | 70 casos de teste | 44 | [Ver projeto](https://github.com/ingridmatosn/QA-Sprint4-Testes-API) |
| 5 | Mobile end-to-end (Urban Lunch) | 36 verificações | 6 | [Ver projeto](https://github.com/ingridmatosn/QA-Sprint5-Testes-Mobile) |
| 6 | Terminal e banco de dados | 6 tarefas práticas | — | [Ver projeto](https://github.com/ingridmatosn/QA-Sprint6-Terminal-Database) |
| 7 e 8 | Automação E2E (Python, Selenium, Pytest, POM) | 8 testes automatizados | — | [Ver projeto](https://github.com/ingridmatosn/QA-Brazil_Python_Automation) |

**Totais:** 261 verificações registradas e **87 defeitos com identificador rastreável** no Jira (BR-001 a BR-005 e KAN-1 a KAN-83).

## Projetos em destaque

### Automação de testes E2E — 8 testes, projeto aprovado
[QA-Brazil_Python_Automation](https://github.com/ingridmatosn/QA-Brazil_Python_Automation)

Automação do fluxo completo de pedido de táxi do app web Urban Routes com Python, Selenium WebDriver e Pytest, no padrão **Page Object Model**. Os testes cobrem rota, tarifa, cadastro de telefone com código SMS, cartão, comentário para o motorista, itens extras e o modal de busca de carro, usando esperas explícitas no lugar de pausas fixas.

### Testes de API REST — 70 casos, 44 defeitos
[QA-Sprint4-Testes-API](https://github.com/ingridmatosn/QA-Sprint4-Testes-API)

Testes de dois endpoints REST no Postman. O achado principal não foi um defeito isolado, e sim um padrão: a API respondia **500 Internal Server Error** em cenários que exigiam **400 Bad Request** — erro do cliente devolvido como falha do servidor. Isso impede o cliente de se corrigir, polui o monitoramento e desvia a investigação de produção. Recomendação registrada: bloquear a release até a correção do tratamento de erros.

### Design de testes com BVA e partição de equivalência — 44 classes
[QA-Sprint2-Design-de-Testes](https://github.com/ingridmatosn/QA-Sprint2-Design-de-Testes)

Casos desenhados antes da execução, com partição de equivalência e análise de valor limite em um formulário de cadastro. A classe "29 de fevereiro em ano não bissexto" expôs o defeito mais grave: o sistema aceitou **29/02/2005**, data que não existe. A validação de fevereiro existia, mas ignorava a regra de ano bissexto.

### Testes web cross-browser — 104 verificações, 32 defeitos
[Qa-Sprint3-Testes-Web](https://github.com/ingridmatosn/Qa-Sprint3-Testes-Web)

Layout comparado ao design e validações do formulário de pagamento, em Chrome 800x600 e Firefox 1920x1080. Ao fim do sprint, **não recomendei o lançamento do produto**, pela quantidade e gravidade dos defeitos, incluindo uma falha crítica que impedia o cancelamento de corridas.

## Competências demonstradas

**Técnicas de teste:** partição de equivalência, análise de valor limite, teste funcional, teste de regressão, teste exploratório de layout, teste end-to-end.

**Automação:** Python, Selenium WebDriver, Pytest e Page Object Model (POM).

**Tipos de aplicação:** web, mobile e APIs REST.

**Documentação:** casos de teste com pré-condição, etapas e resultado esperado; checklists por seção; relatórios de defeito com passos de reprodução, resultado esperado, resultado real e prioridade.

**Ferramentas:** Jira, Postman, DevTools, emulador Android, Cygwin/Bash, PostgreSQL, Python, Selenium WebDriver, Pytest, PyCharm, Git e GitHub.

## Como este portfólio está organizado

Cada repositório de sprint tem:

- um **README** com objetivo, escopo, técnicas aplicadas, resultados, defeitos, ferramentas, aprendizados e melhorias pendentes;
- os **artefatos em Markdown**, que abrem direto no GitHub, sem download;
- a **planilha ou documento original** da entrega.

## Sobre mim

Analista de QA em formação pela TripleTen, com mais de 8 anos de experiência anterior em atendimento e suporte operacional de alta demanda — o que me acostumou a ouvir o problema do ponto de vista de quem usa o produto e a registrar cada passo do que aconteceu.

Busco a primeira oportunidade como QA Júnior, Manual QA Tester ou QA Intern, em modelo remoto ou híbrido.

---

**Ingrid Matos** — Analista de QA Júnior
Feira de Santana, Bahia, Brasil
[LinkedIn](https://www.linkedin.com/in/ingridmatosn/) · [GitHub](https://github.com/ingridmatosn) · ingridmatosyt01@gmail.com
