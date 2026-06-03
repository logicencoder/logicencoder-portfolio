# Logic Encoder — Portfolio

**Orchestration · AI coding agents · full stack · production, end to end**

I build and ship software across the full stack — orchestrating AI coding agents alongside architecture, Python and Node.js backends, real-time dashboards, web and standalone apps, WordPress themes and plugins, blockchain tooling, trading systems, and monitoring. I design the system, review and integrate the code, and deploy where the project belongs: **Linux VPS, dedicated hardware, Docker, or cloud** when that is the right fit. Then I debug under real load, profile what is slow, and improve from production data. One owner from first commit to live.

| | |
|---|---|
| **Site** | [logicencoder.com](https://logicencoder.com/) |
| **Live apps** | [logicencoder.com/applications/](https://logicencoder.com/applications/) |
| **Blog** | [logicencoder.com/blog/](https://logicencoder.com/blog/) |
| **About** | [logicencoder.com/about/](https://logicencoder.com/about/) |
| **Contact** | [logicencoder.com/contact/](https://logicencoder.com/contact/) |

---

## What I build

**Web & standalone** — Browser apps, local operator tools, hybrid setups: trading dashboards, analytics viewers, service panels, hardware monitors, custom workflows. UI, data layer, auth, and deployment in one deliverable.

**Backends & APIs** — Python 3 / FastAPI / asyncio as primary stack; Node.js / TypeScript when the project needs it. REST and WebSocket APIs, workers, aggregation pipelines, scheduled jobs, Telegram backends. Structured to run on a VPS without mandatory Kubernetes.

**Realtime & blockchain** — Live market feeds, on-chain events, analytics streams, monitoring and decoding. Ingestion, normalization, caching, dashboards that update in real time. On-chain execution where the product requires it.

**Data** — Time buckets, rolling windows, ranked lists, ratios, exports. SQLite, PostgreSQL, DuckDB, in-memory caches — chosen by access pattern and hosting cost.

**WordPress** — Custom themes, plugins, REST for JS consumers, caching that survives publish. Live plugins that connect a public WP front end to private Python or Node backends (tunnels when needed).

**Infrastructure & ops** — Linux production: nginx, systemd, SSL, logs, firewall, git-based deploy. Profiling and measured fixes. App-level security: validation, rate limits, secrets across environments.

---

## Stack (production)

| Layer | Choices |
|-------|---------|
| **Backend** | Python / FastAPI / asyncio; Node.js / TypeScript where it fits |
| **Frontend** | HTML, CSS, vanilla JS for operator UIs; React / Vite when it simplifies; PHP / WP templates for CMS sites |
| **Data** | SQLite, PostgreSQL, DuckDB, JSON caches |
| **Infra** | Linux VPS, dedicated servers, Docker, cloud when appropriate; monitoring dashboards |

---

## GitHub

Private repos hold implementation; public **overview** repos hold scope, screenshots, and architecture narrative.

| | Pattern | Visibility |
|---|---------|------------|
| App / worker code | `{name}` | Private |
| Product overview | `{name}-overview` | Public |
| WordPress plugin code | `{name}-plugin` | Private |
| Plugin overview | `{name}-plugin-overview` | Public |

---

## Live on LogicEncoder.com

### [Ethereum Gas Tracker](https://logicencoder.com/ethereum-gas-tracker/)

![ETH Gas Tracker](https://raw.githubusercontent.com/logicencoder/eth-gas-live-backend-overview/main/assets/eth-gas-tracker-overview.png)

Live Gwei, history, heatmaps, fee calculator, alerts.  
**Overview:** [eth-gas-live-backend-overview](https://github.com/logicencoder/eth-gas-live-backend-overview) · [eth-gas-live-plugin-overview](https://github.com/logicencoder/eth-gas-live-plugin-overview)

### [MEXC — live trading statistics](https://logicencoder.com/mexc-app/)

![MEXC Live Stats](https://raw.githubusercontent.com/logicencoder/mexc-live-stats-plugin-overview/main/screenshot.png)

Per-pair buy/sell stats, live dashboard, async backend, SEO snapshots.  
**Overview:** [mexc-live-stats-backend-overview](https://github.com/logicencoder/mexc-live-stats-backend-overview) · [mexc-live-stats-plugin-overview](https://github.com/logicencoder/mexc-live-stats-plugin-overview)

### [0xDNX DHIP V2 Richlist](https://logicencoder.com/0xdnx-dhip-v2-richlist/)

Holder ranks, wallets, concentration — on-chain tables.  
**Overview:** [dynex-0xdnx-dhip-richlist-plugin-overview](https://github.com/logicencoder/dynex-0xdnx-dhip-richlist-plugin-overview) · [dynex-0xdnx-dhip-richlist-monitor-overview](https://github.com/logicencoder/dynex-0xdnx-dhip-richlist-monitor-overview)

### [Dynex large transactions monitor](https://logicencoder.com/dynex-large-transactions-monitor/)

Large transfers with threshold filter and decoded fields.  
**Overview:** [dynex-large-transactions-plugin-overview](https://github.com/logicencoder/dynex-large-transactions-plugin-overview)

---

## Trading & operator tools

| Product | Summary | Overview |
|---------|---------|----------|
| **MEXC Trading Dashboard + bots** | Manual UI, automation modes, orderbook, diagnostics — local operator runtime | [mexc_trading_app-overview](https://github.com/logicencoder/mexc_trading_app-overview) · [mexc-trading-dashboard-bot-suite-overview](https://github.com/logicencoder/mexc-trading-dashboard-bot-suite-overview) |
| **DNX Swap WebApp** | Swap execution, presets, safety and recovery tooling | [dnx-swap-webapp-overview](https://github.com/logicencoder/dnx-swap-webapp-overview) |
| **ETH Chain Swaps Monitor** | Swap detection, decode, alerts, operator dashboard | [eth-chain-swaps-monitor-overview](https://github.com/logicencoder/eth-chain-swaps-monitor-overview) |
| **Multi-coin monitor** | Cross-asset monitoring and alerts | [multi-coin-monitor-overview](https://github.com/logicencoder/multi-coin-monitor-overview) |

![MEXC Dashboard](https://raw.githubusercontent.com/logicencoder/mexc_trading_app-overview/main/assets/mexc-trading-dashboard-bot-overview.png)

![DNX Swap UI](https://raw.githubusercontent.com/logicencoder/dnx-swap-webapp-overview/main/assets/ui.png)

![ETH Chain Swaps Monitor](https://raw.githubusercontent.com/logicencoder/eth-chain-swaps-monitor-overview/main/assets/eth-chain-swaps-monitor-overview.png)

---

## WordPress & commerce

| Product | Summary | Overview |
|---------|---------|----------|
| **Logic Encoder theme** | Public site theme | [logic-encoder-theme-overview](https://github.com/logicencoder/logic-encoder-theme-overview) |
| **LogicEncoder Shop** | App catalogue + store backend / Mini App | [le-shop-plugin-overview](https://github.com/logicencoder/le-shop-plugin-overview) · [le-crypto-app-store-overview](https://github.com/logicencoder/le-crypto-app-store-overview) |
| **Site settings** | SEO, security, hardening | [le-settings-plugin-overview](https://github.com/logicencoder/le-settings-plugin-overview) |
| **Login system** | Access control | [logicencoder-login-system-plugin-overview](https://github.com/logicencoder/logicencoder-login-system-plugin-overview) |
| **Sitemap manager** | Sitemaps | [logicencoder-sitemap-manager-plugin-overview](https://github.com/logicencoder/logicencoder-sitemap-manager-plugin-overview) |
| **Visitor stats** | Analytics, short links | [wp-visitor-stats-plugin-overview](https://github.com/logicencoder/wp-visitor-stats-plugin-overview) |

---

## Platform & tooling

| Product | Summary | Overview |
|---------|---------|----------|
| **Service manager** | One dashboard for processes, health, ops | [universal-service-manager-overview](https://github.com/logicencoder/universal-service-manager-overview) |
| **Cloudflare ops (CFMS)** | Tunnel and zone management UI | [cfms-overview](https://github.com/logicencoder/cfms-overview) |
| **Karaoke studio** | Transcription and render pipeline | [le-karaoke-studio-overview](https://github.com/logicencoder/le-karaoke-studio-overview) |
| **Coding agent workstation** | LLM tools and local API | [le-cs-agent-overview](https://github.com/logicencoder/le-cs-agent-overview) |
| **Hardware monitor** | Live machine metrics in the browser | [hardware-monitor-overview](https://github.com/logicencoder/hardware-monitor-overview) |
| **System monitor (TUI)** | CPU, RAM, disk, net, GPU | [system-monitor-app](https://github.com/logicencoder/system-monitor-app) |

---

## Also public

- [react-vite-architecture-for-dummies](https://github.com/logicencoder/react-vite-architecture-for-dummies) — architecture docs style for handoff  
- [logicencoder-portfolio](https://github.com/logicencoder/logicencoder-portfolio) — this index  

---

## Fit for roles (quick map)

| Looking for | Evidence |
|-------------|----------|
| Full-stack delivery | Live apps on logicencoder.com + private code repos |
| Python / async backends | FastAPI products above |
| Realtime / WebSocket | MEXC stats, monitors, trading UIs |
| WordPress + private API | Plugin overviews + live deployments |
| Orchestration / agentic workflow | le-cs-agent, production discipline, architecture docs |
| Performance & ops | Monitoring tools, measured production fixes |

---

## Looking for collaboration

- Real-time dashboards and trading operator tools  
- DeFi / on-chain monitoring and execution  
- WordPress ↔ backend integration  
- Backend services and data pipelines  
- Performance and production hardening  

---

## Background

Formal grounding in **HTML, CSS, PHP, databases** (courses and earlier work). Day-to-day delivery is **agentic coding**: I orchestrate AI coding agents, own architecture, integration, review, deploy, tuning, and measurement — not encyclopedic syntax recall in every language. I work in **Python, JavaScript, TypeScript**, and whatever else the product needs; depth is in **shipping, debugging under load, and optimization from real metrics**.

I do not claim to know every framework by heart. I claim **clear architecture**, **production ownership**, and **systems that stay up** when operators depend on them.

---

## Availability

Python / FastAPI · realtime data · WordPress integrations · VPS / cloud / dedicated Linux · solo end-to-end delivery.

**Contact:** [logicencoder.com/contact/](https://logicencoder.com/contact/)  
**GitHub:** [github.com/logicencoder](https://github.com/logicencoder)
