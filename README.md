# 🚖 Ride Revenue Recovery – Estimating Lost Revenue in Ride-Hailing (Dashboard link: https://app.thebricks.com/file/786a0a26-bcd8-4fa5-a758-44872ee62f48/157@6fc87763-94ff-4535-8678-6a0a26bcd83f:0/visual-board)

Objective: Estimate and recover revenue lost due to unmet demand (with a focus on cancellations) in ride-hailing services using statistical imputation and Monte Carlo simulations.

# 📌 Project Overview

### Ride-hailing platforms lose significant revenue when demand is unmet due to:

Driver cancellations

Customer cancellations

No driver available

Incomplete rides

The dataset lacked booking values for unsuccessful rides, making direct loss calculation impossible. This project demonstrates how statistics and simulation can convert missing data into actionable business insights.

# 🛠️ Methodology

### Problem Framing

#### Unmet demand = lost revenue.

Booking values missing for cancellations & unavailability.

### Imputation Strategy

Ride fares are right-skewed → mean/median imputation unsuitable.

Chosen method: Monte Carlo Simulation using the distribution of completed rides.

👉 [Insert plot: Completed ride fare distribution vs. simulated distribution]

Validation

Simulation validated against incomplete rides (true values available).

Actual values fell within 95% CI, confirming reliability.

👉 [Insert plot: CI range with true incomplete ride values]

Segmentation

Losses broken down by:

Cancellation type (driver vs. customer)

Hour of day

Vehicle type

Hotspots identified via Pareto 70% rule.

👉 [Insert chart: Loss share by cancellation type]
👉 [Insert heatmap: Hour × Vehicle cancellation hotspots]

Target Setting

Recovery target set at 40% of loss from hotspots (ambitious yet realistic).

Revenue uplift estimated at ~3% daily and hourly.

👉 [Insert table: Pre vs. Post-intervention revenue]

# 📊 Key Results

Global Estimates (Loss by Driver Type)

Driver cancellations: ~₹13.7M (47%)

Customer cancellations: ~₹5.3M (18%)

No driver found: ~₹5.3M (18%)

Incomplete rides: ~₹4.6M (16%)

Total Loss: ~₹29M (~38% of booking value demand)

Hotspot Analysis (Top 10 segments)

Driver: Auto (9–11 AM, 4–9 PM), Go Mini (6–7 PM), Go Sedan (6–8 PM)

Customer: Auto (10–11 AM, 3–8 PM, 9–10 PM), Bike (6–7 PM), Go Mini (6–8 PM)

Recovery Potential

Recoverable Loss (40% target): ~₹1.37M

Revenue Uplift: +3% daily and hourly

# 💡 Insights

Cancellations are the largest driver of loss.

Loss distribution by location was uniform → location-based prioritization not viable.

Monte Carlo simulations provided a reliable proxy for missing booking values.

Demonstrated how statistics can enable decision-making even with incomplete data.

# 🧰 Tools & Skills

Python: pandas, numpy, matplotlib, seaborn

Simulation & Stats: Monte Carlo, Confidence Intervals

Modeling: LightGBM with Bayesian tuning (baseline check)

Business Analytics: Pareto analysis, hotspot identification, recovery targets

# 🚀 Conclusion

By applying Monte Carlo simulations to missing ride data, this project quantified revenue lost to cancellations and other unmet demand, validated estimates with incomplete rides, and identified targeted interventions capable of driving a ~3% uplift in revenue.

From missing data → to actionable insights → to strategic decisions.
