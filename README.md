# Pastry Palace — Business Data Management & Sales Analysis

**Optimizing Inventory and Sales Forecasting Through Data-Driven Decision Making**

## Project Overview

This project demonstrates end-to-end business analytics applied to a real local bakery facing zero formal data tracking. By conducting a 50-day field study, I collected and analyzed 36 core SKUs to uncover profit drivers, demand volatility, and wastage patterns. The deliverable was an actionable data report with specific recommendations that quantified financial opportunity—enabling the owner to transition from intuition-based decisions to evidence-based operations.

**Outcome:** Identified that 47% of products drive 81.4% of profit, quantified Rs.414-per-unit waste loss on specialty cakes, and recommended targeted interventions expected to improve margins by 15–20% on high-variance items.

---

## Business Context

**The Problem:**
Pastry Palace, a local bakery in Dakra, Jharkhand, operated entirely on the owner's intuition. No daily sales tracking, no demand patterns, no systematic understanding of which products were profitable or where waste occurred. Inventory decisions were made by feel, leading to over-production on slow days and stock-outs on high-demand days.

**Why This Matters:**
Small bakeries operate on thin margins (typically 15–25% for fresh goods). Wastage of perishable items is a direct profit leak. Demand volatility, if unmanaged, compounds this problem.

**The Approach:**
Rather than rely on historical data (which didn't exist), I conducted owner interviews and on-site observations to manually collect granular daily sales data over 50 consecutive days (June 1 – July 20, 2025). This real-world dataset became the foundation for identifying quick wins and strategic optimizations.

---

## Data Collection

- **Period:** 50 consecutive days (June 1 – July 20, 2025)
- **Products:** 36 core SKUs (excluded niche items with unreliable verbal estimates)
- **Method:** Daily owner interviews + on-site observation; all quantities and costs manually recorded
- **Scope:** Daily sales units, cost price, selling price, unsold quantity (wastage), and product category
- **Data Quality:** Estimates subject to owner recall; no POS system; validated through cross-checks with sales receipts where available

---

## Methodology

### 1. **ABC Analysis**
Ranked all 36 products by cumulative profit contribution to identify the vital few products driving most revenue. This revealed which SKUs deserve production priority and promotional focus.

### 2. **Coefficient of Variation (CV) Analysis**
Calculated CV (standard deviation ÷ mean) for each product to quantify demand volatility. Low CV = predictable, high CV = erratic. Essential for safety stock planning and production scheduling.

### 3. **Wastage Cost Analysis**
Multiplied unsold units by cost price per product to quantify financial loss per SKU. Identified which products cause the largest absolute waste and where pre-order or demand forecasting would have highest ROI.

### 4. **Time Series Analysis**
Plotted daily profit over 50 days with a 7-day moving average to smooth noise and reveal trends. Identified day-of-week effects (e.g., Friday dips) and anomalies (e.g., Father's Day spike).

### 5. **Product Portfolio Matrix**
Created a 2×2 scatter plot (sales volume vs. profit margin) to segment products into four strategic categories:
- **Stars:** High volume + high margin (e.g., Momos/plate)
- **Opportunities:** Low volume + high margin (specialty cakes — high wastage risk)
- **Workhorses:** High volume + low margin (bread items)
- **Dogs:** Low volume + low margin (niche sweets — candidates for discontinuation)

### 6. **Descriptive Statistics**
Computed mean, median, and standard deviation on quantity sold and profit per product to summarize central tendency and spread.

---

## Key Findings

- **Profit Concentration:** 47% of products (17 SKUs) generate 81.4% of total profit (ABC Class A). The remaining 19 SKUs contribute only 18.6%.

- **Fresh Category Dominance:** Fresh items account for 76% of total profit. This category is the business engine.

- **Top Products:** Chocolate Cake + Butterscotch Cake alone contribute 22.8% of all profit—a concentration risk if supply is disrupted.

- **Most Reliable Product:** Momos/plate averages 10.6 units sold daily with the lowest CV (19.6%), indicating consistent, predictable demand. Best candidate for fixed daily production.

- **Most Volatile Products:** Birthday cakes, custom orders, and seasonal items have CV > 65%, driven by event-based demand spikes rather than daily consumption.

- **Wastage by Unit Count:** Pav Bhaji leads with 19 unsold units across the period; high production relative to demand.

- **Wastage by Financial Cost:** Specialty cakes create the largest financial loss per unsold unit (Rs.414 each). Over 50 days, this category accumulated significant preventable loss.

- **Demand Spikes:** Father's Day (single day) generated Rs.3,317 profit—8× the daily average. Event-triggered sales create opportunity for pre-order optimization.

- **Day-of-Week Pattern:** Consistent Friday dip observed; local market events draw foot traffic away from the bakery on that day.

---

## Recommendations Delivered

1. **Pre-Order Model for Specialty Cakes**
   - Eliminate Rs.414-per-unit waste on custom/celebration cakes by introducing a 24–48 hour pre-order system.
   - Target impact: Reduce Category B/C specialty cake waste by 80%; recover Rs.2,000–3,000 monthly.

2. **Safety Stock Thresholds for High-CV Items**
   - Define minimum inventory levels for birthday cakes and event-driven items based on historical CV (65%+).
   - Prevent stock-outs during surprise demand spikes while reducing overproduction on quiet days.

3. **Daily Production Targets for Low-CV Items**
   - Set fixed daily targets: e.g., prepare 11–12 Momos/plate every day (based on 10.6 avg + 1 unit safety stock).
   - Low CV justifies production consistency; eliminates daily guesswork.

4. **Friday Production Reduction**
   - Reduce fresh item production (bread, pastries) by 15–20% on Fridays to align with observed demand dip.
   - Reallocate ingredients to high-demand items (Momos, cakes).

5. **Formalize Google Sheets Tracking**
   - Transition owner's informal notes into a structured daily log within the existing Google Sheets setup.
   - Rolling 30-day profit trend + daily wastage tracking visible at a glance.

---

## Tools Used

- **Google Sheets:** Pivot tables, scatter plots, time series charts, STDEV/AVERAGE formulas, manual data entry and validation
- **Python + Pandas:** Data cleaning, anomaly detection, statistical calculations (CV, mean, std dev)
- **All visualizations:** Created in Google Sheets

---

## Limitations

1. **Short Time Window:** 50 days captures daily volatility but misses seasonal trends (summer vs. monsoon vs. winter demand shifts).

2. **Data Collection Method:** All quantities are owner estimates, not transaction-level POS data. Subject to recall bias and rounding.

3. **External Events Not Fully Captured:** One Father's Day spike visible, but impact of other regional holidays, festivals, or local events may be underrepresented in a single 50-day window.

4. **Product Mix Stability:** Analysis assumes the 36 SKUs remain constant; doesn't account for potential recipe changes, supplier shifts, or new product launches during a longer period.

---

## Future Scope

1. **12-Month Data Collection**
   - Validate seasonal patterns (monsoon demand, festival months, summer slump).
   - Establish confidence in recommendations before full implementation.

2. **Demand Forecasting Model**
   - Build a simple moving average or exponential smoothing model for each SKU.
   - Upgrade from fixed targets to probabilistic demand forecasts by season.

3. **Database Migration**
   - Move from manual Google Sheets to a lightweight POS app or database (e.g., Inventory Mate, Zoho Inventory, or custom Google Apps Script).
   - Enable real-time tracking, automated alerts for low stock, and integrated wastage logging.

4. **Cost-of-Goods-Sold (COGS) Impact Analysis**
   - Expand wastage tracking to include ingredient spoilage, energy, and labor cost-per-SKU.
   - Model total margin impact, not just direct wastage.

5. **Customer Feedback Loop**
   - Correlate sales patterns with foot traffic counts, local events, and weather.
   - Refine production schedules based on external demand signals.

---

## Author

**Aryan Kumar**  
B.S. Data Science, Indian Institute of Technology (IIT) Madras

---

*This project demonstrates applied analytics on a real business problem with measurable outcomes. All findings and recommendations were validated with the owner and are ready for implementation.*
