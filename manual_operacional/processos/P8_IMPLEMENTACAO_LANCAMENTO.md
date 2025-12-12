## P8 — Implementação & Lançamento (Build + QA + Publicação)

> **Objetivo do macroprocesso (P8)**: transformar estratégia e materiais aprovados em campanhas publicadas, com qualidade garantida e monitoramento inicial para detectar problemas rapidamente.

---

### P8.1 — Build de campanhas (estrutura, nomenclatura, configurações)
- **Código/ID**: P8.1
- **Tipo**: **[U] Única** (por campanha/cliente)
- **Objetivo**: criar campanhas no Ads Manager seguindo estrutura e padrões definidos.
- **Momento**: após aprovação de estratégia (P4.7) e materiais prontos (P6).
- **Gatilho**: criativos aprovados + tracking validado (P7).
- **Saída esperada**:
  - Campanhas criadas no Ads Manager (status: rascunho ou pausado).
  - Registro em `Campanhas (Meta)` no Notion.
- **Papéis envolvidos**: Gestor de Tráfego (executor).
- **Ferramentas**: Meta Ads Manager, Notion, Drive.

#### Registro no FL (dados mínimos)
- `Campanhas (Meta)`: criar item com `Status = Build`, `Campanha_ID`, `Objetivo`, `Estágio do funil`.
- `Tarefas`: criar tarefas de QA vinculadas.

#### Passo a passo
- **P8.1-T1 (Obrigatória) Acessar conta de anúncios**
  - Verificar se está na conta correta (cliente).
  - Confirmar forma de pagamento ativa.
- **P8.1-T2 (Obrigatória) Criar estrutura de campanha**
  - Usar padrão de nomenclatura:
    ```
    Campanha: [CLT]_[Objetivo]_[Funil]_[YYYYMM]
    Conjunto: [CLT]_[Publico]_[Placement]
    Anúncio: [CLT]_[Criativo-ID]_[Variação]
    ```
  - Exemplo: `CLT0007_LEADS_TOFU_202512`
- **P8.1-T3 (Obrigatória) Configurar campanha**
  - Objetivo: Leads, Conversões, Tráfego, etc.
  - Orçamento: ABO ou CBO conforme estratégia.
  - Otimização: conversão, cliques em link, etc.
  - Agendamento: início e fim (se aplicável).
- **P8.1-T4 (Obrigatória) Configurar conjuntos de anúncios**
  - Público: segmentação definida em P7.6.
  - Posicionamentos: automáticos ou manuais.
  - Orçamento do conjunto (se ABO).
  - Agendamento de veiculação (horários, se aplicável).
- **P8.1-T5 (Obrigatória) Criar anúncios**
  - Upload de criativos (imagem/vídeo).
  - Copys (título, texto principal, descrição, CTA).
  - URL de destino com UTMs.
  - Preview: mobile e desktop.
- **P8.1-T6 (Obrigatória) Registrar no Notion**
  - Atualizar `Campanhas (Meta)` com `Status = Build`.
  - Linkar criativos relacionados.

#### Checklist de build
- [ ] Conta correta selecionada
- [ ] Nomenclatura padronizada aplicada
- [ ] Objetivo de campanha correto
- [ ] Orçamento definido (diário/lifetime)
- [ ] Público configurado corretamente
- [ ] Criativos carregados
- [ ] Copys inseridas
- [ ] URLs com UTMs
- [ ] Preview verificado

#### Critérios de qualidade
- Estrutura espelha o planejado em P5.
- Todos os campos obrigatórios preenchidos.
- Sem erros ou avisos no Ads Manager.

#### Métricas relacionadas
- Tempo de build, quantidade de campanhas/mês.

#### Exceções
- **Erro de criação**: verificar permissões, limites de conta, problemas de pagamento.
- **Criativo muito pesado**: comprimir ou reencodar.

---

### P8.2 — Fluxos por tipo (Lead Ads, LP, RMK, retomada)
- **Código/ID**: P8.2
- **Tipo**: **[U] Única**
- **Objetivo**: aplicar configurações específicas para cada tipo de campanha.
- **Momento**: durante build (P8.1).
- **Gatilho**: estratégia define tipo de campanha.
- **Saída**: campanha configurada conforme tipo.
- **Papéis**: Gestor de Tráfego.

#### Fluxo A: Lead Ads (formulário nativo do Meta)
- **Configuração específica**:
  - Criar formulário instantâneo (Lead Form).
  - Campos: nome, telefone, email (mínimo).
  - Perguntas de qualificação (opcional).
  - Política de privacidade (obrigatório).
  - Thank you screen com instruções.
- **Integração**: webhook configurado em P7.5.
- **Checklist adicional**:
  - [ ] Formulário criado e vinculado
  - [ ] Campos mapeados para integração
  - [ ] Mensagem de confirmação configurada

#### Fluxo B: Conversão em LP
- **Configuração específica**:
  - URL de destino = LP com formulário.
  - Evento de conversão = `Lead` ou custom.
  - Pixel configurado (P7.1).
- **Checklist adicional**:
  - [ ] LP carrega rápido (< 3s)
  - [ ] Formulário funciona no mobile
  - [ ] Evento de conversão dispara

#### Fluxo C: Remarketing (RMK)
- **Configuração específica**:
  - Público = custom audience (visitantes, engajadores, leads).
  - Exclusões: compradores (se aplicável).
  - Mensagem diferente (reconhecimento de retorno).
- **Checklist adicional**:
  - [ ] Público de RMK com tamanho suficiente (> 1.000)
  - [ ] Exclusões configuradas
  - [ ] Criativo específico para RMK

#### Fluxo D: Campanhas de retomada (leads frios)
- **Configuração específica**:
  - Público = leads que não converteram / não responderam.
  - Mensagem de "segunda chance" ou nova oferta.
  - Frequência controlada.
- **Checklist adicional**:
  - [ ] Lista de leads atualizada
  - [ ] Mensagem diferenciada
  - [ ] Frequency cap definido

---

### P8.3 — QA pré-publicação (política, links, UTMs, tracking, preview)
- **Código/ID**: P8.3
- **Tipo**: **[U] Única**
- **Objetivo**: revisar campanha antes de publicar para evitar erros, reprovações e desperdício.
- **Momento**: após build completo (P8.1).
- **Gatilho**: campanha em status "rascunho" ou "pausada".
- **Saída**: campanha aprovada para publicação ou lista de correções.
- **Papéis**: Gestor de Tráfego (executor), CS ou Founder (revisor).
- **Ferramentas**: Ads Manager, Events Manager, LP, Notion.

#### Checklist de QA pré-publicação

**1. Compliance e Políticas**
- [ ] Sem promessas irreais ("garantia de resultado", "X reais em Y dias")
- [ ] Sem atributos pessoais ("você está com dívidas", "está acima do peso")
- [ ] Sem conteúdo proibido (antes/depois em saúde, claims absolutos)
- [ ] Imagens sem texto excessivo (< 20% texto)
- [ ] Disclaimers necessários incluídos

**2. Copy e Criativos**
- [ ] Ortografia verificada
- [ ] CTA claro e coerente com destino
- [ ] Benefício principal visível nos primeiros 3 segundos
- [ ] Marca/logo visível (se aplicável)
- [ ] Thumbnail atrativa (vídeos)

**3. Links e Destino**
- [ ] URL correta (não quebrada)
- [ ] UTMs presentes e corretos
- [ ] LP carrega em < 3 segundos
- [ ] LP responsiva (mobile)
- [ ] Formulário funciona

**4. Tracking**
- [ ] Pixel dispara na LP
- [ ] Evento de conversão configurado
- [ ] Test event enviado e recebido
- [ ] Integração de leads funcionando

**5. Configuração de Campanha**
- [ ] Orçamento correto
- [ ] Agendamento correto (data início/fim)
- [ ] Público correto (tamanho e segmentação)
- [ ] Posicionamentos adequados
- [ ] Otimização correta

**6. Preview Final**
- [ ] Preview no mobile verificado
- [ ] Preview no desktop verificado
- [ ] Preview nos posicionamentos selecionados

#### Critérios de aprovação
- **GO**: todos os itens críticos OK.
- **NO-GO**: qualquer item de compliance, tracking ou link incorreto.

#### Registro
- Criar item em `Decisões` se houver desvio do plano.
- Atualizar `Campanhas (Meta)` com `Status = Em QA`.

#### Exceções
- **Urgência**: se cliente exige publicação imediata, documentar riscos e seguir com checklist mínimo (compliance + links).

---

### P8.4 — Publicação + monitoramento 24–48h
- **Código/ID**: P8.4
- **Tipo**: **[U] Única**
- **Objetivo**: publicar campanha e monitorar primeiras horas para detectar problemas.
- **Momento**: após QA aprovado.
- **Gatilho**: checklist P8.3 completo.
- **Saída**: campanha ativa + relatório de primeiras 24–48h.
- **Papéis**: Gestor de Tráfego.
- **Ferramentas**: Ads Manager, Notion.

#### Passo a passo
- **P8.4-T1 (Obrigatória) Ativar campanha**
  - Mudar status para "Ativo".
  - Confirmar que está em "Learning" ou entregando.
- **P8.4-T2 (Obrigatória) Monitoramento H+1 a H+6**
  - Verificar se anúncios foram aprovados.
  - Verificar se está entregando (impressões > 0).
  - Checar se eventos estão sendo registrados.
- **P8.4-T3 (Obrigatória) Monitoramento D+1 (24h)**
  - Métricas iniciais: CPM, CTR, CPC, CPL (se já houver leads).
  - Comparar com benchmarks do nicho/cliente.
  - Verificar se leads estão chegando no destino.
- **P8.4-T4 (Obrigatória) Monitoramento D+2 (48h)**
  - Avaliar fase de learning.
  - Identificar anúncios com problemas (baixa entrega, alta frequência).
  - Primeiras decisões: pausar, ajustar, escalar.
- **P8.4-T5 (Obrigatória) Registrar no Notion**
  - Atualizar `Campanhas (Meta)` com `Status = Ativa`.
  - Criar registro inicial em `Testes & Hipóteses` (se aplicável).

#### Alertas críticos (primeiras 24h)
- Anúncio reprovado → seguir P12.1.
- Zero impressões → verificar orçamento, público, agendamento.
- Zero eventos → verificar tracking (P7).
- CPM muito alto (> 2x benchmark) → verificar segmentação.

#### Métricas de monitoramento inicial
- Impressões, alcance, frequência.
- CPM, CTR, CPC.
- Conversões, CPL (se houver).
- Taxa de aprovação de anúncios.

#### Automação Python (futuro A06)
- Script que monitora campanhas ativas e alerta se:
  - Anúncio reprovado.
  - Gasto > X sem conversões.
  - CPL > threshold.

---

### P8.5 — Ajustes pós-lançamento (reprovações, learning, pacing)
- **Código/ID**: P8.5
- **Tipo**: **[U] Única** (por ciclo de ajuste)
- **Objetivo**: corrigir problemas identificados nas primeiras 48h.
- **Momento**: D+1 a D+7 após publicação.
- **Gatilho**: problemas detectados em P8.4 ou fim da fase de learning.
- **Saída**: campanha otimizada ou decisão de pausar/substituir.
- **Papéis**: Gestor de Tráfego.
- **Ferramentas**: Ads Manager, Notion.

#### Cenários e ações

**Cenário 1: Anúncio reprovado**
- Verificar motivo da reprovação (política).
- Ajustar criativo/copy.
- Reenviar para revisão.
- Se persistir, seguir P12.1 (recurso).

**Cenário 2: Em "Learning Limited"**
- Causas: orçamento baixo, público pequeno, muitas conversões necessárias.
- Ações: aumentar orçamento, ampliar público, considerar otimização diferente.

**Cenário 3: CPL muito alto**
- Verificar: criativo (CTR baixo?), LP (CVR baixo?), público (relevância?).
- Testar: novo criativo, nova copy, novo público.

**Cenário 4: Pacing incorreto (gastando muito rápido ou devagar)**
- Ajustar orçamento.
- Verificar bid/cap (se usado).
- Revisar agendamento.

**Cenário 5: Zero leads mas há cliques**
- Verificar LP (carrega? formulário funciona?).
- Verificar tracking (evento dispara?).
- Verificar integração (lead chega no destino?).

#### Registro
- Documentar ajustes em `Decisões`.
- Atualizar `Testes & Hipóteses` com hipótese e resultado.

---

### P8.6 — Registro de baseline e IDs (para auditoria/BI)
- **Código/ID**: P8.6
- **Tipo**: **[U] Única**
- **Objetivo**: documentar ponto de partida para comparação futura e rastreabilidade.
- **Momento**: após estabilização da campanha (D+3 a D+7).
- **Gatilho**: campanha fora do learning e entregando.
- **Saída**: baseline documentado.
- **Papéis**: Gestor de Tráfego.
- **Ferramentas**: Notion, Ads Manager, Sheets/BI.

#### Dados a registrar (baseline)

**IDs para rastreio**
- Campaign ID (Meta).
- Ad Set IDs.
- Ad IDs.
- Pixel ID usado.
- Event(s) de conversão.

**Métricas de referência (primeiros 7 dias)**
- CPM médio.
- CTR médio.
- CPC médio.
- CVR (LP ou Lead Ads).
- CPL.
- Volume de leads.
- Qualidade de leads (se já houver feedback).

**Configuração**
- Orçamento inicial.
- Públicos usados.
- Criativos ativos.

#### Registro no FL
- Atualizar `Campanhas (Meta)` com:
  - `Link Ads Manager` (URL direta).
  - `UTM padrão`.
  - Métricas de baseline (campos customizados ou no corpo da página).

#### Uso do baseline
- Comparação semanal/mensal de performance.
- Identificação de degradação ou melhoria.
- Input para relatórios e reuniões de revisão.

#### Automação Python (futuro)
- Script que puxa métricas via Meta Ads API e registra no Notion automaticamente.
