# Initial threat model

Research proposal; no Safehouse implementation or independently verified mitigation. This model needs architectural approval before engineering work.

## Assets and trust boundaries

Assets: memory contents and metadata, authorized scope, one-time authority, review snapshots, audit provenance, keys and private identifiers.
Boundaries: browser to local service; service to independent operator; untrusted memory to trusted structure; local generation to external delivery; private audit to public evidence.

The related prototype uses independent terminal decisions. That is not OS-level identity authentication, a trusted display, or separation from malicious software with the same user privileges.

| Threat | Research objective | Related evidence / remaining gap |
|---|---|---|
| Scope expansion or dependency disclosure | Bind target, purpose, question and explicit memory selection | Bounded local prototype evidence; no Safehouse receiver |
| Replay or expired authority | Refuse reuse; never restore historical approval | Round 19–20 observations; no universal or cross-implementation proof |
| Prompt/structure injection | Treat body as data; check trusted bindings | Structural checks do not prove a model resists prompt injection |
| Browser-origin abuse | Constrain local transport and decisions | Related prototype tests; no OS isolation guarantee |
| Same-user malware or malicious administrator | Protect authority and display | Not addressed; requires separate Safehouse architecture review |
| False or missing audit | Preserve provenance and distinguish evidence stages | No Safehouse cryptographic ledger or independent witnesses |
| Metadata correlation and public evidence leakage | Minimize disclosure and publication | Public evidence review required; hashing is not anonymization |
| Remote service misuse | Obtain verifiable receipt and assess limitations | Remote acknowledgment, retention and deletion not proven |
| Key loss, theft and recovery | Define revocation and recovery without bypass | Keys/recovery design not implemented |

No promise is made about fully compromised hosts, side channels, remote erasure or legal admissibility. Availability, rate limiting, rollback, crash recovery and key lifecycle need explicit implementation-specific testing.

Research objectives must be tagged separately from observed prototype behavior. Independent review, negative tests and failure evidence are prerequisites to stronger claims.
