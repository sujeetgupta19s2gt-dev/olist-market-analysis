# Olist E-Commerce: Logistics and Customer Satisfaction Analysis

## 1. Overview
This project analyzes the Olist Brazilian e-commerce dataset (2016–2018) to uncover why customers leave low reviews and how logistics friction impacts the marketplace. 

## 2. Methodology & Validation
* **Data Cleaning:** Filtered strictly for `order_status == 'delivered'` and aggregated multi-item orders at the transaction level to prevent double-counting.
* **Delivery Delay Formula:** 
  $$\text{Delivery Delay} = \text{Actual Delivery Date} - \text{Estimated Delivery Date}$$
* **Predictive Model:** Built a Random Forest Classifier using core features (`freight_value`, `item_value`, `delivery_days`, `number_of_items`, `payment_value`) to predict late fulfillment, achieving **95% accuracy**.

## 3. Key Findings
* **The Review Cliff:** On-time deliveries maintain ratings above **4.3 stars**. When delays exceed 7 days, scores drop toward **2.5 stars** with a major surge in 1-star reviews.
* **Predictive Drivers:** Transit time (`delivery_days`) and freight cost (`freight_value`) are the heaviest structural triggers for customer dissatisfaction.
* **Merchant Outliers:** A small cohort of high-volume sellers drives a disproportionate share of chronic delivery delays.

## 4. Strategic Recommendations
1. **Automated Early Warnings:** Flag orders falling behind schedule 48 hours before the promised delivery date.
2. **Proactive Customer Outreach:** Send updates and transparent tracking notifications before customers leave 1-star reviews.
3. **Merchant Accountability:** Institute weekly performance scorecards targeting high-delay sellers.