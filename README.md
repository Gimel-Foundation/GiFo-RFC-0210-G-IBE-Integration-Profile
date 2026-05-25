# GiFo-RFC-0210 (V0.8)

G-IBE Integration Profile - Combined Credential- and Platform-bound Enforcement (CCPE-G)

New Request for Comments of Gimel Foundation (GiFo RFC) - G-IBE Integration Profile - Combined Credential- and Platform-bound Enforcement (CCPE-G)

Abstract of RFC: The seventh integration pattern within the Combined Credential- and Platform-Bound Enforcement (CCPE) family named G-IBE, the Identity-Bound Enforcement profile. This RFC defines how GAuth integrates with identity-bound IAM platforms - IAM platforms that issue an agent-as-first-class identity object inside an enterprise directory and that bind the agent's authority to act on behalf of a principal to the attributes, entitlements, and lifecycle state of that identity object.

The architectural pattern this RFC names - “identity = mandate”, in shorthand - is the structural posture taken by a wide and growing set of identity-bound IAM platforms. This RFC is the engine-neutral integration profile for that pattern. It specifies 
a)	the architectural model of identity-bound enforcement and the four boundary primitives at which the IAM platform's authority surface is exposed; 
b)	the four normative non-conformant variants NCI / NCP / NCO / NCM; 
c)	the bridge contract by which a CCPE-G deployment derives a synthetic CCPE-A/B/F-shaped mandate envelope from identity attributes plus a recorded principal-delegation event; 
d)	the audit-trail invariants under the catalogue-and-prescribe posture of §3.0; 
e)	the four governance-profile categories Minimal / Standard / Strict / Platform-Native;
f)	the Preliminary Microsoft Entra Agent ID Cookbook (Appendix A) and the Preliminary Cookbooks for Okta + Auth0 (B), Ping + ForgeRock (C), SPIFFE/SPIRE-with-layered-principal-delegation (D), and CyberArk + Venafi (E); and 
g)	the GAuth Open-Core Reference Connector Slot Registry of §13.A.

Central thesis: A credential-bound identity is not the same as a credential-bound authority. Identity-bound enforcement, taken on its own, does not yet meet the state-of-the-art PoA-protocol bar set by GiFo-RFC 0117's Power-PEP pipeline operating on a GiFo-RFC 0115 PoA Credential. A pure identity bound mandate does not necessarily comply with the EU AI Act`s requirements.
Identity-based authentication establishes that an agent is registered and that its credential is valid; it does not establish, on a per-action basis, who the natural-person principal is, what scope the action falls within, what consent the principal gave, what evidence was used, or how the action can be revoked or overridden. The EU AI Act's Articles 12, 13, 14, 15, 26, and 27 require precisely those per-action, per-principal, evidentiary properties. Pure identity-based enforcement, deployed in isolation against any AI Act high-risk use-case, cannot generate the evidentiary record the regulator will ask for.
CCPE-G's contribution, therefore, is to bring both angles together in a single deployable architecture: Phase 1 - GAuth's credential-bound authority enforcement (mandate / PoA Credential / 16-check Power-PEP) - combined with Phase 2 - the IAM platform's identity-platform-bound authentication enforcement (Conditional Access / authorization-server / workload-attestation). The bridge contract of §6 is the central operational mechanism (not a sidecar) by which Phase 2 hands a derived synthetic mandate to Phase 1 at every action class governed by §6.2's trigger conditions; a Phase-2-only deployment that omits the bridge Should not claim CCPE-G conformance above the Minimal profile of §8.1. The full Phase-1 / Phase-2 architectural statement is §3.0.

This RFC refers to Apache 2.0 together with the legal terms of Gimel Foundation. The RFC inherits three Exclusions (AI-Enabled Governance, Web3, DNA-based ID / PQC), in line with the legal terms.

You are more than welcome to contribute !

Legal Provisions for users of this page

Please see the Legal Provisions under https://gimelfoundation.com

In particular the following terms apply:

GiFo RFC 0080 Legal Provisions for the Gimel Foundation

GiFo RFC 0090 Legal Provisions Related to Gimel Foundation Documents

GiFo RCC 0100 Rights Contributors Provide to the Gimel Foundation
