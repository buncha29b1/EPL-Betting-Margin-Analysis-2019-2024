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
├── Final Project Code.Rmd          # Reproducible R/Quarto analysis
├── Final Project Code.html         # Rendered notebook (open in browser)
├── DA220_Final_Project_Report.pdf  # Full write-up
├── Final Project Proposal.pdf       # Original proposal & scope
└── README.md                        # (this file)
```

Data source: [Football-Data.co.uk](https://www.football-data.co.uk/englandm.php) (EPL season match odds, aggregated at match level).
