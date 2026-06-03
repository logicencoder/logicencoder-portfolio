# Logic Encoder — Web3 tools, realtime systems & full-stack delivery

I build **real-time dashboards**, crypto analytics, trading operator UIs, gas and mempool tooling, WordPress themes and plugins, and the backends that power them. Systems are **multi-asset** and **multi-exchange ready** where the product calls for it — not locked to one pair or chain.

I am self-taught, shipped this stack from zero, and keep improving by **measuring production** (dedicated SOL server, Hostinger WordPress, controlled tunnels) rather than demo-only deployments. I own projects end to end: research, architecture, implementation, deploy, and fixes under real load.

Most **code** lives in private GitHub repos (`{app}` or `{name}-plugin`). Each major product has a **public overview** (`{app}-overview` or `{name}-plugin-overview`) with screenshots, scope, and what/why/who per feature. Deep implementation notes are in private `README.md` and `ARCHITECTURE.md` where applicable.

| Link | |
|------|---|
| **Live applications** | [logicencoder.com/applications/](https://logicencoder.com/applications/) |
| **Blog** (production write-ups) | [logicencoder.com/blog/](https://logicencoder.com/blog/) |
| **About** | [logicencoder.com/about/](https://logicencoder.com/about/) |
| **Contact** | [logicencoder.com/contact/](https://logicencoder.com/contact/) |

---

## What I focus on

- **Python + FastAPI** — async APIs, background workers, WebSocket fan-out, structured logging  
- **Realtime data** — hybrid REST + WebSocket: snapshots for first paint, streams for deltas  
- **Data-heavy dashboards** — ranked feeds, heatmaps, aggregation under load — not vanity charts  
- **Low-resource operation** — caching, prebuilt templates, RAM mirrors of chain head, minimal RPC chatter  
- **WordPress as public surface** — PHP plugins and custom theme; Node/Python on SOL for ingestion, money-moving logic, and tunnels  
- **Honest delivery** — I state whether something is live on the web, standalone local, or SOL-only  

---

## Core stack

**Backend:** Python 3, FastAPI, asyncio; Node/Fastify for `le-crypto-app-store`; Web3.py-style execution (swaps, transfers, nonce/gas lifecycle); DuckDB / SQLite / PostgreSQL / JSON caches by access pattern.

**Frontend:** Operator HTML/CSS/JS dashboards; WordPress (PHP) + [logic-encoder-theme](https://github.com/logicencoder/logic-encoder-theme-overview); React/Vite where it genuinely simplifies the UI ([react-vite-architecture-for-dummies](https://github.com/logicencoder/react-vite-architecture-for-dummies)).

**Infrastructure:** **SOL** (`/home/sol/lojzo`) — bots, gas SSR, MEXC apps, DNX swap, monitors, USM; **Hostinger** — public WP plugins; **WSL** — dev and diff vs prod; **Cloudflare tunnels** — controlled exposure of private backends; observability via [hardware-monitor](https://github.com/logicencoder/hardware-monitor-overview) and [system-monitor-app](https://github.com/logicencoder/system-monitor-app).

---

## How to read my GitHub

| Type | Name pattern | Visibility |
|------|--------------|------------|
| Application code | `{app}` | Private |
| Marketing / scope | `{app}-overview` | Public |
| WordPress plugin code | `{name}-plugin` | Private |
| WP plugin marketing | `{name}-plugin-overview` | Public |

No `-private` / `-public` suffixes. **le-shop-plugin** and **le-settings-plugin** are different products. **le-crypto-app-store** is the SOL backend, not a WordPress plugin name.

---

## Live on LogicEncoder.com

Public tools with overview repos and production backends on SOL.

### Ethereum Gas Tracker

![ETH Gas Tracker](https://raw.githubusercontent.com/logicencoder/eth-gas-live-backend-overview/main/assets/eth-gas-tracker-overview.png)

**Features:** live Gwei, history charts, heatmaps, fee calculator, alerts, mission-control metrics  
**Live:** [logicencoder.com/ethereum-gas-tracker/](https://logicencoder.com/ethereum-gas-tracker/)  
**Overviews:** [eth-gas-live-backend-overview](https://github.com/logicencoder/eth-gas-live-backend-overview) · [eth-gas-live-plugin-overview](https://github.com/logicencoder/eth-gas-live-plugin-overview)  
**Code (private):** `eth-gas-live-backend`, `eth-gas-live-plugin`

### MEXC — live trading statistics

![MEXC Exchange Live Stats](https://raw.githubusercontent.com/logicencoder/mexc-live-stats-plugin-overview/main/screenshot.png)

**Features:** buy/sell volume, per-pair stats, live dashboard, async ingestion, snapshot/SEO publishing  
**Live:** [logicencoder.com/mexc-app/](https://logicencoder.com/mexc-app/)  
**Overviews:** [mexc-live-stats-backend-overview](https://github.com/logicencoder/mexc-live-stats-backend-overview) · [mexc-live-stats-plugin-overview](https://github.com/logicencoder/mexc-live-stats-plugin-overview)  
**Code (private):** `mexc-live-stats-backend`, `mexc-live-stats-plugin`

### 0xDNX DHIP V2 Richlist

**Features:** DHIP v2 holder ranks, wallet lists, concentration — sortable tables from on-chain data  
**Live:** [logicencoder.com/0xdnx-dhip-v2-richlist/](https://logicencoder.com/0xdnx-dhip-v2-richlist/) · [guide](https://logicencoder.com/wrapped-dynex-richlist-0xdnx-dvhip-v2/)  
**Overviews:** [dynex-0xdnx-dhip-richlist-plugin-overview](https://github.com/logicencoder/dynex-0xdnx-dhip-richlist-plugin-overview) · [dynex-0xdnx-dhip-richlist-monitor-overview](https://github.com/logicencoder/dynex-0xdnx-dhip-richlist-monitor-overview)  
**Code (private):** `dynex-0xdnx-dhip-richlist-plugin`, `dynex-0xdnx-dhip-richlist-monitor`

### Dynex large transactions monitor

**Features:** large DNX transfers as they hit the chain — threshold filter and decoded fields  
**Live:** [logicencoder.com/dynex-large-transactions-monitor/](https://logicencoder.com/dynex-large-transactions-monitor/)  
**Overview:** [dynex-large-transactions-plugin-overview](https://github.com/logicencoder/dynex-large-transactions-plugin-overview)  
**Code (private):** `dynex-large-transactions-plugin` (+ SOL worker `dnx_large_txs`)

---

## Trading & operator systems (SOL / local-first)

### MEXC Trading Dashboard + multi-mode automation

![MEXC Dashboard](https://raw.githubusercontent.com/logicencoder/mexc_trading_app-overview/main/assets/mexc-trading-dashboard-bot-overview.png)

**Features:** manual trading UI, multi-mode bots, live orderbook/trades, diagnostics  
**Delivery:** standalone on operator hardware (production on SOL)  
**Overviews:** [mexc_trading_app-overview](https://github.com/logicencoder/mexc_trading_app-overview) · [mexc-trading-dashboard-bot-suite-overview](https://github.com/logicencoder/mexc-trading-dashboard-bot-suite-overview)  
**Code (private):** `mexc_trading_app`, `mexc-trading-dashboard-bot-suite`

### DNX Swap WebApp

![DNX Swap UI](https://raw.githubusercontent.com/logicencoder/dnx-swap-webapp-overview/main/assets/ui.png)

**Features:** DNX⇄USDC presets, config gas, MEV builders, recovery tooling, mempool-aware controls  
**Delivery:** standalone operator runtime (not the primary public WP app)  
**Overview:** [dnx-swap-webapp-overview](https://github.com/logicencoder/dnx-swap-webapp-overview)  
**Code (private):** `dnx-swap-webapp`

### ETH Chain Swaps Monitor

![ETH Chain Swaps Monitor](https://raw.githubusercontent.com/logicencoder/eth-chain-swaps-monitor-overview/main/assets/eth-chain-swaps-monitor-overview.png)

**Features:** swap detection, tx decoding, alert feed, operator dashboard  
**Delivery:** local-first on SOL; public site when released  
**Overview:** [eth-chain-swaps-monitor-overview](https://github.com/logicencoder/eth-chain-swaps-monitor-overview)  
**Code (private):** `eth-chain-swaps-monitor`

### Multi-coin monitor

**Features:** cross-coin monitoring and alerting for operator workflows  
**Overview:** [multi-coin-monitor-overview](https://github.com/logicencoder/multi-coin-monitor-overview)  
**Code (private):** `multi-coin-monitor`

---

## WordPress & catalogue (logicencoder.com)

### Logic Encoder theme

Custom theme for the public site (performance, layout, blog/applications templates).  
**Overview:** [logic-encoder-theme-overview](https://github.com/logicencoder/logic-encoder-theme-overview) · **Code (private):** `logic-encoder-theme`

### LogicEncoder Shop + Telegram store

**Features:** WP `application` posts as catalogue; webhook sync to Node store on SOL; Mini App checkout  
**Overview:** [le-shop-plugin-overview](https://github.com/logicencoder/le-shop-plugin-overview) · [le-crypto-app-store-overview](https://github.com/logicencoder/le-crypto-app-store-overview)  
**Code (private):** `le-shop-plugin`, `le-crypto-app-store`

### le-settings (site hygiene — separate product)

SEO, security headers, brute-force protection, caching discipline.  
**Overview:** [le-settings-plugin-overview](https://github.com/logicencoder/le-settings-plugin-overview) · **Code (private):** `le-settings-plugin`

### Other production plugins

| Product | Overview |
|---------|----------|
| Login / access | [logicencoder-login-system-plugin-overview](https://github.com/logicencoder/logicencoder-login-system-plugin-overview) |
| Sitemap manager | [logicencoder-sitemap-manager-plugin-overview](https://github.com/logicencoder/logicencoder-sitemap-manager-plugin-overview) |
| Visitor stats & short links | [wp-visitor-stats-plugin-overview](https://github.com/logicencoder/wp-visitor-stats-plugin-overview) |

---

## Platform, media & agent tooling (SOL)

| Project | What it does | Overview |
|---------|--------------|----------|
| **Universal Service Manager** | Start/stop/health for many SOL processes from one dashboard | [universal-service-manager-overview](https://github.com/logicencoder/universal-service-manager-overview) |
| **le-karaoke-studio** | GPU-assisted transcription and karaoke render pipeline | [le-karaoke-studio-overview](https://github.com/logicencoder/le-karaoke-studio-overview) |
| **le-cs-agent** | LLM coding workstation (orchestration, tools, local API) | [le-cs-agent-overview](https://github.com/logicencoder/le-cs-agent-overview) |
| **hardware-monitor** | Browser dashboard via WebSocket hardware metrics | [hardware-monitor-overview](https://github.com/logicencoder/hardware-monitor-overview) |
| **system-monitor-app** | Linux TUI — CPU/RAM/disk/net/GPU/sensors | [system-monitor-app](https://github.com/logicencoder/system-monitor-app) (public app repo) |

---

## Supporting public repositories

- [react-vite-architecture-for-dummies](https://github.com/logicencoder/react-vite-architecture-for-dummies) — how I document architecture for handoff  
- [logicencoder-portfolio](https://github.com/logicencoder/logicencoder-portfolio) — this index  

---

## Requirement → evidence (quick match)

| Typical requirement | Where to look |
|---------------------|---------------|
| Python / FastAPI backend | Gas, MEXC stats, DNX swap, ETH swaps, store backend — private `ARCHITECTURE.md` |
| Realtime architecture | WebSocket + REST in all overview repos above |
| Performance / low RPC | DNX swap (base fee cache, balance RAM); gas SSR design |
| Analytics mindset | Gas heatmaps; ranked swap feeds; richlist & large-tx monitors |
| WordPress delivery | le-shop, mexc-live-stats, eth-gas-live, dynex plugin overviews |
| Architecture communication | react-vite-architecture-for-dummies + per-repo ARCHITECTURE.md |
| Learning velocity | Independent stack; continuous expansion from production needs |

---

## How I work

1. **Understand the domain first** — fees, exchange WS formats, nonce rules, WP hook order — before committing to architecture.  
2. **Ship a narrow version** — one pair, one chain, one admin screen — then measure and expand on working code.  
3. **Optimise what data shows is slow** — profilers, structured logs, and metrics from day one; fixes target measured bottlenecks.  
4. **Document from code** — overview repos use what/why/who per feature; no secrets in public repos.  
5. **Operator-first UX** — presets, logs beside controls, stuck-tx tools separated from trade buttons.  

---

## Looking for collaboration

Open to work on:

- real-time dashboards and trading operator tools  
- DeFi / on-chain execution and monitoring  
- WordPress ↔ private backend integration  
- web3 infrastructure and blockchain analytics  
- performance and production hardening on self-hosted Linux  

---

## Experience (honest)

I built and learned this stack independently by shipping systems that run on my own servers and on [logicencoder.com](https://logicencoder.com/) — not tutorial clones.

I do not claim encyclopedic knowledge of every framework. I claim **fast learning**, **readable architecture**, and **systems that stay up under real operator use**.

---

## Availability

Roles aligned with:

- Python / FastAPI backend and async design  
- Realtime data products (WebSocket, aggregation, caching)  
- WordPress ↔ private backend integration  
- Production-minded optimization on dedicated Linux  

**Contact:** [logicencoder.com/contact/](https://logicencoder.com/contact/)  
**GitHub org:** [github.com/logicencoder](https://github.com/logicencoder)
