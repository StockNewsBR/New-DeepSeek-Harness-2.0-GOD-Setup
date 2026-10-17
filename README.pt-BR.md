<p align="center">🌐 <strong>Documentação:</strong><br><a href="README.md">🇺🇸 English</a> · <strong>🇧🇷 Português (Brasil)</strong> · <a href="README.es.md">🇪🇸 Español</a></p>

<div align="center">

# ⚡ DEEPSEEK HARNESS 2.0
## 👑 GOD SETUP — CENTRAL DE COMANDO DE ENGENHARIA DE SOFTWARE COM IA

**UM DESKTOP · MEMÓRIA PERSISTENTE · INTELIGÊNCIA DE CÓDIGO · ROTEAMENTO DE MODELOS · AUTONOMIA CONTROLADA**

**PENSAR → LEMBRAR → COMPREENDER → CONSTRUIR → REVISAR → VALIDAR → ENTREGAR**

Uma alternativa personalizável às ferramentas isoladas de programação com IA.

</div>

---

## 🔥 A proposta

Assistentes de programação podem perder contexto entre conversas, inspecionar novamente o mesmo código e separar planejamento, execução, revisão e entrega em ferramentas diferentes. O **DeepSeek Harness 2.0 — GOD SETUP** propõe um centro de engenharia integrado: interface desktop, memória durável, seleção explícita do workspace, grafos de código, revisão especializada, inferência configurável e operações Git auditáveis.

A intenção é **substituir o fluxo de trabalho de várias ferramentas**, não afirmar que o sistema supera automaticamente modelos proprietários em todos os testes. Ganhos de velocidade, memória útil e custo precisam ser medidos.

## 🧬 Diagrama completo da arquitetura

\`\`\`mermaid
flowchart TB
    U["👤 Desenvolvedor"] --> D["🖥️ Harness 2.0 Desktop"]
    D --> R["🧭 Roteador de workspace e intenção"]
    R --> P["🔐 Escopo e permissões"]
    P --> F["♾️ LETTA_ALWAYS_FIRST: consulta antes da inferência"]
    F <--> L[("Letta: memória persistente")]
    L <--> N["Memória global e isolada por workspace"]
    F --> A["Diretor / Orquestrador"]
    A <--> O["OmniRoute: gateway local"]
    O <--> M["DeepSeek: identificador do modelo verificado"]
    A <--> G["Graphify: dependências e relações"]
    G <--> S[("Código-fonte local")]
    A --> T["Terminal, arquivos, Git e testes"]
    T <--> S
    A <--> W["Pesquisa web opcional"]
    T --> V["Ponytail: revisão"]
    V --> Q["Testes, build, lint e segurança"]
    Q --> C{"Tudo aprovado?"}
    C -->|"Não"| A
    C -->|"Sim"| H{"Exige autorização?"}
    H -->|"Sim"| Z["Autorização humana"]
    Z --> GH["GitHub: commit / push / PR"]
    H -->|"Não; dentro da política"| E["Relatório de evidências"]
    GH --> E
    E --> L
    E --> D
\`\`\`

## 🧩 Os dez pilares

| Componente | Função | Resultado esperado |
|---|---|---|
| Harness Desktop | Central de missões | Planejar, executar e acompanhar |
| Roteador de contexto | Identificação e isolamento | Evitar mistura entre repositórios |
| Letta | Memória persistente | Continuidade entre chats e reinícios |
| LETTA_ALWAYS_FIRST | Recuperação antes de inferência | Carregar contexto correto |
| DeepSeek | Raciocínio e programação | Planejamento, implementação, diagnóstico |
| OmniRoute | Gateway de modelos | Roteamento e integração configuráveis |
| Graphify | Grafo do código | Dependências e análise de impacto |
| Ponytail | Revisão independente | Detectar falhas e complexidade excessiva |
| Ferramentas locais | Arquivos, terminal e testes | Alterações reais verificáveis |
| GitHub + CI | Versionamento e auditoria | Commits e PRs autorizados |

## 🥊 Alternativa a Claude Code, Cursor e Codex

O objetivo é reunir num único ambiente **memória controlada pelo usuário, continuidade entre sessões, compreensão estrutural do código, escolha de modelos e custos mais transparentes**. Isso não significa automaticamente possuir janela de contexto maior ou desempenho superior aos concorrentes. Claude Code, Cursor e Codex também evoluem continuamente.

Compare em tarefas idênticas: porcentagem de sucesso, tempo mediano e p95, tokens, custo por tarefa bem-sucedida, precisão da memória, regressões e intervenção humana. Só divulgue números de vantagem após medições reproduzíveis.

## ♾️ Memória que sobrevive a conversas

Fluxo obrigatório: identificar o workspace → aplicar permissões → buscar memória Letta relevante **antes** da inferência → anexar origem e data dos registros → raciocinar → inspecionar o estado real do Git e dos arquivos → implementar → validar → salvar aprendizados comprovados. Se a busca de memória falhar, não carregar silenciosamente o contexto de outro projeto.

Namespaces recomendados: **global**, **por workspace** e **temporário por sessão**. Memória registrada não substitui a verificação do código atual.

## 🕸️ Graphify e 🪶 Ponytail

**Graphify** deve mapear símbolos, imports, dependências e mudanças de impacto. Sua instalação, sozinha, não comprova que o grafo esteja atualizado; valide o índice com o HEAD do Git e teste o uso real em uma missão.

**Ponytail** deve revisar diffs, simplificar abstrações desnecessárias e apontar riscos de segurança, compatibilidade e testes. Revisor carregado não significa revisão concluída.

## 🔀 Gateway OmniRoute e modelo DeepSeek

O gateway fornece um ponto de integração com os modelos, com recursos que dependem da implementação efetiva. O nome comercial de um modelo pode ser diferente do seu ID na API: valide o identificador, disponibilidade, preços, timeout e suporte a ferramentas.

Exemplo **ilustrativo**:

\`\`\`dotenv
AI_BASE_URL=http://127.0.0.1:20128/v1
AI_MODEL=<id-do-modelo-verificado>
LETTA_BASE_URL=http://127.0.0.1:<porta-configurada>
GITHUB_WRITE_REQUIRES_APPROVAL=true
\`\`\`

Não publicar segredos, caminhos privados, tokens ou exportações integrais de memória.

## 🔁 Ciclo completo da missão

1. Identificar a intenção e o workspace.
2. Recuperar memória Letta no escopo correto.
3. Confirmar branch, HEAD, Git status e arquivos atuais.
4. Analisar dependências e plano de impacto com Graphify.
5. Preparar alteração mínima e critérios de aceitação.
6. Executar apenas ferramentas autorizadas.
7. Revisar com Ponytail quando aplicável.
8. Rodar testes, build, lint e verificações de segurança.
9. Produzir evidências; commit/push apenas com autorização.
10. Persistir aprendizados confirmados no namespace correto.

## 📥 Links oficiais e recursos

| Ferramenta | Documentação / Download |
|---|---|
| Windows + WSL2 | [Microsoft WSL](https://learn.microsoft.com/windows/wsl/install) |
| Git | [git-scm.com](https://git-scm.com/downloads) |
| GitHub CLI | [cli.github.com](https://cli.github.com/) |
| VS Code | [code.visualstudio.com](https://code.visualstudio.com/) |
| Docker | [Docker Desktop](https://docs.docker.com/desktop/) |
| DeepSeek | [Documentação API](https://api-docs.deepseek.com/) |
| Letta | [Docs](https://docs.letta.com/) · [GitHub](https://github.com/letta-ai/letta) |
| NVIDIA NIM opcional | [build.nvidia.com](https://build.nvidia.com/) |
| Graphify | [Pesquisar repositórios](https://github.com/search?q=graphify&type=repositories) — upstream exato a confirmar |
| Ponytail | [Pesquisar repositórios](https://github.com/search?q=ponytail&type=repositories) — upstream exato a confirmar |
| OmniRoute | [Pesquisar repositórios](https://github.com/search?q=omniroute&type=repositories) — upstream exato a confirmar |
| Python | [python.org](https://www.python.org/downloads/) |
| Node.js | [nodejs.org](https://nodejs.org/) |
| pytest | [docs.pytest.org](https://docs.pytest.org/) |
| Playwright | [playwright.dev](https://playwright.dev/) |
| Semgrep | [semgrep.dev](https://semgrep.dev/) |
| Gitleaks | [GitHub](https://github.com/gitleaks/gitleaks) |
| GitHub Actions | [Documentação](https://docs.github.com/en/actions) |
| OpenTelemetry | [opentelemetry.io](https://opentelemetry.io/) |

**Atenção:** este repositório é um guia arquitetural, e não um instalador público homologado do Harness 2.0.

## 🛠️ Instalação e configuração — roteiro

1. Instalar Windows/WSL2 seguindo a documentação oficial.
2. No WSL executar: \`sudo apt update && sudo apt install -y git curl ca-certificates python3 python3-venv python3-pip\`.
3. Criar diretórios isolados e proteger configurações com permissões restritas.
4. Configurar a implementação **verificada** do OmniRoute e testar o modelo escolhido.
5. Instalar Letta e testar gravação, reinicialização e recuperação em novo chat.
6. Integrar Graphify, reconstruir índice e confirmar correspondência ao HEAD atual.
7. Integrar Ponytail e verificar revisão de um diff real.
8. Conectar GitHub com credenciais de menor privilégio e aprovações obrigatórias.
9. Executar testes completos em um repositório descartável.
10. Registrar resultados, versões, logs sem segredos e passos de rollback.

## 🚀 Melhorias prioritárias

| Prioridade | Melhoria | Prova necessária |
|---|---|---|
| P0 | Roteamento com falha segura | Testes contra mistura de workspaces |
| P0 | Garantir LETTA_ALWAYS_FIRST | Traces comprovando a ordem |
| P0 | Motor de permissões e aprovação | Ações recusadas corretamente |
| P0 | Confirmação de modelo e timeout | ID real, tempos p50/p95 |
| P1 | Índice Graphify incremental | Grafo atualizado no HEAD |
| P1 | Revisão Ponytail obrigatória | Achados reais em diffs |
| P1 | Cache de recuperação | Menos buscas e tokens |
| P1 | Pesquisa web com fontes | Custos e fontes comprovados |
| P1 | CI, scans e prevenção de segredos | Pipelines e testes negativos |
| P1 | Backup, restore e reinicialização | Recuperação demonstrada |
| P2 | Agentes especializados em paralelo | Ganho medido sem colisões |
| P2 | Observabilidade e custo por missão | Painéis e traces |
| P2 | Relatórios de PR automáticos | Evidências reproduzíveis |
| P2 | Bootstrap reproduzível | Instalação limpa de teste |
| P2 | Benchmark público | Metodologia e resultados reais |

## ✅ Critérios para homologar o GOD SETUP

Aprovar somente com provas: interface reinicia corretamente; isolamento entre workspaces; memória Letta recuperada antes do modelo; contexto persiste em novas conversas; ID de modelo real; Graphify atual e utilizado; Ponytail revisando diffs; testes/build/lint/scans; GitHub commit/push em branch autorizada; pesquisa web verificada, se ativada; recuperação após falhas; relatório com SHAs e limitações.

**Situação:** arquitetura documentada, mas o fluxo ponta a ponta ainda precisa de homologação independente. Não tratar objetivos como resultados medidos.

## 🛡️ Segurança

Nenhum push, merge, deploy, gasto, envio real ou comando destrutivo sem a autorização necessária. Isolar credenciais, bloquear injeção de prompt vinda de conteúdos externos e registrar auditoria sem expor segredos. Testes passando não autorizam produção.

---

<div align="center">

### 👑 DEEPSEEK HARNESS 2.0 — GOD SETUP

**Controle o fluxo. Preserve a memória. Entenda o código. Valide tudo. Entregue com autorização.**

Guia de arquitetura · Não é instalador pronto · Sem afiliação com os fornecedores mencionados

### 🤝 Patrocínio / Sponsored by

<a href="https://iamarketmaster.com"><img src="./assets/sponsors.svg" alt="Patrocínio AI Market Master e StockNewsBR" width="850"></a>

[AI Market Master](https://iamarketmaster.com) · [StockNewsBR](https://stocknewsbr.com)

</div>
