### Ayoub Boukadida · `@viperco`

Pi Network Pioneer · Open Source Contributor · building decentralized commerce with **PiDCTP** & **Pi Visual Builder**

---

## Projects

| Project | What it is | Status |
|---|---|---|
| [**π = π — Pi fungibility proof**](https://github.com/aybvip/pi-fungibility) | Source-verified, dependency-free proof that mined π and exchange π are the same native asset | ✅ **Verified and runnable** · MIT |
| [**Pi fixed supply**](https://github.com/aybvip/pi-fixed-supply) | Every ledger header examined on Pi Mainnet reports `totalCoins = 100,000,000,000 π`, with SHA-256-verified raw header bytes | ✅ **Verified and runnable** · MIT |
| [**pi-ecosystem-mcap**](https://github.com/aybvip/pi-ecosystem-mcap) | Independent analysis of Pi ecosystem market-cap mechanics at activation: PiDEX liquidity, OUSD, AI Tokens, NFTs, CiDi Games case study — confirmed facts vs speculation | ✅ **Live site + tools** · MIT |
| [**Pi payment reference**](https://github.com/aybvip/aybvip/tree/archive/payment-app) | A working Pi payment integration: `server.js` plus Netlify functions for `approve` / `complete` / `cancel` | 📦 **Archived** — kept off `main` on the [`archive/payment-app`](https://github.com/aybvip/aybvip/tree/archive/payment-app) branch |
| [**Pi Visual Builder**](https://github.com/aybvip/Pi-Visual-Builder) | Design specification and static UI mockups for a visual, no-code app builder on Pi Network | 📄 **Proposal — no implementation yet** |

**Honest note on Pi Visual Builder:** it is a specification and mockups, not a product. There is no
application code in that repository. The "PiRC4" name is a placeholder — the official
[`PiNetwork/PiRC`](https://github.com/PiNetwork/PiRC) repository contains only `PiRC1` and `PiRC2`, and
[Issue #381](https://github.com/PiNetwork/PiRC/issues/381) / [PR #382](https://github.com/PiNetwork/PiRC/pull/382)
are open and unassigned.

### Measurement tooling

Read-only, zero-dependency tools that answer a question **with a measurement** rather than an opinion.
Each one prints what it can prove and what it cannot.

| Project | The question it answers |
|---|---|
| [**pi-soroban-events**](https://github.com/aybvip/pi-soroban-events) | What does the Pi Soroban RPC's `getEvents` actually do? (There is **no** ~10 000-ledger cap; the real footguns are different.) |
| [**pi-event-integrity**](https://github.com/aybvip/pi-event-integrity) | Which ledger ranges can be **proven** covered, and which are only a lower bound — with a replayable SHA-256 digest, plus event identity: duplicate/gap detection, resume, and independent-source comparison. |
| [**pi-contract-simulator**](https://github.com/aybvip/pi-contract-simulator) | What does a contract simulation return on Pi Testnet, and how do its failures classify? Never signs or submits. |
| [**pi-contract-upgrade-trail**](https://github.com/aybvip/pi-contract-upgrade-trail) | How has a contract's `wasmHash` changed across deployments? |
| [**pi-gap-index**](https://github.com/aybvip/pi-gap-index) | What is measurably missing from the public Pi developer surface, and what would a read contract look like? |
| [**pi-api-contract-registry**](https://github.com/aybvip/pi-api-contract-registry) | What do Pi's Soroban RPC methods **actually** return — with wire types — and where does behaviour drift from what a spec-following client expects? Re-measurable live. |
| [**pi-user-behavior**](https://github.com/aybvip/pi-user-behavior) | What user behavior is observable on the Pi blockchain — and what is **not**. |
| [**pi-contribution-evidence-model**](https://github.com/aybvip/pi-contribution-evidence-model) | A reference model for a contribution evidence layer, with executable invariants. Offline; no personal data; no combined score. |
| [**pi-app-security-scanner**](https://github.com/aybvip/pi-app-security-scanner) | Does a Pi app's source contain documented SDK anti-patterns? Every rule is anchored to a verbatim official quote. Executes nothing. |
| [**pi-chaos-lab**](https://github.com/aybvip/pi-chaos-lab) | What does the Pi Soroban RPC do when a request is **wrong**? Measures the failure shapes (HTTP 200 with an error, HTTP 204 empty body, silent empty ranges, ignored `limit`) and replays them **offline** to test client error handling. Never attacks or floods. |
| [**pi-proofkit**](https://github.com/aybvip/pi-proofkit) | How do I make a claim **checkable without trusting its author**? Packages claims + evidence + a SHA-256 over a fully-specified canonical form, so anyone can recompute the digest by hand. A digest proves **integrity, not truth**. |

### Pi NFT and asset work

| Project | What it is |
|---|---|
| [**pi-nft-provenance**](https://github.com/aybvip/pi-nft-provenance) | Reads a transaction, its ledger, operations and effects. |
| [**pi-nft-fee-check**](https://github.com/aybvip/pi-nft-fee-check) | Reconciles declared fees against on-chain events. |
| [**pi-zk-nft-gate**](https://github.com/aybvip/pi-zk-nft-gate) | A zero-knowledge NFT gate, read-only. |
| [**pi-muxed-guard**](https://github.com/aybvip/pi-muxed-guard) | Guards against muxed-address handling mistakes in Pi integrations. |

## How I work

A claim is only worth as much as the evidence someone else can rerun.

- **Official sources only**, quoted verbatim and pinned to a specific revision.
- **Runnable, dependency-free proofs** — no install step, no build step, `node` and nothing else.
- **Explicit scope** — what is proven, what is merely verifiable per case, and what is *not* claimed.
- **Limitations stated on the page**, not hidden. "Not independently audited" is printed on the work itself.
- **Measurement over opinion** — tools probe the live public surface before asserting anything about it.
- **No unbacked claims** — prior-art statements say "no prior work found", never "first"; adoption by Pi Network is always `not-claimed`.

---

## π = π — Pi fungibility proof

Source-verified, dependency-free, read-only proof that Pi Network's native asset is fungible:
**a native Pi payment carries no observable per-unit mining origin on the Pi Mainnet ledger.**
Mined π and π withdrawn from an exchange are the **same native asset**.

- 🌐 **Website / all pages:** <https://aybvip.github.io/pi-fungibility/>
- 📦 **Repository:** <https://github.com/aybvip/pi-fungibility>- 📄 **The proof, step by step:** <https://aybvip.github.io/pi-fungibility/PROOF.html>
- 🧭 **Index — every file, by file and by question:** <https://aybvip.github.io/pi-fungibility/docs/INDEX.html>
- 🎯 **Scope — what is proven vs NOT claimed:** <https://aybvip.github.io/pi-fungibility/docs/SCOPE.html>
- 📚 **Sources — verbatim quotes from official docs:** <https://aybvip.github.io/pi-fungibility/docs/SOURCES.html>
- 🤖 **Machine-readable index (AI tools):** <https://aybvip.github.io/pi-fungibility/llms.txt>
- 🏷️ **Release v1.0.0:** <https://github.com/aybvip/pi-fungibility/releases/tag/v1.0.0>

### Reproduce it (Node 18+, zero dependencies, read-only)

```bash
git clone https://github.com/aybvip/pi-fungibility
cd pi-fungibility
node examples/run-all.mjs           # everything at once (+ summary)
node examples/run-all.mjs --offline # skip network checks
```

### Scope, kept honest

| Claim | Status |
|---|---|
| **A** — Fungibility (mined π ≡ exchange π) | ✅ Proven (deterministic, reproducible) |
| **B** — A specific deposit is native on-chain | ✅ Verifiable per case (from the txid) |
| **C** — Reserve backing of an exchange's internal balances | ❌ Not claimed |

Also **not** claimed: price, identity-hiding, IOU equivalence, or an independent audit.

> Independent & unofficial — not affiliated with Pi Network. **Not independently audited** (self-verified and reproducible). MIT licensed.

---

## pi-ecosystem-mcap

Independent analysis of Pi ecosystem market-cap mechanics at ecosystem activation:
**how value flows through PiDEX, OUSD, AI Tokens, NFTs — with CiDi Games as a live case study.**
Separates what is officially confirmed from community speculation.

- 🌐 **Website + interactive flow visualizer:** <https://aybvip.github.io/pi-ecosystem-mcap/>
- 🎨 **Ecosystem Flow Viz (animated canvas):** <https://aybvip.github.io/pi-ecosystem-mcap/viz.html>
- 📦 **Repository:** <https://github.com/aybvip/pi-ecosystem-mcap>
- 🎮 **CiDi Games case study:** <https://aybvip.github.io/pi-ecosystem-mcap/docs/CASE_CIDI>
- 🚀 **PiRC Launchpad analysis:** <https://aybvip.github.io/pi-ecosystem-mcap/docs/LAUNCHPAD_PIRC>
- ⚖️ **Ecosystem comparison (Pi vs BNB vs Solana):** <https://aybvip.github.io/pi-ecosystem-mcap/docs/ECOSYSTEM_COMPARE>
- 🤖 **Machine-readable index:** <https://aybvip.github.io/pi-ecosystem-mcap/llms.txt>
