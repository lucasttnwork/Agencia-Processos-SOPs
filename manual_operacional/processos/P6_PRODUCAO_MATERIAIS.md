## P6 — Produção de Materiais (Copy, Criativos, LP, Scripts)

> **Objetivo do macroprocesso (P6)**: transformar a estratégia (P5) em materiais prontos para campanha com volume, qualidade, consistência e rastreio (versões, aprovações e uso em campanhas).

---

### P6.1 — Intake de demandas (novo cliente, refresh, teste específico)
- **Código/ID**: P6.1
- **Tipo**: **[P+A] Pipeline + automação**
- **Objetivo**: toda demanda virar tarefa/brief claro (sem pedido “solto no WhatsApp”).
- **Momento**: contínuo (operação).
- **Gatilho**: nova demanda interna (P5) ou pedido do cliente.
- **Saída**: itens criados/atualizados em `Criativos` e `Tarefas` com prazo e responsável.
- **Papéis**: CS (triagem), Gestor de Tráfego (prioriza), Copywriter/Designer.
- **Ferramentas**: Notion (`Tarefas`, `Criativos`, `Campanhas`), Drive.

#### Registro no FL
- `Tarefas`: `Tipo = Criativo/Copy/LP`, `Prioridade`, `Prazo`, `Projeto`.
- `Criativos`: criar item com `Status = Ideia` ou `Brief criado`.

#### Passo a passo
- **P6.1-T1 (Obrigatória) Padronizar pedido**: objetivo, funil, oferta, ângulo, formato, deadline.
- **P6.1-T2 (Obrigatória) Criar item em `Criativos`** (ID + link Drive).
- **P6.1-T3 (Obrigatória) Criar tarefas** para produção + QA + aprovação.
- **P6.1-T4 (Obrigatória) Priorizar** (P0/P1) com base em impacto e urgência.

#### Checklist
- Brief contém: persona, dor, promessa segura, prova, CTA.

#### Critérios de qualidade
- Nenhuma produção iniciada sem brief aprovado internamente.

#### Métricas
- Lead time (pedido→entrega), taxa de retrabalho, volume de criativos/mês.

#### Automação
- Pedido marcado como `Aprovado para produção` → criar tarefas padrão (copy/design/QA).

#### Exceções
- Pedido urgente sem briefing: abrir exceção com risco explícito (pode gerar retrabalho).

---

### P6.2 — Roteiros de vídeo (UGC, reels, VSL curta)
- **Código/ID**: P6.2
- **Tipo**: **[P] Pipeline**
- **Objetivo**: produzir roteiros com hook forte, clareza e CTA.
- **Gatilho**: demanda em P6.1.
- **Saída**: roteiro final + instruções de gravação/edição.
- **Papéis**: Copywriter/Roteirista, Gestor de Tráfego (revisor), (opcional) editor.
- **Ferramentas**: Notion (`Criativos`), Drive.

#### Passo a passo
- Criar 3 variações de hook (0–3s).
- Desenvolver estrutura: Hook → Problema → Solução → Prova → Oferta → CTA.
- Incluir instruções: cenários, b-roll, texto na tela, duração, entonação.
- QA interno: políticas/claims.
- Enviar para aprovação (interno/cliente).

#### Checklist
- Hook nos 2–3 primeiros segundos.
- CTA explícito (o que fazer agora).
- Sem promessas absolutas/irrealistas.

#### Qualidade
- Linguagem do público (P5.2) + alinhado com oferta.

#### Métricas
- Thumbstop/Hook rate, retenção de vídeo, CTR.

#### Automação
- Criativo `Status = Brief criado` + `Tipo = Vídeo` → tarefa “Escrever roteiro” atribuída.

#### Exceções
- Cliente exige “antes/depois” proibido: registrar e adaptar para prova segura.

---

### P6.3 — Criativos estáticos (imagens, carrosséis)
- **Código/ID**: P6.3
- **Tipo**: **[P] Pipeline**
- **Objetivo**: produzir peças com clareza (mensagem/benefício) e forte legibilidade mobile.
- **Saída**: exports (1:1, 4:5, 9:16) + variações.
- **Papéis**: Designer, Copy (headline), Gestor de Tráfego (QA).
- **Ferramentas**: Figma/Canva (ou fornecedor), Drive, Notion.

#### Checklist
- Texto legível no mobile.
- Branding consistente (cores/fonte).
- Prova (ex.: depoimento curto) quando aplicável.

#### Qualidade
- Arquivos organizados e nomeados (ID do criativo).

#### Métricas
- CTR, CPC, frequência/fadiga.

---

### P6.4 — Copys de anúncios (título, primário, descrição, CTA)
- **Código/ID**: P6.4
- **Tipo**: **[P] Pipeline**
- **Objetivo**: escrever variações testáveis por ângulo e funil.
- **Saída**: 3–5 variações por ângulo, prontas para Ads Manager.
- **Papéis**: Copywriter, Gestor de Tráfego (QA).
- **Ferramentas**: Notion/Drive.

#### Checklist de copy (Meta)
- Benefício claro, CTA direto.
- Evitar linguagem proibida (atributos pessoais, promessas sensíveis).
- Clareza > criatividade.

#### Métricas
- CTR, CPC, taxa de conversão.

---

### P6.5 — Landing pages (estrutura + copy + QA)
- **Código/ID**: P6.5
- **Tipo**: **[P] Pipeline**
- **Objetivo**: criar/ajustar LP para converter e qualificar lead (sem fricção).
- **Saída**: LP publicada + tracking validado.
- **Papéis**: Copywriter, Designer/Web, Gestor de Tráfego (tracking/QA), CS.
- **Ferramentas**: Webflow/WP/Lead pages, Drive, Notion (`LPs`).

#### Seções mínimas (serviços locais)
- Headline (benefício) + subheadline (prova)
- Oferta (o que recebe) + urgência/escassez real
- Provas (reviews, cases, credenciais)
- Como funciona (passo a passo)
- FAQ (objeções)
- CTA repetido + formulário simples

#### Checklist
- Página rápida (mobile), CTA acima da dobra.
- Formulário envia para canal certo.
- Pixel/eventos/UTMs ok.

#### Métricas
- CVR LP, CPL, taxa de qualificação.

---

### P6.6 — Scripts de atendimento (WhatsApp) + atualizações
- **Código/ID**: P6.6
- **Tipo**: **[U+R] Criar + atualizar**
- **Objetivo**: aumentar conversão lead→agendamento→venda via processo de atendimento.
- **Saída**: scripts prontos + playbook de qualificação.
- **Papéis**: CS, Copywriter, cliente (time comercial).
- **Ferramentas**: WhatsApp Business, Drive/Notion.

#### Conteúdos mínimos
- Mensagem inicial (resposta rápida)
- Qualificação (3–6 perguntas)
- Agendamento (link + confirmação)
- Reativação (sem resposta)
- Pós-atendimento (follow-up)

#### Métricas
- tempo 1º contato, taxa de contato, taxa de agendamento, taxa de venda.

---

### P6.7 — QA interno (políticas, ortografia, clareza, promessa)
- **Código/ID**: P6.7
- **Tipo**: **[P] Pipeline**
- **Objetivo**: reduzir reprovações, evitar risco de conta e garantir padrão.
- **Saída**: material “aprovado internamente”.
- **Papéis**: Revisor (Gestor/CS), Copy/Designer.

#### Checklist QA (mínimo)
- Políticas Meta (atributos pessoais, saúde/finanças, antes/depois, claims absolutos)
- Ortografia e clareza
- CTA e oferta coerentes
- Adequação a público e funil

---

### P6.8 — Aprovação com cliente (envio, revisão, versão final)
- **Código/ID**: P6.8
- **Tipo**: **[P] Pipeline**
- **Objetivo**: aprovar sem travar a operação (SLA de aprovação + limite de revisões).
- **Saída**: criativo aprovado e pronto para publicação.
- **Papéis**: CS (coordena), cliente.

#### Exceções
- Cliente demora aprovação: mover tarefa para `Aguardando cliente` e registrar impacto no prazo.

---

### P6.9 — Backlog contínuo de ideias e testes criativos
- **Código/ID**: P6.9
- **Tipo**: **[R] Recorrente**
- **Objetivo**: nunca depender de “criar do zero” sob pressão.
- **Saída**: backlog priorizado para 2–4 semanas.
- **Papéis**: Gestor de Tráfego, Copy/Designer.

#### Passo a passo
- Semanal: adicionar 10 novas ideias (concorrência, comentários, performance).
- Priorizar por impacto e facilidade.
- Transformar top ideias em briefs (P6.1).

---

### P6.10 — Gestão de versões e arquivamento (Drive + IDs)
- **Código/ID**: P6.10
- **Tipo**: **[R] Recorrente**
- **Objetivo**: rastrear o que foi usado, aprovado e performou.
- **Saída**: Drive organizado + Notion atualizado (`Status = Publicado`).
- **Papéis**: Ops/Designer.

#### Checklist
- Arquivo final salvo em `03_Criativos/Aprovados`.
- Nome do arquivo contém `ID` do criativo.
- Link Drive preenchido no Notion.
