# Olist E-Commerce Marketplace & Logistics Optimization

An end-to-end data analysis and machine learning pipeline evaluating Olist's Brazilian e-commerce dataset (2016–2018) to uncover the root causes of customer dissatisfaction and optimize supply chain fulfillment.

## Team Name
**REWIRE NINJAS** (Team Members: Sujeet Gupta)

---

## Project Structure

* **`olist_market_analysis.ipynb`**: Complete Jupyter notebook containing the full data engineering pipeline, exploratory data analysis, visualizations, and a **Random Forest Classifier** achieving **95% accuracy** in predicting late delivery risk.
* **`analysis_report.md`**: Executive markdown report detailing data methodology, key findings (including the "Review Cliff" at 7+ days delay), and strategic operational recommendations.
* **`data_source_validation.md`**: Data hygiene report covering order-status filtering (`order_status == 'delivered'`), missing timestamp handling, and metric definitions.
* **`three_minute_video_script.md`**: Structured pitch script designed for executive presentation and defense.

---

## Key Technical Highlights

1. **Transactional Data Hygiene:** Aggregated multi-item orders, freight costs, and payment values at the order level to maintain statistical integrity.
2. **Predictive Modeling:** Trained a Random Forest Classifier on core operational features (`freight_value`, `item_value`, `delivery_days`, `number_of_items`, `payment_value`) to flag vulnerable shipments.
3. **Merchant Audit:** Grouped delivery anomalies by `seller_id` to highlight high-volume merchant outliers driving chronic downstream friction.

---

## Strategic Recommendations

* **Proactive Telemetry:** Deploy an early-warning system flagging shipments falling behind schedule 48 hours prior to promised delivery dates.
* **Customer Recovery Loops:** Manage expectations and transmit tracking updates before dissatisfied customers leave 1-star reviews.
* **Merchant Scorecards:** Institute weekly performance reviews targeting high-delay seller accounts.
