--- 

title: Invisible Commerce API 

language_tabs: 
   - shell 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

API provides access to Invisible Commerce functions, including its subsidiary Ethical Paws 

**Version:** 0.0.1 

# Authentication 

|apiKey|*API Key*|
|---|---| 

# /V1/PRODUCTS/{ID}
## ***GET*** 

**Description:** Returns a specific Product by ID

### HTTP Request 
`***GET*** /v1/products/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Returns a specific Product by ID |

# /V1/PRODUCTS
## ***GET*** 

**Description:** Returns a list of Products

### HTTP Request 
`***GET*** /v1/products` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| page | query | Page offset to fetch. | No | integer |
| per_page | query | Number of results to return per page. | No | integer |
| offset | query | Pad a number of results. | No | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Returns a list of Products |

# /V1/STOREFRONTS/{ID}
## ***GET*** 

**Description:** Returns a specific Storefront by ID

### HTTP Request 
`***GET*** /v1/storefronts/{id}` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes | integer |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Returns a specific Storefront by ID |

# /V1/STOREFRONTS
## ***GET*** 

**Description:** Returns a list of Storefronts

### HTTP Request 
`***GET*** /v1/storefronts` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| page | query | Page offset to fetch. | No | integer |
| per_page | query | Number of results to return per page. | No | integer |
| offset | query | Pad a number of results. | No | integer |
| shelterluv_prefix | query |  | No | string |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Returns a list of Storefronts |

# /V1/PRODUCT_SUBSCRIPTIONS
## ***POST*** 

**Description:** Creates a Product Subscription

### HTTP Request 
`***POST*** /v1/product_subscriptions` 

**Parameters**

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| V1ProductSubscriptions | body |  | Yes |  |

**Responses**

| Code | Description |
| ---- | ----------- |
| 201 | Creates a Product Subscription |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
