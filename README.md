# HJS-AIIP Integration Layer

This repository defines the integration layer between **HJS (Human Judgment System)** and **AIIP (Agent Identity Protocol)**.

## Overview

HJS provides four accountability primitives (Judgment, Delegation, Termination, Verification) with OpenTimestamps anchoring to Bitcoin. AIIP provides identity, authentication, and policy enforcement for AI agents.

This integration enables:
- **AIIP audit logs** to be structured as **HJS evidence packages**
- **HJS primitives** to be populated from **AIIP events** (AAT validation, tool calls, policy decisions)
- **Long-term verifiability** of AI agent actions via blockchain anchoring

## Repository Structure
.
├── mappings/ # Field-level mappings between HJS and AIIP
├── scripts/ # Conversion scripts (AIIP log → HJS evidence)
├── examples/ # Sample audit logs and generated evidence
└── docs/ # Integration proposals for IETF/working groups

text

## Quick Start

*(Coming soon)*

## Related Specifications

- [HJS Protocol](https://github.com/schchit/hjs-spec) - Human Judgment System core specification
- [AIIP v1alpha3](https://agentidentityprotocol.io/specs/aip-v1alpha3) - Agent Identity Protocol

## IETF Discussion

This work is part of the Agent2Agent IETF working group discussion:
- [Working Group Thread](https://github.com/yungcero/agent2agent/issues/14)

## License

MIT
