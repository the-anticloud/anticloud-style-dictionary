# Command Line Interface — STYLE_DICTIONARY

**Upstream:** https://github.com/nicolo-ribaudo/style-dictionary

## Anticloud CLI

```bash
# Install
pip install anticloud-style-dictionary

# Run offline with PAX inference
anticloud-style-dictionary --offline --pax-local

# Run with AIOSS logging
anticloud-style-dictionary --aioss-log ./ledger.jsonl

# Single binary (after build)
./style_dictionary --config config.yaml
```

## Options

| Flag | Description |
| --- | --- |
| `--offline` | Disable all network calls |
| `--pax-local` | Use local PAX inference at 127.0.0.1:11434 |
| `--aioss-log PATH` | Write AIOSS audit chain to PATH |
| `--encrypt` | Enable AES-256 at rest for output files |
| `--gpu` | Force GPU inference |
| `--cpu` | Force CPU inference |
| `--config PATH` | Load configuration from YAML file |
