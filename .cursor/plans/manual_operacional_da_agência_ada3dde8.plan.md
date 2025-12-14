# Manual Operacional da Agência (Meta Ads Full-Funnel)

## Premissas (explícitas)

- **Escopo**: full-funnel (Meta Ads + LP + tracking + roteiros/processo de atendimento via WhatsApp/CRM + automações).
- **Canais padrão**: WhatsApp como canal principal de atendimento; e-mail para documentos/registro; Drive como repositório; automações via Make/Zapier.
- **FL**: Notion como “sistema operacional” (bases de dados + templates + views) — automações e integrações via Make/Zapier.
- **Tipo de cliente**: negócios locais/serviços (métrica final geralmente = leads qualificados/agendamentos/vendas).
- **Onde houver variação (ex.: modelo de contrato, uso de CRM externo, BI)**: o processo terá um “caminho padrão” + variações opcionais.

## Entregáveis (formato pronto para o Notion/FL)

1. **Mapa macro completo** (P1…Pn) + visão de fases (aquisição → vendas → onboarding → entrega → CS → financeiro → pessoas → governança → compliance).
2. **Arquitetura do Notion (FL)**: bases de dados, propriedades obrigatórias, relações, status/pipelines, templates por tipo (cliente, projeto, campanha, criativo, incidente, cobrança etc.).
3. **Catálogo de processos**: para cada subprocesso (P?.?) entregar a “ficha completa” com:

- Objetivo, momento, gatilho, saídas, papéis, ferramentas
- Passo a passo (tarefas/subtarefas) + checklists
- Critérios de qualidade/aceitação + erros comuns
- Métricas relacionadas
- Oportunidades de automação (gatilho → ação)
- Templates/padrões associados
- Fluxos de exceção (não-resposta, reprovação, bloqueio, atraso, queda de performance etc.)

4. **Playbooks de crise e risco** (incidentes) + padrão de comunicação com cliente.
5. **Padrões e biblioteca**: nomenclatura (campanhas, arquivos, pastas), SOPs, scripts, modelos (briefing, proposta, contrato, relatórios).

## Mapa macro (primeira versão)

- **P1 – Estratégia & Posicionamento da Agência**
- **P2 – Aquisição de Clientes (Marketing & Prospecção)**
- **P3 – Vendas & Fechamento**
- **P4 – Onboarding de Cliente**
- **P5 – Descoberta, Pesquisa & Planejamento de Campanhas**
- **P6 – Produção de Materiais (Copy, Criativos, LP, Scripts de Atendimento)**
- **P7 – Setup Técnico (Pixel/CAPI, UTMs, CRM/WhatsApp, Eventos/Conversões)**
- **P8 – Implementação & Lançamento (Build + QA + Publicação)**
- **P9 – Rotina de Gestão e Otimização (D/S/M + registro de testes/aprendizados)**
- **P10 – Relatórios, Reuniões e Comunicação (CS)**
- **P11 – Retenção, Renovação, Upsell e Encerramento**
- **P12 – Crises, Exceções e Gestão de Risco**
- **P13 – Financeiro & Administrativo**
- **P14 – Pessoas, Treinamento e Gestão de Capacidade**
- **P15 – Documentação, Governança, Acessos e Segurança**
- **P16 – Compliance, Jurídico, Políticas e LGPD**
- **P17 – Qualidade & Melhoria Contínua (QA, auditorias, pós-mortem, playbook vivo)**

## Sequência de execução (para evitar excesso e manter implementável)

1. **Fundação do FL (Notion)**: definir bases, campos, status/pipelines, templates e padrão de nomeação.
2. **Fluxo crítico ponta-a-ponta** (core): P2→P11 (aquisição até renovação), com fichas detalhadas e automações principais.
3. **Operação de entrega (produção + tráfego + tracking)**: P5→P9 com rotinas D/S/M, regras de decisão e registro de testes.
4. **Suporte de escala**: P13–P17 (financeiro, pessoas/capacidade, governança, compliance, QA/melhoria contínua).
5. **Playbooks de exceção/crise**: P12 conectado aos processos core (com templates de comunicação e logs).

## Referências internas que vou reaproveitar

- Estrutura de fases e checkpoints descritos em `SYSTEM_SPEC.md` (ciclo de vida do cliente, setup, lançamento, otimização, reporting).
- Conceito de decomposição máxima + checkpoints humanos como padrão de QA (adaptado para operação humana/FL).