
<center>
<img src="https://generalbots.org/icons/general-bots-text.svg" />
</center>


<a href="https://github.com/generalbots/generalbots/graphs/contributors">
<img src="https://contrib.rocks/image?repo=generalbots/generalbots" />
</a>
# General Bots

**Enterprise-Grade LLM Orchestrator and AI Automation Platform**

A strongly-typed, self-hosted conversational platform built in Rust with 100+ workspace crates, focused on convention over configuration and code-less approaches.

---

## Architecture

![General Bots Architecture](architecture.svg)

---

## Platform Data Flow

![General Bots Platform](platform.svg)

---

## Workspace Crates

The **[generalbots](https://github.com/GeneralBots/generalbots)** repository is a Cargo workspace monorepo containing all crates under `botserver/crates/`:

### Core

| Crate | Description |
|-------|-------------|
| [**botserver**](https://github.com/GeneralBots/generalbots/tree/main/botserver) | Core API server — LLM orchestration, automation, routing |
| [**botlib**](https://github.com/GeneralBots/generalbots/tree/main/botlib) | Shared library — common types, utilities, traits |
| [**botcore**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcore) | Core shared logic, config, bootstrap, package manager |
| [**botcorebot**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcorebot) | Core bot abstractions and bot runtime |
| [**botcorepkg**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcorepkg) | Core package management (container installer) |
| [**botcoresession**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcoresession) | Session management |
| [**botcoreoauth**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcoreoauth) | OAuth authentication providers |
| [**botcoresecrets**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcoresecrets) | Secrets and vault integration |
| [**botcoredirectory**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcoredirectory) | Directory services |
| [**botdatabase**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botdatabase) | Database migrations and schema management |
| [**botapi**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botapi) | API route handlers and middleware |
| [**botdrive**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botdrive) | MinIO/Drive storage integration |
| [**botsettings**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsettings) | Settings and configuration management |
| [**botproviders**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botproviders) | External provider integrations |
| [**botintegrations**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botintegrations) | Third-party integration framework |

### BASIC Language & Compiler

| Crate | Description |
|-------|-------------|
| [**botbasic_compiler**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbasic_compiler) | BASIC script compiler (.bas → .ast) |
| [**botbasic_core**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbasic_core) | Core BASIC language runtime |
| [**botbasic_types**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbasic_types) | BASIC type system and values |
| [**botbasic_data**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbasic_data) | BASIC database keywords (GET, SAVE, FIND) |
| [**botbasic_ai**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbasic_ai) | BASIC AI keywords (USE KB, LLM, USE WEBSITE) |
| [**botbasic_comms**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbasic_comms) | BASIC communication keywords (SEND MAIL, SEND SMS) |
| [**botbasic_system**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbasic_system) | BASIC system keywords (TALK, HEAR, ADD_SUGGESTION) |

### AI & LLM

| Crate | Description |
|-------|-------------|
| [**botllm**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botllm) | LLM provider implementations — OpenAI, Groq, Claude, Anthropic |
| [**botqdrant**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botqdrant) | Qdrant vector database client |
| [**botsearch**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsearch) | Full-text search service |
| [**botresearch**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botresearch) | Web search, knowledge base exploration, deep research |
| [**botmodelsbridge**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botmodelsbridge) | BotModels API bridge |
| [**botmultimodal**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botmultimodal) | Multimodal AI — image, video, audio, speech |
| [**botkb**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botkb) | Knowledge base — embeddings, chunking, retrieval |
| [**botnvidia**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botnvidia) | NVIDIA GPU monitoring module |
| [**botvision**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botvision) | Computer vision and image processing |
| [**boteval**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/boteval) | LLM evaluation and benchmarking |
| [**botbiometry**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbiometry) | Biometric identification |

### Security

| Crate | Description |
|-------|-------------|
| [**botsecurity**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsecurity) | Security infrastructure — TLS integration |
| [**botsecurity-auth**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsecurity-auth) | Authentication providers |
| [**botsecurity-core**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsecurity-core) | Core security primitives |
| [**botsecurity-crypto**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsecurity-crypto) | Cryptographic operations |
| [**botsecurity-protection**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsecurity-protection) | Rate limiting, CSRF, security headers |

### Channels

| Crate | Description |
|-------|-------------|
| [**botchannels**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botchannels) | Channel adapter framework |
| [**botchannels-core**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botchannels-core) | Core channel abstractions |
| [**botwhatsapp**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botwhatsapp) | WhatsApp Business API connector |
| [**botmsteams**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botmsteams) | Microsoft Teams connector |
| [**bottelegram**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bottelegram) | Telegram Bot API connector |
| [**botinstagram**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botinstagram) | Instagram messaging connector |
| [**botemail**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botemail) | Email channel integration |
| [**bothandoff**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bothandoff) | Human handoff and escalation |
| [**botm365**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botm365) | Microsoft 365 integration |

### Business Applications

| Crate | Description |
|-------|-------------|
| [**botattendance**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botattendance) | Attendance — queue, SLA, webhooks |
| [**botattendant**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botattendant) | Contact center attendant and agent management |
| [**botbilling**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbilling) | Billing, invoicing, quotas, subscriptions |
| [**botcalendar**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcalendar) | Calendar and scheduling |
| [**botcompliance**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcompliance) | Compliance and regulatory tracking |
| [**botcontacts**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcontacts) | Contact and CRM management |
| [**botproducts**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botproducts) | Products, services, inventory, pricing |
| [**botproject**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botproject) | Project management |
| [**bottasks**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bottasks) | Task management |
| [**bottickets**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bottickets) | Ticket and helpdesk system |
| [**botmarketing**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botmarketing) | Marketing campaigns, email, WhatsApp, IP routing |
| [**botsocial**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsocial) | Social media management |
| [**botpeople**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botpeople) | People and HR management |
| [**bothr**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bothr) | HR and payroll management |
| [**botlearn**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botlearn) | Learning Management System (LMS) |
| [**botlegal**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botlegal) | Legal document management |
| [**botcloud**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcloud) | Cloud SaaS — signup, auth, org management |
| [**botsales**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsales) | Sales and pipeline management |
| [**botretail**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botretail) | Retail and POS management |
| [**botpos**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botpos) | Point of Sale integration |
| [**botbanking**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbanking) | Banking and financial operations |
| [**botfraud**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botfraud) | Fraud detection and prevention |
| [**botkyc**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botkyc) | Know Your Customer (KYC) verification |
| [**botitsm**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botitsm) | IT Service Management (ITSM) |
| [**botplan**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botplan) | Business planning and goals |
| [**botgl**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botgl) | General ledger accounting |
| [**boteditor**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/boteditor) | Bot editor and workflow designer |
| [**botvibe**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botvibe) | Vibecode integration |
| [**botdesktop**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botdesktop) | Desktop application support |
| [**botbrazil**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbrazil) | Brazil-specific regulations (NF, eSocial, FGTS) |
| [**botclock**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botclock) | Time clock and attendance |
| [**bottimeclock**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bottimeclock) | Time clock management |

### Productivity & Content

| Crate | Description |
|-------|-------------|
| [**botdocs**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botdocs) | Document processing, collaboration, conversion |
| [**botsheet**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsheet) | Spreadsheet processing |
| [**botsheet-core**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsheet-core) | Spreadsheet core engine |
| [**botslides**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botslides) | Presentation and slides |
| [**botpaper**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botpaper) | Paper and report generation |
| [**botplayer**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botplayer) | Media player |
| [**botvideo**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botvideo) | Video processing and meetings |
| [**botmeet**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botmeet) | Meeting and video conferencing |
| [**botminutes**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botminutes) | Meeting minutes transcription |
| [**botcanvas**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botcanvas) | Canvas and drawing |
| [**botdesigner**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botdesigner) | Visual designer |
| [**botweba**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botweba) | Web application builder |
| [**bottax**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bottax) | Tax calculation engine |
| [**botinventory**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botinventory) | Inventory management |
| [**boterp**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/boterp) | ERP integration framework |
| [**botgit**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botgit) | Git integration and version control |

### Infrastructure

| Crate | Description |
|-------|-------------|
| [**botdeployment**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botdeployment) | Deployment infrastructure |
| [**botmonitoring**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botmonitoring) | Monitoring, metrics, alerting, distributed tracing |
| [**bottimeseries**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bottimeseries) | Time-series metrics service (InfluxDB-compatible) |
| [**botmaintenance**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botmaintenance) | System maintenance and cleanup |
| [**botbrowser**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botbrowser) | Browser automation |
| [**botsources**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botsources) | Source code management |
| [**botautotask**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botautotask) | Automated task execution |
| [**botdashboards**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botdashboards) | Dashboard and visualization |
| [**botworkspaces**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botworkspaces) | Workspace management |
| [**botanalytics**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botanalytics) | Analytics, insights, OKR goals tracking |

### UI & Desktop

| Crate | Description |
|-------|-------------|
| [**botui**](https://github.com/GeneralBots/generalbots/tree/main/botui) | Pure web interface — HTMX-based |
| [**botapp**](https://github.com/GeneralBots/generalbots/tree/main/botapp) | Tauri desktop wrapper — native file access |
| [**botuifragments**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/botuifragments) | HTMX fragment rendering |
| [**bottemplates**](https://github.com/GeneralBots/generalbots/tree/main/botserver/crates/bottemplates) | Bot template management |

### Non-Workspace Directories

| Directory | Description |
|-----------|-------------|
| [**botbook**](https://github.com/GeneralBots/generalbots/tree/main/botbook) | Documentation — mdBook format |
| [**botdevice**](https://github.com/GeneralBots/generalbots/tree/main/botdevice) | Android, HarmonyOS, and IoT device integration |
| [**botmodels**](https://github.com/GeneralBots/generalbots/tree/main/botmodels) | AI model storage and management (Python/FastAPI) |
| [**botplugin**](https://github.com/GeneralBots/generalbots/tree/main/botplugin) | Plugin system |
| [**bottest**](https://github.com/GeneralBots/generalbots/tree/main/bottest) | Integration and E2E test suite |

---

## Organization Repositories

| Repository | Description | Language |
|------------|-------------|----------|
| [**generalbots**](https://github.com/GeneralBots/generalbots) | Core monorepo — 100+ workspace crates, LLM orchestration | Rust |
| [**botcoder**](https://github.com/GeneralBots/botcoder) | LLM code generator — AI-assisted coding | Rust |
| [**helicoder**](https://github.com/GeneralBots/helicoder) | VR coding environment — Bevy-based 3D code editor | Rust |
| [**magazine**](https://github.com/GeneralBots/magazine) | General Bots Magazine editions | — |
| [**website**](https://github.com/GeneralBots/website) | General Bots website — generalbots.org | TypeScript |
| [**.github**](https://github.com/GeneralBots/.github) | Organization profile and config | — |

---

## Quick Start

### Clone & Build

```bash
git clone https://github.com/GeneralBots/generalbots.git
cd generalbots
cargo build
```

### Run

```bash
cargo run --bin botserver
```

---

## Key Features

| Feature | Description |
|---------|-------------|
| Multi-Vendor LLM | Unified API for OpenAI, Groq, Claude, Anthropic, Azure |
| MCP and Tools | Instant tool creation from code and functions |
| Semantic Cache | 70% cost reduction on LLM calls |
| Web Automation | Browser automation with AI intelligence |
| Enterprise Connectors | CRM, ERP, database integrations |
| Version Control | Git-like history with rollback |
| Omnichannel | WhatsApp, Teams, Telegram, Instagram, Email, Web |
| Vector Search | Qdrant-powered RAG and semantic retrieval |
| VR Coding | Helicoder — Bevy-based 3D development environment |

---

## Documentation

- [Complete Docs](https://github.com/GeneralBots/generalbots/tree/main/botbook)
- [API Reference](https://github.com/GeneralBots/generalbots/tree/main/botserver/docs)
- [Website](https://generalbots.org)

---

## License

**AGPL-3.0** — True open source with dual licensing option.

---

Code Name: Guaribas
