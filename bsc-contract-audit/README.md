# BSC Contract Audit

Evidence-based due-diligence audit for BNB Smart Chain (chain 56) token contracts, NFT mints, and deposit-refund "lock-to-allocate" escrows.

## What it does

- **Verification status** — Sourcify match, contract name, ABI.
- **Live privilege inventory** — owner, pause, blacklist, hidden mint, upgrade, tax, maxTx, baseURI.
- **Sell-or-resell path** — can you actually exit, and through where?
- **Honeypot / mint simulation** — simulate before you trust.
- **Holder distribution and LP lock.**
- **Site-claim vs code diff** — does the code match what the site promises?

Returns a **100-point score** with an **avoid / review / pass** verdict.

## Use it when

- "audit this contract"
- "is this token a scam or rug"
- "check this BSC token before buying"
- "is the LP locked"
- "did the owner renounce"
- "should I mint this NFT"
- "is this NFT drop legit"
- "should I lock BNB/USDT for this allocation"
- "is this 24h lock/refund legit"

## How it works

Read `SKILL.md` for the full method. Supporting files:

- `references/probes.md` — the read probes (selectors and what each one proves).
- `references/selectors.md` — function selectors used by the probes.
- `scripts/rpc.py` — read-only RPC helper (eth_call family via curl).
- `scripts/binance_audit.sh` — end-to-end audit runner.

Everything is **read-only**: no private key, no seed, no wallet, no transaction is ever sent.

## Install

Copy the whole directory into your agent's skills directory.

## Companion skills

- [launch-curve-audit](https://github.com/jesshqi/audit-skills/tree/main/launch-curve-audit) — audit a token launch curve (bonding curve / tranche IEO).
- [mint-authorization-gate](https://github.com/jesshqi/mint-safety-skills/tree/main/mint-authorization-gate) — two confirmations naming the exact mint before any execution.

## License

MIT. See [LICENSE](LICENSE).
