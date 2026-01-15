# Teos Integration — Architecture

This document defines the integration architecture and adapter patterns used to connect TEOS modules with external systems (apps, services, institutions, and partner platforms). The objective is **auditability**, **deterministic behavior**, and **clean separation** between external systems and TEOS core logic.

---

## Integration Overview

```mermaid
flowchart LR
    External[External System / Partner]
    Adapter[Integration Adapter]
    Policy[Policy & Validation]
    SDK[Elmahrosa SDK]
    Chains[Chain Adapters]
    Audit[Audit & Evidence]

    External --> Adapter
    Adapter --> Policy
    Policy --> SDK
    SDK --> Chains
    Policy --> Audit

