# LearningOps

[English](README.md) | **Português**

**Um sistema Human–AI de aprendizagem contínua, guiada por métodos, evidências e desenvolvimento observável.**

LearningOps transforma um Projeto do ChatGPT em um ambiente persistente de aprendizagem.

Você configura o sistema uma vez. Depois, cria um chat com o nome daquilo que quer aprender e começa.

## Por que LearningOps?

Perguntas isoladas funcionam bem em um chatbot genérico. Estudar por semanas, meses ou anos exige continuidade, método, plano, revisão, retenção, competências observáveis, PDI, evidências, histórico, adaptação e lineage.

LearningOps adiciona essa camada: o ChatGPT executa o runtime de aprendizagem, enquanto o GitHub preserva o sistema e o estado validado.

## O que o LearningOps entrega

- **Learning Planner** — contrato versionado do que foi acordado estudar em cada domínio.
- **Currículo adaptativo** — organiza capacidades e sequência a partir de objetivo, pré-requisitos e evidências.
- **PDI global baseado em evidências** — prioriza gaps entre todos os campos ativos.
- **Observed Mastery** — representa somente capacidades realmente demonstradas.
- **Competency Model** — separa breadth, depth, aplicação, transferência, design, diagnóstico, retenção e comunicação.
- **Evidence Lineage** — toda evolução relevante pode ser rastreada até origem, momento, assistência e versão do sistema.
- **Knowledge Graph** — conecta conceitos, mecanismos, pré-requisitos, alternativas, trade-offs e failure modes.
- **Knowledge Debt** — registra dependências importantes ainda não demonstradas na profundidade necessária.
- **Retention & Review** — revisita conhecimento ao longo do tempo.
- **Learning Cockpit** — visão única de domínios, Planner, PDI, gaps, evidências e evolução.
- **Professional Profile** — verdade profissional estruturada e sustentada por evidências.
- **Evidence-Based Résumé** — currículo para pessoas, ATS e sistemas de IA sem inventar experiência.

## LearningOps começa com um prompt, mas não é só um prompt

O prompt oficial do Projeto funciona como um **orquestrador**. Ele define papéis, invariantes, roteamento, fontes autoritativas e quais specs carregar.

A inteligência detalhada permanece versionada em specs e schemas no GitHub.

Isso evita um megprompt monolítico e mantém o sistema testável e portátil.

## Single Responsibility Principle

Single Responsibility é um pilar do LearningOps.

- **Generative AI Architecture** → arquitetura, contexto, prompts, ferramentas e evals.
- **Learning Method** → como ensinar.
- **Competency Model** → o que significa demonstrar competência.
- **Curriculum** → quais capacidades formam um domínio e como sequenciá-las.
- **Planner** → qual formação foi aprovada para um learner em um domínio.
- **PDI** → quais prioridades de desenvolvimento possuem maior valor agora.
- **Evidence** → o que conta como evidência.
- **Mastery** → como evidências sustentam estado observado.
- **Knowledge Graph** → como conhecimento e relações são modelados.
- **Session Runtime** → comportamento dos chats.
- **Workspace Runtime** → persistência do estado humano.
- **Automation** → manutenção recorrente segura.
- **Cockpit** → apresentação do estado governado.
- **Professional Profile** → verdade profissional estruturada.
- **Resume Generation** → publicação dessa verdade para oportunidades.

## Os três tipos de chat

### `LearningOps OS`

Responsabilidade: **manter o sistema**.

Use para instalação, validação do GitHub, Core, Workspace, arquitetura, specs, schemas, evals, migrations, versionamento, Cockpit, automações, branches, commits, PRs e merges autorizados.

Neste chat, o assistente atua como **Generative AI Engineering Architect**.

**`LearningOps OS` nunca é uma sessão de estudo.**

Na primeira mensagem do usuário, o chat deve apresentar seu papel e exemplos como:

- `Valide minha instalação.`
- `Verifique o Core e o Workspace.`
- `Revise a arquitetura.`
- `Configure o Cockpit.`
- `Configure as automações.`
- `Prepare uma mudança para revisão.`

### `My Learning`

Responsabilidade: **visão transversal do learner**.

Use para:

- PDI global;
- gaps de maior prioridade;
- comparação entre domínios;
- competências demonstradas;
- retention e knowledge debt;
- professional profile;
- résumé/currículo profissional;
- interpretação transversal do Cockpit.

Na primeira mensagem do usuário, deve apresentar seu papel e exemplos como:

- `Como está meu PDI?`
- `Quais são meus maiores gaps?`
- `O que devo priorizar agora?`
- `Compare minha evolução entre os domínios.`
- `Atualize meu perfil profissional.`
- `Gere meu currículo para esta vaga.`

### Chats de estudo

Use apenas o nome natural do campo:

`Modern Data Architecture`

`Prompt Engineering`

`Distributed Systems`

O nome do campo pode estar no idioma do usuário.

Nesses chats, o assistente atua como **Adaptive Technical Tutor**.

Na primeira mensagem do usuário — qualquer que seja ela — o chat deve apresentar brevemente seu papel e tornar as ações descobríveis. Se a mensagem já trouxer um tema ou pedido claro, a introdução deve ser curta e o pedido deve continuar imediatamente.

Exemplos de ações:

- definir ou refinar o Planner;
- aprender um tópico;
- praticar problemas e system design;
- revisar conhecimento;
- fechar o Planner;
- registrar evidências quando o sistema oferecer.

## Mensagens bilíngues

Os nomes canônicos permanecem `LearningOps OS` e `My Learning`.

O runtime detecta o idioma do usuário e responde nele. As mensagens do sistema devem possuir comportamento semanticamente equivalente em PT-BR e EN.

## Método de aprendizagem

LearningOps combina métodos complementares:

- Socratic Learning;
- Microlearning;
- Retrieval Practice;
- Spaced Revisit;
- Interleaving;
- Problem-Based Learning;
- Pareto Two-Pass;
- Analogy Bridging;
- Error Reverse Engineering;
- Deliberate Practice;
- System Design Practice;
- Adversarial Learning;
- Transfer Practice;
- Metacognitive Regulation.

Ciclo adaptativo:

`ORIENT → MAP → LEARN → RETRIEVE → APPLY → DESIGN → DEFEND → STRESS → DEBUG → DEEPEN → CONNECT → REFLECT → REVISIT`

Não é um checklist. O runtime escolhe o menor subconjunto útil.

## Zero Baseline

Todo novo campo começa em:

`0% observed mastery`

Experiência anterior, cargo, certificações, confiança ou memória de chat não inicializam domínio. Conhecimento prévio pode acelerar o caminho depois de demonstrado.

## Evidence before progress

Exposição não é mastery.

LearningOps procura comportamentos observáveis como explicar, distinguir, aplicar, diagnosticar, comparar, defender, projetar, transferir e recuperar conhecimento após intervalo.

Em avaliação, preserve:

`tentativa independente → menor pista útil → nova tentativa → explicação completa quando necessária`

O nível de assistência faz parte da evidência.

# Getting Started

## Passo 1 — Crie o Projeto

No ChatGPT, crie um Projeto chamado:

`LearningOps`

Configure a memória como **somente do projeto**.

## Passo 2 — Conecte o GitHub

Autorize acesso a:

- Core público: https://github.com/euvictorhfs/LearningOps
- Workspace privado: https://github.com/euvictorhfs/LearningOps-workspace

Core contém o sistema. Workspace contém o estado observado do learner.

## Passo 3 — Instale as Project Instructions

Abra:

https://github.com/euvictorhfs/LearningOps/blob/main/runtime/CHATGPT_PROJECT_INSTRUCTIONS.md

Copie o conteúdo completo para as **Instruções do Projeto**.

## Passo 4 — Crie `LearningOps OS`

Crie o primeiro chat com o nome:

`LearningOps OS`

Envie:

> Inicialize o LearningOps e valide minha instalação. Confirme quais repositórios e branches `main` você realmente consegue acessar. Não faça alterações.

O sistema deve testar o acesso real e nunca assumir capacidade apenas porque recebeu um link.

## Passo 5 — Inicialize o Workspace

Ainda em `LearningOps OS`, envie:

> Valide e inicialize meu LearningOps Workspace seguindo as specs atuais. Não invente nenhum dado sobre mim.

O sistema deve verificar estrutura, schemas, domínios, histórico, lineage, compatibilidade e permissões.

## Workspace — memória durável do learner

O Workspace privado preserva, conforme aplicável:

- Planners;
- domínios;
- checkpoints;
- evidências;
- mastery;
- PDI;
- gaps e misconceptions;
- knowledge debt;
- retention;
- learner graph;
- professional profile;
- Cockpit config/snapshots;
- histórico e lineage.

### Guardrail fundamental

**Planner, PDI, mastery, evidence, curriculum state e knowledge graph nunca devem depender exclusivamente da memória do chat.**

`Chat → runtime`

`Workspace → persisted learner state`

`GitHub → source of truth`

## Passo 6 — Crie o Learning Cockpit com ChatGPT Sites

Use ChatGPT Sites quando disponível na sua conta.

Abra a experiência Sites/Work do ChatGPT ou acione `@Sites` em um ambiente compatível.

Peça, por exemplo:

> Crie meu Learning Cockpit usando as specs atuais do LearningOps e o contrato do Workspace. O Cockpit deve apenas apresentar estado governado e nunca inventar evidências ou métricas.

Revise o preview, revise privacidade/compartilhamento e publique quando estiver pronto.

O deployment gera uma URL de produção.

### Registre a URL

Volte ao `LearningOps OS` e envie:

> Este é o URL oficial do meu Learning Cockpit: `<URL>`. Registre-o no Workspace como meu Cockpit ativo.

O sistema deve persistir e verificar essa configuração no Workspace.

**Não adicione a URL do Cockpit como fonte global do Projeto.** A URL é configuração; o Workspace continua sendo source of truth.

### O Cockpit atualiza sozinho?

Não assuma.

O adapter deve declarar um modo:

- **live-data** — lê estado governado atual por integração validada;
- **snapshot** — apresenta um snapshot que precisa ser reconstruído/atualizado quando o Workspace muda.

Uma URL publicada não prova auto-sync com GitHub.

## Passo 7 — Configure automações

LearningOps recomenda dois jobs iniciais.

### `LearningOps Workspace Maintenance`

Cadência padrão: **diária**.

Use para reconciliar estado derivado de evidências já persistidas, revisar PDI, retention, knowledge debt, learner graph e snapshot do Cockpit quando aplicável.

Prompt sugerido:

> Leia o estado atual do meu LearningOps Workspace. Reconcilie apenas estados derivados de evidências já persistidas segundo as specs atuais. Verifique PDI, mastery, retention, knowledge debt, learner graph e Cockpit snapshot quando aplicável. Nunca crie evidência ou mastery por inferência. Se não tiver permissão real para uma alteração, informe e não alegue que atualizou.

### `LearningOps Health Review`

Cadência padrão: **semanal**.

Use para verificar schemas, lineage, Planner, compatibilidade Core/Workspace, PDI, retention, referências quebradas e Cockpit.

Prompt sugerido:

> Faça um health review do LearningOps Workspace. Verifique integridade de schemas, lineage, Planners, compatibilidade com o Core, PDI, retention, mastery e Cockpit. Não invente evidências. Aplique apenas mudanças permitidas pelas specs e reporte qualquer item que exija decisão humana.

### Regra da automação

`READ → VALIDATE → DERIVE → RECONCILE → WRITE → VERIFY`

Se a escrita não estiver disponível:

`READ → VALIDATE → DERIVE → PROPOSE → REPORT`

**Automação pode organizar e derivar estado a partir de evidência. Automação nunca pode fabricar evidência.**

A capacidade de Tasks/apps pode mudar. Valide a capacidade real antes de depender de acesso a arquivos do Projeto ou escrita não assistida em GitHub.

## Passo 8 — Crie `My Learning`

Crie um chat chamado:

`My Learning`

Use-o como seu painel conversacional transversal.

Não crie chats separados para PDI, mastery, gaps, professional profile ou résumé.

## Passo 9 — Crie seu primeiro chat de estudo

Crie um chat com o nome do campo, por exemplo:

`Modern Data Architecture`

Comece naturalmente. Não é necessário um comando de bootstrap.

## Passo 10 — Planner Discovery

LearningOps propõe uma formação inicial e você ajusta em linguagem natural:

- `Tire Kubernetes.`
- `Inclua Snowflake.`
- `Quero mais profundidade em Iceberg.`
- `Não quero Machine Learning agora.`

Exploração não precisa ser persistida.

## Passo 11 — Feche o Planner

Quando o plano estiver maduro, o próprio sistema deve oferecer:

> Seu plano está consistente. Gostaria de fechar seu Planner e começar a estudar?

Você também pode dizer:

> Feche meu Planner.

O sistema gera um candidato com objetivo, escopo, out of scope, competências, pré-requisitos, currículo, profundidade, evidence expectations, checkpoints e relações iniciais relevantes.

## Passo 12 — Aprove e persista

Depois de revisar:

> Aprovo o Planner.

O sistema deve oferecer a persistência no Workspace.

`Planner aprovado → Workspace → GitHub`

Fechar não significa aprovar. Aprovar não significa que a escrita ocorreu. A persistência só é considerada concluída depois de verificada.

### Planner não é prompt

`Planner → source of truth`

`Prompt → runtime adapter`

Nunca adicione um Planner específico como fonte global do Projeto.

## Durante o estudo

O usuário não deve precisar lembrar quando atualizar o Workspace.

LearningOps usa **Proactive Consentful Persistence**:

`DETECT → EXPLAIN → OFFER → USER DECIDES → EXECUTE → VERIFY`

Exemplos:

> Tenho 3 evidências relevantes deste bloco prontas para registro. Gostaria de atualizar seu Workspace?

> Gostaria de fechar este checkpoint e persistir o progresso observado?

Se o usuário disser não, não há escrita.

Uma autorização compreensível pode cobrir consequências derivadas permitidas pelas specs, como evidência, checkpoint, mastery derivado, PDI, knowledge debt, learner graph e snapshot do Cockpit. Não pergunte separadamente por cada detalhe interno.

## Chat de estudo versus sessão interna

Um chat de estudo é o contexto contínuo de um campo.

`session` / `checkpoint` são unidades internas de lineage persistidas no Workspace. O usuário não precisa criar chats `01-foundations`, `02-storage` etc.

## PDI global

PDI pode ter itens ligados a domínios, mas a priorização canônica é transversal e é acessada pelo `My Learning`.

Método:

`GOAL → TARGET COMPETENCIES → CURRENT EVIDENCE → GAP → PRIORITY → INTERVENTION → EVIDENCE → REVIEW → ADAPT`

Curriculum responde: `quais capacidades formam este domínio e em que sequência?`

Planner responde: `o que foi acordado estudar neste domínio?`

PDI responde: `considerando todos os objetivos e evidências, o que possui maior valor agora?`

## Professional Profile e Résumé

`My Learning` agrega verdade profissional sustentada por evidência entre os domínios.

Pipeline:

`Learning Evidence → Professional Profile → Job Matching → Résumé Generation → Validation → PDF/DOCX`

Experiência de estudo não deve ser convertida em experiência de produção sem evidência atribuível.

## Não use o Study Mode genérico por padrão

LearningOps já possui seu próprio runtime pedagógico.

Não ative genericamente `@study`, `/study` ou Study Mode dentro de um chat de estudo LearningOps por padrão. Dois tutores podem disputar perguntas, hints, sequência, Planner, currículo e assistência.

A disponibilidade real pode variar entre documentação, conta e rollout. LearningOps deve avaliar o comportamento observado, não depender de suposição de disponibilidade.

### Compatibility Eval futuro

Antes de permitir Study Mode como adapter opcional, testar:

- respeito às Project Instructions;
- respeito ao Planner;
- attempt-before-answer;
- hint escalation;
- assistance lineage;
- compatibilidade com currículo/PDI;
- isolamento de papéis;
- capacidade de coexistir sem dupla orquestração.

## GitHub é a memória durável

### Core

`euvictorhfs/LearningOps`

Sistema, métodos, specs, schemas, runtime, evals, governance e adapters.

### Workspace

`euvictorhfs/LearningOps-workspace`

Estado privado e observado do learner.

## Arquitetura detalhada

Principais specs:

- [Generative AI Architecture](specs/genai-architecture-spec.md)
- [Evaluation](specs/evaluation-spec.md)
- [Learning Method](specs/learning-method-spec.md)
- [Learning](specs/learning-spec.md)
- [Competency Model](specs/competency-model-spec.md)
- [Curriculum](specs/curriculum-spec.md)
- [Learning Planner](specs/planner-spec.md)
- [PDI](specs/pdi-spec.md)
- [Evidence & Lineage](specs/evidence-spec.md)
- [Mastery](specs/mastery-spec.md)
- [Knowledge Graph](specs/knowledge-graph-spec.md)
- [Session Runtime](specs/session-runtime-spec.md)
- [Workspace Runtime](specs/workspace-runtime-spec.md)
- [Automation](specs/automation-spec.md)
- [ChatGPT Sites Adapter](specs/chatgpt-sites-adapter-spec.md)
- [Learning Cockpit](specs/cockpit-spec.md)
- [Professional Profile](specs/professional-profile-spec.md)
- [Evidence-Based Resume](specs/evidence-based-resume-spec.md)
- [Governance](specs/governance-spec.md)

## Regra simples

Para manter o sistema: `LearningOps OS`.

Para sua visão global: `My Learning`.

Para estudar: crie um chat com o nome do campo.

Quando o plano estiver bom: `Feche meu Planner.`

Quando algo relevante puder ser persistido: **LearningOps oferece; você decide.**

## Princípio central

**Não medir quanto conteúdo foi apresentado. Medir o que a pessoa consegue fazer com o conhecimento — com evidência, contexto e lineage.**
