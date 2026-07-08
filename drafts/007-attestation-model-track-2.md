# TASC-ADR-007: Attestation-based review model for Track 2

**Date:** 2026-07-08 | **Status:** Proposed  

**Deciders:** TASC  
**Keywords:** verification, track-2, attestation, closed-source, commercial, inspection  
**Work Streams Impacted:** All work streams  
**Products Affected:** All GA4GH technical products delivered as commercial platforms or managed services  

---

## Context

Track 2 of the GA4GH Verification Framework (GA4GH-REC-05) covers closed-source software, commercial platforms, and managed services. These implementations cannot be assessed through direct inspection of source code, CI pipelines, or repository artefacts — yet adopters still need a trustworthy basis on which to evaluate them.

**The Problem:**

Track 1 verification relies on the ability to inspect publicly available code, documentation, and CI outputs. For closed-source and platform implementations, this is not possible. The question was: **how should GA4GH assess compliance for implementations that cannot be directly inspected?**

**Alternatives Considered:**

1. **Require third-party audit**
   - ✅ High assurance — independent verification
   - ❌ Prohibitively expensive and time-consuming for providers
   - ❌ GA4GH lacks the infrastructure and accreditation to mandate or conduct audits
   - ❌ Would exclude most commercial implementers, reducing framework uptake

2. **Apply Track 1 criteria as-is, requiring public artefacts**
   - ✅ Consistent with Track 1 — no new model required
   - ❌ Impossible for closed-source implementations by definition
   - ❌ Would exclude the majority of commercial GA4GH implementers

3. **Attestation model: provider-supplied evidence reviewed by GA4GH**
   - ✅ Feasible for closed-source providers — evidence rather than artefact inspection
   - ✅ Scales to a range of provider types (cloud platforms, commercial toolkits, national services)
   - ✅ Consistent with approaches used in comparable standards bodies (ISO, SOC 2)
   - ❌ Places greater burden on the reviewer to assess evidence quality
   - ❌ Relies partly on good faith; cannot guarantee accuracy of self-declared evidence

---

## Decision

Track 2 verification SHALL use an attestation-based model. The provider supplies a completed self-declaration form and supporting evidence; GA4GH reviews the quality and completeness of that evidence rather than inspecting underlying artefacts directly.

**Key Points:**

- Track 2 replaces source-code and CI inspection with structured evidence packs covering security posture, operational practices, terms of use, and interoperability.
- The compliance suite (GA4GH Testbed) remains the primary technical verification lever and carries over unchanged from Track 1.
- A continuity and exit statement (data portability, lock-in risks) is new to Track 2 and has no Track 1 equivalent, reflecting the additional risk of service discontinuation.
- The review pathway (Technical Team representative and CPO, supplemented by relevant work stream leads) is the same as Track 1, but the greater evidential burden justifies applying a fair charge for commercial Track 2 reviews.

---

## Consequences

### Positive

✅ Enables verification for the large class of GA4GH implementers who cannot expose source code.  
✅ Review mechanism is proportionate — focused on evidence quality, not exhaustive audit.  
✅ Compliance suite results provide an objective technical anchor independent of attestation.  
✅ Continuity and exit requirements protect adopters from lock-in risk, which is absent from open-source implementations.

### Negative

❌ Reviewer must assess the completeness and credibility of evidence rather than inspecting facts directly — higher skill and judgement required.  
❌ Good-faith reliance on provider declarations introduces risk that evidence may not reflect actual practices.  
❌ Criteria require ongoing maintenance as Track 2 matures through the pilot programme.

### Risks & Mitigations

**Risk:** Providers supply superficial or misleading attestations that pass review but do not reflect actual practices.  
- **Mitigation:** Review includes a quality and completeness assessment, not just a checklist check. Reviewers may request additional evidence. Removal from the catalogue remains available if practices are found to be inconsistent with attestations.

**Risk:** The review burden is high enough to deter GA4GH staff from conducting Track 2 reviews.  
- **Mitigation:** A fair charge for commercial implementations is built into the framework from the outset, creating resource for the additional review effort.

---

## References

- **Full Policy:** [GA4GH Verification Framework (GA4GH-REC-05)]
- **Related ADRs:** [TASC-ADR-006] — Three-track structure; [TASC-ADR-008] — Verified Adoption framing for Track 3

---

## Notes

*Drafted with assistance from Claude Sonnet 4.6 (`claude-sonnet-4-6`), Anthropic.*
