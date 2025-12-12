# P15 – Governança, Documentação, Acessos e Segurança

## Visão Geral

Este macroprocesso organiza a governança da informação, documentação estruturada, gestão de acessos e segurança de dados da agência. Garante que conhecimento esteja centralizado, acessível e atualizado; que acessos sejam concedidos/revogados de forma controlada; e que dados sensíveis estejam protegidos.

**Objetivo central**: Transformar conhecimento tácito em conhecimento explícito (documentado), garantir que ninguém seja "ponto único de falha", proteger dados da agência e clientes, e facilitar escalabilidade (novos membros encontram tudo documentado).

---

## P15.1 – Estrutura Padronizada de Pastas e Arquivos

### Objetivo
Definir e manter uma estrutura organizada, consistente e intuitiva para armazenamento de todos os documentos, materiais e arquivos da agência, facilitando localização e evitando perda de informação.

### Momento
- Inicial: Ao estruturar operação da agência
- Contínuo: Manutenção e organização diária
- Periódico: Revisão e limpeza (trimestral)

### Gatilho
- Novo cliente fechado (criar estrutura de pastas)
- Novo projeto/campanha (criar subpastas)
- Revisão trimestral (P17.6 - Melhoria Contínua)

### Saídas
- Estrutura de pastas padrão implementada (Google Drive, Notion)
- Todos os arquivos organizados conforme padrão
- Facilidade de localização (qualquer membro encontra qualquer arquivo em <2min)

### Papéis Envolvidos
- **Founder/Diretor**: Definição da estrutura inicial
- **Todos os membros**: Seguir padrão ao salvar arquivos
- **Administrativo** (se aplicável): Revisão e limpeza periódica

### Ferramentas
- Google Drive (armazenamento de arquivos)
- Notion (documentação de processos, bases de dados)

---

### Passo a Passo

#### Tarefa 1: Definir Estrutura de Pastas do Google Drive
- **T1.1**: Estrutura raiz (nível 1):
  ```
  📁 AUTO-Marketing (Agência)
    ├── 📁 00_Administrativo
    ├── 📁 01_Clientes
    ├── 📁 02_Marketing_da_Agência
    ├── 📁 03_Financeiro
    ├── 📁 04_Equipe
    ├── 📁 05_Templates_e_Padroes
    ├── 📁 06_Treinamentos
    └── 📁 07_Backup
  ```

- **T1.2**: Subpastas de cada raiz:

  **00_Administrativo**:
  ```
  00_Administrativo/
    ├── Contratos_da_Agencia (aluguel, contabilidade, etc.)
    ├── Documentos_Legais (CNPJ, contrato social, etc.)
    ├── Fornecedores
    └── Planejamento_Estrategico
  ```

  **01_Clientes**:
  ```
  01_Clientes/
    ├── [Nome_Cliente_1]/
    │   ├── 01_Briefing
    │   ├── 02_Contratos_e_Propostas
    │   ├── 03_Estrategia_e_Pesquisa
    │   ├── 04_Campanhas
    │   │   ├── [Nome_Campanha_1]/
    │   │   │   ├── Criativos (imagens, videos)
    │   │   │   ├── Copys (textos de anuncios)
    │   │   │   └── Performance (prints, relatorios)
    │   │   └── [Nome_Campanha_2]/...
    │   ├── 05_Relatorios
    │   ├── 06_Reunioes (pautas, atas)
    │   └── 07_Materiais_Cliente (logo, fotos, guidelines)
    ├── [Nome_Cliente_2]/...
    └── _Templates_Cliente (estrutura padrão para copiar)
  ```

  **02_Marketing_da_Agência**:
  ```
  02_Marketing_da_Agencia/
    ├── Campanhas_da_Agencia
    │   ├── [Nome_Campanha]/...
    ├── Conteudo_Organico (posts, videos, scripts)
    ├── Site_e_Branding (logo, identidade, assets)
    └── Estudos_de_Caso (cases de clientes, antes/depois)
  ```

  **03_Financeiro**:
  ```
  03_Financeiro/
    ├── Notas_Fiscais
    │   ├── [Ano]/
    │   │   └── [Mes]/
    ├── Contratos_Clientes
    ├── Propostas_Comerciais
    └── DREs_e_Relatorios (planilhas, relatórios mensais)
  ```

  **04_Equipe**:
  ```
  04_Equipe/
    ├── Contratos_de_Trabalho
    ├── Avaliacoes_de_Performance
    ├── Treinamentos_Internos (gravações, materiais)
    └── Onboarding (checklists, documentos de novos membros)
  ```

  **05_Templates_e_Padroes**:
  ```
  05_Templates_e_Padroes/
    ├── Templates_de_Campanhas (estruturas prontas de Meta Ads)
    ├── Templates_de_Criativos (PSDs, Figma, Canva)
    ├── Templates_de_Copys (anúncios, LPs, e-mails)
    ├── Templates_de_Relatorios (Google Slides, Sheets)
    ├── Scripts (vendas, atendimento, qualificação)
    └── SOPs_Resumidos (versões simplificadas de P1-P17)
  ```

  **06_Treinamentos**:
  ```
  06_Treinamentos/
    ├── Gravacoes (vídeos de treinamentos internos)
    ├── Materiais_Externos (cursos, PDFs, links)
    └── Playbooks (guias de processos por papel)
  ```

  **07_Backup**:
  ```
  07_Backup/
    ├── Bases_de_Dados_Notion (exports mensais)
    ├── Campanhas_Antigas (campanhas de clientes inativos)
    └── Arquivos_Descontinuados
  ```

#### Tarefa 2: Definir Padrão de Nomeação de Arquivos
- **T2.1**: Regras de nomeação:
  - **Data no início** (se relevante): `AAAA-MM-DD_` (ex.: `2025-01-15_Relatorio_Cliente_X.pdf`)
  - **Separador**: Underscore `_` (não espaço, não hífen quando possível)
  - **Sem caracteres especiais**: Evitar `#, &, %, @, $, !` (podem quebrar automações)
  - **Descritivo**: Nome deve indicar conteúdo (ex.: `Criativo_Carrossel_Oferta_Consulta_v1.png`)
  - **Versão** (se aplicável): `_v1`, `_v2`, `_final` (ex.: `Copy_Anuncio_Lead_v3.txt`)
  - **Tudo em minúsculo ou PascalCase** (consistência): `relatorio_semanal.pdf` ou `RelatorioSemanal.pdf` (escolher 1 padrão)

- **T2.2**: Exemplos de nomeação:
  - Briefing: `2025-01-10_Briefing_ClienteX.pdf`
  - Criativo: `ClienteX_Criativo_Carrossel_Janeiro_v2.png`
  - Copy: `ClienteX_Copy_Lead_Consulta_v1.txt`
  - Relatório: `2025-01-15_Relatorio_Semanal_ClienteX.pdf`
  - Contrato: `2025-01-05_Contrato_ClienteX_Assinado.pdf`
  - Proposta: `2025-01-03_Proposta_ClienteY.pdf`

#### Tarefa 3: Criar Estrutura Padrão para Novos Clientes
- **T3.1**: Ao fechar cliente (P3, pós-contrato P13.2):
  - Copiar pasta `_Templates_Cliente` dentro de `01_Clientes/`
  - Renomear para `[Nome_Cliente]` (ex.: `Clinica_Dr_Silva`)
  - Estrutura já vem pronta (01_Briefing, 02_Contratos_e_Propostas, etc.)
- **T3.2**: Mover documentos iniciais para pastas certas:
  - Briefing → `01_Briefing/`
  - Contrato/Proposta → `02_Contratos_e_Propostas/`
  - Logo e materiais do cliente → `07_Materiais_Cliente/`

#### Tarefa 4: Definir Estrutura do Notion
- **T4.1**: Bases de dados principais (já definidas em 01_FL_NOTION_ARQUITETURA.md):
  - Clientes, Leads, Campanhas, Criativos, Tarefas, Equipe, Financeiro, Incidentes, etc.
- **T4.2**: Repositório de Conhecimento (P15.5):
  - Página raiz: `📚 Repositório de Conhecimento`
  - Subpáginas:
    - `P1-P17 (SOPs)` → Links para cada processo
    - `Templates` → Templates de documentos (propostas, contratos, relatórios, etc.)
    - `Playbooks por Papel` → Guias específicos (Gestor de Tráfego, Copywriter, CS, etc.)
    - `FAQs` → Perguntas frequentes (internas e de clientes)
    - `Glossário` → Termos técnicos (CPL, CTR, Pixel, CAPI, etc.)

#### Tarefa 5: Comunicar e Treinar Equipe
- **T5.1**: Apresentar estrutura em reunião (30min):
  - Mostrar organização do Drive (onde fica cada coisa)
  - Explicar padrão de nomeação
  - Demonstrar como salvar arquivos corretamente
- **T5.2**: Criar guia rápido (1 página, Notion):
  - "Onde salvar X?" (tabela com tipo de arquivo → pasta correta)
  - "Como nomear arquivos?" (regras + exemplos)
- **T5.3**: Estabelecer regra:
  - "Sempre salvar no Drive/Notion, nunca só no computador local"
  - "Se não sabe onde salvar, pergunte antes (não criar pasta nova aleatoriamente)"

#### Tarefa 6: Revisão e Limpeza Periódica
- **T6.1**: Trimestral (P17.6):
  - Revisar estrutura (há pastas duplicadas? Arquivos fora do lugar?)
  - Mover arquivos mal organizados para lugar certo
  - Deletar arquivos obsoletos (versões antigas, materiais de campanhas descontinuadas)
  - Fazer backup (P15.3) antes de deletar
- **T6.2**: Anual:
  - Revisão completa (estrutura ainda faz sentido? Precisa ajustar?)
  - Arquivar clientes inativos (mover para `07_Backup/Campanhas_Antigas/`)

---

### Checklist de Qualidade

- [ ] Estrutura de pastas definida (Drive + Notion)
- [ ] Padrão de nomeação documentado e comunicado
- [ ] Template de pasta de cliente criado (_Templates_Cliente)
- [ ] Equipe treinada (todos sabem onde salvar e como nomear)
- [ ] Guia rápido de organização disponível (Notion)
- [ ] Revisão periódica agendada (trimestral)
- [ ] Nenhum arquivo crítico perdido (todos estão onde deveriam estar)

---

### Erros Comuns a Evitar

- Estrutura muito complexa (muitas subpastas, dificulta localização) — manter simples
- Não comunicar padrão (cada um salva do seu jeito) — treinar e reforçar
- Permitir "pastas pessoais" soltas (fora da estrutura) — centralizar tudo
- Não fazer limpeza (acumula arquivos velhos, dificulta busca) — revisar periodicamente
- Salvar tudo no Desktop/Downloads (perda de dados, desorganização) — cultura de salvar no Drive/Notion

---

### Métricas Relacionadas

| Métrica | Fórmula/Fonte | Frequência |
|---------|---------------|------------|
| **Taxa de Adesão ao Padrão** | (Arquivos nomeados corretamente / Total arquivos novos) × 100 (amostra) | Mensal |
| **Tempo Médio de Localização** | Média(tempo para encontrar arquivo solicitado) | Ad-hoc (observação) |
| **% de Arquivos Fora do Lugar** | (Arquivos fora da estrutura / Total arquivos) × 100 (amostra) | Trimestral |

---

### Automações Python

| ID | Gatilho | Ação |
|----|---------|------|
| **A54** | Novo cliente criado (Notion) | Criar estrutura de pastas automaticamente no Drive (via API do Google Drive) |
| **A55** | Arquivo adicionado fora da estrutura (Google Drive API) | Alerta para administrativo revisar e mover |

---

### Templates Associados

- **Guia Rápido de Organização** (Notion, ver T5.2)
- **Template de Estrutura de Pasta de Cliente** (Drive, `_Templates_Cliente`)

---

### Fluxos de Exceção

| Situação | Ação |
|----------|------|
| **Arquivo crítico não encontrado** | Buscar no Drive (função de busca), verificar lixeira, verificar backups (P15.3), perguntar quem criou, prevenir: reforçar padrão |
| **Membro insiste em salvar fora do padrão** | Feedback (P14.5), explicar impacto (perda de tempo de equipe, risco de perda), se persiste: ação corretiva (parte de avaliação P14.6) |
| **Estrutura fica desatualizada** (novos tipos de arquivos não têm lugar) | Revisar estrutura (adicionar pasta nova se necessário), comunicar equipe, atualizar guia |

---

---

## P15.2 – Padrões de Nomeação (Campanhas, Conjuntos, Anúncios, Pastas)

### Objetivo
Estabelecer convenções de nomeação claras e consistentes para campanhas, conjuntos e anúncios no Meta Ads, facilitando identificação, análise de performance e colaboração entre membros da equipe.

### Momento
- Sempre que criar campanha, conjunto ou anúncio (P8.1)
- Revisão: Quando padrão não está sendo seguido

### Gatilho
- Novo cliente (definir nomeação específica do cliente)
- Build de campanha (P8.1)

### Saídas
- Todas as campanhas/conjuntos/anúncios nomeados de forma consistente
- Fácil identificação de objetivo, público, criativo e data em relatórios
- Redução de erro (ex.: pausar campanha errada)

### Papéis Envolvidos
- **Gestor de Tráfego**: Aplicar padrão ao criar campanhas
- **Founder/Diretor**: Definir padrão inicial

### Ferramentas
- Meta Ads Manager
- Notion (documentação do padrão P15.5)

---

### Passo a Passo

#### Tarefa 1: Definir Padrão de Nomeação de Campanhas
- **T1.1**: Estrutura básica (adaptar conforme necessidade):
  ```
  [ClienteAbrev]_[Objetivo]_[Funil]_[Data/Versão]
  ```
  - **ClienteAbrev**: Abreviação do nome do cliente (3-5 letras)
    - Ex.: `CLNDR` (Clínica Dr. Silva), `RESTO` (Restaurante X)
  - **Objetivo**: Objetivo da campanha no Meta
    - Ex.: `LEADS`, `CONV` (conversão), `TRAF` (tráfego), `ENGAJ` (engajamento)
  - **Funil**: Estágio do funil
    - Ex.: `TOP` (topo, cold), `MID` (meio, warm), `BOT` (fundo, hot), `RETARG` (remarketing)
  - **Data/Versão**: Mês de início ou versão de teste
    - Ex.: `JAN25`, `v1`, `v2`

- **T1.2**: Exemplos:
  - `CLNDR_LEADS_TOP_JAN25`: Campanha de leads, topo de funil, Clínica Dr. Silva, Janeiro 2025
  - `RESTO_CONV_BOT_v1`: Campanha de conversão, fundo de funil, Restaurante X, versão 1
  - `CLNDR_LEADS_RETARG_FEV25`: Remarketing de leads, Clínica Dr. Silva, Fevereiro 2025

#### Tarefa 2: Definir Padrão de Nomeação de Conjuntos
- **T2.1**: Estrutura básica:
  ```
  [Publico]_[Local]_[Idade]_[Interesse/Lookalike]_[Data/Versão]
  ```
  - **Público**: Tipo de público
    - Ex.: `BROAD` (amplo), `INT` (interesses), `LAL` (lookalike), `CUSTOM` (personalizado)
  - **Local**: Localização (se relevante)
    - Ex.: `SP` (São Paulo), `RJ`, `BR` (Brasil todo), `SP-Capital` (mais específico)
  - **Idade**: Faixa etária
    - Ex.: `25-45`, `35-55`, `18+` (todos)
  - **Interesse/Lookalike**: Interesse ou fonte do lookalike
    - Ex.: `Odontologia`, `LAL-Clientes`, `LAL-Leads`
  - **Data/Versão**: Versão de teste
    - Ex.: `v1`, `v2`, `A`, `B` (para testes A/B)

- **T2.2**: Exemplos:
  - `BROAD_SP-Capital_30-50_v1`: Público amplo, São Paulo capital, 30-50 anos, versão 1
  - `LAL-Clientes_SP_25-55_v1`: Lookalike de clientes, São Paulo, 25-55 anos, versão 1
  - `INT-Saude_BR_30-60_Odontologia_v1`: Interesses em saúde/odontologia, Brasil, 30-60 anos

#### Tarefa 3: Definir Padrão de Nomeação de Anúncios
- **T3.1**: Estrutura básica:
  ```
  [TipoCreativo]_[AnguloCopy]_[CTA]_[Versão]
  ```
  - **TipoCreativo**: Formato do criativo
    - Ex.: `IMG` (imagem), `VID` (vídeo), `CARR` (carrossel), `COLL` (coleção)
  - **AnguloCopy**: Ângulo/mensagem principal da copy
    - Ex.: `Desconto20`, `Depoimento`, `Urgencia`, `Beneficio`, `Problema`
  - **CTA**: Call to action
    - Ex.: `SaibaMais`, `Agende`, `Compre`, `Cadastre`, `Whatsapp`
  - **Versão**: Versão de teste
    - Ex.: `v1`, `v2`, `A`, `B`

- **T3.2**: Exemplos:
  - `IMG_Desconto20_Agende_v1`: Imagem, copy sobre desconto de 20%, CTA para agendar, versão 1
  - `VID_Depoimento_Whatsapp_v1`: Vídeo com depoimento, CTA para WhatsApp, versão 1
  - `CARR_Beneficios_SaibaMais_v2`: Carrossel sobre benefícios, CTA Saiba Mais, versão 2

#### Tarefa 4: Documentar Padrão
- **T4.1**: Criar página no Notion (P15.5 - Repositório de Conhecimento):
  - Título: "Padrão de Nomeação de Campanhas, Conjuntos e Anúncios"
  - Explicar estrutura (exemplos acima)
  - Tabela de abreviações (Clientes, Objetivos, Públicos, CTAs)
  - Exemplos práticos (prints de campanhas bem nomeadas)

#### Tarefa 5: Treinar Equipe
- **T5.1**: Parte do onboarding (P14.1) de Gestor de Tráfego:
  - Estudar padrão de nomeação
  - Exercício prático: nomear campanha/conjunto/anúncio de cliente fictício
- **T5.2**: Revisão em treinamento (P14.3) se houver inconsistências
- **T5.3**: QA pré-lançamento (P8.2):
  - Checklist inclui: "Nomeação segue padrão? (Sim/Não)"

#### Tarefa 6: Aplicar Consistentemente
- **T6.1**: Ao criar campanha (P8.1):
  - Seguir padrão rigorosamente
  - Se dúvida: consultar documentação (Notion P15.5)
- **T6.2**: Revisão mensal (P9.2):
  - Auditar nomeação de campanhas criadas no mês
  - Corrigir inconsistências (renomear se necessário, ou marcar para renomear em próxima otimização)

---

### Checklist de Qualidade

- [ ] Padrão de nomeação definido (campanhas, conjuntos, anúncios)
- [ ] Documentado no Notion (P15.5)
- [ ] Equipe treinada (todos sabem nomear corretamente)
- [ ] QA inclui verificação de nomeação (P8.2)
- [ ] 100% das campanhas novas seguem padrão (meta)
- [ ] Campanhas antigas renomeadas (ou marcadas para renomear)

---

### Erros Comuns a Evitar

- Nomeação inconsistente (cada gestor nomeia diferente) — estabelecer padrão único
- Padrão muito longo (nomes cortados no Meta Ads Manager) — máximo 60 caracteres
- Não documentar abreviações (ninguém lembra o que significa `CLNDR`) — manter glossário
- Não treinar novos membros (cada um inventa seu padrão) — parte obrigatória de onboarding
- Ignorar padrão em "testes rápidos" (depois vira bagunça) — sempre seguir

---

### Métricas Relacionadas

| Métrica | Fórmula/Fonte | Frequência |
|---------|---------------|------------|
| **Taxa de Adesão ao Padrão** | (Campanhas nomeadas corretamente / Total campanhas novas) × 100 | Mensal |
| **Tempo de Identificação de Campanha** | Tempo para encontrar campanha específica em relatório (observação) | Ad-hoc |

---

### Automações Python

| ID | Gatilho | Ação |
|----|---------|------|
| **A56** | Nova campanha criada (Meta API) | Verificar se nome segue padrão (regex), alertar gestor se não seguir |

---

### Templates Associados

- **Glossário de Abreviações** (Notion):
  ```
  CLIENTES:
  - CLNDR: Clínica Dr. Silva
  - RESTO: Restaurante X
  - ...

  OBJETIVOS:
  - LEADS: Geração de Leads
  - CONV: Conversão
  - TRAF: Tráfego
  - ENGAJ: Engajamento

  FUNIL:
  - TOP: Topo (cold, audiência fria)
  - MID: Meio (warm, audiência aquecida)
  - BOT: Fundo (hot, audiência quente)
  - RETARG: Remarketing

  PÚBLICOS:
  - BROAD: Amplo (sem segmentação específica)
  - INT: Interesses
  - LAL: Lookalike
  - CUSTOM: Personalizado

  CRIATIVOS:
  - IMG: Imagem
  - VID: Vídeo
  - CARR: Carrossel
  - COLL: Coleção

  CTAs:
  - SaibaMais: Saiba Mais
  - Agende: Agende Agora
  - Compre: Compre Agora
  - Cadastre: Cadastre-se
  - Whatsapp: Envie Mensagem (WhatsApp)
  ```

---

### Fluxos de Exceção

| Situação | Ação |
|----------|------|
| **Padrão não funciona para cliente específico** (ex.: múltiplas ofertas, múltiplos locais) | Adaptar padrão (criar variação), documentar exceção, comunicar equipe |
| **Nomes ficam muito longos** (cortados no Meta Ads) | Encurtar abreviações, remover campo menos importante, ou usar campo "Descrição" da campanha para detalhes adicionais |
| **Cliente quer nomeação diferente** (ex.: quer ver nome da oferta na campanha) | Negociar: explicar benefício do padrão (organização, relatórios), se cliente insiste: adaptar (mas manter lógica interna) |

---

---

## P15.3 – Backup e Recuperação de Dados

### Objetivo
Garantir que dados críticos da agência (Notion, Drive, campanhas, contratos, financeiro) estejam protegidos contra perda acidental, falhas técnicas ou ataques, com capacidade de recuperação rápida.

### Momento
- Contínuo: Backups automáticos
- Periódico: Backups manuais mensais (dados críticos)
- Emergencial: Recuperação quando necessário

### Gatilho
- Agendamento automático (mensal)
- Perda de dados identificada
- Antes de mudanças grandes (ex.: migração de sistema)

### Saídas
- Backups completos e atualizados (Notion, Drive, outros sistemas)
- Capacidade de recuperar dados em <24h
- Nenhum dado crítico perdido permanentemente

### Papéis Envolvidos
- **Administrativo/Dev**: Executar backups
- **Founder/Diretor**: Garantir que backups existem

### Ferramentas
- Google Drive (já tem backup automático Google)
- Notion (export manual mensal)
- Sistemas externos (backups de CRM, e-mails, etc.)
- Armazenamento externo (Google Drive, Dropbox, HD externo)

---

### Passo a Passo

#### Tarefa 1: Identificar Dados Críticos
- **T1.1**: Listar o que **não pode** ser perdido:
  - **Notion**:
    - Bases de dados (Clientes, Campanhas, Tarefas, Equipe, Financeiro, Incidentes)
    - Documentação (P1-P17, Repositório de Conhecimento)
  - **Google Drive**:
    - Pastas de clientes (campanhas, relatórios, contratos)
    - Financeiro (notas fiscais, DREs)
    - Templates
  - **E-mails** (Google Workspace):
    - Contratos via e-mail
    - Comunicações críticas com clientes
  - **Meta Ads**:
    - Configurações de campanhas (para recriar se conta bloquear)
    - Histórico de performance (se Meta não disponibiliza mais)
  - **Sistemas externos**:
    - CRM (se não for Notion)
    - Gateway de pagamento (histórico de cobranças)

#### Tarefa 2: Implementar Backups Automáticos

##### Google Drive:
- **T2.1**: Google Drive já tem backup nativo (versionamento, lixeira por 30 dias)
- **T2.2**: Adicional (recomendado):
  - Usar Google Takeout (mensalmente) para export completo
  - Salvar export em outro local (Dropbox, HD externo)

##### Notion:
- **T2.3**: Notion não tem backup automático externo (só interno da plataforma)
- **T2.4**: Backup manual mensal:
  - Settings → Export All Workspace Content → Format: Markdown & CSV (ou HTML)
  - Baixar ZIP e salvar em `Google Drive / 07_Backup / Bases_de_Dados_Notion / [Ano-Mes]`
- **T2.5**: Agendar tarefa recorrente (Python A57 ou manual):
  - Todo dia 1 do mês: "Fazer backup do Notion"

##### E-mails (Google Workspace):
- **T2.6**: Google Workspace já tem backup nativo (e-mails não deletam permanentemente por 30 dias)
- **T2.7**: Adicional (opcional):
  - Usar Google Takeout para export de e-mails críticos
  - Ou usar ferramenta de backup de e-mail (ex.: Backupify, Spinbackup)

##### Meta Ads:
- **T2.8**: Meta não permite backup automático de campanhas via API (limitação da plataforma)
- **T2.9**: Backup manual trimestral (ou antes de mudanças grandes):
  - Exportar configurações de campanhas (CSV de campanhas, conjuntos, anúncios)
  - Salvar em `Google Drive / 01_Clientes / [Cliente] / 04_Campanhas / _Backup`
  - Ou usar ferramenta de terceiros (ex.: Supermetrics, exportar para Google Sheets)

#### Tarefa 3: Testar Recuperação (Anual)
- **T3.1**: Uma vez por ano, simular perda de dados:
  - Deletar página de teste no Notion
  - Recuperar do backup (restaurar ZIP, importar)
  - Verificar: dados voltaram? Integridade OK?
- **T3.2**: Se falhar:
  - Revisar processo de backup (está funcionando?)
  - Ajustar e testar novamente

#### Tarefa 4: Documentar Procedimento de Recuperação
- **T4.1**: Criar página no Notion (P15.5):
  - Título: "Procedimento de Recuperação de Dados"
  - Passo a passo:
    1. Identificar o que foi perdido
    2. Localizar backup mais recente (onde está salvo)
    3. Restaurar:
       - **Notion**: Importar ZIP (Settings → Import)
       - **Google Drive**: Restaurar da lixeira (30 dias) ou de backup Takeout
       - **Meta Ads**: Recriar campanhas manualmente usando CSV exportado
    4. Verificar integridade (tudo voltou? Algo falta?)
    5. Documentar incidente (P12.8)

#### Tarefa 5: Armazenar Backups com Segurança
- **T5.1**: Princípio 3-2-1:
  - **3 cópias** dos dados (original + 2 backups)
  - **2 mídias diferentes** (ex.: Google Drive + Dropbox, ou Drive + HD externo)
  - **1 offsite** (fora do local físico, ex.: nuvem)
- **T5.2**: Proteger com senha (se dados sensíveis):
  - Zipar backups com senha
  - Senha armazenada em cofre (ex.: 1Password, Bitwarden)

#### Tarefa 6: Revisar Backups Trimestralmente
- **T6.1**: A cada 3 meses (P17.6):
  - Verificar se backups estão sendo executados
  - Verificar espaço de armazenamento (não está cheio?)
  - Testar integridade (abrir backup, verificar se abre corretamente)

---

### Checklist de Qualidade

- [ ] Dados críticos identificados (lista completa)
- [ ] Backups automáticos implementados (Google Drive nativo, Notion manual mensal)
- [ ] Backups armazenados em local seguro (3-2-1)
- [ ] Procedimento de recuperação documentado (P15.5)
- [ ] Teste de recuperação realizado (anual, bem-sucedido)
- [ ] Revisão trimestral de backups (agendada e executada)

---

### Erros Comuns a Evitar

- Assumir que "nuvem faz backup automático" (não 100% garantido) — fazer backup adicional
- Não testar recuperação (descobrir que backup não funciona quando precisar) — testar anualmente
- Backup só em 1 lugar (se aquele lugar falha, perde tudo) — princípio 3-2-1
- Backups muito antigos (perda de dados recentes) — mensal no mínimo
- Não documentar procedimento (em crise, ninguém sabe como recuperar) — documentar claramente

---

### Métricas Relacionadas

| Métrica | Fórmula/Fonte | Frequência |
|---------|---------------|------------|
| **Taxa de Sucesso de Backup** | (Backups executados / Backups agendados) × 100 | Mensal |
| **Idade do Backup Mais Recente** | Dias desde último backup | Mensal |
| **Tempo de Recuperação (RTO)** | Tempo desde perda até restauração completa | Por incidente (meta: <24h) |
| **Taxa de Sucesso de Recuperação** | (Testes de recuperação bem-sucedidos / Total testes) × 100 | Anual |

---

### Automações Python

| ID | Gatilho | Ação |
|----|---------|------|
| **A57** | Dia 1 de cada mês (cron) | Alerta para administrativo fazer backup manual do Notion + Google Takeout |
| **A58** | Backup salvo (detectar novo arquivo em pasta 07_Backup/) | Verificar tamanho do arquivo (se muito pequeno, alerta de possível erro), notificar conclusão |

---

### Templates Associados

- **Checklist de Backup Mensal**:
  ```
  BACKUP MENSAL: [Mês/Ano]
  Data de execução: [Data]
  Responsável: [Nome]

  NOTION:
  - [ ] Export All Workspace Content (Markdown & CSV)
  - [ ] Salvar ZIP em `Drive / 07_Backup / Bases_de_Dados_Notion / [Ano-Mes]`
  - [ ] Verificar tamanho do arquivo (>100MB esperado)

  GOOGLE DRIVE (opcional):
  - [ ] Google Takeout (Drive completo)
  - [ ] Salvar em Dropbox / HD externo

  META ADS (trimestral):
  - [ ] Exportar campanhas de cada cliente (CSV)
  - [ ] Salvar em `Drive / 01_Clientes / [Cliente] / 04_Campanhas / _Backup`

  E-MAIL (opcional):
  - [ ] Google Takeout (Gmail) ou ferramenta de backup

  VERIFICAÇÃO:
  - [ ] Todos os backups salvos com sucesso
  - [ ] Tamanhos dos arquivos OK (não corrompidos)
  - [ ] Backups armazenados em ≥2 locais (3-2-1)

  OBSERVAÇÕES:
  [Qualquer problema ou nota relevante]
  ```

- **Procedimento de Recuperação de Dados** (Notion, ver T4.1)

---

### Fluxos de Exceção

| Situação | Ação |
|----------|------|
| **Perda de dados críticos** (ex.: Notion deletado acidentalmente) | Não entrar em pânico, localizar backup mais recente, restaurar seguindo procedimento (P15.5), verificar o que falta (comparar com memória/registros), documentar incidente (P12.8), revisar processo para prevenir |
| **Backup falha** (ex.: erro de export do Notion) | Tentar novamente, verificar causa (espaço insuficiente? Bug?), se persistir: contatar suporte Notion, usar método alternativo (copiar bases manualmente) |
| **Backup corrompido** (não abre) | Usar backup anterior, investigar causa (download incompleto? Corrupção de arquivo?), melhorar processo (verificação de integridade pós-backup) |
| **Armazenamento cheio** (sem espaço para novos backups) | Deletar backups mais antigos (manter últimos 12 meses), aumentar espaço (upgrade de plano), ou usar armazenamento adicional |

---

---

## P15.4 – Gestão de Acessos e Permissões

### Objetivo
Controlar quem tem acesso a quais sistemas, ferramentas e dados da agência, garantindo segurança (mínimo privilégio necessário) e facilitando onboarding/offboarding.

### Momento
- Onboarding (P14.1): Conceder acessos
- Mudança de papel (P14.6 - promoção): Ajustar permissões
- Offboarding (P14.7): Revogar acessos
- Revisão trimestral (P17.6): Auditar acessos

### Gatilho
- Novo membro contratado
- Membro saindo
- Mudança de responsabilidades
- Revisão de segurança (trimestral)

### Saídas
- Todos os acessos documentados (quem tem acesso a quê)
- Nenhum acesso desnecessário (princípio do mínimo privilégio)
- Remoção de acessos imediata ao sair (segurança)
- Auditoria de acessos atualizada

### Papéis Envolvidos
- **Administrativo/Founder**: Conceder e revogar acessos
- **Gestor Direto**: Solicitar acessos necessários para membro

### Ferramentas
- Google Workspace Admin (e-mails, Drive)
- Notion Admin (workspace)
- Meta Business Manager (contas de anúncios, páginas)
- CRM, ferramentas de design, etc.
- Notion (Base de Dados: Equipe - campo "Acessos")

---

### Passo a Passo

#### Tarefa 1: Mapear Todos os Sistemas da Agência
- **T1.1**: Listar sistemas e ferramentas:
  - **Essenciais**:
    - Google Workspace (e-mail, Drive, Calendar)
    - Notion
    - Meta Business Manager (Contas de Anúncios, Páginas, Pixel)
    - WhatsApp Business (se usado para atendimento)
  - **Operacionais**:
    - CRM (se externo)
    - Ferramentas de design (Canva, Adobe, Figma)
    - Plataformas de landing page (Unbounce, Leadpages, etc.)
    - Google Analytics
  - **Financeiros**:
    - Sistema bancário (online banking)
    - Gateway de pagamento (PagSeguro, Stripe, etc.)
    - Sistema de emissão de NF
  - **Administrativos**:
    - Plataforma de RH (se houver)
    - Ferramentas de gestão de senha (1Password, Bitwarden)

#### Tarefa 2: Definir Níveis de Acesso por Papel
- **T2.1**: Para cada papel (P14.2), definir quais acessos precisa:

  **Founder/Diretor**:
  - Admin completo em tudo (Google Workspace, Notion, Meta BM, Bancário, etc.)

  **Gestor de Tráfego**:
  - E-mail corporativo (Google Workspace)
  - Notion (editor, acesso a bases de Clientes, Campanhas, Tarefas)
  - Meta Business Manager:
    - Admin de contas de anúncios dos clientes atribuídos
    - Editor de Páginas (se gerenciar)
    - Visualizador de Pixel (para configurar)
  - Google Analytics (visualizador)
  - Ferramentas de design (se criar criativos básicos)

  **Copywriter/Designer**:
  - E-mail corporativo
  - Notion (editor, acesso a bases de Campanhas, Criativos, Tarefas)
  - Drive (acesso a pastas de clientes)
  - Ferramentas de design (Canva Pro, Adobe Creative Cloud, Figma)
  - Meta BM (opcional, só para visualizar anúncios publicados)

  **CS/Atendimento**:
  - E-mail corporativo
  - Notion (editor, acesso a Clientes, Tarefas, Relatórios)
  - WhatsApp Business (admin ou editor)
  - CRM (se externo)
  - Meta BM (visualizador, para ver performance e gerar relatórios)

  **Closer/SDR**:
  - E-mail corporativo
  - Notion (editor, acesso a Leads, Tarefas, Propostas)
  - CRM (se externo)
  - Ferramenta de agendamento (Calendly, Google Calendar compartilhado)

  **Financeiro**:
  - E-mail corporativo
  - Notion (editor, acesso a Financeiro, Clientes, Contratos, Cobranças)
  - Sistema bancário (visualizador ou operador, conforme necessidade)
  - Gateway de pagamento
  - Sistema de emissão de NF

- **T2.2**: Documentar em tabela (Notion P15.5):
  | Sistema/Ferramenta | Founder | Gestor Tráfego | Copy/Design | CS | Closer | Financeiro |
  |--------------------|---------|----------------|-------------|----|---------| -----------|
  | Google Workspace | Admin | Usuário | Usuário | Usuário | Usuário | Usuário |
  | Notion | Admin | Editor | Editor | Editor | Editor | Editor |
  | Meta BM | Admin | Admin (contas clientes) | Visualizador | Visualizador | - | - |
  | Ferramentas Design | - | - | Admin | - | - | - |
  | WhatsApp Business | Admin | Visualizador | - | Admin | - | - |
  | Bancário | Admin | - | - | - | - | Operador |
  | Gateway Pagamento | Admin | - | - | - | - | Operador |

#### Tarefa 3: Conceder Acessos no Onboarding (P14.1)
- **T3.1**: Checklist de acessos (parte de P14.1 - Tarefa 1.2):
  - Criar e-mail corporativo (Google Workspace)
  - Adicionar ao Notion (workspace, conceder permissões conforme papel)
  - Adicionar ao Meta Business Manager:
    - Se Gestor: Admin de contas de clientes atribuídos
    - Se CS/Copy/Design: Visualizador ou Editor conforme necessidade
  - Adicionar a ferramentas específicas (Canva, CRM, WhatsApp, etc.)
  - Compartilhar pastas do Drive (conforme papel)
  - Fornecer credenciais (senhas temporárias, instruir para trocar)
  - Configurar 2FA (autenticação de dois fatores) em sistemas críticos

- **T3.2**: Registrar acessos no Notion:
  - Base **Equipe** → Campo "Acessos" (multi-select):
    - Ex.: `Google Workspace`, `Notion`, `Meta BM - Contas A, B, C`, `Canva Pro`, `WhatsApp Business`

#### Tarefa 4: Revogar Acessos no Offboarding (P14.7)
- **T4.1**: Checklist de remoção de acessos (parte de P14.7 - Tarefa 4):
  - **Imediato** (no último dia ou antes, se justa causa):
    - Suspender e-mail corporativo (Google Workspace) ou remover usuário
    - Remover do Notion (workspace)
    - Remover de Meta Business Manager (todas as contas, páginas, pixels)
    - Remover de WhatsApp Business
    - Revogar acesso ao Drive (ou remover de pastas sensíveis)
    - Remover de CRM
    - Remover de ferramentas de design (se licença era da agência)
    - Remover de sistemas financeiros (bancário, gateway, NF)
    - Trocar senhas compartilhadas (se membro tinha acesso a senhas de clientes)
  - **Opcional** (se membro saiu em bons termos):
    - Manter acesso a e-mail por 7-14 dias (para transição de comunicações), depois arquivar/remover
    - Transferir propriedade de arquivos no Drive (de membro para gestor/founder)

- **T4.2**: Registrar remoção no Notion:
  - Equipe → Status = "Inativo"
  - Campo "Acessos" → Limpar (ou marcar como "Revogados em [Data]")

#### Tarefa 5: Auditar Acessos Trimestralmente
- **T5.1**: A cada 3 meses (P17.6):
  - Revisar lista de usuários em cada sistema:
    - Google Workspace: Admin Console → Usuários → Verificar quem está ativo
    - Notion: Settings → Members → Verificar lista
    - Meta BM: Business Settings → People → Verificar pessoas com acesso
    - Outras ferramentas (Canva, CRM, etc.)
  - Comparar com lista de equipe ativa (Notion - Equipe, Status = Ativo)
  - Identificar discrepâncias:
    - Alguém inativo ainda tem acesso? → Revogar
    - Alguém ativo não tem acesso necessário? → Conceder
    - Alguém tem acesso excessivo (além do papel)? → Reduzir (princípio do mínimo privilégio)

- **T5.2**: Revisar permissões de Admin:
  - Quem tem Admin completo? (Google, Notion, Meta BM)
  - Necessário? Ou pode ser reduzido?
  - **Regra**: Apenas Founder/Diretor deve ter Admin completo (exceção: CTO/Dev se houver)

#### Tarefa 6: Gestão de Senhas
- **T6.1**: Implementar cofre de senhas (1Password, Bitwarden, LastPass):
  - Armazenar senhas de sistemas compartilhados (ex.: Meta BM, CRM, ferramentas)
  - Organizar em "vaults" (cofres) por papel:
    - Ex.: "Gestor de Tráfego" (senhas de contas de Meta Ads)
    - Ex.: "CS" (senhas de WhatsApp Business, CRM)
  - Conceder acesso ao vault conforme papel
  - Revogar acesso ao sair (P14.7)

- **T6.2**: Política de senhas:
  - Senhas fortes (mínimo 12 caracteres, mix de letras/números/símbolos)
  - Não reutilizar senhas (cada sistema tem senha única)
  - Trocar senhas críticas a cada 6 meses (ou imediatamente após saída de membro que tinha acesso)
  - Nunca compartilhar senhas via WhatsApp/e-mail (usar cofre de senhas)

---

### Checklist de Qualidade

- [ ] Todos os sistemas e ferramentas mapeados
- [ ] Níveis de acesso por papel definidos (tabela)
- [ ] Acessos concedidos corretamente no onboarding (P14.1)
- [ ] Acessos revogados imediatamente no offboarding (P14.7)
- [ ] Auditoria trimestral de acessos agendada e executada
- [ ] Cofre de senhas implementado (1Password/Bitwarden)
- [ ] 2FA habilitado em sistemas críticos (Google, Meta, bancário)
- [ ] Princípio do mínimo privilégio aplicado (ninguém tem acesso desnecessário)

---

### Erros Comuns a Evitar

- Não revogar acessos ao sair (risco de sabotagem, vazamento) — revogar imediatamente
- Dar acesso Admin para todos (risco de erro/sabotagem) — mínimo privilégio
- Não auditar (acessos ficam desatualizados, ex-membros ainda têm acesso) — auditar trimestralmente
- Compartilhar senhas via WhatsApp/e-mail (inseguro) — usar cofre de senhas
- Não habilitar 2FA (contas vulneráveis a hacking) — obrigatório em sistemas críticos

---

### Métricas Relacionadas

| Métrica | Fórmula/Fonte | Frequência |
|---------|---------------|------------|
| **Taxa de Conformidade de Acessos** | (Acessos corretos / Total acessos auditados) × 100 | Trimestral |
| **Tempo de Remoção de Acesso** (Offboarding) | Horas entre saída e remoção completa de acessos | Por offboarding (meta: <4h) |
| **% de Sistemas com 2FA** | (Sistemas com 2FA / Total sistemas críticos) × 100 | Trimestral (meta: 100%) |
| **Incidentes de Acesso Não Autorizado** | Número de tentativas de acesso por ex-membros ou não autorizados | Mensal (meta: 0) |

---

### Automações Python

| ID | Gatilho | Ação |
|----|---------|------|
| **A59** | Novo membro criado (Notion - Equipe, Status = Ativo) | Criar checklist de concessão de acessos, alerta para administrativo |
| **A60** | Membro → Status = Inativo (Notion - Equipe) | Criar checklist de remoção de acessos, alerta urgente para administrativo (revogar em <4h) |
| **A61** | Fim do trimestre | Gerar relatório de auditoria de acessos (comparar Notion vs. Google Workspace vs. Meta BM) |

---

### Templates Associados

- **Checklist de Concessão de Acessos** (Onboarding P14.1, ver T3.1)
- **Checklist de Remoção de Acessos** (Offboarding P14.7, ver T4.1)
- **Tabela de Acessos por Papel** (Notion, ver T2.2)
- **Relatório de Auditoria de Acessos**:
  ```
  AUDITORIA DE ACESSOS: [Trimestre/Ano]
  Data: [Data]
  Responsável: [Nome]

  SISTEMAS AUDITADOS:
  - [ ] Google Workspace
  - [ ] Notion
  - [ ] Meta Business Manager
  - [ ] WhatsApp Business
  - [ ] CRM
  - [ ] Ferramentas de Design
  - [ ] Sistema Bancário
  - [ ] Gateway de Pagamento
  - [ ] Outros: [Listar]

  DISCREPÂNCIAS ENCONTRADAS:
  | Pessoa | Sistema | Problema | Ação Tomada |
  |--------|---------|----------|-------------|
  | [Nome] | Google Workspace | Inativo mas tem acesso | Removido em [Data] |
  | [Nome] | Meta BM | Acesso desnecessário (não trabalha mais com cliente) | Revogado em [Data] |

  ESTATÍSTICAS:
  - Total de usuários ativos (Equipe): [N]
  - Total de acessos auditados: [N]
  - Discrepâncias encontradas: [N]
  - Taxa de conformidade: [%]
  - Ações corretivas tomadas: [N]

  RECOMENDAÇÕES:
  [Sugestões de melhorias de segurança, processos, etc.]

  PRÓXIMA AUDITORIA: [Data]
  ```

---

### Fluxos de Exceção

| Situação | Ação |
|----------|------|
| **Ex-membro tenta acessar sistema** | Alerta de segurança, confirmar que acessos foram revogados (deveria ser impossível), investigar brecha (senha compartilhada? Acesso não revogado?), corrigir, trocar senhas |
| **Membro perde acesso crítico** (ex.: senha esquecida, 2FA não funciona) | Reset de senha (via Admin), desabilitar 2FA temporariamente (se necessário), reabilitar após recuperação, documentar para prevenir |
| **Auditoria identifica muitos acessos desnecessários** (>10%) | Revisão completa de processos de onboarding/offboarding (P14.1, P14.7), treinamento de equipe, implementar automações (A59, A60, A61) para prevenir |
| **Sistema crítico não suporta 2FA** | Mitigar risco: senha muito forte, trocar frequentemente, limitar acesso (só quem realmente precisa), considerar migrar para sistema que suporta 2FA |

---

---

## P15.5 – Repositório de Conhecimento (Playbooks, SOPs, Templates)

### Objetivo
Centralizar, organizar e manter atualizada toda a documentação da agência (processos, templates, scripts, playbooks), transformando conhecimento tácito em explícito e facilitando acesso rápido para toda equipe.

### Momento
- Contínuo: Atualização de documentação quando processos mudam
- Periódico: Revisão e melhoria (trimestral P17.6)
- Reativo: Criar documentação quando gap é identificado (P12.8, P14.3)

### Gatilho
- Novo processo criado
- Processo existente modificado
- Gap de documentação identificado (membro não sabe como fazer X)
- Revisão trimestral (P17.6)

### Saídas
- 100% dos processos documentados (P1-P17)
- Todos os templates, scripts e padrões acessíveis (Notion)
- Nenhum conhecimento crítico apenas "na cabeça" de uma pessoa
- Facilidade de onboarding (novo membro lê documentação e aprende)

### Papéis Envolvidos
- **Founder/Diretor**: Curadoria, garantir que documentação existe
- **Gestores**: Manter documentação de suas áreas atualizada
- **Todos os membros**: Consultar e sugerir melhorias

### Ferramentas
- Notion (página raiz: `📚 Repositório de Conhecimento`)
- Google Drive (templates de arquivos: PSDs, Figma, etc.)

---

### Passo a Passo

#### Tarefa 1: Estruturar Repositório de Conhecimento (Notion)
- **T1.1**: Criar página raiz (Notion):
  ```
  📚 REPOSITÓRIO DE CONHECIMENTO
  ---
  "Todo o conhecimento da agência em um só lugar"

  📂 SEÇÕES:
  1. 📋 Processos (SOPs - P1 a P17)
  2. 📄 Templates
  3. 📘 Playbooks por Papel
  4. ❓ FAQs (Perguntas Frequentes)
  5. 📖 Glossário de Termos
  6. 🔗 Links Úteis
  ```

- **T1.2**: Subpáginas detalhadas:

  **1. Processos (SOPs - P1 a P17)**:
  - Links para cada processo:
    - P1 – Estratégia & Posicionamento
    - P2 – Aquisição de Clientes
    - P3 – Vendas & Fechamento
    - ... (todos até P17)
  - Cada link aponta para página completa do processo (já criadas neste manual operacional)

  **2. Templates**:
  - Subpáginas por tipo:
    - **Comercial**:
      - Template de Proposta Comercial (P13.1)
      - Template de Contrato (P13.2)
    - **Operacional**:
      - Template de Briefing de Cliente (P4.1)
      - Template de Estratégia de Campanha (P5.1)
      - Checklist de QA Pré-Lançamento (P8.2)
      - Template de Relatório Semanal (P10.1)
    - **Criativos e Copys**:
      - Templates de Copys de Anúncios (P6.1)
      - Templates de Criativos (links para Drive: PSDs, Figma, Canva)
      - Scripts de Vídeo/UGC (P6.3)
    - **Comunicação com Cliente**:
      - Scripts de Call de Vendas (P3.3)
      - Templates de WhatsApp (onboarding, crises, follow-up)
      - Templates de E-mail (relatórios, cobranças, crises)
    - **Internos**:
      - Template de Reunião 1:1 (P14.5)
      - Template de Avaliação de Performance (P14.6)
      - Template de Entrevista de Saída (P14.7)

  **3. Playbooks por Papel**:
  - Guias específicos para cada papel (resumo dos processos relevantes):
    - **Playbook do Gestor de Tráfego**:
      - O que você faz: Resumo (P5, P7, P8, P9, P12.1, P12.4, P12.6)
      - Rotina diária: Checklist (P9.1)
      - Rotina semanal: Checklist (P9.2)
      - Como criar campanha: Passo a passo simplificado (P8.1 + P8.2)
      - Como resolver crises: Anúncio reprovado (P12.1), Queda de performance (P12.4)
      - Ferramentas principais: Meta Ads, Notion, Analytics
    - **Playbook do Copywriter**:
      - O que você faz: Resumo (P6.1)
      - Como criar copy: Processo (P6.1), Templates, Melhores práticas
      - Como receber briefing: P4.1, P5
      - Como enviar para aprovação: P6.7
    - **Playbook do Designer**:
      - O que você faz: Resumo (P6.2, P6.3)
      - Como criar criativos: Processo, Templates (Drive), Padrões de design
      - Onde salvar arquivos: P15.1
    - **Playbook do CS/Atendimento**:
      - O que você faz: Resumo (P10, P11)
      - Como atender cliente: Scripts, SLA de resposta (P10.5)
      - Como fazer relatório: P10.1
      - Como detectar churn: P11.3
    - **Playbook do Closer/SDR**:
      - O que você faz: Resumo (P2, P3)
      - Como qualificar lead: P3.1
      - Como fazer call: P3.3
      - Como enviar proposta: P13.1

  **4. FAQs (Perguntas Frequentes)**:
  - Internas (para equipe):
    - "Onde salvo arquivos de cliente?" → P15.1
    - "Como nomeio campanhas?" → P15.2
    - "Como faço backup?" → P15.3
    - "Esqueci minha senha, como recupero?" → P15.4
    - "Como pedir férias/folga?" → (definir processo, se aplicável)
  - De Clientes (para CS responder):
    - "Quanto tempo leva para ver resultados?" → (resposta padrão)
    - "Por que meu anúncio foi reprovado?" → (explicação + link para políticas Meta)
    - "Posso pausar contrato?" → (explicar cláusula de contrato P13.2)
    - "Como funciona o relatório?" → (explicar estrutura P10.1)

  **5. Glossário de Termos**:
  - Lista alfabética de termos técnicos:
    - **Ad Account**: Conta de Anúncios no Meta Business Manager
    - **BM**: Business Manager (Meta)
    - **CAPI**: Conversions API (Meta)
    - **CPL**: Custo por Lead
    - **CTR**: Click-Through Rate (Taxa de Cliques)
    - **CPC**: Custo por Clique
    - **CPM**: Custo por Mil Impressões
    - **Pixel**: Código de rastreamento do Meta instalado no site
    - **UTM**: Parâmetros de rastreamento de links
    - **LAL**: Lookalike Audience (Público Semelhante)
    - **Retargeting**: Remarketing (alcançar pessoas que já interagiram)
    - **QA**: Quality Assurance (Garantia de Qualidade)
    - **SOP**: Standard Operating Procedure (Procedimento Operacional Padrão)
    - **NPS**: Net Promoter Score (índice de satisfação)
    - **Churn**: Taxa de cancelamento de clientes
    - **MRR**: Monthly Recurring Revenue (Receita Recorrente Mensal)
    - **LTV**: Lifetime Value (Valor Vitalício do Cliente)
    - (adicionar mais conforme necessário)

  **6. Links Úteis**:
  - **Meta/Facebook**:
    - Meta Business Help Center: https://www.facebook.com/business/help
    - Políticas de Anúncios: https://www.facebook.com/policies/ads
    - Meta Blueprint (cursos): https://www.facebook.com/business/learn
    - Events Manager: https://business.facebook.com/events_manager2/
  - **Google**:
    - Google Analytics: https://analytics.google.com
    - Google Tag Manager: https://tagmanager.google.com
  - **Ferramentas Internas**:
    - Notion Workspace: [link]
    - Google Drive da Agência: [link]
    - Meta Business Manager: https://business.facebook.com
  - **Aprendizado**:
    - Hotmart (cursos): [links específicos]
    - YouTube (canais recomendados): [lista]
  - **Suporte**:
    - Contato do Contador: [e-mail/telefone]
    - Suporte Técnico (Dev/TI): [contato]

#### Tarefa 2: Popular Repositório (Inicial)
- **T2.1**: Transferir SOPs (P1-P17):
  - Criar páginas no Notion para cada processo
  - Copiar conteúdo deste manual operacional (markdown → Notion)
  - Formatar (títulos, listas, tabelas)
- **T2.2**: Adicionar templates:
  - Criar páginas com templates (ou embeds de documentos do Drive)
  - Linkar templates relevantes em cada SOP
- **T2.3**: Criar playbooks por papel:
  - Resumir processos relevantes para cada papel
  - Adicionar checklists práticas
- **T2.4**: Popular FAQs:
  - Listar perguntas frequentes (coletar de equipe + histórico de dúvidas)
  - Escrever respostas claras
- **T2.5**: Criar glossário:
  - Listar termos técnicos usados na agência
  - Definir cada termo (1-2 frases)

#### Tarefa 3: Comunicar e Treinar Equipe
- **T3.1**: Apresentar Repositório em reunião (30min):
  - Tour pelo Notion (mostrar estrutura)
  - Como buscar informação (função de busca do Notion, índice)
  - Expectativa: "Sempre que tiver dúvida, consulte o Repositório antes de perguntar"
- **T3.2**: Adicionar ao onboarding (P14.1):
  - Dia 1: Tour pelo Repositório (T2 de P14.1)
  - Tarefa: Ler playbook do seu papel
- **T3.3**: Cultura de documentação:
  - "Se você descobriu algo que não está documentado, documente."
  - "Se você teve dúvida, adicione no FAQ para próximos não terem."

#### Tarefa 4: Manter Atualizado (Contínuo)
- **T4.1**: Sempre que processo muda:
  - Atualizar SOP correspondente no Notion
  - Comunicar equipe ("SOP P8.2 foi atualizado, por favor leiam")
- **T4.2**: Sempre que novo template é criado:
  - Adicionar em "Templates" (Notion ou Drive)
  - Linkar em SOP relevante
- **T4.3**: Sempre que nova dúvida surge (recorrente):
  - Adicionar em FAQs com resposta clara

#### Tarefa 5: Revisar e Melhorar (Trimestral - P17.6)
- **T5.1**: Revisão de SOPs:
  - Ler cada processo (P1-P17)
  - Ainda está correto? Mudou algo?
  - Está claro? Ou confuso?
  - Atualizar conforme necessário
- **T5.2**: Revisão de Templates:
  - Templates ainda são usados?
  - Precisam de atualização (ex.: novo layout de relatório)?
  - Há templates faltando (equipe criou informalmente)?
- **T5.3**: Revisão de Playbooks:
  - Playbooks refletem realidade do papel?
  - Membros seguem playbooks? Ou há disconnect?
  - Atualizar com feedback de equipe
- **T5.4**: Revisão de FAQs:
  - Adicionar novas perguntas frequentes
  - Atualizar respostas (se mudou algo)
- **T5.5**: Revisão de Glossário:
  - Adicionar novos termos (se surgiram)
  - Clarificar definições (se houver confusão)

#### Tarefa 6: Coletar Feedback
- **T6.1**: Perguntar à equipe (trimestral):
  - "Vocês conseguem encontrar informações facilmente no Repositório?"
  - "O que está faltando?"
  - "O que está confuso ou desatualizado?"
- **T6.2**: Implementar melhorias com base em feedback

---

### Checklist de Qualidade

- [ ] Repositório estruturado (Notion) com 6 seções principais
- [ ] 100% dos SOPs (P1-P17) documentados e acessíveis
- [ ] Templates centralizados (Notion + Drive) e linkados em SOPs
- [ ] Playbooks por papel criados (resumo prático para cada papel)
- [ ] FAQs populadas (internas + de clientes)
- [ ] Glossário de termos completo
- [ ] Equipe treinada (todos sabem como usar Repositório)
- [ ] Cultura de documentação estabelecida ("se não está documentado, não existe")
- [ ] Revisão trimestral agendada e executada (P17.6)

---

### Erros Comuns a Evitar

- Documentação existe mas ninguém usa (não foi comunicada, difícil de acessar) — treinar e reforçar uso
- Documentação desatualizada (processos mudam, docs não) — revisar trimestralmente
- Documentação muito complexa (ninguém lê, muito longo) — ser conciso, usar checklists
- Só Founder sabe onde está documentação (centralização do conhecimento) — descentralizar, todos acessam
- Não coletar feedback (docs não melhoram) — perguntar à equipe o que falta/confunde

---

### Métricas Relacionadas

| Métrica | Fórmula/Fonte | Frequência |
|---------|---------------|------------|
| **% de Processos Documentados** | (Processos com SOP / Total processos) × 100 | Trimestral (meta: 100%) |
| **Taxa de Uso do Repositório** | (Membros que consultaram no mês / Total membros) × 100 | Mensal |
| **Clareza de Documentação** (Pesquisa) | "De 0 a 10, quão fácil é encontrar info no Repositório?" | Trimestral |
| **Tempo Médio de Atualização de SOP** | Dias entre mudança de processo e atualização de doc | Por atualização (meta: <7 dias) |

---

### Automações Python

| ID | Gatilho | Ação |
|----|---------|------|
| **A62** | Processo atualizado (Notion - página de SOP editada) | Notificar equipe (e-mail/Slack): "SOP [Nome] foi atualizado" |
| **A63** | Fim do trimestre | Alerta para Founder/Gestor revisar Repositório (checklist de revisão) |

---

### Templates Associados

- **Estrutura do Repositório de Conhecimento** (Notion, ver T1.1 e T1.2)
- **Template de Playbook por Papel**:
  ```
  # PLAYBOOK: [Nome do Papel]

  ## Visão Geral
  [1-2 parágrafos: O que você faz, por que é importante]

  ## Processos Principais
  [Lista de SOPs relevantes com links]
  - P[X]: [Nome do Processo]
  - P[Y]: [Nome do Processo]

  ## Rotina Diária
  [Checklist do que fazer todo dia]
  - [ ] [Tarefa 1]
  - [ ] [Tarefa 2]

  ## Rotina Semanal
  [Checklist do que fazer toda semana]
  - [ ] [Tarefa 1]
  - [ ] [Tarefa 2]

  ## Como Fazer [Tarefa Principal]
  [Passo a passo simplificado da tarefa mais comum]
  1. [Passo 1]
  2. [Passo 2]
  3. [Passo 3]

  ## Ferramentas que Você Usa
  [Lista de ferramentas + para que serve cada uma]
  - [Ferramenta 1]: [Para que serve]
  - [Ferramenta 2]: [Para que serve]

  ## Dúvidas Frequentes
  [FAQs específicos do papel]
  - **Pergunta 1?** Resposta.
  - **Pergunta 2?** Resposta.

  ## Contatos Importantes
  - Seu Gestor: [Nome]
  - Suporte Técnico: [Nome/Contato]
  - [Outros contatos relevantes]
  ```

---

### Fluxos de Exceção

| Situação | Ação |
|----------|------|
| **Membro não encontra informação** (mesmo estando documentada) | Melhorar indexação (adicionar em múltiplos lugares, melhorar busca), treinar uso de busca do Notion, adicionar em FAQ com link para doc |
| **Documentação fica muito longa** (ninguém lê) | Resumir (criar versão "Quick Start"), usar checklists visuais, adicionar vídeos (Loom) para processos complexos |
| **Equipe não atualiza documentação** (processos mudam, docs não) | Tornar parte de avaliação (P14.6): "Você manteve documentação atualizada?", criar automação (A62), reforçar cultura |
| **Informação crítica só está "na cabeça" de 1 pessoa** | Priorizar documentação urgente (shadowing P14.1 + registrar conhecimento), criar redundância (2+ pessoas conhecem cada processo crítico) |

---

---

## Integração de P15 com Outros Processos

| Processo | Integração |
|----------|------------|
| **P1-P17 (Todos)** | Documentados em P15.5 (Repositório de Conhecimento) |
| **P4 (Onboarding Cliente)** | Criar estrutura de pastas (P15.1) ao fechar cliente |
| **P8 (Implementação)** | Seguir padrão de nomeação (P15.2) ao criar campanhas |
| **P12 (Crises)** | Backup (P15.3) permite recuperação de dados perdidos |
| **P14.1 (Onboarding Membro)** | Conceder acessos (P15.4), estudar Repositório (P15.5) |
| **P14.3 (Treinamento)** | Repositório (P15.5) é fonte de aprendizado assíncrono |
| **P14.7 (Offboarding)** | Revogar acessos (P15.4), transferir conhecimento (documentar em P15.5) |
| **P17 (Qualidade/Melhoria)** | Revisão trimestral de documentação (P15.5), auditoria de acessos (P15.4) |

---

## Métricas Consolidadas de P15

| Métrica | Fórmula/Fonte | Frequência | Meta |
|---------|---------------|------------|------|
| **Taxa de Adesão ao Padrão de Organização** | (Arquivos bem organizados / Total) × 100 | Trimestral | >95% |
| **Taxa de Adesão ao Padrão de Nomeação** | (Campanhas nomeadas corretamente / Total) × 100 | Mensal | >95% |
| **Taxa de Sucesso de Backup** | (Backups executados / Agendados) × 100 | Mensal | 100% |
| **Taxa de Conformidade de Acessos** | (Acessos corretos / Total auditados) × 100 | Trimestral | >98% |
| **% de Processos Documentados** | (SOPs completos / Total processos) × 100 | Trimestral | 100% |
| **Clareza de Documentação** (Pesquisa) | "Fácil encontrar info?" (0-10) | Trimestral | >8 |
| **Tempo de Remoção de Acesso** (Offboarding) | Horas entre saída e remoção completa | Por offboarding | <4h |

---

## Documentos e Ferramentas de P15

| Documento/Ferramenta | Localização | Responsável por Manter |
|----------------------|-------------|------------------------|
| **Estrutura de Pastas (Drive)** | Google Drive raiz | Todos (seguir padrão), Administrativo (revisar) |
| **Padrão de Nomeação** | Notion (P15.5) | Gestor de Tráfego (aplicar), Founder (definir) |
| **Backups** | Google Drive / 07_Backup | Administrativo/Dev |
| **Checklist de Acessos** | Notion (templates) | Administrativo |
| **Repositório de Conhecimento** | Notion (📚 página raiz) | Founder (curadoria), Gestores (atualizar áreas), Todos (consultar) |

---

## Resumo de P15

**P15 – Governança, Documentação, Acessos e Segurança** garante organização, conhecimento acessível e proteção de dados através de:

1. **Estrutura padronizada** (P15.1): Pastas e arquivos organizados, fácil localização
2. **Padrões de nomeação** (P15.2): Campanhas/conjuntos/anúncios identificáveis, relatórios claros
3. **Backup e recuperação** (P15.3): Dados protegidos, capacidade de recuperação rápida
4. **Gestão de acessos** (P15.4): Segurança (mínimo privilégio), auditoria trimestral, remoção imediata ao sair
5. **Repositório de conhecimento** (P15.5): SOPs, templates, playbooks, FAQs, glossário — tudo centralizado e atualizado

**Filosofia central**: Conhecimento é poder, mas conhecimento não documentado é vulnerável (perda de pessoas, esquecimento, inconsistência). Governança forte e documentação completa transformam agência de "dependente de indivíduos" para "operação escalável e resiliente".

**Próximos passos**: Popular Repositório (P15.5) com todos os SOPs (P1-P17). Implementar automações Python (A54-A63). Treinar equipe em padrões e uso do Repositório. Fazer primeira auditoria de acessos (P15.4). Executar primeiro backup completo (P15.3).

---

**Status**: ✅ **P15 - Completo** | Próximo: **P16 – Compliance, Jurídico e Políticas**
