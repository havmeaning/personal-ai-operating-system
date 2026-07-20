# Hiring Intelligence: Building a Decision System for Employment Opportunities

### Methodology and Emerging Case Study

**Status:** Operational methodology documented; historical evidence consolidation in progress.
**Validation:** Founder-designed personal workflow; operational history and external transferability not yet validated.

---

Most job searches run on volume: apply broadly, adjust the resume slightly, hope the numbers work out. Hiring Intelligence started from a different premise — that a job search is a sequence of decisions, and decisions get better when the evidence behind them is explicit rather than assumed. This piece walks through the problem the method was built to solve, the eight-layer architecture itself, the decision logic underneath the prioritization system, and — just as important — what the method has not yet proven. The full technical write-up, including the evidence-mapping framework, artifact inventory, and claim audit, lives on GitHub; this is the shorter version for anyone who wants the reasoning without the appendix.

## The Problem

An unstructured job search fails in specific, identifiable ways — not because effort is missing, but because effort isn't connected to evidence or measurement.

Roles get selected by title rather than requirement, which obscures whether the tools, seniority, or domain knowledge a posting actually asks for line up with real experience. Every opportunity gets treated as equally valuable, so a strong-fit role and a speculative long-shot consume the same time. Required and preferred qualifications blur together, causing self-disqualification from roles that were reachable, or over-investment in roles with a hard gate the candidate can't clear. A single generic resume gets applied across structurally different postings. Transferable evidence — military leadership, operational communications, independent research — gets undercounted when it doesn't already use the target industry's vocabulary. And application tracking, when it happens at all, records activity ("applied / not applied") without capturing the reasoning behind each decision, so the same misjudgments repeat — the same weak-fit role type gets applied to again next month, for the same reasons that didn't work the first time, because nothing was written down to catch the pattern.

Hiring Intelligence was built to correct these failure modes in one operator's process during a career transition toward AI strategy, knowledge operations, and decision-intelligence roles — not to model employer behavior or predict hiring outcomes generally. None of this is a claim about the broader labor market or how employers make decisions; it's a description of what goes wrong when one person runs a job search without a structure for capturing and reviewing their own reasoning, and what that structure needed to look like to actually fix it.

## Design Objective

The goal was not to automate hiring decisions or predict how employers behave — both would overstate what a single-operator, AI-assisted workflow can responsibly claim, and both were explicitly out of scope from the start. The actual goal was narrower and more useful: a repeatable framework for understanding what a role is actually asking for, assessing candidate-role alignment against direct evidence rather than impression, translating prior experience — including experience that doesn't map cleanly onto a job posting's vocabulary — into verifiable terms, prioritizing applications by expected value instead of convenience or recency, and preserving the reasoning behind each decision so it can eventually be measured against outcomes rather than just remembered as a vague sense of "it went well" or "it didn't."

## The Eight-Layer Architecture

**1. Opportunity Intake.** Captures a role as a discrete unit before analysis starts — job description, employer, location and work model, compensation where available, seniority, visa or residency constraints, deadline, recruiter contact.

**2. Role Decomposition.** Separates core responsibilities, required qualifications, preferred qualifications, tools and technical requirements, leadership expectations, domain knowledge, implied seniority signals, and potential disqualifiers — the layer that exists specifically to separate what a role actually requires from what its title implies.

**3. Candidate Evidence Mapping.** Maps each requirement to direct evidence, transferable evidence, a supporting project, its location in the resume, an assessed strength rating, an identified gap, and proposed positioning language. This is the core evidentiary layer — every claim of fit has to point to something specific.

**4. Employer and Market Research.** Assesses employer legitimacy, business model, organizational maturity, hiring signals, strategic fit, geographic feasibility, and identifiable risk — applying the same evidentiary standard to the employer side of the decision.

**5. Fit Assessment.** Separates capability fit, evidence fit, experience fit, seniority fit, domain fit, location fit, compensation fit, career-direction fit, and application-effort fit, so strength in one dimension can't mask weakness in another.

**6. Prioritization.** Classifies opportunities into Priority A (strong evidence and strategic fit), Priority B (credible fit with manageable gaps), Priority C (exploratory or low-probability), or Do Not Apply (material disqualifier or poor strategic value). This is the formalized version of a judgment call most job-seekers already make informally — the point of writing it down is that it can be applied consistently and reviewed later, instead of shifting quietly from one opportunity to the next based on mood or deadline pressure.

**7. Application Production.** Uses the analysis to inform resume selection and tailoring, summary positioning, bullet selection, keyword alignment, cover-letter emphasis, portfolio-link selection, and interview preparation. The analysis is meant to produce the material, not the other way around — a resume bullet exists because Layer 3 identified a piece of evidence worth surfacing, not because it sounded good in isolation.

**8. Outcome Learning.** The intended layer for tracking applications submitted, screening responses, recruiter contacts, interviews, rejections, time spent per application, response rate by category, resume version, and application channel — not yet populated with a consolidated dataset. This is the current bottleneck in the whole system: without it, the other seven layers describe a well-reasoned process, but there's no way yet to check whether that process actually correlates with better results. Closing this gap is the next priority, not refining the architecture further.

## Decision Logic

The assessment model deliberately doesn't collapse a hiring decision into one number. A composite score can hide a disqualifying constraint — an unmet visa requirement, for instance — behind an otherwise strong average, which is exactly the kind of false precision a structured system should be built to avoid, not reproduce with more decimal points.

Instead the model combines gating criteria, checked first and independent of any score, with nine dimensions scored separately rather than blended: role alignment (how closely core responsibilities match demonstrated experience), evidence strength (what proportion of requirements are backed by direct rather than transferable evidence), transferable-skill strength (how credible the translation actually is), employer attractiveness, geographic feasibility, compensation alignment, career-direction alignment, application effort relative to expected value, and strategic portfolio value — whether pursuing the role builds useful evidence regardless of the outcome. Each dimension carries a short written rationale, not just a number, and the whole assessment carries an explicit confidence level reflecting how much information was actually available when it was made.

A role that scores well on every dimension except an unmet hard requirement is still routed to Do Not Apply. That's a deliberate design choice: a single disqualifying fact can't be diluted by an otherwise strong average, no matter how good the rest of the fit looks on paper.

## Illustrative Assessment: AI Workflow Specialist

The architecture above is easier to evaluate with a worked example than as a list of layer descriptions. The one below shows how the layers combine into an actual apply-or-decline call.

*Constructed to show how the layers combine — not drawn from a saved application record.*

- **Requirements:** Designing structured AI-assisted workflows; translating ambiguous requests into repeatable process; documentation discipline; stakeholder communication.
- **Strongest alignment:** Workflow design and documentation discipline (direct evidence); communication and training background (direct evidence, transferable framing).
- **Material gap:** No documented enterprise-team deployment of an AI workflow at scale — experience is single-operator to date.
- **Recommended priority:** B — credible fit, with the team-scale gap addressed directly in the cover letter rather than concealed.
- **Confidence level:** Moderate, pending employer research on actual team structure and tooling.

## Human-AI Governance

AI supports job-description parsing, requirement classification, keyword extraction, draft comparison between resume and posting, employer-research synthesis, draft scoring, evidence-gap identification, and tailoring suggestions.

The human retains responsibility for determining career direction, verifying that cited evidence is accurate, deciding whether a transferable-skill claim is credible enough to make, assessing personal constraints, reviewing employer risk, approving every specific claim in application materials, rejecting AI-suggested language that overstates experience, and making the final apply-or-decline decision.

**Governing principle: AI can organize the evidence. It cannot authorize an unsupported claim.**

That boundary matters more than it might sound. It's easy for an AI-assisted drafting process to smooth a resume bullet into something slightly more impressive than the underlying evidence supports — a transferable skill quietly becomes direct experience, a self-directed project quietly becomes a team achievement. The workflow is designed so that every one of those upgrades has to be caught and approved by a human before it reaches an application, not waved through because it reads well.

## Current Limitations

The method has been used by a single operator, with no inter-rater or team-based validation. Outcome data — Layer 8 — has not been consolidated into a dataset, which means no claim about response rates, interview conversion, or efficiency gains relative to an unstructured approach can currently be supported. Labor-market conditions aren't controlled for. Employer decision processes aren't observable from the candidate side. Transferable-skill mapping is inherently subjective, particularly translating a military background into civilian technical-role language. Any future application sample will likely be small. Visa, residency, and geographic constraints affect viability independent of fit score. AI-assisted parsing can introduce interpretation errors that require human review to catch. No external validation of the scoring framework exists yet.

## Where This Stands

Hiring Intelligence reframes job searching as an evidence and decision problem instead of a volume problem. What's demonstrated so far is the architecture itself — a repeatable structure for decomposing roles, mapping evidence, and separating human judgment from AI-assisted synthesis. What it hasn't yet demonstrated is that this structure changes outcomes, or that it's operated consistently across a real, trackable set of opportunities.

That distinction matters more here than it would in most portfolio writeups, precisely because the subject is evidence discipline. It would be easy to describe the method glowingly and let the description itself stand in for proof that it works — but a case study that grades its own homework isn't practicing what it's arguing for. So the honest version of where this stands is: the architecture is done, it's been used informally in real decisions during this career transition, and the next real milestone isn't a better framework — it's a populated Layer 8. Applications with dates, resume versions actually sent, employer research actually written down, and whatever responses come back, good or bad, recorded rather than remembered. That's the record that will eventually say whether the structure was worth building.

The full methodology write-up — including the complete evidence-mapping framework, artifact inventory, evidence request ledger, and claim audit — is on GitHub: [**Read the full methodology and evidence record on GitHub.**](https://github.com/havmeaning/personal-ai-operating-system/blob/main/case-studies/HIRING_INTELLIGENCE_PROJECT.md).
