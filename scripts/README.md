# Scripts

This directory contains conversion scripts that transform AIP audit logs into HJS evidence packages.

## Planned scripts

| Script | Language | Description |
|--------|----------|-------------|
| `aip2hjs.py` | Python | Reads AIP v1alpha3 audit logs, extracts HJS primitives, generates evidence package with hash chain |
| `ots-anchor.py` | Python | Optional: submits chain_hash to OpenTimestamps for Bitcoin anchoring |

## Usage (once available)

```bash
# Convert AIP audit log to HJS evidence
python aip2hjs.py input-audit.json --output evidence.json

# Generate OTS proof (optional)
python ots-anchor.py evidence.json --anchor
