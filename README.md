# Which Countries Are Improving Fastest in Reducing Gas Flaring? (2012–2024)

## 📌 Business Problem
Gas flaring — the burning of associated gas during oil production — remains a major environmental and economic issue. 

It contributes to:
- CO₂ and methane emissions
- Air pollution
- Energy waste
- Lost economic value

Reducing flaring is a key target in global climate commitments and energy transition strategies.

This project answers the central question:

**Which countries have improved the fastest in reducing gas flaring between 2012 and 2024?**

## 🎯 Objective
To identify and rank countries based on:
- Absolute reduction in flaring volume (billion cubic meters, bcm)
- Percentage reduction
- Compound Annual Reduction Rate (CAGR)
- Trend consistency over time

The goal is to distinguish between:
- Countries achieving large structural reductions
- Countries with short-term or inconsistent declines


## 📂 Data Source
- Gas flaring data (billion cubic meters — bcm) was obtained from:

**World Bank Global Gas Flaring Tracker**

- Time period analyzed:
**2012–2024**

- Data structure:
Country
Year
Flaring volume (bcm)

## Tools Used
- Python
- Pandas
- NumPy
- Matplotlib / Seaborn

## 🧹 Data Cleaning & Preparation (Python)

Steps performed:

1. Loaded dataset into Pandas

2. Removed:

- Empty rows
- Total / aggregated rows

3. Reshaped data from wide to long format
4. Filtered years between 2012 and 2024
5. Calculated reduction metrics:
- Absolute change (bcm)
- Percentage change (%)
- Compound annual reduction rate (CAGR)
  
Reduction Formulas Used
```wide["abs_change_bcm"] = wide[2024] - wide[2012]```
```wide["pct_change_%"] = (wide[2024] / wide[2012] - 1) * 100```
```wide["cagr_%"] = ((wide[2024] / wide[2012]) ** (1/12) - 1) * 100```


CAGR was calculated across a 12-year period.
Negative values indicate flaring reduction.


## 📊 Analysis & Visualizations

#### 1️⃣ Fastest Percentage Reductions (CAGR %)

This visualization ranks countries by compound annual reduction rate.

##### 📌 What this measures:

Speed of improvement over time.

##### Key Findings
- Countries such as Uzbekistan, Kazakhstan, and Yemen show significant percentage reductions.
- Sustained multi-year declines indicate structural policy or operational improvements.
- Large percentage reductions may reflect:
  - Flaring capture infrastructure investments
  - Regulatory enforcement
  - Reduced production volumes
 
⚠️ Smaller initial volumes can exaggerate percentage changes.

#### 2️⃣ Largest Absolute Reductions (bcm)

This visualization ranks countries by total flaring reduction in volume terms.

##### 📌 What this measures:

Total contribution to global flaring reduction.

##### Key Findings
- Nigeria and Kazakhstan recorded large absolute reductions.
- Even moderate percentage declines in high-flaring countries create large environmental impact.
- Scale matters more than rate when assessing global emissions reduction impact.

#### 3️⃣ Time-Series Trends (2012–2024)

A trend visualization tracks flaring changes year-by-year.

##### Observations
- Several countries show steady structural decline.
- Some exhibit volatility linked to:
  - Oil production fluctuations
  - Infrastructure expansion delays
  - Policy shifts
- COVID-related production slowdown influenced temporary reductions in 2020.

## Overall Findings
1. Structural flaring reductions are concentrated in a subset of producing countries.
2. Percentage improvements differ from absolute environmental impact.
3. High-flaring countries contribute most to global reduction when improvements occur.
4. Some reductions may be linked to lower oil production rather than improved capture technology.
5. Flaring reduction progress remains uneven across producers.

## Limitations
1. The analysis does not adjust for:
- Oil production levels
- Changes in associated gas output
- Field maturity differences
  
2. Reductions may result from:
- Production declines rather than improved gas capture.

3. Data does not distinguish between:
- Routine flaring
- Emergency flaring

4. 2024 data may be provisional.

5. Environmental impact (CO₂ equivalent) was not directly calculated.

## Conclusion
Between 2012 and 2024, several oil-producing countries demonstrated measurable progress in reducing gas flaring.

While percentage-based rankings highlight rapid improvements in some economies, absolute reductions reveal that major producing countries drive the largest environmental gains.

The distinction between reduction speed and reduction scale is critical when evaluating global climate impact.

Continued infrastructure investment, regulatory enforcement, and associated gas commercialization will determine whether flaring reduction trends are sustained.

