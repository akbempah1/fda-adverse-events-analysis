# FDA Adverse Event Reporting System (FAERS) Analysis

![Python](https://img.shields.io/badge/Python-3.10-blue) ![pandas](https://img.shields.io/badge/pandas-2.0-green) ![API](https://img.shields.io/badge/Data-FDA%20FAERS%20API-red) ![matplotlib](https://img.shields.io/badge/matplotlib-3.7-orange)

**Analyzing millions of FDA adverse event reports to identify high-risk drugs, patient demographic patterns, and the gap between clinical trial efficacy and real-world performance.**

> Author: Afriyie Karikari Bempah, PharmD | [LinkedIn](https://linkedin.com/in/afriyiekarikaribempah) | [GitHub](https://github.com/akbempah1)

---

## Overview

This project queries the FDA's Adverse Event Reporting System (FAERS) via the OpenFDA API to perform real-time pharmacovigilance analysis. Rather than working from a static dataset, all data is pulled live — demonstrating API integration skills alongside clinical pharmacy domain expertise.

The FDA FAERS database contains millions of voluntary adverse event reports submitted by patients, healthcare professionals, and manufacturers since 1969.

---

## Key Findings

| Finding | Insight |
|---|---|
| **Zantac has a 95% serious event rate** | Carcinogen (NDMA) contamination signal was visible in reporting data — confirmed by 2020 market withdrawal |
| **"Drug Ineffective" is the #1 reaction** | Real-world drug performance consistently falls short of clinical trial results |
| **Women report 60% of adverse events** | Sex-based differences in drug response are underrecognized in clinical practice |
| **Adults + elderly = 95%+ of all reports** | Pediatric adverse event surveillance remains a critical gap |
| **High report volume ≠ high risk** | Humira leads total reports but has a 49% serious rate vs Zantac's 95% |

---

## Analyses

1. **Top 20 Drugs by Adverse Event Volume** — Identifies most-reported drugs with data quality observations
2. **Serious Adverse Event Rate** — Separates high-volume reporting from high-severity risk
3. **Patient Demographics** — Sex and age group breakdown across all reports
4. **Top 20 Adverse Reactions** — What is actually happening to patients

---

## Technical Highlights

- **Live API integration** — data pulled directly from OpenFDA, no static CSV
- **JSON response parsing** — handling nested API response structures
- **Data quality identification** — duplicate drug name entries flagged and documented

---

## How to Run

```bash
git clone https://github.com/akbempah1/fda-adverse-events-analysis.git
pip install pandas matplotlib requests jupyter
jupyter notebook fda_adverse_events.ipynb
```

No API key required. OpenFDA is publicly accessible.

---

## Relationship to Project 1

This project extends the [Medicare Drug Spending Analysis](https://github.com/akbempah1/medicare-drug-spending-analysis) — several high-spend drugs (Humira, Eliquis, Xarelto, Pantoprazole) appear in both datasets, connecting cost burden to safety burden.

---

**Data Source:** FDA Adverse Event Reporting System via [OpenFDA API](https://api.fda.gov)  
*Analysis and interpretations are independent and not affiliated with the FDA.*
