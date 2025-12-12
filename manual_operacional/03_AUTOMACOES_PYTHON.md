# 03 – ARQUITETURA DE AUTOMAÇÕES PYTHON

**Versão**: 1.0
**Data**: 12/12/2025
**Responsável**: Diretor de Operações + Tech Lead

---

## VISÃO GERAL

Este documento define a arquitetura técnica de **automações próprias em Python** da agência, substituindo plataformas no-code como Make/Zapier por soluções customizadas, escaláveis e integradas ao nosso stack operacional (Notion, Meta Ads, WhatsApp, Google Drive, etc.).

**Por Que Automações Próprias?**
- ✅ Controle total sobre lógica e funcionalidades
- ✅ Custo previsível (não escala linearmente com volume)
- ✅ Integrações profundas com sistemas proprietários (Notion como FL)
- ✅ Manutenibilidade e evolução contínua
- ✅ Dados sensíveis permanecem sob nosso controle (segurança)

**Escopo**: 76+ automações mapeadas nos processos P1-P17, cobrindo:
- Monitoramento e alertas (performance, incidentes, prazos)
- Sincronização de dados (Notion ↔ Meta Ads ↔ Google Sheets)
- Geração automática de relatórios (PDF, Google Slides)
- Comunicação automatizada (WhatsApp, Email, Slack)
- Gestão de tarefas e workflows (Notion)
- Coleta e análise de dados (dashboards)

---

## STACK TECNOLÓGICO

### Linguagem e Runtime
- **Python 3.11+** (type hints, async/await, performance)
- **Virtual Environment** (venv ou poetry para gestão de dependências)

### Bibliotecas Core
```python
# Integrações APIs
notion-client          # Notion API (nosso FL - sistema operacional)
facebook-business      # Meta Ads API (campanhas, métricas)
google-api-python-client  # Google Drive, Sheets, Analytics
gspread                # Google Sheets (mais simples que google-api)
openai                 # Claude/GPT para análises de dados, copywriting

# Agendamento e Execução
apscheduler            # Scheduler (cron jobs, triggers temporais)
celery                 # Task queue (tarefas assíncronas, distribuídas)
redis                  # Backend para Celery (message broker)

# Comunicação
requests               # HTTP requests (webhooks, APIs REST)
python-telegram-bot    # Telegram (alternativa a WhatsApp)
twilio                 # WhatsApp Business API, SMS
slack-sdk              # Slack (notificações internas)

# Dados e Relatórios
pandas                 # Manipulação de dados (dataframes)
openpyxl               # Excel (leitura/escrita)
python-pptx            # PowerPoint (relatórios automatizados)
reportlab / weasyprint # PDF (relatórios)
plotly / matplotlib    # Gráficos

# Utilidades
python-dotenv          # Variáveis de ambiente (.env)
loguru                 # Logging estruturado
pydantic               # Validação de dados (type safety)
tenacity               # Retry logic (resiliência)
```

### Infraestrutura e Deploy
- **Servidor**: VPS (DigitalOcean, AWS EC2, Hetzner) ou serverless (AWS Lambda para automações leves)
- **Banco de Dados**: Redis (cache, filas), PostgreSQL (se necessário armazenar histórico)
- **Monitoramento**: Sentry (error tracking), Grafana + Prometheus (métricas)
- **Secrets Management**: Variáveis de ambiente (.env local), AWS Secrets Manager (prod)

---

## ESTRUTURA DE PASTAS

```
automacoes/
├── README.md                  # Documentação principal
├── requirements.txt           # Dependências Python
├── .env.example               # Template de variáveis de ambiente
├── .gitignore                 # Não commitar .env, __pycache__, etc.
│
├── config/
│   ├── __init__.py
│   ├── settings.py            # Configurações centralizadas (carrega .env)
│   ├── notion_db_ids.py       # IDs dos databases Notion (Clientes, Campanhas, etc.)
│   └── meta_ads_config.py     # Configurações Meta Ads (Business ID, Ad Account IDs)
│
├── integrations/              # Wrappers para APIs externas
│   ├── __init__.py
│   ├── notion_client.py       # Cliente Notion com métodos helpers
│   ├── meta_ads_client.py     # Cliente Meta Ads
│   ├── google_client.py       # Google Sheets, Drive, Analytics
│   ├── whatsapp_client.py     # WhatsApp Business API (Twilio)
│   ├── slack_client.py        # Slack
│   └── email_client.py        # SMTP / SendGrid
│
├── workflows/                 # Automações organizadas por processo
│   ├── __init__.py
│   │
│   ├── p7_setup_tecnico/
│   │   ├── a01_pixel_health_check.py
│   │   └── ...
│   │
│   ├── p8_implementacao/
│   │   ├── a02_alerta_campanha_pendente.py
│   │   └── ...
│   │
│   ├── p9_gestao_otimizacao/
│   │   ├── a08_alerta_cpa_acima_meta.py
│   │   ├── a09_sugestoes_otimizacao.py
│   │   └── ...
│   │
│   ├── p10_relatorios/
│   │   ├── a20_relatorio_semanal_auto.py
│   │   ├── a21_relatorio_mensal_pdf.py
│   │   └── ...
│   │
│   ├── p11_retencao/
│   │   ├── a30_alerta_renovacao_vencendo.py
│   │   ├── a33_envio_pesquisa_nps.py
│   │   └── ...
│   │
│   ├── p12_crises/
│   │   ├── a38_alerta_anuncio_reprovado.py
│   │   ├── a39_alerta_conta_bloqueada.py
│   │   └── ...
│   │
│   ├── p13_financeiro/
│   │   ├── a50_lembrete_pagamento_vencendo.py
│   │   ├── a53_calculo_dre_mensal.py
│   │   └── ...
│   │
│   ├── p14_pessoas/
│   │   ├── a57_lembrete_1on1.py
│   │   ├── a58_calculo_utilizacao_time.py
│   │   └── ...
│   │
│   ├── p15_governanca/
│   │   ├── a62_backup_notion.py
│   │   └── ...
│   │
│   ├── p16_compliance/
│   │   ├── a64_verificacao_lgpd.py
│   │   └── ...
│   │
│   └── p17_qualidade/
│       ├── a72_alerta_acoes_corretivas.py
│       ├── a73_coleta_dados_dashboard.py
│       └── ...
│
├── scheduler/
│   ├── __init__.py
│   ├── jobs.py                # Definição de jobs agendados (APScheduler)
│   └── run_scheduler.py       # Script principal do scheduler
│
├── utils/
│   ├── __init__.py
│   ├── logger.py              # Configuração de logging (Loguru)
│   ├── retry.py               # Retry logic com tenacity
│   ├── validators.py          # Validação de dados (Pydantic models)
│   └── formatters.py          # Formatadores (moeda, data, etc.)
│
└── tests/
    ├── __init__.py
    ├── test_notion_client.py
    ├── test_meta_ads_client.py
    └── ...
```

---

## ÍNDICE COMPLETO DE AUTOMAÇÕES (A01-A76)

### P7 – SETUP TÉCNICO

| ID | Nome | Trigger | Ação | Arquivo |
|----|------|---------|------|---------|
| **A01** | Pixel Health Check | Diário (00:00) | Verificar eventos Pixel/CAPI últimas 24h → Alertar se <5 eventos ou erro | `p7_setup_tecnico/a01_pixel_health_check.py` |

---

### P8 – IMPLEMENTAÇÃO E LANÇAMENTO

| ID | Nome | Trigger | Ação | Arquivo |
|----|------|---------|------|---------|
| **A02** | Alerta de Campanha Pendente Lançamento | Diário (09:00) | Notion: Campanhas "Aprovada Cliente" sem data lançamento → Alertar gestor | `p8_implementacao/a02_alerta_campanha_pendente.py` |
| **A03** | Checklist QA Pré-Lançamento | Manual/Webhook | Validar 42 pontos QA antes de lançar campanha | `p8_implementacao/a03_checklist_qa.py` |

---

### P9 – GESTÃO E OTIMIZAÇÃO

| ID | Nome | Trigger | Ação | Arquivo |
|----|------|---------|------|---------|
| **A08** | Alerta CPA Acima da Meta | Diário (08:00) | Meta Ads API: CPA >110% meta por 3 dias → Alertar gestor + criar tarefa Notion | `p9_gestao_otimizacao/a08_alerta_cpa_acima_meta.py` |
| **A09** | Sugestões de Otimização (IA) | Semanal (Segunda 09:00) | Analisar dados campanha → GPT-4 gera sugestões → Postar em Notion | `p9_gestao_otimizacao/a09_sugestoes_otimizacao.py` |
| **A10** | Detecção de Fadiga de Criativo | Diário (10:00) | Frequência >4 ou CTR caiu >30% → Alertar "trocar criativo" | `p9_gestao_otimizacao/a10_fadiga_criativo.py` |
| **A11** | Alerta de Budget Diário Esgotado | Tempo Real (webhook) | Budget diário esgotado antes 18h → Alertar (possível perda vendas) | `p9_gestao_otimizacao/a11_alerta_budget_esgotado.py` |
| **A12** | Dashboard de Performance (atualização) | A cada 6h | Coletar métricas Meta Ads → Atualizar Google Sheets/Data Studio | `p9_gestao_otimizacao/a12_update_dashboard.py` |

---

### P10 – RELATÓRIOS E COMUNICAÇÃO

| ID | Nome | Trigger | Ação | Arquivo |
|----|------|---------|------|---------|
| **A20** | Geração Automática de Relatório Semanal | Segunda 07:00 | Coletar dados semana anterior → Preencher template Google Slides/PDF | `p10_relatorios/a20_relatorio_semanal_auto.py` |
| **A21** | Geração de Relatório Mensal (PDF) | 1º dia do mês (08:00) | Dados mês anterior → PDF com gráficos → Salvar Drive + Notion | `p10_relatorios/a21_relatorio_mensal_pdf.py` |
| **A22** | Lembrete de Reunião com Cliente | 1 dia antes reunião | Notion (Reuniões agendadas) → Notificar gestor + enviar pauta | `p10_relatorios/a22_lembrete_reuniao.py` |
| **A23** | Envio Automático de Relatório Semanal | Segunda 10:00 | Gerar relatório (A20) → Enviar email/WhatsApp cliente | `p10_relatorios/a23_envio_relatorio_semanal.py` |
| **A24** | Qualificação de Leads (Score) | Webhook (novo lead) | Dados lead → Calcular score (BANT) → Atualizar Notion | `p10_relatorios/a24_qualificacao_leads.py` |
| **A25** | Alerta de CPA Escalado >30% | Tempo Real (webhook) | CPA aumentou >30% após escalonamento → Alertar imediatamente | `p10_relatorios/a25_alerta_cpa_escalado.py` |

---

### P11 – RETENÇÃO E RENOVAÇÃO

| ID | Nome | Trigger | Ação | Arquivo |
|----|------|---------|------|---------|
| **A30** | Alerta de Renovação Vencendo | Diário (09:00) | Contratos vencendo em 30/15/7 dias → Notificar atendimento | `p11_retencao/a30_alerta_renovacao_vencendo.py` |
| **A31** | Detecção de Risco de Churn | Semanal (Segunda 10:00) | Calcular health score cliente → Se <50: Alertar + criar plano ação | `p11_retencao/a31_deteccao_risco_churn.py` |
| **A32** | Identificação de Oportunidades Upsell | Mensal (dia 5) | Clientes com ROI >300% + budget <80% capacidade → Sugerir upsell | `p11_retencao/a32_oportunidades_upsell.py` |
| **A33** | Envio de Pesquisa NPS | Trimestral (1º dia) | Enviar email/WhatsApp com link pesquisa NPS | `p11_retencao/a33_envio_pesquisa_nps.py` |
| **A34** | Consolidação de Resultados NPS | Webhook (resposta NPS) | Atualizar Notion + Calcular NPS geral + Alertar detratores | `p11_retencao/a34_consolidacao_nps.py` |

---

### P12 – CRISES E EXCEÇÕES

| ID | Nome | Trigger | Ação | Arquivo |
|----|------|---------|------|---------|
| **A38** | Alerta de Anúncio Reprovado | Webhook Meta Ads | Anúncio reprovado → Notificar gestor + criar incidente Notion | `p12_crises/a38_alerta_anuncio_reprovado.py` |
| **A39** | Alerta de Conta/BM Bloqueado | Webhook Meta Ads | Conta bloqueada → Alerta CRÍTICO (Slack, WhatsApp, Email) | `p12_crises/a39_alerta_conta_bloqueada.py` |
| **A40** | Detecção de Queda Performance >50% | A cada 6h | CPA aumentou >50% ou conversões caíram >50% em 24h → Alerta | `p12_crises/a40_deteccao_queda_performance.py` |
| **A41** | Monitoramento de Tracking (Pixel/CAPI) | A cada 2h | Zero eventos nas últimas 2h (horário comercial) → Alerta URGENTE | `p12_crises/a41_monitoramento_tracking.py` |
| **A42** | Envio de Comunicado de Crise | Manual/Trigger | Template comunicado → Enviar WhatsApp/Email cliente | `p12_crises/a42_envio_comunicado_crise.py` |

---

### P13 – FINANCEIRO

| ID | Nome | Trigger | Ação | Arquivo |
|----|------|---------|------|---------|
| **A50** | Lembrete de Pagamento Vencendo | Diário (09:00) | Faturas vencendo em 3/1 dias → Notificar financeiro | `p13_financeiro/a50_lembrete_pagamento_vencendo.py` |
| **A51** | Follow-up Automático de Atraso | Diário (10:00) | Pagamentos atrasados (+1, +3, +7, +10 dias) → Enviar email sequencial | `p13_financeiro/a51_followup_atraso.py` |
| **A52** | Geração de Fatura (PDF) | Manual/Webhook | Dados Notion → Gerar PDF fatura → Salvar Drive + Enviar cliente | `p13_financeiro/a52_geracao_fatura.py` |
| **A53** | Cálculo Automático de DRE Mensal | 1º dia do mês | Coletar receitas + custos Notion → Calcular DRE → Postar Google Sheets | `p13_financeiro/a53_calculo_dre.py` |
| **A54** | Alerta de Lucratividade por Cliente <20% | Mensal (dia 5) | Calcular margem cliente → Se <20%: Alertar para revisão pricing | `p13_financeiro/a54_alerta_lucratividade.py` |

---

### P14 – PESSOAS E CAPACIDADE

| ID | Nome | Trigger | Ação | Arquivo |
|----|------|---------|------|---------|
| **A57** | Lembrete de 1:1 Agendado | 1 dia antes | Notion (1:1s agendados) → Notificar líder + liderado | `p14_pessoas/a57_lembrete_1on1.py` |
| **A58** | Cálculo de Utilização do Time | Semanal (Segunda 08:00) | Contar clientes por gestor → Calcular % utilização → Dashboard | `p14_pessoas/a58_calculo_utilizacao.py` |
| **A59** | Alerta de Sobrecarga (>100% utilização) | Semanal (Segunda 09:00) | Gestor >100% utilização → Alertar Diretor Operações | `p14_pessoas/a59_alerta_sobrecarga.py` |
| **A60** | Lembrete de Avaliação de Performance | Trimestral (15 dias antes) | Avaliações trimestrais → Notificar líderes para preparar | `p14_pessoas/a60_lembrete_avaliacao.py` |

---

### P15 – GOVERNANÇA E ACESSOS

| ID | Nome | Trigger | Ação | Arquivo |
|----|------|---------|------|---------|
| **A62** | Backup Automático do Notion | Diário (02:00) | Export completo Notion → Salvar Drive (pasta Backups) | `p15_governanca/a62_backup_notion.py` |
| **A63** | Auditoria de Acessos Inativos | Mensal (dia 1) | Listar usuários sem login >60 dias → Notificar para revisar acessos | `p15_governanca/a63_auditoria_acessos.py` |

---

### P16 – COMPLIANCE E JURÍDICO

| ID | Nome | Trigger | Ação | Arquivo |
|----|------|---------|------|---------|
| **A64** | Verificação de Conformidade LGPD | Semanal (Segunda) | Verificar checkboxes de consentimento em formulários → Alertar se faltando | `p16_compliance/a64_verificacao_lgpd.py` |
| **A65** | Alerta de DSAR Pendente | Diário (09:00) | Solicitações LGPD (DSAR) >10 dias sem resposta → Alertar (prazo 15 dias) | `p16_compliance/a65_alerta_dsar_pendente.py` |
| **A66** | Análise de Taxa de Reprovação de Anúncios | Semanal (Segunda) | Calcular % anúncios reprovados → Se >2%: Alertar compliance | `p16_compliance/a66_analise_taxa_reprovacao.py` |

---

### P17 – QUALIDADE E MELHORIA

| ID | Nome | Trigger | Ação | Arquivo |
|----|------|---------|------|---------|
| **A72** | Alerta de Ações Corretivas Vencendo | Diário (08:00) | Notion (Projetos Melhoria com prazo <3 dias) → Notificar responsável | `p17_qualidade/a72_alerta_acoes_corretivas.py` |
| **A73** | Coleta de Dados para Dashboard Qualidade | Diário (00:00) | API Notion → Query databases → Update Google Sheets | `p17_qualidade/a73_coleta_dados_dashboard.py` |
| **A74** | Cálculo de KPIs de Qualidade | Diário (01:00) | Ler Google Sheets → Calcular indicadores → Atualizar dashboard | `p17_qualidade/a74_calculo_kpis.py` |
| **A75** | Alerta de KPIs Fora da Meta | Diário (07:00) | Verificar KPIs vermelhos → Notificar Diretor Operações | `p17_qualidade/a75_alerta_kpis_fora_meta.py` |

---

### P1 – ESTRATÉGIA E POSICIONAMENTO

| ID | Nome | Trigger | Ação | Arquivo |
|----|------|---------|------|---------|
| **A76** | Lembrete Trimestral de Revisão VMV | Trimestral (último dia) | Notificar CEO/Sócios → Revisar Visão, Missão, Valores em P17.5 | `p1_estrategia/a76_lembrete_revisao_vmv.py` |

---

## EXEMPLO DE CÓDIGO: A08 – Alerta CPA Acima da Meta

**Arquivo**: `workflows/p9_gestao_otimizacao/a08_alerta_cpa_acima_meta.py`

```python
"""
A08 - Alerta de CPA Acima da Meta

Trigger: Diário às 08:00
Ação: Verificar campanhas com CPA >110% da meta por 3+ dias consecutivos
       → Alertar gestor + Criar tarefa no Notion
"""

import os
from datetime import datetime, timedelta
from loguru import logger

from integrations.notion_client import NotionClient
from integrations.meta_ads_client import MetaAdsClient
from integrations.slack_client import SlackClient
from config.settings import NOTION_DB_IDS
from utils.validators import Campaign


def check_cpa_above_threshold():
    """Verifica campanhas com CPA acima da meta."""

    notion = NotionClient()
    meta_ads = MetaAdsClient()
    slack = SlackClient()

    # 1. Buscar campanhas ativas no Notion
    campaigns = notion.query_database(
        database_id=NOTION_DB_IDS["campanhas"],
        filter={
            "property": "Status",
            "select": {"equals": "Ativa"}
        }
    )

    logger.info(f"Encontradas {len(campaigns)} campanhas ativas")

    alerts = []

    for campaign_notion in campaigns:
        try:
            # 2. Extrair dados do Notion
            campaign_id = campaign_notion["properties"]["ID Meta Ads"]["rich_text"][0]["text"]["content"]
            meta_cpa = float(campaign_notion["properties"]["Meta CPA"]["number"])
            gestor_id = campaign_notion["properties"]["Gestor"]["people"][0]["id"]
            cliente_nome = campaign_notion["properties"]["Cliente"]["relation"][0]["id"]  # Simplificado

            # 3. Buscar métricas dos últimos 3 dias no Meta Ads
            end_date = datetime.now()
            start_date = end_date - timedelta(days=3)

            insights = meta_ads.get_campaign_insights(
                campaign_id=campaign_id,
                date_preset=None,
                time_range={
                    'since': start_date.strftime('%Y-%m-%d'),
                    'until': end_date.strftime('%Y-%m-%d')
                },
                fields=['spend', 'actions', 'cost_per_action_type']
            )

            if not insights:
                logger.warning(f"Sem dados para campanha {campaign_id}")
                continue

            # 4. Calcular CPA médio dos últimos 3 dias
            total_spend = sum(float(day['spend']) for day in insights)
            total_conversions = sum(
                int(action['value'])
                for day in insights
                for action in day.get('actions', [])
                if action['action_type'] == 'purchase'  # Ajustar conforme evento de conversão
            )

            if total_conversions == 0:
                logger.warning(f"Campanha {campaign_id} sem conversões nos últimos 3 dias")
                continue

            cpa_atual = total_spend / total_conversions

            # 5. Verificar se CPA está >110% da meta
            threshold = meta_cpa * 1.10

            if cpa_atual > threshold:
                alert_data = {
                    'campaign_id': campaign_id,
                    'cliente': cliente_nome,
                    'cpa_meta': meta_cpa,
                    'cpa_atual': cpa_atual,
                    'desvio_percentual': ((cpa_atual - meta_cpa) / meta_cpa) * 100,
                    'gestor_id': gestor_id
                }
                alerts.append(alert_data)

                logger.warning(
                    f"⚠️ CPA Acima da Meta | Campanha: {campaign_id} | "
                    f"Meta: R${meta_cpa:.2f} | Atual: R${cpa_atual:.2f} "
                    f"(+{alert_data['desvio_percentual']:.1f}%)"
                )

        except Exception as e:
            logger.error(f"Erro ao processar campanha {campaign_notion['id']}: {e}")
            continue

    # 6. Gerar alertas
    if alerts:
        for alert in alerts:
            # 6.1 Criar tarefa no Notion
            notion.create_page(
                database_id=NOTION_DB_IDS["tarefas"],
                properties={
                    "Nome": {"title": [{"text": {"content": f"🚨 Otimizar CPA - Campanha {alert['campaign_id']}"}}]},
                    "Responsável": {"people": [{"id": alert['gestor_id']}]},
                    "Prioridade": {"select": {"name": "Alta"}},
                    "Prazo": {"date": {"start": (datetime.now() + timedelta(days=1)).isoformat()}},
                    "Descrição": {
                        "rich_text": [{
                            "text": {
                                "content": f"CPA atual (R${alert['cpa_atual']:.2f}) está {alert['desvio_percentual']:.1f}% acima da meta (R${alert['cpa_meta']:.2f}). Analisar campanhas e otimizar urgentemente."
                            }
                        }]
                    }
                }
            )

            # 6.2 Notificar gestor no Slack
            slack.send_message(
                channel=f"@{alert['gestor_id']}",  # DM
                message=f"🚨 *Alerta de CPA* - Campanha `{alert['campaign_id']}`\n\n"
                        f"• Cliente: {alert['cliente']}\n"
                        f"• CPA Meta: R${alert['cpa_meta']:.2f}\n"
                        f"• CPA Atual (3 dias): R${alert['cpa_atual']:.2f}\n"
                        f"• Desvio: +{alert['desvio_percentual']:.1f}%\n\n"
                        f"✅ Tarefa criada no Notion. Prazo: 24h"
            )

        logger.success(f"✅ {len(alerts)} alertas enviados")
    else:
        logger.info("✅ Todas as campanhas dentro da meta de CPA")


if __name__ == "__main__":
    check_cpa_above_threshold()
```

---

## EXEMPLO DE CÓDIGO: A20 – Geração Automática de Relatório Semanal

**Arquivo**: `workflows/p10_relatorios/a20_relatorio_semanal_auto.py`

```python
"""
A20 - Geração Automática de Relatório Semanal

Trigger: Segunda-feira às 07:00
Ação: Coletar dados da semana anterior (Segunda a Domingo)
       → Preencher template Google Slides/PDF
       → Salvar no Drive
"""

from datetime import datetime, timedelta
from loguru import logger

from integrations.notion_client import NotionClient
from integrations.meta_ads_client import MetaAdsClient
from integrations.google_client import GoogleSlidesClient, GoogleDriveClient
from config.settings import GOOGLE_SLIDES_TEMPLATE_ID


def generate_weekly_report(cliente_id: str):
    """Gera relatório semanal para um cliente."""

    notion = NotionClient()
    meta_ads = MetaAdsClient()
    slides = GoogleSlidesClient()
    drive = GoogleDriveClient()

    # 1. Buscar dados do cliente no Notion
    cliente = notion.get_page(cliente_id)
    cliente_nome = cliente["properties"]["Nome"]["title"][0]["text"]["content"]
    ad_account_id = cliente["properties"]["Ad Account ID"]["rich_text"][0]["text"]["content"]

    logger.info(f"Gerando relatório semanal para {cliente_nome}")

    # 2. Calcular período (segunda a domingo da semana passada)
    today = datetime.now()
    last_monday = today - timedelta(days=today.weekday() + 7)
    last_sunday = last_monday + timedelta(days=6)

    # 3. Coletar métricas do Meta Ads
    insights = meta_ads.get_account_insights(
        account_id=ad_account_id,
        time_range={
            'since': last_monday.strftime('%Y-%m-%d'),
            'until': last_sunday.strftime('%Y-%m-%d')
        },
        fields=[
            'spend', 'impressions', 'clicks', 'ctr', 'cpc', 'cpm',
            'actions', 'cost_per_action_type', 'action_values'
        ]
    )

    # 4. Processar dados
    spend = float(insights[0]['spend'])
    impressions = int(insights[0]['impressions'])
    clicks = int(insights[0]['clicks'])
    ctr = float(insights[0]['ctr'])
    cpc = float(insights[0]['cpc'])

    # Conversões (assumindo evento 'purchase')
    conversions = next(
        (int(action['value']) for action in insights[0].get('actions', []) if action['action_type'] == 'purchase'),
        0
    )
    revenue = next(
        (float(action['value']) for action in insights[0].get('action_values', []) if action['action_type'] == 'purchase'),
        0
    )

    cpa = spend / conversions if conversions > 0 else 0
    roi = ((revenue - spend) / spend * 100) if spend > 0 else 0

    # 5. Copiar template do Google Slides
    presentation_id = slides.copy_template(
        template_id=GOOGLE_SLIDES_TEMPLATE_ID,
        new_name=f"Relatório Semanal - {cliente_nome} - {last_monday.strftime('%d/%m/%Y')}"
    )

    # 6. Preencher placeholders no template
    replacements = {
        '{{cliente_nome}}': cliente_nome,
        '{{periodo}}': f"{last_monday.strftime('%d/%m')} a {last_sunday.strftime('%d/%m/%Y')}",
        '{{investimento}}': f"R$ {spend:,.2f}",
        '{{impressoes}}': f"{impressions:,}",
        '{{cliques}}': f"{clicks:,}",
        '{{ctr}}': f"{ctr:.2f}%",
        '{{cpc}}': f"R$ {cpc:.2f}",
        '{{conversoes}}': f"{conversions}",
        '{{cpa}}': f"R$ {cpa:.2f}",
        '{{receita}}': f"R$ {revenue:,.2f}",
        '{{roi}}': f"{roi:.1f}%"
    }

    slides.replace_text(presentation_id, replacements)

    # 7. Exportar como PDF e salvar no Drive
    pdf_file_id = slides.export_as_pdf(
        presentation_id=presentation_id,
        destination_folder_id=cliente["properties"]["Pasta Drive"]["url"].split('/')[-1]  # Simplificado
    )

    logger.success(f"✅ Relatório gerado: {cliente_nome} | PDF ID: {pdf_file_id}")

    # 8. Atualizar Notion com link do relatório
    notion.update_page(
        page_id=cliente_id,
        properties={
            "Último Relatório": {
                "url": f"https://drive.google.com/file/d/{pdf_file_id}/view"
            }
        }
    )

    return presentation_id, pdf_file_id


def run_for_all_active_clients():
    """Executa geração de relatório para todos os clientes ativos."""

    notion = NotionClient()

    # Buscar todos os clientes ativos
    clientes = notion.query_database(
        database_id=NOTION_DB_IDS["clientes"],
        filter={
            "property": "Status",
            "select": {"equals": "Ativo"}
        }
    )

    logger.info(f"Gerando relatórios semanais para {len(clientes)} clientes")

    for cliente in clientes:
        try:
            generate_weekly_report(cliente["id"])
        except Exception as e:
            logger.error(f"Erro ao gerar relatório para {cliente['id']}: {e}")

    logger.success(f"✅ Todos os relatórios gerados!")


if __name__ == "__main__":
    run_for_all_active_clients()
```

---

## GUIA DE IMPLEMENTAÇÃO

### 1. Setup Inicial

```bash
# 1.1 Criar estrutura de pastas
cd /path/to/project
mkdir -p automacoes/{config,integrations,workflows,scheduler,utils,tests}

# 1.2 Inicializar ambiente Python
cd automacoes
python3.11 -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate

# 1.3 Instalar dependências
pip install -r requirements.txt

# 1.4 Configurar variáveis de ambiente
cp .env.example .env
# Editar .env com suas credenciais (Notion API Key, Meta Ads Token, etc.)
```

### 2. Configuração de Secrets (.env)

```bash
# .env
# Notion
NOTION_API_KEY=secret_xxxxxxxxxxxxx
NOTION_DB_CLIENTES=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
NOTION_DB_CAMPANHAS=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
# ... (todos os database IDs)

# Meta Ads
META_APP_ID=xxxxxxxxxxxxx
META_APP_SECRET=xxxxxxxxxxxxxxxxxxxxxxxx
META_ACCESS_TOKEN=EAAxxxxxxxxxxxx
META_BUSINESS_ID=xxxxxxxxxxxxx

# Google
GOOGLE_CREDENTIALS_JSON=/path/to/credentials.json
GOOGLE_SLIDES_TEMPLATE_ID=xxxxxxxxxxxxxxxxxxxxx

# WhatsApp (Twilio)
TWILIO_ACCOUNT_SID=ACxxxxxxxxxxxxxxxx
TWILIO_AUTH_TOKEN=xxxxxxxxxxxxxxxx
TWILIO_WHATSAPP_FROM=whatsapp:+14155238886

# Slack
SLACK_BOT_TOKEN=xoxb-xxxxxxxxxxxxx

# Email
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=seu-email@gmail.com
SMTP_PASSWORD=sua-senha-app

# Redis (Celery)
REDIS_URL=redis://localhost:6379/0

# Sentry (Monitoring)
SENTRY_DSN=https://xxxxxx@sentry.io/xxxxxx
```

### 3. Executar Scheduler (APScheduler)

**Arquivo**: `scheduler/run_scheduler.py`

```python
from apscheduler.schedulers.blocking import BlockingScheduler
from apscheduler.triggers.cron import CronTrigger
from loguru import logger

# Importar workflows
from workflows.p9_gestao_otimizacao.a08_alerta_cpa_acima_meta import check_cpa_above_threshold
from workflows.p10_relatorios.a20_relatorio_semanal_auto import run_for_all_active_clients
# ... outros imports

def main():
    scheduler = BlockingScheduler()

    # A08 - Alerta CPA (Diário às 08:00)
    scheduler.add_job(
        check_cpa_above_threshold,
        trigger=CronTrigger(hour=8, minute=0),
        id='a08_alerta_cpa',
        name='Alerta CPA Acima da Meta'
    )

    # A20 - Relatório Semanal (Segunda às 07:00)
    scheduler.add_job(
        run_for_all_active_clients,
        trigger=CronTrigger(day_of_week='mon', hour=7, minute=0),
        id='a20_relatorio_semanal',
        name='Geração Relatório Semanal'
    )

    # ... adicionar todos os outros jobs

    logger.info("🚀 Scheduler iniciado. Jobs agendados:")
    scheduler.print_jobs()

    try:
        scheduler.start()
    except (KeyboardInterrupt, SystemExit):
        logger.info("⏹️ Scheduler encerrado")

if __name__ == "__main__":
    main()
```

**Executar**:
```bash
python scheduler/run_scheduler.py
```

### 4. Deploy em Produção (VPS)

```bash
# 4.1 Usar systemd para rodar scheduler como serviço
sudo nano /etc/systemd/system/automacoes-scheduler.service

# Conteúdo:
[Unit]
Description=Automacoes Scheduler
After=network.target

[Service]
Type=simple
User=seu-usuario
WorkingDirectory=/path/to/automacoes
Environment="PATH=/path/to/automacoes/venv/bin"
ExecStart=/path/to/automacoes/venv/bin/python scheduler/run_scheduler.py
Restart=on-failure

[Install]
WantedBy=multi-user.target

# 4.2 Ativar e iniciar serviço
sudo systemctl daemon-reload
sudo systemctl enable automacoes-scheduler
sudo systemctl start automacoes-scheduler

# 4.3 Verificar status
sudo systemctl status automacoes-scheduler
```

---

## BOAS PRÁTICAS

### 1. Logging Estruturado
```python
from loguru import logger

# Configurar logger
logger.add(
    "logs/automacoes_{time:YYYY-MM-DD}.log",
    rotation="1 day",
    retention="30 days",
    level="INFO"
)

# Uso
logger.info("Iniciando processamento")
logger.warning("CPA acima da meta", cpa_atual=150, cpa_meta=100)
logger.error("Erro ao conectar API", error=str(e))
```

### 2. Retry Logic (Resiliência)
```python
from tenacity import retry, stop_after_attempt, wait_exponential

@retry(
    stop=stop_after_attempt(3),
    wait=wait_exponential(multiplier=1, min=2, max=10)
)
def call_meta_ads_api():
    # Código que pode falhar (network issues, rate limit)
    ...
```

### 3. Validação de Dados (Pydantic)
```python
from pydantic import BaseModel, validator

class Campaign(BaseModel):
    id: str
    nome: str
    meta_cpa: float
    status: str

    @validator('meta_cpa')
    def cpa_must_be_positive(cls, v):
        if v <= 0:
            raise ValueError('CPA deve ser positivo')
        return v
```

### 4. Testes Unitários
```python
# tests/test_a08_alerta_cpa.py
import pytest
from workflows.p9_gestao_otimizacao.a08_alerta_cpa_acima_meta import check_cpa_above_threshold

def test_alerta_cpa_acima_meta(mocker):
    # Mock de APIs externas
    mock_notion = mocker.patch('integrations.notion_client.NotionClient')
    mock_meta_ads = mocker.patch('integrations.meta_ads_client.MetaAdsClient')

    # Setup
    mock_notion.return_value.query_database.return_value = [...]
    mock_meta_ads.return_value.get_campaign_insights.return_value = [...]

    # Execute
    check_cpa_above_threshold()

    # Assert
    assert mock_notion.return_value.create_page.called
```

---

## MONITORAMENTO E ALERTAS

### Sentry (Error Tracking)
```python
import sentry_sdk
from config.settings import SENTRY_DSN

sentry_sdk.init(
    dsn=SENTRY_DSN,
    traces_sample_rate=1.0,
    environment="production"
)

# Erros são automaticamente enviados ao Sentry
```

### Health Check Endpoint (opcional)
```python
# Simple FastAPI app para health checks
from fastapi import FastAPI

app = FastAPI()

@app.get("/health")
def health_check():
    return {"status": "ok", "scheduler": "running"}

# Monitorar com UptimeRobot ou similar
```

---

## ROADMAP DE IMPLEMENTAÇÃO

### Fase 1 (Mês 1-2): Fundação
- ✅ Setup de infraestrutura (VPS, Python, deps)
- ✅ Implementar clients base (Notion, Meta Ads, Google)
- ✅ Implementar automações críticas:
  - A08 (Alerta CPA)
  - A20 (Relatório Semanal)
  - A38/A39 (Alertas de Crise)
  - A50 (Lembrete Pagamento)

### Fase 2 (Mês 3-4): Expansão
- ✅ Implementar automações de otimização (A09, A10, A11, A12)
- ✅ Implementar automações de retenção (A30-A34)
- ✅ Dashboard de qualidade (A73-A75)

### Fase 3 (Mês 5-6): Refinamento
- ✅ Implementar automações de pessoas (A57-A60)
- ✅ Implementar automações de compliance (A64-A66)
- ✅ Monitoramento e testes automatizados

---

## CONCLUSÃO

Esta arquitetura de automações Python substitui completamente plataformas no-code (Make/Zapier), oferecendo:
- **Controle Total**: Lógica customizada para necessidades específicas
- **Escalabilidade**: Suporta crescimento da agência sem aumento proporcional de custo
- **Integração Profunda**: Notion como FL (sistema operacional) totalmente integrado
- **Manutenibilidade**: Código versionado, testado e documentado

**Próximos Passos**:
1. Priorizar automações críticas (Fase 1)
2. Implementar clients base (Notion, Meta Ads)
3. Deploy de scheduler em produção
4. Monitorar e iterar

---

**Responsável**: Diretor de Operações + Tech Lead
**Revisão**: Trimestral (adicionar novas automações conforme processos evoluem)
