# Raphaela-Penteado

Construo e opero sistemas multi-agente autônomos em produção. Sou criadora do NOA (Núcleo Operacional Autônomo), um motor multi-agente escrito do zero em TypeScript, sem framework de agentes pronto por baixo, que hoje opera um produto real de IA em saúde rodando no GCP.

Antes de IA agêntica, passei 8 anos em engenharia de qualidade e backend. Essa origem define como eu construo agentes: com pirâmide de testes, observabilidade, contratos explícitos entre agentes e trilha de auditoria desde o primeiro commit. Autonomia sem rastreabilidade é protótipo, não produto.

O que estou construindo

NOA é um kernel que coordena cinco agentes especializados (ingestão, classificação, planejamento, execução e memória). O conhecimento de domínio não vive nos agentes: é injetado em runtime por arquivos de skill, o que torna o motor white-label. Cada handoff entre agentes tem contrato definido, então o comportamento autônomo continua explicável e defensável.

#mermaid-r19e-r1 { font-family: "Anthropic Sans", system-ui, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; font-size: 16px; fill: rgb(229, 229, 229); }
#mermaid-r19e-r1 .edge-animation-slow { stroke-dashoffset: 900; animation: 50s linear 0s infinite normal none running dash; stroke-linecap: round; stroke-dasharray: 9, 5 !important; }
#mermaid-r19e-r1 .edge-animation-fast { stroke-dashoffset: 900; animation: 20s linear 0s infinite normal none running dash; stroke-linecap: round; stroke-dasharray: 9, 5 !important; }
#mermaid-r19e-r1 .error-icon { fill: rgb(204, 120, 92); }
#mermaid-r19e-r1 .error-text { fill: rgb(51, 135, 163); stroke: rgb(51, 135, 163); }
#mermaid-r19e-r1 .edge-thickness-normal { stroke-width: 1px; }
#mermaid-r19e-r1 .edge-thickness-thick { stroke-width: 3.5px; }
#mermaid-r19e-r1 .edge-pattern-solid { stroke-dasharray: 0; }
#mermaid-r19e-r1 .edge-thickness-invisible { stroke-width: 0; fill: none; }
#mermaid-r19e-r1 .edge-pattern-dashed { stroke-dasharray: 3; }
#mermaid-r19e-r1 .edge-pattern-dotted { stroke-dasharray: 2; }
#mermaid-r19e-r1 .marker { fill: rgb(161, 161, 161); stroke: rgb(161, 161, 161); }
#mermaid-r19e-r1 .marker.cross { stroke: rgb(161, 161, 161); }
#mermaid-r19e-r1 svg { font-family: "Anthropic Sans", system-ui, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; font-size: 16px; }
#mermaid-r19e-r1 p { margin: 0px; }
#mermaid-r19e-r1 .label { font-family: "Anthropic Sans", system-ui, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; color: rgb(229, 229, 229); }
#mermaid-r19e-r1 .cluster-label text { fill: rgb(51, 135, 163); }
#mermaid-r19e-r1 .cluster-label span { color: rgb(51, 135, 163); }
#mermaid-r19e-r1 .cluster-label span p { background-color: transparent; }
#mermaid-r19e-r1 .label text, #mermaid-r19e-r1 span { fill: rgb(229, 229, 229); color: rgb(229, 229, 229); }
#mermaid-r19e-r1 .node rect, #mermaid-r19e-r1 .node circle, #mermaid-r19e-r1 .node ellipse, #mermaid-r19e-r1 .node polygon, #mermaid-r19e-r1 .node path { fill: transparent; stroke: rgb(161, 161, 161); stroke-width: 1px; }
#mermaid-r19e-r1 .rough-node .label text, #mermaid-r19e-r1 .node .label text, #mermaid-r19e-r1 .image-shape .label, #mermaid-r19e-r1 .icon-shape .label { text-anchor: middle; }
#mermaid-r19e-r1 .node .katex path { fill: rgb(0, 0, 0); stroke: rgb(0, 0, 0); stroke-width: 1px; }
#mermaid-r19e-r1 .rough-node .label, #mermaid-r19e-r1 .node .label, #mermaid-r19e-r1 .image-shape .label, #mermaid-r19e-r1 .icon-shape .label { text-align: center; }
#mermaid-r19e-r1 .node.clickable { cursor: pointer; }
#mermaid-r19e-r1 .root .anchor path { stroke-width: 0; stroke: rgb(161, 161, 161); fill: rgb(161, 161, 161) !important; }
#mermaid-r19e-r1 .arrowheadPath { fill: rgb(11, 11, 11); }
#mermaid-r19e-r1 .edgePath .path { stroke: rgb(161, 161, 161); stroke-width: 1px; }
#mermaid-r19e-r1 .flowchart-link { stroke: rgb(161, 161, 161); fill: none; }
#mermaid-r19e-r1 .edgeLabel { background-color: transparent; text-align: center; }
#mermaid-r19e-r1 .edgeLabel p { background-color: transparent; }
#mermaid-r19e-r1 .edgeLabel rect { opacity: 0.5; background-color: transparent; fill: transparent; }
#mermaid-r19e-r1 .labelBkg { background-color: rgba(0, 0, 0, 0.5); }
#mermaid-r19e-r1 .cluster rect { fill: rgb(204, 120, 92); stroke: rgb(138, 115, 107); stroke-width: 1px; }
#mermaid-r19e-r1 .cluster text { fill: rgb(51, 135, 163); }
#mermaid-r19e-r1 .cluster span { color: rgb(51, 135, 163); }
#mermaid-r19e-r1 div.mermaidTooltip { position: absolute; text-align: center; max-width: 200px; padding: 2px; font-family: "Anthropic Sans", system-ui, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; font-size: 12px; background: rgb(204, 120, 92); border: 1px solid rgb(138, 115, 107); border-radius: 2px; pointer-events: none; z-index: 100; }
#mermaid-r19e-r1 .flowchartTitleText { text-anchor: middle; font-size: 18px; fill: rgb(229, 229, 229); }
#mermaid-r19e-r1 rect.text { fill: none; stroke-width: 0; }
#mermaid-r19e-r1 .icon-shape, #mermaid-r19e-r1 .image-shape { background-color: transparent; text-align: center; }
#mermaid-r19e-r1 .icon-shape p, #mermaid-r19e-r1 .image-shape p { background-color: transparent; padding: 2px; }
#mermaid-r19e-r1 .icon-shape .label rect, #mermaid-r19e-r1 .image-shape .label rect { opacity: 0.5; background-color: transparent; fill: transparent; }
#mermaid-r19e-r1 .label-icon { display: inline-block; height: 1em; overflow: visible; vertical-align: -0.125em; }
#mermaid-r19e-r1 .node .label-icon path { fill: currentcolor; stroke: revert; stroke-width: revert; }
#mermaid-r19e-r1 .node .neo-node { stroke: rgb(161, 161, 161); }
#mermaid-r19e-r1 [data-look="neo"].node rect, #mermaid-r19e-r1 [data-look="neo"].cluster rect, #mermaid-r19e-r1 [data-look="neo"].node polygon { stroke: url("#mermaid-r19e-r1-gradient"); filter: drop-shadow(rgb(185, 185, 185) 1px 2px 2px); }
#mermaid-r19e-r1 [data-look="neo"].node path { stroke: url("#mermaid-r19e-r1-gradient"); stroke-width: 1px; }
#mermaid-r19e-r1 [data-look="neo"].node .outer-path { filter: drop-shadow(rgb(185, 185, 185) 1px 2px 2px); }
#mermaid-r19e-r1 [data-look="neo"].node .neo-line path { stroke: rgb(161, 161, 161); filter: none; }
#mermaid-r19e-r1 [data-look="neo"].node circle { stroke: url("#mermaid-r19e-r1-gradient"); filter: drop-shadow(rgb(185, 185, 185) 1px 2px 2px); }
#mermaid-r19e-r1 [data-look="neo"].node circle .state-start { fill: rgb(0, 0, 0); }
#mermaid-r19e-r1 [data-look="neo"].icon-shape .icon { fill: url("#mermaid-r19e-r1-gradient"); filter: drop-shadow(rgb(185, 185, 185) 1px 2px 2px); }
#mermaid-r19e-r1 [data-look="neo"].icon-shape .icon-neo path { stroke: url("#mermaid-r19e-r1-gradient"); filter: drop-shadow(rgb(185, 185, 185) 1px 2px 2px); }
#mermaid-r19e-r1 :root { --mermaid-font-family: "Anthropic Sans",system-ui,"Segoe UI",Roboto,Helvetica,Arial,sans-serif; }KernelIngestãoClassificaçãoPlanejamentoExecuçãoMemóriaArquivos de skilldomínio em runtime

Em produção, o NOA conduz os fluxos multi-etapa da Aylla MedIA, produto de IA na área de saúde: uso de ferramentas, memória persistente em Postgres + pgvector e inferência self-hosted (Gemma em NVIDIA L4 via vLLM).

Do lado da confiabilidade, a mesma operação inclui a camada completa de qualidade no GCP: testes em três níveis, 9 políticas de alerta entre ambientes e resposta a incidentes P1 (falhas de autenticação SSO, OOM kills, indisponibilidade regional do Vertex AI, latência de cold start).

Projetos públicos


agent-eval-kit: camada de testes para agentes de LLM. Golden datasets, LLM-as-judge e scorecard com veredito pass/fail plugável no CI. Roda offline com juiz mock determinístico, sem API key. É a minha resposta para o problema de testar saída não determinística: não dá para usar assert, dá para usar avaliação com limiar.


O desenho de arquitetura do NOA (builders, contratos de handoff e modelo de maturidade) está a caminho de virar repositório público de documentação.

Stack

IA: orquestração multi-agente, RAG, pgvector, MCP, function calling, avaliação de agentes e guardrails, vLLM, Ollama, Vertex AI (Gemini), Gemma
Backend: TypeScript strict, Node 20, Fastify, NestJS, Drizzle ORM, PostgreSQL, arquitetura orientada a eventos
Cloud e confiabilidade: GCP (Cloud Run, Cloud SQL, Cloud Monitoring, Secret Manager), GitHub Actions, observabilidade, FinOps
Qualidade: governança TMMi, automação de testes, testes baseados em risco, Cypress, Selenium

Contato

LinkedIn https://www.linkedin.com/in/raphaela-penteado-453789a9/?skipRedirect=true · raphaela.penteado97@gmail.com · São Paulo, Brasil (remoto)
