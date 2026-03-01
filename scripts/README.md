# Scripts

**Status: NOT IMPLEMENTED**

This directory is reserved for future conversion scripts. No code 
currently exists.

## Planned (if AIP extensions adopted)

| Script | Purpose | Blocked By |
|--------|---------|------------|
| `aip2hjs.py` | AIP log → HJS evidence | AIP v1alpha3 missing model_id, output_commitment |
| `ots-anchor.py` | Bitcoin anchoring | HJS standalone already provides this |

## Current Reality

Complete evidence chain from AIP logs alone is **IMPOSSIBLE** with 
v1alpha3. See `/mappings/hjs-aip-mapping.json` for gap analysis.

**Alternative**: Use [HJS standalone](https://github.com/schchit/hjs-api) 
for production accountability.

## If AIP Adopts Extensions

If AIP v1alpha4+ adds required fields, scripts may be implemented 
to:
- Extract Delegation primitive (fully supported)
- Extract partial Verification (with semantic gaps)
- Supplement or skip Judgment/Termination (requires extensions)

No development until AIP extensions confirmed.

## Contributing

If interested in prototyping, open an issue to discuss approach 
before submitting PR.
