# Safehouse specification discussion draft

Editorial basis: the Chinese source “跃云安全屋规范（草案 v0.1）”, October 2026. This English summary reorganizes that draft for engineering review; it is not an approved replacement or a released standard. The source has not undergone independent implementation validation. Requirements below are proposed obligations, not implemented capabilities.

## Scope and objects

The source discusses task mandates, disclosure records and visitor receipts. These are Safehouse proposal concepts, not new aliases for YMIS objects. YMIS revision-0.2.3 audit-only authorization decisions must not activate grants. A mapping, schema, interoperability profile and implementation remain future work.

A proposed mandate contains: identity; authorizer (possibly pseudonymous); recipient; purpose; information scope; optional budget; validity interval; risk level; delegation permission (default no); revocation status.
It requires explicit user confirmation; scope expansion requires new confirmation; expiry ends authority. Delegation, if later allowed, only narrows scope. Revocation before disclosure does not imply recall after disclosure.

## Disclosure and data boundaries

The source proposes full-content review before high-risk disclosure and one or bounded consumption per approval. It requires visitor content to be treated as data, not authority to change a mandate or trigger sensitive actions. Disclosure markers are proposed identifiers whose robustness under rewriting would need measured evaluation; they have not been designed or validated.

Approve ≠ Consume ≠ External Disclosure. Local Context generation is not remote delivery.

## Proposed ledger and receipts

The ledger proposal includes record ID, previous-record hash, timestamp, mandate ID, recipient, salted content hash, disclosure category, approval method and outcome. It proposes append-only corrections, encryption, local salt retention, export/self-review and batched external anchoring. None of this cryptographic ledger is implemented in Safehouse.

Visitor receipts would contain record reference, content hash, visitor signature, use terms and time. Standard reviewed cryptographic libraries would be required; algorithms, key lifecycle, trust roots and verification behavior are not specified here. Reconciliation would display disagreements. A local receipt is not a visitor signature.

## Proposed levels

| Level | Source proposal | Current Safehouse status |
|---|---|---|
| L0 | Mandate, disclosure and user-side ledger requirements | Not achieved |
| L1 | L0 plus visitor receipts and reconciliation | Not achieved |
| L2 | L1 plus witnessing and external anchoring | Not achieved |
| L3 | TEE or conditional-payment extension | Reserved, undefined |

Related prototypes must not claim L0 from local audit files. Safehouse has no conformance result.

## Source invariants and open engineering questions

The source proposes user control, no privileged bypass, user-only security downgrades with cooldown, continuing audit, minimal public data and deletion sufficient to prevent reconstruction. These require precise threat models and testable contracts. The deletion requirement is not a proven erasure guarantee; backups, caches, remote copies and public anchors require separate treatment.

A hash alone does not prove truth, author identity or an independently authenticated time. Chaining alone does not prevent rollback or establish completeness. “Accountability first” remains a research goal, not a promise that every disclosure is traceable.

Source-proposed risk-based automatic low-risk execution, key rotation, recovery, witnessing, and payment extensions have not been approved as implementation scope here. Persona Public Network discovery, delegation and settlement remain a separate planning layer.

## Test agenda

The source lists T1–T10: scope excess; instruction-like visitor data; repeated consumption; revoked/expired authority; excluded memory probing; ledger tampering; deletion; receipt mismatch; security downgrade controls; multiple model behavior. These are a proposed agenda, not ten passing tests. A model declining a question does not prove enforced privacy or universal compatibility.

Unresolved issues include identity formats, marker evaluation, witnesses, cross-jurisdiction evidence, delegation liability, deletion versus anchoring and usability thresholds. No API, schema or reference implementation is provided by this repository.
