# Liftgate Starter — manual unlock stub

Internal ops note (not customer-facing brand copy).

## Flow

1. Customer pays **$49 USD** via PayPal to `hudson.gouge@projxon.ai` with note `Liftgate Starter $49`.
2. Customer emails the same address with:
   - PayPal transaction ID
   - Workspace email
   - Agent / tool stack
3. Ops verifies payment → issues one-time unlock code → emails ingest instructions.

## Code format (draft)

```
LG-START-{YYYYMM}-{8HEX}
```

Example: `LG-START-202609-A1B2C3D4`

Log unlocks in `data/unlocks.ndjson` (gitignored locally):

```json
{"code":"LG-START-202609-A1B2C3D4","tier":"starter","email":"buyer@example.com","paypalTxn":"...","createdAt":"2026-09-16T18:00:00-04:00","usedAt":null}
```

## Public brand rules

- Product: **Liftgate**
- Billing: **Kestrel Ops**
- Never put a personal name in public marketing copy
- PayPal / contact address may appear as `hudson.gouge@projxon.ai`

## Next (not this ship)

- PayPal webhook or Stripe Checkout → auto-set `tier=starter`
- Hosted ingest API + signed upload URLs
- Scheduled monthly eval-gate job
