# Commission Distribution Analysis

## Overview
Data analysis project to reconcile and correctly distribute insurance commissions across agents using Python and Pandas.

The project focuses on resolving commission misallocations caused by fragmented client-agent mappings, especially cases involving a lead agent holding clients that belong to other agents.

## Business Problem
Commission data was inconsistent due to:
- Lead agent commissions including clients belonging to other agents
- Risk of duplicated or incorrect commission payouts
- Manual reconciliation consuming excessive time

A reliable and auditable process was required to correctly assign commissions to the appropriate agents.

## Data Sources
- **Commission records**: Transaction-level commission data per client
- **Clean master list**: Validated client-to-agent mapping used as the source of truth

## Analysis Process
- Performed integrity checks on commission totals and client counts
- Identified clients present in commission data but missing from the master list
- Isolated lead-agent cases requiring manual validation
- Removed duplicated client records from the master list
- Reconciled commission data using a many-to-one merge validation
- Ensured total commission amounts remained unchanged after reconciliation

## Outputs
- Clean commission dataset with correct agent assignments
- Commission summary by agent
- Validation checks confirming:
  - No duplicated clients
  - No lost or duplicated commission values

## Tools
- Python
- Pandas
- Jupyter Notebook

## Results
- Accurate commission distribution across all agents
- Prevention of duplicated or incorrect commission payouts
- Reliable monthly commission reconciliation process

## Business Impact
- Reduced manual review time for lead-agent cases
- Improved trust in commission reporting
- Enabled faster and safer commission settlements
