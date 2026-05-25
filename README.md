# Backpack (backpack)
Backpack is a Solana-first crypto company founded by Armani Ferrante and Tristan Yver — the same team behind Coral and the [Anchor framework](https://github.com/coral-xyz/anchor) that powers a majority of Solana programs. It operates two flagship products: **Backpack Wallet**, an open-source self-custodial multichain wallet (Solana, Ethereum, Bitcoin) with an xNFT plugin runtime, available as a Chrome/Brave extension and iOS/Android app; and **Backpack Exchange**, a fully fledged centralized exchange offering spot, perpetual futures, dated futures, prediction markets, borrow/lend, RFQ, strategies, vaults, and securities, with a comprehensive ED25519-signed REST + WebSocket API documented at [docs.backpack.exchange](https://docs.backpack.exchange/).

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/backpack/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Crypto, Exchange, Wallet, Trading, Perpetuals, Solana, Web3, DeFi, xNFT, Anchor, Coral, Centralized Exchange, Self-Custody

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## Founders

| Person | Role | Background |
|---|---|---|
| Armani Ferrante | Co-founder, CEO | Creator of the Anchor framework (the dominant Solana program framework) and the xNFT protocol via Coral |
| Tristan Yver | Co-founder | Operations, exchange product, previously FTX US |

## APIs

### Backpack Exchange API
Canonical programmatic surface for the Backpack Exchange centralized crypto venue — spot, perpetual futures, dated futures, prediction markets, borrow/lend, RFQ, strategies, and vaults. Authentication is ED25519 keypair-based: every signed request carries `X-API-Key`, `X-Signature`, `X-Timestamp`, and `X-Window` headers, with each operation bound to a named instruction (`orderExecute`, `balanceQuery`, `borrowLendExecute`, etc.).

**Human URL:** [https://docs.backpack.exchange/](https://docs.backpack.exchange/)
**Base URL:** `https://api.backpack.exchange`

- [Documentation](https://docs.backpack.exchange/)
- [Authentication](https://docs.backpack.exchange/#section/Authentication)
- [Signing Requests](https://docs.backpack.exchange/#section/Authentication/Signing-requests)
- [Infrastructure](https://docs.backpack.exchange/#section/Infrastructure)
- [Changelog](https://docs.backpack.exchange/#section/Changelog)
- [OpenAPI](openapi/backpack-exchange-openapi.yml) — 69 paths, 162 schemas extracted from the upstream Redoc spec
- [Naftiko Capability — Account](capabilities/account.yaml)
- [Naftiko Capability — Assets](capabilities/assets.yaml)
- [Naftiko Capability — Borrow Lend](capabilities/borrow-lend.yaml)
- [Naftiko Capability — Borrow Lend Markets](capabilities/borrow-lend-markets.yaml)
- [Naftiko Capability — Capital](capabilities/capital.yaml)
- [Naftiko Capability — Markets](capabilities/markets.yaml)
- [Naftiko Capability — Order](capabilities/order.yaml)
- [Naftiko Capability — Position](capabilities/position.yaml)
- [Naftiko Capability — RFQ](capabilities/rfq.yaml)
- [Naftiko Capability — Strategy](capabilities/strategy.yaml)
- [Naftiko Capability — System](capabilities/system.yaml)
- [Naftiko Capability — Trades](capabilities/trades.yaml)
- [JSON Schema — Order](json-schema/backpack-order-schema.json)
- [JSON Schema — Market](json-schema/backpack-market-schema.json)
- [JSON Schema — Position](json-schema/backpack-position-schema.json)
- [JSON Schema — Balance](json-schema/backpack-balance-schema.json)
- [JSON Schema — Trade](json-schema/backpack-trade-schema.json)
- [JSON-LD Context](json-ld/backpack-context.jsonld)
- [Example — Execute Order (signed)](examples/backpack-order-execute-example.json)
- [Example — List Markets](examples/backpack-markets-list-example.json)
- [Example — Order Book Depth](examples/backpack-depth-example.json)

### Backpack Exchange WebSocket Streams API
Real-time market and account event streams over WebSocket. Public streams cover ticker, depth, trades, klines, mark price, open interest, and liquidation events keyed by symbol. Private (signed) streams cover per-symbol order updates (`account.orderUpdate.<symbol>`), position updates (`account.position`), and RFQ updates (`account.rfqUpdate`).

**Human URL:** [https://docs.backpack.exchange/#tag/Streams](https://docs.backpack.exchange/#tag/Streams)
**Base URL:** `wss://ws.backpack.exchange`

- [Documentation — Streams](https://docs.backpack.exchange/#tag/Streams)
- [OpenAPI (shared spec)](openapi/backpack-exchange-openapi.yml)

### Backpack Wallet
Self-custodial multichain wallet for Solana, Ethereum, and Bitcoin, originally built around the xNFT (executable NFT) protocol that lets dApps run as plugins inside the wallet. Available as a Chrome/Brave extension and iOS/Android mobile app, sharing identity and session with Backpack Exchange when linked. Open source under GPL-3.0.

**Human URL:** [https://backpack.app/](https://backpack.app/)

- [Backpack Wallet repository](https://github.com/coral-xyz/backpack) (TypeScript, GPL-3.0, 1.6k stars)
- [Chrome / Brave Extension](https://chromewebstore.google.com/detail/backpack/aflkmfhebedbjioipglgcbcmnbpgliof)
- [iOS App](https://apps.apple.com/us/app/backpack-wallet-exchange/id6445964121)
- [Android App](https://play.google.com/store/search?q=backpack+wallet+and+exchange&c=apps&hl=en_US)

## Resource Groups in the Exchange API

Public:
- **Assets** — `/api/v1/assets`, `/api/v1/collateral`
- **Markets** — `/api/v1/markets`, `/api/v1/market`, `/api/v1/depth`, `/api/v1/markPrices`, `/api/v1/openInterest`, `/api/v1/fundingRates`, `/api/v1/klines`, `/api/v1/ticker`, `/api/v1/tickers`, `/api/v1/prediction`
- **Trades** — `/api/v1/trades`, `/api/v1/trades/history`
- **Borrow Lend Markets** — `/api/v1/borrowLend/markets`, `/api/v1/borrowLend/markets/history`, `/api/v1/borrowLend/apy`
- **System** — `/api/v1/status`, `/api/v1/ping`, `/api/v1/time`, `/api/v1/wallets`

Authenticated (ED25519 signed):
- **Account** — `/api/v1/account` plus per-instruction limit endpoints (`limits/borrow`, `limits/order`, `limits/withdrawal`)
- **Order** — `/api/v1/order`, `/api/v1/orders` (batch + cancel-all), history at `/wapi/v1/history/orders` and `/wapi/v1/history/fills`
- **Position** — `/api/v1/position`, `/wapi/v1/history/funding`, `/wapi/v1/history/position`
- **Borrow Lend** — `/api/v1/borrowLend`, `/api/v1/borrowLend/positions`, `/api/v1/borrowLend/position/liquidationPrice`, history at `/wapi/v1/history/borrowLend` and `/wapi/v1/history/interest`
- **Capital** — `/api/v1/capital`, `/api/v1/capital/collateral`, `/wapi/v1/capital/deposits`, `/wapi/v1/capital/deposit/address`, `/api/v1/withdrawals`, `/wapi/v1/capital/withdrawals`, `/api/v1/account/convertDust`, `/wapi/v1/dust/history`, `/wapi/v1/settlements`
- **RFQ** — `/api/v1/rfq`, `/api/v1/rfq/quote`, `/api/v1/rfq/accept`, `/api/v1/rfq/refresh`, `/api/v1/rfq/cancel`, `/api/v1/rfqs`, history at `/wapi/v1/history/rfqs` and `/wapi/v1/history/quotes`
- **Strategy** — `/api/v1/strategy`, `/api/v1/strategies`, history at `/wapi/v1/history/strategies`
- **Withdrawal Delays** — `/wapi/v1/capital/withdrawals/delay`

WebSocket:
- **Streams** — `wss://ws.backpack.exchange/`

## Coral / Anchor / xNFT Ecosystem

Backpack is published by the same team as the foundational Solana developer tools:

| Repository | Purpose | Stars |
|---|---|---|
| [coral-xyz/anchor](https://github.com/coral-xyz/anchor) | Solana program framework (the dominant one) | n/a |
| [coral-xyz/backpack](https://github.com/coral-xyz/backpack) | Backpack Wallet (this project) | 1,636 |
| [coral-xyz/xnft](https://github.com/coral-xyz/xnft) | xNFT executable NFT protocol | 143 |
| [coral-xyz/sealevel-attacks](https://github.com/coral-xyz/sealevel-attacks) | Solana program security exploits library | 657 |
| [coral-xyz/multisig](https://github.com/coral-xyz/multisig) | Multi-signature transaction execution | 210 |
| [coral-xyz/anchor-book](https://github.com/coral-xyz/anchor-book) | The Anchor Book | 125 |
| [coral-xyz/anchor-by-example](https://github.com/coral-xyz/anchor-by-example) | Anchor By Example | 124 |
| [coral-xyz/xnft-quickstart](https://github.com/coral-xyz/xnft-quickstart) | Starter code for building an xNFT | 94 |

## Authentication

Every signed request is bound to a named **instruction** (e.g. `orderExecute`, `balanceQuery`, `withdraw`). The signing prefix is `instruction=<name>` followed by alphabetically ordered key=value pairs of the request body or query string, suffixed by `&timestamp=<X-Timestamp>&window=<X-Window>`. The resulting string is signed with the ED25519 private key and base64-encoded into the `X-Signature` header. This pattern prevents a captured signature from being replayed against a different operation.

See [examples/backpack-order-execute-example.json](examples/backpack-order-execute-example.json) for a worked signed-request example.

## Fees and Tiers

- Volume-tier-based maker/taker fee schedule for spot and perpetual futures
- **Effective tier = max(30-day volume tier, BP stake tier, pre-TGE Mad Lad NFT tier)** — recalculated hourly
- USDT/USDC trades at **0% fee** and does not count toward volume-tier upgrades
- Sub-account volume aggregates into main-account tier
- See [plans/backpack-plans-pricing.yml](plans/backpack-plans-pricing.yml)

## FinOps

Backpack does not charge a metered API subscription. The cost surface is per-fill maker/taker fees, withdrawal network fees, wire fees, and borrow interest. The `/wapi/v1/history/fills`, `/wapi/v1/history/funding`, and `/wapi/v1/history/interest` endpoints are the canonical cost-line sources for desk-level FinOps reporting. See [finops/backpack-finops.yml](finops/backpack-finops.yml) for FOCUS mapping.

## Common Resources

- [Backpack App (Wallet)](https://backpack.app/)
- [Backpack Exchange](https://backpack.exchange/)
- [Documentation](https://docs.backpack.exchange/)
- [Status Page](https://status.backpack.exchange/)
- [Support](https://support.backpack.exchange/)
- [Twitter / X](https://twitter.com/Backpack)
- [Discord](https://discord.gg/backpack)
- [LinkedIn](https://www.linkedin.com/company/backpack-exchange)
- [GitHub Organization (coral-xyz)](https://github.com/coral-xyz)
- [Spectral Ruleset](rules/backpack-rules.yml)
- [Vocabulary](vocabulary/backpack-vocabulary.yml)
- [Plans & Pricing](plans/backpack-plans-pricing.yml)
- [Rate Limits](rate-limits/backpack-rate-limits.yml)
- [FinOps](finops/backpack-finops.yml)

## Maintainer

- **Kin Lane** — info@apievangelist.com — [apievangelist.com](https://apievangelist.com) — [@apievangelist](https://twitter.com/apievangelist)
