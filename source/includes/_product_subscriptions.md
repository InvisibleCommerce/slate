# Product Subscriptions

## Create a Product Subscription

> Sample request payload:

```json
{
    "storefront_id": 14, 
    "address": {
        "first_name": "John",
        "last_name": "Doe",
        "address1": "123 Main St",
        "address2": "",
        "city": "Springfield",
        "state": "IL",
        "zip": "22803",
        "phone": "888-111-4343",
        "country": "US"
    },
    "customer": {
        "email": "john.doe@johndoe.com",
        "first_name": "John",
        "last_name": "Doe"
    },
    "stripe_token": "tok_1Iv7zqE13IfS2ayBawZXcrpH",
    "items": [
        {
            "variant_id": 6428,
            "quantity": 1
        }
    ],
    "recurrence": {
        "every": "week",
        "interval": 6
    }
}
```

> Sample response payload:

```json
{
    "number": "PS-2243846360",
    "storefront": {
        "id": 14,
        "name": "IC Dev",
        "shelterluv_prefix": "TEST"
    },
    "customer": {
        "email": "john.doe@johndoe.com",
        "first_name": "John",
        "last_name": "Doe"
    },
    "address": {
        "first_name": "John",
        "last_name": "Doe",
        "address1": "123 Main St",
        "address2": null,
        "city": "Springfield",
        "state": "IL",
        "zip": "22803",
        "country": "US",
        "phone": "888-111-4343"
    },
    "product_subscription_items": [
        {
            "variant": {
                "id": 6428,
                "name": "3-inch",
                "full_name": "Redbarn Peanut Butter Filled Bone For Dogs (3-inch)",
                "price": "5.01",
                "retail_price": "5.99",
                "global_barcode": "785184403037"
            },
            "quantity": 1,
            "price": "5.01"
        }
    ],
    "recurrence": {
        "every": "week",
        "interval": 6
    },
    "status": "new"
}
```

This endpoint creates a product subscription. 

### HTTP Request

`POST /api/v1/product_subscriptions`

### Payload Parameters

| Name | Location | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| storefront_id | body | ID of the Storefront the Product Subscription is related to | Yes | integer |
| stripe_token | body | Stripe token used to charge the customer | Yes | string |
| address[first_name] | body | Shipping address first name | Yes | string |
| address[last_name] | body | Shipping address last name | Yes | string |
| address[address1] | body | Shipping address line 1 | Yes | string |
| address[address2] | body | Shipping address line 2 | No | string |
| address[city] | body | Shipping address city | Yes | string |
| address[state] | body | Shipping address state | Yes | string |
| address[zip] | body | Shipping address ZIP code | Yes | string |
| address[country] | body | Shipping address country | No | string |
| address[phone] | body | Shipping address phone number | Yes | string |
| customer[email] | body | Customer's email address | Yes | string |
| customer[first_name] | body | Customer's first name | Yes | string |
| customer[last_name] | body | Customer's last name | Yes | string |
| items\[\][variant_id] | body | ID of Variant to subscribe to | Yes | Integer |
| items\[\][quantity] | body | Quantity of the Variant to subscribe to | Yes | Integer |
| recurrence[every] | body | Unit of recurrence, e.g. week for "every 4 weeks" | Yes | string |
| recurrence[interval] | body | Number of units between each recurrence, e.g. 4 for "every 4 weeks" | Yes | Integer |

### Validations

- `stripe_token` must be a valid token available in our Stripe account (use Stripe test mode with Staging environment). The endpoint will return a 400 error if it is not valid.
- `address[state]` must be a 2-letter state code, e.g. `IL`
- `address[country]` can only be 'US'. Given that only one value is possible, it can optionally be omitted from the request. 
- `customer[email]` must be a valid email. 
- `items[][quantity]` can optionally be omitted, in which case it will default to a value of `1`.
- `recurrence[every]` can only be one of the following 3 values: `day`, `week`, or `month`.
