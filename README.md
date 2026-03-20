# @stablefi/sdk — StableFi Wallet SDK (TypeScript)

Give your AI agent a USDC wallet, AgentPassport identity, and trust score.

## What's New (March 2026)
- **AgentPassport** — SSO identity for AI agents (like Google SSO but for agents)
- **x402 Micropayments** — pay as low as $0.000001 per API call
- **Circle Nanopayments** — zero-gas sub-cent USDC transfers
- **Multi-stablecoin** — USDC, USDT, PYUSD acceptance
- **Virtual Visa Card** — via Crossmint partnership
- **TrustModel.ai** — agent safety certification boosts trust score

## Install

```bash
npm install @stablefi/sdk
```

## Quick Start

```typescript
import { StableFi } from '@stablefi/sdk';

const sf = new StableFi({ apiKey: process.env.STABLEFI_API_KEY });

// Register agent + get wallet in one call
const agent = await sf.agents.createWithWallet({
  name: 'My AI Agent',
  capabilities: ['research', 'data-analysis'],
});

console.log(agent.id);          // agt_xxx
console.log(agent.wallet);      // 0x...
console.log(agent.trustScore);  // 305 (Bronze)
```

## Features
- **AgentPassport** — register in Agent Registry, get TrustScore (0-1000)
- **USDC Wallet** — real wallet on Coinbase Base, gasless transfers
- **Transactions** — buy from merchants or other agents
- **Trust Score** — grows with every successful transaction
- **x402** — micropayments for pay-per-API-call pricing
- **Disputes** — 15 reason codes, auto-refund under $100

## Built On
- Coinbase (Base chain, CDP SDK)
- Circle (USDC, RefundProtocol, Nanopayments)
- Visa (virtual cards via Crossmint)

## Links
- [Documentation](https://stablefi.ai/docs)
- [Agent Registry](https://stablefi.ai/registry)
- [Merchant Portal](https://stablefi.ai/merchants)
- [Python SDK](https://github.com/Stablefi-Payments/stablefi-wallet-python)
- [IDE Extension](https://github.com/Stablefi-Payments/stablefi-ide-extension)
