# ThunderLoan — Proxies, Oracles & Lending Security Portfolio Project

## Overview
ThunderLoan is a lending-protocol security project focused on upgradeability, centralization risk, oracle manipulation, and storage correctness. It is ideal for demonstrating how smart contract risks expand when proxies and external pricing dependencies are involved.

## Why This Project Matters
This project touches several production-grade attack surfaces:
- Proxy initialization issues
- Storage collision risk
- Centralization and admin trust
- Upgrade safety
- Oracle and price manipulation
- Lending protocol assumptions

## Objectives
- Review the protocol architecture and trust boundaries
- Test initialization and upgrade flows
- Analyze storage layout safety
- Evaluate oracle-dependent pricing and borrowing logic

## Scope
Primary review areas:
- Proxy/deployment configuration
- Upgrade execution paths
- Storage layout assumptions
- Oracle integrations
- Borrow/lend accounting
- Privileged role design

## Security Themes
- Failure to initialize
- Storage collisions in upgradeable systems
- Unsafe or overly powerful admin controls
- Missing events for critical actions
- Bad upgrades and broken state transitions
- Oracle manipulation and pricing abuse

## What This Repository Shows
- Architecture review notes
- Upgrade and storage risk analysis
- Oracle manipulation writeups
- Lending exploit PoCs
- Practical mitigation recommendations

## Suggested Repository Structure
```text
ThunderLoan/
├── README.md
├── findings/
│   ├── H-01-oracle-manipulation.md
│   ├── H-02-storage-collision.md
│   └── M-01-centralization-risk.md
├── notes/
│   ├── upgradeability-review.md
│   └── oracle-review.md
├── poc/
│   ├── initialize-bug.t.sol
│   └── price-manipulation.t.sol
└── report/
    └── audit-report.md
```

## Key Learning Outcomes
- Upgradeable systems require storage discipline
- Initialization mistakes can become critical vulnerabilities
- Oracles are often the weakest link in lending systems
- Centralization is a security issue, not just a governance issue

## Run Locally
```bash
forge install
forge build
forge test
```

## Portfolio Value
This project demonstrates advanced audit skills across proxies, lending flows, oracles, and trust-boundary analysis.

## Disclaimer
This repository is for educational, research, and portfolio purposes only.
