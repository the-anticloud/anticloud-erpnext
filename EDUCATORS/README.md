# Educators — ERPNEXT

**Project:** ERPNEXT  
**Category:** SUPERMARKETS  
**Upstream:** https://github.com/frappe/erpnext  
**Pinned commit:** `d607837e80fa731e2b3b285c9873f3f1185653bc`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `f7f1688da851e6b4993ed1564ba25f864b6e6bccafd4f5a7eedc29d04bc32ced`  
**Date:** October 2026

## Teaching with ERPNEXT

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `f7f1688da851e6b4993ed1564ba25f864b6e6bccafd4f5a7eedc29d04bc32ced` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
