# Technical Architecture — STYLE_DICTIONARY

**Upstream:** [https://github.com/nicolo-ribaudo/style-dictionary](https://github.com/nicolo-ribaudo/style-dictionary)
**License:** Apache 2.0
**Category:** DESIGN_TOOLS
**Anticloud Integration:** PAX L5 Narrow L2 General 27B + AIOSS + Offline-First

## Upstream Description

Design token management

## Anticloud Architectural Changes

1. PAX L5 Narrow L2 General 27B local generative UI/UX suggestions and copy
2. Single-binary offline design tool — no subscription, no cloud sync required
3. AIOSS version history with cryptographic integrity verification
4. AES-256 encryption for client assets and proprietary designs
5. Zero-cloud: all fonts, assets, and templates bundled locally
6. GPU/CPU equalizer: AI generation on GPU or CPU seamlessly
7. Open format exports: SVG, PNG, PDF — no proprietary format lock-in
8. Zero-telemetry: removes all usage tracking and analytics

## Integration Points

- **PAX Inference Socket:** Local HTTP endpoint at `127.0.0.1:11434/v1/chat` — same OpenAI-compatible API, zero cloud
- **AIOSS Hook:** Every write operation calls `aioss_append(event, payload)` before commit
- **Encryption Layer:** All file I/O routed through `anticloud_crypto.encrypt_at_rest()`
- **Single Binary Build:** `pyinstaller anticloud_style_dictionary.spec` or `go build -o style_dictionary`

## Deployment Modes

| Mode | Hardware | Notes |
| --- | --- | --- |
| Edge CPU | Raspberry Pi 4 / Intel NUC | Full feature set, PAX on CPU |
| Desktop GPU | RTX 3060 / A10 | PAX GPU inference, <1s latency |
| Server | 2× A100 | Full batch throughput |
| Air-gapped | Any x86/ARM | Zero network dependency |