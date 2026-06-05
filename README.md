# Backpack (backpack)

Backpack is a Solana-first crypto company founded by Armani Ferrante and Tristan Yver — the same team behind Coral and the Anchor framework that powers a majority of Solana programs. It operates two flagship products: Backpack Wallet, an open-source self-custodial multichain wallet (Solana, Ethereum, Bitcoin) with an xNFT plugin runtime, available as a Chrome/Brave extension and iOS/Android app; and Backpack Exchange, a fully fledged centralized exchange offering spot, perpetual futures, dated futures, prediction markets, borrow/lend, RFQ, strategies, vaults, and securities, with a comprehensive ED25519-signed REST + WebSocket API documented at docs.backpack.exchange. Backpack Exchange acquired and processes FTX EU claims and is one of the more technically transparent venues to emerge post-FTX.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/backpack/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/backpack/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Crypto
- Exchange
- Wallet
- Trading
- Perpetuals
- Solana
- Web3
- DeFi
- xNFT
- Anchor
- Coral
- Centralized Exchange
- Self-Custody

## Timestamps

- **Created:** 2026-05-24
- **Modified:** 2026-05-24

## APIs

### Backpack Exchange API

The Backpack Exchange API is the canonical programmatic surface for the Backpack Exchange centralized crypto venue — spot, perpetual futures, dated futures, prediction markets, borrow/lend, RFQ, strategies, and vaults. Authentication is ED25519 keypair-based: every signed request carries X-API-Key, X-Signature, X-Timestamp, and X-Window headers, with each operation bound to a named instruction (orderExecute, balanceQuery, borrowLendExecute, etc.). Resource groups include Account, Account Limits, Capital, Order, Position, Borrow Lend, Markets, Trades, Assets, RFQ, Strategy, Vaults, Withdrawal Delays, and System, plus public and authenticated WebSocket streams on wss://ws.backpack.exchange/.

- **Human URL:** [https://docs.backpack.exchange/](https://docs.backpack.exchange/)
- **Base URL:** `https://api.backpack.exchange`

#### Tags

- Crypto
- Exchange
- Trading
- Spot
- Perpetuals
- Order Book
- Market Data
- Solana
- Web3
- DeFi

#### Properties

- [Documentation](https://docs.backpack.exchange/)
- [Authentication](https://docs.backpack.exchange/#section/Authentication)
- [Authentication](https://docs.backpack.exchange/#section/Authentication/Signing-requests)
- [Documentation](https://docs.backpack.exchange/#section/Infrastructure)
- [Changelog](https://docs.backpack.exchange/#section/Changelog)
- [OpenAPI](openapi/backpack-exchange-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/backpack-exchange.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backpack-exchange.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/backpack-order-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/backpack-market-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/backpack-position-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/backpack-balance-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/backpack-trade-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/backpack-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/backpack-order-execute-example.json)
- [Example](examples/backpack-markets-list-example.json)
- [Example](examples/backpack-depth-example.json)

### Backpack Exchange WebSocket Streams API

Real-time market and account event streams over WebSocket. Public streams cover ticker, depth, trades, klines, mark price, open interest, and liquidation events keyed by symbol. Private (signed) streams cover per-symbol order updates (account.orderUpdate.<symbol>), position updates (account.position), and RFQ updates (account.rfqUpdate). Signing uses the same ED25519 instruction model as the REST API (subscribe instruction).

- **Human URL:** [https://docs.backpack.exchange/#tag/Streams](https://docs.backpack.exchange/#tag/Streams)
- **Base URL:** `wss://ws.backpack.exchange`

#### Tags

- Crypto
- Exchange
- WebSocket
- Streaming
- Market Data
- Real-Time
- Order Updates
- Position Updates

#### Properties

- [Documentation](https://docs.backpack.exchange/#tag/Streams)
- [OpenAPI](openapi/backpack-exchange-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/backpack-exchange.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backpack-exchange.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](asyncapi/backpack-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)

### Backpack Wallet

Backpack Wallet is a self-custodial multichain wallet for Solana, Ethereum, and Bitcoin, originally built around the xNFT (executable NFT) protocol that lets dApps run as plugins inside the wallet. Available as a Chrome/Brave extension and iOS/Android mobile app, sharing identity and session with Backpack Exchange when linked. Open source under GPL-3.0 at github.com/coral-xyz/backpack.

- **Human URL:** [https://backpack.app/](https://backpack.app/)

#### Tags

- Crypto
- Wallet
- Solana
- Ethereum
- Bitcoin
- Multi-Chain
- xNFT
- Self-Custody

#### Properties

- [Documentation](https://backpack.app/)
- [GitHub Repository](https://github.com/coral-xyz/backpack)
- [Tool](https://chromewebstore.google.com/detail/backpack/aflkmfhebedbjioipglgcbcmnbpgliof)
- [Tool](https://apps.apple.com/us/app/backpack-wallet-exchange/id6445964121)
- [Tool](https://play.google.com/store/search?q=backpack+wallet+and+exchange&c=apps&hl=en_US)
- [Postman Collection](collections/backpack-exchange.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backpack-exchange.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Portal](https://backpack.app/)
- [Portal](https://backpack.exchange/)
- [Documentation](https://docs.backpack.exchange/)
- [Sign Up](https://backpack.exchange/join)
- [Sign Up](https://backpack.exchange/refer)
- [GitHub Organization](https://github.com/coral-xyz)
- [GitHub Repository](https://github.com/coral-xyz/backpack)
- [GitHub Repository](https://github.com/coral-xyz/anchor)
- [GitHub Repository](https://github.com/coral-xyz/xnft)
- [GitHub Repository](https://github.com/coral-xyz/multisig)
- [GitHub Repository](https://github.com/coral-xyz/sealevel-attacks)
- [Status Page](https://status.backpack.exchange/)
- [Blog](https://backpack.exchange/blog)
- [Twitter](https://twitter.com/Backpack)
- [Forum](https://discord.gg/backpack)
- [LinkedIn](https://www.linkedin.com/company/backpack-exchange)
- [Support](https://support.backpack.exchange/)
- [F A Q](https://support.backpack.exchange/)
- [Terms of Service](https://backpack.exchange/refer/terms)
- [Privacy Policy](https://backpack.exchange/privacy)
- [Authentication](https://docs.backpack.exchange/#section/Authentication)
- [Spectral Rules](rules/backpack-rules.yml)
- [Vocabulary](vocabulary/backpack-vocabulary.yml)
- [Plans](plans/backpack-plans-pricing.yml)
- [Rate Limits](rate-limits/backpack-rate-limits.yml)
- [Fin Ops](finops/backpack-finops.yml)
- [Changelog](https://docs.backpack.exchange/#section/Changelog)
- [Sign Up](https://backpack.exchange/refer/api)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
