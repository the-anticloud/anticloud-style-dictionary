# Students — STYLE_DICTIONARY

**Project:** STYLE_DICTIONARY  
**Category:** DESIGN_TOOLS  
**Upstream:** see BENCH.json  
**Pinned commit:** `8710de9f9dc5e65fad40a5fba979699ed2f8b3cb`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `d1a4263cef1a119f92e090afb9b1ed36071a6e5305117f7c0637ea4503170143`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `8710de9f9dc5e65fad40a5fba979699ed2f8b3cb`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `d1a4263cef1a119f92e090afb9b1ed36071a6e5305117f7c0637ea4503170143`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
