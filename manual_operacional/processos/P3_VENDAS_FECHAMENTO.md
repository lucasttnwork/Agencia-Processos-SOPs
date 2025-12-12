## P3 — Vendas & Fechamento

> **Objetivo do macroprocesso (P3)**: converter leads qualificados em contratos assinados com escopo claro, expectativas alinhadas e handoff perfeito para onboarding.

---

### P3.1 — Pré-qualificação (fit mínimo)
- **Código/ID**: P3.1
- **Tipo**: **[P] Pipeline**
- **Objetivo**: filtrar rapidamente leads sem potencial (ou sem momento) e priorizar os com maior chance.
- **Momento**: antes da call.
- **Gatilho**: lead em `Novo` / `Contato feito`.
- **Saída**: lead classificado (`Pré-qualificado` / `Nutrição` / `Perdido`).
- **Papéis**: SDR/Closer.
- **Ferramentas**: Notion (`Pipeline` + `Interações`), WhatsApp/e-mail.

#### Passo a passo
- **P3.1-T1 (Obrigatória) Perguntas de fit** (via WhatsApp):
  - segmento/localidade, oferta, ticket médio, orçamento de mídia, estrutura comercial/atendimento.
- **P3.1-T2 (Obrigatória) Classificar**:
  - `Fit` (sim/não) + prioridade.
- **P3.1-T3 (Obrigatória) Próxima ação**:
  - agendar call ou nutrir.

#### Checklist
- Orçamento de mídia mínimo definido (se aplicável).
- Existe alguém para atender leads rapidamente.

#### Qualidade
- Motivo de perda registrado para ajustar ICP.

#### Métricas
- % leads pré-qualificados, tempo até pré-qualificação, taxa de call agendada.

#### Exceções
- Lead tem fit, mas sem estrutura de atendimento: oferecer “setup mínimo + scripts + automação” como pré-requisito.

---

### P3.2 — Agendamento de call + confirmações
- **Código/ID**: P3.2
- **Tipo**: **[P+A] Pipeline + automação**
- **Objetivo**: reduzir no-show e melhorar taxa de comparecimento.
- **Gatilho**: lead `Pré-qualificado`.
- **Saída**: `Call agendada` com lembretes enviados.
- **Papéis**: SDR/Closer.
- **Ferramentas**: Calendly/agenda, WhatsApp/e-mail, Notion.

#### Passo a passo
- Enviar link de agendamento (janela de 3–5 dias).
- Confirmar horário (D-1) e lembrar (H-3 e H-1).
- Criar tarefa: `Preparar call`.

#### Checklist
- Link de agenda funcionando.
- Timezone correto.

#### Métricas
- show rate, reagendamentos, tempo lead→call.

#### Automação
- Agendou → criar tarefa “Preparar call” + “Enviar confirmação” + atualizar etapa.

#### Exceções
- No-show: mover para `No-show`, disparar sequência de reagendamento (D0/D1/D3).

---

### P3.3 — Preparação da call
- **Código/ID**: P3.3
- **Tipo**: **[U] Única**
- **Objetivo**: chegar na call com contexto e hipóteses claras.
- **Gatilho**: call agendada.
- **Saída**: notas de preparação + hipóteses.
- **Papéis**: Closer.
- **Ferramentas**: site do lead, Meta Ad Library, Notion.

#### Passo a passo
- Revisar site/Instagram; identificar oferta e fricções.
- Checar sinais de demanda e posicionamento.
- Anotar hipóteses (3 alavancas): oferta, criativo, funil, atendimento.

#### Checklist
- Entender o que o lead vende e para quem.

---

### P3.4 — Call de diagnóstico
- **Código/ID**: P3.4
- **Tipo**: **[U] Única**
- **Objetivo**: diagnosticar, gerar confiança e definir caminho (fit + plano).
- **Gatilho**: horário da call.
- **Saída**: diagnóstico + próximos passos + dados para operação.
- **Papéis**: Closer (Founder opcional).
- **Ferramentas**: Meet/Zoom, Notion (template de notas).

#### Passo a passo (roteiro mínimo)
- Contexto e meta do cliente (resultado final desejado).
- Oferta e ticket; capacidade (atender/fechar).
- Histórico de tráfego (o que já tentou e por quê falhou).
- Pilares: (1) oferta, (2) criativos, (3) tracking, (4) atendimento.
- Alinhamento de expectativa (prazo de testes, variância, responsabilidades).
- Próximo passo: proposta.

#### Checklist
- Coletar: acesso a BM? site/LP? CRM? WhatsApp? orçamento?

#### Qualidade
- Saída clara: “vamos fazer X em Y dias”.

#### Métricas
- taxa call→proposta, taxa call→ganho.

#### Exceções
- Se não há fit: encaminhar recomendação mínima e encerrar com elegância.

---

### P3.5 — Proposta comercial + escopo (SOW)
- **Código/ID**: P3.5
- **Tipo**: **[U] Única**
- **Objetivo**: transformar diagnóstico em escopo claro e vendável.
- **Gatilho**: call realizada.
- **Saída**: proposta + SOW + termos.
- **Papéis**: Closer/Founder, (opcional) Financeiro.
- **Ferramentas**: Drive (modelo), Notion (registro), e-mail.

#### Passo a passo
- Selecionar plano (retainer) + extras.
- Definir escopo: entregáveis, SLAs, número de criativos/mes, reuniões.
- Definir limites: orçamento de mídia é do cliente; prazos; aprovações.
- Definir condições: pagamento, cancelamento, acesso.

#### Checklist
- Escopo sem ambiguidades.
- Promessas compatíveis com políticas e realidade.

#### Qualidade
- Proposta com seção “o que NÃO está incluso”.

#### Métricas
- tempo call→proposta, taxa proposta→ganho.

---

### P3.6 — Envio de proposta/contrato + acompanhamento
- **Código/ID**: P3.6
- **Tipo**: **[P+A] Pipeline + automação**
- **Objetivo**: manter cadência de follow-up até decisão.
- **Gatilho**: proposta enviada.
- **Saída**: `Ganho` ou `Perdido` com motivo.
- **Papéis**: Closer.
- **Ferramentas**: e-mail/WhatsApp, Notion.

#### Passo a passo
- Enviar e-mail com proposta + resumo.
- Follow-up em D1/D3/D7.
- Registrar objeções e respostas.

#### Exceções
- “Sumiu”: mover para `Nutrição` e sequenciar reativação.

---

### P3.7 — Pagamento inicial + criação de cliente no FL
- **Código/ID**: P3.7
- **Tipo**: **[U+A] Única + automação**
- **Objetivo**: iniciar operação só com base jurídica/financeira ok.
- **Gatilho**: contrato assinado (ou aceite formal) + pagamento.
- **Saída**: registro em `Clientes` + `Projeto Onboarding` criado.
- **Papéis**: Financeiro, CS/Ops, Founder.
- **Ferramentas**: Notion, Drive, e-mail, (opcional) gateway.

#### Passo a passo
- Confirmar assinatura.
- Confirmar pagamento (ou acordos).
- Criar `Cliente_ID`, pasta Drive, dossiê, projeto onboarding.

#### Checklist
- Dados fiscais e contatos do cliente.

---

### P3.8 — Handoff para onboarding (kickoff interno)
- **Código/ID**: P3.8
- **Tipo**: **[U] Única**
- **Objetivo**: evitar perda de informação entre vendas e operação.
- **Gatilho**: cliente ganho.
- **Saída**: briefing inicial de vendas + riscos + metas.
- **Papéis**: Closer → CS + Gestor de Tráfego.
- **Ferramentas**: Notion (template handoff).

#### Passo a passo
- Preencher template: meta, oferta, ticket, objeções, restrições, prazos.
- Reunião interna (15 min) se necessário.

---

### P3.9 — Follow-up estruturado (quase-fechados / nutrição)
- **Código/ID**: P3.9
- **Tipo**: **[R] Recorrente**
- **Objetivo**: aumentar conversão sem aumentar volume de leads.
- **Gatilho**: leads em `Negociação` ou `Nutrição`.
- **Saída**: decisão tomada ou reativação futura.
- **Papéis**: Closer.
- **Ferramentas**: WhatsApp/e-mail, Notion.

#### Passo a passo
- Sequência por contexto: objeção preço, timing, confiança, parceiro atual.
- Enviar prova (case/antes-depois) e reforço de próximos passos.

#### Métricas
- taxa de reativação, ganho tardio.
