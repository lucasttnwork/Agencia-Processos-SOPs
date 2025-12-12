## P10 — Relatórios, Reuniões e Comunicação (CS)

> **Objetivo do macroprocesso (P10)**: manter o cliente informado, alinhado e satisfeito através de comunicação estruturada, relatórios claros e gestão proativa de expectativas.

---

### P10.1 — Comunicação contínua + SLA + triagem de urgências
- **Código/ID**: P10.1
- **Tipo**: **[R] Recorrente** (contínuo)
- **Objetivo**: garantir comunicação fluida sem virar caos, com SLAs claros e priorização.
- **Momento**: durante toda a operação.
- **Gatilho**: mensagem do cliente.
- **Saída esperada**:
  - Mensagem respondida dentro do SLA.
  - Urgências tratadas imediatamente.
  - Demandas viram tarefas (P10.2).
- **Papéis envolvidos**: CS (principal), Gestor de Tráfego (técnico), Founder (escalação).
- **Ferramentas**: WhatsApp, e-mail, Notion.

#### SLAs de resposta (padrão)

| Tipo de mensagem | SLA de primeira resposta | SLA de resolução |
|------------------|--------------------------|------------------|
| Urgência crítica (conta bloqueada, campanha parada) | 30 minutos | Até resolver |
| Dúvida operacional | 2 horas (horário comercial) | 24 horas |
| Solicitação de ajuste | 4 horas | 48-72 horas |
| Feedback/sugestão | 24 horas | Próxima reunião |

#### Classificação de urgência

**Nível 1 - Crítico (responder em 30 min)**
- Conta bloqueada ou restrita.
- Campanha parou de entregar sem motivo.
- Problema de cobrança no Meta.
- Lead não está chegando (integração quebrada).

**Nível 2 - Alto (responder em 2h)**
- Anúncio reprovado.
- Performance caiu drasticamente.
- Cliente reporta problema com leads.
- Erro em criativo/LP publicado.

**Nível 3 - Normal (responder em 4h)**
- Pedido de novo criativo.
- Dúvida sobre métricas.
- Solicitação de ajuste em campanha.
- Agendamento de reunião.

**Nível 4 - Baixo (responder em 24h)**
- Feedback geral.
- Sugestão de melhoria.
- Pergunta não urgente.

#### Boas práticas de comunicação
- **Confirmar recebimento**: "Recebido! Vou verificar e retorno em [prazo]."
- **Ser proativo**: comunicar problemas antes do cliente perguntar.
- **Documentar**: toda decisão importante por escrito.
- **Evitar promessas vagas**: dar prazos realistas.

#### Horário de atendimento (padrão)
- Segunda a sexta: 9h às 18h.
- Urgências fora do horário: definir política (cobrar extra? não atender?).

---

### P10.2 — Transformar pedidos/mensagens em tarefas (fluxo de demandas)
- **Código/ID**: P10.2
- **Tipo**: **[P+A] Pipeline + automação**
- **Objetivo**: evitar que pedidos se percam e garantir rastreabilidade.
- **Momento**: sempre que cliente faz um pedido.
- **Gatilho**: mensagem com solicitação (não só dúvida).
- **Saída**: tarefa criada no Notion com prazo e responsável.
- **Papéis**: CS (triagem), Gestor de Tráfego (execução).
- **Ferramentas**: WhatsApp, Notion (`Tarefas`).

#### Passo a passo

**1. Identificar se é demanda**
- É pedido de ação? (Sim → criar tarefa)
- É só dúvida/informação? (Não → responder e registrar se relevante)

**2. Criar tarefa no Notion**
```markdown
Tarefa: [Descrição clara]
Cliente: [Nome]
Tipo: [Criativo/Tráfego/LP/CS]
Prioridade: [P0/P1/P2/P3]
Prazo: [Data]
Responsável: [Quem executa]
Contexto: [Link para mensagem ou resumo]
```

**3. Confirmar com cliente**
- "Anotei! Vamos entregar [descrição] até [data]. Precisa de mais alguma coisa?"

**4. Acompanhar execução**
- Atualizar status da tarefa.
- Comunicar cliente quando concluído.

#### Regras de priorização

| Prioridade | Critério | Prazo típico |
|------------|----------|--------------|
| P0 | Urgência crítica, impacta operação | Hoje |
| P1 | Importante, pedido explícito | 24-48h |
| P2 | Normal, pode esperar | 3-5 dias |
| P3 | Baixa, backlog | Próximo ciclo |

#### Automação Python (futuro)
- Bot que identifica padrões de pedido no WhatsApp.
- Cria tarefa automaticamente no Notion.
- Envia confirmação para cliente.

---

### P10.3 — Relatório semanal (resumo executivo + ações)
- **Código/ID**: P10.3
- **Tipo**: **[R] Recorrente** (semanal)
- **Objetivo**: manter cliente informado da performance sem sobrecarregar com dados.
- **Momento**: final da semana (sexta) ou início da próxima (segunda).
- **Gatilho**: calendário semanal.
- **Saída**: relatório enviado ao cliente.
- **Papéis**: Gestor de Tráfego (dados), CS (envio).
- **Ferramentas**: Ads Manager, Sheets/BI, Notion, WhatsApp/e-mail.

#### Estrutura do relatório semanal

```markdown
## Relatório Semanal — [Cliente]
**Período**: DD/MM a DD/MM/YYYY

### Resumo executivo (3 linhas)
- Esta semana geramos X leads com CPL médio de R$ Y.
- [Principal conquista ou problema].
- [Próximo passo principal].

### Métricas principais
| Métrica | Esta semana | Semana anterior | Meta |
|---------|-------------|-----------------|------|
| Investimento | R$ X | R$ Y | R$ Z |
| Leads | X | Y | Z |
| CPL | R$ X | R$ Y | R$ Z |
| CTR | X% | Y% | Z% |

### O que fizemos
- [Ação 1]
- [Ação 2]
- [Ação 3]

### O que aprendemos
- [Insight principal]

### Próximos passos
- [ ] [Ação planejada 1]
- [ ] [Ação planejada 2]

### Pendências do cliente (se houver)
- [ ] [O que precisamos do cliente]
```

#### Formato de envio
- **WhatsApp**: resumo em 5-7 linhas + link para relatório completo.
- **E-mail**: relatório completo (para registro).
- **Notion/Drive**: versão arquivável.

#### Checklist de envio
- [ ] Dados verificados (sem erros).
- [ ] Linguagem clara (cliente não técnico entende).
- [ ] Próximos passos definidos.
- [ ] Pendências do cliente destacadas.

---

### P10.4 — Relatório mensal (deep dive + plano do mês)
- **Código/ID**: P10.4
- **Tipo**: **[R] Recorrente** (mensal)
- **Objetivo**: análise profunda + apresentação de resultados + planejamento.
- **Momento**: primeira semana do mês seguinte.
- **Gatilho**: calendário mensal.
- **Saída**: relatório mensal + plano do próximo mês.
- **Papéis**: Gestor de Tráfego, CS, (opcional) Founder.
- **Ferramentas**: Ads Manager, Sheets/BI, Slides, Notion.

#### Estrutura do relatório mensal

```markdown
## Relatório Mensal — [Cliente]
**Período**: Mês/Ano

---

### 1. Resumo executivo
- Resultado principal: X leads com CPL R$ Y (vs meta de Z).
- Destaque positivo: [o que funcionou bem].
- Ponto de atenção: [o que precisa melhorar].
- Recomendação principal: [próximo foco].

---

### 2. Resultados do mês

#### Métricas gerais
| Métrica | Realizado | Meta | Variação |
|---------|-----------|------|----------|
| Investimento | R$ X | R$ Y | +/-% |
| Leads | X | Y | +/-% |
| CPL médio | R$ X | R$ Y | +/-% |
| CTR médio | X% | Y% | +/-% |
| CVR (LP) | X% | Y% | +/-% |

#### Evolução semanal
[Gráfico ou tabela semana a semana]

#### Por campanha/funil
| Campanha | Leads | CPL | % do total |
|----------|-------|-----|------------|
| TOFU | X | R$ Y | Z% |
| MOFU | X | R$ Y | Z% |
| RMK | X | R$ Y | Z% |

---

### 3. Análise de performance

#### O que funcionou
- Criativo X: [dados + por que funcionou]
- Público Y: [dados]

#### O que não funcionou
- Criativo Z: [dados + hipótese]
- Teste W: [resultado + aprendizado]

#### Qualidade dos leads
- Feedback do cliente: [resumo]
- Taxa de conversão lead→venda: [se disponível]
- Ajustes necessários: [se houver]

---

### 4. Testes e aprendizados
| Teste | Hipótese | Resultado | Aprendizado |
|-------|----------|-----------|-------------|
| X | Y | Ganhou/Perdeu | Z |

---

### 5. Plano do próximo mês

#### Metas
- Leads: X
- CPL meta: R$ Y
- Investimento: R$ Z

#### Estratégia
- Foco principal: [ex.: escalar público X]
- Testes planejados: [lista]
- Novos criativos: [quantidade/tipo]

#### Calendário
- Semana 1: [foco]
- Semana 2: [foco]
- Semana 3: [foco]
- Semana 4: [foco]

---

### 6. Pendências e alinhamentos
- [ ] [Pendência 1]
- [ ] [Alinhamento necessário]
```

#### Formato de entrega
- **Slides**: para apresentar em reunião.
- **PDF/Doc**: para arquivo.
- **Notion**: versão dinâmica.

---

### P10.5 — Reuniões de alinhamento (pauta, ata, decisões, próximos passos)
- **Código/ID**: P10.5
- **Tipo**: **[R] Recorrente**
- **Objetivo**: alinhar expectativas, discutir estratégia e tomar decisões conjuntas.
- **Momento**: frequência acordada (semanal, quinzenal ou mensal).
- **Gatilho**: calendário ou demanda específica.
- **Saída**: ata com decisões e próximos passos.
- **Papéis**: CS (facilitador), Gestor de Tráfego, Cliente.
- **Ferramentas**: Meet/Zoom, Notion (`Reuniões`).

#### Tipos de reunião

| Tipo | Frequência | Duração | Pauta principal |
|------|------------|---------|-----------------|
| Check-in rápido | Semanal | 15-30 min | Status, bloqueios, dúvidas |
| Revisão de performance | Quinzenal/Mensal | 45-60 min | Resultados, análise, plano |
| Estratégica | Trimestral | 60-90 min | Revisão de estratégia geral |
| Crise | Ad-hoc | Variável | Problema específico |

#### Pauta padrão (reunião de revisão)

```markdown
## Reunião — [Cliente] — DD/MM/YYYY

### 1. Status geral (5 min)
- Como estão as coisas do lado do cliente?
- Feedback sobre leads da última semana?

### 2. Resultados (10 min)
- Apresentar números principais.
- Destaques positivos e negativos.

### 3. Análise e discussão (15 min)
- O que funcionou e por quê?
- O que precisa ajustar?
- Hipóteses e próximos testes.

### 4. Próximos passos (10 min)
- O que vamos fazer.
- O que precisamos do cliente.
- Prazos.

### 5. Perguntas e alinhamentos (10 min)
- Espaço para dúvidas.
- Confirmação de entendimento.
```

#### Ata de reunião (template)

```markdown
## Ata — [Cliente] — DD/MM/YYYY

### Participantes
- [Nome] — Agência
- [Nome] — Cliente

### Decisões tomadas
1. [Decisão 1]
2. [Decisão 2]

### Próximos passos
| Ação | Responsável | Prazo |
|------|-------------|-------|
| X | Agência | DD/MM |
| Y | Cliente | DD/MM |

### Pendências do cliente
- [ ] [Pendência]

### Observações
- [Notas relevantes]
```

#### Registro no FL
- Criar item em `Reuniões` vinculado ao cliente.
- Criar tarefas a partir dos próximos passos.
- Registrar decisões importantes em `Decisões`.

---

### P10.6 — Gestão de expectativas e educação do cliente
- **Código/ID**: P10.6
- **Tipo**: **[R] Recorrente** (contínuo)
- **Objetivo**: evitar frustrações através de comunicação proativa sobre o que esperar.
- **Momento**: onboarding + continuamente.
- **Gatilho**: momentos-chave (início, mudanças, problemas).
- **Saída**: cliente alinhado e educado sobre o processo.
- **Papéis**: CS, Gestor de Tráfego.

#### Momentos de gestão de expectativa

**1. Onboarding**
- "Nas primeiras 2-4 semanas estamos em fase de testes. Resultados variam."
- "O Meta precisa de tempo para aprender. Paciência nas primeiras 72h."
- "CPL inicial pode ser mais alto até encontrarmos a fórmula."

**2. Lançamento de campanha**
- "Campanha vai ao ar hoje. Primeiros resultados em 24-48h."
- "Pode haver reprovações. Temos processo para resolver."
- "Fase de learning dura X dias."

**3. Problemas**
- "Identificamos [problema]. Estamos trabalhando em [solução]. Prazo: [X]."
- "Isso é comum e tem solução. Próximos passos: [lista]."

**4. Resultados abaixo do esperado**
- "Este mês ficamos abaixo da meta. Análise: [motivo]. Plano: [ações]."
- "Tráfego pago tem variância. Algumas semanas são melhores que outras."

**5. Resultados acima do esperado**
- "Excelente resultado! Vamos [escalar/manter/testar mais]."
- "Importante: manter consistência é mais importante que picos."

#### Educação do cliente (temas comuns)

| Tema | Quando abordar | Mensagem-chave |
|------|----------------|----------------|
| Fase de learning | Onboarding/lançamento | "Meta precisa de ~50 conversões para otimizar" |
| Variância de CPL | Sempre | "Resultado varia dia a dia; olhar tendência semanal" |
| Qualidade vs. volume | Quando pedir mais leads | "Mais leads nem sempre = mais vendas" |
| Sazonalidade | Datas específicas | "Black Friday/fim de ano afetam CPM" |
| Concorrência | Aumento de CPM | "Mais anunciantes = leilão mais caro" |

---

### P10.7 — Coleta de feedback/NPS + ações corretivas
- **Código/ID**: P10.7
- **Tipo**: **[R] Recorrente** (mensal/trimestral)
- **Objetivo**: medir satisfação e identificar melhorias.
- **Momento**: mensalmente ou após marcos importantes.
- **Gatilho**: calendário ou fim de projeto.
- **Saída**: score de satisfação + ações de melhoria.
- **Papéis**: CS, Founder.
- **Ferramentas**: Forms, WhatsApp, Notion.

#### Tipos de feedback

**1. Feedback informal (contínuo)**
- Prestar atenção em sinais durante comunicação.
- Perguntar: "Como você está se sentindo com o trabalho?"
- Documentar reclamações ou elogios.

**2. NPS (Net Promoter Score) — Trimestral**
- Pergunta: "De 0 a 10, qual a probabilidade de você recomendar nosso serviço?"
- Follow-up: "O que podemos melhorar?"

**3. Pesquisa de satisfação — Mensal**
```markdown
1. De 1 a 5, como você avalia:
   - Qualidade dos leads: [ ]
   - Comunicação da equipe: [ ]
   - Cumprimento de prazos: [ ]
   - Clareza dos relatórios: [ ]

2. O que está funcionando bem?
3. O que podemos melhorar?
4. Alguma sugestão ou pedido?
```

#### Classificação de NPS

| Score | Classificação | Ação |
|-------|---------------|------|
| 9-10 | Promotor | Pedir indicação/depoimento |
| 7-8 | Neutro | Identificar o que falta para ser 9-10 |
| 0-6 | Detrator | Reunião urgente para entender e resolver |

#### Ações corretivas

**Para detratores (0-6)**
- Marcar reunião imediata.
- Identificar problema específico.
- Criar plano de ação com prazos.
- Follow-up semanal até resolver.

**Para neutros (7-8)**
- Perguntar: "O que faria você nos dar 9 ou 10?"
- Implementar melhorias sugeridas.
- Comunicar mudanças.

**Para promotores (9-10)**
- Agradecer.
- Pedir depoimento/case (se aplicável).
- Ativar programa de indicação.

#### Registro
- `Clientes`: atualizar campo `NPS` e `Risco de Churn`.
- Criar tarefas para ações corretivas.
- Registrar feedback em histórico do cliente.
