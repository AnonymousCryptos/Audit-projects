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
