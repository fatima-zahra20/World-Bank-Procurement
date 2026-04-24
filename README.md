
# 🌍 World Bank Loan Analysis — Project README

## Big Question
**Are World Bank loans actually worth it for developing countries?**

---

## Data Sources
| Table | Rows | Description |
|---|---|---|
| `contracts_clean` | 273,497 | Individual contracts awarded under each loan |
| `loans_clean` | 11,236 | Loan-level data — amounts, dates, repayment |
| `countries_clean` | 211 | Country metadata — income level, region, lending type |
| `education_clean` | 1,500 | Education indicators per country per year (2015-2025) |

---

## Table Relationships

## The Core Tension

By the end of this project we won't just have clean data — we'll have a **multi-angle verdict**
on whether these loans help or just create dependency and debt.


## Analysis Layers

### Layer 1 — The Money Trail
*Tables: contracts + countries*

> When a developing country gets a World Bank loan, does the money stay
> in the country or flow straight back out to foreign suppliers?

**Questions:**
1. What percentage of total contract value goes to **local vs foreign suppliers**?
2. Which **supplier countries** benefit the most from World Bank contracts?
3. Do **low income countries** get more foreign suppliers than high income ones?
4. Which **sectors** (education, infrastructure, health) attract the most foreign suppliers?
5. Is there a pattern between a country's **income level** and where its suppliers come from?

---

### Layer 2 — The Loan Itself
*Tables: loans + countries*

> Are loans actually being used well — and are the poorest countries
> ending up with more debt than benefit?

**Questions:**
1. What is the ratio of **disbursed vs original principal** — are loans being fully used?
2. Which countries have the highest **cancellation rates** — money borrowed but never used?
3. Which **income groups** carry the most debt relative to what they actually received?
4. What does the **repayment landscape** look like — how many loans are fully repaid vs still active vs cancelled?
5. Are **soft loan countries** (IDA/XDR) borrowing more than they can handle?

---

### Layer 3 — The Impact
*Tables: loans + education*

> Did World Bank education loans actually move the needle on
> enrollment and literacy — or did the money disappear without a trace?

**Questions:**
1. Did **primary and secondary enrollment** improve in countries that received education loans?
2. Which countries improved the **most vs least** on literacy after receiving loans?
3. Is there a **correlation** between total loan amount received and education improvement?
4. Did improvement happen **during the loan period** or only after?
5. Which **income group** saw the most education gains from loans?

---

## Limitations
- Education data covers only **50 out of 211 countries**
- Contracts date range is **2019-2026** — loans go back to 1961
- Missing education values are **honest reporting gaps**, not zeros
- `wb_contract_number` is not unique — multi-supplier consortiums exist

---

## Key Concepts
| Term | Meaning |
|---|---|
| **IDA** | World Bank's soft loan arm for poorest countries |
| **IBRD** | World Bank's market-rate loans for middle income countries |
| **XDR** | Special Drawing Rights — IMF reserve currency used for IDA loans |
| **Consortium** | Multiple suppliers sharing one contract |
| **Logical missingness** | Data missing for a real-world reason, not a data error |