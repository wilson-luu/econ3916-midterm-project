# Do Higher Tariffs Go With Less Trade? Average Applied Import Tariffs and Trade Openness Across Countries, 2000–2021

## Research Question
Across countries from 2000 to 2021, how much lower is trade openness (natural log of exports plus imports as a percent of GDP) associated with higher average applied import tariffs (simple mean, all products, %), holding country size, natural-resource dependence, lagged income, and country and year fixed effects constant?

## Headline Finding
Using a two-way fixed-effects OLS panel model across **2,841 country-years covering 173 economies (2000–2021)** with country-clustered standard errors, a **1 percentage point higher average applied tariff rate is associated with trade openness that is 0.27% lower** (`−0.0027` log points, country-clustered SE `0.0037`, 95% CI `−0.99%` to `+0.45%`, `p = 0.4563`, `R² = 0.9258`). 

While the raw pooled relationship without fixed effects is strongly negative (`−0.0328`, or roughly `−3.3%` per percentage point), adding country and year fixed effects shrinks the estimate tenfold and its confidence interval straddles zero. Because reverse causality (countries cutting tariffs alongside trade agreements) and unobserved confounders (such as non-tariff barriers) remain open, this estimate is a **conditional association**, not a causal effect; the hypothesis is neither supported nor rejected.

## Data Source & Provenance
* **Source:** World Bank, *World Development Indicators (WDI)* via DataBank  
* **URL:** https://databank.worldbank.org/source/world-development-indicators  
* **Download Date:** 2026-11-01  
* **Series Downloaded (217 economies, 1999–2021):**
  * `NE.TRD.GNFS.ZS` — Trade (% of GDP)
  * `TM.TAX.MRCH.SM.AR.ZS` — Tariff rate, applied, simple mean, all products (%)
  * `SP.POP.TOTL` — Population, total
  * `NY.GDP.TOTL.RT.ZS` — Total natural resources rents (% of GDP)
  * `NY.GDP.PCAP.KD` — GDP per capita (constant 2015 US$)
* **Notes:** 1999 is used solely to build the one-year lag of log real GDP per capita for 2000. Twelve zero-trade observations for Venezuela (2000–2011) are set to missing before taking natural logs. Missingness in tariffs is classified as MAR conditional on observed country size and median income.

## Repository Contents
* `project-data.csv` — Raw World Bank WDI CSV export (1,085 data rows × 27 columns, wide format).
* `midterm-starter.ipynb` — Complete reproducible analysis notebook producing all tables, figures, diagnostics, and the `REPORT_NUMBERS` verification cell.
* `project-report.pdf` — Final written report and appendix.
* `README.md` — Project overview and reproduction instructions.

## How to Reproduce
Open the Colab link and select **Runtime › Restart and run all**. The notebook automatically loads `project-data.csv` directly from the public GitHub repository.
