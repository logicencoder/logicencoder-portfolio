# LogicEncoder Portfolio

This repository is the **public index** of what I build: trading dashboards, chain monitors, WordPress–backend bridges, and operator tooling. It is meant for recruiters, collaborators, and technical reviewers who want substance—not a list of buzzwords.

I am self-taught, shipped these systems from zero, and keep improving by measuring production behaviour (SOL server, Hostinger WordPress, controlled tunnels) rather than demo-only deployments.

Each product typically uses a **private code repo** (`{app}` or `{name}-plugin`) plus a **public overview repo** (`{app}-overview` or `{name}-plugin-overview`) for screenshots, scope, and what/why/who documentation. Implementation depth lives in private `README.md` + `ARCHITECTURE.md` where applicable.

**Contact:** [logicencoder.com/contact/](https://logicencoder.com/contact/)

---

## What I focus on

| Area | What that means in practice |
|------|----------------------------|
| **Python + FastAPI** | Async-first APIs, background tasks, WebSocket fan-out, structured logging |
| **Realtime systems** | Hybrid REST + WebSocket: snapshots for first paint, streams for deltas |
| **Data-heavy dashboards** | Ranked feeds, heatmaps, aggregation under load—not vanity charts |
| **Low-resource operation** | Caching, prebuilt templates, RAM mirrors of chain head, minimal RPC chatter |
| **WordPress as catalogue** | PHP plugins for editorial truth; Node/Python on SOL for money-moving logic |
| **Honest delivery modes** | I state whether something is live on the web, standalone local, or SOL-only |

---

## Core stack

### Backend

- Python 3, FastAPI, asyncio orchestration  
- Web3.py-style on-chain execution (swaps, transfers, nonce lifecycle)  
- Node/Fastify for selected store backends (`le-crypto-app-store`)  
- DuckDB / SQLite / JSON caches where latency and hosting cost dictate storage  

### Frontend

- Operator HTML/CSS/JS dashboards (single-page, preset-driven)  
- WordPress plugins (PHP) + custom theme work where the public site is WP  
- React/Vite on selected learning and architecture documentation repos  

### Infrastructure / ops

- **SOL** (`/home/sol/lojzo`) — production runtime for bots, gas SSR, MEXC apps, DNX swap, USM  
- **Hostinger** — WordPress plugins (shop catalogue, settings, live stats embeds)  
- **WSL** — development and diff against prod; not treated as production truth  
- **Cloudflare tunnels** — controlled exposure of private backends to WP frontends  
- **Observability** — [hardware-monitor](https://github.com/logicencoder/hardware-monitor), [system-monitor-app](https://github.com/logicencoder/system-monitor-app)  

---

## Repository pattern (how to read my GitHub)

| Type | GitHub name | Visibility | Docs |
|------|-------------|------------|------|
| Application code | `{app}` | Private | README + ARCHITECTURE + REPOS |
| Marketing / scope | `{app}-overview` | Public | Useful-content README (what/why/who) |
| WordPress plugin code | `{name}-plugin` | Private | Same as application |
| WP plugin marketing | `{name}-plugin-overview` | Public | Same as overview |

I do **not** use `-private`, `-public`, or combined plugin repos. **le-shop-plugin** and **le-settings-plugin** are different products.

---

## Featured projects (public overviews)

### 1) MEXC Trading Dashboard + multi-mode automation

![MEXC Dashboard](https://raw.githubusercontent.com/logicencoder/mexc_trading_app-overview/main/assets/mexc-trading-dashboard-bot-overview.png)

| | |
|---|---|
| **Overview** | [mexc_trading_app-overview](https://github.com/logicencoder/mexc_trading_app-overview) |
| **Code** | `logicencoder/mexc_trading_app` (private) |
| **Delivery** | Standalone local-first operator runtime |
| **What** | Manual trading UI, multi-mode bots, live orderbook/trades, diagnostics |
| **Why** | Exchange web UI was too slow for the execution style I needed |
| **Who** | Operator running MEXC strategies on own hardware |

**Stack:** Python/FastAPI, HTML/JS, REST + WebSocket.

---

### 2) MEXC Exchange — live trading statistics (WordPress + FastAPI)

![MEXC Exchange Live Stats](https://raw.githubusercontent.com/logicencoder/mexc-live-stats-plugin-overview/main/screenshot.png)

| | |
|---|---|
| **Backend overview** | [mexc-live-stats-backend-overview](https://github.com/logicencoder/mexc-live-stats-backend-overview) |
| **Plugin overview** | [mexc-live-stats-plugin-overview](https://github.com/logicencoder/mexc-live-stats-plugin-overview) |
| **Code** | `mexc-live-stats-backend` + `mexc-live-stats-plugin` (private) |
| **Live** | [logicencoder.com/mexc-app/](https://logicencoder.com/mexc-app/) |
| **What** | Public stats UI fed by async ingestion; snapshot/SEO publishing |
| **Why** | Visitors need exchange context without hitting rate-limited APIs from the browser |
| **Who** | Site visitors (read); operator (deploy); backend (aggregate) |

**Stack:** FastAPI/asyncpg, WordPress/PHP plugin, WebSocket + REST, tunnel to SOL.

---

### 3) ETH Gas Tracker (live + local runtime)

![ETH Gas Tracker](https://raw.githubusercontent.com/logicencoder/eth-gas-live-backend-overview/main/assets/eth-gas-tracker-overview.png)

| | |
|---|---|
| **Product overview** | [eth-gas-live-backend-overview](https://github.com/logicencoder/eth-gas-live-backend-overview) |
| **Plugin overview** | [eth-gas-live-plugin-overview](https://github.com/logicencoder/eth-gas-live-plugin-overview) |
| **Code** | `eth-gas-live-backend`, `eth-gas-live-plugin` (private) |
| **Live** | [logicencoder.com/ethereum-gas-tracker/](https://logicencoder.com/ethereum-gas-tracker/) |
| **What** | Realtime gas intelligence, heatmaps, calculator, alerts, mission-control metrics |
| **Why** | Gas decisions need continuous signal, not a static “low/medium/high” widget |
| **Who** | Ethereum users planning txs; operator monitoring SSR health |

**Stack:** Python/FastAPI, WP plugin, SQLite, WebSocket, Cloudflare tunnel, SSR helper on SOL.

---

### 4) DNX Swap WebApp / operator execution engine

![DNX Swap UI](https://raw.githubusercontent.com/logicencoder/dnx-swap-webapp-overview/main/assets/ui.png)

| | |
|---|---|
| **Overview** | [dnx-swap-webapp-overview](https://github.com/logicencoder/dnx-swap-webapp-overview) |
| **Code** | `dnx-swap-webapp` (private) |
| **Delivery** | Standalone operator runtime (production on SOL) |
| **What** | DNX⇄USDC presets, config gas, MEV builders, recovery tooling |
| **Why** | Generic DEX UX was too laggy; needed mempool-aware operator controls |
| **Who** | Operator trading Dynex ecosystem size ladders |

**Stack:** Python/FastAPI, async Web3, MEXC price WS + on-chain pools.

---

### 5) ETH Chain Swaps Monitor

![ETH Chain Swaps Monitor](https://raw.githubusercontent.com/logicencoder/eth-chain-swaps-monitor-overview/main/assets/eth-chain-swaps-monitor-overview.png)

| | |
|---|---|
| **Overview** | [eth-chain-swaps-monitor-overview](https://github.com/logicencoder/eth-chain-swaps-monitor-overview) |
| **Code** | `eth_chain_swaps_monitor` |
| **Delivery** | Local-first monitor; public site planned |
| **What** | Swap detection, tx decoding, alert feed, operator dashboard |
| **Why** | Watching chain activity required unified decode + alert stream, not block explorers alone |
| **Who** | Operator monitoring Ethereum swap flow |

**Stack:** Python/FastAPI, HTML/JS, WebSocket + REST.

---

### 6) LogicEncoder Shop (WordPress catalogue + Telegram store backend)

| | |
|---|---|
| **Plugin overview** | [le-shop-plugin-overview](https://github.com/logicencoder/le-shop-plugin-overview) |
| **Store backend** | `le-crypto-app-store` (private) + public overview sibling |
| **What** | WP `application` posts as catalogue; webhook sync to Node store on SOL |
| **Why** | Editors use wp-admin; buyers pay in Telegram—two surfaces, one product truth |
| **Who** | Operator publishing apps; buyers in Mini App; backend matching USDC/ETH |

**Not the same as** [le-settings-plugin-overview](https://github.com/logicencoder/le-settings-plugin-overview) (SEO, security, brute-force—site hygiene).

---

### 7) Dynex 0xDNX / DHIP richlist monitor

| | |
|---|---|
| **Repo** | [dynex-0xdnx-dhip-richlist-monitor](https://github.com/logicencoder/dynex-0xdnx-dhip-richlist-monitor) |
| **What** | Blockchain analytics dashboard for Dynex richlist / holder views |
| **Why** | Community and operator visibility into concentration and movement |
| **Who** | Analysts and ecosystem participants |

---

### 8) Universal Service Manager (USM)

| | |
|---|---|
| **Overview** | `universal-service-manager-overview` (public) |
| **Code** | `universal-service-manager` (private) |
| **What** | Dashboard to supervise many SOL processes from one place |
| **Why** | Dozens of Python bots need start/stop/health without ad-hoc SSH scripts |
| **Who** | Operator maintaining production on SOL |

---

## Supporting public repositories

| Repo | Purpose |
|------|---------|
| [react-vite-architecture-for-dummies](https://github.com/logicencoder/react-vite-architecture-for-dummies) | How I document architecture for handoff (readable diagrams + narrative) |
| [hardware-monitor](https://github.com/logicencoder/hardware-monitor) | Browser dashboard fed by WebSocket hardware metrics |
| [system-monitor-app](https://github.com/logicencoder/system-monitor-app) | All-in-one Linux TUI for CPU/RAM/disk/net/GPU/sensors |
| [logicencoder-portfolio](https://github.com/logicencoder/logicencoder-portfolio) | This index |

---

## Requirement → evidence (quick match)

| Typical requirement | Where to look |
|---------------------|---------------|
| Python backend | FastAPI repos above; private ARCHITECTURE files |
| Realtime architecture | WebSocket + REST patterns in gas, MEXC, DNX, ETH swaps overviews |
| Performance / low RPC | DNX swap docs (base fee cache, balance RAM); gas SSR design |
| Analytics mindset | Gas heatmaps; ranked swap feeds; richlist monitor |
| WordPress delivery | le-shop-plugin-overview, mexc-live-stats-plugin-overview, eth-gas-live-plugin-overview |
| Architecture communication | react-vite-architecture-for-dummies + per-repo ARCHITECTURE.md |
| Production discipline | INVENTORY in [githelper](https://github.com/logicencoder/githelper) (agent ops repo)—SOL vs WSL vs GitHub truth |

---

## How I work

1. **Research the domain** before coding (fees, nonce rules, exchange WS formats, WP hooks).  
2. **Ship a working narrow version** (one pair, one chain, one admin screen).  
3. **Document from code**, not from chat memory—overview repos use what/why/who per feature.  
4. **Optimize for operator time**: presets, logs beside buttons, stuck-tx tools separated from trade buttons.  
5. **Keep secrets out of public repos**—overviews describe behaviour, not keys or tunnels.  
6. **Learn tools quickly** when the problem demands it (protobuf decode, builder APIs, asyncpg).  

---

## Experience statement (honest)

I built and learned this stack independently by shipping real projects that run on my own servers and on LogicEncoder.com—not tutorial clones.

I do not claim encyclopedic knowledge of every framework. I claim **fast learning**, **readable architecture**, and **systems that stay up under real operator use**.

---

## Availability

Open to roles focused on:

- Python / FastAPI backend and async design  
- Realtime data products (WebSocket, aggregation, caching)  
- WordPress ↔ private backend integration  
- Production-minded optimization on self-hosted Linux  

**Contact:** [logicencoder.com/contact/](https://logicencoder.com/contact/)  
**GitHub org:** [github.com/logicencoder](https://github.com/logicencoder)
