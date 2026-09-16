# Risk Register: Bank Scenario

## Operational Environment

The bank is located in a coastal area with low crime rates. Many people and systems handle the bank's data — 100 on-premise employees and 20 remote employees. The customer base includes 2,000 individual accounts and 200 commercial accounts. The bank's services are marketed by a professional sports team and ten local businesses in the community. Strict financial regulations require the bank to secure its data and funds, including maintaining enough cash available each day to meet Federal Reserve requirements.

## Risk Register

| Asset | Risk(s) | Description | Likelihood | Severity | Priority |
|---|---|---|---|---|---|
| Funds | Business email compromise | An employee is tricked into sharing confidential information. | 2 | 2 | 4 |
| Funds | Compromised user database | Customer data is poorly encrypted. | 2 | 3 | 6 |
| Funds | Financial records leak | A database server of backed-up data is publicly accessible. | 3 | 3 | 9 |
| Funds | Theft | The bank's safe is left unlocked. | 1 | 3 | 3 |
| Funds | Supply chain disruption | Delivery delays due to natural disasters. | 1 | 2 | 2 |

**Notes:** all the risks listed show that security is currently poor — the bank can be compromised because of this weak physical and virtual security, which could lead to a catastrophic outcome for the company.

### Scoring Reference

- **Asset** — the asset at risk of being harmed, damaged, or stolen
- **Risk(s)** — a potential risk to the organization's information systems and data
- **Description** — a vulnerability that might lead to a security incident
- **Likelihood** — score from 1–3 for the chances of a vulnerability being exploited (1 = low, 2 = moderate, 3 = high)
- **Severity** — score from 1–3 for the potential damage the threat would cause to the business (1 = low, 2 = moderate, 3 = high)
- **Priority** — how quickly a risk should be addressed, calculated as Likelihood × Severity

### Sample Risk Matrix

| | Low (1) | Moderate (2) | Catastrophic (3) |
|---|---|---|---|
| **Certain (3)** | 3 | 6 | 9 |
| **Likely (2)** | 2 | 4 | 6 |
| **Rare (1)** | 1 | 2 | 3 |
