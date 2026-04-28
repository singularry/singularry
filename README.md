# Singularry

An AI-powered DeFi platform with autonomous trading agents, modular smart contract wallets, proprietary machine learning models, and natural language interaction — built on BNB Smart Chain and compatible with EVM networks.

---

## Technology Stack

| Layer | Technology |
|-------|------------|
| **Blockchain** | BNB Smart Chain + EVM-compatible chains |
| **Smart Contracts** | Solidity ^0.8.x, EIP-2535 Diamond Standard |
| **Frontend** | Next.js 15, React 19, TypeScript, Tailwind CSS |
| **Web3** | ethers.js v6, wagmi, viem, Privy authentication |
| **AI / ML** | Multi-model LLM orchestration, ONNX model serving, reinforcement learning |
| **Agent Runtime** | Node.js, TypeScript, autonomous 24/7 operation |
| **ML Platform** | Python, FastAPI, GPU-accelerated training pipeline |
| **Data** | PostgreSQL + pgvector, TimescaleDB (time-series), Redis |
| **Infrastructure** | Vercel, Railway, Neon PostgreSQL |

---

## Supported Networks

| Network | Chain ID | Status |
|---------|----------|--------|
| BNB Smart Chain Mainnet | 56 | **Primary** |
| BNB Smart Chain Testnet | 97 | Testing |
| HyperEVM | 999 | Supported |
| Ethereum Mainnet | 1 | Supported |
| Polygon | 137 | Supported |
| Arbitrum | 42161 | Supported |
| Optimism | 10 | Supported |
| Base | 8453 | Supported |

---

## Autonomous AI Agent

Singularry's core differentiator is a **24/7 autonomous agent runtime** — a self-operating trading and portfolio management system that continuously monitors markets, evaluates opportunities, and executes strategies without human intervention.

### Architecture

```
┌──────────────────────────────────────────────────────────────────────┐
│                     Frontend (Next.js)                                │
│   AI Chat  │  Dashboard  │  Strategies  │  Portfolio  │  Admin       │
└──────────────────────────────────────────────────────────────────────┘
                               │
                               ▼
┌──────────────────────────────────────────────────────────────────────┐
│                     Agent Runtime (Node.js)                           │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│   ┌────────────┐   ┌────────────┐   ┌─────────────┐                 │
│   │   Brain     │   │  Scheduler │   │   Memory    │                 │
│   │  (ReAct +  │   │  (Lane-    │   │ (3-Tier     │                 │
│   │  Workflows)│   │   Based)   │   │  Adaptive)  │                 │
│   └─────┬──────┘   └─────┬──────┘   └──────┬──────┘                 │
│         │                 │                 │                         │
│   ┌─────▼─────────────────▼─────────────────▼──────┐                 │
│   │              Tool Registry (140+ tools)         │                 │
│   │   Wallet │ CEX │ DEX │ Market │ Portfolio │ ML  │                 │
│   └─────────────────────┬───────────────────────────┘                 │
│                         │                                            │
│   ┌─────────────────────▼───────────────────────────┐                 │
│   │          Execution Engine (DEX + CEX)            │                 │
│   └─────────────────────────────────────────────────┘                 │
│                                                                      │
├──────────────────────────────────────────────────────────────────────┤
│   Security: Capability Bitmap │ Simulation │ HITL Approvals          │
└──────────────────────────────────────────────────────────────────────┘
         │                                          │
         ▼                                          ▼
┌──────────────────┐                    ┌──────────────────────────┐
│  ML Platform     │                    │  SLY Wallet (Diamond)    │
│  (Python)        │                    │  ┌──────┐ ┌──────┐      │
│                  │                    │  │Venus │ │ DCA  │ ...  │
│  RL Ensemble     │                    │  │Facet │ │Facet │      │
│  Regime Classif. │                    │  └──────┘ └──────┘      │
│  Vol Forecaster  │                    └──────────────────────────┘
│  Drift Monitor   │                                │
└──────────────────┘                                ▼
                                        ┌──────────────────────────┐
                                        │     DeFi Protocols       │
                                        │ Venus │ Thena │ Lista    │
                                        │ Pendle│ LiFi  │ Binance  │
                                        └──────────────────────────┘
```

### Brain & Decision Engine

The agent's **Brain** is a reasoning engine that plans and executes multi-step DeFi operations:

- **ReAct Loop** — iterative reason-act-observe cycle for tool-augmented decision-making
- **Workflow Engine** — orchestrates complex multi-step operations (rebalancing, yield migration, cross-chain bridging) with checkpointing and crash recovery
- **Intelligent Model Routing** — automatically selects the optimal LLM based on task complexity and criticality, routing routine tasks to faster models and financial decisions to the most capable
- **Human-in-the-Loop (HITL)** — high-value or risky operations are paused for user approval before execution, with configurable thresholds

### Proprietary ML Models

Singularry runs a dedicated **machine learning platform** with proprietary models trained on GPU infrastructure:

| Model | Purpose |
|-------|---------|
| **RL Ensemble** | Multi-agent reinforcement learning system for adaptive strategy selection and position sizing |
| **Regime Classifier** | Identifies current market regime (trending, mean-reverting, volatile) to dynamically adjust strategy parameters |
| **Volatility Forecaster** | Predicts near-term volatility for dynamic risk calibration and position sizing |
| **Dynamic Clustering** | Groups assets by behavioral similarity for portfolio construction and diversification |

- Models are trained on GPU and exported to **ONNX** for efficient production inference
- **Drift monitoring** continuously tracks prediction accuracy and feature distribution shifts, triggering model reloads when performance degrades
- Models hot-reload in production without service downtime

### Three-Tier Memory System

The agent maintains persistent memory across sessions using **vector embeddings** for intelligent retrieval:

- **Semantic Memory** — user preferences, facts, and learned context (risk tolerance, preferred protocols, etc.)
- **Episodic Memory** — trade history, market events, and outcomes for experience-driven decision-making
- **Procedural Memory** — strategy performance scores continuously updated via reinforcement learning, enabling the agent to learn which strategies work best under which market conditions

Retrieval uses **hybrid search** combining dense vector similarity with keyword matching for high-recall context injection.

### Multi-Tier Strategy Portfolio

The agent manages strategies spanning conservative to aggressive risk profiles:

| Tier | Risk Level | Strategy Types |
|------|-----------|---------------|
| **Tier 1** | Conservative | Dollar-cost averaging, market-cap index tracking |
| **Tier 2** | Moderate | Risk-parity allocation, AI-driven portfolio optimization, grid trading |
| **Tier 3** | Active | Momentum trading, funding rate arbitrage, basis trading |
| **Tier 4** | Advanced | Yield optimization, concentrated liquidity management, delta-neutral strategies |
| **Tier 5** | Aggressive | Cross-venue arbitrage, prediction markets, multi-leg strategies |

Each strategy follows a full lifecycle: **evaluate** (market conditions) → **execute** (position entry) → **monitor** (ongoing management) → **exit** (position close).

### Execution Engine

Unified execution layer supporting both centralized and decentralized exchanges:

- **DEX Execution** — on-chain swaps via aggregator routing through the Diamond wallet
- **CEX Execution** — order management on centralized exchanges with TWAP and limit order support
- **Transaction Simulation** — high-value trades are simulated before execution to prevent costly errors

### Data Pipeline

Automated data collection powering the ML models and trading decisions:

- **Market data** — OHLCV candles, order book snapshots, funding rates
- **Macro indicators** — economic data (rates, inflation, volatility indices)
- **On-chain metrics** — TVL, whale movements, protocol health indicators
- **Sentiment analysis** — aggregated market sentiment scoring
- **Time-series storage** — hypertable-optimized for fast range queries and analysis

---

## SLY Wallets (Smart Contract Wallets)

Modular smart contract wallets using the **EIP-2535 Diamond Standard**:

- **Upgradeable Architecture** — add, replace, or remove strategy modules without migrating assets
- **Facet-Based Design** — each DeFi strategy is a separate on-chain module
- **Capability Bitmap** — on-chain access control encoded as a `uint256` bitmap for O(1) permission checks
- **Gasless Transactions** — meta-transaction support via relayer infrastructure
- **Delegation & Co-Signing** — multi-party wallet management via Privy TEE signing
- **Unified Asset Management** — single wallet address for all DeFi operations across protocols

```
User calls wallet.supplyToVenus(100 USDT)
  → Diamond looks up selector
  → Routes to Venus Facet
  → Facet executes using wallet's storage
```

---

## AI Chat Interface

Natural language DeFi interaction:

- **Intent Understanding** — swap, bridge, lend, borrow, stake, and complex multi-step requests
- **Multi-Chain Operations** — execute transactions across supported networks via conversation
- **Portfolio Analysis** — AI-driven insights, risk assessment, and strategy recommendations
- **Expert Mode** — auto-execute transactions for experienced users
- **Real-Time Data** — live market data, on-chain analytics, and web search integration

---

## Automated Strategies

### On-Chain Strategy Facets

| Strategy | Description | Key Features |
|----------|-------------|--------------|
| **DCA** | Periodic token purchases | TWAP oracle, slippage protection, configurable intervals |
| **DRIP** | Buy-the-dip / sell-the-rip | EMA-based triggers, customizable deviation thresholds |
| **VTYO** | Venus-Thena yield optimization | Leveraged yield farming, auto-compounding, health monitoring |
| **Yield Loop** | Leveraged yield strategies | Pendle PT support, sUSDe integration, auto-deleveraging |
| **Lista** | CDP management | BNB/stablecoin looping, liquidation alerts, automated unwinding |
| **VLP** | Venus liquidation protection | Health monitoring, auto-repay triggers |

### Agent-Managed Strategies

Additional strategies managed by the autonomous agent runtime:

- Hierarchical risk parity portfolio allocation
- AI-optimized portfolio rebalancing
- Grid trading with adaptive grid spacing
- Funding rate arbitrage (CEX ↔ DEX)
- Basis trading (spot vs. perpetual)
- Cross-venue arbitrage
- Concentrated liquidity delta-neutral positions
- Passive yield vaults (ERC-4626)

---

## Protocol Integrations

| Protocol | Integration |
|----------|------------|
| **Venus Protocol** | Lending, borrowing, liquidation protection |
| **Thena** | V3 concentrated liquidity, yield farming |
| **Lista DAO** | CDP management, lisUSD minting |
| **Pendle** | Principal token strategies |
| **Aster DEX** | Perpetual futures trading |
| **Binance** | Spot + futures trading, market data |
| **LiFi** | Cross-chain swaps and bridging |
| **Enso** | DeFi aggregation and routing |
| **Altura Vault** | ERC-4626 yield vaults (HyperEVM) |

---

## Non-Fungible Agents (NFA)

On-chain AI agent identity and ownership:

- **BAP578 Standard** — tokenized agent ownership as NFTs
- **On-Chain Learning** — strategy evolution recorded on-chain
- **Capability System** — bitmap-encoded permissions control agent actions
- **Automated Execution** — DeFi operations with verifiable on-chain provenance

---

## Security

| Audit Firm | Report |
|------------|--------|
| **Fairyproof** | [View Audit](https://www.fairyproof.com/report/Singularry) |

### Security Practices

- All strategy facets audited before mainnet deployment
- **Transaction simulation** — high-value trades simulated before execution; simulation failure blocks the trade
- **Human-in-the-Loop approvals** — dangerous operations require explicit user confirmation
- **Capability-gated tools** — on-chain bitmap controls agent access per wallet
- **Encrypted credential storage** — AES-256-GCM encryption for all stored keys
- **Daily loss circuit breakers** — per-strategy and per-user spending limits
- Timelocked administrative functions
- Emergency pause capability
- Real-time position health monitoring with proactive alerts

---

## Contract Addresses

### BSC Mainnet - Core Infrastructure

| Contract | Address | Version |
|----------|---------|---------|
| **Factory** | `0x50C1B075E312530d970b40D205B6eF1313740Fb0` | 2.1.0 |
| **Diamond Cut** | `0x9755236Ce347d5E75964a1f6BA0BDdBA037aC85b` | 1.0.0 |
| **Diamond Loupe** | `0x75aD4055787F96E49905fF8adfcC209E773f5dfE` | 1.0.0 |
| **Base Facet** | `0x4A95942DC5DA9867aCdB54a2c5D4a10bA48c6F2f` | 1.0.0 |
| **Address Management** | `0xc92a6883146c5B69cd0F43dA9E59DD43C75a6976` | 1.0.0 |
| **Fee Management** | `0x98B935e9918558C304abA28eb419943F7e6aBEAc` | 1.0.0 |

### BSC Mainnet - DeFi Strategy Facets

| Contract | Address | Version |
|----------|---------|---------|
| **Venus** | `0x3AE2ebF18BF77dAA92dBF3F46d5EF990BD67400E` | 1.0.0 |
| **DCA** | `0xcA7323b8e7e3608Bf331EC680c1f931FE89Fa519` | 2.0.1 |
| **DRIP** | `0x47d745a039843499F34CDB0984A3C141349ff9a7` | 2.1.0 |
| **VLP** | `0x8b8EE7Cd9902dEB4BC2f0a89Fd56E00DFE6270a7` | 1.0.0 |
| **USDD Vault** | `0x43cC9cbb349477F10502879Eac96840b9e9B6A24` | 1.1.0 |

### BSC Mainnet - VTYO (Venus Thena Yield Optimizer)

| Contract | Address | Version |
|----------|---------|---------|
| **VTYO Management** | `0x26CbFD1ba3d35783EBF96AeFe1Eda0e3aF6D5025` | 1.1.0 |
| **VTYO Execution** | `0x5c1747111e8bae209A9f4416a1325809b227a60a` | 1.1.0 |
| **VTYO Harvest** | `0x56B09056Bb52327c2eaEB119e2D62f4D57B930ED` | 1.1.0 |

### BSC Mainnet - Yield Loop

| Contract | Address | Version |
|----------|---------|---------|
| **YL Management** | `0x23dEEE66585C34578078531d4eBdB9571794c132` | 1.3.0 |
| **YL Execution** | `0x5c0b461c3C3Cff267307446e07e6fB524fBF83D6` | 1.3.0 |
| **YL Monitoring** | `0x06D6a568b902e152db657f54cFEa2Fcc808eDf53` | 1.2.0 |

### BSC Mainnet - Lista DAO Integration

| Contract | Address | Version |
|----------|---------|---------|
| **Lista Management** | `0x58E115fCBf83C4A670c347923027B16bCc91e0d7` | 2.0.0 |
| **Lista BNB Looping** | `0x475Eec27Cd0d38D517dD1F038EF4a473b8037Cf1` | 2.0.0 |
| **Lista Stable Looping** | `0x52FaBF24fd61a9B939C8c584A6667122c7E4A2ab` | 2.0.0 |
| **Lista Direct** | `0x213A8dDea6b6362cfdfEE8e72A864780fa7781EE` | 2.0.0 |
| **Lista Unwind** | `0x6325b899C45Aa8CF7881C88Ef1985edC45F413FC` | 2.0.0 |
| **Lista Monitoring** | `0x7305eB2A83eD9BBD7cd2F4e5c64B5339E070cE80` | 2.0.0 |

### BSC Mainnet - AI Agent

| Contract | Address | Version |
|----------|---------|---------|
| **Agent Facet** | `0x5b4857d0cB9b9147CE7D78412361B8188252b455` | 1.0.0 |
| **NFA (Non-Fungible Agent)** | `0x039D7d0096d2989647133f9676f2b341e602d2fF` | 1.0.0 |
| **Learning Module** | `0xcE27D129a79a62652261e203f7c1074782045949` | 1.0.0 |

---

## Notifications

Multi-channel alerting:

- **Telegram** — real-time trade alerts, strategy updates, risk warnings
- **Discord** — community and team notifications
- **Email** — daily summaries and critical alerts
- **WebSocket** — live streaming to the frontend dashboard

---

## Why Is Our GitHub Private?

You may notice limited public activity across our repositories — this is intentional.

Singularry is in an **advanced build phase**, developing proprietary AI-driven DeFi infrastructure including autonomous agents, smart wallet execution layers, and cross-protocol integrations.

To protect our intellectual property and prevent premature forking or cloning, our core codebase is kept private until full Go-To-Market (GTM).

### Security & Responsibility First

We build systems that interact directly with user funds and on-chain execution. Our priorities:

- Rigorous internal testing and validation
- Third-party security audits with industry-leading firms
- Controlled release cycles aligned with product readiness

### What to Expect

- Public audit reports prior to or during launch
- Gradual open-sourcing of selected components post-GTM
- Full product rollout with verifiable on-chain activity

### Build > Hype

We believe in shipping real, secure, and scalable products — not optimizing for GitHub optics during development.

If you're here early, you're seeing us before the switch flips. Stay tuned.

---

## Related Documentation

- [Smart Contract Registry](./SMART_CONTRACTS.md) — full contract address list
- [Facet Integration Guide](https://github.com/singularry/sly-community-facets) — developer guide for new facets
- [Security Audits](https://www.fairyproof.com/report/Singularry) — audit reports

---

## Links

| Resource | URL |
|----------|-----|
| **Website** | [singularry.com](https://singularry.com) |
| **GitHub** | [github.com/singularry](https://github.com/singularry) |
| **Twitter** | [@singularry](https://twitter.com/singularry) |
| **Discord** | [Join Discord](https://discord.gg/singularry) |

---

*Last updated: 2026-04-28*
