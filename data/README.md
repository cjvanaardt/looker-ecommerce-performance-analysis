Data - https://www.kaggle.com/datasets/mustafakeser4/looker-ecommerce-bigquery-dataset


# Data Description
There are 7 data files

## distribution_centers

|Column|Data Type|Description|
|---|---|---|
|id|Numerical discrete|Unique distribution center id|
|city|Categorical nominal|City of the distrbution center|
|state|Categorical nominal|State of the distribution center|
|latitude|Numerical continuous|Latitude of the distribution center|
|longitude|Numerical continuous|Longitude of the distribution center|


## events
|Column|Data Type|Description|
|---|---|---|
|id|Numerical discrete|Unique event id| 
|user_id|Numerical discrete|Id of user associated with the event|
|sequence_number|Numerical discrete|Sequence number of event in session|
|session_id|Categorical nominal|Identifier for the session during which the event occurs|
|created_at|Date-time|When the event occured|
|ip_address|Categorical nominal|IP address from which the event originated|
|city|Categorical nominal|City where the event occured|
|state|Categorical nominal|State where the event occured|
|browser|Categorical nominal|Web browser used during the event|
|traffic_source|Categorical nominal|Traffic source leading to the event|
|uri|Categorical nomial|Uniform Resource Identifier associated with the event|
|event_type|Categorical nomial|Type of event recorded|

## inventory_items
|Column|Data Type|Description|
|---|---|---|
|id|Numerical discrete|Unique inventory item id|
|product_id|Numerical discrete|Product id associated with inventory item|
|created_at|Date-time|When the item was acquired|
|sold_at|Date-time|When the item was sold|
|cost|Numerical continuous|Cost of the item|
|product_category|Categorical nomial|Category of the associated product|
|product_name|Categorical nomial|Name of the associated product|
|product_brand|Categorical nomial|Brand of the associated product|
|product_retail_price|Numerical continuous|Retail price of the associated product|
|product_department|Categorical nominal|The department the product belongs to|
|product_sku|Categorical nominal|Stock Keeping Unit (SKU) of the product|
|product_distribution_center_id|Numerical discrete|Id for the distribution center associated with the product|

## order_items
|Column|Data Type|Description|
|---|---|---|
|id|Numerical discrete|Unique id for each order item|
|order_id|Numerical discrete|Id of associated order|
|user_id|Numerical discrete|Id of associated user|
|product_id|Numerical discrete|Id of associated product|
|inventory_item_id|Numerical discrete|Id of associated inventory item|
|status|Categorical nomial|Status of the order item|
|created_at|Date-time|When the order item was created|
|shipped_at|Date-time|When the order was shipped|
|delivered_at|Date-time|When the order was delivered|
|returned_at|Date-time|When the order was returned|
|sale_price|Numerical continuous|Price of the order item|

## orders
|Column|Data Type|Description|
|---|---|---|
|order_id|Numerical discrete|Unique order id|
|user_id|Numerical discrete|Id of user who placed the order|
|status|Categorical nominal|Status of the order|
|gender|Categorical nominal|Gender of user who placed the order|
|created_at|Date-time|When the order was created|
|shipped_at|Date-time|When the order was shipped|
|delivered_at|Date-time|When the order was delivered|
|returned_at|Date-time|When the order was returned|
|num_of_item|Numerical discrete|Number of items in the order|

## products
|Column|Data Type|Description|
|---|---|---|
|id|Numerical discrete|Unique product id|
|cost|Numerical continuous|Product cost|
|name|Categorical nominal|Name of the product|
|brand|Categorical nominal|Brand of the product|
|retail_price|Numerical continuous|Retail price of the product|
|department|Categorical nominal|Department the product belongs to|
|sku|Categorical nominal|Stock Keeping Unit (SKU) of the product|
|distribution_center_id|Numerical discrete|Id of distribution center associated with the product.

## users
|Column|Data Type|Description|
|---|---|---|
|id|Numerical discrete|Unique user id|
|first_name|Categorical nominal|First name of the user|
|last_name|Categorical nominal|Last name of the user|
|email|Categorical nominal|Email address of the user|
|age|Numerical discrete|Age of the user|
|state|Categorical nominal|State of the user|
|street_address|Categorical nominal|Street address of the user|
|postal_code|Categorical nominal|Postal code of the user|
|city|Categorical nominal| City of the user|
|latitude|Numerical continuous|Latitude of the user|
|longitude|Numerical continuous|Longitude of the user|
|traffic_source|Traffic source leading to the user|
|created_at|Date-time|When the user account was created|