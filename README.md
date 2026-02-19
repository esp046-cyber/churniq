# churniq
Philippine Telco Customer Churn Predictor Web Application with CSV Upload Capability.

🇵🇭 Philippine Telecom Context
The application simulate churn prediction for Philippine telecom companies such as:
* Globe
* Smart
* DITO
Assume realistic Philippine telecom conditions:
* Prepaid customers higher churn risk
* Month-to-month plans higher risk
* Low tenure increases churn
* High monthly charges increase churn
* No tech support increases churn
* Rural customers slightly higher churn
* Fiber subscribers lower churn than DSL
* Senior citizens slightly higher churn
* Postpaid with long contracts lower churn
No backend allowed. Use advanced JavaScript rule-based weighted scoring logic.
🎯 Core Application Requirements
Create ONE fully self-contained HTML file that includes:
* Embedded CSS
* Embedded JavaScript
* No external dependencies
* Modern SaaS dashboard design
* Fully responsive (mobile optimized)
* Executive analytics style
📂 Feature 1: CSV Upload & Batch Prediction
Include:
1. CSV File Upload section
2. Accept .csv file
3. Parse CSV using JavaScript
4. Required CSV Columns:
   * Gender
   * SeniorCitizen
   * Partner
   * Dependents
   * Tenure
   * PlanType (Prepaid/Postpaid)
   * InternetService (DSL/Fiber/None)
   * Contract
   * TechSupport
   * MonthlyCharges
   * TotalCharges
   * Region (Urban/Rural)
   * TelcoProvider (Globe/Smart/DITO)
5. After upload:
   * Predict churn probability per row
   * Add new column: ChurnRisk (%)
   * Add Risk Category (Low/Medium/High)
6. Display:
   * Total Customers
   * High Risk Count
   * Medium Risk Count
   * Low Risk Count
   * Average Churn Risk
   * Risk Distribution Pie Chart
   * Provider Comparison Chart
   * Region Risk Comparison
7. Add Export Updated CSV Button (with predictions included)
🧍 Feature 2: Single Customer Prediction Form
Include professional input form with:
* Gender
* Senior Citizen
* Partner
* Dependents
* Tenure
* Plan Type (Prepaid/Postpaid)
* Internet Service
* Contract Type
* Tech Support
* Monthly Charges
* Total Charges
* Region
* Telco Provider
Include:
* Predict Button
* Reset Button
* Random Sample Generator
Display:
* Churn Probability %
* Risk Category
* Animated Risk Gauge
* Contributing Risk Factors
* Visual Progress Bar
📊 Advanced Dashboard Analytics
Include dynamic visualizations:
* Pie Chart (Risk Distribution)
* Bar Chart (Top Risk Drivers)
* Telco Provider Risk Comparison
* Regional Risk Breakdown
* Average Revenue at Risk calculation
Charts must be rendered using pure JavaScript (no external libraries).
🎨 UI / UX Requirements
Design must look like a telecom analytics SaaS platform.
Include:
* Dark mode toggle
* Glassmorphism dashboard cards
* Smooth animations
* Gradient backgrounds
* Modern typography
* Professional executive theme
🧠 Prediction Logic Requirements
Use weighted scoring logic such as:
* Prepaid = +15%
* Month-to-month = +20%
* Tenure < 12 months = +15%
* No Tech Support = +10%
* High Monthly Charges = +10%
* Rural = +5%
* Senior Citizen = +5%
* Fiber = -5%
* Two-year contract = -15%
Cap probability between 0% and 100%.
Risk Category:
* 0–39% → Low
* 40–69% → Medium
* 70–100% → High
📁 Output Rules

Logistic Regression Engine
Full z = β₀ + β₁X₁ + ... + βₙXₙ → sigmoid(z) pipeline with 18 calibrated PH telecom coefficients
Raw logit score displayed per prediction
Rule-Based ↔ LR toggle in the nav bar (persists across all predictions + batch)
🆕 ML Model Center (5th nav tab)
⚖️ Model Comparison — side-by-side Accuracy/Precision/Recall/ROC-AUC/F1/Log Loss for both engines with comparison bar chart
📊 Feature Importance — Top-10 |β| coefficient chart, full coefficient table, positive vs. negative SHAP-style waterfall
🎛️ What-If Simulator — 7 interactive sliders/dropdowns updating probability in real-time with logit breakdown and trend sparkline
🎯 Risk Segmentation — Save Immediately / Offer Discount / Monitor / Safe counts + pie + stacked provider chart + intervention guide cards
📈 Revenue Forecast — 6-month forecast line chart (No Intervention vs With Intervention), adjustable intervention effectiveness slider, provider recovery bars
🔢 Confusion Matrix — Simulated TP/TN/FP/FN with adjustable decision threshold slider + precision/recall/F1 threshold curve


Investor Mode — All 7 Sections Fully Functional:
SaaS Revenue Model Simulator — 7 interactive inputs → live MRR, ARR, Revenue Saved, Platform Value, 3-Year + 5-Year projections with animated KPI cards, 5-year line forecast chart, and revenue components bar chart
LTV/CAC Unit Economics — CAC, lifetime, margin & op-cost inputs → LTV, LTV/CAC ratio, payback period, EBITDA Year 1. SVG gauge + traffic light (red/yellow/green) + 5-year GP/EBITDA comparison chart
Churn Cost Impact Engine — Pulls live revenue-at-risk from uploaded CSV (or uses simulated PH market data). Shows Before vs. After AI comparison across 10%, 20%, 30% churn reduction scenarios with grouped bar chart
SaaS Valuation Calculator — ARR × Multiple selector (3x/5x/8x/12x) with animated selection. Shows company valuation, 10%/25% equity scenarios, 3-year exit return, and multi-line valuation growth chart
Investor Pitch Metrics — TAM ₱28.5B / SAM ₱8.2B / SOM (dynamic from ARR), animated horizontal bars, market donut chart, AI adoption curve forecast chart (2023–2028)
Executive Summary Generator — "Generate Investor Snapshot" button creates full pitch-card with problem/solution/market/revenue sections, live KPI stats grid, ROI narrative. "Download PDF Sim" exports styled HTML file
Competitive Moat Cards — 4 moat cards with animated score bars (92%/88%/85%/78%), SVG ring showing 86/100 overall advantage score
CSV integration: When batch data is loaded, Churn Cost Impact pulls real revenue-at-risk numbers from the uploaded dataset automatically.

