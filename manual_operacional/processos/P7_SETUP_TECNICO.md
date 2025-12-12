## P7 — Setup Técnico (Pixel/CAPI, UTMs, CRM/WhatsApp, Eventos)

> **Objetivo do macroprocesso (P7)**: garantir que toda a infraestrutura técnica de mensuração, rastreamento e integração esteja funcionando antes do primeiro real investido — sem tracking correto, não há otimização possível.

---

### P7.1 — Pixel + CAPI (instalação, validação, troubleshooting)
- **Código/ID**: P7.1
- **Tipo**: **[U] Única** (por cliente) + **[R]** validação periódica
- **Objetivo**: instalar e validar o Meta Pixel + Conversions API para mensuração confiável.
- **Momento**: onboarding, antes de qualquer campanha.
- **Gatilho**: acessos validados (P4.3) + LP/site disponível.
- **Saída esperada**:
  - Pixel instalado e disparando eventos corretamente.
  - CAPI configurada (se aplicável).
  - Registro em `Acessos & Governança` com status `Validado`.
- **Papéis envolvidos**: Gestor de Tráfego (dono), Dev/TI cliente (se necessário).
- **Ferramentas**: Events Manager, GTM (se usado), Notion, documentação técnica.

#### Registro no FL (dados mínimos)
- `Acessos & Governança`: item `Pixel` com `Status = Validado`, `Data concessão`.
- `Decisões`: registrar se foi usado Pixel nativo, GTM ou CAPI.

#### Passo a passo
- **P7.1-T1 (Obrigatória) Verificar se já existe Pixel**
  - Acessar Events Manager do cliente.
  - Verificar se há Pixel associado ao domínio.
  - Se não existir, criar novo Pixel na BM do cliente.
- **P7.1-T2 (Obrigatória) Instalar Pixel no site/LP**
  - **Opção A (direto)**: código base no `<head>` de todas as páginas.
  - **Opção B (GTM)**: criar tag do Pixel no Google Tag Manager.
  - **Opção C (plataforma)**: usar integração nativa (WordPress, Webflow, etc.).
- **P7.1-T3 (Recomendável) Configurar Conversions API (CAPI)**
  - Usar parceiro de integração (Zapier, Make, Stape) ou setup manual.
  - Garantir deduplicação com `event_id`.
- **P7.1-T4 (Obrigatória) Testar eventos**
  - Usar "Test Events" no Events Manager.
  - Verificar: `PageView`, `Lead`, `Purchase`, etc.
  - Confirmar que dados extras (nome, email, telefone) estão sendo enviados (para match rate).
- **P7.1-T5 (Obrigatória) Documentar e validar**
  - Registrar no Notion (`Acessos & Governança`).
  - Atualizar dossiê do cliente.

#### Checklist operacional
- Pixel ID correto associado à conta de anúncios.
- Código instalado em todas as páginas relevantes.
- Eventos de conversão disparando (verificar em tempo real).
- Match rate acima de 50% (idealmente 80%+).
- Deduplicação ativa (se CAPI).

#### Critérios de qualidade / aceitação
- Eventos aparecem em "Test Events" sem erros.
- Match rate visível no Events Manager.
- Nenhum aviso de "Pixel não encontrado" ou "Evento ausente".

#### Métricas relacionadas
- Match rate (%), eventos recebidos/dia, qualidade do evento (EM, Events Manager).

#### Oportunidades de automação (Python)
- **Gatilho**: cliente em onboarding + acessos concedidos.
- **Ação**: enviar checklist técnico + criar tarefa "Validar Pixel".
- **Futuro**: script de verificação automática de eventos via Meta API.

#### Templates/padrões associados
- Checklist de instalação de Pixel (passo a passo visual).
- Template de troubleshooting (erros comuns + soluções).

#### Fluxos de exceção
- **Pixel não dispara**: verificar se código está no `<head>`, se há bloqueadores, se domínio está correto.
- **Match rate baixo**: verificar se dados de lead (email/telefone) estão sendo enviados.
- **Cliente não tem acesso ao site**: solicitar acesso ao dev/hospedagem ou gravar tutorial.

---

### P7.2 — Eventos e conversões (padrão + personalizados)
- **Código/ID**: P7.2
- **Tipo**: **[U] Única**
- **Objetivo**: configurar eventos de conversão alinhados ao objetivo do cliente.
- **Momento**: junto com P7.1.
- **Gatilho**: Pixel instalado.
- **Saída**: eventos configurados e validados no Events Manager.
- **Papéis**: Gestor de Tráfego.
- **Ferramentas**: Events Manager, GTM, LP builder.

#### Registro no FL
- Documentar em `02_Estrategia/Tracking.md` (Drive) os eventos usados.

#### Passo a passo
- **P7.2-T1 (Obrigatória) Mapear conversões do cliente**
  - Qual é a conversão principal? (Lead, Agendamento, Venda)
  - Quais micro-conversões são úteis? (ViewContent, InitiateCheckout)
- **P7.2-T2 (Obrigatória) Configurar eventos padrão**
  - `Lead`: formulário enviado.
  - `Schedule`: agendamento confirmado.
  - `Purchase`: venda concluída (se aplicável).
- **P7.2-T3 (Opcional) Criar eventos personalizados**
  - Ex.: `LeadQualificado`, `AgendamentoConfirmado`, `NoShow`.
  - Usar convenção de nomenclatura: `[Cliente]_[Evento]`.
- **P7.2-T4 (Obrigatória) Testar no Events Manager**
  - Simular conversão e verificar em tempo real.
- **P7.2-T5 (Obrigatória) Configurar conversão personalizada (se necessário)**
  - No Ads Manager, criar "Custom Conversion" baseada em URL ou evento.

#### Checklist
- Evento principal de conversão configurado.
- Evento aparece em "Eventos" no Ads Manager.
- Conversão personalizada criada (se aplicável).

#### Exceções
- **LP não permite eventos personalizados**: usar evento padrão `Lead` + filtrar por UTM.

---

### P7.3 — Domínio + AEM + permissões (se aplicável)
- **Código/ID**: P7.3
- **Tipo**: **[U] Única**
- **Objetivo**: verificar e preparar domínio para tracking e agregação de eventos.
- **Momento**: onboarding.
- **Gatilho**: Pixel configurado.
- **Saída**: domínio verificado + AEM configurado (se iOS 14.5+).
- **Papéis**: Gestor de Tráfego, Dev/TI cliente.
- **Ferramentas**: Events Manager, BM, DNS do cliente.

#### Passo a passo
- **P7.3-T1 (Obrigatória) Verificar domínio na BM**
  - Adicionar registro DNS TXT ou upload de arquivo HTML.
- **P7.3-T2 (Obrigatória) Configurar Aggregated Event Measurement (AEM)**
  - Priorizar até 8 eventos por domínio.
  - Definir ordem de prioridade (ex.: Purchase > Lead > ViewContent).
- **P7.3-T3 (Obrigatória) Validar permissões**
  - Garantir que BM tem controle do domínio.

#### Checklist
- Domínio verificado (badge verde no BM).
- AEM configurado com eventos priorizados.

#### Exceções
- **Cliente usa domínio compartilhado (ex.: landing page builder)**: verificar limitações e alternativas.

---

### P7.4 — UTMs + padrão de links + rastreio
- **Código/ID**: P7.4
- **Tipo**: **[U] Única** + **[R]** manutenção
- **Objetivo**: padronizar rastreamento de origem para atribuição e análise.
- **Momento**: antes do primeiro anúncio.
- **Gatilho**: estratégia definida (P5).
- **Saída**: padrão de UTMs documentado + links prontos.
- **Papéis**: Gestor de Tráfego.
- **Ferramentas**: Google Sheets (ou gerador de UTM), Notion.

#### Registro no FL
- Criar documento `05_Tracking_UTM/Padrão_UTMs.md` no Drive do cliente.
- Registrar padrão no dossiê do cliente.

#### Passo a passo
- **P7.4-T1 (Obrigatória) Definir padrão de nomenclatura**
  ```
  utm_source=meta
  utm_medium=cpc|cpm|social
  utm_campaign=[objetivo]_[funil]_[yyyymm]
  utm_content=[criativo_id]
  utm_term=[publico_id]
  ```
- **P7.4-T2 (Obrigatória) Criar planilha de UTMs**
  - Modelo com colunas: campanha, conjunto, anúncio, URL final.
- **P7.4-T3 (Obrigatória) Testar links**
  - Verificar se parâmetros aparecem na URL de destino.
  - Confirmar que Analytics/CRM captura UTMs.
- **P7.4-T4 (Recorrente) Manter consistência**
  - Revisar a cada nova campanha.

#### Checklist
- Padrão documentado e compartilhado com equipe.
- Todos os anúncios têm UTMs.
- CRM/Notion captura UTMs dos leads.

#### Métricas
- Leads por source/medium/campaign, atribuição correta.

#### Exceções
- **LP não captura UTMs**: configurar hidden fields no formulário.

---

### P7.5 — Integração Leads → WhatsApp/Notion + roteamento
- **Código/ID**: P7.5
- **Tipo**: **[U+A] Única + automação**
- **Objetivo**: garantir que leads cheguem instantaneamente ao atendimento e sejam registrados.
- **Momento**: onboarding, antes de campanhas.
- **Gatilho**: LP/formulário configurado.
- **Saída**: fluxo testado (lead → notificação → registro).
- **Papéis**: Gestor de Tráfego, Ops, Dev (automações Python).
- **Ferramentas**: Meta Lead Ads, Webhooks, Python (automações próprias), Notion API, WhatsApp API.

#### Registro no FL
- Documentar fluxo em `05_Tracking_UTM/Integracao_Leads.md`.
- Criar item em `Acessos & Governança` para `Integração Leads`.

#### Passo a passo
- **P7.5-T1 (Obrigatória) Mapear fluxo de leads**
  - Lead Ads → Webhook → Python → Notion + WhatsApp.
  - LP Form → Webhook → Python → Notion + WhatsApp.
- **P7.5-T2 (Obrigatória) Configurar webhook/integração**
  - Usar sistema de automações Python próprio.
  - Campos mínimos: nome, telefone, email, UTMs, timestamp.
- **P7.5-T3 (Obrigatória) Configurar notificação**
  - WhatsApp (via API Business): mensagem automática para responsável.
  - Fallback: e-mail.
- **P7.5-T4 (Obrigatória) Testar end-to-end**
  - Enviar lead teste.
  - Verificar: chegou no Notion? Notificação enviada? Tempo < 1 min?
- **P7.5-T5 (Obrigatória) Documentar e monitorar**
  - Criar alerta para falhas de integração.

#### Checklist
- Lead teste chega em < 1 minuto.
- Campos mapeados corretamente.
- Notificação funciona.

#### Automação Python (prioridade A01)
```python
# Fluxo básico
# 1. Webhook recebe lead (Meta Lead Ads ou formulário)
# 2. Script Python processa e enriquece dados
# 3. Cria item no Notion (DB Leads do Cliente)
# 4. Envia notificação WhatsApp para responsável
# 5. Loga resultado para monitoramento
```

#### Exceções
- **Integração falha**: alertar imediatamente (fallback: email) + abrir incidente.
- **Cliente usa CRM externo**: integrar Python → CRM (via API).

---

### P7.6 — Públicos (custom/lookalike/interesses) + janelas RMK
- **Código/ID**: P7.6
- **Tipo**: **[U] Única** + **[R]** atualização
- **Objetivo**: criar base de públicos para campanhas (cold + warm + hot).
- **Momento**: após Pixel validado.
- **Gatilho**: Pixel com dados / listas de clientes.
- **Saída**: públicos criados no Ads Manager.
- **Papéis**: Gestor de Tráfego.
- **Ferramentas**: Ads Manager, Notion.

#### Registro no FL
- Documentar públicos em `02_Estrategia/Publicos.md`.

#### Passo a passo
- **P7.6-T1 (Obrigatória) Criar públicos de remarketing**
  - Visitantes do site (7d, 30d, 90d).
  - Engajamento IG/FB (30d, 90d).
  - Video viewers (25%, 50%, 75%).
  - Leads que não converteram.
- **P7.6-T2 (Obrigatória) Criar públicos lookalike**
  - LAL de clientes/compradores (1%, 2%, 5%).
  - LAL de leads qualificados.
- **P7.6-T3 (Opcional) Públicos de interesse**
  - Mapear interesses relevantes para o nicho.
- **P7.6-T4 (Obrigatória) Documentar**
  - Nome padronizado: `[Cliente]_[Tipo]_[Janela]_[Data]`.

#### Checklist
- Pelo menos 3 públicos de RMK criados.
- Pelo menos 1 LAL criado (se houver dados).
- Nomeação padronizada.

#### Métricas
- Tamanho dos públicos, CPL por público.

---

### P7.7 — Checklist técnico pré-lançamento
- **Código/ID**: P7.7
- **Tipo**: **[U] Única** (por campanha/cliente)
- **Objetivo**: garantir que tudo está pronto antes de gastar.
- **Momento**: após build de campanhas (P8.1), antes de publicar.
- **Gatilho**: campanhas prontas para review.
- **Saída**: go/no-go documentado.
- **Papéis**: Gestor de Tráfego (executor), CS (validador).
- **Ferramentas**: Notion (checklist), Ads Manager, Events Manager.

#### Checklist pré-lançamento (mínimo)

**Tracking**
- [ ] Pixel instalado e eventos testados
- [ ] CAPI configurada (se aplicável)
- [ ] UTMs definidos e testados
- [ ] Integração leads funcionando (teste enviado)

**Campanhas**
- [ ] Nomenclatura padronizada
- [ ] Orçamento correto (diário/lifetime)
- [ ] Agendamento correto (início/fim)
- [ ] Objetivo de otimização correto

**Anúncios**
- [ ] Criativos aprovados (QA interno)
- [ ] Copys revisadas (ortografia, políticas)
- [ ] Links corretos (UTMs inclusos)
- [ ] Preview verificado (mobile/desktop)

**Destino**
- [ ] LP funcionando (velocidade, mobile)
- [ ] Formulário testado
- [ ] Pixel dispara na LP
- [ ] Thank you page configurada

**Atendimento**
- [ ] Script de atendimento pronto
- [ ] Responsável definido
- [ ] Notificação de leads funcionando

#### Qualidade
- Todos os itens marcados = GO.
- Qualquer item crítico faltando = NO-GO + tarefa de correção.

---

### P7.8 — Auditoria técnica periódica (pixel/UTM/qualidade de dados)
- **Código/ID**: P7.8
- **Tipo**: **[R] Recorrente** (mensal)
- **Objetivo**: identificar e corrigir degradações de tracking.
- **Momento**: primeira semana do mês.
- **Gatilho**: calendário (recorrente).
- **Saída**: relatório de auditoria + tarefas de correção.
- **Papéis**: Gestor de Tráfego.
- **Ferramentas**: Events Manager, Ads Manager, Notion.

#### Passo a passo
- **P7.8-T1 (Obrigatória) Verificar saúde do Pixel**
  - Eventos recebidos nas últimas 24h.
  - Match rate atual.
  - Avisos/erros no Events Manager.
- **P7.8-T2 (Obrigatória) Verificar UTMs**
  - Leads estão chegando com UTMs preenchidos?
  - Atribuição está correta?
- **P7.8-T3 (Obrigatória) Verificar integração de leads**
  - Teste de lead (end-to-end).
  - Tempo de chegada.
- **P7.8-T4 (Obrigatória) Documentar e corrigir**
  - Criar tarefas para itens fora do padrão.
  - Registrar em `Decisões` se houver mudança estrutural.

#### Checklist de auditoria
- [ ] Pixel ativo e recebendo eventos
- [ ] Match rate > 50%
- [ ] UTMs sendo capturados
- [ ] Integração de leads funcionando
- [ ] Públicos de RMK com dados recentes

#### Métricas
- Match rate (%), leads com UTM (%), eventos/dia.

#### Automação Python (futuro)
- Script que verifica automaticamente saúde do Pixel via Meta API.
- Alerta se match rate cair abaixo do threshold.
