# Educators — STYLE_DICTIONARY

**Project:** STYLE_DICTIONARY  
**Category:** DESIGN_TOOLS  
**Upstream:** see BENCH.json  
**Pinned commit:** `8710de9f9dc5e65fad40a5fba979699ed2f8b3cb`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `d1a4263cef1a119f92e090afb9b1ed36071a6e5305117f7c0637ea4503170143`  
**Date:** October 2026

## Teaching with STYLE_DICTIONARY

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `d1a4263cef1a119f92e090afb9b1ed36071a6e5305117f7c0637ea4503170143` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
