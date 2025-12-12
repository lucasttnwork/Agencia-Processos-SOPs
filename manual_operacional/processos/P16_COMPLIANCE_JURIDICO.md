# P16 – Compliance, Jurídico e Políticas

## Visão Geral

Este macroprocesso garante que a agência opere em conformidade com legislações vigentes (trabalhista, tributária, proteção de dados), políticas das plataformas (Meta Ads, Google), e boas práticas de mercado. Inclui adequação às políticas de anúncios, conformidade com LGPD, gestão de contratos, prevenção de riscos legais e relacionamento com consultorias jurídicas.

**Objetivo central**: Proteger a agência e os clientes de riscos legais, garantindo operação ética, transparente e em conformidade com leis e regulamentos, minimizando passivos e construindo reputação sólida.

---

## P16.1 – Adequação às Políticas de Anúncios (Meta, Google, etc.)

### Objetivo
Garantir que 100% das campanhas e anúncios criados pela agência estejam em conformidade com as políticas das plataformas (Meta Ads, Google Ads), evitando reprovações, bloqueios de contas e problemas legais.

### Momento
- Preventivo: Durante criação de copys/criativos (P6) e QA pré-lançamento (P8.2)
- Reativo: Ao receber reprovação (P12.1)
- Contínuo: Atualização sobre mudanças de políticas

### Gatilho
- Criação de campanha/anúncio (P8)
- Nova política anunciada pela plataforma
- Reprovação recorrente (P12.8 - padrão identificado)

### Saídas
- 100% das campanhas em conformidade antes de publicar
- Taxa de reprovação <2% (meta)
- Equipe treinada em políticas
- Checklist de políticas integrado em QA (P8.2)

### Papéis Envolvidos
- **Gestor de Tráfego**: Aplicar políticas ao criar campanhas
- **Copywriter/Designer**: Criar copys/criativos em conformidade
- **Founder/Diretor**: Manter-se atualizado sobre mudanças de políticas, treinar equipe

### Ferramentas
- Políticas oficiais:
  - Meta: https://www.facebook.com/policies/ads
  - Google: https://support.google.com/adspolicy
- Notion (Checklist de Políticas em P8.2 e P15.5)
- Treinamento interno (P14.3)

---

### Passo a Passo

#### Tarefa 1: Conhecer as Políticas Principais

##### Meta Ads - Categorias Proibidas/Restritas:
- **T1.1**: Proibidas (não podem anunciar):
  - Produtos/serviços ilegais (drogas, armas, explosivos)
  - Tabaco e produtos relacionados
  - Drogas recreativas, produtos para passar em testes de drogas
  - Anúncios discriminatórios (raça, religião, orientação sexual, etc.)
  - Produtos de vigilância (spyware, equipamentos de espionagem)
  - Conteúdo chocante/sensacionalista (violência gráfica, gore)
  - Brinquedos sexuais e produtos para adultos (com exceções)
  - Anúncios enganosos ou fraudulentos
  - Falsificação (produtos piratas, contas falsas de celebridades)

- **T1.2**: Restritas (podem anunciar com limitações):
  - **Álcool**: Exige segmentação de idade (18+), não promover consumo excessivo
  - **Suplementos e Produtos de Saúde**:
    - NÃO pode prometer cura/tratamento/prevenção de doenças
    - NÃO pode ter claims de perda de peso específica ("Perca 10kg em 7 dias")
    - NÃO pode ter "antes/depois" de corpo (transformações físicas)
    - Pode: Promover suplementação, bem-estar geral (sem promessas específicas)
  - **Serviços Financeiros**:
    - Exige divulgação clara de termos (taxas, juros, riscos)
    - NÃO pode prometer "enriquecimento rápido"
    - Pode: Promover serviços legítimos (empréstimos, investimentos) com transparência
  - **Jogos de Azar e Loterias**:
    - Restrito a jurisdições permitidas
    - Exige segmentação de idade (18+)
  - **Medicamentos com Prescrição**:
    - Proibido promover diretamente
    - Pode: Promover consulta médica, diagnóstico

- **T1.3**: Restrições de Conteúdo (Geral):
  - **Texto na Imagem**: Evitar >20% de texto na imagem (não é proibido, mas afeta alcance)
  - **Gramática e Ortografia**: Erros excessivos podem reprovar
  - **Uso de "Você"**: Não usar "você" de forma que implique conhecimento de atributos pessoais (ex.: "Você tem diabetes?" proibido se segmentar por interesse em diabetes)
  - **Sensacionalismo**: Evitar clickbait excessivo ("Você NÃO VAI ACREDITAR nisto!")
  - **Afirmações sobre Características Pessoais**: Não pode fazer afirmações sobre raça, religião, orientação sexual, saúde, dificuldades financeiras, etc. ("Você está endividado?" proibido)

##### Google Ads - Políticas Principais:
- **T1.4**: Similar ao Meta, com adições:
  - **Saúde**: Mais restritivo (não permite anúncios de farmácias online sem certificação)
  - **Política de Marca Registrada**: Mais rigoroso (não usar marca de terceiros sem autorização)

#### Tarefa 2: Integrar Políticas no Processo de Criação

##### Durante Produção (P6):
- **T2.1**: Copywriter revisa checklist de políticas antes de enviar copy:
  - [ ] Não há claims proibidos (cura, perda de peso específica, etc.)
  - [ ] Não há linguagem discriminatória
  - [ ] Não há sensacionalismo excessivo
  - [ ] Gramática e ortografia corretas
  - [ ] Não usa "você" de forma proibida

- **T2.2**: Designer revisa checklist antes de enviar criativo:
  - [ ] Texto na imagem <20% (se possível)
  - [ ] Não há imagens de "antes/depois" (se saúde/fitness)
  - [ ] Não há conteúdo chocante/violento
  - [ ] Não há imitação de funcionalidade da plataforma (ex.: botão falso de "Play")

##### Durante QA (P8.2):
- **T2.3**: Gestor de Tráfego revisa checklist completo de políticas:
  - [ ] Copy em conformidade (revisar T2.1)
  - [ ] Criativo em conformidade (revisar T2.2)
  - [ ] Landing Page em conformidade:
    - [ ] Funciona corretamente (não dá erro 404)
    - [ ] Conteúdo alinhado com anúncio (não é enganoso)
    - [ ] Não tem conteúdo proibido (drogas, violência, etc.)
    - [ ] Política de Privacidade presente (se coleta dados)
  - [ ] Segmentação apropriada (idade mínima para álcool, jogos, etc.)
  - [ ] Não usa marca registrada de terceiros sem autorização

#### Tarefa 3: Treinar Equipe (P14.3)
- **T3.1**: Onboarding (P14.1):
  - Dia 2-3: Estudar políticas (Meta + Google)
  - Exercício: Identificar problemas em 10 anúncios de exemplo (quais violariam políticas?)
- **T3.2**: Treinamento anual (ou quando políticas mudam):
  - Revisão de políticas atualizadas
  - Casos reais de reprovações (P12.8) → O que aprendemos?
  - Quiz (10 perguntas sobre políticas) → Todos devem acertar >80%

#### Tarefa 4: Monitorar Mudanças de Políticas
- **T4.1**: Assinar newsletters/alertas oficiais:
  - Meta for Business (https://www.facebook.com/business/news)
  - Google Ads Updates (https://support.google.com/google-ads/answer/12155607)
- **T4.2**: Quando houver mudança relevante:
  - Ler atentamente
  - Avaliar impacto (afeta clientes atuais?)
  - Atualizar checklist (P8.2, Notion)
  - Treinar equipe (P14.3 - sessão rápida)
  - Revisar campanhas ativas (se necessário, ajustar)

#### Tarefa 5: Lidar com Reprovações (P12.1)
- **T5.1**: Quando anúncio é reprovado:
  - Identificar política violada (notificação do Meta/Google)
  - Corrigir (remover elemento proibido) OU enviar recurso (se reprovação foi erro)
  - Documentar (P12.8): Qual política? Por que violou? Como evitar recorrência?
- **T5.2**: Se reprovações recorrentes de mesma política:
  - Adicionar item no checklist de QA (P8.2)
  - Treinar equipe (P14.3) especificamente nessa política

---

### Checklist de Qualidade

- [ ] Checklist de políticas integrado em P6 (Produção) e P8.2 (QA)
- [ ] Equipe treinada (todos conhecem políticas principais)
- [ ] Taxa de reprovação <2% (meta)
- [ ] 100% das reprovações documentadas (P12.8) com aprendizado extraído
- [ ] Monitoramento de mudanças de políticas implementado
- [ ] Revisão anual de treinamento (P14.3)

---

### Erros Comuns a Evitar

- Não consultar políticas antes de criar (reprovar depois, retrabalho) — verificar preventivamente
- Assumir que "todos sabem" políticas (novos membros podem não saber) — treinar sempre
- Ignorar mudanças de políticas (continuar fazendo errado) — monitorar atualizações
- Enviar recurso sem ler política (negar automaticamente) — sempre revisar política antes de recorrer
- Fazer anúncios "no limite" da política (arriscado, pode reprovar) — ser conservador

---

### Métricas Relacionadas

| Métrica | Fórmula/Fonte | Frequência |
|---------|---------------|------------|
| **Taxa de Reprovação** | (Anúncios reprovados / Total publicados) × 100 | Mensal (meta: <2%) |
| **Taxa de Sucesso de Recurso** | (Recursos aprovados / Total recursos) × 100 | Trimestral |
| **Score de Conhecimento de Políticas** (Quiz) | Média de acertos no quiz de políticas (%) | Anual (meta: >80%) |

---

### Automações Python

| ID | Gatilho | Ação |
|----|---------|------|
| **A64** | Anúncio reprovado (Meta API, status = "Disapproved") | Criar incidente (P12.1), notificar gestor, adicionar em dashboard de reprovações |
| **A65** | Nova política anunciada (web scraping de página de políticas do Meta/Google) | Alerta para Founder/Gestor revisar e treinar equipe |

---

### Templates Associados

- **Checklist de Políticas** (integrado em P8.2 QA, ver T2.3)
- **Quiz de Políticas** (Google Forms ou Notion):
  ```
  QUIZ DE POLÍTICAS DE ANÚNCIOS

  1. Posso prometer perda de peso específica (ex.: "Perca 10kg em 7 dias") em anúncio de suplemento no Meta Ads?
     a) Sim
     b) Não ✅

  2. Posso usar imagem "antes/depois" de corpo em anúncio de fitness?
     a) Sim
     b) Não ✅

  3. Posso usar "você" no copy do anúncio?
     a) Sim, sempre
     b) Não, nunca
     c) Sim, mas não de forma que implique conhecimento de atributos pessoais ✅

  4. Qual é o percentual máximo recomendado de texto na imagem no Meta Ads?
     a) 10%
     b) 20% ✅
     c) 50%
     d) Não há limite

  5. Posso anunciar álcool no Meta Ads?
     a) Sim, sem restrições
     b) Não, é proibido
     c) Sim, com segmentação de idade (18+) e sem promover consumo excessivo ✅

  [... continuar com 10 perguntas, cobrir políticas principais]
  ```

---

### Fluxos de Exceção

| Situação | Ação |
|----------|------|
| **Cliente insiste em copy proibida** (ex.: quer prometer cura) | Educar cliente (explicar políticas, risco de bloqueio de conta), oferecer alternativa em conformidade, se cliente insiste: não aceitar campanha (proteger agência) |
| **Reprovação em massa** (>10 anúncios) | Pausar criação de novos anúncios, revisar processo completo (P6, P8.2), treinar equipe urgentemente (P14.3), contatar suporte Meta/Google |
| **Política mudou e campanhas ativas violam** | Pausar campanhas afetadas imediatamente, ajustar (remover elemento proibido), republicar, comunicar clientes afetados (P12.7) |

---

---

## P16.2 – Conformidade com LGPD (Lei Geral de Proteção de Dados)

### Objetivo
Garantir que a agência e os clientes estejam em conformidade com a LGPD (Lei nº 13.709/2018) no tratamento de dados pessoais de leads e clientes, protegendo privacidade e evitando multas/sanções.

### Momento
- Preventivo: Ao coletar dados de leads (P2, P3, P4)
- Contínuo: Tratamento de dados (armazenamento, uso, compartilhamento)
- Reativo: Quando lead/cliente solicita acesso/exclusão de dados (DSAR - Data Subject Access Request)

### Gatilho
- Nova campanha que coleta dados (P8)
- Solicitação de lead/cliente sobre seus dados
- Auditoria de LGPD (anual, P17)

### Saídas
- 100% das campanhas com aviso de privacidade (quando coleta dados)
- Política de Privacidade publicada (site, LP)
- Dados pessoais armazenados com segurança (P15.3, P15.4)
- Solicitações de DSAR atendidas em até 15 dias (prazo legal)

### Papéis Envolvidos
- **Founder/Diretor**: Responsável legal (DPO - Data Protection Officer, se aplicável)
- **Gestor de Tráfego**: Implementar avisos de privacidade em campanhas
- **Administrativo/Dev**: Gerenciar dados, responder DSARs
- **Jurídico** (externo): Revisar Política de Privacidade, contratos

### Ferramentas
- Política de Privacidade (site, LP)
- Termos de Uso (se aplicável)
- Consentimento (checkboxes em formulários)
- Notion (registro de DSARs, Consentimentos)

---

### Passo a Passo

#### Tarefa 1: Mapear Tratamento de Dados

##### Dados Pessoais Coletados:
- **T1.1**: Listar todos os dados pessoais que agência/clientes coletam:
  - **De leads**:
    - Nome completo
    - E-mail
    - Telefone (WhatsApp)
    - Localização (cidade, estado - via Meta Ads)
    - Comportamento online (páginas visitadas, cliques, interações - via Pixel/CAPI)
  - **De clientes da agência**:
    - Nome, e-mail, telefone, CNPJ/CPF, endereço
    - Dados de pagamento (boleto, cartão - armazenados por gateway)
    - Documentos (contratos, notas fiscais)

##### Finalidade do Tratamento:
- **T1.2**: Para cada dado, definir finalidade:
  - **Leads**: Contato comercial (oferecer produtos/serviços), qualificação, remarketing
  - **Clientes da agência**: Execução de contrato, faturamento, comunicação

##### Base Legal:
- **T1.3**: Identificar base legal (LGPD, Art. 7):
  - **Consentimento**: Lead autoriza uso de dados (checkbox em formulário)
  - **Legítimo Interesse**: Agência tem interesse legítimo em processar dados para marketing
  - **Execução de Contrato**: Dados necessários para cumprir contrato

#### Tarefa 2: Implementar Política de Privacidade

##### Criar/Revisar Política de Privacidade:
- **T2.1**: Redigir Política de Privacidade (com apoio jurídico):
  - **Quem somos**: Identificação da agência (razão social, CNPJ, contato)
  - **Dados coletados**: Lista de dados pessoais (T1.1)
  - **Finalidade**: Por que coletamos (T1.2)
  - **Base legal**: Consentimento, legítimo interesse, contrato (T1.3)
  - **Compartilhamento**: Com quem compartilhamos dados (Meta, Google, CRM, gateway de pagamento)
  - **Armazenamento**: Onde e por quanto tempo armazenamos
  - **Segurança**: Medidas de segurança implementadas (P15.3, P15.4)
  - **Direitos do titular**:
    - Acesso aos dados
    - Correção de dados
    - Exclusão de dados (direito ao esquecimento)
    - Portabilidade de dados
    - Revogação de consentimento
  - **Como exercer direitos**: E-mail de contato (ex.: privacidade@agencia.com)
  - **Cookies**: Se site usa cookies (Meta Pixel, Google Analytics)

- **T2.2**: Publicar Política de Privacidade:
  - **Site da agência**: Link no rodapé (footer)
  - **Landing pages de clientes**: Link obrigatório no rodapé (perto de formulário)
  - **E-mails de marketing**: Link no rodapé (ex.: "Ver nossa Política de Privacidade")

##### Implementar Consentimento:
- **T2.3**: Em formulários de captura de lead (Meta Lead Ads, LP):
  - Adicionar checkbox:
    ```
    [ ] Concordo em fornecer meus dados para contato comercial e marketing.
    Li e aceito a Política de Privacidade [link].
    ```
  - Checkbox **não pode** vir pré-marcado (deve ser ação ativa do lead)
  - Sem consentimento, lead não pode ser contactado (LGPD exige)

#### Tarefa 3: Armazenar Dados com Segurança
- **T3.1**: Seguir P15.3 (Backup) e P15.4 (Acessos):
  - Dados armazenados em sistemas seguros (Google Workspace, Notion - com 2FA)
  - Acessos restritos (mínimo privilégio)
  - Backups regulares (não perder dados, mas também não manter indefinidamente sem necessidade)
- **T3.2**: Não armazenar dados sensíveis desnecessários:
  - Nunca armazenar senhas de leads em texto plano
  - Dados de cartão de crédito: nunca armazenar (gateway faz isso)

#### Tarefa 4: Respeitar Direitos dos Titulares (DSARs)

##### Quando lead/cliente solicita:
- **T4.1**: **Acesso aos dados**:
  - Lead pede: "Quais dados vocês têm sobre mim?"
  - Responder em até 15 dias: "Temos seu nome, e-mail, telefone, coletados em [data], para finalidade de [X]."
  - Formato: E-mail ou documento (PDF)

- **T4.2**: **Correção de dados**:
  - Lead pede: "Meu e-mail está errado, corrija para [novo]."
  - Atualizar em todos os sistemas (CRM, Notion, Meta Ads - se remarketing)
  - Confirmar correção em até 15 dias

- **T4.3**: **Exclusão de dados** (direito ao esquecimento):
  - Lead pede: "Quero que deletem meus dados."
  - Verificar se há obrigação legal de manter (ex.: contrato ativo, obrigação fiscal de 5 anos)
  - Se não há obrigação: deletar de todos os sistemas (CRM, Notion, Meta Ads)
  - Confirmar exclusão em até 15 dias
  - **Importante**: Excluir de públicos de remarketing (Meta Ads) também

- **T4.4**: **Revogação de consentimento**:
  - Lead pede: "Não quero mais receber mensagens."
  - Remover de listas de marketing (e-mail, WhatsApp)
  - Manter dados mínimos se há base legal diferente (ex.: contrato)
  - Confirmar em até 15 dias

- **T4.5**: **Portabilidade de dados**:
  - Lead pede: "Quero meus dados em formato que eu possa usar."
  - Exportar dados em formato estruturado (CSV, JSON)
  - Enviar em até 15 dias

##### Registrar DSARs:
- **T4.6**: Criar base no Notion:
  - **DSARs** (Data Subject Access Requests):
    - Solicitante (nome, e-mail)
    - Tipo (Acesso, Correção, Exclusão, Revogação, Portabilidade)
    - Data de solicitação
    - Data de resposta (prazo: 15 dias)
    - Status (Aberta, Em análise, Concluída)
    - Ações tomadas (descrição)

#### Tarefa 5: Revisar Contratos (Cláusula de LGPD)
- **T5.1**: Contratos com clientes (P13.2) devem incluir cláusula de LGPD:
  - "A CONTRATADA compromete-se a tratar dados pessoais de leads e clientes da CONTRATANTE em conformidade com a Lei Geral de Proteção de Dados (LGPD, Lei nº 13.709/2018). Os dados coletados serão usados exclusivamente para finalidades acordadas (geração de leads, remarketing) e não serão compartilhados com terceiros sem autorização, exceto prestadores de serviços essenciais (Meta, Google, CRM)."
- **T5.2**: Contratos com fornecedores (CRM, gateway, etc.):
  - Garantir que fornecedores também são LGPD-compliant (cláusula de proteção de dados)

#### Tarefa 6: Auditoria Anual de LGPD (P17)
- **T6.1**: Uma vez por ano, revisar conformidade:
  - Política de Privacidade está atualizada?
  - Formulários têm checkbox de consentimento?
  - Dados são armazenados com segurança? (P15.3, P15.4)
  - DSARs foram atendidos no prazo?
  - Há dados desnecessários armazenados (devem ser deletados)?
- **T6.2**: Consultar jurídico (se necessário) para validar conformidade

---

### Checklist de Qualidade

- [ ] Política de Privacidade publicada (site, LPs) e atualizada
- [ ] Formulários têm checkbox de consentimento (não pré-marcado)
- [ ] Dados armazenados com segurança (P15.3, P15.4)
- [ ] Processo de DSAR documentado (Notion)
- [ ] 100% dos DSARs atendidos em ≤15 dias (prazo legal)
- [ ] Contratos incluem cláusula de LGPD
- [ ] Auditoria anual de LGPD realizada (P17)

---

### Erros Comuns a Evitar

- Não ter Política de Privacidade (ilegal, passível de multa) — publicar imediatamente
- Checkbox de consentimento pré-marcado (não é consentimento válido) — sempre desmarcado por padrão
- Ignorar DSARs (passível de multa, até R$50 milhões) — responder em até 15 dias
- Armazenar dados indefinidamente (sem necessidade) — deletar quando não mais necessário
- Não consultar jurídico (risco de não-conformidade) — revisar com advogado especializado

---

### Métricas Relacionadas

| Métrica | Fórmula/Fonte | Frequência |
|---------|---------------|------------|
| **% de Formulários com Consentimento** | (Formulários com checkbox / Total formulários) × 100 | Trimestral (meta: 100%) |
| **Tempo Médio de Resposta a DSAR** | Média(data resposta − data solicitação) | Por DSAR (meta: ≤15 dias) |
| **Número de DSARs** | Contagem de solicitações | Mensal |
| **% de DSARs Atendidos no Prazo** | (Atendidos em ≤15 dias / Total DSARs) × 100 | Trimestral (meta: 100%) |

---

### Automações Python

| ID | Gatilho | Ação |
|----|---------|------|
| **A66** | DSAR criado (Notion) | Alerta para Administrativo/Founder responder em até 15 dias, lembrete em 10 dias se ainda aberta |
| **A67** | Novo formulário de lead sem checkbox de consentimento (auditoria de LPs) | Alerta para corrigir formulário imediatamente |

---

### Templates Associados

- **Política de Privacidade** (ver T2.1 - deve ser revisada por jurídico)
- **Cláusula de LGPD para Contratos** (ver T5.1)
- **Template de Resposta a DSAR**:
  ```
  Assunto: Resposta à sua solicitação de [Acesso/Correção/Exclusão] de dados

  Olá [Nome],

  Recebemos sua solicitação de [tipo de DSAR] de dados pessoais em [data].

  [Se Acesso:]
  Seguem os dados que temos sobre você:
  - Nome: [X]
  - E-mail: [X]
  - Telefone: [X]
  - Data de coleta: [X]
  - Finalidade: [X]

  [Se Correção:]
  Seus dados foram corrigidos conforme solicitado. O novo e-mail cadastrado é: [X].

  [Se Exclusão:]
  Seus dados foram excluídos de nossos sistemas. Você não receberá mais comunicações nossas.

  [Se Revogação de Consentimento:]
  Seu consentimento foi revogado. Você foi removido de nossas listas de marketing.

  [Se Portabilidade:]
  Seus dados estão em anexo (formato CSV/JSON).

  Qualquer dúvida, entre em contato conosco em [e-mail].

  Atenciosamente,
  [Nome]
  [Agência]
  ```

---

### Fluxos de Exceção

| Situação | Ação |
|----------|------|
| **DSAR de exclusão mas há obrigação legal de manter dados** (ex.: contrato ativo, fiscal) | Explicar ao solicitante que dados devem ser mantidos por obrigação legal (especificar qual), mas serão deletados após fim da obrigação, não serão usados para marketing |
| **Lead reclama que não deu consentimento** | Verificar registro de consentimento (Notion, CRM), se não há registro: pedir desculpas, deletar dados imediatamente, revisar processo (P16.2 - T2.3) |
| **Multa da ANPD** (Autoridade Nacional de Proteção de Dados) | Consultar jurídico urgentemente, corrigir não-conformidade imediatamente, implementar melhorias (P17), comunicar clientes se necessário |

---

---

## P16.3 – Gestão de Contratos e Cláusulas Importantes

### Objetivo
Garantir que todos os contratos da agência (com clientes, fornecedores, equipe) tenham cláusulas essenciais que protejam interesses da agência, definam responsabilidades claras e previnam disputas legais.

### Momento
- Preventivo: Ao criar templates de contratos (P13.2, P14.1, outros)
- Revisão: Anual (P17) ou quando legislação muda

### Gatilho
- Novo tipo de contrato necessário (ex.: parceria, freelancer fixo)
- Disputa contratual (revisar cláusulas para prevenir recorrência)
- Mudança de legislação

### Saídas
- Templates de contratos revisados por jurídico
- Cláusulas essenciais presentes em 100% dos contratos
- Redução de disputas contratuais

### Papéis Envolvidos
- **Founder/Diretor**: Negociação e assinatura de contratos
- **Jurídico** (externo): Redação e revisão de contratos
- **Financeiro**: Execução de cláusulas financeiras (pagamento, multas)

### Ferramentas
- Templates de contratos (Notion P15.5, Google Drive)
- Plataforma de assinatura eletrônica (Autentique, Clicksign)
- Registro de contratos (Notion - Contratos)

---

### Passo a Passo

#### Tarefa 1: Identificar Tipos de Contratos da Agência
- **T1.1**: Listar todos os tipos:
  - **Com clientes**:
    - Contrato de Prestação de Serviços (P13.2)
  - **Com equipe**:
    - Contrato de Trabalho (CLT, PJ)
    - Contrato de Freelancer
  - **Com fornecedores**:
    - Contrato de Prestação de Serviços (contabilidade, jurídico, dev)
    - Contrato de Licença de Software (Notion, Canva, etc.)
  - **Parcerias**:
    - Acordo de Indicação (parceria com outras empresas)
    - Contrato de Afiliação

#### Tarefa 2: Definir Cláusulas Essenciais

##### Contrato com Clientes (P13.2):
- **T2.1**: Cláusulas obrigatórias:
  - **Objeto**: Descrição detalhada dos serviços (o que está incluído, o que NÃO está)
  - **Investimento**: Valor, forma de pagamento, vencimento, multa/juros por atraso
  - **Prazo**: Data de início, prazo mínimo, renovação automática
  - **Responsabilidades da Contratante** (cliente):
    - Fornecer acessos (BM, site, etc.) em até X dias
    - Fornecer materiais (logo, fotos, etc.)
    - Aprovar criativos em até X dias
    - Investir mínimo de R$X em mídia
  - **Responsabilidades da Contratada** (agência):
    - Executar serviços conforme escopo
    - Entregar relatórios
    - Responder em até X horas
  - **Rescisão**:
    - Aviso prévio (30 dias)
    - Multa por rescisão antes do prazo mínimo (ex.: equivalente a X mensalidades)
    - Motivos de rescisão imediata (não pagamento, comportamento abusivo, etc.)
  - **Propriedade Intelectual**:
    - Criativos/materiais produzidos pertencem ao cliente após quitação
  - **Confidencialidade**:
    - Ambas as partes se comprometem a não divulgar informações confidenciais
  - **LGPD** (P16.2):
    - Agência compromete-se a tratar dados em conformidade com LGPD
  - **Foro**:
    - Cidade/estado para dirimir disputas

##### Contrato com Equipe (CLT/PJ):
- **T2.2**: Cláusulas obrigatórias:
  - **Cargo e Atribuições**: Descrição do papel (P14.2)
  - **Remuneração**: Valor, periodicidade (mensal), forma de pagamento
  - **Jornada de Trabalho**: Horas semanais, flexibilidade, home office/presencial
  - **Confidencialidade e Não-Concorrência**:
    - Não divulgar informações confidenciais da agência
    - Não trabalhar para concorrentes diretos durante vínculo (e por X meses após, se aplicável)
  - **Propriedade Intelectual**:
    - Trabalhos criados durante vínculo pertencem à agência
  - **Rescisão**:
    - Aviso prévio (conforme legislação trabalhista)
    - Motivos de justa causa

##### Contrato com Fornecedores:
- **T2.3**: Cláusulas obrigatórias:
  - **Escopo de Serviços**: O que fornecedor entregará
  - **SLA** (Service Level Agreement): Prazos, disponibilidade (ex.: suporte em até 24h)
  - **Confidencialidade**: Fornecedor não pode divulgar dados/informações da agência
  - **LGPD** (se fornecedor tem acesso a dados pessoais): Compromisso de conformidade
  - **Rescisão**: Aviso prévio, multa (se aplicável)

##### Acordo de Parceria/Indicação:
- **T2.4**: Cláusulas obrigatórias:
  - **Comissão**: % ou valor fixo por indicação convertida
  - **Condições de Pagamento**: Quando comissão é paga (ex.: após primeiro pagamento do cliente)
  - **Prazo**: Validade do acordo
  - **Exclusividade** (se aplicável): Parceiro não pode indicar para concorrentes

#### Tarefa 3: Criar/Revisar Templates com Jurídico
- **T3.1**: Contratar advogado especializado (Direito Empresarial/Contratos):
  - Redigir templates de contratos (se ainda não existem)
  - Revisar templates existentes (se estão desatualizados)
- **T3.2**: Garantir que templates incluem todas as cláusulas essenciais (T2)
- **T3.3**: Salvar templates em P15.5 (Repositório de Conhecimento, Notion + Drive)

#### Tarefa 4: Usar Templates Consistentemente
- **T4.1**: Sempre que assinar contrato:
  - Usar template padrão (não criar "do zero")
  - Preencher campos variáveis (nome, valor, prazo, etc.)
  - Se necessário customizar: consultar jurídico antes (não remover cláusulas essenciais)
- **T4.2**: Registrar contrato assinado (Notion - Contratos):
  - Partes, objeto, valor, prazo, data de assinatura, anexar PDF

#### Tarefa 5: Revisar Contratos Periodicamente
- **T5.1**: Anual (P17):
  - Revisar todos os templates de contratos
  - Verificar se legislação mudou (ex.: nova lei trabalhista, mudança na LGPD)
  - Atualizar templates com apoio de jurídico
  - Comunicar equipe (se mudanças afetam contratos ativos, pode ser necessário adendo)

---

### Checklist de Qualidade

- [ ] Todos os tipos de contratos mapeados (clientes, equipe, fornecedores, parceiros)
- [ ] Templates criados/revisados por jurídico
- [ ] Cláusulas essenciais presentes em 100% dos templates
- [ ] Templates salvos em P15.5 (Repositório)
- [ ] 100% dos contratos novos usam templates (não "do zero")
- [ ] Revisão anual agendada (P17)
- [ ] Registro de contratos atualizado (Notion - Contratos)

---

### Erros Comuns a Evitar

- Usar contrato "genérico da internet" (não protege adequadamente) — sempre revisar com jurídico
- Não ter cláusula de rescisão clara (disputas quando cliente/membro quer sair) — definir claramente
- Não registrar contratos (perder histórico, dificultar cobrança) — registrar sempre no Notion
- Customizar contrato sem jurídico (remover cláusula essencial por engano) — consultar antes
- Não revisar contratos antigos (ficam desatualizados com legislação) — revisar anualmente

---

### Métricas Relacionadas

| Métrica | Fórmula/Fonte | Frequência |
|---------|---------------|------------|
| **% de Contratos com Templates** | (Contratos usando template / Total contratos) × 100 | Trimestral (meta: 100%) |
| **Número de Disputas Contratuais** | Contagem de disputas/ações judiciais | Anual (meta: 0) |

---

### Automações Python

| ID | Gatilho | Ação |
|----|---------|------|
| **A68** | Novo contrato registrado (Notion - Contratos) | Verificar se template foi usado (campo "Tipo de Contrato"), alerta se "Customizado" (deve ter revisão jurídica) |

---

### Templates Associados

- **Template de Contrato com Cliente** (P13.2, ver detalhes lá)
- **Template de Contrato com Equipe** (CLT/PJ - consultar jurídico para criar)
- **Checklist de Revisão de Contrato**:
  ```
  REVISÃO DE CONTRATO: [Tipo]
  Data de revisão: [Data]
  Revisado por: [Jurídico/Founder]

  CLÁUSULAS ESSENCIAIS:
  - [ ] Objeto (detalhado, claro)
  - [ ] Investimento/Remuneração (valor, forma, prazo)
  - [ ] Prazo (início, duração, renovação)
  - [ ] Responsabilidades (ambas as partes)
  - [ ] Rescisão (aviso prévio, multa, justa causa)
  - [ ] Propriedade Intelectual (se aplicável)
  - [ ] Confidencialidade
  - [ ] LGPD (se trata dados pessoais)
  - [ ] Foro (cidade/estado)

  VERIFICAÇÕES:
  - [ ] Linguagem clara (não ambígua)
  - [ ] Conforme legislação vigente (trabalhista, civil, etc.)
  - [ ] Assinaturas de ambas as partes (nome completo, CPF/CNPJ, data)
  - [ ] Anexos referenciados (se houver)

  OBSERVAÇÕES:
  [Qualquer nota relevante]

  APROVADO POR:
  [Nome do Jurídico/Founder] - [Data]
  ```

---

### Fluxos de Exceção

| Situação | Ação |
|----------|------|
| **Disputa contratual** (cliente/membro alega que contrato não é claro) | Revisar contrato com jurídico, tentar resolver amigavelmente, se não resolver: mediação ou ação judicial, aprender: ajustar template para prevenir recorrência |
| **Cliente quer remover cláusula essencial** (ex.: não aceita multa de rescisão) | Negociar, explicar importância da cláusula (proteção mútua), se cliente insiste: avaliar risco (vale a pena fechar sem cláusula? Ou melhor não fechar?), consultar jurídico |
| **Legislação muda** (ex.: nova lei trabalhista) | Atualizar templates urgentemente com jurídico, revisar contratos ativos (pode ser necessário adendo/renovação antecipada), comunicar equipe/clientes se aplicável |

---

---

## P16.4 – Prevenção de Riscos Legais

### Objetivo
Identificar, avaliar e mitigar riscos legais que a agência enfrenta (trabalhistas, tributários, contratuais, de propriedade intelectual), prevenindo ações judiciais, multas e danos à reputação.

### Momento
- Contínuo: Monitoramento de conformidade
- Preventivo: Ao tomar decisões estratégicas (contratação, novo serviço, parceria)
- Periódico: Revisão anual de riscos (P17)

### Gatilho
- Nova atividade/serviço (avaliar risco antes de oferecer)
- Disputa/reclamação de cliente/membro
- Mudança de legislação
- Revisão anual de riscos (P17)

### Saídas
- Matriz de riscos legais identificados e avaliados
- Ações preventivas implementadas
- Seguro de responsabilidade civil (se aplicável)
- Redução de exposição legal

### Papéis Envolvidos
- **Founder/Diretor**: Tomada de decisão sobre mitigação de riscos
- **Jurídico** (externo): Identificação e avaliação de riscos, consultoria
- **Contador**: Riscos tributários

### Ferramentas
- Matriz de Riscos (Notion ou planilha)
- Consultoria jurídica externa
- Seguros (se aplicável)

---

### Passo a Passo

#### Tarefa 1: Identificar Riscos Legais Principais

##### Riscos Trabalhistas:
- **T1.1**:
  - **Pejotização indevida**: Contratar PJ mas tratar como CLT (horário fixo, subordinação, exclusividade) → Ação trabalhista, conversão em CLT, pagamento retroativo de encargos + multas
  - **Justa causa mal aplicada**: Demitir por justa causa sem motivo legal → Ação trabalhista, reversão + indenização
  - **Não pagamento de verbas rescisórias**: Atraso em pagamento → Multa, juros, ação trabalhista

##### Riscos Tributários:
- **T1.2**:
  - **Emissão incorreta de NF**: Erros em notas fiscais → Multas da Receita Federal/Estadual/Municipal
  - **Não recolhimento de impostos**: Atraso ou não pagamento (ISS, INSS, IR) → Multas, juros, penhora de bens
  - **Desenquadramento de regime tributário**: Faturar acima do limite do Simples Nacional sem migrar → Cobrança retroativa, multas

##### Riscos Contratuais:
- **T1.3**:
  - **Descumprimento de contrato com cliente**: Não entregar serviços conforme acordado → Rescisão, devolução de valores, ação de danos
  - **Descumprimento de contrato com fornecedor**: Não pagar fornecedor → Ação judicial, negativação
  - **Contrato sem cláusulas essenciais**: Disputas sem previsão contratual → Processo longo e caro

##### Riscos de Propriedade Intelectual:
- **T1.4**:
  - **Uso indevido de imagens/vídeos**: Usar imagem de banco sem licença, ou foto de terceiros sem autorização → Ação de direitos autorais, indenização
  - **Plágio de criativos**: Copiar criativo de concorrente → Ação de concorrência desleal, danos
  - **Uso de marca registrada**: Usar marca de terceiro em anúncio sem autorização → Ação de propriedade industrial, indenização

##### Riscos de Proteção de Dados (LGPD):
- **T1.5**: Ver P16.2 (já mapeado)
  - **Vazamento de dados**: Falha de segurança → Multa ANPD (até R$50 milhões), danos à reputação
  - **Não atendimento de DSAR**: Ignorar solicitação de exclusão → Multa ANPD

##### Riscos de Políticas de Plataformas:
- **T1.6**: Ver P16.1 (já mapeado)
  - **Bloqueio de contas de clientes**: Violação de políticas → Perda de capacidade de anunciar, insatisfação do cliente, rescisão

##### Riscos Reputacionais:
- **T1.7**:
  - **Promessas não cumpridas**: Prometer resultados irrealistas → Reclamações, Reclame Aqui, perda de credibilidade
  - **Atendimento ruim**: Cliente insatisfeito → Avaliações negativas, perda de novos clientes

#### Tarefa 2: Avaliar Riscos (Probabilidade × Impacto)
- **T2.1**: Para cada risco, avaliar:
  - **Probabilidade**: Baixa (raro), Média (pode acontecer), Alta (provável)
  - **Impacto**: Baixo (pequeno prejuízo), Médio (prejuízo moderado), Alto (prejuízo grave, pode inviabilizar agência)
- **T2.2**: Criar matriz de riscos:
  | Risco | Probabilidade | Impacto | Prioridade (P×I) | Ações Preventivas |
  |-------|---------------|---------|------------------|-------------------|
  | Pejotização indevida | Média | Alto | Alta | Revisar contratos PJ, garantir autonomia real, não ter exclusividade/subordinação |
  | Emissão incorreta de NF | Baixa | Médio | Média | Treinar Financeiro, revisar com contador |
  | Uso indevido de imagens | Média | Alto | Alta | Usar apenas bancos de imagens licenciados (ex.: Unsplash, Pexels), ou criar próprios |
  | Vazamento de dados (LGPD) | Baixa | Alto | Média | Seguir P15.3 (Backup) e P15.4 (Acessos), 2FA obrigatório |
  | Bloqueio de contas Meta | Média | Alto | Alta | Seguir P16.1 (Políticas), QA rigoroso (P8.2) |
  | Promessas irrealistas | Média | Médio | Média | Scripts de vendas honestos (P3.3), não prometer ROI específico |

#### Tarefa 3: Implementar Ações Preventivas
- **T3.1**: Para cada risco de prioridade Alta:
  - Definir ação preventiva específica (ver coluna "Ações Preventivas")
  - Atribuir responsável
  - Implementar
  - Monitorar (trimestral P17)
- **T3.2**: Exemplos de ações preventivas:
  - **Contratos PJ**: Revisar com jurídico, garantir autonomia (sem horário fixo, sem exclusividade), documentar entregas (não horas)
  - **Imagens licenciadas**: Usar Unsplash, Pexels, Canva (com licença Pro), ou contratar fotógrafo (com cessão de direitos)
  - **Políticas de anúncios**: Treinar equipe (P14.3), QA rigoroso (P8.2), checklist de políticas (P16.1)
  - **LGPD**: Seguir P16.2 (Política de Privacidade, consentimento, segurança)

#### Tarefa 4: Contratar Seguros (Opcional)
- **T4.1**: Avaliar necessidade de seguro de responsabilidade civil:
  - Cobre danos causados a terceiros (ex.: erro em campanha que gera prejuízo ao cliente)
  - Custo: Varia conforme faturamento e risco (consultar corretora)
  - Recomendado: Se agência tem alto faturamento ou clientes grandes (risco de processos altos)
- **T4.2**: Outros seguros possíveis:
  - Seguro de Cyber (proteção contra vazamento de dados, ataques hackers)
  - Seguro de Erros e Omissões (E&O Insurance, comum em agências)

#### Tarefa 5: Revisar Riscos Anualmente (P17)
- **T5.1**: Uma vez por ano:
  - Revisar matriz de riscos (T2.2)
  - Adicionar novos riscos (mudanças na operação, legislação)
  - Reavaliar probabilidade e impacto (mudou?)
  - Verificar se ações preventivas estão sendo seguidas
  - Atualizar ações se necessário
- **T5.2**: Consultar jurídico para validar avaliação

---

### Checklist de Qualidade

- [ ] Riscos legais principais identificados (trabalhistas, tributários, contratuais, PI, LGPD, plataformas, reputacionais)
- [ ] Matriz de riscos criada (probabilidade × impacto)
- [ ] Ações preventivas definidas e implementadas (prioridade alta)
- [ ] Contratos revisados (PJ, clientes, fornecedores) para mitigar riscos
- [ ] Seguros avaliados (se aplicável)
- [ ] Revisão anual de riscos agendada (P17)

---

### Erros Comuns a Evitar

- Ignorar riscos ("não vai acontecer comigo") — avaliar realisticamente
- Não documentar (matriz de riscos mental, não escrita) — documentar sempre
- Não implementar ações preventivas (só identificar, não agir) — agir proativamente
- Não revisar periodicamente (riscos mudam) — revisar anualmente
- Contratar PJ e tratar como CLT (risco altíssimo) — garantir autonomia real

---

### Métricas Relacionadas

| Métrica | Fórmula/Fonte | Frequência |
|---------|---------------|------------|
| **Número de Ações Judiciais** | Contagem de processos | Anual (meta: 0) |
| **Valor Total de Multas/Sanções** | Soma de multas (tributárias, trabalhistas, LGPD, etc.) | Anual (meta: R$0) |
| **% de Riscos com Ações Preventivas** | (Riscos com ação implementada / Total riscos Alta prioridade) × 100 | Trimestral (meta: 100%) |

---

### Automações Python

| ID | Gatilho | Ação |
|----|---------|------|
| **A69** | Fim do ano | Alerta para Founder/Diretor revisar matriz de riscos (P16.4), agendar consultoria jurídica |

---

### Templates Associados

- **Matriz de Riscos Legais** (Notion ou planilha, ver T2.2)

---

### Fluxos de Exceção

| Situação | Ação |
|----------|------|
| **Ação judicial recebida** | Não ignorar, contatar advogado imediatamente, fornecer toda documentação (contratos, e-mails, provas), seguir orientação jurídica, documentar em P12.8 (Incidentes), aprender: ajustar processos para prevenir recorrência |
| **Multa tributária** | Contatar contador, verificar se há erro (recorrer), pagar se procedente (não ignorar - juros e multas aumentam), revisar processo de emissão de NF/recolhimento de impostos (P13.3) |
| **Risco novo identificado** (não estava na matriz) | Adicionar na matriz imediatamente, avaliar (probabilidade × impacto), definir ação preventiva, implementar, comunicar equipe se necessário |

---

---

## P16.5 – Relacionamento com Consultorias Jurídicas e Contábeis

### Objetivo
Estabelecer relacionamento produtivo e estruturado com consultorias jurídicas e contábeis externas, garantindo suporte especializado em conformidade legal, tributária e prevenção de riscos.

### Momento
- Contínuo: Uso de serviços de contabilidade (mensal)
- Periódico: Consultoria jurídica (conforme necessidade)
- Preventivo: Antes de decisões importantes (nova contratação, novo serviço, contrato grande)

### Gatilho
- Fechamento mensal (P13.7 - enviar documentos para contador)
- Dúvida legal (contrato, disputa, LGPD)
- Mudança de legislação
- Revisão anual de riscos/contratos (P16.3, P16.4)

### Saídas
- Contabilidade em dia (notas fiscais, impostos, DRE)
- Consultorias jurídicas documentadas (parecer, orientação)
- Redução de riscos tributários e legais

### Papéis Envolvidos
- **Founder/Diretor**: Ponto de contato com consultorias
- **Financeiro**: Interface com contador (envio de documentos, pagamento)
- **Jurídico** (externo): Consultoria legal
- **Contador** (externo): Contabilidade, impostos, folha de pagamento

### Ferramentas
- E-mail, WhatsApp (comunicação)
- Drive compartilhado (troca de documentos)
- Notion (registro de consultorias, pareceres)

---

### Passo a Passo

#### Tarefa 1: Selecionar e Contratar Consultorias

##### Contador:
- **T1.1**: Critérios de seleção:
  - Especialização em empresas de serviços/digitais (não só comércio)
  - Conhecimento de regimes tributários (Simples, Lucro Presumido, Lucro Real)
  - Disponibilidade (responde rápido, não só no prazo fiscal)
  - Custo (mensal, geralmente R$300-800 para agências pequenas)
- **T1.2**: Contratar (P16.3 - usar contrato de prestação de serviços)
- **T1.3**: Definir escopo:
  - Emissão de notas fiscais (agência faz ou contador faz?)
  - Cálculo e recolhimento de impostos
  - Folha de pagamento (se CLT)
  - DRE mensal (P13.7)
  - Declarações obrigatórias (IRPJ, CSLL, PIS/COFINS, DEFIS - Simples)
  - Consultoria tributária (ex.: dúvidas sobre desenquadramento)

##### Advogado/Escritório Jurídico:
- **T1.4**: Critérios de seleção:
  - Especialização em Direito Empresarial, Contratos, Trabalhista
  - Conhecimento de LGPD (plus)
  - Modelo de cobrança:
    - Consultoria por demanda (hora): R$300-800/h (advogado júnior/pleno)
    - Retainer mensal (valor fixo por X horas/mês): R$2.000-5.000 (se demanda recorrente)
- **T1.5**: Quando contratar:
  - **Inicial** (estruturação da agência): Redigir contratos base (P16.3), Política de Privacidade (P16.2)
  - **Por demanda**: Quando há dúvida legal, disputa, ação judicial, revisão de contrato customizado
  - **Retainer** (se agência grande): Suporte contínuo

#### Tarefa 2: Estabelecer Rotina de Contabilidade

##### Mensal (P13.7):
- **T2.1**: No fechamento mensal (até dia 5 do mês seguinte):
  - Financeiro envia documentos ao contador:
    - Notas fiscais emitidas (PDF)
    - Notas fiscais recebidas (fornecedores)
    - Extratos bancários
    - Comprovantes de pagamento (salários, fornecedores)
    - Informações de novas contratações/demissões (se CLT)
- **T2.2**: Contador processa:
  - Calcula impostos devidos
  - Emite guias de recolhimento (DAS - Simples, ou guias separadas)
  - Envia guias para agência pagar (até vencimento, geralmente dia 20)
  - Gera DRE do mês (P13.7)
- **T2.3**: Financeiro paga impostos e registra (P13.5 - Custos)

##### Anual:
- **T2.4**: Declarações obrigatórias (contador faz):
  - DEFIS (Declaração de Informações Socioeconômicas e Fiscais - Simples Nacional)
  - IRPF (se Founder é pessoa física com pró-labore/distribuição de lucros)
  - DIRF (se tem funcionários CLT)

#### Tarefa 3: Estabelecer Rotina de Consultoria Jurídica

##### Preventiva:
- **T3.1**: Antes de:
  - Contratar CLT (revisar contrato de trabalho)
  - Assinar contrato grande com cliente (>R$10k/mês)
  - Lançar novo serviço (avaliar riscos legais)
  - Fazer parceria formal (redigir/revisar acordo)
  - Demitir por justa causa (validar motivo legal)
- **T3.2**: Consultar jurídico:
  - E-mail ou call explicando situação
  - Jurídico analisa e emite parecer (documento ou e-mail)
  - Agência decide com base em orientação

##### Reativa:
- **T3.3**: Quando:
  - Receber ação judicial (trabalhista, cível)
  - Receber notificação extrajudicial (ex.: cliente ameaça processar)
  - Disputa contratual (cliente/fornecedor não cumpre)
  - Dúvida urgente sobre LGPD (ex.: DSAR complexo)
- **T3.4**: Contatar jurídico imediatamente:
  - Fornecer toda documentação (contratos, e-mails, provas)
  - Seguir orientação (responder notificação, preparar defesa, negociar acordo)

#### Tarefa 4: Documentar Consultorias e Pareceres
- **T4.1**: Criar base no Notion:
  - **Consultorias Jurídicas**:
    - Data, assunto, advogado, parecer (resumo ou anexar documento), custo, status (concluída/pendente)
- **T4.2**: Sempre que consultar:
  - Registrar consulta
  - Salvar parecer (se escrito)
  - Registrar decisão tomada (seguiu ou não seguiu orientação)
- **T4.3**: Facilita futuras consultas (histórico) e auditorias

#### Tarefa 5: Revisar Relacionamento Anualmente
- **T5.1**: Uma vez por ano:
  - Avaliar contador:
    - Serviços foram entregues no prazo?
    - Qualidade (DRE está correto? Não houve erros fiscais?)
    - Atendimento (responde rápido?)
    - Custo está adequado? (comparar com mercado)
    - Decisão: manter ou trocar
  - Avaliar jurídico (se uso recorrente):
    - Qualidade das orientações (resolveram problemas?)
    - Custo (dentro do orçamento?)
    - Disponibilidade (atendem rápido?)
    - Decisão: manter ou trocar

---

### Checklist de Qualidade

- [ ] Contador contratado (contrato assinado P16.3)
- [ ] Advogado/jurídico contratado ou identificado (para consultas por demanda)
- [ ] Rotina mensal de contabilidade estabelecida (envio de docs, pagamento de impostos, DRE)
- [ ] Consultorias jurídicas documentadas (Notion)
- [ ] 100% das obrigações fiscais em dia (impostos pagos, declarações entregues)
- [ ] Revisão anual de relacionamento com consultorias (avaliar qualidade)

---

### Erros Comuns a Evitar

- Não ter contador (tentar fazer sozinho) — risco fiscal altíssimo, não vale a pena
- Não consultar jurídico preventivamente (esperar ter problema) — prevenir é mais barato que remediar
- Enviar documentos atrasados ao contador (atrasa impostos, gera multas) — enviar no prazo (até dia 5)
- Não documentar consultorias (perder histórico) — registrar sempre no Notion
- Ignorar orientação jurídica (achar que "sabe melhor") — se contratou especialista, seguir orientação
- Não revisar relacionamento (manter contador ruim por anos) — avaliar anualmente

---

### Métricas Relacionadas

| Métrica | Fórmula/Fonte | Frequência |
|---------|---------------|------------|
| **Taxa de Conformidade Fiscal** | (Obrigações em dia / Total obrigações) × 100 | Mensal (meta: 100%) |
| **Número de Consultorias Jurídicas** | Contagem de consultas | Anual |
| **Custo Total de Consultorias** | Soma(contador + jurídico) | Mensal, P13.5 |
| **Tempo Médio de Resposta do Contador** | Média(data resposta − data solicitação) | Trimestral |

---

### Automações Python

| ID | Gatilho | Ação |
|----|---------|------|
| **A70** | Dia 5 de cada mês | Alerta para Financeiro enviar documentos ao contador |
| **A71** | Dia 15 de cada mês | Alerta para Financeiro pagar impostos (vencimento geralmente dia 20, lembrete 5 dias antes) |

---

### Templates Associados

- **Checklist de Envio para Contador (Mensal)**:
  ```
  ENVIO PARA CONTADOR: [Mês/Ano]
  Data de envio: [Data]

  DOCUMENTOS:
  - [ ] Notas fiscais emitidas (PDF de todas as NFs do mês)
  - [ ] Notas fiscais recebidas (fornecedores)
  - [ ] Extratos bancários (todas as contas)
  - [ ] Comprovantes de pagamento (salários, pró-labore, fornecedores)
  - [ ] Novas contratações (nome, CPF, data de admissão, salário)
  - [ ] Demissões (nome, data de demissão)
  - [ ] Outras informações relevantes: [Descrever]

  ENVIADO POR:
  - [ ] E-mail para [e-mail do contador]
  - [ ] Upload em Drive compartilhado

  PRAZO DE RETORNO: [Data esperada de recebimento de DRE e guias]
  ```

- **Template de Solicitação de Consultoria Jurídica**:
  ```
  Assunto: Consultoria Jurídica - [Assunto]

  Olá [Nome do Advogado],

  Precisamos de orientação jurídica sobre [assunto resumido].

  CONTEXTO:
  [Descrição detalhada da situação, histórico, partes envolvidas]

  DÚVIDA/QUESTÃO:
  [O que precisa ser decidido? Qual orientação buscamos?]

  DOCUMENTOS ANEXOS:
  - [Contrato]
  - [E-mails]
  - [Outros]

  URGÊNCIA:
  [Urgente (resposta em 24h) / Normal (resposta em 3-5 dias)]

  Aguardo retorno.

  Atenciosamente,
  [Nome]
  [Agência]
  ```

---

### Fluxos de Exceção

| Situação | Ação |
|----------|------|
| **Contador entrega DRE/guias atrasado** | Cobrar (e-mail/call), se recorrente (>2 meses): considerar trocar contador |
| **Contador comete erro fiscal** (guia errada, valor errado) | Notificar imediatamente, contador deve corrigir sem custo adicional, se erro gera multa: contador deve arcar (depende de contrato) |
| **Advogado dá orientação que agência não concorda** | Discutir argumentos, entender melhor, buscar segunda opinião (outro advogado) se necessário, mas ponderar: especialista geralmente tem razão |
| **Custo de consultorias fica muito alto** (>10% do faturamento) | Avaliar: (1) Há muitos problemas (melhorar processos para reduzir demanda), (2) Contador/jurídico está cobrando caro demais (comparar com mercado, negociar ou trocar) |

---

---

## Integração de P16 com Outros Processos

| Processo | Integração |
|----------|------------|
| **P6 (Produção de Materiais)** | Copy/criativos devem seguir P16.1 (Políticas de Anúncios) |
| **P8 (Implementação/QA)** | QA (P8.2) inclui checklist de políticas (P16.1) e LGPD (P16.2) |
| **P12.1 (Anúncios Reprovados)** | Conectado a P16.1 (causa raiz: violação de políticas) |
| **P13.2 (Contratos Clientes)** | Baseado em P16.3 (Gestão de Contratos) e revisado por P16.5 (Jurídico) |
| **P13.3 (Faturamento)** | Notas fiscais enviadas a contador (P16.5) mensalmente |
| **P13.7 (Fechamento Financeiro)** | Documentos enviados a contador (P16.5), DRE recebido |
| **P14.1 (Onboarding)** | Contratos de trabalho baseados em P16.3, revisados por P16.5 (Jurídico) |
| **P14.7 (Offboarding)** | Rescisão conforme P16.3 (cláusulas de contrato) e P16.5 (orientação trabalhista) |
| **P15.2 (Nomeação)** | Não usar marcas registradas de terceiros (P16.4 - risco de PI) |
| **P15.4 (Acessos)** | Segurança de dados conectada a P16.2 (LGPD) |
| **P17 (Qualidade/Melhoria)** | Revisão anual de riscos (P16.4), contratos (P16.3), relacionamento com consultorias (P16.5) |

---

## Métricas Consolidadas de P16

| Métrica | Fórmula/Fonte | Frequência | Meta |
|---------|---------------|------------|------|
| **Taxa de Reprovação de Anúncios** | (Reprovados / Publicados) × 100 | Mensal | <2% |
| **% de Formulários com Consentimento LGPD** | (Com checkbox / Total) × 100 | Trimestral | 100% |
| **Tempo Médio de Resposta a DSAR** | Média(data resposta − data solicitação) | Por DSAR | ≤15 dias |
| **% de Contratos com Templates** | (Usando template / Total) × 100 | Trimestral | 100% |
| **Número de Ações Judiciais** | Contagem de processos | Anual | 0 |
| **Valor de Multas/Sanções** | Soma(multas tributárias, trabalhistas, LGPD) | Anual | R$0 |
| **Taxa de Conformidade Fiscal** | (Obrigações em dia / Total) × 100 | Mensal | 100% |
| **% de Riscos com Ações Preventivas** | (Riscos mitigados / Total alta prioridade) × 100 | Trimestral | 100% |

---

## Documentos e Ferramentas de P16

| Documento/Ferramenta | Localização | Responsável por Manter |
|----------------------|-------------|------------------------|
| **Checklist de Políticas de Anúncios** | Notion (P8.2 QA) | Gestor de Tráfego (aplicar), Founder (atualizar) |
| **Política de Privacidade** | Site, LPs (link rodapé) | Founder + Jurídico (revisar) |
| **Registro de DSARs** | Notion (DSARs) | Administrativo/Founder |
| **Templates de Contratos** | Notion (P15.5), Drive | Jurídico (criar/revisar), Founder (usar) |
| **Matriz de Riscos Legais** | Notion ou planilha | Founder + Jurídico (anual) |
| **Registro de Consultorias Jurídicas** | Notion (Consultorias) | Founder/Administrativo |
| **Documentos Contábeis** | Drive compartilhado com contador | Financeiro (enviar), Contador (processar) |

---

## Resumo de P16

**P16 – Compliance, Jurídico e Políticas** protege a agência e clientes através de:

1. **Adequação às políticas de anúncios** (P16.1): 100% em conformidade (Meta, Google), taxa de reprovação <2%
2. **Conformidade com LGPD** (P16.2): Política de Privacidade, consentimento, segurança, resposta a DSARs ≤15 dias
3. **Gestão de contratos** (P16.3): Templates revisados por jurídico, cláusulas essenciais, proteção mútua
4. **Prevenção de riscos legais** (P16.4): Matriz de riscos, ações preventivas, seguros (se aplicável)
5. **Relacionamento com consultorias** (P16.5): Contador (mensal), jurídico (preventivo/reativo), documentação estruturada

**Filosofia central**: Compliance não é burocracia, é proteção. Agências que operam em conformidade legal evitam multas, processos, bloqueios de contas e danos à reputação. Investir em compliance (contador, jurídico, processos) é investir em sustentabilidade de longo prazo.

**Próximos passos**: Implementar checklist de políticas em P8.2 (QA). Publicar Política de Privacidade (site, LPs). Revisar contratos com jurídico (P16.3). Criar matriz de riscos (P16.4). Estabelecer rotina mensal com contador (P16.5). Treinar equipe em políticas de anúncios (P14.3). Implementar automações Python (A64-A71).

---

**Status**: ✅ **P16 - Completo** | Próximo: **P17 – Qualidade & Melhoria Contínua** (último processo de suporte!)
