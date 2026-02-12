# Customer Growth / CRM

## Data loading and preparation
We describe and define the tables we will use for our analysis.

We will start with a customer Analytics base table. The grain of the table will be user.

Relevant features include
- user id (grain)
- user features
  - age
  - gender
  - location
- user purchase behaviours
  - first purchase date
  - first purchase category
  - most common category
  - time to second order
  - number of orders within 90, 180, 365 days of first purchase
- value metrics
  - revenue within 90, 180, 365 days of first purchase\ 
  total cost
  - 
- number of orders
- number of order items
- total cost of period
- total revenue of period

Important aggregates to invetigate changing repeat purchase patterns
- Average number of items per order by year-month
- Average order value by year-month
- Average order profit by year-month
- Proportion of total orders coming from repeated orders
- Proportion of revenue coming from repeated orders
- Proportion of profit coming from repeated orders

For final aggregate we will need a year-month grain table for all customers with features
- acquisition channel
- age
- location
- number of orders
- total revenue of period
- total cost of period
which we can join to calculate the proportions.

### Customer Behaviours Driving Lifetime Value
We will use a customer grain containing features
- 

