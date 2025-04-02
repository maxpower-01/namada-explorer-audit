# namada-explorer-audit 🟡

This repository tracks an open effort to audit and evaluate different Namada blockchain explorers. The aim is to compare their features and accuracy against reliable data sources, with the long-term goal of improving the quality and trustworthiness of Namada's ecosystem tools.

It's the first attempt at putting something like this together, and we’ll figure things out as we go. We’ll use branches to explore different parts of the project without overcommitting to any single structure right away.

## About This Audit

This project does not aim to promote or criticize any specific explorer, validator, or operator. The goal is to build a transparent, community-driven reference for understanding what data each explorer exposes—and how accurate and complete it is when compared to known sources.

This is not about ranking anyone. It’s about helping everyone, including end users and explorer operators, understand the current landscape and identify areas for improvement.

Every branch or report in this repository should clearly explain how to verify the data yourself. Our role here is to document, cross-check, and provide guidance—not to take sides.

We ❤️ all operators contributing to the Namada ecosystem. Running explorers is hard work, and every effort to make data accessible is valuable. This audit exists to support that work, not compete with it.

## What this project is based on

We use mainly CometBFT RPC as the main data source for comparison. It serves as the reference point for checking how accurate and complete the data shown in each explorer actually is. For now, we plan to rely on endpoints from well-known and active Namada operators.

More information about CometBFT can be found here:  
[https://github.com/cometbft/cometbft](https://github.com/cometbft/cometbft)

## What we’re comparing

Each explorer will be reviewed based on how well it supports the following core features:

* Blocks and Transactions - Includes block height, hash, timestamp, and transaction details like type, sender/receiver, fees, and amount.

* Accounts and Balances - Transparent balances, shielded pool data, and transaction history (including which transactions are shielded or not).

* Validators and Staking - Validator info such as address, voting power, commission, status, delegation amounts, and slashing history.

* Governance - Proposal metadata, voting progress, proposers, status, and whether the proposals passed or failed.

* Epochs - Current and historical epoch data, including validator changes and staking adjustments per epoch.

* Network Health - Basic uptime and performance data, block times, and missed blocks.

* Token and Supply Information - Total supply, circulating supply, and any inflation or issuance mechanisms.

* Shielded Transactions and Privacy Metrics - Volume of shielded vs transparent transactions, and trends in shielded pool activity (in a privacy-preserving way).

* IBC Transfers - Cross-chain transfers, including source/target chains, amounts, and channel statuses.

## How the repository is organized

Main branch:
- Contains this README and serves as the landing page for the project.

Branches:
- `data-validation` – raw RPC queries and results from trusted nodes.
- `explorer-[name]` – one branch per explorer being audited.
- `comparison-matrix` – summary views of how explorers stack up against each other.
- `scripts` – tools to automate comparisons or fetch data from RPC endpoints.

## Next steps

This audit is still in its early days. If you're working on Namada, running an explorer, or just want to help improve the ecosystem, you’re welcome to contribute. More structure will be added as we learn what works best.

You can also follow the discussion here:  
[https://forum.namada.net/t/request-audit-our-five-namada-explorers/1631](https://forum.namada.net/t/request-audit-our-five-namada-explorers/1631)
