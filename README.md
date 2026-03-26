# Smart Contract Audit Reports

This repository contains a collection of smart contract audit reports I have worked on as an individual auditor or contributor.

It reflects my approach to auditing, the type of issues I focus on, and the level of depth I aim for in reviews.

## Background

I have been working as a blockchain developer since 2018 on EVM-based systems.

My experience includes building and reviewing:

- DeFi protocols
- NFT marketplaces
- Token systems and custom contract logic

Over time, I have moved deeper into smart contract security, with a strong focus on identifying logic flaws, broken assumptions, and real world exploit paths rather than surface-level issues.

## Audit Philosophy

I treat audits as a problem of understanding intent versus actual behaviour.

Most critical issues do not come from syntax mistakes, but from gaps between what the system is expected to do and what it actually allows under edge conditions.

My focus is on:

- Breaking assumptions
- Tracking state transitions across flows
- Identifying trust boundaries and how they can fail
- Looking for economically viable attack paths

The goal is not just to find issues, but to understand how they can realistically be exploited.

## Audit Process

### 1. Context and Requirements Review
I start by gathering all relevant materials including the codebase, requirement documents, and any supporting context provided by the team.

I go through the requirements to understand the intended behaviour of the system before looking at the implementation. This helps in identifying gaps between expected and actual behaviour later in the audit.

### 2. Initial Review
I go through the full codebase to understand architecture, module interactions, and intended behaviour. This sets the baseline for deeper analysis.

### 3. Manual Analysis
This is the core of my process.

I perform a line by line review with focus on:
- State transitions
- Access control boundaries
- Input validation
- Cross function and cross contract interactions
- Edge cases that break expected invariants

### 4. Tool Assisted Checks
I use auditing tools to complement manual review, mainly to surface patterns such as:
- Reentrancy risks
- Unsafe external calls
- Known vulnerability patterns

Tools are used as a signal, not as a source of truth.

### 5. Issue Validation
All potential issues identified through manual review, tools, or other analysis are validated before being reported.

I attempt to reproduce findings in a local environment wherever applicable to confirm impact and rule out false positives. Only confirmed issues are included in the report.

### 6. Interim Report
Findings are shared in an interim report with:
- Clear description of the issue
- Impact assessment
- Suggested remediation

This allows the team to start fixing issues early.

### 7. Fix Review
After the team responds, I review both code changes and any explanations provided.

Issues may be:
- Fixed in code
- Addressed through valid design explanations

If the reasoning is sound and aligns with the intended behaviour, the issue is marked accordingly.

### 8. Final Report
The final report is an updated version of the initial findings.

Each issue is marked with its final status, such as fixed or acknowledged, along with any relevant notes from the review process.

No separate report is created, the original report is amended to reflect the final state.
This ensures the audit trail is clear and complete.

## Report Structure

Each report typically includes:

- Scope
- System overview
- Methodology
- Detailed findings
- Severity classification
- Recommendations

## Severity Classification

- **Critical**  
  Leads to direct loss of funds or full protocol compromise

- **High**  
  Breaks core functionality or creates strong attack vectors

- **Medium**  
  Impacts assumptions, edge cases, or specific flows

- **Low**  
  Minor inconsistencies or improvements

- **Informational**  
  Observations related to code quality or clarity

## Repository Scope

This repository contains only audit reports.

No source code is included. Each report corresponds to the specific version of the codebase that was reviewed during the audit.

## Disclaimer

All findings are based on the state of the code at the time of the audit(commit ID is mentioned on which audit was conducted in the audit report, where the git repo is provided).

Projects may have changed or fixed issues after the audit was completed. Always refer to the latest version of the code for the current behaviour.

## Responsible Disclosure

All vulnerabilities were disclosed to the respective teams before being made public.

Sensitive issues are only included after confirmation or resolution.
