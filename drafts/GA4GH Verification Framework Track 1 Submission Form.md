# GA4GH Verification Framework: Track 1 Submission Form

**Source**: TASC  
**Title**: GA4GH Verification Framework: Track 1 Submission Form  
**Related document**: GA4GH-REC-05 GA4GH Verification Framework  
**Authors**: Andy Yates  
**Date:** 2026-07-08  
**Status:** Draft  
**Keywords**: verification, track-1, submission-form, open-source, compliance  
**Work Streams Impacted**: All work streams  
**Products Affected**: All GA4GH technical products  

## About this form

This form is used to request Track 1 Verified Implementation status under the GA4GH Verification Framework (GA4GH-REC-05). Complete all sections and submit to the GA4GH Technical Team and Chief Product Officer (CPO).

Assessment criteria are defined in the Track 1 attribute table in GA4GH-REC-05. Feedback will be provided to unsuccessful applications.

---

## About the implementation

- Implementation name
- Brief description (1–2 sentences: what it does and who it's for)
- GA4GH product(s) implemented (e.g. htsget, DRS, VRS)
- GA4GH product version(s) (the approved standard version, e.g. htsget v1.3)
- Version being submitted for review (release tag or commit SHA)
- Repository URL
- Primary programming language(s)

## About the submitter

- Submitting organisation or group
- Primary contact name
- Primary contact email
- Secondary contact name (optional)
- Secondary contact email (optional)

## Licence

- What licence is the software released under?
- Link to the licence file in the repository

## Documentation

- Link to the README
- Link to installation instructions (if separate from README)
- Link to configuration guide (if separate from README)
- Link to instructions for operating on custom data
- Link to upgrade/migration documentation between versions (or state that this is not yet applicable and why)
- Links to any additional documentation (hosted docs, wiki, API reference)

## Deployment

- What deployment mechanism(s) are available? (e.g. container image, source build, pip/npm/conda package, Helm chart)
- Container image location, if applicable (e.g. docker.io/org/image, ghcr.io/org/image)
- Link to versioned releases (e.g. GitHub Releases page, PyPI page)

## Demo deployment

- URL of a running demo instance
- Brief description of what the demo shows
- Any access instructions or credentials needed to use the demo

## Interoperability

- Does a compliance suite exist for this GA4GH product? (Yes / No)
- If yes: link to compliance suite results (CI output, Testbed entry, or test report)
- If no: named contributor who will participate in developing a compliance suite (name and affiliation)
- If no: target date or milestone for that contribution
- Has the implementation been tested for interoperability with any other implementations? If so, which ones?

## Support

- Link to issue tracker (e.g. GitHub Issues)
- How should security issues be reported? (e.g. SECURITY.md, private email, GitHub private vulnerability reporting)
- How can external contributors submit code changes? (e.g. pull requests, contribution guide)
- How are external contributors recognised? (e.g. CONTRIBUTORS file, release notes, other)
- Additional support channels, if any (e.g. Slack, mailing list, discussion forum)

## Engineering practices

- Link to CI/CD pipeline configuration or recent runs
- What code quality or linting tools are in use?
- Link to developer environment setup instructions
- How can the implementation be run in debug or developer mode? (or state N/A)

## Security

- Briefly describe the security practices in place for this project (e.g. dependency scanning, static analysis, container scanning, signed releases, vulnerability disclosure policy)
- Link to a security policy document, if one exists

## Testing and operational quality

- Link to the test suite (directory or configuration)
- How and when are tests executed? (e.g. on every PR, nightly, manually)
- What logging library is used? Is log level/output configurable by the deployer?
- Does the implementation produce standard HTTP/access logs? (Yes / No / N/A)
- If this is intended as a reference implementation: briefly describe the software stack and confirm it aims for minimal dependencies

## Anything else

- Is there any additional context we should be aware of?

---

*Drafted with assistance from Claude Sonnet 4.6 (`claude-sonnet-4-6`), Anthropic.*
