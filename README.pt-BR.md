# LearningOps

[English](README.md) | **Português**

**Um sistema de aprendizagem com IA para transformar conversas de estudo em desenvolvimento contínuo, observável e versionado.**

## Por que usar o LearningOps?

Você pode abrir o ChatGPT e simplesmente começar a perguntar sobre qualquer assunto. Isso funciona bem para respostas isoladas, mas estudar por meses exige algo diferente: continuidade, método, critérios para saber o que realmente foi aprendido, revisão de gaps e um plano que evolui com você.

O LearningOps adiciona essa camada.

Ele transforma o ChatGPT de um chatbot genérico em um **runtime de aprendizagem guiada**: existe um prompt de Projeto pronto, conectado a métodos, specs e estado versionado no GitHub. Você configura uma vez e depois pode simplesmente abrir um chat e estudar.

## O que o LearningOps entrega

- **Plano de estudo adaptativo** — organiza o caminho a partir do objetivo, pré-requisitos, competências e evidências, em vez de seguir apenas uma lista fixa de conteúdos.
- **PDI baseado em evidências** — mantém poucas prioridades de desenvolvimento, escolhidas pelos gaps mais relevantes para o objetivo atual.
- **Observed Mastery** — estima apenas o que você demonstrou; exposição, cargo, certificação ou autopercepção não contam como domínio.
- **Mapa de competências** — separa amplitude generalista, profundidade especialista, aplicação, transferência, design, diagnóstico, retenção e outras capacidades observáveis.
- **Evidence Lineage** — cada evolução pode ser rastreada até a atividade, resposta, assistência recebida, momento e versão do sistema.
- **Knowledge Graph** — conecta conceitos, mecanismos, pré-requisitos, trade-offs, alternativas e falhas sem misturar conhecimento do domínio com estado do aluno.
- **Revisão e retenção** — recupera conceitos anteriores, mistura tópicos e revisita conhecimento frágil ao longo do tempo.
- **Learning Cockpit** — oferece uma visão unificada de domínios, PDI, gaps, competências, evidências e evolução.
- **Currículo profissional baseado em evidências** — pode transformar capacidades realmente demonstradas em afirmações profissionais rastreáveis, sem inventar senioridade ou experiência.

## O método de aprendizagem

O LearningOps não depende de uma única técnica. Ele combina métodos complementares e escolhe os necessários conforme o momento do estudo:

- **Socratic Learning** — usa uma pergunta relevante por vez para revelar raciocínio, hipóteses e trade-offs antes de entregar respostas prontas.
- **Microlearning** — introduz o menor conceito útil possível e pede uma ação do aluno antes de continuar.
- **Retrieval Practice** — faz você recuperar conhecimento sem mostrar a resposta primeiro, fortalecendo lembrança independente.
- **Spaced Revisit** — revisita conhecimento depois de intervalos; um acerto isolado não é tratado como domínio permanente.
- **Interleaving** — mistura conceitos relacionados para treinar a escolha do princípio correto sem avisar previamente qual assunto está sendo testado.
- **Problem-Based Learning** — ensina por problemas realistas com contexto, requisitos e restrições.
- **Pareto Two-Pass** — primeiro cria o mapa mental com os conceitos de maior poder explicativo; depois retorna para internals, edge cases, performance, falhas e trade-offs.
- **Analogy Bridging** — usa `analogia → intuição → conceito técnico → limite da analogia`, evitando que simplificações virem misconceptions.
- **Error Reverse Engineering** — aprende também por erros comuns, mitos, anti-patterns e decisões que parecem corretas mas quebram sob restrições reais.
- **Deliberate Practice** — ataca um gap específico com uma tarefa ligeiramente acima do desempenho independente atual e feedback proporcional ao erro.
- **System Design Practice** — exige levantamento de requisitos, desenho, hipóteses, trade-offs, falhas e adaptação da solução.
- **Adversarial Learning** — desafia soluções com advogado do diabo, mudança de restrições, arquitetura problemática e debugging.
- **Transfer Practice** — testa se o princípio aprendido funciona em um cenário diferente daquele usado durante a explicação.
- **Metacognitive Regulation** — usa `planejar → monitorar → avaliar → adaptar` para ajustar a estratégia de estudo com base em evidência recorrente.

### Ciclo operacional

O runtime escolhe apenas as etapas úteis para o momento:

`ORIENTAR → MAPEAR → APRENDER → RECUPERAR → APLICAR → PROJETAR → DEFENDER → ESTRESSAR → DEPURAR → APROFUNDAR → CONECTAR → REFLETIR → REVISITAR`

O ciclo não é um checklist obrigatório. Ele se adapta à competência, ao gap e à evidência disponível.

## Como o prompt funciona

O LearningOps começa com um **prompt de Projeto do ChatGPT**.

Esse prompt não contém o sistema inteiro. Ele funciona como um orquestrador: define as regras essenciais, valida acesso ao GitHub e carrega apenas as specs necessárias para a tarefa atual.

Isso segue o princípio de **responsabilidade única**:

- o prompt orquestra;
- cada spec define uma responsabilidade;
- schemas validam registros;
- o Core contém o sistema;
- o Workspace contém o estado observado do aluno;
- o Cockpit apenas apresenta o estado governado.

Prompt oficial:

https://github.com/euvictorhfs/LearningOps/blob/main/runtime/CHATGPT_PROJECT_INSTRUCTIONS.md

## Instalação no ChatGPT

### Passo 1 — Crie o Projeto

No ChatGPT, crie um Projeto chamado:

`LearningOps`

Configure a memória como **somente do projeto**.

### Passo 2 — Conecte o GitHub

Dê ao ChatGPT acesso aos dois repositórios:

- Core público: https://github.com/euvictorhfs/LearningOps
- Workspace privado: https://github.com/euvictorhfs/LearningOps-workspace

O Core guarda o sistema. O Workspace guarda seu estado de aprendizagem.

### Passo 3 — Adicione a instrução do Projeto

Abra:

https://github.com/euvictorhfs/LearningOps/blob/main/runtime/CHATGPT_PROJECT_INSTRUCTIONS.md

Copie o conteúdo completo para as **Instruções do Projeto** no ChatGPT.

Você faz isso uma vez.

### Passo 4 — Crie o primeiro chat

Crie um chat chamado:

`Sistema LearningOps`

Esse chat é usado para:

- validar a instalação e o acesso aos repositórios;
- manutenção do sistema;
- arquitetura;
- atualização de specs e schemas;
- versionamento;
- branches, commits, Pull Requests e merges quando você autorizar.

Envie:

> Inicialize o LearningOps e valide minha instalação. Confirme quais repositórios e branches `main` você realmente consegue acessar. Não faça alterações.

O ChatGPT deve testar o acesso real. Ele não deve assumir que tem acesso apenas porque recebeu um link.

### Passo 5 — Comece a estudar

Crie outro chat dentro do mesmo Projeto e dê a ele apenas o nome do campo que você quer estudar.

Exemplos:

`Arquitetura Moderna de Dados`

`Engenharia de Prompt`

`Sistemas Distribuídos`

Não é necessário usar prefixos, números de sessão ou comandos de bootstrap.

Comece naturalmente:

> Quero aprender Arquitetura Moderna de Dados.

O LearningOps deve carregar o estado existente, começar em **0% de observed mastery** quando o domínio for novo, montar o caminho inicial e conduzir o estudo usando o método oficial.

## Regra simples de chats

- **`Sistema LearningOps`** = instalação, governança e manutenção.
- **Qualquer outro chat** = estudo do tema indicado pelo nome/contexto do chat.

Internamente o sistema pode registrar checkpoints e evidências, mas você não precisa gerenciar essa complexidade no ChatGPT.

## Durante o estudo

O comportamento padrão é pequeno e interativo:

1. um microconceito ou problema;
2. uma pergunta relevante;
3. sua tentativa;
4. uma pista pequena se necessário;
5. nova tentativa;
6. explicação completa quando necessário;
7. evidência e próximo passo atualizados apenas quando justificável.

Quando você pedir uma explicação direta em vez de uma avaliação, o sistema pode responder diretamente.

## Zero Baseline

Todo novo campo começa em:

`0% observed mastery`

Experiência anterior, cargo, certificações, confiança ou memória de conversa não inicializam domínio.

Conhecimento prévio acelera o caminho somente depois de ser demonstrado.

## GitHub é a memória durável

O ChatGPT executa o estudo. O GitHub preserva o sistema e o histórico validado.

- `euvictorhfs/LearningOps` — Core público e versionado.
- `euvictorhfs/LearningOps-workspace` — estado privado e versionado do aluno.

A memória do Projeto ajuda na continuidade, mas não substitui evidência persistida.

## Para quem quer entender a arquitetura

As regras detalhadas estão em [`specs/`](specs/).

Principais specs:

- [Generative AI Architecture](specs/genai-architecture-spec.md)
- [Learning Method](specs/learning-method-spec.md)
- [Learning](specs/learning-spec.md)
- [Competency Model](specs/competency-model-spec.md)
- [Curriculum](specs/curriculum-spec.md)
- [PDI](specs/pdi-spec.md)
- [Evidence & Lineage](specs/evidence-spec.md)
- [Mastery Computation](specs/mastery-spec.md)
- [Knowledge Graph](specs/knowledge-graph-spec.md)
- [Session Runtime](specs/session-runtime-spec.md)
- [Learning Cockpit](specs/cockpit-spec.md)
- [Evidence-Based Resume](specs/evidence-based-resume-spec.md)
- [Governance](specs/governance-spec.md)

## Princípio central

**Não medir quanto conteúdo foi apresentado. Medir o que a pessoa consegue fazer com o conhecimento, com evidência e lineage.**
