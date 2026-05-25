<div align="center">

# Abe Dupa

### AI Systems Engineer · Full-Stack Engineer · Workflow Automation & Agentic Systems

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=next.js&logoColor=white)](https://nextjs.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)](https://www.docker.com/)
[![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat&logo=openai&logoColor=white)](https://openai.com/)

I build production-ready AI systems, multi-tenant SaaS platforms, and automation pipelines —
where reliability, auditability, and real business outcomes matter.

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=abdupa&show_icons=true&theme=default&hide_border=true&count_private=true&include_all_commits=true)](https://github.com/abdupa)
&nbsp;
[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=abdupa&layout=compact&hide_border=true&langs_count=6)](https://github.com/abdupa)

</div>

---

## Engineering Highlights

- **303 integration tests** — zero mocks, all against a real PostgreSQL database, full workflow and RBAC coverage
- **14 Temporal workflows** in production — inquiry triage, order intake, support cases, scheduling monitors, eternal polling loop, and daily briefs
- **Multi-tenant SaaS** with JWT-enforced data isolation, append-only audit trails, and per-tenant RBAC at every query boundary
- **90% manual workload reduction** delivered through AI-assisted automation pipelines on a live production platform
- **70% platform speed improvement** through performance engineering: caching, async delivery, Core Web Vitals optimization
- **Validation-first AI design** — Pydantic boundaries between LLM outputs and deterministic business logic across every system

---

## Live Work

| Project | URL | What it is |
|---------|-----|-----------|
| AI Operations Platform | [automatriq.com](https://www.automatriq.com) | Multi-tenant B2B SaaS — email, WhatsApp, web chat, 14 Temporal workflows, ops dashboards |
| GadgetPH | [gadgetph.com](https://gadgetph.com/) | Production web platform — AI content pipelines, WooCommerce tooling, distributed scraping, SEO automation |
| AGA Frontend | [aga-frontend-five.vercel.app](https://aga-frontend-five.vercel.app/) | AI-assisted growth workflow frontend |

---

## Projects

### AI Operations Platform
**Multi-tenant B2B SaaS for wholesale and distribution operations**
Live: [automatriq.com](https://www.automatriq.com) · *Repository: private, access on request*

A production-deployed, 0→1 enterprise operations platform automating the full order-to-cash and supplier lifecycle for B2B wholesale and distribution businesses.

**What I built:**

- **14 Temporal workflows** — W1 inquiry triage routing inbound messages to W9 order intake, W12–W13 support cases and billing disputes, W16 supplier intake, W17 eternal Gmail polling loop, plus scheduled workflows for quote aging, reorder monitoring, dormant accounts, daily operational briefs, fulfillment alerts, and payment follow-ups
- **Multi-channel adapters** — Gmail OAuth2 with continuous polling, WhatsApp Business API (bidirectional), embedded web chat widget with SSE streaming and live rep handoff, Wix Chat webhook normalizer
- **AI layer** — LangGraph intent classification and draft generation behind human-in-the-loop approval gates; GPT-4o order document parser extracting structured line items from unstructured emails; corpus-backed pgvector semantic retrieval for catalog-aware replies; credit and inventory preflight check before order approval
- **Role-based portal** — 12 `/ops` routes across five roles: rep order queue, manager dashboard, executive view, approval queue, exception panel, product catalog, live chat interface, and tenant settings
- **Security and isolation** — Auth0 v4 JWKS verification, `tenant_id` derived from JWT only (never request body), append-only audit trail on every critical action
- **Test coverage** — 303 integration tests, 25 test files, zero mocks, real PostgreSQL — full workflow, activity, channel adapter, AI feature, and RBAC coverage
- **Technical documentation** — [Full Architecture Manual →](https://www.automatriq.com/docs/technical-manual-v2.html) *(deployed on Vercel)*

`Python` `FastAPI` `Temporal` `LangGraph` `OpenAI GPT-4o` `PostgreSQL` `pgvector` `Next.js 16` `TypeScript` `Tailwind CSS v4` `Auth0` `Docker` `GCP` `Vercel` `Render` `Neon` `Redis` `Upstash` `pytest`

---

### GadgetPH
**Production web platform — AI content automation, WordPress tooling, distributed data pipelines, SEO**
Live: [gadgetph.com](https://gadgetph.com/) · *Repository: private*

A live consumer electronics platform in the Philippines. I designed and implemented the full AI content automation system, distributed scraping infrastructure, custom WordPress plugins, and SEO stack that powers product publishing at scale.

**Key contributions:**

- **AI content pipelines** — multi-stage LLM workflows (LangGraph) transforming raw scraped marketplace data into structured, SEO-ready product content; reduced manual workload by **90%**
- **WordPress plugins (production)** — built two plugins live on gadgetph.com:
  - *Product Offers Plugin v2.3.1* — multi-source price comparison tables, historical price charts (Chart.js), price drop email alerts, WooCommerce integration
  - *Smartphone Price List Plugin v5.0.0* — dynamic filterable price lists, batch processing, Google Sheets integration, admin cache management UI
- **Distributed scraping** — Scrapy + Playwright + Celery + Redis pipelines processing thousands of product records concurrently with circuit breakers and retry orchestration
- **SEO engineering** — GA4, GTM, Google Search Console API, schema markup, XML sitemaps, Core Web Vitals optimization; page speed scores improved by **70%**
- **Validation layer** — Pydantic-based sanitization and normalization of AI-generated outputs before publishing; reduced failure risk from non-deterministic model responses

`PHP` `WordPress` `WooCommerce` `Python` `LangGraph` `OpenAI GPT-4o` `Pydantic` `Scrapy` `Playwright` `Celery` `Redis` `PostgreSQL` `Google Sheets API` `Google Search Console API` `Chart.js` `GA4` `GTM`

---

### Dealer Flow AI
**Multi-tenant SaaS for automotive lead conversion**
*Repository: private, access on request*

Helps dealership teams move inbound leads toward booked test drives — lead intake, AI-assisted qualification, deterministic inventory matching, appointment scheduling, and staff dashboards.

- Multi-tenant modular monolith with authenticated user workflows and RBAC
- Scheduling rules, availability windows, and blackout logic
- AI assistance strictly separated from deterministic business truth

`Next.js` `TypeScript` `NestJS` `PostgreSQL` `Prisma` `Redis` `BullMQ` `Docker Compose`

---

### Nexus AI Growth Engine
**Multi-tenant lead qualification and agent workflow system**
*Repository: private, access on request*

Agentic workflow platform coordinating AI-assisted discovery, triage, and drafting across multiple concurrent clients.

- LangGraph state machine coordinating specialized AI agents
- Backend-enforced tenant isolation and UUID-scoped data access
- Execution audit traces for transparent, explainable AI decisions

`Python` `FastAPI` `LangGraph` `Gemini` `OpenAI` `Supabase` `PostgreSQL` `Docker`

---

### Nexus Ingest
**Browser automation and distributed ingestion engine**
[Public repo →](https://github.com/abdupa/nexus-ingest)

Resilient ingestion system for high-friction data collection environments.

- Playwright-based browser automation and session management
- Redis-backed circuit breakers and retry orchestration
- Tiered routing logic to reduce proxy cost

`Python` `Celery` `Redis` `PostgreSQL` `Playwright` `BeautifulSoup` `Docker`

---

## Toolbox

| Area | Technologies |
|------|-------------|
| **Frontend** | React, Next.js 16, TypeScript, Tailwind CSS v4, responsive dashboards |
| **Backend** | Python, FastAPI, Node.js, NestJS, REST APIs |
| **Workflow Orchestration** | Temporal (Cloud + self-hosted GCP), durable workflows, signal/query patterns, eternal loops |
| **AI & Automation** | LangGraph, LangChain, OpenAI GPT-4o, Gemini, Claude, RAG, pgvector, Pydantic validation layers |
| **Data & Auth** | PostgreSQL, Neon, Supabase, Prisma, pgvector, Auth0 v4, RBAC, JWT-enforced tenant isolation |
| **Infrastructure** | Docker, GCP (Compute Engine), Redis, Upstash, Celery, BullMQ, Vercel, Render, Linux/systemd |
| **Testing** | pytest, integration tests against real databases, Playwright E2E, zero-mock philosophy |
| **Web & E-Commerce** | WordPress, WooCommerce, GA4, GTM, Search Console API, schema markup, Core Web Vitals |

---

## Open To

Freelance engagements, contract roles, and collaborations on:
- AI workflow systems, agentic platforms, and LLM-backed automation
- Multi-tenant SaaS — architecture, backend, full-stack
- Internal tools, operator portals, and business process automation

---

## Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abemael-dupa-b2a768249/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:dupa.abe@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/abdupa)
