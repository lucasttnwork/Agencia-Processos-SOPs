# 📘 MANUAL OPERACIONAL DA AGÊNCIA

**Versão**: 1.0
**Data de Criação**: 12/12/2025
**Responsável**: Diretor de Operações
**Status**: ✅ **Completo** (17 processos + arquitetura técnica)

---

## 🎯 SOBRE ESTE MANUAL

Este é o **Manual Operacional Completo** de uma agência de marketing digital especializada em **Meta Ads** (Facebook e Instagram).

**Objetivo**: Documentar de forma estruturada e implementável **todos os processos, sistemas, ferramentas e melhores práticas** necessários para operar a agência com excelência, escalabilidade e consistência.

**Diferenciais**:
- ✅ **17 processos detalhados** cobrindo toda operação (estratégia, vendas, execução, suporte)
- ✅ **Sistema operacional centralizado** (Notion como FL - Foundations Layer)
- ✅ **76+ automações Python** (substituindo Make/Zapier)
- ✅ **165 templates prontos** (propostas, relatórios, checklists, planilhas)
- ✅ **Implementável imediatamente** (não é teoria, é operação real)
- ✅ **Cultura de melhoria contínua** (auditorias, post-mortems, OKRs)

---

## 📂 ESTRUTURA DO MANUAL

```
manual_operacional/
│
├── README.md                              # 👈 Você está aqui (índice geral)
│
├── 01_FL_NOTION_ARQUITETURA.md            # Arquitetura de 18 databases Notion
├── 02_MAPA_PROCESSOS.md                   # Visão geral dos 17 processos
├── 03_AUTOMACOES_PYTHON.md                # 76+ automações (stack, código, guia)
├── 04_TEMPLATES_SCRIPTS.md                # Índice de 165 templates
├── 05_GLOSSARIO.md                        # 150+ termos técnicos
│
└── processos/
    ├── P1_ESTRATEGIA_POSICIONAMENTO.md    # Visão, Missão, ICP, OKRs, Roadmap
    ├── P2_AQUISICAO_CLIENTES.md           # Prospecção e geração de leads
    ├── P3_VENDAS_FECHAMENTO.md            # Processo comercial e contratos
    ├── P4_ONBOARDING_CLIENTES.md          # Kick-off e integração de novos clientes
    ├── P5_PESQUISA_PLANEJAMENTO.md        # Estratégia de campanha e briefing
    ├── P6_PRODUCAO_MATERIAIS.md           # Criação de criativos e copy
    ├── P7_SETUP_TECNICO.md                # Pixel, CAPI, UTMs, integrações
    ├── P8_IMPLEMENTACAO_LANCAMENTO.md     # Build de campanhas e QA
    ├── P9_GESTAO_OTIMIZACAO.md            # Rotinas diárias, otimizações
    ├── P10_RELATORIOS_COMUNICACAO.md      # Relatórios e reuniões com clientes
    ├── P11_RETENCAO_RENOVACAO.md          # Upsell, NPS, anti-churn
    ├── P12_CRISES_EXCECOES.md             # Gestão de incidentes críticos
    ├── P13_FINANCEIRO.md                  # Faturas, cobrança, DRE, lucratividade
    ├── P14_PESSOAS_CAPACIDADE.md          # Onboarding, treinamento, avaliação
    ├── P15_GOVERNANCA_ACESSOS.md          # Organização, backups, segurança
    ├── P16_COMPLIANCE_JURIDICO.md         # LGPD, políticas de anúncios, contratos
    └── P17_QUALIDADE_MELHORIA.md          # Auditorias, post-mortems, melhoria contínua
```

---

## 🗺️ OS 17 PROCESSOS (VISÃO GERAL)

### 🎯 ESTRATÉGIA (1 processo)

| Código | Processo | Objetivo | Subprocessos |
|--------|----------|----------|--------------|
| **P1** | Estratégia & Posicionamento | Definir identidade, ICP, OKRs e roadmap da agência | 6 |

---

### 💼 CORE - OPERAÇÃO PRINCIPAL (10 processos)

**Aquisição → Vendas → Execução → Retenção**

| Código | Processo | Objetivo | Subprocessos |
|--------|----------|----------|--------------|
| **P2** | Aquisição de Clientes | Gerar leads qualificados (inbound + outbound) | 5 |
| **P3** | Vendas e Fechamento | Converter leads em clientes pagantes | 6 |
| **P4** | Onboarding de Clientes | Integrar novos clientes e preparar para lançamento | 5 |
| **P5** | Pesquisa & Planejamento | Criar estratégia de campanha vencedora | 6 |
| **P6** | Produção de Materiais | Produzir criativos de alta conversão | 5 |
| **P7** | Setup Técnico | Configurar Pixel, CAPI, UTMs, integrações | 8 |
| **P8** | Implementação e Lançamento | Construir campanhas e lançar com QA rigoroso | 6 |
| **P9** | Gestão e Otimização | Monitorar, otimizar e escalar campanhas | 8 |
| **P10** | Relatórios e Comunicação | Comunicar resultados e manter cliente engajado | 7 |
| **P11** | Retenção e Renovação | Evitar churn, renovar contratos, fazer upsell | 6 |

---

### 🛡️ SUPORTE - PROCESSOS DE SUSTENTAÇÃO (6 processos)

**Gestão de Crises, Finanças, Pessoas, Governança, Compliance, Qualidade**

| Código | Processo | Objetivo | Subprocessos |
|--------|----------|----------|--------------|
| **P12** | Crises e Exceções | Responder rapidamente a incidentes críticos | 8 |
| **P13** | Financeiro e Administrativo | Garantir saúde financeira e lucratividade | 7 |
| **P14** | Pessoas e Capacidade | Construir time de alta performance | 7 |
| **P15** | Governança e Acessos | Organizar conhecimento e garantir segurança | 5 |
| **P16** | Compliance e Jurídico | Operar em conformidade (LGPD, políticas Meta) | 5 |
| **P17** | Qualidade e Melhoria Contínua | Evoluir constantemente processos e resultados | 6 |

---

**Total**: 17 processos | 106 subprocessos | 500+ tarefas detalhadas

---

## 🧭 COMO NAVEGAR ESTE MANUAL

### Para Novos Colaboradores (Onboarding)

**Semana 1 - Fundamentos**:
1. Ler [README.md](README.md) (este arquivo)
2. Estudar [01_FL_NOTION_ARQUITETURA.md](01_FL_NOTION_ARQUITETURA.md) (nosso sistema operacional)
3. Estudar [02_MAPA_PROCESSOS.md](02_MAPA_PROCESSOS.md) (visão geral de processos)
4. Estudar [05_GLOSSARIO.md](05_GLOSSARIO.md) (termos essenciais)

**Semana 2 - Processos da Sua Área**:
- **Tráfego**: P5, P6, P7, P8, P9 (pesquisa → execução → otimização)
- **Atendimento**: P4, P10, P11 (onboarding → comunicação → retenção)
- **Comercial**: P2, P3 (aquisição → vendas)
- **Liderança**: P1, P13, P14, P17 (estratégia → finanças → pessoas → qualidade)

**Semana 3 - Templates e Automações**:
5. Explorar [04_TEMPLATES_SCRIPTS.md](04_TEMPLATES_SCRIPTS.md) (templates da sua área)
6. Conhecer [03_AUTOMACOES_PYTHON.md](03_AUTOMACOES_PYTHON.md) (automações que facilitam seu trabalho)

---

### Para Executar uma Tarefa Específica

**Exemplo: "Preciso lançar uma campanha nova"**

1. Acesse [processos/P8_IMPLEMENTACAO_LANCAMENTO.md](processos/P8_IMPLEMENTACAO_LANCAMENTO.md)
2. Siga os subprocessos P8.1 → P8.6
3. Use [Checklist de QA (42 pontos)](04_TEMPLATES_SCRIPTS.md#t070) antes do lançamento
4. Configure automação A02 (Alerta de Campanha Pendente) se aplicável

**Exemplo: "Cliente está insatisfeito, risco de churn"**

1. Acesse [processos/P11_RETENCAO_RENOVACAO.md](processos/P11_RETENCAO_RENOVACAO.md) → P11.3 (Detecção de Risco de Churn)
2. Siga [Template de Plano Anti-Churn](04_TEMPLATES_SCRIPTS.md#t104)
3. Se escalar para crise: acesse [processos/P12_CRISES_EXCECOES.md](processos/P12_CRISES_EXCECOES.md)

---

### Para Líderes e Gestores

**Revisões Estratégicas**:
- **Semanal**: P17.6 (Dashboard de Qualidade) + P9.3 (Rotina Semanal)
- **Mensal**: P13.7 (Fechamento Financeiro) + P14.5 (1:1s com time)
- **Trimestral**: P17.5 (Revisão Estratégica) + P1.5 (OKRs)
- **Anual**: P1.5 (Planejamento Estratégico) + P1.6 (Roadmap de Inovação)

**Auditorias e Qualidade**:
- P17.1 (Auditorias Internas - mensal/trimestral)
- P17.2 (Post-Mortems de campanhas/incidentes)
- P17.4 (Ciclos de Melhoria Contínua - PDCA)

---

## 🛠️ FERRAMENTAS E TECNOLOGIAS

### Sistema Operacional (FL - Foundations Layer)

**Notion** - 18 Databases integrados:
- Clientes, Campanhas, Criativos, Tarefas, Reuniões, Relatórios
- Incidentes, Financeiro, Contratos, Time, Treinamentos
- Base de Conhecimento, Auditorias, Post-Mortems, Projetos de Melhoria
- OKRs, Compliance, Fornecedores

Ver detalhes em [01_FL_NOTION_ARQUITETURA.md](01_FL_NOTION_ARQUITETURA.md)

---

### Stack de Automações Python

**76+ automações** cobrindo:
- Monitoramento e alertas (CPA, performance, incidentes)
- Geração de relatórios (semanal, mensal, PDF)
- Sincronização de dados (Notion ↔ Meta Ads ↔ Google Sheets)
- Comunicação automatizada (WhatsApp, Email, Slack)
- Dashboards em tempo real (Google Data Studio)

**Tecnologias**:
- Python 3.11+ (notion-client, facebook-business, google-api)
- APScheduler / Celery (agendamento de tarefas)
- Redis (filas de mensagens)
- Google Data Studio (dashboards)

Ver detalhes em [03_AUTOMACOES_PYTHON.md](03_AUTOMACOES_PYTHON.md)

---

### Outras Ferramentas Essenciais

| Categoria | Ferramenta | Uso |
|-----------|-----------|-----|
| **Meta Ads** | Meta Business Suite, Ads Manager | Criação e gestão de campanhas |
| **Comunicação** | Slack, WhatsApp Business, Email | Comunicação interna e com clientes |
| **Armazenamento** | Google Drive | Arquivos, templates, criativos (estrutura de 7 pastas) |
| **Relatórios** | Google Slides, Data Studio | Relatórios visuais automatizados |
| **Financeiro** | Google Sheets, Notion | Fluxo de caixa, DRE, controle de pagamentos |
| **Design** | Figma, Canva, Adobe Creative Cloud | Produção de criativos |
| **Analytics** | Google Analytics, Meta Pixel | Tracking e análise de dados |

---

## 📊 MÉTRICAS DE SUCESSO (KPIs DA AGÊNCIA)

### Comercial e Crescimento
- **MRR (Monthly Recurring Revenue)**: Meta >R$300k
- **Número de Clientes Ativos**: Meta >50
- **Taxa de Fechamento (Vendas)**: Meta >30%
- **Ticket Médio**: Meta >R$8k/mês

### Operação e Qualidade
- **ROI Médio de Clientes**: Meta >300%
- **% Clientes Atingindo Meta de CPA**: Meta >75%
- **Score de Auditorias (P17.1)**: Meta >85%
- **NPS de Clientes**: Meta >60

### Financeiro
- **Margem de Lucro Líquido**: Meta >30%
- **Lucratividade por Cliente**: Meta >25%
- **Taxa de Inadimplência**: Meta <5%

### Pessoas
- **eNPS (Satisfação Interna)**: Meta >40
- **Turnover Voluntário**: Meta <10%/ano
- **Horas de Treinamento/Colaborador**: Meta >20h/ano

### Retenção
- **Churn Rate**: Meta <8%/ano
- **Taxa de Renovação**: Meta >90%
- **LTV (Lifetime Value)**: Meta >R$80k

---

## 🚀 ROADMAP DE IMPLEMENTAÇÃO

**Se você está implementando este manual do zero**, sugerimos:

### Fase 1 (Mês 1-2): Fundação
- ✅ Configurar Notion (18 databases - ver P01_FL)
- ✅ Implementar processos core críticos: P3 (Vendas), P4 (Onboarding), P8 (Implementação)
- ✅ Criar templates essenciais (proposta comercial, briefing, relatório)
- ✅ Setup de automações críticas (A08, A20, A38)

### Fase 2 (Mês 3-4): Expansão
- ✅ Implementar processos restantes (P1-P17)
- ✅ Expandir automações (30-50 automações)
- ✅ Treinar time nos processos
- ✅ Primeira auditoria de qualidade (P17.1)

### Fase 3 (Mês 5-6): Refinamento
- ✅ Implementar todas as 76+ automações
- ✅ Cultura de melhoria contínua (P17 completo)
- ✅ Dashboards em tempo real
- ✅ OKRs definidos e tracking ativo

---

## 🔄 MANUTENÇÃO E ATUALIZAÇÃO

**Este manual é um documento vivo**. Processos evoluem, ferramentas mudam, mercado se transforma.

### Responsabilidades

| Responsável | Ação | Frequência |
|-------------|------|------------|
| **Diretor de Operações** | Revisar e atualizar manual completo | Trimestral (P17.5) |
| **Líderes de Área** | Atualizar processos de sua área quando mudanças ocorrem | Contínua |
| **Todo o Time** | Sugerir melhorias, identificar gaps, documentar aprendizados | Contínua |

### Como Sugerir Mudanças

1. Identificar gap ou melhoria em processo
2. Documentar sugestão (Notion - Database "Projetos de Melhoria")
3. Discutir em reunião semanal/mensal
4. Se aprovado: Atualizar processo documentado
5. Comunicar mudança ao time (All-Hands ou Slack)
6. Treinar time na nova forma de trabalho

### Versionamento

- **v1.0** (12/12/2025): Versão inicial completa (17 processos + arquitetura técnica)
- **v1.1** (futura): [Descrever mudanças significativas]

---

## 📚 RECURSOS ADICIONAIS

### Documentos Essenciais
- **[Prompt.md](../Prompt.md)**: Contexto original que guiou criação do manual
- **[Plan File](.cursor/plans/manual_operacional_da_agência_ada3dde8.plan.md)**: Planejamento e checklist de implementação

### Links Úteis
- **Meta for Business**: https://www.facebook.com/business
- **Meta Blueprint** (Certificações): https://www.facebook.com/business/learn
- **Notion API**: https://developers.notion.com
- **Google Ads API**: https://developers.google.com/google-ads/api
- **LGPD (Lei Completa)**: http://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm

---

## 💡 FILOSOFIA DO MANUAL

### Princípios que Guiam Este Manual

1. **Operação > Teoria**: Tudo aqui é implementável, não apenas conceitual
2. **Processos Vivos**: Documentar → Executar → Medir → Melhorar (ciclo contínuo)
3. **Transparência Radical**: Compartilhar tudo, inclusive falhas e aprendizados
4. **Excelência Operacional**: Processos documentados, execução impecável, zero improviso
5. **Melhoria Contínua**: Pequenas melhorias constantes > grandes mudanças esporádicas
6. **Foco no Cliente**: Toda operação existe para gerar resultado real para clientes
7. **Time de Alta Performance**: Processos liberam o time para focar em estratégia e criatividade

---

## ❓ FAQ (Perguntas Frequentes)

**P: Por que 17 processos? Não é demais?**
R: Cada processo cobre uma área crítica da agência. Ter menos seria omitir partes importantes (ex: compliance, crises, qualidade). Processos bem documentados reduzem caos, não aumentam burocracia.

**P: Preciso implementar tudo de uma vez?**
R: Não. Siga o roadmap de implementação (Fase 1 → 2 → 3). Comece com processos core críticos (P3, P4, P8, P9, P10).

**P: E se minha agência é menor/maior?**
R: Processos são escaláveis. Agência menor pode simplificar (ex: 1 pessoa faz múltiplos papéis). Agência maior pode especializar (1 pessoa por papel, ou times por processo).

**P: Automações Python são obrigatórias?**
R: Não. Você pode começar manual e automatizar gradualmente. Ou usar Make/Zapier temporariamente. Mas automações próprias oferecem controle total e escalabilidade.

**P: Como garantir que time siga os processos?**
R: Treinamento (P14.2), auditorias (P17.1), feedback contínuo (P14.5), cultura de qualidade (P17), liderança modelando comportamento.

**P: Quanto tempo leva para implementar tudo?**
R: 3-6 meses para implementação completa (ver Roadmap). Mas você verá resultados nas primeiras semanas ao implementar processos core.

---

## 🎓 PARA ESTUDANTES / CONSULTORES

Se você está estudando este manual para aprender sobre operações de agências de marketing digital:

**Pontos-Chave**:
1. Estrutura P1-P17 cobre ciclo completo: Estratégia → Core (Vendas → Execução → Retenção) → Suporte
2. Notion como FL (sistema operacional) é diferencial competitivo
3. Automações Python substituem no-code (Make/Zapier), dando controle total
4. Cultura de qualidade (P17) é o que diferencia agências excelentes de medianas
5. Métricas certas (ROI, NPS, Churn) guiam decisões melhores que achismos

**Adaptações**:
- Para agência Google Ads: Trocar "Meta Ads" por "Google Ads", ajustar P7 (setup técnico)
- Para agência full-service: Adicionar processos para SEO, Social Media, etc.
- Para consultoria: Adaptar P3-P11 para modelo de consultoria vs. execução

---

## 🏆 SOBRE A CONSTRUÇÃO DESTE MANUAL

Este manual foi construído seguindo metodologia rigorosa:

**Processo de Criação**:
1. Análise profunda de melhores práticas de agências de performance
2. Mapeamento completo de jornada do cliente (Lead → Ativo → Renovação)
3. Definição de 17 macroprocessos com 106 subprocessos
4. Detalhamento de 500+ tarefas executáveis
5. Criação de 165 templates prontos para uso
6. Arquitetura de 76+ automações Python
7. Documentação de 150+ termos técnicos

**Princípios de Documentação**:
- Cada processo tem: Objetivo, Gatilhos, Entregas, Tarefas detalhadas, Checklists, Métricas, Automações, Templates, Fluxos de Exceção
- Linguagem clara e direta (não academicismo)
- Exemplos concretos em cada seção
- Integrações entre processos mapeadas
- Foco em implementação, não teoria

---

## 📞 SUPORTE E CONTATO

**Responsável Geral**: Diretor de Operações

**Para Dúvidas sobre Processos**:
- Consultar [05_GLOSSARIO.md](05_GLOSSARIO.md)
- Postar em Slack #duvidas-processos
- Agendar 1:1 com líder da área

**Para Sugerir Melhorias**:
- Postar em Notion → Database "Projetos de Melhoria"
- Discussão em reunião semanal de liderança
- Apresentar em Sessão "Lessons Learned" (quinzenal)

---

## ✅ CHECKLIST DE USO DO MANUAL

**Novos Colaboradores** (Onboarding - P14.1):
```
☐ Ler README.md (este arquivo)
☐ Estudar 01_FL_NOTION_ARQUITETURA.md
☐ Estudar 02_MAPA_PROCESSOS.md
☐ Estudar 05_GLOSSARIO.md (termos essenciais)
☐ Ler processos da minha área (P5-P10 para tráfego, por exemplo)
☐ Explorar templates que vou usar (04_TEMPLATES_SCRIPTS.md)
☐ Conhecer automações que facilitam meu trabalho (03_AUTOMACOES_PYTHON.md)
☐ Fazer shadowing com colega sênior executando processos
```

**Líderes** (Revisão Trimestral - P17.5):
```
☐ Revisar processos da minha área (ainda fazem sentido?)
☐ Atualizar templates que mudaram
☐ Adicionar novos aprendizados à base de conhecimento
☐ Identificar gaps ou processos obsoletos
☐ Propor melhorias (Projetos de Melhoria)
☐ Garantir que time está seguindo processos (auditoria)
☐ Atualizar versionamento do manual se mudanças significativas
```

---

## 🎉 CONCLUSÃO

Este manual representa **a operação completa e escalável de uma agência de Meta Ads de alta performance**.

**O que você tem aqui**:
- ✅ 17 processos detalhados (estratégia → core → suporte)
- ✅ 106 subprocessos com 500+ tarefas executáveis
- ✅ 76+ automações Python (código pronto)
- ✅ 165 templates (docs, planilhas, checklists, dashboards)
- ✅ 150+ termos técnicos (glossário completo)
- ✅ Sistema operacional (Notion com 18 databases)
- ✅ Cultura de excelência e melhoria contínua

**Próximos Passos**:
1. Se está começando: Siga [Roadmap de Implementação](#-roadmap-de-implementação)
2. Se já opera: Faça auditoria (P17.1) para identificar gaps
3. Se é líder: Defina OKRs (P1.5) e priorize melhorias (P17.4)

**Lembre-se**: Manual excelente não executado = papel. Execução medíocre sem processo = caos. **Excelência = Processos Documentados + Execução Impecável + Melhoria Contínua**.

---

**Vamos construir uma agência excepcional! 🚀**

---

**Manual Operacional - v1.0**
Criado com rigor, implementado com disciplina, evoluído com humildade.

**Data**: 12/12/2025
**Status**: Completo e pronto para implementação

