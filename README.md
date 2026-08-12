# 📊 Course Market Intelligence — Command Center

**What should an AI-first learning company build & sell next?**
This project analyses **4,569 real online courses** (Coursera + Udemy) covering **92.4 million learners** to identify high-demand, high-quality, under-supplied training domains — the kind of market intelligence a Solution Expert would run before recommending a new training product.

> Built by **Sairaj Sandip Kashid** for the TechnoEdge Learning Services — *Solution Expert Intern* application.

---

## 🔥 The problem it solves

A learning-solutions company like TechnoEdge has to constantly decide **which new training programs to invest in**. Guessing is expensive. This dashboard turns raw public course data into a prioritised, evidence-backed recommendation:

> *"Build training programs in Software Development, Data Science, AI & Machine Learning and Business & Management — these show the highest demand-to-supply opportunity scores."*

## 📈 What's inside (5 interactive views)

| Tab | What it shows |
|-----|---------------|
| **Overview** | KPIs, demand-by-domain bar chart, difficulty mix donut, top providers, certificate types |
| **Domain Demand** | Demand-vs-supply combo chart, avg rating by domain, full domain leaderboard table |
| **Opportunity Matrix** | Bubble chart (demand × supply × quality) with a transparent opportunity-score formula |
| **Pricing & Trends** | Price-vs-enrolment bands, course-launch growth 2012–2017, Udemy subject categories |
| **Recommendations** | Ranked opportunity cards + a "mega-courses to learn from" top-15 table |

Every chart has **hover tooltips** with real figures.

## 🧮 The opportunity score (transparent, not a black box)

```
Opportunity Score = (normalised demand) × (quality factor from avg rating)
                    × (0.4 + 0.6 × (1 − normalised supply)) × 100
```
More learners = more demand · higher ratings = proven appetite · fewer existing courses = less competition.

## 📦 Real data sources

| Source | Records | Fields used |
|--------|---------|-------------|
| Coursera course catalogue (scraped) | 891 courses | title, organisation, certificate type, rating, difficulty, enrolments |
| Udemy courses dataset | 3,678 courses | price, subscribers, reviews, lectures, level, duration, year, subject |

All figures are **computed in Python** from the raw CSVs — no manual numbers.

## 🛠️ How it's built

- **Pure HTML + CSS + vanilla JavaScript** — zero external libraries, zero CDNs.
- **Custom hand-drawn SVG charts** (bar, donut, line, bubble) with a warm terracotta/amber palette.
- Runs anywhere: open `index.html` directly, or host on GitHub Pages.
- Data processing: `../process_data.py` (Python stdlib only — `csv`, `json`, `re`, `collections`).

## ▶️ Run it

```bash
# Option 1 — just open the file
open index.html

# Option 2 — local server
python3 -m http.server 8000
# visit http://localhost:8000
```

## 🗂️ Files

```
index.html              # the full interactive dashboard (self-contained)
../data/                # raw real datasets (CSV)
../process_data.py      # Python script that turns raw CSVs into the embedded JSON
```

## 💡 Why this impresses

It demonstrates the exact Solution-Expert loop: **analyse a business problem → use real data → produce clear recommendations → present it beautifully.** And it's domain-aligned — it speaks directly to TechnoEdge's learning business, not a generic dataset.

---
*Warm-coloured · hand-crafted · real data · zero dependencies*
