# Independent Insurance — STYLE_DICTIONARY

**Project:** STYLE_DICTIONARY  
**Category:** DESIGN_TOOLS  
**Upstream:** see BENCH.json  
**Pinned commit:** `8710de9f9dc5e65fad40a5fba979699ed2f8b3cb`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `d1a4263cef1a119f92e090afb9b1ed36071a6e5305117f7c0637ea4503170143`  
**Date:** October 2026

## Why AI-specific cover matters

Deploying AI in a regulated sector creates liability surfaces that ordinary
technology cover does not reach: inference liability, audit-trail liability,
data-breach liability and IP-infringement liability.

## How this project's architecture reduces insurable risk

| Risk | Cloud AI | STYLE_DICTIONARY with AIOSS |
|---|---|---|
| Audit-trail loss | high — vendor-controlled logs | low — append-only chain, verifiable offline |
| Data breach in transit | high — data transits external servers | low — no external endpoint |
| Compliance violation | high — cannot satisfy air-gap requirements | low — structural |
| IP liability | moderate | low — pinned provenance chain |

## Evidence package for an insurer

- AIOSS chain verification for head `d1a4263cef1a119f92e090afb9b1ed36071a6e5305117f7c0637ea4503170143`
- The 16-check register with per-check evidence hashes
- Framework control mapping in `BENCH.json`

## Contact

lois@0-1.gg
