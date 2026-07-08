# TASC-ADR-006: Three-track structure for the GA4GH Verification Framework

**Date:** 2026-07-08 | **Status:** Proposed  

**Deciders:** TASC  
**Keywords:** verification, framework, track-1, track-2, track-3, open-source, attestation, verified-adoption  
**Work Streams Impacted:** All work streams  
**Products Affected:** All GA4GH technical products  

---

## Context

GA4GH needed a mechanism to allow potential adopters to assess whether implementations of its products meet a recognised standard of quality, interoperability, and sustainability. The central question was: **how should verification criteria be structured given that GA4GH products span open-source software, commercial platforms, and non-software policy frameworks?**

**The Problem:**

GA4GH products are heterogeneous. A single set of verification criteria that works for an open-source bioinformatics toolkit cannot reasonably apply to a commercial cloud platform or an ethics consent framework. Applying software-oriented criteria to policy adoptions would be category error; applying policy-oriented criteria to software would miss the technical assurances adopters need.

**Alternatives Considered:**

1. **Single unified framework**
   - ✅ Simpler to administer and communicate
   - ❌ Criteria either too onerous for policy adoptions or too permissive for deployed software
   - ❌ Forces products through an ill-fitting model, reducing credibility of verification

2. **Binary split: software vs. non-software**
   - ✅ Acknowledges the fundamental difference between software and policy products
   - ❌ Does not distinguish between open-source (inspectable) and closed-source (attestation-only) software
   - ❌ Adopters of commercial platforms would face criteria designed for open-source inspection, which is not feasible

3. **Three-track structure (open-source / closed-source / non-software)**
   - ✅ Matches criteria to the actual nature of each product class
   - ✅ Allows Track 1 to launch immediately while Tracks 2 and 3 are developed through pilots
   - ✅ Shared principles and a common catalogue provide coherence across tracks
   - ✅ Extensible — additional tracks can be added without disrupting existing ones

---

## Decision

TASC adopts a three-track structure for the GA4GH Verification Framework:

- **Track 1** — Open-source deployable software: criteria based on direct inspection of code, documentation, CI pipelines, and a running demonstration deployment.
- **Track 2** — Closed-source and platform/service implementations: criteria based on provider-supplied attestations and evidence reviewed by GA4GH.
- **Track 3** — Non-software products (Verified Adoption): criteria based on conformance mapping and peer review, led by the relevant work stream.

**Key Points:**

- All tracks share the same governing principles (Transparency, Interoperability, Sustainability, Proportionality, Not an endorsement) and a common implementation catalogue.
- Track 1 is ready for immediate application. Tracks 2 and 3 are developed through structured pilots.
- Verification status under any track is tied to a specific version of the relevant GA4GH product.

---

## Consequences

### Positive

✅ Criteria are appropriate and credible for each product class.  
✅ Track 1 can launch without waiting for Tracks 2 and 3 to be fully developed.  
✅ A shared catalogue and shared principles provide organisation-wide coherence.  
✅ The structure is extensible if new product classes emerge.

### Negative

❌ Three separate frameworks require separate maintenance and governance effort.  
❌ Communicating a three-track model externally is more complex than a single framework.  
❌ Risk of inconsistency developing between tracks over time if they evolve independently.

### Risks & Mitigations

**Risk:** Track 2 and Track 3 criteria may diverge significantly from the principles established in Track 1 as they mature through pilots.  
- **Mitigation:** All tracks are governed by the same normative principles. Cross-track review at each formalisation step (v2.0 publication) is required.

**Risk:** Implementers offering both open-source and commercial versions of the same product may be uncertain which track applies.  
- **Mitigation:** Track selection is based on the nature of the specific submission, not the organisation. A product can hold verification under multiple tracks simultaneously.

---

## References

- **Full Policy:** [GA4GH Verification Framework (GA4GH-REC-05)]
- **Related ADRs:** [TASC-ADR-007] — Attestation model for Track 2; [TASC-ADR-008] — Verified Adoption framing for Track 3

---

## Notes

*Drafted with assistance from Claude Sonnet 4.6 (`claude-sonnet-4-6`), Anthropic.*
