
<p align="center">
  <img src="https://generalbots.org/icons/general-bots-text.svg" width="400" alt="General Bots" />
</p>

<p align="center">
  <a href="https://github.com/generalbots/generalbots">
    <img src="https://img.shields.io/badge/rust-1.85+-orange.svg?logo=rust" alt="Rust" />
  </a>
  <a href="https://github.com/generalbots/generalbots/actions">
    <img src="https://img.shields.io/github/actions/workflow/status/generalbots/generalbots/ci.yml?branch=main" alt="CI" />
  </a>
  <a href="https://github.com/generalbots/generalbots/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/license-AGPL--3.0-blue.svg" alt="License" />
  </a>
  <a href="https://github.com/generalbots/generalbots">
    <img src="https://img.shields.io/github/repo-size/generalbots/generalbots" alt="Repo" />
  </a>
  <br />
  <strong>Enterprise-Grade LLM Orchestrator &amp; AI Automation Platform</strong>
  <br />
  100+ Rust crates · Monorepo · Convention over Configuration
</p>

---

## Architecture

![Architecture](architecture.svg)

![Platform](platform.svg)

---

## Quick Start

```bash
git clone https://github.com/GeneralBots/generalbots.git
cd generalbots
cargo build --bin botserver
cargo run --bin botserver
```

---

## Workspace Crates

All 100+ crates live under [`botserver/crates/`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates):

### Core :: botcore

| Crate | Description |
|-------|-------------|
| [`botserver`](https://github.com/GeneralBots/generalbots/tree/main/botserver) | API server — LLM orchestration, routing, automation |
| [`botlib`](https://github.com/GeneralBots/generalbots/tree/main/botlib) | Shared types, traits, HTTP client |
| [`botcore`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcore) | Shared config, bootstrap, package manager |
| [`botcorebot`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcorebot) | Bot abstractions & runtime |
| [`botcorepkg`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcorepkg) | Container package installer |
| [`botcoresession`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcoresession) | Session management |
| [`botcoreoauth`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcoreoauth) | OAuth providers |
| [`botcoresecrets`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcoresecrets) | Secrets & vault integration |
| [`botcoredirectory`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcoredirectory) | Directory services (Zitadel) |
| [`botdatabase`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botdatabase) | Migrations & schema |
| [`botdrive`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botdrive) | MinIO/Drive storage |
| [`botsettings`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsettings) | Configuration management |
| [`botapi`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botapi) | Route handlers & middleware |

### Language :: botbasic

| Crate | Description |
|-------|-------------|
| [`botbasic_compiler`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbasic_compiler) | BASIC compiler (.bas → .ast) |
| [`botbasic_core`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbasic_core) | BASIC runtime engine |
| [`botbasic_types`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbasic_types) | Type system |
| [`botbasic_data`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbasic_data) | Data keywords: `GET`, `SAVE`, `FIND` |
| [`botbasic_ai`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbasic_ai) | AI keywords: `USE KB`, `LLM`, `USE WEBSITE` |
| [`botbasic_comms`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbasic_comms) | Comms keywords: `SEND MAIL`, `SEND SMS` |
| [`botbasic_system`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbasic_system) | System keywords: `TALK`, `HEAR`, `ADD_SUGGESTION` |

### AI & Search :: botllm

| Crate | Description |
|-------|-------------|
| [`botllm`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botllm) | LLM providers — OpenAI, Groq, Claude, Anthropic, Azure |
| [`botqdrant`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botqdrant) | Qdrant vector database |
| [`botsearch`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsearch) | Full-text search |
| [`botresearch`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botresearch) | Web search, KB exploration, deep research |
| [`botmodelsbridge`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botmodelsbridge) | BotModels API bridge |
| [`botmultimodal`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botmultimodal) | Image, video, audio, speech |
| [`botkb`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botkb) | Knowledge base — embeddings & retrieval |
| [`botnvidia`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botnvidia) | NVIDIA GPU monitoring |
| [`botvision`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botvision) | Computer vision |
| [`boteval`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/boteval) | LLM evaluation |
| [`botbiometry`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbiometry) | Biometric identification |

### Security :: botsecurity

| Crate | Description |
|-------|-------------|
| [`botsecurity`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsecurity) | TLS integration, security setup |
| [`botsecurity-auth`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsecurity-auth) | Authentication providers |
| [`botsecurity-core`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsecurity-core) | Security primitives |
| [`botsecurity-crypto`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsecurity-crypto) | Cryptographic operations |
| [`botsecurity-protection`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsecurity-protection) | Rate limiting, CSRF, security headers |

### Channels :: botchannels

| Crate | Description |
|-------|-------------|
| [`botchannels`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botchannels) | Channel adapter framework |
| [`botchannels-core`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botchannels-core) | Core channel abstractions |
| [`botwhatsapp`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botwhatsapp) | WhatsApp Business API |
| [`botmsteams`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botmsteams) | Microsoft Teams |
| [`bottelegram`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bottelegram) | Telegram Bot API |
| [`botinstagram`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botinstagram) | Instagram messaging |
| [`botemail`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botemail) | Email channel |
| [`bothandoff`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bothandoff) | Human handoff |
| [`botm365`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botm365) | Microsoft 365 integration |

### Business :: botapps

| Crate | Description |
|-------|-------------|
| [`botbilling`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbilling) | Billing, invoicing, subscriptions |
| [`botattendance`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botattendance) | Queue & SLA management |
| [`botattendant`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botattendant) | Contact center agent management |
| [`botcloud`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcloud) | SaaS signup, auth, org management |
| [`botcontacts`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcontacts) | CRM |
| [`botproducts`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botproducts) | Products & inventory |
| [`bottickets`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bottickets) | Helpdesk |
| [`bottasks`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bottasks) | Task management |
| [`botproject`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botproject) | Project management |
| [`botpeople`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botpeople) | HR management |
| [`botmarketing`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botmarketing) | Marketing campaigns |
| [`botsocial`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsocial) | Social media management |
| [`botlearn`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botlearn) | LMS |
| [`botlegal`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botlegal) | Legal document management |
| [`botcompliance`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcompliance) | Regulatory compliance |
| [`botcalendar`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcalendar) | Calendar & scheduling |
| [`botsales`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsales) | Sales pipeline |
| [`botretail`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botretail) | Retail & POS |
| [`botbanking`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbanking) | Banking operations |
| [`botfraud`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botfraud) | Fraud detection |
| [`botkyc`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botkyc) | KYC verification |
| [`botitsm`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botitsm) | IT Service Management |
| [`bothr`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bothr) | HR & payroll |
| [`botplan`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botplan) | Business planning |
| [`botgl`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botgl) | General ledger |
| [`botbrazil`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbrazil) | Brazil regulations (NF, eSocial, FGTS) |
| [`botclock`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botclock) | Time clock |
| [`bottimeclock`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bottimeclock) | Time clock management |
| [`botinventory`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botinventory) | Inventory management |
| [`boterp`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/boterp) | ERP integration |
| [`boteditor`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/boteditor) | Bot editor & workflow designer |
| [`botvibe`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botvibe) | Vibecode integration |
| [`botdesktop`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botdesktop) | Desktop app support |

### Content :: botdocs

| Crate | Description |
|-------|-------------|
| [`botdocs`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botdocs) | Document processing & conversion |
| [`botsheet`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsheet) | Spreadsheet processing |
| [`botsheet-core`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsheet-core) | Spreadsheet engine |
| [`botslides`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botslides) | Presentations |
| [`botpaper`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botpaper) | Reports & paper generation |
| [`botplayer`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botplayer) | Media player |
| [`botvideo`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botvideo) | Video processing |
| [`botmeet`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botmeet) | Video conferencing |
| [`botminutes`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botminutes) | Meeting transcription |
| [`botcanvas`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcanvas) | Canvas & drawing |
| [`botdesigner`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botdesigner) | Visual designer |
| [`botweba`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botweba) | Web app builder |
| [`bottax`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bottax) | Tax calculation |
| [`botgit`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botgit) | Git integration |

### Infrastructure :: botinfra

| Crate | Description |
|-------|-------------|
| [`botdeployment`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botdeployment) | Deployment infrastructure |
| [`botmonitoring`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botmonitoring) | Metrics, alerting, tracing |
| [`bottimeseries`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bottimeseries) | InfluxDB-compatible time-series |
| [`botmaintenance`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botmaintenance) | System maintenance |
| [`botbrowser`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbrowser) | Browser automation |
| [`botsources`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsources) | Source code management |
| [`botautotask`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botautotask) | Automated task execution |
| [`botdashboards`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botdashboards) | Dashboard & visualization |
| [`botworkspaces`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botworkspaces) | Workspace management |
| [`botanalytics`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botanalytics) | Analytics & OKR goals |

### UI :: botui

| Crate | Description |
|-------|-------------|
| [`botui`](https://github.com/GeneralBots/generalbots/tree/main/botui) | Pure web interface — HTMX-based |
| [`botapp`](https://github.com/GeneralBots/generalbots/tree/main/botapp) | Tauri desktop wrapper |
| [`botuifragments`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botuifragments) | HTMX fragment rendering |
| [`bottemplates`](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bottemplates) | Bot & prompt templates |

### External Directories

| Path | Description |
|------|-------------|
| [`botbook`](https://github.com/GeneralBots/generalbots/tree/main/botbook) | mdBook documentation |
| [`botdevice`](https://github.com/GeneralBots/generalbots/tree/main/botdevice) | Android, HarmonyOS, IoT |
| [`botmodels`](https://github.com/GeneralBots/generalbots/tree/main/botmodels) | AI model server (Python/FastAPI) |
| [`botplugin`](https://github.com/GeneralBots/generalbots/tree/main/botplugin) | Plugin system |
| [`bottest`](https://github.com/GeneralBots/generalbots/tree/main/bottest) | Integration & E2E tests |

---

## Organization :: generalbots

| Repository | Description |
|------------|-------------|
| [generalbots](https://github.com/GeneralBots/generalbots) | Core monorepo — Rust |
| [botcoder](https://github.com/GeneralBots/botcoder) | LLM code generator — Rust |
| [helicoder](https://github.com/GeneralBots/helicoder) | VR coding environment (Bevy) — Rust |
| [magazine](https://github.com/GeneralBots/magazine) | Magazine editions |
| [website](https://github.com/GeneralBots/website) | generalbots.org — TypeScript |
| [.github](https://github.com/GeneralBots/.github) | Organization profile & config |

---

## Features

- **Multi-Vendor LLM** — OpenAI, Groq, Claude, Anthropic, Azure (unified API)
- **MCP & Tools** — Instant tool creation from code
- **Semantic Cache** — Up to 70% cost reduction on LLM calls
- **Web Automation** — AI-driven browser automation
- **Enterprise Connectors** — CRM, ERP, databases
- **Omnichannel** — WhatsApp, Teams, Telegram, Instagram, Email, Web
- **Vector Search** — Qdrant-powered RAG & semantic retrieval
- **BASIC Language** — Full DSL for bot scripting (`.bas` → `.ast` compiler)
- **Version Control** — Git-like history with rollback

---

## Docs

- [Complete Docs](https://github.com/GeneralBots/generalbots/tree/main/botbook)
- [API Reference](https://github.com/GeneralBots/generalbots/tree/main/botserver/docs)
- [Website](https://generalbots.org)

---

## License

`AGPL-3.0` — True open source with dual licensing option.

---

<p align="center">
  <code>Code Name: Guaribas</code>
</p>
