# Task 4: Data Storytelling & Statistical Validation

**Internship:** Data Analytics Internship — ApexPlanet Software Pvt. Ltd.
**Timeline:** 16 Days
**Input:** Findings and datasets from Task 1 (Data Wrangling), Task 2 (EDA & BI), and Task 3 (Cohort Deep-Dive)

## Objective
To synthesize all analysis from Parts 1–3 into a compelling business narrative and use statistical methods to validate a key finding, delivering results in a stakeholder-ready presentation.

## Guiding Business Question
> Where should Superstore focus to grow profitable, repeatable revenue?

## Repository Structure
```
├── README.md
├── Task4_Storytelling_Hypothesis.ipynb    # Notebook: narrative + hypothesis test code
├── Task4_Report.docx                      # Written report: data story + hypothesis test summary
├── Superstore_Final_Presentation.pptx     # 12-slide stakeholder deck covering Tasks 1-4
└── images/                                # Chart exports (trend, region, cohort heatmap, hypothesis chart)
```

## 1. Data Story: Synthesis of Tasks 1–3
Each task answers a question raised by the one before it:

| Task | Question | Answer |
|---|---|---|
| Task 1 | Is the data trustworthy enough to analyze? | Yes — cleaned & structured 9,800 orders (2015–2018) |
| Task 2 | Where does revenue concentrate? | West/East regions, Consumer segment, Phones & Chairs |
| Task 3 | Why does it concentrate there? | Near-universal repeat buying (98.4% repeat rate), not new-customer spikes |
| Task 4 | Is the Consumer-segment lead just bigger baskets? | No (p = 0.56) — it's driven by order volume, not order size |

## 2. Hypothesis Testing

**H₀ (null):** There is no difference in average order value between Consumer and Corporate customers.
**H₁ (alternative):** Average order value differs between Consumer and Corporate customers.

**Method:** Welch's independent two-sample t-test on order-level Sales — Consumer (n=5,101) vs. Corporate (n=2,953).

| Metric | Value |
|---|---|
| Consumer mean order value | $225.07 |
| Corporate mean order value | $233.15 |
| t-statistic | -0.587 |
| p-value | 0.5575 |
| Significance threshold (α) | 0.05 |
| Conclusion | Fail to reject H₀ |

**Business conclusion:** No statistically significant difference in spending per order between segments. Consumer's revenue lead comes from order volume, not higher-value transactions — growth strategy should target acquisition and purchase frequency, not average basket size.

## 3. Recommendations
- **Invest in the South region** — lowest-performing region ($389K); a candidate for targeted marketing
- **Prioritize acquisition over retention tactics** — 98.4% repeat rate shows retention isn't the bottleneck
- **Double down on Phones & Chairs** — top two revenue sub-categories; expand assortment or promotions
- **Avoid over-indexing on segment-based pricing** — AOV difference between segments is not statistically significant

## 4. Presentation Deck Structure (12 slides)
1. Title
2. Objective & 4-task roadmap
3. Task 1 — Data Wrangling summary
4. Task 2 — Headline KPIs, yearly trend, region sales
5. Task 2 — Segment split & key insights
6. Task 2 — SQL business questions + top sub-categories
7. Task 3 — Cohort retention heatmap
8. Task 3 — LTV distribution & concentration
9. Task 4 — Hypothesis test (H₀, method, results, conclusion)
10. Task 4 — Data story synthesis (how each task builds on the last)
11. Recommendations
12. Thank you

