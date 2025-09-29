# IMPACT-OF-HEALTH-INSURANCE-REIMBURSEMENT-ON-PHARMACY-PROFITABILITY

# 1. Project Overview
This project analyzes the impact of  Health Insurance Scheme (NHIS) reimbursements on pharmacy profitability at the Federal Medical Center. 
The goal was to evaluate whether NHIS cost structures cover operational costs and ensure financial sustainability. 
while still maintaining affordable patient access to essential medicines.


# 2. Objectives

Assess the profitability of drugs reimbursed under Health insurance compared to self-paying patient sales.

Identify high-revenue vs. low-margin drugs to guide formulary and pricing negotiations.

Track monthly profit/loss trends to detect periods of significant erosion.

Explore the gap between NHIS reimbursement cost vs. actual acquisition cost.

Provide recommendations for pricing adjustments, supplier negotiations, and sustainable models for pharmacy operations.

# 3. Data Sources

Federal Medical Center – Pharmacy Department (dispensing records)

Globmed Electronic Medical Records (EMR)

Data Period: November 2023 – July 2025

Data Attributes Included:

Self-paying patient prices

NHIS reimbursement cost price

Quantity of items dispensed

Drug/item details

Tools Used: Excel, PostgreSQL, SQL, Tableau

# 4. Data Cleaning and Preparation

Created a manual date column (month/year) in PostgreSQL for time-series analysis.

Generated calculated fields, including:

Health insurance Sale = NHIS cost × total quantity dispensed

Selling Price = (self-paying price or cost price × 1.3 markup)

Expected Revenue = Selling price × quantity

Expected Profit = Expected Revenue – Selling Price

Profit Margin = (Health Insurance Sale – cost × quantity) ÷ (cost × quantity)

Checked for missing values (replaced with NULL).

Cleaned 642 inconsistent drug/item names out of 5,662 rows using Excel and SQL.

# 5. Methodology

Descriptive Analysis: Total sales, profit/loss, reimbursement gaps.

Trend Analysis: Monthly profit/loss trends via line chart.

Drug-Level Analysis: Revenue and profitability comparison across drugs.

Comparative Analysis: NHIS reimbursement price vs. actual acquisition cost.

Categorical Analysis: Share of underpriced vs. overpriced drugs.

Visualization: Tableau dashboards with KPIs and charts.

# 6. Key Findings

6.1 Profit/Loss Trend

Out of 12 months analyzed, 9 months recorded losses.

February and August were the steepest deficits (>₦2.8M each).

Health insurance reimbursements generally failed to cover costs, even with strong sales volumes.

6.2 Total Sales by Drug

High-revenue drugs: Indapamide (₦7M), Telmisartan (₦4.8M), Vildagliptin (₦4.3M).

Revenue alone did not guarantee profitability due to reimbursement gaps.

6.3 Drug Sales by Volume

High-volume drugs: Ascorbic Acid, Ferrous Sulphate, Amlodipine, Paracetamol.

Despite large volumes, these were unprofitable under NHIS due to low reimbursement.

6.4 Profitability by Drug

Profitable drugs: Indapamide, Enoxaparin, Sodium Chloride.

Unprofitable drugs: Essential medicines consistently reimbursed below acquisition cost.

6.5 Health Insurance Cost vs. Cost Price

Drugs like Halothane and Oxaliplatin were reimbursed below the purchase price, guaranteeing losses.

6.6 Overpriced vs. Underpriced Drugs

Overpriced (profitable): 3,052 drugs (53.3%).

Underpriced (loss-making): 2,607 drugs (46.7%), mostly high-cost specialty medicines driving pharmacy losses.

# 7. Insights and Recommendations

Quarterly Review of NHIS Pricing

Collaborate with NHIS, hospital management, and stakeholders to update pricing in line with inflation and market dynamics.

Supplier & Manufacturer Negotiations

Secure special pricing for NHIS drugs.

Explore NHIS–manufacturer partnerships to balance affordability and profitability.

Generic Substitution Strategy

Encourage clinicians to prescribe generics over branded high-cost drugs (e.g., Enoxaparin).

Regular Pharmacy Updates

Share NHIS drug lists and generic alternatives with clinical teams to minimize prescribing of unprofitable drugs.

Adopt Sustainable Models

Consider tiered reimbursement or shared-risk pricing models to align pharmacy sustainability with patient affordability.

# 8. Risks of Inaction

Financial strain on pharmacies, leading to reduced availability or substitution with lower-quality drugs.

Threat to patient care, including treatment failures, increased readmissions, and worse outcomes.

Systemic risk: If losses persist, NHIS could undermine trust and fail its mission of equitable, accessible care.

# 9. Conclusion

The analysis shows NHIS reimbursement significantly erodes pharmacy profit margins, with most months operating at a loss.
High-volume essential medicines are disproportionately under-reimbursed, while specialty drugs account for the largest financial gaps. 
Without pricing model reforms, supplier negotiations, and generic substitutions, pharmacy departments risk unsustainable operations, ultimately threatening patient care delivery.
