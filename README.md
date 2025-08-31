# ⚽ How Bookmakers Make Money? Betting Margins in the English Premier League (2019–2024)

**Authors:** Khoi Van · Harry Nguyen · Duc Bui  
**Course:** MATH/DA 220 — Final Project, Denison University

---

## 🔍 Overview
Bookmakers build a margin (“**overround**”) into match odds so the implied probabilities sum to a value larger than **100%**, guaranteeing profit regardless of outcome.  
This project analyzes **five EPL seasons (2019–20 → 2023–24)** to understand:

- Do margins differ by **match result** (home/draw/away)?
- Are margins higher when the **home team is favored**?
- Have margins **changed over time**?
- How much of the margin can be explained by the **odds structure** itself?

---

## 🗂 Project Structure

```
.
├── Data/
│   ├── 19-20.csv
│   ├── 20-21.csv
│   ├── 21-22.csv
│   ├── 22-23.csv
│   └── 23-24.csv
|   .gitignore
├── Final Project Code.Rmd          # Reproducible R/Quarto analysis
├── Final Project Code.html         # Rendered notebook (open in browser)
├── DA220_Final_Project_Report.pdf  # Full write-up
├── Final Project Proposal.pdf       # Original proposal & scope
└── README.md                        # (this file)
```

Data source: [Football-Data.co.uk](https://www.football-data.co.uk/englandm.php) (EPL season match odds, aggregated at match level).

## 🛠 Methodology

**Metric (overround / margin)**  
For each match we compute:

```
margin = 1/AvgH + 1/AvgD + 1/AvgA − 1
```

where `AvgH/AvgD/AvgA` are market-average decimal odds for home/draw/away.

**Statistical workflow**
- **Data prep:** combine five season CSVs; clean types; derive favorite/underdog flags.
- **Hypothesis tests:**  
  - Chi-square tests for margin category (High/Low) vs. result and vs. season.  
  - Two-sample t-tests for favorite vs. underdog, and 2019–20 vs. 2023–24.
- **Modeling:** OLS regression of margin on transformed odds indices + favorite flag; diagnostics via residual plots and Q-Q.

**Tech stack**  
R (tidyverse, dplyr, ggplot2, lubridate). Analysis scripted in an R Markdown/Quarto notebook.

---

## 🔁 Reproducibility

**Quick view**  
- Open `Final Project Code.html` in your browser for the rendered results.

**Run locally (R)**
1. Open `Final Project Code.Rmd` in RStudio/VS Code.
2. Install packages: `tidyverse`, `dplyr`, `ggplot2`, `lubridate`.
3. Click **Render** (or Knit) to reproduce all tables/figures.

---

## 📈 Key Findings (summary)
- **No evidence** that margins depend on the final match result (home/draw/away).  
- **Strong season effects:** margin distributions differ across seasons.  
- **Favorite vs. underdog:** no meaningful difference in average margins.  
- **Margins tightened** over the sample window (later seasons slightly lower).  
- **Low explanatory power** from odds-only linear models (small R²): margins vary more with market conditions than simple odds transformations.

*(See the PDF report for full stats tables and figures.)*

---

## 📚 References
- [Football-Data.co.uk](https://www.football-data.co.uk/englandm.php)
- [Birches Health. 2024. The consolidation of the sports betting industry.](https://bircheshealth.com/resources/consolidation-sports-betting-industry)
- [Hegarty T, Whelan K. 2024. Comparing two methods for testing the efficiency of sports betting markets. UCD Centre for Economic Research Working Paper Series WP24/03.](https://www.ucd.ie/economics/t4media/WP24_03.pdf)

---

## 📬 Contact
- Khoi Van: van_k1@denison.edu
- Harry Nguyen: nguyen_h11@denison.edu
- Duc Bui: bui_d3@denison.edu
