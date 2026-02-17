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
- Date differences
  - time_to_second_order (days)
  - days_since_first_purchase
  - avg_days_between_orders
  - (binary) has_repeated (30, 90, 180 days)
  - orders (90, 180, 365 days)
- Value & RFM
  - revenue (90, 180, 365 days)
  - profit (90, 180, 365 days)
  - lifetime_revenue
  - lifetime_profit
  - total_orders
  - lifetime_AOV
  - recency_days (days since last order)
- purchase dropoff
  - return rate
  - returned item
  - no order is last (90, 180, 360, 540, 720 days)
  - no activity (events) in last (90, 180, 360, 540, 720 days)
  - last_browser
  - last_uri
  
## Exploratory Analaysis
We first focus on 180 day and 365 day horizon analysis. They are short enough to explore act upon while also being long enough to observe meaningful repeat purchase behaviour.

We keep only cohorts with more than 0.6 365d maturity proportion to preserve data quality.

Remark: If we want insights closer to the analysis date we can instead analyse shorter 30, 90 or 180 day chorts, but these might contain less useful repeat purchase behaviour.

Metrics we want to explore by cohort

General repeat cohort behaviour (for each also include the )
- how many and what proportion are repeating? (outside of 180, 365 for curiosity)
  - repeaters share
  - repeat rate 30
  - repeat rate 90
  - repeat rate 180
  - repeat rate 365
  - repeat rate 540
- early behaviour
  - avg_time_to_second_order
  - median_time_to_second_order
  - avg_days_between_orders
- value & lifetime signals
  - avg_lifetime_AOV (and median)
  - avg_lifetime_profit (and median)
  - avg_total_items (and median)
- Recency
  - avg_days_since_last_order
Repeat user behaviour relative to all users (shuffle these around a bit)
- % of cohort which are repeaters
- 