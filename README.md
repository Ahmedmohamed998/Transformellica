# Transformellica AI Marketing Analytics & BI Assistant 📊

> AI-powered analytics platform for automated digital marketing intelligence, elite SEO auditing, and social media strategy — built for [Transformellica](https://app.thetransformix.com/).

## Overview

An advanced, always-on AI pipeline that ingests raw data from websites, SEO performance metrics, and social media footprints (TikTok, Instagram, Facebook). It automatically evaluates technical SEO, visual brand consistency, customer sentiment, and social growth metrics, using an intelligent multi-agent orchestrator to generate actionable, enterprise-grade marketing reports faster than any human agency.

---

## Features

- **Multi-Agent Orchestration** — Utilizes LangGraph to dynamically segment complex analysis tasks into specialized cognitive nodes (SEO, Social, Branding, Sentiment). This eradicates hallucination risks and enforces deep, isolated, expert-level evaluations per domain.
- **Asynchronous Scraping Engine** — Bypasses modern anti-bot systems to scrape rich interactive platforms (e.g., TikTok) via Selenium and custom cookie injection frameworks, seamlessly extracting video stats, textual content, and interaction metrics.
- **Deep Technical SEO Auditing** — Rapidly analyzes canonicals, H1-H6 semantic structuring, JSON-LD/Microdata schemas, Open Graph tags, and integrates with Google PageSpeed Insights for Lighthouse scoring via concurrent `aiohttp` pipelines.
- **Strategic AI Reporting** — Context-aware Azure OpenAI templates formulate highly structured marketing strategies, including embedded SWOT analysis, localized keyword cluster opportunities (e.g., MENA region tailoring), and precise actionable recommendations (Priority, Effort, Impact).
- **Enterprise Cost & Token Monitoring** — A custom telemetry wrapper natively intercepts all complex LLM interactions, logging token consumption, latency, and costs per pipeline stage to optimize ROI and model usage limits in real time.

---

## Architecture

```text
    Data Sources (Web, TikTok, Socials)
                │
   Async Scrapers (Selenium, AIOHTTP)
                │
    FastAPI / Flask Microservices
   ┌────────────┴───────────────┐
   │ LangGraph Orchestration    │
   │  ├─ analyze_seo()          │
   │  ├─ analyze_social()       │
   │  ├─ analyze_branding()     │
   │  └─ analyze_sentiment()    │
   └────────────┬───────────────┘
                │
         Azure OpenAI (GPT-5.2)
   (with custom Token Monitoring)
                │
    Comprehensive PDF Generation
  (Actionable JSON / Data pipelines)
```

## Tech Stack

| Layer | Technology |
|-------|-----------|
| **Core AI & Logic** | Python, Azure OpenAI (GPT-5.2-chat), Transformers, PyTorch |
| **Agent Orchestration** | LangChain, LangGraph |
| **Data Extraction** | Selenium, BeautifulSoup4, LXML, WebDriver Manager, AIOHTTP |
| **Backend API** | FastAPI, Flask, Pandas |
| **Observability** | Custom Token Monitor, MLflow |

---

## Core Data & AI Pipelines

### 1. LangGraph Agent State Machine
Instead of relying on a single monolithic LLM prompt that risks losing context, the system maintains a strict [AnalysisState] that flows through a directed graph of specialized AI agents. Each node runs its distinct evaluation, tracks its own token economy boundaries, validates structured output, and catches failures. Once [analyze_seo] and [analyze_social] nodes complete securely, the state merges into the concluding [generate_comprehensive] reporting node.

### 2. Advanced Prompt Engineering & Localization
The LLM acts strictly within a "Senior Strategy Consultant" persona. Prompts are heavily optimized by separating cacheable static instruction templates from dynamic variable injections. The model doesn't output "fluff"; it strictly formats actionable responses with measurable expectations, specifically tailored for regional audience nuances (like prioritizing Arabic/English metadata alignments in the Middle East).

### 3. Stealth Data Acquisition Modules
The TikTok data extraction pipeline leverages headless, optimized Chrome instances equipped with behavior-mimicking scripts, DOM scrolling heuristics, and environment-variable-backed session restoring. This effortlessly retrieves accurate follower counts, dynamic content, and interaction numbers natively without triggering aggressive automated bot defenses.

---

## License

Private — source code and business logic are proprietary to Transformix. This document serves purely as a high-level architectural overview for project showcase purposes.
