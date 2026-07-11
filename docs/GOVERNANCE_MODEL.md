# Governance Model

P.Ai.O.S. governance exists to keep claims, evidence, privacy, and validation status aligned.

## Public Governance Layers

| Layer | Purpose | Public artifact |
|---|---|---|
| Claims | Control public wording. | `evidence/PUBLIC_CLAIMS_REGISTER.csv` |
| Evidence | Track supporting records. | `evidence/EVIDENCE_LEDGER.md` |
| Source control | Track versions, status, and access level. | `evidence/SOURCE_MANIFEST.csv` |
| Privacy | Define what stays out of the public repository. | `PRIVACY.md` |
| Validation | Test transfer beyond founder use. | `validation/` |
| Reporting | Convert operations into reviewable records. | `docs/REPORT_SYSTEM.md` |

## Review Cadence

- Claims register: review before major README or website changes.
- Evidence ledger: review whenever a new report or case study is added.
- Source manifest: review whenever canonical files change.
- Validation package: review before each pilot cycle.
- Privacy controls: review before adding any source-derived artifact.

## Change Rule

If a public claim changes, update the claims register in the same pull request.
