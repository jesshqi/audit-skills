# Launch Curve Audit

Method and tooling to audit a token launch curve on BSC — bonding-curve or tranche IEO, Agent-ID or allowlist gating, escrowed bids, graduation into a pool, coupled off-chain emissions.

## What it does

- **Models the price path** — the curve, its integral, and the opening price.
- **Pins the deployment** — which contract, which block, who owns it.
- **Runs the lifecycle invariants** — exit, refund, graduation, LP custody.
- **Prices the adversarial order book** — what happens if the worst actor shows up first.
- Returns a **ship / hold / block** verdict with a finding register.

## Use it when

- "audit this launch"
- "is this IEO safe"
- "review the bonding curve"
- "check the launch before it opens"
- "did they burn the LP"
- "can the owner change the curve"

Scope: the **sale mechanism** (curve / tranche / escrow / graduation / LP custody). For post-listing trading risk, use [bsc-contract-audit](https://github.com/jesshqi/audit-skills/tree/main/bsc-contract-audit) instead.

## How it works

Read `SKILL.md` for the full method. Supporting files:

- `references/attack-surface.md` — where a launch can be attacked.
- `references/economics.md` — curve economics and pricing.
- `references/invariants.md` — lifecycle invariants that must hold.
- `scripts/curve_math.py` — pure curve math (no network).
- `scripts/rpc.py` — read-only RPC helper.
- `scripts/snapshot.sh` — pin a snapshot at a block number.
- `roles.example.env` — template for the deployment's contract addresses (copy to `roles.env`, fill what applies, never put secrets in it).

Everything is **read-only**: no private key, no seed, no wallet, no transaction is ever sent.

## Install

Copy the whole directory into your agent's skills directory.

## Companion skills

- [bsc-contract-audit](https://github.com/jesshqi/audit-skills/tree/main/bsc-contract-audit) — audit a BSC token contract or NFT mint.
- [mint-authorization-gate](https://github.com/jesshqi/mint-safety-skills/tree/main/mint-authorization-gate) — two confirmations naming the exact mint before any execution.

## License

MIT. See [LICENSE](LICENSE).
