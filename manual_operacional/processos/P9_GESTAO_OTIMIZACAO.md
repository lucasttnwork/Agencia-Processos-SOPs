## P9 — Rotina de Gestão e Otimização

> **Objetivo do macroprocesso (P9)**: manter campanhas performando através de análise sistemática, decisões baseadas em dados e registro de aprendizados — transformando gestão de tráfego em processo replicável e escalável.

---

### P9.1 — Rotina diária (saúde da conta + alertas)
- **Código/ID**: P9.1
- **Tipo**: **[R] Recorrente** (diária)
- **Objetivo**: identificar problemas rapidamente e garantir que campanhas estão entregando.
- **Momento**: início do dia (manhã) + final do dia (se necessário).
- **Gatilho**: calendário diário.
- **Saída esperada**:
  - Problemas críticos identificados e acionados.
  - Registro rápido de status (opcional).
- **Papéis envolvidos**: Gestor de Tráfego.
- **Ferramentas**: Ads Manager, Events Manager, Notion.

#### Duração estimada
- 10–15 minutos por cliente ativo.

#### Checklist diário (por cliente)

**1. Saúde geral**
- [ ] Campanhas ativas estão entregando (impressões > 0)
- [ ] Nenhum anúncio reprovado novo
- [ ] Nenhuma conta com restrições/avisos
- [ ] Gasto dentro do esperado (sem estouro nem subgasto)

**2. Métricas rápidas**
- [ ] CPM dentro da faixa (sem picos anormais)
- [ ] CTR sem queda brusca (> 50% do baseline)
- [ ] Conversões estão chegando (se campanha > 24h)
- [ ] Leads estão chegando no destino (Notion/WhatsApp)

**3. Alertas para ação imediata**
- Anúncio reprovado → P12.1
- Conta bloqueada → P12.2
- Zero conversões com gasto significativo → investigar
- Leads não chegando → verificar integração (P7.5)

#### Registro (opcional)
- Log rápido no Notion ou planilha: "OK" ou "Problema X identificado".

#### Automação Python (A03 + A06)
- Script que verifica automaticamente:
  - Campanhas sem entrega.
  - Anúncios reprovados.
  - Gasto vs. budget.
  - Alerta via WhatsApp/Telegram se problema detectado.

---

### P9.2 — Rotina semanal (análise, decisões, refresh, roadmap)
- **Código/ID**: P9.2
- **Tipo**: **[R] Recorrente** (semanal)
- **Objetivo**: analisar performance, tomar decisões de otimização e planejar próxima semana.
- **Momento**: início da semana (segunda ou terça).
- **Gatilho**: calendário semanal.
- **Saída esperada**:
  - Análise documentada.
  - Decisões de otimização registradas.
  - Roadmap de ações da semana.
- **Papéis**: Gestor de Tráfego.
- **Ferramentas**: Ads Manager, Sheets/BI, Notion.

#### Duração estimada
- 30–60 minutos por cliente.

#### Passo a passo

**1. Análise de performance (últimos 7 dias)**
- Exportar ou visualizar dados da semana.
- Comparar com semana anterior e baseline.
- Identificar:
  - Top performers (criativos, públicos, campanhas).
  - Bottom performers.
  - Tendências (subindo, caindo, estável).

**2. Métricas a analisar**

| Nível | Métricas |
|-------|----------|
| Conta | Gasto total, leads totais, CPL médio |
| Campanha | CPL, CVR, ROAS (se aplicável), gasto |
| Conjunto | CTR, CPC, CPM, frequência, CPL |
| Anúncio | CTR, CPC, conversões, frequência |

**3. Decisões de otimização**
- O que pausar? (CPL > 2x meta, frequência alta, CTR baixo)
- O que escalar? (CPL < meta, volume bom, consistente)
- O que testar? (novas hipóteses, novos criativos)
- O que ajustar? (orçamento, público, posicionamento)

**4. Planejamento da semana**
- Criar tarefas no Notion:
  - Novos criativos necessários.
  - Novos testes a implementar.
  - Ajustes a fazer.

**5. Registro**
- Atualizar `Testes & Hipóteses` com resultados.
- Registrar decisões importantes em `Decisões`.

#### Template de análise semanal
```markdown
## Semana [DD/MM - DD/MM] — [Cliente]

### Resumo
- Gasto: R$ X
- Leads: X
- CPL médio: R$ X
- Variação vs semana anterior: +/-X%

### Top performers
- Criativo X: CPL R$ Y, X leads
- Público Z: CTR X%, CPL R$ Y

### Bottom performers
- Criativo A: CPL R$ Y (2x meta), pausar
- Público B: frequência X, saturado

### Decisões
- [ ] Pausar criativo A
- [ ] Escalar público Z (+20% budget)
- [ ] Testar novo ângulo (oferta X)

### Próxima semana
- Entregar 3 novos criativos
- Testar público lookalike
```

---

### P9.3 — Rotina mensal (deep dive + planejamento)
- **Código/ID**: P9.3
- **Tipo**: **[R] Recorrente** (mensal)
- **Objetivo**: análise profunda, revisão de estratégia e planejamento do próximo mês.
- **Momento**: última semana do mês ou primeira do próximo.
- **Gatilho**: calendário mensal.
- **Saída**: relatório mensal (P10.4) + plano do mês.
- **Papéis**: Gestor de Tráfego, CS.
- **Ferramentas**: Ads Manager, Sheets/BI, Notion, Drive.

#### Duração estimada
- 1–2 horas por cliente.

#### Análise mensal

**1. Performance geral**
- Gasto total vs. orçamento.
- Leads totais vs. meta.
- CPL médio vs. meta.
- Tendência: melhorou, piorou, estável?

**2. Análise por funil**
- TOFU: alcance, CPM, CTR.
- MOFU/BOFU: engajamento, conversões.
- RMK: frequência, conversões incrementais.

**3. Análise de criativos**
- Quais criativos performaram melhor?
- Quais falharam?
- Padrões identificados (hook, formato, oferta).

**4. Análise de públicos**
- Quais públicos deram melhor CPL?
- Saturação (frequência alta)?
- Novos públicos a testar?

**5. Qualidade de leads**
- Feedback do cliente (leads bons ou ruins?).
- Taxa de conversão lead → venda (se disponível).
- Ajustes necessários?

**6. Planejamento do próximo mês**
- Meta de leads/CPL.
- Orçamento planejado.
- Testes prioritários.
- Criativos necessários.
- Mudanças de estratégia.

---

### P9.4 — Regras de decisão (pausar, escalar, trocar criativo, oferta)
- **Código/ID**: P9.4
- **Tipo**: **[U+R] Definir uma vez + aplicar recorrentemente**
- **Objetivo**: ter critérios claros para decisões, evitando subjetividade.
- **Momento**: durante rotinas diária/semanal.
- **Gatilho**: métricas fora dos parâmetros.
- **Saída**: ação tomada e registrada.
- **Papéis**: Gestor de Tráfego.

#### Regras de decisão padrão

**Quando PAUSAR um anúncio/conjunto**
| Condição | Ação |
|----------|------|
| CPL > 2x meta por 3+ dias | Pausar |
| Frequência > 3 (cold) ou > 6 (RMK) | Pausar ou renovar |
| CTR < 0.5% por 3+ dias | Pausar |
| Zero conversões com > R$ 100 gastos | Pausar e investigar |
| Anúncio reprovado 2x | Substituir criativo |

**Quando ESCALAR**
| Condição | Ação |
|----------|------|
| CPL < meta por 5+ dias | Aumentar budget 20-30% |
| CTR > 1.5% e CPL ok | Testar novos públicos similares |
| Conversões consistentes | Expandir para novos posicionamentos |

**Quando TROCAR CRIATIVO**
| Condição | Ação |
|----------|------|
| CTR caiu > 30% vs baseline | Novo criativo |
| Frequência > 3 (cold) | Novo criativo |
| Mesmo criativo > 4 semanas | Considerar refresh |

**Quando AJUSTAR OFERTA/MENSAGEM**
| Condição | Ação |
|----------|------|
| CTR alto mas CVR baixo | Problema na LP ou oferta |
| Leads mas baixa qualidade | Ajustar qualificação ou mensagem |
| Objeções recorrentes | Ajustar copy/prova |

#### Exceções
- Cliente com budget limitado: ser mais conservador.
- Fase de testes: dar mais tempo antes de pausar.

---

### P9.5 — Registro de testes/hipóteses/resultados (playbook vivo)
- **Código/ID**: P9.5
- **Tipo**: **[R] Recorrente**
- **Objetivo**: construir conhecimento acumulado sobre o que funciona/não funciona.
- **Momento**: sempre que um teste é iniciado ou concluído.
- **Gatilho**: novo teste ou resultado disponível.
- **Saída**: registro em `Testes & Hipóteses` no Notion.
- **Papéis**: Gestor de Tráfego.
- **Ferramentas**: Notion (`Testes & Hipóteses`).

#### Estrutura do registro

```markdown
## Teste: [Nome descritivo]

### Informações básicas
- **Cliente**: [Nome]
- **Data início**: DD/MM/YYYY
- **Data fim**: DD/MM/YYYY
- **Status**: Em andamento / Concluído

### Hipótese
"Acreditamos que [variável X] vai [melhorar/piorar] [métrica Y] porque [razão Z]."

### Variável testada
- [ ] Criativo (hook, formato, estilo)
- [ ] Copy (ângulo, CTA, tamanho)
- [ ] Público (interesse, LAL, RMK)
- [ ] Oferta (preço, bônus, urgência)
- [ ] LP (headline, formulário, layout)
- [ ] Configuração (orçamento, otimização, posicionamento)

### Setup do teste
- Controle: [descrição]
- Variante: [descrição]
- Orçamento: R$ X
- Duração planejada: X dias
- Critério de decisão: [ex.: CPL 20% menor com 50+ conversões]

### Resultado
- Controle: CPL R$ X, CTR Y%, X conversões
- Variante: CPL R$ X, CTR Y%, X conversões
- **Vencedor**: Controle / Variante / Inconclusivo
- **Significância**: Alta / Média / Baixa

### Aprendizado
- O que aprendemos?
- O que fazer diferente?
- Próximo teste sugerido?
```

#### Boas práticas
- Um teste por vez (evitar confusão).
- Orçamento suficiente para significância estatística.
- Documentar mesmo testes que falharam.
- Revisar aprendizados antes de novos testes.

---

### P9.6 — Gestão de fadiga criativa (frequência/CTR/queda)
- **Código/ID**: P9.6
- **Tipo**: **[R] Recorrente**
- **Objetivo**: detectar e resolver saturação de criativos antes que prejudique performance.
- **Momento**: durante rotina semanal.
- **Gatilho**: métricas de fadiga detectadas.
- **Saída**: decisão de pausar/substituir + demanda de novos criativos.
- **Papéis**: Gestor de Tráfego, Copy/Design.
- **Ferramentas**: Ads Manager, Notion.

#### Indicadores de fadiga criativa

| Indicador | Threshold | Ação |
|-----------|-----------|------|
| Frequência > 3 (cold) | Atenção | Monitorar / Substituir |
| Frequência > 6 (RMK) | Crítico | Substituir |
| CTR caiu > 30% vs baseline | Atenção | Testar novo criativo |
| CTR caiu > 50% | Crítico | Pausar e substituir |
| CPL aumentou > 30% | Atenção | Investigar (pode ser fadiga) |
| Mesmo criativo > 4 semanas | Atenção | Planejar refresh |

#### Processo de renovação

1. **Identificar criativos fadigados** (rotina semanal).
2. **Priorizar substituição** (P0 = crítico, P1 = atenção).
3. **Solicitar novos criativos** (P6.1 - intake de demanda).
4. **Testar novo vs. fadigado** (se ainda entregando).
5. **Pausar fadigado** quando novo performar.

#### Backlog de criativos
- Manter sempre 2-3 criativos "na reserva" por cliente.
- Processo P6.9 (backlog contínuo) alimenta este processo.

---

### P9.7 — Governança de orçamento e pacing
- **Código/ID**: P9.7
- **Tipo**: **[R] Recorrente**
- **Objetivo**: garantir que orçamento seja gasto de forma otimizada e dentro do planejado.
- **Momento**: diário (check rápido) + semanal (ajustes).
- **Gatilho**: gasto fora do esperado.
- **Saída**: ajustes de orçamento documentados.
- **Papéis**: Gestor de Tráfego.
- **Ferramentas**: Ads Manager, Sheets, Notion.

#### Monitoramento de pacing

**Fórmula básica**
```
Pacing ideal = (Orçamento mensal / Dias do mês) × Dias passados
Pacing real = Gasto até o momento
Diferença = Pacing real - Pacing ideal
```

**Ações por situação**

| Situação | Causa provável | Ação |
|----------|----------------|------|
| Gastando muito rápido (> 10% acima) | Campanha performando bem ou erro de config | Verificar se é intencional; ajustar budget se necessário |
| Gastando devagar (> 10% abaixo) | Público pequeno, bid baixo, criativos não entregando | Ampliar público, revisar criativos, ajustar otimização |
| Estouro de orçamento | Sem limite configurado | Configurar limites de conta/campanha |
| Subgasto significativo | Campanhas pausadas, problemas de entrega | Investigar e resolver bloqueios |

#### Governança de orçamento

**Níveis de aprovação para mudanças**
| Mudança | Aprovação |
|---------|-----------|
| Ajuste < 20% do budget | Gestor de Tráfego |
| Ajuste 20-50% | Gestor + CS |
| Ajuste > 50% ou aumento não planejado | Cliente |

**Registro**
- Documentar mudanças de orçamento em `Decisões`.
- Comunicar cliente se mudança significativa.

---

### P9.8 — Monitoramento de qualidade de lead (feedback loop)
- **Código/ID**: P9.8
- **Tipo**: **[R] Recorrente** (semanal)
- **Objetivo**: garantir que leads gerados são úteis para o cliente (não apenas volume).
- **Momento**: rotina semanal + feedback do cliente.
- **Gatilho**: leads gerados + feedback disponível.
- **Saída**: score de qualidade + ajustes de campanha.
- **Papéis**: Gestor de Tráfego, CS, Cliente.
- **Ferramentas**: Notion (`Leads do Cliente`), CRM do cliente, WhatsApp.

#### Métricas de qualidade de lead

| Métrica | Como medir | Meta típica |
|---------|------------|-------------|
| Taxa de contato | Leads contatados / Total leads | > 80% |
| Taxa de qualificação | Leads qualificados / Leads contatados | > 50% |
| Taxa de agendamento | Agendamentos / Leads qualificados | > 30% |
| Taxa de comparecimento | Compareceram / Agendamentos | > 70% |
| Taxa de venda | Vendas / Compareceram | Varia por nicho |

#### Feedback loop

**1. Coleta de feedback (semanal)**
- Perguntar ao cliente: "Como estão os leads desta semana?"
- Coletar dados do CRM/Notion: etapas dos leads.
- Identificar padrões: leads de qual fonte/criativo são melhores?

**2. Análise**
- Leads de baixa qualidade vêm de qual campanha/criativo?
- Há padrão de horário, dia, público?
- Formulário está qualificando bem?

**3. Ações corretivas**
| Problema | Ação |
|----------|------|
| Leads não respondem | Verificar tempo de contato, ajustar mensagem |
| Leads sem dinheiro/interesse | Ajustar segmentação, adicionar perguntas no form |
| Leads errados (outro serviço) | Ajustar copy para ser mais específica |
| Leads spam/fake | Adicionar campos de qualificação, considerar LP em vez de Lead Ads |

**4. Registro**
- Atualizar `Leads do Cliente` com qualidade (se possível).
- Registrar aprendizados em `Testes & Hipóteses`.

#### Automação Python (futuro)
- Script que coleta feedback automaticamente via form/WhatsApp.
- Atualiza qualidade dos leads no Notion.
- Alerta se qualidade cair abaixo do threshold.
