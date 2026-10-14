# Related work and source verification register

This is a reading agenda, not a compatibility matrix or an assertion of equivalence. A bounded primary-source review was completed on 2026-10-14 for the entries marked below. Unidentified sources remain unreviewed. This is not an implementation or compatibility audit.

| Candidate | Relevance to investigate | Original source checked? | Relationship status |
|---|---|---|---|
| OAuth 2.1 work | Consent, scope and delegated access | YES, bounded review: [IETF draft-ietf-oauth-v2-1-16](https://datatracker.ietf.org/doc/draft-ietf-oauth-v2-1/), 2026-10-14 | Internet-Draft, not final RFC; no implemented integration |
| Model Context Protocol (MCP) | Tool/context interfaces | YES, authorization section: [2026-07-28](https://modelcontextprotocol.io/specification/2026-07-28/basic/authorization), checked 2026-10-14 | Does not itself establish Safehouse authority or isolation; no compatibility claim |
| Agent2Agent (A2A) | Agent interaction | YES, bounded operations/security/discovery review: [official specification](https://a2a-protocol.org/latest/specification/), 2026-10-14 | Mutable latest page; no fixed release version or compatibility asserted |
| Delegation and receipt drafts | Delegated authority and acknowledgments | NO; source gives no exact document | Exact document/version unresolved; no invented citation |
| Portable memory formats | Memory exchange | NO; source gives no exact format | Comparison pending; YMIS is separate local draft work |
| Certificate Transparency / RFC 9162 | Log and transparency concepts | YES, Merkle inclusion/consistency sections: [RFC 9162](https://www.rfc-editor.org/rfc/rfc9162.html), 2026-10-14 | Not a personal-data ledger specification; no adopted mechanism |
| in-toto | Evidence and provenance concepts | PARTIAL: [official overview](https://in-toto.io/), 2026-10-14; detailed protocol unreviewed | Supply-chain provenance reading candidate, not a verified remote-model receipt mechanism |

Primary-source verification should record exact title, version/date, canonical source, checked sections and a narrow applicability statement. Do not turn a reading candidate into a dependency, endorsement or test result.

The local Safehouse source draft and YMIS architecture documents were read for this package. That does not count as verification of the external works they mention.
