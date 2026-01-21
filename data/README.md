Source - https://www.kaggle.com/datasets/mustafakeser4/looker-ecommerce-bigquery-dataset


# Data Description
Source - https://www.kaggle.com/datasets/mustafakeser4/looker-ecommerce-bigquery-dataset
---
There are 7 data files

## distribution_centers

|Column|Data Type|Description|
|---|---|---|
|id|Numerical (discrete)|Unique distribution center identifier|
|city|Categorical|City of the distribution center|
|state|Categorical|State of the distribution center|
|latitude|Numerical (continuous)|Latitude of the distribution center|
|longitude|Numerical (continuous)|Longitude of the distribution center|


## events
|Column|Data Type|Description|
|---|---|---|
|id|Numerical (discrete)|Unique event identifier| 
|user_id|Numerical (discrete)|Identifier of user associated with the event|
|sequence_number|Numerical (discrete)|Sequence number of event in session|
|session_id|Categorical|Identifier for the session during which the event occurs|
|created_at|Date-time|When the event occurred|
|ip_address|Categorical|IP address from which the event originated|
|city|Categorical|City where the event occurred|
|state|Categorical|State where the event occurred|
|browser|Categorical|Web browser used during the event|
|traffic_source|Categorical|Traffic source leading to the event|
|uri|Categorical|Uniform Resource Identifier associated with the event|
|event_type|Categorical|Type of event recorded|

## inventory_items
|Column|Data Type|Description|
|---|---|---|
|id|Numerical (discrete)|Unique inventory item identifier|
|product_id|Numerical (discrete)|Product identifier associated with inventory item|
|created_at|Date-time|When the item was acquired|
|sold_at|Date-time|When the item was sold|
|cost|Numerical (continuous)|Cost of the item|
|product_category|Categorical|Category of the associated product|
|product_name|Categorical|Name of the associated product|
|product_brand|Categorical|Brand of the associated product|
|product_retail_price|Numerical (continuous)|Retail price of the associated product|
|product_department|Categorical|The department the product belongs to|
|product_sku|Categorical|Stock Keeping Unit (SKU) of the product|
|product_distribution_center_id|Numerical (discrete)|Identifier for the distribution center associated with the product|

## order_items
|Column|Data Type|Description|
|---|---|---|
|id|Numerical (discrete)|Unique identifier for each order item|
|order_id|Numerical (discrete)|Identifier of associated order|
|user_id|Numerical (discrete)|Identifier of associated user|
|product_id|Numerical (discrete)|Identifier of associated product|
|inventory_item_id|Numerical (discrete)|Identifier of associated inventory item|
|status|Categorical|Status of the order item|
|created_at|Date-time|When the order item was created|
|shipped_at|Date-time|When the order was shipped|
|delivered_at|Date-time|When the order was delivered|
|returned_at|Date-time|When the order was returned|
|sale_price|Numerical (continuous)|Price of the order item|

## orders
|Column|Data Type|Description|
|---|---|---|
|order_id|Numerical (discrete)|Unique order identifier|
|user_id|Numerical (discrete)|Identifier of user who placed the order|
|status|Categorical|Status of the order|
|gender|Categorical|Gender of the user who placed the order|
|created_at|Date-time|When the order was created|
|shipped_at|Date-time|When the order was shipped|
|delivered_at|Date-time|When the order was delivered|
|returned_at|Date-time|When the order was returned|
|num_of_item|Numerical (discrete)|Number of items in the order|

## products
|Column|Data Type|Description|
|---|---|---|
|id|Numerical (discrete)|Unique product identifier|
|cost|Numerical (continuous)|Product cost|
|name|Categorical|Name of the product|
|brand|Categorical|Brand of the product|
|retail_price|Numerical (continuous)|Retail price of the product|
|department|Categorical|Department the product belongs to|
|sku|Categorical|Stock Keeping Unit (SKU) of the product|
|distribution_center_id|Numerical (discrete)|Identifier of distribution center associated with the product|

## users
|Column|Data Type|Description|
|---|---|---|
|id|Numerical (discrete)|Unique user identifier|
|first_name|Categorical|First name of the user|
|last_name|Categorical|Last name of the user|
|email|Categorical|Email address of the user|
|age|Numerical (discrete)|Age of the user|
|state|Categorical|State of the user|
|street_address|Categorical|Street address of the user|
|postal_code|Categorical|Postal code of the user|
|city|Categorical| City of the user|
|latitude|Numerical (continuous)|Latitude of the user|
|longitude|Numerical (continuous)|Longitude of the user|
|traffic_source|Traffic source leading to the user|
|created_at|Date-time|When the user account was created|