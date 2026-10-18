### Ayoub Boukadida · `@viperco`

Pi Network Pioneer · Open Source Contributor · building decentralized commerce with **PiDCTP** & **Pi Visual Builder**

---

## Projects

| Project | What it is | Status |
|---|---|---|
| [**π = π — Pi fungibility proof**](https://github.com/aybvip/pi-fungibility) | Source-verified, dependency-free proof that mined π and exchange π are the same native asset | ✅ **Verified and runnable** · MIT |
| [**Pi payment reference**](https://github.com/aybvip/aybvip/tree/archive/payment-app) | A working Pi payment integration: `server.js` plus Netlify functions for `approve` / `complete` / `cancel` | 📦 **Archived** — kept off `main` on the [`archive/payment-app`](https://github.com/aybvip/aybvip/tree/archive/payment-app) branch |
| [**Pi Visual Builder**](https://github.com/aybvip/Pi-Visual-Builder) | Design specification and static UI mockups for a visual, no-code app builder on Pi Network | 📄 **Proposal — no implementation yet** |

**Honest note on Pi Visual Builder:** it is a specification and mockups, not a product. There is no
application code in that repository. The "PiRC4" name is a placeholder — the official
[`PiNetwork/PiRC`](https://github.com/PiNetwork/PiRC) repository contains only `PiRC1` and `PiRC2`, and
[Issue #381](https://github.com/PiNetwork/PiRC/issues/381) / [PR #382](https://github.com/PiNetwork/PiRC/pull/382)
are open and unassigned.

## How I work

A claim is only worth as much as the evidence someone else can rerun.

- **Official sources only**, quoted verbatim and pinned to a specific revision.
- **Runnable, dependency-free proofs** — no install step, no build step, `node` and nothing else.
- **Explicit scope** — what is proven, what is merely verifiable per case, and what is *not* claimed.
- **Limitations stated on the page**, not hidden. "Not independently audited" is printed on the work itself.

---

## π = π — Pi fungibility proof

Source-verified, dependency-free, read-only proof that Pi Network's native asset is fungible:
**a native Pi payment carries no observable per-unit mining origin on the Pi Mainnet ledger.**
Mined π and π withdrawn from an exchange are the **same native asset**.

- 🌐 **Website / all pages:** <https://aybvip.github.io/pi-fungibility/>
- 📦 **Repository:** <https://github.com/aybvip/pi-fungibility>
- 📄 **The proof, step by step:** <https://aybvip.github.io/pi-fungibility/PROOF.html>
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
