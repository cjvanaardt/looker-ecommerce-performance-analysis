# Customer Growth / CRM

## Data loading and preparation
We describe and define the tables we will use for our analysis.

We will start with a customer Analytics base table. The grain of the table will be user.

Relevant features include
- grain
  - user id
  - first_purchase_date
  - acquisition_month (cohort)
  - analysis_date (for tenure calc)
- Demographics and Acquisition
  - age (or age_bin)
  - gender
  - country
  - traffic_source
- Early Purchase Behaviours
  - first_category
  - first_order_revenue
  - first_order_profit
  - first_order_item_count
  - most_common_category
  - time_to_second_order (days)
  - (binary) has_repeated (30, 90, 180 days)
  - orders (90, 180, 365 days)
- Value & RFM
  - revenue (90, 180, 365 days)
  - profit (90, 180, 365 days)
  - lifetime_revenue
  - lifetime_profit
  - lifetime_AOV
  - recency_days (days since last order)
- purchase dropoff
  - return rate
  - returned item
  - no order is last (90, 180, 360, 540, 720 days)
  - no activity (events) in last (90, 180, 360, 540, 720 days)
  - last_browser
  - last_uri
  - most common browser
