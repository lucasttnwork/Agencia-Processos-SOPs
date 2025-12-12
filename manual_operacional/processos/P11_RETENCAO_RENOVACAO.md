## P11 — Renovação, Upsell, Retenção e Encerramento

> **Objetivo do macroprocesso (P11)**: maximizar o LTV (lifetime value) de cada cliente através de retenção proativa, renovações bem gerenciadas, upsells estratégicos e, quando necessário, encerramentos organizados que preservem relacionamento e geram aprendizados.

---

### P11.1 — Monitoramento de saúde do cliente (churn risk)
- **Código/ID**: P11.1
- **Tipo**: **[R] Recorrente** (semanal)
- **Objetivo**: identificar sinais de risco de churn antes que seja tarde.
- **Momento**: rotina semanal de CS.
- **Gatilho**: calendário + eventos específicos (reclamações, atrasos, queda de engajamento).
- **Saída esperada**:
  - Score de saúde atualizado.
  - Alertas para clientes em risco.
  - Ações preventivas iniciadas.
- **Papéis envolvidos**: CS (monitor), Founder (decisões críticas).
- **Ferramentas**: Notion (`Clientes`), Histórico de comunicação.

#### Indicadores de saúde do cliente

**Sinais positivos (cliente saudável)**
- Responde rapidamente às mensagens.
- Participa das reuniões.
- Dá feedback sobre leads (positivo ou construtivo).
- Paga em dia.
- Pede mais (criativos, campanhas, budget).
- Indica outros clientes.

**Sinais de alerta (risco médio)**
- Demora para responder (> 48h).
- Cancela ou adia reuniões.
- Para de dar feedback sobre leads.
- Questiona valor/preço.
- Diminui budget sem motivo claro.
- Reclama mais do que o normal.

**Sinais críticos (risco alto)**
- Não responde há mais de 1 semana.
- Menciona "vamos avaliar continuidade".
- Compara com concorrentes.
- Atrasa pagamento.
- Ignora relatórios e reuniões.
- Performance ruim + cliente insatisfeito.

#### Score de risco (atualizar semanalmente)

| Score | Classificação | Ação |
|-------|---------------|------|
| Verde | Saudável | Manter rotina normal |
| Amarelo | Atenção | Aumentar frequência de contato, identificar causa |
| Vermelho | Crítico | Reunião urgente com Founder, plano de recuperação |

#### Registro no FL
- `Clientes`: atualizar campo `Risco de Churn` (Baixo/Médio/Alto).
- Criar tarefa de acompanhamento se risco > baixo.

#### Ações por nível de risco

**Risco Médio (Amarelo)**
- Entrar em contato proativamente.
- Perguntar: "Como você está se sentindo com os resultados?"
- Identificar preocupação específica.
- Propor solução ou ajuste.

**Risco Alto (Vermelho)**
- Reunião urgente (CS + Founder se necessário).
- Ouvir reclamações sem defensividade.
- Criar plano de ação concreto com prazos.
- Follow-up intensivo (diário/semanal).
- Considerar oferta de desconto/bônus se apropriado.

---

### P11.2 — Renovação de contrato (preparação + proposta + formalização)
- **Código/ID**: P11.2
- **Tipo**: **[U] Única** (por ciclo de contrato)
- **Objetivo**: renovar contratos de forma proativa e organizada.
- **Momento**: 30-45 dias antes do vencimento.
- **Gatilho**: calendário (data de vencimento - 45 dias).
- **Saída**: contrato renovado ou decisão de encerramento.
- **Papéis**: CS (conduz), Founder (aprova condições), Financeiro.
- **Ferramentas**: Notion, Drive (contrato), e-mail.

#### Timeline de renovação

| Quando | Ação |
|--------|------|
| D-45 | Identificar contratos próximos do vencimento |
| D-30 | Preparar análise de resultados + proposta de renovação |
| D-25 | Contato inicial: "Seu contrato vence em X dias, vamos conversar?" |
| D-20 | Reunião de revisão + apresentar proposta |
| D-15 | Follow-up se não houve resposta |
| D-10 | Segunda tentativa de contato |
| D-7 | Decisão: renovar, renegociar ou encerrar |
| D-3 | Formalização (assinatura) |
| D-0 | Início do novo ciclo |

#### Preparação da renovação

**1. Análise de resultados**
- Métricas do período: leads, CPL, ROI (se disponível).
- Comparar com meta e períodos anteriores.
- Identificar conquistas e desafios.

**2. Avaliação de relacionamento**
- Cliente satisfeito? (NPS, feedback).
- Pagamentos em dia?
- Engajamento nas reuniões?
- Risco de churn?

**3. Proposta de renovação**
- Manter condições? Reajustar?
- Oferecer algo a mais? (desconto por renovação, bônus).
- Ajustar escopo se necessário.

#### Template de proposta de renovação

```markdown
## Proposta de Renovação — [Cliente]

### Resumo do período atual
- Período: MM/YYYY a MM/YYYY
- Investimento em mídia: R$ X
- Leads gerados: X
- CPL médio: R$ Y
- Principais conquistas: [lista]

### Proposta para o próximo período
- Período: MM/YYYY a MM/YYYY (12 meses)
- Valor mensal: R$ X (mesmo valor / reajuste de Y%)
- Escopo: [manter / ajustar]

### Condições especiais (se aplicável)
- [Desconto por renovação antecipada]
- [Bônus de criativos extras]

### Próximos passos
1. Confirmação de interesse
2. Assinatura do aditivo/novo contrato
3. Pagamento da primeira parcela
```

#### Cenários de negociação

| Cenário | Abordagem |
|---------|-----------|
| Cliente quer desconto | Avaliar margem; oferecer desconto por compromisso maior (12 meses) ou reduzir escopo |
| Cliente quer pausar | Oferecer pausa de 1-2 meses (P11.4) em vez de cancelar |
| Cliente quer testar concorrente | Destacar resultados, oferecer "trial" de melhoria antes de sair |
| Cliente satisfeito | Propor upsell (P11.3) junto com renovação |

---

### P11.3 — Upsell/cross-sell (sinais + abordagem + entrega)
- **Código/ID**: P11.3
- **Tipo**: **[U] Única** (por oportunidade)
- **Objetivo**: aumentar receita por cliente oferecendo mais valor.
- **Momento**: quando identificar oportunidade.
- **Gatilho**: sinais de prontidão do cliente.
- **Saída**: upsell fechado ou oportunidade descartada com motivo.
- **Papéis**: CS (identifica), Closer (fecha), Founder (aprova).
- **Ferramentas**: Notion, WhatsApp/e-mail.

#### Sinais de oportunidade de upsell

**Cliente está pronto quando:**
- Pede mais leads ("quero aumentar volume").
- Menciona novo produto/serviço ("vamos lançar X").
- Budget de mídia está aumentando.
- Resultados estão bons e consistentes.
- Time de atendimento cresceu.
- Pergunta sobre outros serviços.
- Indica parceiros/conhecidos.

#### Tipos de upsell para agência de tráfego

| Tipo | Descrição | Quando oferecer |
|------|-----------|-----------------|
| Aumento de budget | Gestão de mais verba | Cliente satisfeito, quer mais leads |
| Novos canais | Google Ads, TikTok, LinkedIn | Cliente quer diversificar |
| Mais criativos | Pacote adicional de criativos | Criativos cansam rápido, cliente exige volume |
| LP extras | Landing pages adicionais | Testar novas ofertas |
| Consultoria | Sessões estratégicas | Cliente quer entender mais |
| Setup de automação | Integração, CRM, automações | Cliente crescendo e precisa estrutura |

#### Processo de upsell

**1. Identificar oportunidade**
- Observar sinais durante comunicação.
- Verificar se cliente tem capacidade (financeira e operacional).

**2. Plantar a semente**
- Mencionar casualmente: "Com o volume atual, você poderia considerar X..."
- Não forçar na primeira menção.

**3. Apresentar proposta**
- Se cliente demonstrar interesse, preparar proposta formal.
- Destacar benefício específico para o cliente.
- Mostrar ROI potencial.

**4. Fechar**
- Criar senso de oportunidade (não urgência falsa).
- Facilitar decisão (desconto por aceitar junto com renovação).

**5. Entregar**
- Garantir que entrega do upsell seja impecável.
- Upsell mal executado = risco de churn.

---

### P11.4 — Pausa planejada (hold) e retomada
- **Código/ID**: P11.4
- **Tipo**: **[U] Única** (por evento)
- **Objetivo**: permitir pausa sem perder o cliente.
- **Momento**: quando cliente pede para pausar.
- **Gatilho**: solicitação do cliente.
- **Saída**: contrato pausado com data de retorno ou cancelamento.
- **Papéis**: CS, Financeiro.
- **Ferramentas**: Notion, e-mail (formalização).

#### Quando aceitar pausa

**Motivos válidos**
- Sazonalidade do negócio (ex.: férias, baixa temporada).
- Problema operacional do cliente (equipe, estoque, capacidade).
- Evento externo (pandemia, crise).
- Cliente precisa de tempo para avaliar resultados.

**Motivos que merecem atenção**
- "Quero testar sozinho" → risco de não voltar.
- "Vou ver com outro fornecedor" → provavelmente churn.
- "Não tenho dinheiro agora" → avaliar se é temporário.

#### Condições de pausa (definir em contrato)

| Condição | Padrão |
|----------|--------|
| Duração máxima | 1-2 meses |
| Aviso prévio | 15-30 dias |
| Taxa de manutenção | 0% a 30% do fee (opcional) |
| Data de retorno | Definida previamente |
| Acesso a ativos | Mantido durante pausa |

#### Processo de pausa

**1. Entender motivo**
- Perguntar: "O que está levando a essa decisão?"
- Identificar se é temporário ou sinal de churn.

**2. Oferecer alternativas**
- Reduzir budget em vez de pausar.
- Reduzir escopo temporariamente.
- Desconto por continuar.

**3. Se decidir pausar**
- Formalizar por e-mail: duração, condições, data de retorno.
- Atualizar `Clientes`: `Status = Pausado`.
- Pausar campanhas (não deletar).
- Manter acessos.

**4. Durante a pausa**
- Check-in mensal: "Como estão as coisas? Quando podemos retomar?"
- Enviar conteúdo de valor (não vender).

**5. Retomada**
- 15 dias antes da data: contato para confirmar.
- Se confirmar: reativar campanhas, atualizar status.
- Se não retornar: seguir para encerramento (P11.5).

---

### P11.5 — Encerramento organizado (offboarding)
- **Código/ID**: P11.5
- **Tipo**: **[U] Única** (por cliente)
- **Objetivo**: encerrar relação de forma profissional, preservando relacionamento e aprendizados.
- **Momento**: decisão de encerramento confirmada.
- **Gatilho**: cancelamento (cliente ou agência) ou fim de contrato sem renovação.
- **Saída**: cliente offboarded, acessos devolvidos, documentação arquivada.
- **Papéis**: CS (conduz), Gestor de Tráfego (técnico), Financeiro.
- **Ferramentas**: Notion, Drive, Ads Manager, e-mail.

#### Checklist de encerramento

**1. Comunicação**
- [ ] Confirmar data de encerramento por escrito.
- [ ] Alinhar últimas entregas.
- [ ] Agradecer pela parceria.

**2. Campanhas e anúncios**
- [ ] Pausar todas as campanhas.
- [ ] Exportar dados/relatórios para cliente.
- [ ] Documentar estrutura para eventual retomada.

**3. Acessos**
- [ ] Revogar acesso da agência à BM/Ads.
- [ ] Devolver controle total ao cliente.
- [ ] Atualizar `Acessos & Governança`: `Status = Revogado`.

**4. Financeiro**
- [ ] Verificar faturas em aberto.
- [ ] Emitir última fatura (se aplicável).
- [ ] Confirmar encerramento de cobrança recorrente.

**5. Documentação**
- [ ] Entregar relatório final.
- [ ] Enviar pasta do Drive organizada.
- [ ] Arquivar dossiê do cliente.

**6. Registro**
- [ ] Atualizar `Clientes`: `Status = Encerrado`, `Data Encerramento`.
- [ ] Registrar motivo do encerramento.

#### Entregáveis finais para cliente

| Item | Formato |
|------|---------|
| Relatório final | PDF/Slides |
| Dados de campanha | Export CSV/Excel |
| Criativos aprovados | Pasta Drive |
| Documentação de tracking | Doc/PDF |
| Públicos salvos | Print/lista |

#### Comunicação de encerramento (template)

```markdown
Assunto: Encerramento da parceria — [Agência] + [Cliente]

Olá [Nome],

Conforme alinhado, formalizamos o encerramento da nossa parceria a partir de [data].

**Últimas ações realizadas:**
- Campanhas pausadas em [data].
- Relatório final anexo.
- Criativos e documentos na pasta compartilhada.

**Acessos:**
- Removemos nosso acesso à BM/conta de anúncios.
- Você mantém controle total dos ativos.

**Financeiro:**
- [Última fatura emitida em X] ou [Nenhuma pendência].

Foi um prazer trabalhar com você. Se no futuro quiser retomar, estaremos aqui.

Desejamos sucesso!

[Assinatura]
```

---

### P11.6 — Pós-mortem do cliente + aprendizados
- **Código/ID**: P11.6
- **Tipo**: **[U] Única** (por encerramento)
- **Objetivo**: extrair aprendizados de cada cliente para melhorar processos.
- **Momento**: após encerramento.
- **Gatilho**: cliente encerrado.
- **Saída**: documento de pós-mortem + ações de melhoria.
- **Papéis**: CS, Gestor de Tráfego, Founder.
- **Ferramentas**: Notion.

#### Template de pós-mortem

```markdown
## Pós-mortem — [Cliente]

### Dados básicos
- **Período de trabalho**: MM/YYYY a MM/YYYY
- **Tipo de encerramento**: Cancelamento cliente / Não renovação / Cancelamento agência
- **Motivo declarado**: [o que cliente disse]
- **Motivo real (nossa avaliação)**: [nossa interpretação]

---

### Resultados entregues
- Investimento total em mídia: R$ X
- Leads gerados: X
- CPL médio: R$ Y
- Melhor mês: [dados]
- Pior mês: [dados]

---

### O que funcionou
- [Ponto positivo 1]
- [Ponto positivo 2]

### O que não funcionou
- [Ponto negativo 1]
- [Ponto negativo 2]

---

### Por que o cliente saiu?
- [ ] Resultados abaixo do esperado
- [ ] Expectativa desalinhada
- [ ] Problemas de comunicação
- [ ] Preço/budget
- [ ] Problema operacional do cliente
- [ ] Trocou por concorrente
- [ ] Decidiu fazer interno
- [ ] Fechou o negócio
- [ ] Outro: ___

### O que poderíamos ter feito diferente?
- [Reflexão 1]
- [Reflexão 2]

---

### Ações de melhoria (para próximos clientes)
| Ação | Responsável | Prazo |
|------|-------------|-------|
| [Ação 1] | [Quem] | [Quando] |
| [Ação 2] | [Quem] | [Quando] |

---

### Cliente retornaria no futuro?
- [ ] Sim, provavelmente
- [ ] Talvez
- [ ] Não, provavelmente não
- [ ] Definitivamente não

### Porta aberta?
- [ ] Sim, saiu bem
- [ ] Parcialmente
- [ ] Não, saiu mal
```

#### Reunião de pós-mortem (opcional)

**Quando fazer**: clientes importantes ou encerramentos problemáticos.

**Participantes**: CS, Gestor de Tráfego, Founder.

**Pauta**:
1. Revisão do histórico do cliente.
2. O que aconteceu (linha do tempo).
3. O que aprendemos.
4. O que mudar nos processos.

#### Ações após pós-mortem
- Atualizar SOPs se necessário.
- Compartilhar aprendizado com equipe.
- Criar tarefa para implementar melhorias.
