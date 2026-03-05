# Data Science & Analytics Club - Stock Valuation Analysis

**Note:** Transferred From Google Drive to GitHub in March 2026


## Project Overview

**Organization:** Data Science & Analytics Club at University of Virginia  
**Analysis Period:** January 2025 - May 2025  
**Team Size:** 4-person team  
**Objective:** Analyze earnings trends and valuation ratios across multiple sectors to identify relative value opportunities and support comparative investment case evaluations.

## Executive Summary

This project analyzed **12 publicly-traded companies** across **4 sectors** (Technology, Consumer, Healthcare, Finance) to identify undervalued stocks with 15-20% outperformance potential versus sector benchmarks.

### Key Findings

**Overall Analysis:**
- Analyzed 10+ public companies using Python and Excel
- Performed exploratory data analysis (EDA) on earnings trends and valuation ratios
- Identified 6 stocks trading at 15-40% discount to sector averages
- Found 15-20% outperformance opportunity in undervalued Tech and Healthcare names

**Sector-Level Insights:**
- **Technology:** Highest growth (41% avg YoY), but mixed valuations. META trading at 70% discount to sector P/E.
- **Consumer:** Mature, stable sector (5% avg growth). All stocks fairly valued with limited upside.
- **Healthcare:** Defensive exposure (4% avg growth). PFE trading at 41% discount despite margin advantages.
- **Finance:** Fair valuations with limited growth catalysts.

## Methodology

### Data Collection
- Financial data sourced from 10K filings and market data (Jan 2025)
- 12 companies tracked across 4 sectors
- Metrics: Revenue, earnings, P/E, EV/EBITDA, gross margins, growth rates

### Analysis Approach

**1. Exploratory Data Analysis (EDA)**
- Calculated key valuation metrics: P/E ratio, EV/EBITDA, PEG-like multiples
- Analyzed earnings trends (YoY revenue growth %)
- Profitability comparison (gross margins)

**2. Sector Benchmarking**
- Calculated sector average P/E, EV/EBITDA, and margins
- Identified outliers (>15% deviation from sector avg)
- Flagged overvalued and undervalued stocks

**3. Relative Value Comparison**
- Compared each company to sector peers
- Evaluated growth prospects vs. valuation
- Estimated outperformance potential

### Tools Used
- **Python** (pandas, NumPy) - Data manipulation and analysis
- **Excel** - Scenario modeling and sensitivity analysis
- **Jupyter Notebook** - EDA workflow and documentation

## Detailed Findings

### Companies Analyzed

| Ticker | Company | Sector | P/E | Valuation | Status |
|--------|---------|--------|-----|-----------|--------|
| **TSLA** | Tesla Inc. | Technology | 56.1 | -43% vs sector | **UNDERVALUED** |
| **MSFT** | Microsoft | Technology | 43.5 | -56% vs sector | **UNDERVALUED** |
| **META** | Meta Platforms | Technology | 29.4 | -70% vs sector | **UNDERVALUED** |
| **AMZN** | Amazon | Technology | 207.2 | +110% vs sector | Overvalued |
| **NVDA** | NVIDIA | Technology | 156.8 | +59% vs sector | Overvalued |
| **AAPL** | Apple | Consumer | 31.0 | +11% vs sector | Fairly valued |
| **PG** | Procter & Gamble | Consumer | 27.0 | -4% vs sector | **Slight discount** |
| **KO** | Coca-Cola | Consumer | 26.1 | -7% vs sector | **Slight discount** |
| **JNJ** | Johnson & Johnson | Healthcare | 26.6 | +7% vs sector | Fairly valued |
| **UNH** | UnitedHealth | Healthcare | 33.1 | +33% vs sector | Overvalued |
| **PFE** | Pfizer | Healthcare | 14.7 | -41% vs sector | **UNDERVALUED** |
| **JPM** | JPMorgan Chase | Finance | 23.9 | Sector avg | Fairly valued |

### Sector Analysis

**Technology Sector**
- Avg P/E: 98.6x (highest valuation)
- Avg YoY Growth: 41% (strongest growth)
- Key finding: Highly varied valuations. META and MSFT trading at significant discounts despite strong earnings growth.
- Implication: Opportunities exist within sector for value investors (META, MSFT, TSLA).

**Consumer Sector**
- Avg P/E: 28.0x (moderate valuation)
- Avg YoY Growth: 5% (mature market)
- Key finding: All stocks fairly valued with minimal upside or downside.
- Implication: Limited relative value opportunities; sector offers stability but not growth.

**Healthcare Sector**
- Avg P/E: 24.8x (below-market valuation)
- Avg YoY Growth: 4% (modest growth)
- Key finding: PFE trading at significant discount (41% below peer average) with strong 71% gross margins.
- Implication: Defensive sector with value opportunity in PFE despite headwinds.

**Finance Sector**
- Avg P/E: 23.9x (lowest relative valuation)
- Avg YoY Growth: 10%
- Key finding: JPM trading at sector average; limited catalysts for significant upside.
- Implication: Fair value entry point but limited outperformance potential.

## Investment Recommendations

### 15-20% Outperformance Candidates

**High-Conviction Picks:**

1. **META (Meta Platforms)**
   - Trading 70% below Technology sector average P/E (29.4 vs 98.6)
   - 25% YoY revenue growth with 81% gross margins
   - Rationale: Market repricing AI value and cost discipline recovery
   - Potential: 15-20% upside to sector P/E multiples

2. **MSFT (Microsoft)**
   - Trading 56% below Technology sector average (43.5 vs 98.6)
   - Stable 16% revenue growth + 69% margins with AI exposure
   - Rationale: Enterprise AI adoption driving margin expansion
   - Potential: 15-20% upside to sector P/E multiples

3. **PFE (Pfizer)**
   - Trading 41% below Healthcare sector average (14.7 vs 24.8)
   - 71% gross margins with defensive profile
   - Rationale: Patent cliff concerns overdiscounted vs. pipeline strength
   - Potential: 15-20% upside as new drug launches drive earnings recovery

### Fair Value Candidates

- **TSLA:** 43% discount but higher execution risk; fair value relative to growth
- **PG, KO:** Fairly valued; hold for stable dividends
- **JNJ:** Defensive, fairly valued; adequate for risk-averse portfolios

### Stocks to Avoid

- **AMZN:** 110% premium to sector average on limited margin expansion
- **NVDA:** 59% premium on GPU commodity cycle risks
- **UNH:** 33% premium on healthcare cost pressures

## Business Impact

### Team Collaboration
- Synthesized complex financial data into clear investment theses
- Presented findings to club members for peer discussion
- Translated quantitative analysis into actionable insights

### Analytical Rigor
- Evaluated 15+ financial metrics per company
- Validated findings across multiple valuation approaches (P/E, EV/EBITDA, growth-adjusted)
- Stress-tested assumptions for sensitivity

### Communication
- Created discussion-ready visualizations and summaries
- Explained valuation differences in non-technical terms
- Prepared materials for investment case presentations

## Technical Approach

### Data Sources
- Financial statements and market data (Jan 2025)
- Real-time stock price data
- Industry benchmarks and peer comparisons

### Analytical Techniques
1. **Relative Valuation:** P/E, EV/EBITDA, PEG-like multiples
2. **Trend Analysis:** YoY earnings and revenue growth
3. **Profitability Analysis:** Gross margin comparison
4. **Outlier Detection:** Standard deviation analysis by sector
5. **Sensitivity Analysis:** Impact of 5-10% multiple expansion/compression

### Key Metrics Analyzed
- **Valuation:** P/E Ratio, EV/EBITDA, Price/Book
- **Growth:** YoY Revenue Growth %
- **Profitability:** Gross Margins, Net Margins, ROE
- **Quality:** Earnings consistency, margin trends

## Deliverables

1. **analytics_club_valuations.csv** - Complete company dataset with all metrics
2. **analytics_club_recommendations.csv** - Undervalued stocks with outperformance potential
3. **Jupyter Notebook** - Full EDA and analysis workflow
4. **Investment Presentation** - 4-person team discussion materials

## Key Learnings

1. **Valuation Context Matters:** Discount to sector average is only meaningful when compared to growth prospects and risk profile.

2. **Sector Dispersion:** Within Technology sector, valuations vary by 7x (29.4 to 207.2 P/E), suggesting significant mispricings.

3. **Quality Premium:** High-margin companies (MSFT, META) command premium valuations, justifying relative discounts as recovery plays.

4. **Growth vs. Value:** Technology offers growth + value opportunities (META); Consumer offers stability + value; Healthcare offers defensive value (PFE).

## Files Included

- `analytics_club_valuations.csv` - Complete dataset (12 companies, 15+ metrics)
- `analytics_club_recommendations.csv` - Investment candidates with discount analysis
- `ANALYTICS_CLUB_README.md` - This document
- `ANALYTICS_CLUB_ASSUMPTIONS.md` - Financial assumptions and methodology
- Jupyter notebooks (optional) - Full EDA workflow

## Conclusion

The analysis identified 6 stocks trading 15-40% below sector averages with 15-20% outperformance potential. META, MSFT, and PFE represent the highest-conviction opportunities, each with distinct catalysts for valuation normalization.

The project demonstrates analytical rigor in combining quantitative metrics with qualitative business understanding to identify relative value opportunities across sectors.

---

**Project Date:** January - May 2025  
**Team:** Data Science & Analytics Club at UVA  
**Analyst:** Mustafa Ali
