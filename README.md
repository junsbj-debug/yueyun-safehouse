# YueYun Safehouse — Evidence First

**English** | [简体中文](README.zh-CN.md)

**An open initiative for user-controlled AI disclosures, authorization records, and verifiable evidence.**

**Status:** Early research initiative · No Safehouse reference implementation · No independent security certification

One initiator currently maintains the initiative. Governance and name-use rules remain undecided. This local publication package awaits human review and has not been published. It is intended as a concise engineering collaboration entry point for global developers. The YueYun White Paper 3.0 is the intended home for the broader ideas, social mechanisms and long-term framework; it is not included or independently reviewed here.

## The Problem

As AI agents increasingly use personal memories and act on behalf of people, users need evidence they can keep independently of service providers.

Three questions matter:

**Who received what? Who authorized it? What evidence can the user retain?**

Safehouse explores an open, user-controlled evidence layer for AI interactions.

## A Simple Example

A user authorizes an AI service to use two selected memories for a travel-planning task.

For example, the entirely fictional Mira has three memories: “Mira plans a Kyoto visit,” “Mira prefers relaxed travel,” and “Mira prefers black coffee.” The user selects only the two travel memories and excludes the coffee preference. This illustrates the research objective, not an implemented Safehouse capability.

- A third memory remains excluded.
- The user's local record identifies the authorized scope, recipient, purpose, and decision.
- If a disclosure occurs, the system records its status separately from the authorization.
- If the recipient provides a signed acknowledgment, the user can compare both records.

The example illustrates the intended protocol. It does not imply that recipient acknowledgment is implemented today.

## Three Proposed Building Blocks

### 1. Disclosure Marker

A disclosure-specific identifier intended to support source tracing without becoming a cross-service tracking identifier.

**Status: Concept.** Marker durability, privacy impact, and effects on data usability remain untested.

### 2. User-Side Evidence Ledger

A user-controlled record of authorization decisions, disclosure events, and available delivery evidence.

Potential mechanisms include encrypted local storage, hash chaining, independently verifiable proofs, and batched timestamp anchoring.

**Status: Related local prototypes have undergone limited author-operated testing.** A cryptographically chained, externally anchored Safehouse ledger has not been implemented.

### 3. Signed Receipt & Reconciliation

A receiving service could sign an acknowledgment linking the disclosed information to agreed usage conditions, such as purpose, duration, onward transfer, and model training.

The user could then compare the acknowledgment with their own records.

**Status: Concept.** No verified recipient-signature or cross-party reconciliation implementation exists in this project.

## Design Principles

- User control and minimum necessary disclosure.
- Clear separation of authorization, consumption, delivery, and receipt.
- User-side records remain useful without recipient participation.
- No unnecessary personal-content storage in shared audit evidence.
- No invented cryptography or claims of absolute security.
- Open specifications and independently implementable interfaces.
- Tests and limitations published alongside implementation claims.

## Current Maturity

| Capability | Current status |
|---|---|
| Local memory selection and authorization | Prototype; limited author-observed tests |
| Local denial and expiration handling | Prototype; limited author-observed tests with local audit checks |
| Disclosure Marker | Concept |
| Cryptographic evidence ledger and external anchoring | Concept |
| Signed recipient acknowledgment | Concept |
| Independent Safehouse implementation and replication | Not available |

Related YueYun experiments provide preliminary evidence for local authorization workflows. They are not a completed Safehouse implementation or third-party security validation.

Round 19–20 provide only related-prototype author-run tests, manual observations and local audit checks. Screenshots were not independently read; terminal commands and the complete handoff process are not fully persisted. **I-01 = BLOCKED_CAPABILITY.** See the [evidence scope](docs/validation/README.md).

We aim to publish tests that independent contributors can reproduce.

## Architectural Boundary

- **YMIS:** information-exchange rules for memory, audit-only authorization decisions and audit receipts.
- **Safehouse:** proposed permission enforcement, isolated work environments, user review and evidence handling.
- **Persona Public Network:** proposed service discovery, agent responses, transactions and settlement.

These layers do not automatically confer authority on each other. Historical approval is not a portable, consumable grant. Safehouse responsibilities are research objectives, not implemented security capabilities.

Memory ≠ Permission. Approve ≠ Consume ≠ External Disclosure.
Pre-consumption Revoke ≠ Post-consumption Recall.
Context Ready ≠ External Model Received. Completed ≠ External Model Answered.

## Proposed Conformance Research

An early specification draft proposes ten tests covering authorization scope, untrusted input, single-use permissions, expiration and revocation, excluded memories, ledger integrity, deletion, receipt reconciliation, security-setting changes, and cross-model behavior.

These are **proposed tests, not completed Safehouse certification criteria**.

See the [specification discussion draft](docs/specification-draft.md) and [validation scope](docs/validation/README.md).

## Related Work

Safehouse aims to complement existing authorization and agent interoperability approaches rather than replace them.

Relevant work includes:

- [OAuth 2.1](https://datatracker.ietf.org/doc/draft-ietf-oauth-v2-1/) — delegated authorization.
- [Model Context Protocol](https://modelcontextprotocol.io/) — model-tool and service interoperability, including authorization mechanisms.
- Agent delegation, receipt, and portable-memory approaches — subjects for further source review.

The list above preserves the source draft's related-work overview. External sources and current versions were not verified in this revision; see the [source-verification register](docs/related-work.md).

Safehouse's proposed focus is the **user-controlled evidence record, Disclosure Marker, and recipient reconciliation layer**.

No compatibility with these standards is currently claimed.

## Contributing

Developers, security researchers, privacy engineers, standards contributors, and legal researchers are welcome.

Useful contributions include threat models, minimal schemas, protocol critiques, test cases, independent implementations, and privacy reviews.

Once the repository is published, use GitHub Issues for proposals and design discussions. See the [contribution guide](CONTRIBUTING.md), [security reporting policy](SECURITY.md) and [code of conduct](CODE_OF_CONDUCT.md). GitHub Private Vulnerability Reporting is the preferred proposed channel; its actual availability has not been confirmed. Do not post sensitive details in public issues.

Do not submit personal memories, identifiable conversations, credentials or raw runtime audits. These contribution areas invite discussion; they do not indicate existing implementations or automatically authorize new engineering work.

**Open participation does not imply that a production-ready implementation is available.**

## Non-Goals and Limitations

Safehouse is not a centralized personal-data platform, a payment network, or a tokenization project. It does not replace service providers' own privacy and security obligations.

User-side logs alone cannot prove external receipt or recipient compliance. Disclosed information may not be recoverable or deletable from external systems. Evidence admissibility depends on applicable law and circumstances.

This project is not legal advice, a finalized standard, or a security certification. It does not claim operating-system identity authentication, trusted displays or isolation from malicious software running as the same user. It does not promise remote receipt, remote deletion or absolute security.

## Publication and Licensing

The public documents and specification explicitly included in this repository's [license scope](LICENSE-SCOPE.md) are licensed under [CC BY 4.0](LICENSE). Future reference-implementation code is planned to use Apache License 2.0, with the code's scope and notices established when it is released. YueYun branding, logos and White Paper 3.0 are not automatically included. This decision does not license all future materials. This remains a local review package and has not been publicly released.

**Evidence first. User control by design. Open collaboration.**