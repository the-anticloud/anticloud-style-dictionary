# Build and Test

**Project:** `STYLE_DICTIONARY`
**Upstream:** https://github.com/nicolo-ribaudo/style-dictionary
**License:** Apache 2.0

## Quick Start

```bash
git clone https://github.com/nicolo-ribaudo/style-dictionary
cd style-dictionary
pip install -r requirements-anticloud.txt
python anticloud_main.py --offline --pax-local
```

## Anticloud Improvements Applied

1. PAX L5 Narrow L2 General 27B local generative UI/UX suggestions and copy
2. Single-binary offline design tool — no subscription, no cloud sync required
3. AIOSS version history with cryptographic integrity verification
4. AES-256 encryption for client assets and proprietary designs
5. Zero-cloud: all fonts, assets, and templates bundled locally
6. GPU/CPU equalizer: AI generation on GPU or CPU seamlessly
7. Open format exports: SVG, PNG, PDF — no proprietary format lock-in
8. Zero-telemetry: removes all usage tracking and analytics

## Benchmark Targets

| Metric | Target |
| --- | --- |
| Latency | Primary inference task: <5s on CPU, <1s on GPU |
| Throughput | Batch processing: >100 items/hour on single CPU server |
| Memory | <8GB RAM for standard deployment |
| Accuracy | Task-specific accuracy within 5% of cloud-API baseline |

## Build Status

Not yet measured. Run verified build and record actual figures above.
