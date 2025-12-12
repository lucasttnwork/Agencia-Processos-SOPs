## FL (Notion) — Arquitetura Operacional (Bases, Campos, Status e Templates)

### Objetivo
Definir um **sistema operacional** em Notion que suporte uma agência **full-funnel de Meta Ads** com:
- previsibilidade (checklists + padrões),
- rastreabilidade (dados mínimos por cliente/campanha),
- escala (templates + automações),
- qualidade (QA + logs de decisão),
- governança (acessos, incidentes, compliance).

---

## 1) Princípios de desenho (para não virar “Notion caótico”)
- **Um lugar para cada tipo de dado** (evitar duplicação): cliente, campanha, criativo, tarefa, incidente, financeiro.
- **Tudo que vira trabalho vira item em `Tarefas`**: mensagens e pedidos do cliente viram tarefa/solicitação.
- **Tudo que é “objeto” (cliente/campanha/criativo/LP) vira registro próprio** com ID e status.
- **Tudo que é decisão vira log**: decisões estratégicas importantes são registradas em `Decisões`.
- **Credenciais NUNCA** ficam no Notion: use cofre (ex.: 1Password). No Notion ficam só **links e responsáveis**.

---

## 2) Estrutura de páginas (navegação)
- **00 — Dashboard Founder** (visão geral: vendas, capacidade, saúde de clientes, caixa)
- **01 — Vendas** (pipeline + scripts + follow-up)
- **02 — Operação (Clientes Ativos)** (tarefas, campanhas, criativos, incidentes)
- **03 — Produção (Criativos/LP)** (backlog + aprovações)
- **04 — Financeiro** (faturas, recebimentos, margem)
- **05 — Governança & Compliance** (acessos, LGPD, políticas)
- **06 — Base de Conhecimento (SOPs/Playbooks)**

---

## 3) Bases de dados (DBs) recomendadas (mínimo viável + escalável)

### 3.1 `Clientes`
**Um registro por empresa atendida (ou potencial cliente já qualificado).**
- **Campos obrigatórios**
  - `Cliente (Nome)` (title)
  - `Cliente_ID` (texto; padrão: `CLT-0001`)
  - `Status do Cliente` (select: `Prospect`, `Onboarding`, `Ativo`, `Em risco`, `Pausado`, `Encerrando`, `Encerrado`)
  - `Nicho` (select)
  - `Oferta do Cliente` (texto curto)
  - `Região/Atuação` (texto)
  - `Responsável CS` (person)
  - `Gestor de Tráfego Responsável` (person)
  - `Data Início` (date)
- **Campos recomendáveis**
  - `Plano/Retainer` (select)
  - `SLA combinado` (select)
  - `Canal oficial` (select: WhatsApp, e-mail)
  - `Link Drive (Pasta do cliente)` (url)
  - `Link BM/Conta Ads` (url)
  - `NPS` (number)
  - `Risco de Churn` (select: Baixo/Médio/Alto)

### 3.2 `Contatos`
**Pessoas do cliente (dono, gerente, financeiro).**
- `Contato (Nome)` (title)
- `Cliente` (relation → Clientes)
- `Papel` (select: Dono, Marketing, Comercial, Financeiro, TI, Outro)
- `WhatsApp` (phone/text)
- `E-mail` (email)
- `Preferência de contato` (select)
- `Observações` (text)

### 3.3 `Pipeline (Agência)`
**Leads e oportunidades da sua agência (vendas).**
- `Oportunidade (Nome)` (title; ex.: `Empresa X — Meta Ads`)
- `Lead_ID` (texto; `LEAD-0001`)
- `Etapa` (select: `Novo`, `Contato feito`, `Pré-qualificado`, `Call agendada`, `No-show`, `Call feita`, `Proposta enviada`, `Negociação`, `Ganho`, `Perdido`, `Nutrição`)
- `Origem` (select: Ads, Orgânico, Indicação, Parceria, Evento)
- `Valor estimado (MRR)` (number)
- `Probabilidade` (number %)
- `Próxima ação em` (date)
- `Responsável SDR/Closer` (person)
- `Cliente (se ganhou)` (relation → Clientes)
- `Log de contatos` (relation → Interações)

### 3.4 `Interações (Vendas/CS)`
**Registro de contatos importantes (WhatsApp/e-mail/call).**
- `Interação` (title)
- `Tipo` (select: WhatsApp, E-mail, Call, Reunião)
- `Relacionado a` (relation → Pipeline (Agência) e/ou Clientes)
- `Data` (date)
- `Resumo` (text)
- `Próxima ação` (text)

### 3.5 `Leads (Clientes)`
**Leads recebidos das campanhas (para medir qualidade e funil real).**\n+\n+> Se o cliente já usa CRM externo, esta base pode ser “espelho mínimo” (só para auditoria/qualidade) ou substituída por integração direta.\n+\n+- **Campos obrigatórios**\n+  - `Lead` (title)\n+  - `Cliente` (relation → Clientes)\n+  - `Lead_ID` (texto; ex.: `LD-CLT0007-20251212-001`)\n+  - `Origem` (select: Meta Lead Ads, LP/Form, WhatsApp, Indicação)\n+  - `Etapa` (select: Novo, Contatado, Qualificado, Agendado, Compareceu, Vendeu, Perdeu, Sem resposta)\n+  - `Data entrada` (date)\n+  - `Responsável atendimento` (person)\n+- **Campos recomendáveis (para performance e diagnóstico)**\n+  - `Telefone/WhatsApp` (text)\n+  - `E-mail` (email)\n+  - `Motivo perda` (select)\n+  - `Tempo até 1º contato (min)` (number)\n+  - `UTM source/medium/campaign/content/term` (text)\n+  - `Campaign/Adset/Ad ID` (text)\n+  - `Criativo relacionado` (relation → Criativos)\n+  - `Campanha relacionada` (relation → Campanhas)\n+  - `Qualidade do lead` (select: Baixa/Média/Alta)\n+  - `Observações` (text)\n+\n+### 3.6 `Contratos & Cobranças`
**Controle financeiro por cliente.**
- `Fatura/Contrato` (title)
- `Cliente` (relation → Clientes)
- `Tipo` (select: Contrato, Fatura, Recibo)
- `Competência` (month)
- `Valor` (number)
- `Status` (select: Emitido, Enviado, Pago, Atrasado, Cancelado)
- `Vencimento` (date)
- `Método` (select: PIX, boleto, cartão)
- `Link Documento` (url)
- `Responsável Financeiro` (person)

### 3.7 `Tarefas`
**Tudo que é execução vira tarefa.**
- **Campos obrigatórios**
  - `Tarefa` (title)
  - `Tipo` (select: Vendas, Onboarding, Tráfego, Criativo, LP, CS, Financeiro, Governança, Compliance, QA)
  - `Cliente` (relation → Clientes)
  - `Projeto` (relation → Projetos/Entregas — ver 3.7)
  - `Responsável` (person)
  - `Status` (select: `Backlog`, `A fazer`, `Em andamento`, `Em revisão`, `Aguardando cliente`, `Bloqueado`, `Concluído`)
  - `Prioridade` (select: P0, P1, P2, P3)
  - `Prazo` (date)
- **Campos recomendáveis**
  - `SLA` (select)
  - `Checklist` (checkboxes no corpo da página ou subitens)
  - `Dependências` (relation → Tarefas)
  - `Link referência` (url)
  - `Tempo estimado (h)` / `Tempo gasto (h)` (number)
  - `Processo (SOP)` (relation → SOPs)

### 3.8 `Projetos/Entregas`
**Um “container” por ciclo de trabalho (ex.: Onboarding, Mês 01, Campanha X).**
- `Projeto` (title; ex.: `CLT-0007 — Onboarding`)
- `Cliente` (relation → Clientes)
- `Tipo` (select: Onboarding, Operação Mensal, Campanha, Sprint Criativos, Recuperação, Offboarding)
- `Status` (select: Planejado, Em execução, Em risco, Concluído, Cancelado)
- `Início` / `Fim` (date)
- `Meta principal` (text)

### 3.9 `Campanhas (Meta)`
**Registro operacional (não precisa espelhar 100% do Ads Manager; precisa ser rastreável).**
- `Campanha` (title)
- `Cliente` (relation → Clientes)
- `Campanha_ID` (texto; padrão: `CMP-CLT0007-202512`)
- `Objetivo` (select: Leads, Conversões, Tráfego, Engajamento, Vendas)
- `Estágio do funil` (select: TOFU, MOFU, BOFU, RMK)
- `Oferta/Ângulo` (text)
- `Status` (select: Planejada, Build, Em QA, Ativa, Pausada, Encerrada)
- `Orçamento diário` (number)
- `Data de início` (date)
- `Link Ads Manager` (url)
- `UTM padrão` (text)

### 3.10 `Criativos` (assets + aprovações)
- `Criativo` (title; ex.: `CR-CLT0007-VDO-UGC-001`)
- `Cliente` (relation → Clientes)
- `Tipo` (select: Vídeo, Imagem, Carrossel, Copy, LP Seção)
- `Objetivo` / `Estágio` (select)
- `Status` (select: Ideia, Brief criado, Em produção, QA interno, Enviado p/ cliente, Revisão, Aprovado, Publicado, Arquivado)
- `Hook/Ângulo` (text)
- `Link Drive (arquivo)` (url)
- `Variação` (text)
- `Relacionado à Campanha` (relation → Campanhas)

### 3.11 `LPs (Landing Pages)`
- `LP` (title)
- `Cliente` (relation → Clientes)
- `Status` (select: Planejada, Em produção, QA, Publicada, Iterando, Arquivada)
- `URL` (url)
- `Stack` (select: Webflow, WP, Leadster, Outro)
- `Evento de conversão` (select/text)
- `UTMs` (text)

### 3.12 `Testes & Hipóteses`
**Playbook vivo (o que testamos e aprendemos).**
- `Teste` (title)
- `Cliente` (relation)
- `Hipótese` (text)
- `Variável` (select: Criativo, Público, Oferta, LP, Orçamento, Otimização)
- `Data início` / `Data fim` (date)
- `Critério de decisão` (text)
- `Resultado` (select: Ganhou, Perdeu, Inconclusivo)
- `Aprendizado` (text)
- `Relacionado à Campanha` (relation)

### 3.13 `Incidentes & Crises`
- `Incidente` (title)
- `Cliente` (relation)
- `Tipo` (select: Reprovação, Conta bloqueada, Falha tracking, Queda performance, Cobrança Meta, Leads inválidos, Outro)
- `Severidade` (select: S1, S2, S3)
- `Status` (select: Aberto, Investigando, Mitigado, Resolvido, Pós-mortem)
- `Responsável` (person)
- `Data abertura` (date)
- `Resumo` (text)
- `Impacto` (text)
- `Comunicação ao cliente` (text/link)

### 3.14 `Acessos & Governança` (sem senhas)
- `Acesso` (title; ex.: `BM — Admin`)
- `Cliente` (relation)
- `Tipo` (select: BM, Conta Ads, Página, Pixel, GTM, Domínio, CRM, WhatsApp, Hospedagem, Analytics)
- `Status` (select: Pendente, Solicitado, Concedido, Validado, Revogado)
- `Responsável do lado do cliente` (relation → Contatos)
- `Responsável interno` (person)
- `Link/Local no cofre` (url/text)
- `Data concessão` / `Data revogação` (date)

### 3.15 `SOPs (Processos)`
- `SOP` (title)
- `Código` (text; ex.: `P4.2`)
- `Macroprocesso` (select: P1…P17)
- `Tipo` (select: Único, Recorrente, Pipeline, Automação)
- `Objetivo` (text)
- `Entrada/Saída` (text)
- `Checklist padrão` (text)
- `Link doc` (url ou conteúdo na página)

### 3.16 `Decisões (Log)`
- `Decisão` (title)
- `Cliente` (relation)
- `Categoria` (select: Oferta, Público, Criativo, LP, Orçamento, Operação)
- `Contexto` (text)
- `Decisão tomada` (text)
- `Data` (date)
- `Responsáveis` (people)
- `Impacto esperado` (text)

### 3.17 `Relatórios`
- `Relatório` (title)
- `Cliente` (relation → Clientes)
- `Período` (select: Semanal, Quinzenal, Mensal)
- `Competência` (month)
- `Status` (select: Em produção, Em QA, Enviado, Aguardando feedback)
- `Link (Sheet/BI/Slides)` (url)
- `Resumo executivo` (text)

### 3.18 `Reuniões`
- `Reunião` (title)
- `Cliente` (relation → Clientes)
- `Tipo` (select: Onboarding, Alinhamento, Revisão Mensal, Crise, Renovação)
- `Data/Hora` (date)
- `Participantes` (people/text)
- `Pauta` (text)
- `Decisões` (relation → Decisões)
- `Próximos passos` (relation → Tarefas)

---

## 4) Views (visões) essenciais
- **Operação Hoje** (`Tarefas` filtrado por `Prazo = hoje` e `Status != Concluído`)
- **Bloqueios** (`Status = Bloqueado`)
- **Aguardando Cliente** (`Status = Aguardando cliente`)
- **Fila de QA** (`Status = Em revisão` + `Tipo in (Criativo, Tráfego, LP)`)
- **Pipeline Vendas** (kanban por `Etapa` em `Pipeline (Agência)`)
- **Leads (Clientes) — entrada do dia** (`Leads (Clientes)` com `Data entrada = hoje`)
- **Clientes em risco** (`Clientes` com `Risco de Churn = Alto`)
- **Criativos — Produção** (kanban por `Status`)
- **Incidentes abertos** (`Incidentes` com `Status != Resolvido`)
- **Relatórios pendentes** (`Relatórios` com `Status != Enviado`)
- **Reuniões da semana** (`Reuniões` com `Data/Hora` dentro da semana atual)
- **Financeiro — A receber** (`Contratos & Cobranças` com `Status in (Emitido, Enviado, Atrasado)`)

---

## 5) Templates (modelos) obrigatórios

### 5.1 Template: `Cliente — Dossiê`
Página do cliente com seções fixas:
- Contexto do negócio (oferta, público, região)
- Meta principal e KPIs
- Acessos (lista vinculada à DB `Acessos & Governança`)
- Funil atual (LP/CRM/WhatsApp)
- Regras da marca (tom, palavras proibidas, claims)
- Histórico de decisões (view de `Decisões`)

### 5.2 Template: `Projeto — Onboarding`
- Checklist de onboarding (tarefas pré-criadas)
- Links: Drive, BM, pixel, CRM
- SLA e combinados de comunicação

### 5.3 Template: `Campanha — Build + QA`
- Objetivo, funil, oferta
- Lista de criativos relacionados
- Checklist pré-publicação (pixel, UTMs, links, políticas)
- Plano de testes (o que medir e quando decidir)

### 5.4 Template: `Criativo — Brief`
- Formato + placement
- Hook/ângulo
- Prova/objeção
- Instrução de gravação/arte
- CTA
- Checklist de compliance (políticas + claims)

### 5.5 Template: `Incidente — Resposta`
- Linha do tempo (o que ocorreu / quando)
- Hipóteses
- Ações imediatas
- Comunicação ao cliente (texto pronto)
- Pós-mortem (aprendizados + prevenção)

### 5.6 Template: `Relatório — Padrão`
- Resumo executivo (o que melhorou/piorou e por quê)
- KPIs do período (com metas)
- O que foi testado (hipóteses e resultados)
- Próximas ações (tarefas criadas)
- Riscos/alertas (se houver)

### 5.7 Template: `Reunião — Pauta + Ata`
- Pauta padrão (status geral, KPIs, bloqueios, próximos passos)
- Decisões tomadas (link para `Decisões`)
- Próximos passos (link para `Tarefas`)
- Itens pendentes do cliente

---

## 6) Padrões de nomeação (Notion + Drive)

### 6.1 IDs
- Cliente: `CLT-0001`
- Projeto: `PRJ-CLT0001-ONB-202512`
- Campanha: `CMP-CLT0001-LEADS-TOFU-202512`
- Criativo: `CR-CLT0001-VDO-UGC-001`
- LP: `LP-CLT0001-OFERTA-001`

### 6.2 Drive (pasta por cliente)
`Clientes/CLT-0001_NomeCliente/`
- `00_Admin` (contrato, faturas, NDAs)
- `01_Briefing`
- `02_Estrategia`
- `03_Criativos/` (subpastas: `Fonte`, `Aprovados`, `Exports`)
- `04_LandingPages`
- `05_Tracking_UTM`
- `06_Relatorios`
- `07_Incidentes`
- `99_Arquivo`

---

## 7) Campos mínimos para dashboards (BI)
Para BI/Looker/Sheets, garantir que estes campos existam e sejam preenchidos:
- `Cliente_ID`, `Nicho`, `Plano`, `Status do Cliente`
- `Campanha_ID`, `Objetivo`, `Estágio do funil`, `Status`, `Orçamento`, `Data início`
- `Criativo_ID`, `Tipo`, `Status`, `Relacionado à Campanha`
- `Teste_ID` (ou título único), `Variável`, `Resultado`, `Aprendizado`
- `Fatura`: `Valor`, `Status`, `Vencimento`, `Pago em`

---

## 8) Integrações (Make/Zapier) — princípios
- **Entrada (captação)**: Lead (Meta Lead Ads / formulário / WhatsApp) → cria item em `Pipeline (Agência)` ou em `Leads do Cliente` (se for lead de campanha).
- **Orquestração**: Mudou `Etapa/Status` → cria tarefas padrão / notifica responsável.
- **Saída (reporting)**: atualizar `Relatórios`, registrar aprendizados em `Testes & Hipóteses`.

> As automações específicas (gatilho → ação) ficam detalhadas em `04_AUTOMACOES_MAKE_ZAPIER.md`.
