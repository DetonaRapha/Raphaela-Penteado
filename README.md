# Raphaela-Penteado

Construo e opero sistemas multi-agente autônomos em produção. Sou criadora do NOA (Núcleo Operacional Autônomo), um motor multi-agente escrito do zero em TypeScript, sem framework de agentes pronto por baixo, que hoje opera um produto real de IA em saúde rodando no GCP.

Antes de IA agêntica, passei 8 anos em engenharia de qualidade e backend. Essa origem define como eu construo agentes: com pirâmide de testes, observabilidade, contratos explícitos entre agentes e trilha de auditoria desde o primeiro commit. Autonomia sem rastreabilidade é protótipo, não produto.

O que estou construindo

NOA é um kernel que coordena cinco agentes especializados (ingestão, classificação, planejamento, execução e memória). O conhecimento de domínio não vive nos agentes: é injetado em runtime por arquivos de skill, o que torna o motor white-label. Cada handoff entre agentes tem contrato definido, então o comportamento autônomo continua explicável e defensável.

<img width="791" height="702" alt="image" src="https://github.com/user-attachments/assets/97433f28-6db9-4c88-bac6-872afc6042bc" />


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
