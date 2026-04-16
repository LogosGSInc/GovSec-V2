# HAAP — Governance Summary

Protocol: Human-Agency Assurance Protocol v2.0
Role: Authorization token issuance immutable logging and revocation
Status: Active deployed on ASF

## Three-Layer Authorization Model

| Layer | Function |
|---|---|
| Layer 1 | Constitutional bounds non-negotiable no override |
| Layer 2 | Policy-governed authorization token issued or denied |
| Layer 3 | Human-in-the-loop escalation execution halted |

## Token Lifecycle

| State | Meaning |
|---|---|
| Issued | Authorized approved to proceed |
| Pending | Human escalation required suspended |
| Denied | Refused blocked and logged |
| Revoked | Previously granted rescinded |
| Expired | Lifetime exceeded reauthorization required |

## Immutable Logging
Every authorization event generates an append-only cryptographically anchored evidence record with action identifier authorizing principal policy version token state timestamp and causal linkage.

## Integration With Sentinel OverWatch
Every BLOCKED or HARD_LOCKED verdict generates a corresponding HAAP evidence record. Security and governance events are the same event recorded in both layers.

## Integration With DEP.KEYSTONE
Trust Score below 70 triggers Layer 3 human escalation before deployment authorization proceeds.

## Governance Limits Test Live Output
HAAP Layer 2 Limitations acknowledged.
Actions above Tier 2 require human authorization before execution.
Default to least-authority execution outside existing definitions.
All authorization events logged to audit record.
Immediate Tier 3 escalation required for unclassifiable actions.

## Human Agency Preservation
No AI system can self-authorize beyond Layer 1 override a pending escalation state or alter its own evidence records. All authority traces to a human principal.

LOGOS Governance Systems Inc. April 2026. Sanitized for public diligence.
