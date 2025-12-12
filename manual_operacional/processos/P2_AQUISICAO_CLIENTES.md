## P2 — Aquisição de Clientes (Marketing & Prospecção)

> **Objetivo do macroprocesso (P2)**: gerar leads qualificados de forma previsível, com rastreabilidade de origem, cadência de contato e nutrição até call — sem depender do “improviso do dia”.

---

### P2.1 — Geração de leads via Meta Ads da agência
- **Código/ID**: P2.1
- **Tipo**: **[R] Recorrente** (semanal/mensal) + **[A]** integrações de captura
- **Objetivo**: gerar leads interessados no serviço da agência com CPL controlado e qualidade mínima.
- **Momento**: aquisição (topo/meio do funil da agência).
- **Gatilho de início**: meta de crescimento (ex.: X calls/mês) ou queda do pipeline.
- **Saída esperada**:
  - Campanhas ativas da agência + landing/WhatsApp funcionando.
  - Leads registrados em `Pipeline (Agência)` com `Origem = Ads`.
- **Papéis envolvidos**: Founder/Diretor, Gestor de Tráfego, Copywriter, Designer, (opcional) SDR.
- **Ferramentas**: Meta Ads, Drive, Notion (Pipeline), WhatsApp/e-mail, Make/Zapier.

#### Passo a passo (tarefas e subtarefas)
- **P2.1-T1 (Obrigatória) Definir oferta de aquisição da agência**
  - Definir “isca”: diagnóstico gratuito, auditoria, plano de ação, etc.
  - Definir público-alvo (ICP) e promessa segura (sem claims proibidos).
- **P2.1-T2 (Obrigatória) Definir página/canal de conversão**
  - Opção A: LP com formulário → e-mail/WhatsApp.
  - Opção B: WhatsApp direto com mensagem pré-preenchida.
- **P2.1-T3 (Obrigatória) Criar ativos de campanha**
  - Copy: 3–5 ângulos (dor, oportunidade, prova, método, autoridade).
  - Criativos: 10+ variações (estático + vídeo curto).
- **P2.1-T4 (Obrigatória) Setup e publicação**
  - Estruturar campanhas (ABO/CBO), públicos (broad/interesses), placements.
  - UTMs padrão.
- **P2.1-T5 (Obrigatória) Rotina de otimização**
  - D+1/D+3: checar CTR, CPC, CPL, qualidade.
  - Ajustar criativo/público/orçamento.
- **P2.1-T6 (Obrigatória) Registrar aprendizados**
  - Criar item em `Testes & Hipóteses` com resultado e próxima iteração.

#### Checklist operacional (antes de ativar)
- Pixel/UTM funcionando (ou tracking mínimo de clique/lead).
- Mensagens sem promessas sensíveis (“garantia de resultados”).
- LP/WhatsApp com resposta automática e SLA.
- Formulário com campos mínimos de qualificação.

#### Critérios de qualidade / aceitação
- Leads criados corretamente no `Pipeline (Agência)`.
- Tempo para 1º contato < 15 min (meta) para leads quentes.
- CPL dentro da meta definida **e** taxa de agendamento aceitável.

#### Métricas relacionadas
- CPL (agência), taxa de conversão LP→lead, lead→call agendada, show rate.
- CAC (agência), taxa de fechamento, payback.

#### Oportunidades de automação
- **Gatilho**: novo lead via formulário/Lead Ads → **Ação**: criar item no `Pipeline (Agência)` + tarefa “Contato inicial” + mensagem automática de confirmação.
- **Gatilho**: etapa muda para `Call agendada` → **Ação**: criar tarefas de preparo + lembretes.

#### Templates/padrões
- Script de anúncio da agência, LP padrão, sequência de mensagens (nutrição), padrão UTM.

#### Fluxos de exceção
- **Lead entra fora do ICP**: marcar `Perdido (Sem fit)` + registrar motivo.
- **CPL baixo mas qualidade ruim**: ajustar promessa, formulário (perguntas), criativos e segmentação.

---

### P2.2 — Conteúdo orgânico (Instagram/YouTube/LinkedIn)
- **Código/ID**: P2.2
- **Tipo**: **[R] Recorrente**
- **Objetivo**: gerar demanda orgânica e autoridade que aumente conversão de prospecção e diminua CAC.
- **Momento**: aquisição contínua.
- **Gatilho**: calendário semanal de conteúdo.
- **Saída**: posts publicados + leads capturados (DM/WhatsApp) registrados no pipeline.
- **Papéis**: Founder (ou social media), Copywriter, Designer/Editor.
- **Ferramentas**: Instagram/YouTube/LinkedIn, Drive, Notion.

#### Passo a passo
- **P2.2-T1 (Obrigatória) Planejamento semanal**: 5 temas + CTA (call/WhatsApp).
- **P2.2-T2 (Obrigatória) Produção**: roteiro → gravação → edição → legenda.
- **P2.2-T3 (Obrigatória) Publicação + distribuição**: publicar, comentar, responder DMs.
- **P2.2-T4 (Obrigatória) Captura**: todo lead em DM/WhatsApp vira item em `Pipeline (Agência)`.

#### Checklist
- CTA claro (o que fazer agora).
- Prova/autoridade (cases, números, bastidores).
- Link e mensagem padrão prontos.

#### Qualidade
- Consistência semanal.
- Leads registrados com origem correta.

#### Métricas
- Leads por semana, taxa DM→call, alcance/engajamento, crescimento do perfil.

#### Automação
- Formulário link-in-bio → Notion.

#### Exceções
- Baixo volume: reforçar distribuição, colabs, CTA mais direto, reaproveitar (shorts/reels).

---

### P2.3 — Indicações e parcerias
- **Código/ID**: P2.3
- **Tipo**: **[R] Recorrente** + **[P] pipeline de parceiros**
- **Objetivo**: gerar leads de alta confiança (alta taxa de fechamento).
- **Gatilho**: meta mensal de parcerias / disparo de campanha de indicações.
- **Saída**: novos leads em `Pipeline (Agência)` com origem `Indicação/Parceria`.
- **Papéis**: Founder/Closer, CS (para pedir indicação), Parceiros.
- **Ferramentas**: Notion, WhatsApp/e-mail, Drive.

#### Passo a passo
- **P2.3-T1 (Obrigatória) Definir programa de indicação**: benefício, regras e tracking.
- **P2.3-T2 (Obrigatória) Lista de parceiros-alvo**: contadores, devs, consultores, agências complementares.
- **P2.3-T3 (Obrigatória) Contato e proposta de parceria**: mensagem + call.
- **P2.3-T4 (Obrigatória) Registro**: criar item no pipeline de parceiros + próximas ações.
- **P2.3-T5 (Recorrente) Manutenção**: check-in mensal + atualização de materiais.

#### Checklist
- Regras claras (quando paga, para quem, como comprovar).
- Materiais prontos (deck, one-pager, case).

#### Métricas
- Leads indicados/mês, taxa de fechamento, CAC por canal.

#### Exceções
- Parceiro não entrega: encerrar parceria e registrar motivo.

---

### P2.4 — Eventos/workshops/aulas
- **Código/ID**: P2.4
- **Tipo**: **[R] Recorrente** (mensal/trimestral)
- **Objetivo**: aquisição em lote + autoridade.
- **Gatilho**: calendário de eventos.
- **Saída**: lista de participantes + follow-up + calls agendadas.
- **Papéis**: Founder, SDR/CS.
- **Ferramentas**: Zoom/Meet, Drive, Notion, WhatsApp/e-mail.

#### Passo a passo
- Planejar tema, convite, landing, captação.
- Executar evento.
- Pós-evento: mensagem + oferta (diagnóstico) + agendamento.

#### Métricas
- inscritos, presença, agendamentos, fechamento.

---

### P2.5 — Captura e registro de leads no pipeline (Notion)
- **Código/ID**: P2.5
- **Tipo**: **[P+A] Pipeline + automação**
- **Objetivo**: garantir que todo lead vire registro rastreável e gere próxima ação.
- **Gatilho**: lead chega (form/Lead Ads/WhatsApp/DM).
- **Saída**: item no `Pipeline (Agência)` com etapa correta + tarefa criada.
- **Papéis**: SDR/Closer, Ops.
- **Ferramentas**: Notion, Make/Zapier, WhatsApp/e-mail.

#### Passo a passo
- **P2.5-T1 (Obrigatória) Padronizar campos**: nome, empresa, origem, dor, orçamento (se possível).
- **P2.5-T2 (Obrigatória) Criar/atualizar lead** no `Pipeline (Agência)`.
- **P2.5-T3 (Obrigatória) Criar tarefa** `Contato inicial` com SLA.
- **P2.5-T4 (Obrigatória) Registrar interação** em `Interações`.

#### Checklist
- Origem preenchida.
- Próxima ação com data.

#### Exceções
- Lead duplicado: mesclar e manter histórico.

---

### P2.6 — Primeiro contato + nutrição até call
- **Código/ID**: P2.6
- **Tipo**: **[R+A] Recorrente + automação**
- **Objetivo**: aumentar taxa de agendamento e show, reduzindo perda por falta de resposta.
- **Gatilho**: lead novo no pipeline.
- **Saída**: lead em `Call agendada` ou `Perdido/Nutrição` com motivo.
- **Papéis**: SDR/Closer.
- **Ferramentas**: WhatsApp, e-mail, Notion.

#### Passo a passo
- **P2.6-T1 (Obrigatória) Mensagem em até 15 min** (template).
- **P2.6-T2 (Obrigatória) Pré-qualificação rápida** (3–5 perguntas).
- **P2.6-T3 (Obrigatória) Direcionar para agendamento** (Calendly/link).
- **P2.6-T4 (Recorrente) Sequência de follow-up** (D0/D1/D3/D7).

#### Checklist
- Personalização mínima (nome/negócio).
- Perguntas de fit.

#### Qualidade
- Lead sem resposta recebe sequência completa.

#### Métricas
- Tempo até 1º contato, taxa de resposta, taxa de agendamento, show rate.

#### Exceções
- Lead não responde: mover para `Nutrição` + tarefa de reativação.

---

### P2.7 — Higienização/enriquecimento de leads
- **Código/ID**: P2.7
- **Tipo**: **[R] Recorrente**
- **Objetivo**: manter pipeline limpo e dados consistentes.
- **Gatilho**: semanal (ex.: sexta).
- **Saída**: leads com status atualizado, motivos registrados.
- **Papéis**: SDR/Closer.
- **Ferramentas**: Notion.

#### Passo a passo
- Revisar leads sem próxima ação.
- Marcar perdas com motivo.
- Atualizar campos faltantes.

#### Métricas
- % leads sem próxima ação, tempo médio no pipeline.
