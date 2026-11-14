# Audit Skills

Two skills for evidence-based due diligence on BNB Smart Chain — audit the contract and the launch before you touch either.

## The skills

| Skill | What it does |
|---|---|
| [bsc-contract-audit](bsc-contract-audit/) | Evidence-based audit for BSC token contracts, NFT mints, and deposit-refund escrows — 100-point score, avoid / review / pass verdict. |
| [launch-curve-audit](launch-curve-audit/) | Audit a token launch curve (bonding curve / tranche IEO) — price path, lifecycle invariants, adversarial order book, ship / hold / block verdict. |

## What they check

- **bsc-contract-audit:** Sourcify verification, owner/pause/blacklist/hidden-mint/upgrade/tax/maxTx/baseURI privileges, sell-or-resell path, honeypot/mint simulation, holder distribution, LP lock, site-claim vs code diff.
- **launch-curve-audit:** curve price path and integral, deployment pinning, exit/refund/graduation/LP-custody invariants, opening price, adversarial order book.

## Use them when

- "audit this contract" / "is this token a scam or rug" / "is the LP locked" / "should I mint this NFT"
- "audit this launch" / "is this IEO safe" / "review the bonding curve" / "can the owner change the curve"

Everything is **read-only**: no private key, no seed, no wallet, no transaction is ever sent.

## Install

Copy a skill's folder into your agent's skills directory. Each skill is self-contained (`SKILL.md` + `references/` + `scripts/` + its own README).

## Related collections

- [mint-safety-skills](https://github.com/jesshqi/mint-safety-skills) — the safety gates for any mint, claim, or mine transaction.
- [wallet-platform-skills](https://github.com/jesshqi/wallet-platform-skills) — Binance Agentic Wallet CLI and Cogladius Arena.
- [makefun-skills](https://github.com/jesshqi/makefun-skills) — make.fun submission validity.
- [payment-skills](https://github.com/jesshqi/payment-skills) — GoPay promo payment verification.

## License

MIT. See [LICENSE](LICENSE).
