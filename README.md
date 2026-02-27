# HJS-AIP Integration Layer

This repository defines the integration layer between **HJS (Human Judgment System)** and **AIP (Agent Identity Protocol)**.

## Overview

HJS provides four accountability primitives (Judgment, Delegation, Termination, Verification) with OpenTimestamps anchoring to Bitcoin. AIP provides identity, authentication, and policy enforcement for AI agents.

This integration enables:
- **AIP audit logs** to be structured as **HJS evidence packages**
- **HJS primitives** to be populated from **AIP events** (AAT validation, tool calls, policy decisions)
- **Long-term verifiability** of AI agent actions via blockchain anchoring

## Repository Structure

- `mappings/` - Field-level mappings between HJS and AIP
- `scripts/` - Conversion scripts (AIP log → HJS evidence)
- `examples/` - Sample audit logs and generated evidence
- `docs/` - Integration proposals for IETF/working groups

## Quick Start

*(Coming soon)*

## Related Specifications

- [HJS Protocol](https://github.com/schchit/hjs-spec) - Human Judgment System core specification
- [AIP v1alpha3](https://agentidentityprotocol.io/specs/aip-v1alpha3) - Agent Identity Protocol

## IETF Discussion

This work is part of the Agent2Agent IETF working group discussion:
- [Working Group Thread](https://github.com/yungcero/agent2agent/issues/14)

## License

MIT
