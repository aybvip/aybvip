### Ayoub Boukadida · `@viperco`

Pi Network Pioneer · Open Source Contributor · Building decentralized commerce with **PiDCTP** & **Pi Visual Builder**

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
node examples/run-all.mjs          # everything at once (+ summary)
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
