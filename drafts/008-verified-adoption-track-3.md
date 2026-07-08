# TASC-ADR-008: "Verified Adoption" framing for Track 3 non-software products

**Date:** 2026-07-08 | **Status:** Proposed  

**Deciders:** TASC  
**Keywords:** verification, track-3, verified-adoption, non-software, policy, ethics, REWS  
**Work Streams Impacted:** Regulatory and Ethics Work Stream (REWS), all work streams producing non-software products  
**Products Affected:** GA4GH policy frameworks, consent codes, ethics toolkits, regulatory guidance  

---

## Context

GA4GH's product portfolio includes non-software products: policy frameworks, consent codes, ethics toolkits, and regulatory guidance — primarily from the Regulatory and Ethics Work Stream (REWS), but also from other work streams. These products are not "deployed" in the software sense; organisations incorporate them into their governance processes.

**The Problem:**

The language of Track 1 ("implementation", "deployment", "software licence", "CI pipeline") does not map onto policy and ethics products. Forcing non-software products through a software verification model would produce a poor-fit checklist that neither GA4GH nor adopters could apply meaningfully. The question was: **should non-software products use a variant of the software model, or does the fundamental difference in what is being assessed require a distinct framing?**

**Alternatives Considered:**

1. **Apply a software-inspired checklist with non-software substitutions**
   - ✅ Maintains surface consistency with Tracks 1 and 2
   - ❌ Many Track 1 attributes (software licence, CI pipeline, container image) have no meaningful analogue and would produce "N/A" responses throughout
   - ❌ Adopting organisations would find the form confusing and the process delegitimising
   - ❌ Reviewers would lack meaningful criteria to assess against

2. **Exclude non-software products from the Verification Framework entirely**
   - ✅ Avoids the complexity of adapting a software model
   - ❌ Leaves a major class of GA4GH products without a verification pathway
   - ❌ Fails the adopters of REWS and similar products who need a trust signal

3. **Reframe as "Verified Adoption" with purpose-built concepts**
   - ✅ Accurately describes what is being assessed — adoption of a framework, not deployment of software
   - ✅ Allows each work stream to develop appropriate assessment templates for its own products
   - ✅ Introduces concepts (conformance mapping, mutual recognition, transparency of adoption) that are meaningful for governance products
   - ❌ Adds a third distinct conceptual model to the framework, increasing complexity
   - ❌ Requires significant work stream involvement to develop per-product assessment templates

---

## Decision

Track 3 SHALL use a "Verified Adoption" framing, redefining the core concepts of the Verification Framework for non-software products. "Implementation" becomes "adoption"; "deployment" becomes "incorporation into governance"; "software licence" becomes "terms of adoption and transparency".

**Key Points:**

- The five shared principles (Transparency, Interoperability, Sustainability, Proportionality, Not an endorsement) apply to Track 3 unchanged.
- Each Track 1 attribute is mapped to a Track 3 equivalent: Maturity → Completeness of adoption; Documentation → Conformance mapping; Interoperability → Mutual recognition; Support → Community engagement. A new Transparency attribute is added with no Track 1 equivalent.
- Assessment templates are developed per-product by the relevant work stream (e.g. REWS for consent codes), not centrally by TASC. TASC sets the framework; work streams operationalise it.
- Track 3 reviews MUST include domain expertise from the relevant work stream, supplementing the Technical Team representative and CPO pathway used in Tracks 1 and 2.

---

## Consequences

### Positive

✅ Non-software GA4GH products have a credible, fit-for-purpose verification pathway.  
✅ Adopting organisations can meaningfully engage with criteria designed for governance contexts.  
✅ Mutual recognition becomes an explicit outcome — verified adoption by one organisation can be recognised by another, enabling federated trust.  
✅ Work streams retain ownership of their product-specific assessment criteria.

### Negative

❌ Per-product assessment templates require sustained work stream investment to develop and maintain.  
❌ The absence of a single, central Track 3 template makes the framework harder to communicate at a high level.  
❌ "Verified Adoption" as a label is less immediately intuitive than "Verified Implementation" for external audiences.

### Risks & Mitigations

**Risk:** Work streams do not develop assessment templates, leaving Track 3 as a formal pathway with no practical means of assessment.  
- **Mitigation:** The pilot programme begins with a paper exercise against a single known REWS adopter, producing an initial template. This concrete artefact lowers the barrier for other work streams to develop their own.

**Risk:** "Mutual recognition" as an interoperability criterion is interpreted inconsistently across work streams.  
- **Mitigation:** TASC will publish guidance on what constitutes adequate mutual recognition evidence as part of the Track 3 pilot findings.

---

## References

- **Full Policy:** [GA4GH Verification Framework (GA4GH-REC-05)]
- **Related ADRs:** [TASC-ADR-006] — Three-track structure; [TASC-ADR-007] — Attestation model for Track 2

---

## Notes

*Drafted with assistance from Claude Sonnet 4.6 (`claude-sonnet-4-6`), Anthropic.*
