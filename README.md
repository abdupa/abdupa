# Hi, I'm Abe

**AI Systems Engineer | Full-Stack Engineer | AI Workflow Automation & Agentic Systems**

I build production-ready AI-powered systems, multi-tenant SaaS platforms, and automation pipelines where reliability, auditability, and real business outcomes matter.

My work usually combines:

- Python, FastAPI, LangGraph, and LangChain for AI pipelines, agent orchestration, and LLM workflows
- React, Next.js, and TypeScript for operator-facing portals and admin surfaces
- Temporal for durable workflow orchestration across multi-step business processes
- multi-tenant SaaS architecture with RBAC, audit trails, and strict data isolation
- validation-first AI design — Pydantic boundaries between LLM outputs and deterministic business logic
- integration adapters for real-world channels: email, WhatsApp, web chat, webhooks

## Live Work

| Project | Live URL | Focus |
|---|---|---|
| AI Operations Platform | https://www.automatriq.com | Multi-tenant B2B SaaS — email, WhatsApp, web chat, 15 Temporal workflows, ops dashboards |
| AGA Frontend | https://aga-frontend-five.vercel.app/ | AI-assisted growth workflow frontend |
| GadgetPH | https://gadgetph.com/ | Production web platform, e-commerce/content automation, SEO |

## Featured Projects

### AI Operations Platform

**Multi-tenant B2B SaaS for wholesale and distribution operations**  
Live: [automatriq.com](https://www.automatriq.com) · Repository: private, access on request

A production-deployed, 0→1 enterprise operations platform that automates the full order-to-cash and supplier lifecycle for B2B wholesale and distribution businesses. Every phase was shipped with integration tests against a real PostgreSQL database before the next phase started — no mocks, no shortcuts.

What I built:

- **17 Temporal workflows** — W1 inquiry triage routing inbound messages to W9 order intake, W10–W11 quote support, W12–W13 support cases and billing disputes, W16 supplier intake, W17 eternal Gmail polling loop, plus scheduled workflows for quote aging, reorder monitoring, dormant accounts, daily operational briefs, fulfillment alerts, and payment follow-ups
- **Multi-channel adapters** — Gmail OAuth2 with W17 continuous polling, WhatsApp Business API (bidirectional webhook messaging), embedded web chat widget with SSE streaming and live rep handoff, Wix site chat webhook normalizer
- **AI features** — LangGraph intent classification and AI draft generation behind human-in-the-loop approval gates; GPT-4o order document parser extracting structured line items from unstructured emails and attachments; corpus-backed pgvector semantic retrieval for catalog-aware replies; credit and inventory preflight check before order approval; BIR-compliant invoice PDF generation
- **Role-based portal** — 12 `/ops` routes spanning five roles: rep order processing queue, manager team dashboard, executive business view, reporting dashboard, live chat interface, approval queue, exception panel, product catalog, and tenant settings
- **Security and isolation** — Auth0 v4 JWKS verification, per-tenant data isolation enforced server-side at every query boundary (`tenant_id` derived from JWT only, never from request body), append-only audit trail on every critical action
- **Test coverage** — 365 integration tests, 25 test files, zero mocks, real PostgreSQL — full workflow, activity, channel adapter, AI feature, and RBAC coverage

`Python` `FastAPI` `Temporal` `LangGraph` `OpenAI GPT-4o` `PostgreSQL` `pgvector` `Next.js 16` `TypeScript` `Tailwind CSS v4` `Auth0` `Docker` `Vercel` `Render` `Neon` `pytest`

---

### AGA Frontend

**AI-assisted growth workflow frontend**  
Live app: https://aga-frontend-five.vercel.app/

Built and deployed a frontend application for an AI-assisted growth workflow product, focused on clear user flows, reusable UI structure, and modern Vercel-based delivery.

Tech stack: `React / Next.js`, `TypeScript`, `Vercel`

---

### GadgetPH

**Production web platform for product content, SEO, and automation**  
Live site: https://gadgetph.com/

GadgetPH is a live production platform where I led full-stack development, automation, performance optimization, data workflows, and internal tooling.

What I built:

- business-critical web systems for product data, content publishing, SEO, and admin workflows
- ingestion and processing pipelines using Scrapy, Playwright, and structured automation
- internal tools for non-technical operators managing large catalogs and publishing tasks
- performance improvements through caching, backend optimization, AJAX batch processing, and frontend delivery work
- distributed task workflows using Celery and Redis

Results:

- reduced manual operational workload by up to **90%**
- improved website speed and responsiveness by roughly **70%**

Tech stack: `PHP`, `WordPress`, `WooCommerce`, `JavaScript`, `Python`, `Scrapy`, `Playwright`, `Celery`, `Redis`, `PostgreSQL`, `GA4`, `GTM`, `SEO`

---

### Dealer Flow AI

**Multi-tenant SaaS for automotive lead conversion**  
Repository: private, access available upon request

Dealer Flow AI helps dealership teams move inbound leads toward booked test drives using lead intake, AI-assisted qualification, deterministic inventory matching, appointment scheduling, and operator dashboards.

Highlights:

- authenticated user workflows and staff-facing dashboards
- multi-tenant modular monolith architecture
- scheduling rules, availability windows, and blackout logic
- AI assistance separated from deterministic business truth

Tech stack: `Next.js`, `TypeScript`, `NestJS`, `PostgreSQL`, `Prisma`, `Redis`, `BullMQ`, `Docker Compose`

---

### Nexus AI Growth Engine

**Multi-tenant lead qualification and agent workflow system**  
Repository: private, access available upon request

An agentic workflow platform coordinating AI-assisted discovery, triage, and drafting for multiple concurrent clients.

Highlights:

- LangGraph-based state machine coordinating specialized AI agents
- backend-enforced tenant isolation and UUID-scoped data access
- execution audit traces for transparent AI decisions
- explainability-first workflow design

Tech stack: `Python`, `FastAPI`, `LangGraph`, `Gemini`, `OpenAI`, `Supabase`, `PostgreSQL`, `Docker`

---

### Nexus Ingest

**Browser automation and distributed ingestion engine**  
Repository: private, access available upon request

A resilient ingestion system for high-friction data collection environments where uptime, routing intelligence, and reliability matter.

Highlights:

- Playwright-based browser automation and validation
- Redis-backed circuit breakers and retry orchestration
- tiered routing logic to reduce proxy cost
- high-volume distributed collection workflows

Tech stack: `Python`, `Celery`, `Redis`, `PostgreSQL`, `Playwright`, `BeautifulSoup`, `Docker`

## Toolbox

**Frontend:** React, Next.js 16, TypeScript, JavaScript, Vite, Tailwind CSS v4, responsive dashboards  
**Backend:** Python, FastAPI, Node.js, NestJS, REST APIs, server-side business logic  
**Workflow Orchestration:** Temporal (Cloud + local), durable workflows, activity design, signal/query patterns  
**QA and Testing:** pytest, integration testing against real databases, API verification, manual E2E, Playwright  
**Data and Auth:** PostgreSQL, Supabase, Prisma, pgvector, Auth0 v4, RBAC, tenant-scoped access  
**AI and Automation:** LangGraph, LangChain, OpenAI GPT-4o, Gemini, Claude, structured AI workflows, RAG, prompt engineering, Pydantic validation layers  
**Infrastructure:** Docker, Docker Compose, Redis, BullMQ, Celery, Linux, Vercel, Render, Neon  
**Web and E-Commerce:** WordPress, WooCommerce, Shopify, GA4, GTM, technical SEO, Core Web Vitals

## Engineering Highlights

- Reduced manual operational workload by up to **90%** through AI-assisted automation and structured pipelines
- Improved platform speed and responsiveness by roughly **70%** through performance engineering
- Built multi-tenant SaaS with strict RBAC, append-only audit trails, and JWT-enforced data isolation
- Shipped **365 integration tests** against a real PostgreSQL database — zero mocks, full workflow coverage
- Designed validation-first AI systems combining LLM reasoning with deterministic business logic for reliability
- Delivered complete role-based portals for operators, managers, and executives across complex workflow products

## What I Like Building

I enjoy building software that helps real operators move faster without losing control: dashboards, workflow systems, internal tools, AI-assisted business processes, API-driven products, and automation platforms with clean boundaries.

---

## 📫 Connect With Me

- **GitHub:** [github.com/abdupa](https://github.com/abdupa)
- **LinkedIn:** [linkedin.com/in/abemael-dupa-b2a768249](https://www.linkedin.com/in/abemael-dupa-b2a768249/)
- **Email:** dupa.abe@gmail.com
