# 📋 Project Brief — Maven Toys Regional Revenue Dashboard

---

## 🏢 Background

**Maven Toys** is a small toy store chain operating across multiple cities in the United States. The company runs stores in major markets including Chicago, New York, and Los Angeles, with multiple store locations within each city.

The Regional Sales Managers meet monthly with the COO to review performance. However, each manager was previously presenting data in different formats and with inconsistent metrics — making it difficult to compare regions, identify trends, or spot problems quickly.

---

## 📩 The Brief

**From:** Andy Davis, Chief Operating Officer  
**To:** Lead Business Intelligence Analyst  
**Subject:** Regional Revenue Dashboard

> *"I have a monthly call with the Regional Sales Managers, but they each present their data in different ways and it's impossible to follow.*
>
> *Could you build a dashboard that we can use to filter by region, track monthly revenue trends, and see performance year-over-year?*
>
> *I'd also like to compare performance across stores, and identify which specific products drove the biggest gains and losses."*

---

## 🎯 Objectives

| # | Objective | Status |
|---|---|---|
| 1 | Define the purpose for the dashboard | ✅ Done |
| 2 | Choose the key metrics & interactivity | ✅ Done |
| 3 | Plan ahead for growing source data | ✅ Done |
| 4 | Prepare the data for visualization | ✅ Done |
| 5 | Create primary & supporting visuals | ✅ Done |
| 6 | Design the final dashboard layout | ✅ Done |
| 7 | Configure the workbook for sharing | ✅ Done |

---

## 📐 Dashboard Requirements

### Must-Have Metrics
- Total monthly revenue per region
- Month-over-Month (MoM) % change
- Year-over-Year (YoY) % change
- Revenue trend over time (2020 vs 2021)
- Store-level revenue comparison within region
- Top products driving revenue growth (MoM)
- Top products causing revenue losses (MoM)

### Interactivity
- Single dropdown to filter the entire dashboard by region
- All charts, KPIs, and tables respond to the selection

### Design Principles
- Clean, executive-friendly layout
- Color coding: green for growth, red for losses
- Minimal clutter — one screen, all key info visible

---

## 📦 Data Source

**File:** `MavenToys_Monthly_Sales.xlsx`  
**Scope:** January 2020 — December 2021  
**Granularity:** Individual sales transactions by date, store, and product  

**Key fields used:**
- Transaction Date
- Store Name & City (Region)
- Product Name
- Revenue

---

## 🏗️ Approach

### Step 1 — Data Preparation
Raw transaction data was cleaned and structured. Dates were formatted consistently. A Region column was derived from store city data to enable the dropdown filter.

### Step 2 — PivotTable Architecture
Multiple PivotTables were created as the engine behind each visual:
- Monthly revenue by region (for trend chart)
- Revenue by store with MoM delta (for store performance chart)
- Revenue by product with MoM delta (for product tables)

### Step 3 — KPI Calculation
Dynamic formulas pull the current month's revenue, prior month, and prior year equivalent for the selected region to compute MoM % and YoY % automatically.

### Step 4 — Visualization
Charts were built and linked directly to PivotTable outputs. Conditional formatting was applied to the product delta columns to show green (growth) and red (loss) shading.

### Step 5 — Dashboard Layout
All components were assembled on a single dashboard sheet. The region dropdown at the top controls everything. Non-essential gridlines, headers, and tabs were hidden for a clean, presentation-ready look.

---

## 📊 Regions Covered

| Region | Key Stores |
|---|---|
| **Chicago** | O'Hare, Lincoln Park, Millennium, Michigan Ave |
| **New York** | JFK, Times Square, Fifth Avenue |
| **Los Angeles** | LAX, Beverly Hills, Hollywood |

---

## 📈 Key Findings (July 2021)

- **Chicago** was the top revenue region at **$94,953**, up 34% YoY
- **New York** showed the strongest YoY growth at **+66.1%**
- **Los Angeles** had the highest MoM growth rate at **+29.4%**
- **Action Figure** appeared as a loss driver across multiple regions simultaneously — suggesting a supply, pricing, or demand issue worth investigating
- **Lego Bricks** was the #1 growth product in Chicago, generating $19,035 in revenue

---

## 💡 Recommendations

1. **Investigate Action Figure performance** — consistent losses across LA and NY suggest a systemic issue (pricing, competition, or stock)
2. **Scale Lego Bricks and Rubik's Cube** — strong performers in multiple regions; worth prioritizing for shelf space and promotions
3. **Monitor Magic Sand** — large losses in Chicago despite reasonable overall revenue; may have peaked
4. **Share this dashboard monthly** before regional manager calls to align discussion around a single source of truth

---

*Prepared by: Bushra Khan | [thedataalchemist.co](http://thedataalchemist.co) | [LinkedIn](https://www.linkedin.com/in/bushra-nazeer-khan/) | Date: July 2021 | Tool: Microsoft Excel*
