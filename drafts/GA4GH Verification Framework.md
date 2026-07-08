# GA4GH Verification Framework

**Source**: TASC  
**Recommendation**: GA4GH-REC-05  
**Title**: GA4GH Verification Framework  
**Related GitHub issues**: [#74](https://github.com/ga4gh/TASC/issues/74)  
**Raised by**: Andy Yates (TASC Co-lead)  
**Authors**: Andy Yates  
**Date:** 2026-07-08  
**Status:** Draft  
**Keywords**: verification, implementation, compliance, open-source, attestation, verified-adoption, catalogue
**Work Streams Impacted**: All work streams  
**Products Affected**: All GA4GH technical products  

## Abstract

This document defines the GA4GH Verification Framework, a structured mechanism for potential adopters to assess whether implementations of GA4GH products meet a recognised standard of quality, interoperability, and sustainability. The framework is organised into three tracks: Track 1 for open-source deployable software, Track 2 for closed-source and platform/service implementations, and Track 3 for non-software products (Verified Adoption). Track 1 is ready for immediate application; Tracks 2 and 3 will be developed through structured pilots. The framework also establishes a single GA4GH implementation catalogue as the central registry for all verified and compliant implementations.

## Table of contents

- [Recommendation](#recommendation)
- [Background](#background)
- [Detailed Guidance](#detailed-guidance)
- [Considerations](#considerations)
- [References](#references)
- [Contributors](#contributors)

## Recommendation

The GA4GH Verification Framework SHALL comprise three tracks, each addressing a distinct class of GA4GH product. All verified implementations and adoptions MUST satisfy the following principles:

- **Transparency**: A verified implementation or adoption MUST be describable in sufficient detail that a third party can assess its suitability.
- **Interoperability**: Verification MUST include evidence that the implementation or adoption works with others, whether through compliance suites, peer review, or mutual recognition.
- **Sustainability**: Verification MUST consider the ongoing viability of the implementation or adoption, not only its current state.
- **Proportionality**: The burden of verification SHOULD be proportionate to the nature of the product and the risks involved.
- **Not an endorsement**: Verification SHALL constitute recognition that defined criteria have been met. It MUST NOT be presented or interpreted as a GA4GH recommendation or guarantee of fitness for any particular deployment context.

Track-specific requirements are as follows:

- **Track 1** (open-source deployable software): Implementations MUST meet all mandatory attribute requirements defined in the Track 1 attribute table. Verification SHALL be tied to a major version of the GA4GH product; new major versions MUST be resubmitted. Implementations MUST pass the relevant compliance suite where one exists. A running demonstration deployment MUST be registered with compliance test infrastructure where available.
- **Track 2** (closed-source and platform/service implementations): Implementations MUST supply a completed self-declaration form and evidence checklist in place of direct code inspection. The Terms of Use MUST be compatible with federated GA4GH infrastructure use. A continuity and exit statement MUST be provided.
- **Track 3** (non-software products): Adopting organisations MUST provide a conformance mapping document showing how their local processes correspond to the GA4GH product's requirements. Adoptions MUST be publicly describable to a level that allows another party to understand what was adopted and how.

All verified implementations and adoptions MUST be registered in the GA4GH implementation catalogue. A minimum of 60 days notice MUST be given before an implementation or adoption is removed from the catalogue.

## Background

GA4GH produces a wide range of products: open-source software, commercial platform integrations, and non-software frameworks covering policy, ethics, and regulatory guidance. Potential adopters — research institutes, healthcare providers, and infrastructure operators — need a trustworthy basis for assessing whether a given implementation is suitable for their context.

The framework extends the earlier "Starter Kit" concept and replaces the provisional "Verified Implementations" label. It is designed to answer a single unifying question: **can a potential adopter trust this implementation enough to deploy it in their infrastructure or incorporate it into their governance?**

What "trust" looks like differs by product type. A single set of criteria would either be too onerous for policy adoptions or too permissive for deployed software. The three-track structure reflects this reality while sharing common principles and a common catalogue.

## Detailed Guidance

### Track 1: Open-source deployable software

Track 1 addresses open-source, deploy-it-yourself implementations of GA4GH technical standards. It is the most mature part of the framework and is ready for immediate application.

#### Definition

A Track 1 Verified Implementation is a piece of open-source software that implements one or more GA4GH technical products and meets all mandatory attribute requirements, assessed against a specific versioned release.

Verification under Track 1 is NOT:

- A guarantee that the implementation is production-ready or has been through an independent security review.
- Conformance with country or regional legislation (e.g. GDPR, ELSI).
- An endorsement of the implementation's security posture or compliance status.
- A guarantee that support will be available in perpetuity.
- Confirmation that the implementation integrates with any other specific implementation.

#### Application process

Requests MUST be submitted to the GA4GH Technical Team (from which a representative will be selected) and the Chief Product Officer (CPO) using the standardised submission form (see [GA4GH Verification Framework: Track 1 Submission Form]). The review ensures that the minimum requirements in the attribute table are met. Feedback MUST be provided to unsuccessful applications. GA4GH reserves the right to apply a fair charge for commercial implementations.

#### Verification and publicity

When an implementation meets the minimum requirements:

- It SHALL be registered in the GA4GH implementation catalogue and tagged as a GA4GH Verified Implementation.
- It MAY display a GA4GH Verified Implementation badge in its repository and documentation.
- It SHALL be listed on the GA4GH website with a link to its own documentation.
- A demonstration deployment MUST be registered with compliance test infrastructure where available.

In the first instance, verification operates on the basis of good faith and due diligence, with automated assessment methods to be built over time.

#### Ongoing compliance and removal

Implementations are required to self-check their adherence to the verification attributes. An implementation MAY be removed from the catalogue if it no longer meets the criteria or is no longer aligned with the aims of GA4GH. In such cases, 60 days' notice MUST be given and an open dialogue with the maintainers MUST be conducted before removal.

#### Relationship to other GA4GH efforts

Track 1 is complementary to the GA4GH Testbed (which reports compliance suite results) and GA4GH Service Registry (which supports service discovery). Verified implementations SHOULD link to both where applicable.

#### Support expectations

At minimum, a Track 1 Verified Implementation MUST provide:

- A mechanism to register issues and report bugs.
- A mechanism for external contributors to provide code enhancements or bug fixes (without obligation to integrate them).
- Documentation on integrating custom data and debugging an instance.

Additional support channels (e.g. helpdesk, Slack, mailing list) are encouraged and SHOULD operate on a best-effort basis.

#### Track 1 attribute requirements

| **Attribute** | **Requirements** |
|---|---|
| **Maturity** | Implements one approved version of a GA4GH product. Demo implementation has been verified as running and is available. Implements baseline support for the GA4GH product (as defined by the product itself). |
| **Software licence & availability** | Open-source licence (see OSI). Permissive licence (e.g. Apache 2.0) preferred. Available via a public open-source repository (GitHub, Bitbucket, etc.). |
| **Documentation** | Reviewed README with tested and verified instructions for running the component. Documented mechanism to operate on custom data. Installation guide. Configuration guide. Upgrade path documented between versions (or noted if not possible). |
| **Deployment** | At least one deployment mechanism available (e.g. container image or source repository). Container images (if available) are freely available from a public registry (DockerHub, Quay.io, Amazon ECR, GHCR). Versioned code releases. |
| **Interoperability** | Passes the relevant compliance suite. |
| **Support, issue tracking and enhancements** | Documented mechanism to log support requests, report bugs, and flag security issues (e.g. GitHub Issues). Issue tracker is publicly available. Prescribed way to provide code enhancements or bug fixes (e.g. pull requests or an established commercial update scheme). A recognition process is in place for contributors. |
| **Engineering practices** | Consistent code formatting and adherence to language best practices. Developer environment setup instructions. Instructions for running in debug/developer mode (if available). Continuous integration, linting, and code quality monitoring in place. |
| **Security** | Follows security best practices; provides a statement or evidence of security processes and controls. |
| **Testing and operational quality** | Test suite (e.g. unit tests) developed and executed periodically. If intended as a reference implementation, a minimal software stack SHOULD be used. Logging using a standard library, configurable by the deployer. Ability to generate standard logs (e.g. HTTP logs for a web API). |

#### Initial pilot implementations

Track 1 criteria will be validated against the following implementations:

- **Htsget** — University of Melbourne Centre for Cancer Research
- **DRS Starter Kit** — GA4GH
- **VRS Python** — Genomic Knowledge Standards Work Stream
- **Planetary** — St. Jude TES implementation

Feedback from these pilots will be used to refine the criteria before wider application.

---

### Track 2: Closed-source and platform/service implementations

Many implementations of GA4GH standards are delivered as commercial platforms, managed services, or closed-source software. These cannot be assessed through source code inspection, but adopters still need a basis for trust. Track 2 addresses this through an attestation-based model.

#### Core approach: from inspection to attestation

Where Track 1 relies on the ability to inspect code, repositories, and CI pipelines directly, Track 2 shifts to a model where the provider supplies evidence of their practices. The reviewer assesses the quality and completeness of this evidence rather than inspecting the underlying artefacts.

#### What carries over from Track 1

| **Attribute** | **Track 1** | **Track 2 Adaptation** |
|---|---|---|
| **Support** | GitHub Issues or similar | Support portal, helpdesk, or documented escalation path |
| **Documentation** | Installation, configuration, upgrade guides | Integration/onboarding guides, API documentation, upgrade/migration path |
| **Maturity** | Demo deployment, baseline product support | Demo or sandbox environment, baseline product support |
| **Interoperability** | Passes compliance suite | Passes compliance suite (more critical here as the primary technical verification lever) |

#### What needs substantive adaptation

**Software Licence & Availability → Terms of Use & Access**

The open-source licence requirement is replaced by requirements around API/service terms of use. The terms MUST be compatible with the adopter's intended use. Pricing SHOULD be transparent. Restrictions that would limit deployment within a federated GA4GH infrastructure MUST be declared.

**Engineering practices & Security → Security & Operational Attestation**

Rather than inspecting CI pipelines and code coverage, the provider MUST supply evidence of their security posture. This SHOULD include penetration test summaries (or confirmation of regular testing), vulnerability disclosure and patching policies, SLAs, and incident response procedures. GA4GH is not auditing the provider; it is requiring that the provider demonstrate their practices at a level that enables an adopter to make a risk assessment.

#### What is new to Track 2

**Continuity & exit**

For closed-source and service implementations, adopters need assurance about what happens if the provider changes terms, is acquired, or discontinues the service. Track 2 MUST require a statement on data portability, export capabilities, and any lock-in risks.

**Review mechanism**

Track 2 reviews are likely to carry a greater burden than Track 1. This is the appropriate point at which to apply a fair charge for commercial implementations. The review pathway remains a Technical Team representative and CPO, supported by relevant work stream leads where domain expertise is needed (e.g. GA4GH Data Security work stream members).

#### Pilot programme

Track 2 SHALL be developed through a structured pilot:

1. Identify 2–3 willing closed-source or platform implementers of GA4GH standards to participate. These SHOULD represent a range of implementation types (e.g. a cloud platform, a commercial toolkit, a national infrastructure service).
2. Draft a self-declaration form and evidence checklist based on the adapted attributes above, drawing on the Track 1 submission form as a starting point.
3. Run the pilot, collecting feedback on the clarity, proportionality, and feasibility of the criteria from both reviewers and pilot participants.
4. Refine and formalise the Track 2 criteria based on pilot findings, publishing as v2.0 of this framework.

**Target timeline:** Pilot to begin once Track 1 is operational, with formalised criteria within 6–12 months.

---

### Track 3: Non-software products (Verified Adoption)

GA4GH's product portfolio extends beyond software standards to include policy frameworks, consent codes, ethics toolkits, and regulatory guidance — primarily from the Regulatory and Ethics Work Stream (REWS), but also from other work streams. These products are not "deployed" in the traditional sense; they are adopted. Track 3 reframes verification as "Verified Adoption", recognising this fundamental difference.

#### Mapping Track 1 concepts to non-software products

| **Track 1 Concept** | **Track 3 Equivalent** | **What This Looks Like in Practice** |
|---|---|---|
| **Maturity** | Completeness of adoption | Does the adopter's process or policy cover the baseline requirements of the GA4GH product? A structured self-assessment against the product's requirements. |
| **Documentation** | Conformance mapping | A mapping document showing how the adopter's local processes correspond to the GA4GH product's requirements. Analogous to an ISO statement of applicability. |
| **Interoperability** | Mutual recognition | Organisation A's ethics review is recognised by Organisation B because both have adopted the same GA4GH framework to a verified standard. Assessed via peer review or a structured checklist developed by the relevant work stream. |
| **Support** | Community engagement | The adopter has a contact point, participates in the relevant work stream or community of practice, and feeds back experience. |
| **(New) Transparency** | Public describability | The adopter makes their adoption publicly describable — not necessarily the full internal policy, but enough that another party can understand what was adopted and how. |

#### Track 3 review mechanism

Track 3 reviews MUST involve domain expertise from the relevant work stream. The Technical Team representative and CPO pathway used for Tracks 1 and 2 SHALL be supplemented by work stream leads (e.g. REWS co-chairs) who can assess the substance of the adoption. Each work stream SHOULD develop a standardised template and assessment checklist for its own products to provide consistency.

#### Developing Track 3 in parallel

Track 3 SHALL be developed in parallel with the Track 2 pilot:

1. Identify a pilot product — work with REWS to select one concrete product for the initial pilot.
2. Conduct a paper exercise — take one known adopter and map their practice against a draft set of Track 3 criteria.
3. Draft the assessment template based on the paper exercise.
4. Pilot with one additional adopter to validate the template, then formalise as part of the framework.

**Target timeline:** Paper exercise to begin immediately upon publication of Track 1. Formalised criteria to be published alongside or shortly after Track 2.

---

### The implementation catalogue

A single GA4GH implementation catalogue SHALL serve as the central registry for all tracks. The catalogue SHALL:

- List all known implementations of GA4GH products, including those that have not applied for verification.
- Clearly tag verified implementations with their track and verification status.
- Link to compliance suite results (GA4GH Testbed) and service registrations (GA4GH Service Registry) where applicable.
- Over time, support focused collections — curated groupings of implementations that together address a particular domain (e.g. rare disease, infectious disease surveillance).

Passing a standard's compliance suite SHALL be sufficient to be listed in the catalogue, even without full verification.

---

### Proposed timeline

| **Phase** | **Track 1** | **Track 2** | **Track 3** |
|---|---|---|---|
| **Now** | Publish v1.0 criteria. Begin pilot with named implementations. | Identify pilot participants. | Select pilot product with REWS. Begin paper exercise. |
| **3–6 months** | Refine criteria based on pilot feedback. Open submissions. | Draft self-declaration form. Run pilot. | Draft assessment template. Pilot with 1–2 adopters. |
| **6–9 months** | Catalogue operational. Badge and compliance tagging live. | Refine and formalise Track 2 criteria. | Refine and formalise Track 3 criteria. |
| **9–12 months** | Review cycle established. | Open for submissions. Publish as part of framework v2.0. | Open for submissions. Publish as part of framework v2.0. |

## Considerations

- Verification operates initially on good faith and due diligence. Automated assessment methods are expected to complement but not immediately replace this approach.
- GA4GH reserves the right to apply a fair charge for commercial implementations under both Track 1 and Track 2.
- This framework does not confer conformance with country or regional legislation. Adopters remain responsible for their own legal and regulatory compliance.
- The Track 1 attribute table will be refined following the initial pilot. Implementers who participate in the pilot should expect some evolution of the criteria before wider application.

## References

- [GA4GH Verification Framework: Track 1 Submission Form] — supporting document
- [TASC-ADR-006] — Decision: Three-track structure for the Verification Framework
- [TASC-ADR-007] — Decision: Attestation model for Track 2
- [TASC-ADR-008] — Decision: Verified Adoption framing for Track 3
- [GA4GH Testbed](https://github.com/ga4gh/testbed) — compliance suite infrastructure
- [GA4GH Service Registry](https://github.com/ga4gh-discovery/ga4gh-service-registry) — service discovery
- [OSI Open Source Licences](https://opensource.org/licenses)
- [RFC 2119](https://datatracker.ietf.org/doc/html/rfc2119) — Key words for use in RFCs to indicate requirement levels

## Contributors

| Name | Organisation |
|------|-------------|
| Andy Yates | EMBL-EBI / TASC Co-lead |

**PLEASE ADD MORE IN HERE**

*Drafted with assistance from Claude Sonnet 4.6 (`claude-sonnet-4-6`), Anthropic.*
