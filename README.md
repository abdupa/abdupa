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

- **16 Temporal workflows** — W1 inquiry triage routing inbound messages to W9 order intake, W10–W11 quote support, W12–W13 support cases and billing disputes, W16 supplier intake, W17 eternal Gmail polling loop, plus scheduled workflows for quote aging, reorder monitoring, dormant accounts, daily operational briefs, fulfillment alerts, and payment follow-ups
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

**Production web platform for AI-powered product content, SEO automation, WordPress tooling, and distributed data workflows**  
Live site: https://gadgetph.com/

GadgetPH is a live production web platform serving a large Philippine consumer electronics audience. I designed and implemented AI-driven automation systems, distributed data pipelines, custom WordPress plugins, and SEO infrastructure to support product publishing, price comparison, catalog management, and content operations at scale.

The platform combines AI-assisted workflows with full-stack engineering, content automation, custom WooCommerce tooling, and validation-first publishing pipelines to reduce manual work while improving reliability, speed, and SEO performance.

---

#### Key Contributions

##### AI Workflow Automation

- Designed multi-stage AI pipelines that transformed raw scraped marketplace data into structured, SEO-ready, publishable outputs using LLM reasoning, validation, and feedback loops.
- Automated content generation and data-processing workflows, reducing manual operational workload by up to **90%**.
- Built repeatable AI-assisted workflows for product data enrichment, content transformation, and publishing preparation.

##### Prompt-Driven and Agent-Based Systems

- Built LangGraph-based orchestration workflows to coordinate planning, retrieval, validation, and synthesis across multi-step AI-assisted tasks.
- Applied advanced prompt engineering and workflow refinement across structured generation, content transformation, and operational automation use cases.
- Structured AI execution flows to improve traceability, control execution paths, and output reliability.

##### WordPress Plugin Development

- Designed and built two production WordPress plugins deployed live on GadgetPH.com and used by thousands of active site visitors.

**Product Offers Plugin v2.3.1**

A multi-source price comparison system featuring:

- Dynamic price comparison tables
- Historical price charts using Chart.js
- Price drop email alerts
- Custom database tables, including `wp_price_alerts`
- AJAX handlers with nonce security
- WooCommerce product integration
- Admin notification workflows

**Smartphone Price List Plugin v5.0.0**

A dynamic, filterable price list system featuring:

- Price change tracking
- Batch processing for large product catalogs
- Google Sheets price data integration
- Admin cache management UI with progress tracking
- Shortcode-based rendering through `[gph_price_list]`
- Specs processor pipeline for structured product data

##### SEO and Platform Engineering

- Implemented a full technical SEO stack, including Google Analytics 4, Google Tag Manager, Google Search Console integration, schema markup, XML sitemaps, and structured metadata across product pages.
- Optimized Core Web Vitals through caching strategies, lazy loading, asynchronous asset delivery, and backend performance improvements, increasing page speed scores by up to **70%**.
- Integrated the Google Search Console API to provide live SEO performance feedback and support data-driven content iteration.
- Built a content automation pipeline that delivered AI-generated, SEO-optimized product content directly into live WooCommerce product pages.

##### Distributed Processing and Reliability

- Implemented scalable ingestion pipelines using Scrapy, Playwright, Celery, and Redis to process thousands of product records concurrently.
- Improved throughput, resilience, and operational reliability through asynchronous task distribution and queue-based processing.
- Designed workflows capable of handling large product catalogs, marketplace updates, and recurring content refreshes.

##### Validation and Quality Control

- Developed Pydantic-based validation layers to sanitize, normalize, and standardize AI-generated outputs before publishing.
- Reduced workflow failure risk caused by inconsistent or non-deterministic model responses.
- Added quality-control steps to improve data consistency, publishing reliability, and downstream SEO performance.

---

#### Results

- Reduced manual operational workload by up to **90%** through AI-assisted workflow automation and structured pipelines.
- Improved website speed and responsiveness by up to **70%** through caching, lazy loading, asynchronous asset delivery, and backend optimization.
- Built production WordPress and WooCommerce tooling used on a live consumer electronics platform.
- Enabled scalable product publishing, price tracking, catalog updates, and SEO optimization through distributed workflows and AI-assisted automation.

---

#### Tech Stack

`PHP` · `WordPress` · `WooCommerce` · `JavaScript` · `Chart.js` · `Python` · `FastAPI` · `LangGraph` · `OpenAI GPT-4o` · `Pydantic` · `Scrapy` · `Playwright` · `Celery` · `Redis` · `PostgreSQL` · `Google Sheets API` · `Google Search Console API` · `GA4` · `GTM` · `Schema Markup` · `SEO`

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
