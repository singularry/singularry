# Singularry

An AI-powered DeFi platform with modular smart contract wallets, automated trading strategies, and natural language interaction built on BNB Smart Chain (BSC) and compatible with other EVM networks.

---

## Technology Stack

| Layer | Technology |
|-------|------------|
| **Blockchain** | BNB Smart Chain + EVM-compatible chains |
| **Smart Contracts** | Solidity ^0.8.x, EIP-2535 Diamond Standard |
| **Frontend** | Next.js 15, React 19, TypeScript, Tailwind CSS |
| **Web3** | ethers.js v6, wagmi, viem, Privy authentication |
| **AI** | Vercel AI SDK, Claude/GPT models, tool-use architecture |
| **Development** | Hardhat, OpenZeppelin libraries, Drizzle ORM |
| **Infrastructure** | Vercel, Neon PostgreSQL, BSCScan API |

---

## Supported Networks

| Network | Chain ID | Status |
|---------|----------|--------|
| BNB Smart Chain Mainnet | 56 | **Primary** |
| BNB Smart Chain Testnet | 97 | Testing |
| Ethereum Mainnet | 1 | Supported |
| Polygon | 137 | Supported |
| Arbitrum | 42161 | Supported |
| Optimism | 10 | Supported |
| Base | 8453 | Supported |

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

## Features

### 1. SLY Wallets (Smart Contract Wallets)

Modular smart contract wallets using the **EIP-2535 Diamond Standard**, enabling:

- **Upgradeable Architecture**: Add, replace, or remove functionality without migrating assets
- **Facet-Based Design**: Each DeFi strategy is a separate facet that can be attached/detached
- **Gasless Transactions**: Meta-transactions supported via relayer infrastructure
- **Multi-Signature Support**: Co-owner capabilities via Privy integration
- **Unified Asset Management**: Single wallet for all DeFi operations

### 2. AI-Powered Chat Interface

Natural language DeFi interaction powered by Claude and GPT models:

- **Intent Classification**: AI understands swap, bridge, lend, borrow, stake requests
- **Multi-Chain Operations**: Execute transactions across supported networks
- **Portfolio Analysis**: AI-driven insights and recommendations
- **Web Search Integration**: Real-time market data and research
- **Expert Mode**: Auto-execute transactions for experienced users

### 3. Automated Trading Strategies (Playbooks)

#### DCA (Dollar Cost Averaging)
- Automated periodic token purchases
- TWAP oracle integration for fair pricing
- Configurable intervals and amounts
- Slippage protection

#### DRIP (Buy-the-Dip / Sell-the-Rip)
- Automated buy orders when price drops below threshold
- Automated sell orders when price rises above threshold
- EMA-based trigger calculations
- Customizable deviation percentages

#### VTYO (Venus Thena Yield Optimizer)
- Leveraged yield farming on Thena V3 pools
- Automated LP position management
- Yield harvesting and auto-compounding
- Health factor monitoring

#### Yield Loop
- Leveraged yield farming strategies
- Pendle PT (Principal Token) support
- sUSDe integration on BSC
- Position health monitoring and liquidation alerts

#### Lista DAO Integration
- CDP (Collateralized Debt Position) management
- BNB and stablecoin looping strategies
- Position unwinding and deleveraging
- Real-time health monitoring

### 4. Protocol Integrations

| Protocol | Integration Type |
|----------|-----------------|
| **Venus Protocol** | Lending, borrowing, liquidation protection |
| **Thena** | V3 concentrated liquidity, yield farming |
| **Lista DAO** | CDP management, lisUSD minting |
| **Pendle** | Principal token strategies |
| **LiFi** | Cross-chain swaps and bridging |
| **0x Protocol** | DEX aggregation for optimal swap rates |
| **Expand Network** | Multi-chain bridge integration |

### 5. Security Features

- **Smart Contract Audits**: Audited by Fairyproof
- **Timelocks**: Administrative actions require waiting periods
- **Pause Control**: Emergency pause functionality
- **Health Monitoring**: Real-time position health tracking
- **Liquidation Alerts**: Proactive warnings before liquidation

### 6. Gas Optimization

- **Multicall Batching**: Batch multiple calls into single transactions
- **Gas-Efficient Design**: Optimized for BNB Smart Chain low fees
- **Provider Pooling**: Singleton RPC connections to reduce overhead

---

## Architecture Overview

```
┌─────────────────────────────────────────────────────────────┐
│                    Frontend (Next.js)                        │
├─────────────────────────────────────────────────────────────┤
│  AI Chat Interface  │  Dashboard  │  Playbooks  │  Admin    │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                    AI Tool System                            │
├─────────────────────────────────────────────────────────────┤
│  classifyIntentV2  │  executeMultiStep  │  analyzeCrypto    │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                 SLY Wallet (Diamond Proxy)                   │
├─────────────────────────────────────────────────────────────┤
│  ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐           │
│  │  Venus  │ │   DCA   │ │  DRIP   │ │  VTYO   │  ...      │
│  │  Facet  │ │  Facet  │ │  Facet  │ │  Facets │           │
│  └─────────┘ └─────────┘ └─────────┘ └─────────┘           │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                    DeFi Protocols                            │
├─────────────────────────────────────────────────────────────┤
│  Venus  │  Thena  │  Lista  │  Pendle  │  LiFi  │  0x      │
└─────────────────────────────────────────────────────────────┘
```

---

## Diamond Standard (EIP-2535)

Each SLY wallet is a Diamond proxy that routes function calls to facet contracts:

```
User calls wallet.supplyToVenus(100 USDT)
  → Diamond looks up selector 0x12345678
  → Routes to Venus Facet at 0x3AE2...
  → Facet executes using wallet's storage
```

### Key Operations

| Operation | Action | Use Case |
|-----------|--------|----------|
| **Add** | Register new selectors | Fresh facet attachment |
| **Replace** | Point selectors to new address | Facet upgrade |
| **Remove** | Delete selectors | Cleanup old functions |

---

## Playbook System

Playbooks are automated DeFi strategies that execute predefined operations:

| Playbook | Description | Key Features |
|----------|-------------|--------------|
| **DCA** | Periodic token purchases | TWAP oracle, slippage protection |
| **DRIP** | Buy-dip / sell-rip automation | EMA triggers, customizable thresholds |
| **VTYO** | Thena V3 yield optimization | Auto-compound, health monitoring |
| **Yield Loop** | Leveraged yield farming | Pendle PT support, sUSDe integration |
| **Lista** | CDP management | Looping strategies, liquidation alerts |
| **VLP** | Venus liquidation protection | Health monitoring, auto-repay |

---

## AI Agent System

### Non-Fungible Agents (NFA)

On-chain AI agents with:
- **BAP578 Standard**: Tokenized agent ownership
- **Learning Modules**: On-chain strategy evolution
- **Task Execution**: Automated DeFi operations

### Agent Capabilities

- Execute trades based on market conditions
- Manage portfolio allocations
- Monitor position health
- Harvest yields automatically

---

## Security & Audits

| Audit Firm | Report |
|------------|--------|
| **Fairyproof** | [View Audit](https://www.fairyproof.com/report/Singularry) |

### Security Practices

- All strategy facets audited before deployment
- Timelock on administrative functions
- Emergency pause capability
- Health factor monitoring with alerts
- Gradual rollouts with testnet validation

---

## Related Documentation

- [Smart Contract Registry](./SMART_CONTRACTS.md) - Full contract address list
- [Facet Integration Guide](https://github.com/singularry/sly-community-facets) - Developer guide for new facets
- [Security Audits](https://www.fairyproof.com/report/Singularry) - Audit reports

---

## Links

| Resource | URL |
|----------|-----|
| **Website** | [singularry.com](https://singularry.com) |
| **GitHub** | [github.com/singularry](https://github.com/singularry) |
| **Twitter** | [@singularry](https://twitter.com/singularry) |
| **Discord** | [Join Discord](https://discord.gg/singularry) |

---

*Last updated: 2026-02-09*
