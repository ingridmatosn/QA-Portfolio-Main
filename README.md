# QA Portfolio - TripleTen Bootcamp: Sprints 1-6

Portfólio completo de testes de qualidade (QA) desenvolvido durante o bootcamp **Analista de QA** da TripleTen.

**Período**: Sprints 1-6 | **Status**: ✅ Bootcamp Concluído  
**Tecnologias**: Jira, Postman, Cygwin, PostgreSQL, UI Testing, API Testing, Mobile Testing

---

## 📊 Resumo Geral - Todos os Sprints

| Sprint | Foco | Casos | Bugs | Taxa | Link |
|--------|------|-------|------|------|------|
| **1** | Testes Funcionais (Urban Routes) | 37 | 5 | 86.5% | [📌 Sprint 1](#sprint-1-testes-funcionais) |
| **2** | Design de Testes (BVA + EP) | 45 | 14 | 69% | [📌 Sprint 2](#sprint-2-design-de-testes) |
| **3** | Testes Web Cross-Browser | 79 | 32 | 73% | [📌 Sprint 3](#sprint-3-testes-web) |
| **4** | Testes API REST | 70 | 44 | 37% | [📌 Sprint 4](#sprint-4-testes-api) |
| **5** | Testes Mobile (Urban Lunch) | 36 | 6 | 83% | [📌 Sprint 5](#sprint-5-testes-mobile) |
| **6** | Terminal (Cygwin) + SQL | 6 | — | ✅ | [📌 Sprint 6](#sprint-6-terminal--banco-de-dados) |
| **TOTAL** | | **273** | **101** | **71%** | |

---

## 🎯 Principais Aprendizados

### ✅ Habilidades QA Desenvolvidas

**Testes Funcionais**:
- Teste de fluxos end-to-end
- Identificação de bugs em UI
- Análise de casos críticos

**Design de Testes**:
- Boundary Value Analysis (BVA)
- Equivalence Partitioning (EP)
- Teste de datas inválidas (ano bissexto)

**Testes Web**:
- Cross-browser testing (Chrome, Firefox)
- Diferentes resoluções (800x600, 1920x1080)
- Testes de layout e responsividade

**Testes API**:
- POST requests com validação
- Tratamento de erros HTTP
- Edge cases em parâmetros

**Testes Mobile**:
- Funcionalidades de app móvel
- Fluxo completo do usuário
- Performance em diferentes dispositivos

**Skills Técnicos**:
- Jira (rastreamento de bugs)
- Postman (testes de API)
- Terminal/Bash (análise de logs)
- PostgreSQL (SQL queries)
- UI Testing (validação visual)

---

## 📁 Repositórios por Sprint

### Sprint 1: Testes Funcionais

**🔗 [qa-sprint-1-testes-funcionais](https://github.com/ingridmatosn/qa-sprint-1-testes-funcionais)**

**Objetivo**: Testes funcionais de aplicação web (Urban Routes)

**Métricas**:
- **37 casos de teste** executados
- **5 bugs** encontrados (BR-001 a BR-005)
- **Taxa de sucesso**: 86.5%

**Bugs Encontrados**:
- BR-001: Erro em rolagem de mapa
- BR-002: Problema com zoom
- BR-003: Erro em street view
- BR-004: Campos De/Para incorretos
- BR-005: Erro em ícones/pop-ups

**Tecnologias**: Manual Testing, UI Testing, Jira

---

### Sprint 2: Design de Testes

**🔗 [qa-sprint-2-design-testes](https://github.com/ingridmatosn/qa-sprint-2-design-testes)**

**Objetivo**: Aplicar técnicas de design de testes (BVA + Equivalence Partitioning)

**Métricas**:
- **45 classes de equivalência** analisadas
- **14 casos de teste** executados
- **14 bugs** encontrados
- **Taxa de sucesso**: 69%

**Bugs Críticos**:
- Data 29/02/2005 aceita (ano não-bissexto) ⚠️ CRÍTICO
- Campos de nome/sobrenome permitem caracteres inválidos
- Validação de data incompleta

**Técnicas Aplicadas**:
- Boundary Value Analysis
- Equivalence Partitioning
- Testes de entrada inválida

---

### Sprint 3: Testes Web Cross-Browser

**🔗 [qa-sprint-3-testes-web](https://github.com/ingridmatosn/qa-sprint-3-testes-web)**

**Objetivo**: Testes em múltiplos navegadores e resoluções

**Métricas**:
- **79 casos de teste** executados
- **32 bugs** encontrados (KAN-21 a KAN-53)
- **Taxa de sucesso**: 73%

**Distribuição de Bugs**:
- Layout checklist: 13 bugs (KAN-21 a KAN-33)
- Método de pagamento: 16 bugs (KAN-1 a KAN-17)
- Botão de teste: 3 bugs (KAN-18 a KAN-20)
- Locação: 1 bug (KAN-21)

**Navegadores Testados**:
- Chrome 800x600
- Firefox 1920x1080

---

### Sprint 4: Testes API REST

**🔗 [qa-sprint-4-testes-api](https://github.com/ingridmatosn/qa-sprint-4-testes-api)**

**Objetivo**: Testes completos de endpoints REST

**Métricas**:
- **70 casos de teste** executados
- **44 bugs** encontrados (KAN-34 a KAN-77)
- **Taxa de sucesso**: 37%

**Endpoints Testados**:
1. POST /api/v1/kits/{id}/products (28 casos → 20 bugs)
2. POST /order-and-go/v1/delivery (42 casos → 24 bugs)

**Padrão de Bugs**:
- ❌ Retorna 500 quando deveria retornar 400
- ❌ Falta validação de entrada
- ❌ Tratamento de erro inconsistente

**Recomendação**: BLOQUEAR release até correção

---

### Sprint 5: Testes Mobile

**🔗 [qa-sprint-5-testes-mobile](https://github.com/ingridmatosn/qa-sprint-5-testes-mobile)**

**Objetivo**: Testes end-to-end de aplicativo móvel

**Métricas**:
- **36 casos de teste** executados
- **6 bugs** encontrados (KAN-78 a KAN-83)
- **Taxa de sucesso**: 83%

**Bugs Encontrados**:
- KAN-78: Ordem de pontos no mapa incorreta
- KAN-79: Informação de prato incompleta
- KAN-80: Cálculo de total incorreto ⚠️ CRÍTICO
- KAN-81: Localização não atualiza em tempo real ⚠️ CRÍTICO
- KAN-82: Avaliação não salva
- KAN-83: Mensagem de erro não clara

**Seções Testadas**:
1. Seleção do local de coleta
2. Escolha de pratos
3. Confirmação do pedido
4. Acompanhamento da entrega
5. Pedido entregue
6. Notificações de erro

---

### Sprint 6: Terminal + Banco de Dados

**🔗 [qa-sprint-6-terminal-database](https://github.com/ingridmatosn/qa-sprint-6-terminal-database)**

**Objetivo**: Aprender terminal e SQL com dados reais

**Tarefas Completadas**: 6 práticas

**Seção 1: Console (Cygwin)**
- Tarefa 1: Busca em logs Apache com grep
- Tarefa 2: Manipulação de arquivos e filtering
  - 172 erros HTTP 400 encontrados
  - 156 erros HTTP 500 encontrados

**Seção 2: Banco de Dados (PostgreSQL)**
- Tarefa 1: COUNT - 5.529 táxis total
- Tarefa 2: GROUP BY + HAVING - 51 empresas pequenas
- Tarefa 3: CASE WHEN - Transformação de dados (clima)
- Tarefa 4: INNER JOIN - Viagens por empresa (64 empresas)

**Dataset**: Chicago Taxi Trips Database

---

## 📈 Estatísticas Gerais

### Total de Testes
Casos Testados: 273
Bugs Encontrados: 101
Taxa de Sucesso: 71%

### Distribuição de Bugs

| Sprint | Bugs | Severidade |
|--------|------|-----------|
| Sprint 1 | 5 | Baixo-Médio |
| Sprint 2 | 14 | Médio-Alto |
| Sprint 3 | 32 | Médio-Alto |
| Sprint 4 | 44 | **Alto-Crítico** |
| Sprint 5 | 6 | Baixo-Médio |
| **TOTAL** | **101** | |

### Taxa de Sucesso por Sprint
Sprint 1: ████████░ 86.5%
Sprint 2: ██████░░░ 69%
Sprint 3: ███████░░ 73%
Sprint 4: ███░░░░░░ 37% ⚠️
Sprint 5: ████████░ 83%
Sprint 6: ██████████ 100% ✅

---

## 🎓 Conceitos Dominados

### QA Testing
- ✅ Manual Testing
- ✅ Functional Testing
- ✅ UI Testing
- ✅ API Testing
- ✅ Mobile Testing
- ✅ Cross-browser Testing
- ✅ End-to-End Testing

### Test Design
- ✅ Boundary Value Analysis (BVA)
- ✅ Equivalence Partitioning
- ✅ Edge Case Identification
- ✅ Test Case Documentation

### Tools & Technologies
- ✅ Jira (bug tracking)
- ✅ Postman (API testing)
- ✅ Cygwin/Terminal (bash)
- ✅ PostgreSQL (SQL)
- ✅ Manual UI Testing

### Soft Skills
- ✅ Análise de requisitos
- ✅ Documentação profissional
- ✅ Rastreamento de bugs
- ✅ Comunicação de resultados

---

## 🚀 Readiness para Produção

| Aspecto | Status |
|---------|--------|
| Testes Funcionais | ✅ Pronto |
| Web Testing | ✅ Pronto |
| Mobile Testing | ✅ Pronto |
| API Testing | ⚠️ Com issues |
| SQL / Database | ✅ Pronto |
| Terminal Skills | ✅ Pronto |

---

## 💼 O Que Este Portfólio Demonstra

### Para Recrutadores

1. **Experiência Prática**: 6 sprints com dados reais
2. **Profundidade**: De testes básicos até API testing
3. **Qualidade**: Documentação profissional em cada repo
4. **Progressão**: Aprendizado crescente ao longo dos sprints
5. **Números Reais**: 273 casos, 101 bugs encontrados
6. **Variedade**: Diferentes tipos de testes e tecnologias

### Casos de Uso Destacáveis

- **Sprint 2**: Bug crítico de ano bissexto (29/02/2005)
- **Sprint 3**: 32 bugs em teste cross-browser
- **Sprint 4**: Análise profunda de validação de API
- **Sprint 5**: Teste completo de fluxo móvel
- **Sprint 6**: Análise de dados real com SQL

---

## 🔗 Todos os Repositórios

| # | Sprint | Repositório | Link |
|---|--------|-------------|------|
| 1 | Testes Funcionais | qa-sprint-1-testes-funcionais | [github.com/ingridmatosn/qa-sprint-1-testes-funcionais](https://github.com/ingridmatosn/qa-sprint-1-testes-funcionais) |
| 2 | Design de Testes | qa-sprint-2-design-testes | [github.com/ingridmatosn/qa-sprint-2-design-testes](https://github.com/ingridmatosn/qa-sprint-2-design-testes) |
| 3 | Testes Web | qa-sprint-3-testes-web | [github.com/ingridmatosn/qa-sprint-3-testes-web](https://github.com/ingridmatosn/qa-sprint-3-testes-web) |
| 4 | Testes API | qa-sprint-4-testes-api | [github.com/ingridmatosn/qa-sprint-4-testes-api](https://github.com/ingridmatosn/qa-sprint-4-testes-api) |
| 5 | Testes Mobile | qa-sprint-5-testes-mobile | [github.com/ingridmatosn/qa-sprint-5-testes-mobile](https://github.com/ingridmatosn/qa-sprint-5-testes-mobile) |
| 6 | Terminal + SQL | qa-sprint-6-terminal-database | [github.com/ingridmatosn/qa-sprint-6-terminal-database](https://github.com/ingridmatosn/qa-sprint-6-terminal-database) |

---

## 👤 Sobre

**Ingrid Matos** - Analista de QA Junior

- 📧 Email: ingridmatosyt01@gmail.com
- 📱 Telefone: (75) 98293-2378
- 🔗 LinkedIn: [linkedin.com/in/ingridmatosn](https://linkedin.com/in/ingridmatosn)
- 💻 GitHub: [github.com/ingridmatosn](https://github.com/ingridmatosn)

---

## 📝 Certificações & Bootcamp

**Bootcamp**: Analista de QA - TripleTen  
**Marcos Completados**:
- ✅ "Localizador de Bugs" (100% completo)
- ✅ Habilidades: Rastreamento de bugs, Jira, UI Testing
- ✅ Sprints 1-6: Testes Funcionais, Design, Web, API, Mobile, Terminal+SQL

---

## 📚 Próximos Passos

- [ ] Completar certificação do bootcamp
- [ ] Aplicar para vagas de QA Junior
- [ ] Aprender testes automatizados (Selenium, Cypress)
- [ ] Dominar SQL mais avançado
- [ ] Testes de performance e carga

---

## ⭐ Destaques do Portfólio

### 🏆 Maior Desafio
**Sprint 4** - Testes de API com 44 bugs encontrados  
Demonstra capacidade de análise profunda e identificação de padrões de erro.

### 🎯 Melhor Taxa de Sucesso
**Sprint 1** - 86.5% de casos aprovados  
Demonstra capacidade de executar testes funcionais com alta qualidade.

### 📊 Maior Volume
**Sprint 3** - 79 casos em cross-browser  
Demonstra resistência e capacidade de executar grande volume de testes.

### 💡 Mais Educativo
**Sprint 6** - Terminal + SQL  
Demonstra aprendizado em tecnologias além de testing (backend skills).

---

**Status**: ✅ Portfólio Completo | **Última Atualização**: Setembro 2026
