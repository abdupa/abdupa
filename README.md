<div align="center">

# Abe Dupa

### AI Systems Engineer · Full-Stack Engineer · Workflow Automation & Agentic Systems

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org/) [![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/) [![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white)](https://nodejs.org/) [![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat&logo=nestjs&logoColor=white)](https://nestjs.com/) [![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)](https://www.typescriptlang.org/) [![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=next.js&logoColor=white)](https://nextjs.org/) [![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)](https://react.dev/) [![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat&logo=php&logoColor=white)](https://www.php.net/) [![WordPress](https://img.shields.io/badge/WordPress-21759B?style=flat&logo=wordpress&logoColor=white)](https://wordpress.org/) [![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)](https://www.langchain.com/) [![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat&logo=openai&logoColor=white)](https://openai.com/) [![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat&logo=postgresql&logoColor=white)](https://www.postgresql.org/) [![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)](https://redis.io/) [![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)](https://www.docker.com/)

I build production-ready AI systems, multi-tenant SaaS platforms, and automation pipelines —
where reliability, auditability, and real business outcomes matter.

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

## Experience

### Automatriq.com
`February 2025 – Present` · **Enterprise, Multi-tenant B2B SaaS — wholesale & distribution operations automation**  
🌐 [automatriq.com](https://www.automatriq.com) · *Repository: private, access on request*
**Technical documentation** — [Full Architecture Manual →](https://www.automatriq.com/docs/technical-manual-v2.html)

A production-deployed, 0→1 enterprise operations platform automating the full order-to-cash and supplier lifecycle for B2B wholesale and distribution businesses.

**Core Systems Built:**

- **Durable workflow engine** — 14 Temporal workflows covering the full ops lifecycle: inquiry triage (W1), order intake (W9), support cases and billing disputes (W12–W13), supplier intake (W16), eternal Gmail polling loop (W17), plus 6 scheduled monitors for quote aging, reorder, dormant accounts, daily briefs, fulfillment alerts, and payment follow-ups

- **Gmail inbound email automation** — eternal Temporal polling workflow (W17) continuously monitors a Gmail inbox via OAuth2 refresh (no webhooks, no missed messages); inbound emails are normalized and routed through the full triage pipeline — LangGraph classifies intent, GPT-4o generates a catalog-grounded draft reply, and the draft is queued in the `/ops` approval panel for rep review; approved replies are sent via Gmail API with full thread continuity

- **WhatsApp Business integration** — bidirectional messaging via WhatsApp Business Cloud API; inbound messages verified by X-Hub-Signature-256 HMAC and normalized into the same canonical inquiry pipeline as email — same intent classification, same draft generation, same approval gate; outbound delivery sends approved replies back to the customer's WhatsApp thread

- **Embedded web chat AI agent** — real-time AI sales assistant deployable on any client site via a single script tag; SSE streaming with typing indicators, catalog-grounded replies via pgvector RAG, live rep handoff, and full session continuity; intent classified by LangGraph before each response

- **AI layer** — LangGraph intent classification and context-aware draft generation behind human-in-the-loop approval gates; GPT-4o structured order document parser extracting line items from unstructured emails; credit and inventory preflight checks before order approval

- **Multi-tenant ops portal** — 12 `/ops` routes across 5 roles: rep order queue, manager dashboard, executive view, approval queue, exception panel, product catalog, live chat console, and tenant settings

- **Security & multi-tenancy** — Auth0 v4 JWKS verification, `tenant_id` enforced from JWT at every query boundary (never request body), append-only audit trail on every critical action

- **Test coverage** — 303 integration tests, 25 files, zero mocks, all against real PostgreSQL — full workflow, activity, channel adapter, AI feature, and RBAC coverage

`Python` `FastAPI` `Temporal` `LangGraph` `OpenAI GPT-4o` `PostgreSQL` `pgvector` `Next.js 16` `TypeScript` `Tailwind CSS v4` `Auth0` `Docker` `GCP` `Vercel` `Render` `Neon` `Redis` `Upstash` `pytest`

---

### GadgetPH
`January 2021 – January 2025` · **Production web platform — AI content automation, WordPress tooling, distributed data pipelines, SEO**  
🌐 [gadgetph.com](https://gadgetph.com/) · *Repository: private*

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

## Projects

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
