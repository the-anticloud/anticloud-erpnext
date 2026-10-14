# Students — ERPNEXT

**Project:** ERPNEXT  
**Category:** SUPERMARKETS  
**Upstream:** https://github.com/frappe/erpnext  
**Pinned commit:** `d607837e80fa731e2b3b285c9873f3f1185653bc`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `f7f1688da851e6b4993ed1564ba25f864b6e6bccafd4f5a7eedc29d04bc32ced`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `d607837e80fa731e2b3b285c9873f3f1185653bc`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `f7f1688da851e6b4993ed1564ba25f864b6e6bccafd4f5a7eedc29d04bc32ced`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
