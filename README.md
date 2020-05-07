# Opyn Analysis
An analysis of Opyn's user segments

## Data Sources

### 1. oToken Transactions
Based on the [Opyn: All Accounts 2](https://explore.duneanalytics.com/queries/3043) query on Dune Analytics, which I created by modifying the [Opyn: Notional Volume Graph](https://explore.duneanalytics.com/queries/2301) query. Results were exported on 4/30/20.

### 2. Opyn Vaults
Scraped from [Opyn Monitor](Opynmonitor.xyz) on 5/3/20

## Analysis
Analysis looked primarily at distributions of value (transactions and vaults) and derived clusters of transacting addresses and clusters of vault owners.

The following transacting addresses were removed from the transaction analysis
- 0x076c95c6cd2eb823acc6347fdf5b3dd9b83511e4 -- Opyn's address
- 0x39246c4f3f6592c974ebc44f80ba6dc69b817c71 -- one of Opyn's Options Exchange contracts, which masked the actual user addresses. Transactions by this address were included in value distribution analysis but excluded from transaction address clustering.

The following vault owners were removed from the vault analysis
- 0x076c95c6cd2eb823acc6347fdf5b3dd9b83511e4 -- Opyn's address
- any vaults from expired option series
- any vaults with 0 oToken outstanding balance

See the [jupyter notebook](./Opyn_segments.ipynb) for details and results.

## Write-up and Recommendations

My full write-up and recommendations can be found in this [Google Doc](https://docs.google.com/document/d/1Rk_hOs26xTdrL_TAt007v0UNUbZVDpuY0fdBEhV4y7U/)
