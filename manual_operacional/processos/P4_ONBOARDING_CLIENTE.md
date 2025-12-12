## P4 — Onboarding de Cliente

> **Objetivo do macroprocesso (P4)**: transformar um cliente “ganho” em um cliente **pronto para rodar campanha** com: briefing completo, acessos validados, tracking mínimo funcionando, expectativas alinhadas e operação organizada no FL/Notion.

---

### P4.1 — Boas-vindas + alinhamento de expectativas + SLAs
- **Código/ID**: P4.1
- **Tipo**: **[U] Única**
- **Objetivo**: alinhar o “como vamos trabalhar” para evitar ruído e churn precoce.
- **Momento**: imediatamente após contrato/pagamento.
- **Gatilho**: `Cliente` criado no Notion com `Status do Cliente = Onboarding`.
- **Saída esperada**:
  - Canal oficial definido.
  - SLAs e rituais acordados (relatórios/reuniões).
  - Agenda do onboarding confirmada.
- **Papéis envolvidos**: CS/Atendimento (dono do processo), Founder (opcional), cliente (contato principal).
- **Ferramentas**: WhatsApp/e-mail, Notion (`Clientes`, `Contatos`, `Projetos/Entregas`, `Tarefas`).

#### Registro no FL (dados mínimos)
- `Clientes`: `Canal oficial`, `SLA combinado`, `Responsável CS`, `Gestor de Tráfego`.
- `Contatos`: contato principal + financeiro + TI (se houver).
- `Projeto`: criar `Projeto — Onboarding`.

#### Passo a passo
- **P4.1-T1 (Obrigatória) Enviar mensagem de boas-vindas** (template) com:
  - próximos passos do onboarding,
  - lista de acessos/documentos,
  - prazos.
- **P4.1-T2 (Obrigatória) Confirmar canal oficial** (WhatsApp grupo ou 1:1) e regras:
  - horário de atendimento,
  - urgências (o que é urgência),
  - SLA.
- **P4.1-T3 (Obrigatória) Marcar reunião de kickoff** (se aplicável).
- **P4.1-T4 (Obrigatória) Criar tarefas do onboarding** no Notion (checklist padrão).

#### Checklist operacional
- Cliente sabe o que precisa entregar (acessos e materiais).
- Cliente entende que performance inicial = fase de testes.

#### Critérios de qualidade / aceitação
- Cliente confirma por escrito (WhatsApp/e-mail) o canal e SLAs.
- Tarefas de onboarding criadas com prazos.

#### Métricas
- Tempo de resposta (CS), tempo para concluir onboarding.

#### Automação
- **Gatilho**: `Status do Cliente = Onboarding` → **Ação**: criar `Projeto Onboarding` + tarefas padrão + e-mail/WhatsApp de boas-vindas.

#### Fluxos de exceção
- Cliente quer “tudo por áudio e fora do horário”: reforçar canal oficial + política de SLA.

---

### P4.2 — Briefing completo (negócio, público, oferta, histórico)
- **Código/ID**: P4.2
- **Tipo**: **[U] Única**
- **Objetivo**: coletar informações operacionais e estratégicas suficientes para planejar campanha e criativos.
- **Momento**: primeiro passo do onboarding.
- **Gatilho**: kickoff marcado ou contrato assinado.
- **Saída**: briefing preenchido + materiais anexados/links.
- **Papéis**: CS (conduz), Gestor de Tráfego, Copy/Designer (consultados), cliente.
- **Ferramentas**: Form/Doc (Drive), Notion (Dossiê do Cliente).

#### Registro no FL
- `Clientes`: `Oferta do Cliente`, `Nicho`, `Região`, `Meta principal`, `KPIs`.
- `Drive`: salvar `Briefing` em `01_Briefing/`.

#### Passo a passo
- Enviar formulário/arquivo de briefing (template).
- Revisar respostas e marcar dúvidas.
- Fazer call curta (30–45 min) para completar lacunas.
- Registrar “restrições” (ex.: não pode falar preço; não pode usar antes/depois).

#### Checklist
- Oferta e diferenciais claros.
- Capacidade de atendimento (horários, equipe, resposta).
- Histórico: campanhas passadas, criativos vencedores/perdedores.

#### Qualidade
- Sem lacunas críticas (ex.: quem atende leads? qual WhatsApp?).

#### Métricas
- % briefings completos no prazo.

#### Automação
- Envio automático do briefing após pagamento.

#### Exceções
- Cliente não preenche: CS agenda call guiada e preenche junto.

---

### P4.3 — Solicitação e validação de acessos (BM, Ads, Pixel, Domínio, Site, WhatsApp)
- **Código/ID**: P4.3
- **Tipo**: **[P] Pipeline de acessos**
- **Objetivo**: obter acessos mínimos com segurança (sem pedir senha) e validar funcionamento.
- **Momento**: onboarding.
- **Gatilho**: briefing iniciado.
- **Saída**: acessos `Concedidos` e `Validados` na DB `Acessos & Governança`.
- **Papéis**: CS (coordena), Gestor de Tráfego (valida Ads/Pixels), (opcional) TI cliente.
- **Ferramentas**: Notion (`Acessos & Governança`), Meta Business Suite, Drive.

#### Registro no FL
- Criar itens em `Acessos & Governança` para: BM, Conta Ads, Página, Pixel, Domínio, GTM/Tag, Hospedagem/LP, WhatsApp, CRM.

#### Passo a passo
- **P4.3-T1 (Obrigatória) Enviar checklist de acessos** (template) com passo a passo.
- **P4.3-T2 (Obrigatória) Criar/atualizar itens de acesso** no Notion (`Status = Solicitado`).
- **P4.3-T3 (Obrigatória) Validar**:
  - Ads Manager abre e permite criar/editar.
  - Pixel aparece no Events Manager.
  - Página/Instagram conectados (se necessário).
- **P4.3-T4 (Obrigatória) Marcar como `Validado`** e registrar o que foi concedido (sem senhas).

#### Checklist
- Permissão correta (Admin/Advertiser conforme necessário).
- Domínio verificado (se aplicável).

#### Qualidade
- Nenhuma ação bloqueada por permissão.

#### Métricas
- Tempo médio para receber acessos; % clientes que atrasam acessos.

#### Automação
- Quando item `Acesso` muda para `Concedido` → criar tarefa de `Validação` para o responsável.

#### Exceções
- Cliente não consegue dar acesso: gravar tutorial curto + envolver TI.
- BM indisponível/conta restrita: abrir incidente P12.2 (bloqueio) e seguir playbook.

---

### P4.4 — Auditoria inicial (conta, pixel, LP, processo de atendimento)
- **Código/ID**: P4.4
- **Tipo**: **[U] Única**
- **Objetivo**: diagnosticar riscos antes do primeiro real investido.
- **Gatilho**: acessos validados.
- **Saída**: relatório curto de auditoria + lista de correções.
- **Papéis**: Gestor de Tráfego (dono), CS.
- **Ferramentas**: Meta Ads, Events Manager, site/LP, Notion.

#### Registro no FL
- Criar `Tarefas` de correção (tracking/LP/conta).
- Registrar decisões em `Decisões` se alterar estrutura.

#### Passo a passo
- Revisar histórico de conta: rejeições, limitações, estrutura.
- Verificar pixel/CAPI e eventos.
- Avaliar LP: velocidade, CTA, formulário, compliance.
- Avaliar atendimento: tempo resposta, script, qualificação.

#### Checklist
- Eventos disparam corretamente (test events).
- Formulário envia para canal certo (Notion/WhatsApp).

#### Qualidade
- Lista de riscos priorizada (P0/P1).

#### Exceções
- Tracking quebrado: seguir P12.6 e travar go-live até mínimo funcionar.

---

### P4.5 — Estruturação inicial (Drive + Notion: dossiê, projetos, tarefas)
- **Código/ID**: P4.5
- **Tipo**: **[U+A] Única + automação**
- **Objetivo**: garantir organização e padrão desde o dia 1.
- **Gatilho**: cliente ganhou.
- **Saída**: pasta Drive + bases Notion vinculadas + templates aplicados.
- **Papéis**: Ops/CS.
- **Ferramentas**: Drive, Notion, Make/Zapier.

#### Passo a passo
- Criar pasta Drive seguindo padrão.
- Criar página `Cliente — Dossiê` (template).
- Criar `Projeto — Onboarding` e tarefas.

#### Automação
- `Cliente criado` → criar pasta Drive e atualizar link no Notion.

---

### P4.6 — Definição de metas e KPIs (operacionais e de negócio)
- **Código/ID**: P4.6
- **Tipo**: **[U] Única**
- **Objetivo**: converter objetivo do cliente em KPIs controláveis.
- **Gatilho**: briefing completo.
- **Saída**: metas documentadas e aprovadas.
- **Papéis**: Gestor de Tráfego, CS, cliente.
- **Ferramentas**: Notion, planilha/BI.

#### KPIs típicos (local services)
- Negócio: agendamentos, comparecimento, vendas.
- Mídia: CPL, CTR, CPM, taxa de conversão LP.
- Operação: tempo até 1º contato, taxa de contato, taxa de qualificação.

#### Exceções
- Cliente quer “garantia de vendas”: documentar que há fase de testes e dependências (atendimento, oferta, sazonalidade).

---

### P4.7 — Aprovação da estratégia inicial (checkpoint)
- **Código/ID**: P4.7
- **Tipo**: **[U] Única**
- **Objetivo**: evitar retrabalho e alinhar expectativas antes de produzir/lançar.
- **Gatilho**: estratégia inicial pronta (P5.7).
- **Saída**: estratégia aprovada (ok para produção/build).
- **Papéis**: Gestor de Tráfego, CS, cliente.
- **Ferramentas**: Notion/Drive.

#### Critérios de aceitação
- Cliente aprova oferta, mensagens sensíveis e direcionamento do funil.

#### Exceções
- Cliente pede mudança grande: registrar em `Decisões` e replanejar prazos.

---

### P4.8 — Checklist de prontidão para lançamento (go-live)
- **Código/ID**: P4.8
- **Tipo**: **[U] Única**
- **Objetivo**: garantir que o “mínimo viável de mensuração e operação” existe.
- **Gatilho**: campanhas prontas para build (P8.1).
- **Saída**: Go/No-go documentado.
- **Papéis**: Gestor de Tráfego (dono), CS.
- **Ferramentas**: Meta Ads, Events Manager, Notion.

#### Checklist (mínimo)
- Pixel/eventos testados.
- UTMs padrão definidos.
- Canal de atendimento pronto + script.
- Lead cai no lugar certo (Notion/CRM/WhatsApp).
- Criativos aprovados (QA + cliente quando aplicável).

#### Exceções
- Se algum item crítico falhar: abrir `Incidente` (P12.6) e travar lançamento.
