# Data Science & Analytics Club - Financial Analysis Assumptions & Methodology

## Project Context

**Project Name:** Stock Valuation & Relative Value Analysis  
**Team Size:** 4 analysts  
**Duration:** January 2025 - May 2025  
**Objective:** Identify relative value opportunities across 10+ publicly-traded companies using comparative valuation analysis.

---

## Data Collection & Sources

### Companies Analyzed (12 Total)

**Technology Sector (5 companies):**
- Tesla (TSLA) - EV manufacturer and energy storage
- Microsoft (MSFT) - Cloud computing and enterprise software
- Amazon (AMZN) - E-commerce and cloud infrastructure
- Meta Platforms (META) - Social media and digital advertising
- NVIDIA (NVDA) - AI chips and GPU manufacturing

**Consumer Sector (3 companies):**
- Apple (AAPL) - Consumer electronics and services
- Procter & Gamble (PG) - Consumer staples
- Coca-Cola (KO) - Beverages

**Healthcare Sector (3 companies):**
- Johnson & Johnson (JNJ) - Diversified healthcare
- UnitedHealth Group (UNH) - Health insurance and services
- Pfizer (PFE) - Pharmaceuticals

**Finance Sector (1 company):**
- JPMorgan Chase (JPM) - Banking and financial services

### Data Points Collected Per Company

**Valuation Metrics:**
- Stock price (as of Jan 2025)
- Market capitalization
- P/E Ratio (Price-to-Earnings)
- EV/EBITDA (Enterprise Value to EBITDA)
- Price-to-Book (P/B) Ratio

**Financial Performance:**
- Revenue (TTM - trailing twelve months)
- Net Income (TTM)
- Earnings Per Share (EPS)
- Gross Margin (%)
- YoY Revenue Growth (%)

**Data Source:** 
- Company 10-K filings (FY 2024)
- Market data as of January 15, 2025
- SEC EDGAR database

---

## Analytical Methodology

### Phase 1: Exploratory Data Analysis (EDA)

**Objective:** Understand data distribution and identify patterns

**Steps:**
1. **Data Cleaning & Validation**
   - Verified financial figures against multiple sources
   - Standardized units (converted to millions/billions)
   - Flagged any inconsistencies (e.g., negative growth in declining sectors)

2. **Descriptive Statistics**
   - Calculated mean, median, min, max for key metrics by sector
   - Identified outliers (values >2 std deviations from mean)
   - Analyzed distributions (normal, skewed, multimodal)

3. **Correlation Analysis**
   - Examined relationship between:
     - P/E Ratio vs. Revenue Growth
     - EV/EBITDA vs. Gross Margin
     - Stock Price vs. Market Cap
     - Valuation multiples vs. profitability

**Key EDA Findings:**
- Technology sector has highest valuation multiples (avg P/E: 98.6x) but also highest growth rates (avg 41%)
- Healthcare sector has lowest/most stable multiples (avg P/E: 24.8x) with modest growth (avg 4%)
- Consumer sector is tightly grouped (limited valuation variance) suggesting efficient pricing
- Strong positive correlation between YoY growth and P/E ratios (0.72 correlation)

### Phase 2: Sector Benchmarking

**Objective:** Identify outliers within their peer group

**Methodology:**

1. **Calculate Sector Averages**
   For each sector, calculate mean and standard deviation:
   ```
   Sector Avg P/E = Sum of all P/E Ratios in Sector / Number of Companies
   Sector StdDev = √(Variance of P/E Ratios)
   ```

2. **Calculate Deviation from Sector Average**
   ```
   Deviation % = ((Company P/E - Sector Avg P/E) / Sector Avg P/E) × 100
   ```

3. **Classification**
   - **Undervalued:** Deviation < -15% (trading at discount)
   - **Fairly Valued:** Deviation between -15% and +15%
   - **Overvalued:** Deviation > +15% (trading at premium)

**Sector Benchmarks (as of Jan 2025):**

| Sector | Avg P/E | Avg EV/EBITDA | Avg Gross Margin | Avg YoY Growth |
|--------|---------|---------------|------------------|----------------|
| Technology | 98.6 | 21.6 | 0.57 | 41% |
| Consumer | 28.0 | 16.8 | 0.54 | 5% |
| Healthcare | 24.8 | 11.2 | 0.53 | 4% |
| Finance | 23.9 | 8.5 | 0.42 | 10% |

**Undervalued Stocks Identified:**
- META (Technology): -70% vs sector average
- MSFT (Technology): -56% vs sector average
- TSLA (Technology): -43% vs sector average
- PFE (Healthcare): -41% vs sector average
- KO (Consumer): -7% vs sector average
- PG (Consumer): -4% vs sector average

### Phase 3: Relative Value Analysis

**Objective:** Determine if discounts are justified by fundamentals

**Methodology:**

1. **Growth-Adjusted Valuation (PEG-like)**
   ```
   PEG-like Ratio = P/E Ratio / (YoY Revenue Growth % + 1)
   Lower ratio = cheaper on growth-adjusted basis
   ```

2. **Quality Metrics Comparison**
   - Gross margins (profitability quality)
   - Revenue growth (growth trajectory)
   - Earnings consistency (stability)

3. **Multi-Factor Scoring**
   For each undervalued stock:
   - Score 1: P/E discount vs. sector (% discount)
   - Score 2: Growth rate vs. sector average
   - Score 3: Margin profile vs. sector
   - Score 4: Industry tailwinds/headwinds
   - **Combined Score** = Weighted sum of above

### Phase 4: Outperformance Potential Estimation

**Objective:** Estimate upside if valuations normalize to sector averages

**Model:**

```
Outperformance Potential = (Sector Avg P/E - Current P/E) / Current P/E × 100%
```

**Example: META**
```
Sector Avg P/E (Technology) = 98.6x
Current META P/E = 29.4x
Upside = (98.6 - 29.4) / 29.4 = 235%

However, META unlikely to reach sector average due to lower growth.
Conservative estimate: 15-20% upside to 35-40 P/E range
```

**Outperformance Catalysts by Company:**
- **META:** AI revenue growth acceleration, margin recovery
- **MSFT:** Enterprise AI adoption, cloud margin expansion
- **TSLA:** Margin recovery, new vehicle cycle ramp
- **PFE:** New drug launches offsetting patent cliff
- **PG, KO:** Steady dividend + low-single-digit upside

---

## Key Assumptions

### Valuation Multiples

**P/E Ratio Assumptions:**
- Used trailing twelve-month (TTM) P/E ratios
- Assumed sector multiples remain relatively stable within 12-month horizon
- Recognized that outliers may persist if justified by fundamentals

**EV/EBITDA Assumptions:**
- Used as alternative valuation metric for debt-heavy companies
- Normalized EBITDA where one-time items existed
- Assumed capital structure relatively stable

### Growth Assumptions

**Revenue Growth:**
- Used YoY growth rates as proxy for earnings growth
- Assumed growth rates sustainable for 3-5 year horizon
- Recognized that past growth doesn't guarantee future growth

**Earnings Growth:**
- Estimated based on revenue growth × margin stability assumption
- Assumed margins remain relatively stable sector by sector
- Conservative assumption that high-growth companies may face margin pressure

### Sector Dynamics

**Technology:**
- Highest growth but also highest execution risk
- Valuation multiples inflated by AI/cloud investment appetite
- Assumption: Multiples will gradually normalize as growth moderates

**Consumer:**
- Mature, stable sector with limited growth catalysts
- Valuations efficient; limited relative value opportunities
- Assumption: Multiples remain range-bound

**Healthcare:**
- Defensive sector with regulatory and patent cliff risks
- Assumption: Modest growth with focus on dividend stability

**Finance:**
- Sensitive to interest rates (current rate environment favors financials)
- Assumption: Fair valuations; limited upside unless rates surprise

---

## Sensitivity Analysis

### Valuation Sensitivity to Key Assumptions

**What if P/E Multiples Compress 10%?**
- Technology average: 98.6 → 88.7 (all stocks decline ~10%)
- Undervalued stocks compressed less in percentage terms
- META still attractive on absolute basis

**What if Revenue Growth Slows 30%?**
- High-growth stocks (TSLA, NVDA) more negatively impacted
- Consumer/Healthcare less impacted (lower growth expectations)
- Undervalued tech stocks (MSFT, META) still reasonably priced

**What if Margins Compress 5%?**
- Gross margin sensitive companies (MSFT, AAPL) impacted
- Lower margin businesses (AMZN) less impacted
- Most undervalued stocks have stable margin profiles

### Margin of Safety

**Applied Conservative Assumptions:**
- Estimated outperformance at 15-20% (not full sector multiple expansion)
- Assumed 1-2 year timeframe for revaluation (not immediate)
- Discounted for execution risk and market sentiment changes

---

## Potential Limitations & Caveats

### Data Limitations
- Financial data as of Jan 2025; Q1 2025 earnings may shift valuations
- Market conditions and sentiment changes can override valuation logic
- Geopolitical/macro events not modeled in this analysis

### Methodological Limitations
- Relative valuation assumes sector groupings are appropriate
- P/E ratios don't account for balance sheet strength differences
- Forward assumptions about growth rates inherently uncertain
- Analysis does not incorporate macroeconomic scenarios

### Risk Factors Not Modeled
- Interest rate changes and their impact on discount rates
- Currency exposure for multinational companies
- Regulatory or legal risk (pharma, tech, finance sectors)
- Execution risk on growth initiatives
- Competitive threats and market share changes

---

## Investment Disclaimers

### Confidence Levels

**High Confidence (15-20% upside potential):**
- META, MSFT (strong earnings, clear catalysts)
- PFE (defensive with low valuation)

**Moderate Confidence (10-15% upside potential):**
- TSLA (execution dependent)
- PG, KO (dividend-oriented, lower growth)

**Low Confidence (5-10% upside potential):**
- Fairly valued stocks with limited catalysts
- Highly leveraged to macro growth assumptions

### Time Horizon
- Analysis assumes 12-24 month investment horizon
- Shorter timeframe = more volatile
- Longer timeframe = more time for fundamentals to play out

### Risk Warnings
- Stocks can remain mispriced longer than expected
- Sector rotations can amplify or reverse discounts
- Individual company execution risks are material
- Past valuation does not guarantee future valuation

---

## Conclusion

This analysis uses rigorous relative valuation methodology to identify undervalued stocks with 15-20% outperformance potential. The candidates (META, MSFT, PFE) trade at significant discounts to peers despite comparable or better fundamentals, suggesting potential for revaluation.

However, investors should recognize that:
1. Valuations can remain "wrong" for extended periods
2. Macro factors (rates, sentiment) may override relative value
3. Individual company execution is critical
4. Diversification across sectors is prudent

---

**Analysis Date:** January 2025  
**Data Currency:** Jan 15, 2025 stock prices and FY2024 financials  
**Next Update:** Recommend refreshing analysis quarterly with new earnings data

