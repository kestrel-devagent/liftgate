# Liftgate

**Agent preference infrastructure** for coding / tool agents.

Mine trajectories → audit soft vs strong preference labels → export DPO / preference splits → agent-eval gate.

Product: **Liftgate** · Billing: **Kestrel Ops**

> Not an ops / Datadog dashboard.

## Live

- Landing + thesis: https://kestrel-devagent.github.io/liftgate/
- Starter ($49/mo draft): https://kestrel-devagent.github.io/liftgate/starter.html
- Repo: https://github.com/kestrel-devagent/liftgate

## Free tier (Hub)

Honest FINDINGS tone — inspect cards before claiming lift:

| Artifact | URL |
|----------|-----|
| Strong preference split | https://huggingface.co/datasets/asaverren/openhands-divergence-dpo-strong |
| Qwen3.5-4B LoRA (strong-scale default) | https://huggingface.co/asaverren/qwen35-4b-openhands-divergence-dpo |
| Parent full mined set | https://huggingface.co/datasets/asaverren/openhands-divergence-dpo |

## Paid Starter (draft) — $49/mo

- Private trajectory ingest
- Soft-label audit
- Strong-split export
- Monthly agent-eval gate

PayPal to `hudson.gouge@projxon.ai` (note `Liftgate Starter $49`) → email txn ID → manual unlock code. See `UNLOCK.md` and `docs/starter.html`.

## Waitlist

Pages form uses **mailto** to `hudson.gouge@projxon.ai` plus optional browser-local NDJSON download (static hosting).

## GitHub Pages

Source: `main` branch · folder `/docs`.

```bash
# Enable once:
gh api -X POST repos/kestrel-devagent/liftgate/pages \
  -f build_type=legacy \
  -f source[branch]=main \
  -f source[path]=/docs
```

## Brand

- Say **Liftgate** (product) and **Kestrel Ops** (billing)
- Do not put a personal name in public marketing copy
