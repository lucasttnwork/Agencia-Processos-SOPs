# Guia Narrativo: Funcionamento Completo do Sistema de Agência Autônoma de Marketing (AMA)

Este documento explica, de forma simples e em português, como o sistema funciona por dentro. Ele descreve a lógica de cada componente, o fluxo de decisões e como os agentes de IA trabalham juntos para produzir resultados de marketing.

---

## O Que é Este Sistema?

Imagine que você pudesse contratar uma equipe completa de marketing — estrategista, redator, designer, mídia buyer, analista de dados — mas em vez de pessoas, você tem um software inteligente que faz tudo isso, 24 horas por dia, sem cansar.

Este sistema é exatamente isso: uma "agência virtual" que você opera através de uma conversa em um editor de código (como o Cursor ou Claude Code). Você dá instruções em linguagem natural, e o sistema executa todas as etapas necessárias para entregar campanhas de marketing completas.

---

## Capítulo 1: A Filosofia Central — "Passos Pequenos, Nunca Errar"

### O Problema dos Sistemas de IA Tradicionais

Quando você pede para uma IA fazer algo grande e complexo, como "crie toda a campanha de Black Friday para meu cliente", ela tende a falhar. Ela tenta fazer tudo de uma vez, se perde no meio do caminho, esquece detalhes e produz resultados inconsistentes.

### A Solução: Decomposição Máxima (MAKER)

Nosso sistema usa uma abordagem chamada "Decomposição Máxima" (do inglês Maximal Agentic Decomposition). Em vez de tentar fazer uma tarefa grande, o sistema quebra essa tarefa em centenas ou milhares de micro-tarefas. Cada micro-tarefa é tão simples que é quase impossível errar.

Por exemplo, a tarefa "criar campanha de Black Friday" seria decomposta em:
1. Ler o site do cliente.
2. Extrair o tom de voz da marca.
3. Identificar os 3 principais produtos.
4. Criar ângulo de persuasão "economia".
5. Criar ângulo de persuasão "urgência".
6. Escrever headline 1 para ângulo "economia".
7. Escrever headline 2 para ângulo "economia".
8. ... e assim por diante, até centenas de passos.

Cada passo é executado por um agente especializado, um de cada vez, com verificação.

---

## Capítulo 2: O Sistema de Votação — "O Congresso de Agentes"

### Por Que Votar?

Mesmo uma tarefa simples pode ter múltiplas respostas válidas. Se eu pedir para três redatores escreverem um título de anúncio, os três provavelmente escreverão títulos diferentes. Qual é o melhor?

### Como Funciona a Votação

Para cada tarefa criativa (escrever copy, escolher imagem, definir ângulo), o sistema não usa apenas um agente. Ele usa vários agentes em paralelo, cada um gerando sua própria versão.

Depois, um grupo de "agentes críticos" analisa as opções e vota. O processo funciona assim:

1. **Geração Paralela**: 3 agentes "redatores" recebem a tarefa "escreva um headline para o produto X com foco em economia".
2. **Produção**: Cada um produz uma versão diferente:
   - Agente A: "Economize 40% nesta Black Friday"
   - Agente B: "Seu bolso vai agradecer: descontos de até 40%"
   - Agente C: "A maior promoção do ano chegou"
3. **Votação**: 5 agentes "críticos" analisam as 3 opções e votam qual é a melhor, com base em critérios como clareza, apelo emocional e alinhamento com a marca do cliente.
4. **Seleção**: A opção que receber mais votos é a escolhida.

### O Que Acontece Quando Não Há Consenso?

Se os votos ficarem muito divididos (por exemplo, 2 votos para A, 2 votos para B, 1 para C), o sistema identifica isso como uma "bandeira vermelha" (red flag). Isso significa que a decisão é ambígua demais para ser automática.

Nesse caso, o sistema pausa essa tarefa específica e notifica você, o operador humano, dizendo algo como: "Não consegui decidir entre estas duas opções de headline. Qual você prefere?"

Você escolhe, e o sistema continua executando as próximas tarefas.

---

## Capítulo 3: O "Harness" — O Sistema Operacional da Agência

### O Problema de Tarefas Longas

Se você pedir para uma IA trabalhar por horas seguidas em um projeto grande, ela vai eventualmente "se perder". A conversa fica muito longa, ela esquece o que já fez, e começa a cometer erros ou repetir trabalho.

### A Solução: Ambiente Gerenciado

O Harness (ou "arnês") é o sistema que gerencia todo o estado da agência. Ele funciona como o "escritório" onde os agentes trabalham. Esse escritório tem:

1. **Um Arquivo de Progresso (progress.json)**: Uma lista de todas as tarefas, indicando quais estão pendentes, quais estão em andamento e quais estão concluídas. O agente sempre consulta esse arquivo antes de começar a trabalhar, para saber exatamente o que fazer a seguir.

2. **Um Repositório Git**: Todas as alterações feitas pelo sistema são "commitadas" (salvas) em um repositório de código. Isso significa que nunca perdemos trabalho e podemos voltar atrás se algo der errado.

3. **Arquivos de Conhecimento**: A pasta do cliente contém tudo o que o sistema sabe sobre aquele cliente: tom de voz, regras da marca, assets visuais, histórico de campanhas.

### O Ciclo de Trabalho

O sistema trabalha em ciclos:

1. **Escanear**: O sistema lê o arquivo `progress.json` e encontra a próxima tarefa marcada como "pendente".
2. **Executar**: Ele chama o agente apropriado para executar a tarefa (por exemplo, um agente redator para escrever copy).
3. **Verificar**: Se necessário, o sistema "vota" para escolher a melhor opção ou verifica se o resultado está correto.
4. **Registrar**: O resultado é salvo no sistema de arquivos, o `progress.json` é atualizado para marcar a tarefa como "concluída", e um commit é feito no Git.
5. **Repetir**: O ciclo recomeça com a próxima tarefa pendente.

Esse processo pode rodar por horas ou dias, completando centenas de tarefas sem perder o fio da meada.

---

## Capítulo 4: Os Papéis dos Agentes

O sistema é composto por vários tipos de agentes, cada um especializado em uma função. Pense neles como funcionários virtuais da sua agência.

### O Estrategista (Gerente)

Este é o agente que "pensa grande". Quando você diz "lance uma campanha para o cliente X", o Estrategista é quem quebra essa meta em centenas de micro-tarefas e as escreve no arquivo `progress.json`.

Ele é responsável por:
- Entender o objetivo do operador humano.
- Decompor metas em tarefas atômicas.
- Priorizar a ordem de execução.

### Os Criadores (Trabalhadores)

Estes são os agentes que produzem conteúdo. Existem vários subtipos:

- **Redator de Copy**: Escreve headlines, textos de anúncios, emails, scripts de vídeo.
- **Designer de Briefing**: Cria instruções detalhadas para geração de imagens (a serem enviadas para APIs como DALL-E ou Midjourney).
- **Roteirista de Vídeo**: Escreve scripts com estrutura de hook, corpo e CTA.

Cada Criador trabalha em uma única micro-tarefa de cada vez e gera múltiplas versões para votação.

### Os Críticos (Juízes)

Estes agentes não criam, eles avaliam. Seu trabalho é receber as opções geradas pelos Criadores e votar na melhor.

Os Críticos usam critérios específicos para julgar, como:
- "Esta copy está alinhada com o tom de voz do cliente?"
- "Esta imagem viola alguma política de anúncios da Meta?"
- "Este headline é claro e direto?"

### O Espião (Analista de Mercado)

Este agente tem um trabalho único: observar os concorrentes. Ele escaneia a Biblioteca de Anúncios da Meta regularmente para ver o que os concorrentes estão fazendo.

Quando ele identifica uma tendência interessante (por exemplo, "os concorrentes estão usando muitos vídeos com depoimentos"), ele registra essa informação no arquivo `market_intel/trends.json`.

Isso pode disparar novas tarefas. Por exemplo, o Estrategista pode ler esse arquivo e criar tarefas como: "Gerar 3 roteiros de vídeo de depoimento para o cliente Y, inspirados na tendência Z."

### O Analista de Performance

Este agente é responsável pelo ciclo de melhoria contínua. Ele:
1. Coleta dados de performance das campanhas (ROAS, CTR, CPC, etc.).
2. Identifica quais anúncios estão performando bem e quais estão falhando.
3. Salva os padrões de sucesso em um arquivo de "melhores práticas".
4. Cria novas tarefas para pausar anúncios ruins e iterar sobre os bons.

---

## Capítulo 5: O Ciclo de Vida de um Projeto de Cliente

Vamos acompanhar como o sistema funciona na prática, desde o momento em que um novo cliente é cadastrado até a otimização contínua de suas campanhas.

### Fase 1: Onboarding — Conhecendo o Cliente

Você, o operador, diz ao sistema: "Aqui está o site do novo cliente: www.exemplo.com, e aqui estão 3 PDFs com informações sobre os produtos deles."

O sistema imediatamente inicia o processo de "Absorção":

1. Um agente lê o site do cliente, página por página.
2. Outro agente analisa os PDFs.
3. Um agente especializado extrai o "tom de voz" da marca: é formal ou informal? Técnico ou acessível? Divertido ou sério?
4. Outro agente identifica os principais produtos ou serviços.
5. Os resultados são salvos na pasta `/clients/exemplo/brand_voice/`.

Ao final, o sistema tem um "dossiê" completo sobre o cliente.

### Fase 2: Planejamento — Definindo a Estratégia

O Estrategista entra em ação. Ele cria um plano de campanha detalhado:

1. Define os ângulos de persuasão (economia, urgência, exclusividade, etc.).
2. Define a estrutura do funil (anúncio → landing page → email de follow-up).
3. Cria um calendário de lançamento.
4. Escreve todas as tarefas necessárias no `progress.json`.

Por exemplo, o arquivo pode conter:
```
- [pendente] Escrever headline para ângulo "economia" - versão 1
- [pendente] Escrever headline para ângulo "economia" - versão 2
- [pendente] Escrever headline para ângulo "economia" - versão 3
- [pendente] Votar no melhor headline para ângulo "economia"
- [pendente] Escrever corpo do anúncio para ângulo "economia"
... (centenas de linhas)
```

### Fase 3: Produção — A Fábrica de Conteúdo

Agora o sistema começa a executar as tarefas, uma a uma.

Para cada tarefa criativa, ele usa a lógica de votação:
1. Gera 3 versões em paralelo.
2. Os Críticos votam.
3. A melhor versão é selecionada e salva.

O output é salvo em arquivos organizados, como:
- `/clients/exemplo/campaigns/black_friday/copy/headlines.json`
- `/clients/exemplo/campaigns/black_friday/images/briefs/`

### Fase 4: Configuração Técnica

Antes de lançar os anúncios, o sistema verifica a infraestrutura técnica:

1. Gera o código para instalação do Pixel da Meta.
2. Verifica se o domínio está verificado na conta de negócios.
3. Cria uma estrutura de UTMs para rastreamento.

### Fase 5: Lançamento

O sistema se conecta à API de Marketing da Meta e:
1. Cria a campanha.
2. Cria os conjuntos de anúncios (Ad Sets) com as audiências definidas.
3. Cria os anúncios individuais com a copy e as imagens/vídeos selecionados.
4. Define o orçamento e as regras de otimização.

Antes de ativar, ele faz uma "verificação final": usa ferramentas de automação de navegador para abrir o Gerenciador de Anúncios e confirmar que tudo está configurado corretamente.

### Fase 6: Monitoramento e Otimização

Uma vez que a campanha está no ar, o trabalho não para.

Diariamente:
1. O Analista de Performance coleta os dados de performance.
2. Ele identifica quais anúncios estão abaixo do threshold de performance (por exemplo, CPA > R$50).
3. Ele cria tarefas para pausar esses anúncios.
4. Ele identifica os anúncios campeões e cria tarefas para "iterar" sobre eles (criar novas versões com pequenas variações).

Semanalmente:
1. O Espião verifica a Biblioteca de Anúncios para ver se os concorrentes lançaram algo novo.
2. O sistema gera um relatório de performance para enviar ao cliente.

Continuamente:
1. Os padrões de sucesso são salvos na memória de longo prazo.
2. Esses padrões influenciam futuras criações. Por exemplo, se headlines com números performam melhor, o sistema aprende a preferir headlines com números.

---

## Capítulo 6: Os Pontos de Verificação Humana

Apesar de ser autônomo, o sistema não é uma "caixa preta" que faz tudo sozinho. Existem momentos críticos onde ele para e pede sua aprovação.

### Quando o Sistema Pede Ajuda?

1. **Aprovação Final de Copy**: Antes de publicar qualquer anúncio, a versão final é apresentada a você para revisão. Você pode aprovar, pedir ajustes ou reescrever.

2. **Aumento de Orçamento**: Se o sistema quiser aumentar o orçamento em mais de 50%, ele precisa da sua aprovação. Isso evita gastos descontrolados.

3. **Decisões Ambíguas**: Se o Congresso de Críticos não conseguir decidir (votos muito divididos), o sistema para e pergunta sua opinião.

4. **Conteúdo Sensível**: Se a copy envolver claims de saúde, finanças ou qualquer assunto regulamentado, o sistema marca para revisão humana obrigatória.

5. **Materiais do Cliente**: Propostas, relatórios e contratos são sempre apresentados para você antes de serem enviados ao cliente.

---

## Capítulo 7: A Memória e a Auto-Melhoria

O sistema não apenas executa, ele aprende.

### Memória de Curto Prazo

O arquivo `progress.json` funciona como a memória de trabalho. Ele sabe o que está fazendo agora e o que vem a seguir.

### Memória de Longo Prazo

Existem dois tipos de memória de longo prazo:

1. **Memória do Cliente**: Tudo sobre um cliente específico é salvo na pasta dele. Isso inclui tom de voz, histórico de campanhas, e o que funcionou ou não para aquele cliente.

2. **Memória Global (Best Practices)**: Padrões que funcionam para múltiplos clientes são salvos em um arquivo central. Por exemplo:
   - "Headlines com números tendem a ter CTR 15% maior."
   - "Vídeos com hook nos primeiros 2 segundos têm maior taxa de conclusão."
   - "A cor vermelha em CTAs aumenta conversões em 10%."

Essa memória global é consultada pelos agentes Criadores e Críticos para informar suas decisões.

### O Ciclo de Melhoria

1. O sistema executa tarefas.
2. Os resultados são medidos (performance real dos anúncios).
3. Os padrões de sucesso são extraídos e salvos na memória.
4. Novas tarefas são executadas usando esses padrões.
5. Repetir indefinidamente.

Com o tempo, o sistema fica cada vez melhor, porque ele aprende com seus próprios resultados.

---

## Conclusão: O Que Você Precisa Saber

Este sistema é projetado para ser:

1. **Confiável**: A decomposição máxima e o sistema de votação garantem que erros são raros e corrigidos rapidamente.
2. **Autônomo**: Ele pode trabalhar por horas ou dias sem intervenção, executando centenas de tarefas.
3. **Transparente**: Tudo é salvo em arquivos e commits de Git. Você sempre sabe exatamente o que foi feito.
4. **Evolutivo**: Ele aprende com os resultados e melhora continuamente.
5. **Controlado**: Checkpoints humanos garantem que você está sempre no comando das decisões críticas.

Você, como operador, é o "dono da agência". Você define os objetivos, aprova as decisões importantes e colhe os resultados. O sistema cuida de toda a execução.
