# HJS-AIP Integration Analysis

**Status: CONCEPTUAL - PENDING COMMUNITY FEEDBACK**

This repository documents the **proposed** integration between **HJS (Human Judgment System)** and **AIP (Agent Identity Protocol)**.

**Not a working integration.** Subject to AIP community adoption of extensions.

---

## Current Reality

| HJS Primitive | AIP v1alpha3 Support | Extractable? |
|:---|:---|:---:|
| **Delegation** | `user_id`, `agent_id`, `delegation_scope` | ✅ **YES** |
| **Verification** | `aat_issuer`, AAT validation | ⚠️ Partial |
| **Judgment** | `model_id`, `model_parameters` - **MISSING** | ❌ **NO** |
| **Termination** | `output_commitment`, execution status - **MISSING** | ❌ **NO** |

**Result: Only 1.5/4 primitives extractable from current AIP v1alpha3.**

Complete evidence chain **requires AIP extensions or HJS standalone mode**.

---

## What This Repository Contains

| Directory | Content | Status |
|:---|:---|:---|
| `mappings/` | Field-level mapping analysis with gap annotations | ✅ Draft complete |
| `scripts/` | Planned conversion scripts | ❌ **Not implemented** |
| `examples/` | Sample AIP log + simulated HJS evidence (labeled) | ✅ Shows target state |
| `docs/` | Integration proposals for IETF discussion | 📝 In progress |

---

## Examples

### `examples/sample-aip-audit.json`
**Real AIP v1alpha3 audit log format** (Section 12).

Shows what AIP actually logs today. Includes `_comment` fields explaining gaps.

### `examples/sample-hjs-evidence.json`
**Simulated HJS evidence** showing target state.

Demonstrates what complete evidence WOULD look like if AIP adopted proposed extensions. **Cannot be generated from real AIP logs alone.**

---

## Required AIP Extensions

For complete integration, AIP v1alpha4+ would need:

| Extension | For HJS Primitive | Purpose |
|:---|:---|:---|
| `model_id` | Judgment | Identify AI model |
| `model_parameters` | Judgment | Record model config |
| `input_commitment` | Judgment | Cryptographic input hash |
| `execution_status` | Termination | Success/failure/exception |
| `output_commitment` | Termination | Cryptographic output hash |

**Status: Proposed to AIP maintainers. Not confirmed.**

---

## Honest Assessment

**What works today:**
- Extracting Delegation from AIP logs
- Using AAT validation as partial Verification
- HJS standalone mode (complete, no AIP dependency)

**What doesn't work:**
- Complete evidence chain from AIP logs alone
- Judgment/Termination without AIP extensions
- Verifiable hash chain (requires all 4 primitives)

**Recommendation:**
Use [HJS standalone](https://github.com/schchit/hjs-api) for production accountability. This AIP integration is experimental and incomplete.

---

## IETF Discussion

Active discussion with AIP maintainers:
- [Agent2Agent Working Group Thread](https://github.com/openagentidentityprotocol/agentidentityprotocol/discussions/14#discussioncomment-15927585)

## Related Specifications

- [HJS Protocol](https://github.com/schchit/hjs-api) - Human Judgment System (standalone)
- [AIP v1alpha3](https://agentidentityprotocol.io/specs/aip-v1alpha3) - Agent Identity Protocol

## License

MIT
