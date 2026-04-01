# LogicEncoder — Python/FastAPI Realtime Portfolio

This portfolio is a practical map of what I build.
I am self-taught, built these systems from zero, and keep improving by shipping, measuring, and iterating.

Most implementation repositories are private (IP protection), but each major app has a public overview with architecture, feature scope, and screenshots.

## What I Focus On

- Python + FastAPI backends (async-first)
- Realtime systems (WebSocket + REST)
- Data-heavy dashboards and practical analytics (finding useful signals in large streams)
- Performance-minded architecture (aggregation, caching, low-resource operation, non-blocking flows)
- Fast AI-assisted delivery (Windsurf as primary, plus Cursor/Claude-style workflows when useful)

## Core Stack I Use

### Backend
- Python
- FastAPI
- AsyncIO
- Web3 integrations
- API-first service design

### Frontend
- HTML/CSS/JavaScript dashboards
- WordPress-based frontend delivery on selected production setups
- Custom WordPress theme work + plugin development in PHP
- React/Vite on selected projects
- Vue and vanilla JS when they fit the delivery goal

### Data & Database Approach
- SQLite/JSON/in-memory/cache-style storage where it fits product constraints
- Database choice based on workload, latency profile, and deployment limits (not SQL-only)
- Practical analytics pipelines for sorting, filtering, and ranking high-volume event data

### Infrastructure / Ops
- Self-hosted processing with controlled public exposure
- Shared-hosting-aware frontend strategy where needed (low RAM / constrained environment)
- Dockerization when architecture reaches stable deployment stage
- Monitoring/diagnostic dashboards and runtime metrics

## Project Overviews (Public)

### 1) MEXC Trading Dashboard + Multi-Mode Bot

![MEXC Dashboard](https://raw.githubusercontent.com/logicencoder/mexc_trading_app-overview/main/assets/mexc-trading-dashboard-bot-overview.png)

- Overview repo: `https://github.com/logicencoder/mexc_trading_app-overview`
- Private implementation: `logicencoder/mexc_trading_app`
- Delivery mode: standalone local-first application
- Live website mode: not the primary target for this app
- Scope: manual execution + multi-mode automation + realtime orderbook/trades + diagnostics
- Stack used: Python/FastAPI backend, HTML/JS frontend, REST + WebSocket hybrid

### 2) MEXC Exchange — Live Trading Statistics (WordPress + FastAPI)

![MEXC Exchange Live Stats](https://raw.githubusercontent.com/logicencoder/mexc-live-stats-plugin-overview-public/main/screenshot.png)

- Backend overview repo: `https://github.com/logicencoder/mexc-live-stats-backend-overview-public`
- Plugin overview repo: `https://github.com/logicencoder/mexc-live-stats-plugin-overview-public`
- Private implementation repos: `logicencoder/mexc-live-stats-backend-private` + `logicencoder/mexc-live-stats-plugin-private`
- Delivery mode: live web deployment (WordPress frontend + private FastAPI backend)
- Live URL: `https://logicencoder.com/mexc-app/`
- Scope: realtime exchange statistics UI, async ingestion/aggregation backend, snapshot/SEO publishing flow
- Stack used: Python/FastAPI/asyncpg backend + WordPress/PHP plugin frontend + WebSocket/REST + snapshot pipeline

### 3) ETH Gas Tracker

![ETH Gas Tracker](https://raw.githubusercontent.com/logicencoder/eth-gas-tracker-overview/main/assets/eth-gas-tracker-overview.png)

- Standalone overview repo: `https://github.com/logicencoder/eth-gas-tracker-overview`
- Live backend overview repo: `https://github.com/logicencoder/eth-gas-live-backend-overview-public`
- Live plugin overview repo: `https://github.com/logicencoder/eth-gas-live-plugin-overview-public`
- Private implementation repos: `logicencoder/eth_gas_tracker`, `logicencoder/eth-gas-live-backend-private`, `logicencoder/eth-gas-live-plugin-private`
- Delivery mode: local-first runtime + live WordPress deployment
- Live URL: `https://logicencoder.com/ethereum-gas-tracker/`
- Scope: realtime gas intelligence, heatmaps, calculator, alerts, mission-control observability
- Stack used: Python/FastAPI backend, WordPress/PHP plugin frontend, native HTML/JS dashboard, SQLite, WebSocket + REST, Cloudflare Tunnel

### 4) DNX Swap WebApp / Arbitrage Engine

![DNX Swap UI](https://raw.githubusercontent.com/logicencoder/dnx-swap-webapp-overview/main/assets/ui.png)

- Overview repo: `https://github.com/logicencoder/dnx-swap-webapp-overview`
- Private implementation: `logicencoder/dnx-swap-webapp`
- Delivery mode: standalone operator runtime
- Live website mode: not the primary target for this app
- Scope: swap/arbitrage operations with execution controls and safety tooling
- Stack used: Python/FastAPI backend, HTML/JS frontend, chain-aware tx workflow

### 5) ETH Chain Swaps Monitor

![ETH Chain Swaps Monitor](https://raw.githubusercontent.com/logicencoder/eth-chain-swaps-monitor-overview/main/assets/eth-chain-swaps-monitor-overview.png)

- Overview repo: `https://github.com/logicencoder/eth-chain-swaps-monitor-overview`
- Private implementation: `logicencoder/eth_chain_swaps_monitor`
- Delivery mode: standalone local-first monitor
- Live website mode: planned (public link will be added when released)
- Live URL: `Coming soon`
- Scope: swap detection + transaction decoding + alert feed + operator dashboard
- Stack used: Python/FastAPI backend, HTML/JS frontend, WebSocket + REST APIs

## Requirement -> Evidence (Quick HR Match)

| Typical requirement | Evidence in portfolio |
|---|---|
| Python backend development | FastAPI-based backend systems across MEXC, ETH Gas Tracker, DNX Swap, ETH Swaps Monitor |
| Realtime architecture | WebSocket + REST hybrid patterns documented in all overview repos |
| Performance optimization | Low-latency dashboards, caching/aggregation patterns, and low-resource hosting constraints handled in production workflows |
| Data analytics mindset | Gas heatmaps, trend analysis, ranked event feeds, and signal-focused dashboard design |
| Practical frontend delivery | HTML/CSS/JS operator UIs + live WordPress frontend deployments + custom PHP plugins/themes |
| Architecture communication | `https://github.com/logicencoder/react-vite-architecture-for-dummies` + structured architecture sections in overviews |
| Tooling flexibility | Windsurf-primary workflow with Cursor/Claude support when it improves delivery speed/quality |
| Learning velocity | Built stack independently from zero and continuously expand tools based on project requirements |

## Supporting Public Repositories

- `https://github.com/logicencoder/react-vite-architecture-for-dummies` (my architecture documentation template/style for readable handoff)
- `https://github.com/logicencoder/hardware-monitor` (runtime observability tooling)
- `https://github.com/logicencoder/dynex-0xdnx-dhip-richlist-monitor` (blockchain analytics dashboard)

## How I Work

- Start with deep requirement/domain research before implementation
- Build from concrete problem to working version quickly
- Keep architecture readable so another developer can follow it
- Optimize continuously for speed, low resource usage, and non-blocking behavior
- Use prompt-engineering playbooks and AI workflows to accelerate repetitive/problem-structuring tasks
- Learn missing tools fast when needed
- Prefer honest capability statements over inflated claims

## Experience Statement (Honest)

I built and learned this stack independently from zero by shipping real projects.
I do not claim to know everything; I focus on learning fast, solving practical problems, and delivering systems that work.

## Availability

Open to roles focused on Python/FastAPI backend, realtime systems, practical analytics delivery, and production-minded optimization.

Contact: `https://logicencoder.com/contact/`
