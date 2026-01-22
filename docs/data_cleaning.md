# Data cleaning
Summary
- No data quality issues were identified that obstructed primary project analysis.
- Limitations data issues had on any analysis.
- Several data modelling redundancies were identified and documented for further investigation.

## distribution_centers (10 rows)

### Observations
- Inconsistent names for New York distribution center.
- name column contains both city and state values.

### Actions
- Renamed New York distribution center.
- Split name into separate city and state columns since each represent independent dimensions for each distribution center.

## events (2431963 rows)

### Observations
- created_at column isn't in date-time format.
- 1125671 missing user_id values (46%).
- 23080 missing city values (0.95%).

### Actions
- Set created_at data type to date-time.
- Attempted to recover missing user_id from other events within the same session. Found no session sharing events with missing and present user_id values.

### Impact
- While there are a large proportion of user_ids are missing, the remaining records (1306292) still provide sufficient coverage for reliable analysis.
- Only a small proportion of city values are missing, minimally impacting anaysis.

### Recommendations
- In production setting, consider recovering missing city values using event postal_code or ip_address.
- Further investigate where the missing user_id and city values originate. Missing city values in events table mirror those in the user table, suggesting the user table may be the source of the missing values. Ask the data engineering team to identify where in the pipeline these missing values start occurring and a possible solution.

## inventory_items (490705 rows)

### Observations
- created_at and sold_at columns aren't in date-time format.
- Inconsistent number of decimals in cost and product_retail_price columns.
- 29 missing product_name values (0.01%).
- 401 missing product_brand values (0.08%).

### Actions
- Set created_at and sold_at columns to date-time data types.
- Rounded cost and retail_price columns to 2 decimal places. 
- Attempted to recover missing product_name and product_brand values from product table. No missing values were found in the product table.

### Impact
- A very small proportion of product_name and product_brand values are missing, minimally influencing analysis.

### Recommendations
- Further investigate where the missing product_name and product_brand values originate. Missing name and product values mirror the product table, suggesting the product table is the source of the missing values.

## order_items (181759 rows)

### Observations
- Date columns don't have date-time types.
- sale_price has inconsistent number of decimals
- 35872 rows with shipped_at_date before created_date (20%).

### Actions
- Updated date columns to have date-time data types.
- Rounded sale_price to 2 decimal places.

### Impact
- The remaining correctly ordered created_at and shipped_at records (145887) still provide sufficient coverage for reliable analysis.

### Recommendation
- Further investigate where the incorrect ordering of created_at and shipped_at values originate. Ask the data engineering team to identify where in the pipeline the incorrect ordering starts occurring and a possible solution.

## orders (125226 rows)

### Observations
- Date columns don't have date-time types.

### Actions
- Updated date columns to have date-time data types.

## products (29120 rows)

### Observations
- Inconsistent number of decimals in cost and retail_price columns.
- 2 missing name values (0.01%).
- 24 missing brand values (0.08%).

### Actions
- Rounded number of decimals in cost and retail_price columns to 2.
- Attempted to recover product and brand names from products table but none where found.

### Impact
- The large number of present product brand and names (29118 and 29096 respectively) still provide sufficient coverage for reliable analysis.

### Recommendations
- Further investigate the missing product and brand values. Ask the data engineering team if there is a source of truth for product names and brands from the product_id. Remember to also filter missing product and brand names through to missing product names and brands in the inventory items table.

## users (100000 rows)

### Observations
- created_at isn't date-time data type.
- 958 missing 958 city values (0.96%)

### Actions
- Updated created_at column to date-time data type.
- Tried to recover missing city values from events table but none where found.

### Impact
- The large number of present city values (99042) still provide sufficient coverage for reliable analysis.

### Recommendations
- Further investigate where the missing city values originate. Ask the data engineering team to identify where in the pipeline these missing values start occurring and a possible solution. Remember to filter recovered city values to the events table.
- In production setting, consider recovering city values using user postal code.




# Data Modelling Observations
To be further investigated in another project.

- Duplicated values
    - Orders and order items
        - status
        - returned_at
        - created_at
        - shipped_at
        - delivered_at
    - Product and inventory items
        - name/product_name
        - category
        - distribution_center_id
        - sku
    - Users and orders
        - gender
- product id and sku are both unique per product
