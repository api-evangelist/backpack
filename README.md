# Backpack (backpack)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
