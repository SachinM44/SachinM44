<div align="center">

<img src="./assets/dashboard.svg" alt="live dashboard" width="100%"/>

</div>

<br/>

<table>
<tr>
<td width="55%" valign="top">

```
> sachin --whoami

  AI Engineer, building agent systems
  that survive contact with production.

  currently   AarogyaID — claims adjudication at scale
  before      RevenueHero, OneFinity Labs
  based       Bengaluru, IN
```

**What I actually do:** multi-agent orchestration, RAG that doesn't
hallucinate, and the unglamorous infrastructure underneath —
rate limiters, circuit breakers, event buses, deterministic
validation layers that catch what the model got wrong.

</td>
<td width="45%" valign="top">

```
> sachin --stack

  ai        Vertex AI · Gemini · LangGraph
            Google ADK · LangChain
  core      Python · TypeScript · C++ · Go
  backend   FastAPI · Node · Hono · Pydantic
  data      Mongo · Postgres · Redis · Prisma
  infra     GCP · AWS · Docker · K8s
```

</td>
</tr>
</table>

<br/>

## Selected work

<table>
<tr>
<td width="50%" valign="top">

### [AuditChain](https://github.com/SachinM44/AuditChain)
`AI` · `blockchain` · `supply-chain security`

Decentralized security auditing for npm packages.
LLM static analysis paired with on-chain audit
attestations, so trust doesn't route through a
single registry.

</td>
<td width="50%" valign="top">

### [Exponus](https://github.com/SachinM44/Exponus)
`Hono` · `Cloudflare Workers` · `Prisma`

Globally distributed serverless publishing
platform. End-to-end type safety through shared
Zod schemas — auth, uploads, and content all
validated from one source of truth.

</td>
</tr>
</table>

<br/>

<details>
<summary><b>Production work at AarogyaID</b></summary>

<br/>

A 16-module agent pipeline for health-insurance claims adjudication.

- **Latency** — cut adjudication turnaround 40–53% by parallelizing module execution, pooling per-backend Gemini rate limiters, adding a quota-exhaustion circuit breaker, and swapping a request-scoped RAG cache for a process-global LRU.
- **Grounding** — Vertex AI Search RAG over hospital tariff and policy documents, with batched retrieval, query cleaning, and procedure-code fallback queries. Hallucinated line items went to zero.
- **Orchestration** — a task-planner LLM routes to specialized agents (tariff, fraud, classification, non-medical expense), running per-document swarms concurrently with Pydantic-validated output.
- **Correctness** — deterministic validation reconciles LLM output against digitized source bills line-by-line. Ungrounded amounts get flagged for human review instead of silently denied.
- **Infrastructure** — MongoDB-backed Socket.IO event bus for multi-worker delivery, server-side module re-run and publish endpoints, deployed on GCE / Cloud Build / GCS with Firebase auth.

</details>

<details>
<summary><b>How this profile is built</b></summary>

<br/>

The dashboard above isn't a third-party badge service. It's an SVG generated
by [`scripts/generate-dashboard.js`](./scripts/generate-dashboard.js), which
queries the GitHub GraphQL API and renders the chart by hand. A scheduled
Action commits it back to this repo every night.

Which means: no rate limits, no dead Heroku hosts, no broken image icons,
and a design that exists exactly once on this website.

</details>

<br/>

## Contribution grid

<div align="center">
  <img src="https://raw.githubusercontent.com/SachinM44/SachinM44/output/snake.svg" alt="contribution snake" width="100%"/>
</div>

<br/>

<div align="center">

[![LinkedIn](https://img.shields.io/badge/linkedin-0a0e14?style=flat-square&logo=linkedin&logoColor=ffb454&labelColor=0a0e14)](https://www.linkedin.com/in/sachin-m99/)
[![Email](https://img.shields.io/badge/email-0a0e14?style=flat-square&logo=gmail&logoColor=ffb454&labelColor=0a0e14)](mailto:sachin69778@gmail.com)

</div>
