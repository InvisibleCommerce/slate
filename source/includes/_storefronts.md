# Storefronts

## Get All Storefronts

```shell
curl "https://nexus.invisiblecommerce.com/api/v1/storefronts" \
  -H "Authorization: 1234567890987654321"
```

> The above command returns JSON structured like this:

```json
[
  {
        "id": 15,
        "name": "Happy Paws Rescue",
        "shelterluv_prefix": null,
        "recommended_variants": []
    },
    {
        "id": 14,
        "name": "IC Dev",
        "shelterluv_prefix": "TEST",
        "recommended_variants": [
            {
                "target": "Small Dog",
                "recurrence": {
                    "every": "week",
                    "interval": "4"
                },
                "variant": {
                    "id": 6424,
                    "name": "6-oz",
                    "full_name": "Zukes Chicken Mini Naturals Dog Treats (6-oz)",
                    "price": "5.99",
                    "retail_price": "7.99",
                    "global_barcode": "013423330517",
                    "product": {
                        "id": 116,
                        "name": "Zukes Chicken Mini Naturals Dog Treats",
                        "brand_name": "Zukes",
                        "category_name": "Dog > Treats",
                        "description_body": "Training is one of the biggest adventures you and your dog will set off on together. And with the right treat, you can keep each and every moment healthy and deliciously fun. At less than 3 calories per treat, Zuke's Mini Naturals dog treats are the perfect little size for use as a training treat, or perfect as a small breed dog treat. These soft and chewy dog treats are specially crafted in the USA using the Earth's best ingredients — like protein-rich meat, wholefood berries, savory herbs and NO corn, wheat or soy.\r\n\r\n\r\nWith less than 3 calories per treat, Zuke's Mini Naturals are ideal for use as training treats or as a small breed dog treats",
                        "images": [
                            "https://invisible-commerce-development.s3.us-west-1.amazonaws.com/cpe7cin1a3tkkqrs7rmf62qmexnu?response-content-disposition=inline%3B%20filename%3D%2212338-1578608193.jpeg%22%3B%20filename%2A%3DUTF-8%27%2712338-1578608193.jpeg&response-content-type=image%2Fjpeg&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIATEU2MX3TZE6K3J7U%2F20210527%2Fus-west-1%2Fs3%2Faws4_request&X-Amz-Date=20210527T203248Z&X-Amz-Expires=300&X-Amz-SignedHeaders=host&X-Amz-Signature=84f8b81d32d0d663c6c4ba69dfedb6fba0699796b657dc8572d6ebf7a0e224d2",
                            "https://invisible-commerce-development.s3.us-west-1.amazonaws.com/2qayweemricge0e3dlid1uum06qi?response-content-disposition=inline%3B%20filename%3D%2212338-1578608220.jpeg%22%3B%20filename%2A%3DUTF-8%27%2712338-1578608220.jpeg&response-content-type=image%2Fjpeg&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIATEU2MX3TZE6K3J7U%2F20210527%2Fus-west-1%2Fs3%2Faws4_request&X-Amz-Date=20210527T203248Z&X-Amz-Expires=300&X-Amz-SignedHeaders=host&X-Amz-Signature=29ee09720a6f101709900d9f720146ba24a4efad0f56d5db6e8c8955f5a82023"
                        ]
                    }
                }
            }
        ]
    }
]
```

This endpoint retrieves all storefronts. This endpoint supports [pagination](#pagination).

### HTTP Request

`GET /api/v1/storefronts`

### Query Parameters

| Name | Location | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| shelterluv_prefix | query | ID prefix used by Shelterluv | No | string |

<aside class="notice">
When querying by <code>shelterluv_prefix</code>, the result will always be an array of one, as the <code>shelterluv_prefix</code> is unique.
</aside>

## Get a Specific Storefront

```shell
curl "https://nexus.invisiblecommerce.com/api/v1/storefronts/14" \
  -H "Authorization: 1234567890987654321"
```

> The above command returns JSON structured like this:

```json
{
        "id": 14,
        "name": "IC Dev",
        "shelterluv_prefix": "TEST",
        "recommended_variants": [
            {
                "target": "Small Dog",
                "recurrence": {
                    "every": "week",
                    "interval": "4"
                },
                "variant": {
                    "id": 6424,
                    "name": "6-oz",
                    "full_name": "Zukes Chicken Mini Naturals Dog Treats (6-oz)",
                    "price": "5.99",
                    "retail_price": "7.99",
                    "global_barcode": "013423330517",
                    "product": {
                        "id": 116,
                        "name": "Zukes Chicken Mini Naturals Dog Treats",
                        "brand_name": "Zukes",
                        "category_name": "Dog > Treats",
                        "description_body": "Training is one of the biggest adventures you and your dog will set off on together. And with the right treat, you can keep each and every moment healthy and deliciously fun. At less than 3 calories per treat, Zuke's Mini Naturals dog treats are the perfect little size for use as a training treat, or perfect as a small breed dog treat. These soft and chewy dog treats are specially crafted in the USA using the Earth's best ingredients — like protein-rich meat, wholefood berries, savory herbs and NO corn, wheat or soy.\r\n\r\n\r\nWith less than 3 calories per treat, Zuke's Mini Naturals are ideal for use as training treats or as a small breed dog treats",
                        "images": [
                            "https://invisible-commerce-development.s3.us-west-1.amazonaws.com/cpe7cin1a3tkkqrs7rmf62qmexnu?response-content-disposition=inline%3B%20filename%3D%2212338-1578608193.jpeg%22%3B%20filename%2A%3DUTF-8%27%2712338-1578608193.jpeg&response-content-type=image%2Fjpeg&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIATEU2MX3TZE6K3J7U%2F20210527%2Fus-west-1%2Fs3%2Faws4_request&X-Amz-Date=20210527T203248Z&X-Amz-Expires=300&X-Amz-SignedHeaders=host&X-Amz-Signature=84f8b81d32d0d663c6c4ba69dfedb6fba0699796b657dc8572d6ebf7a0e224d2",
                            "https://invisible-commerce-development.s3.us-west-1.amazonaws.com/2qayweemricge0e3dlid1uum06qi?response-content-disposition=inline%3B%20filename%3D%2212338-1578608220.jpeg%22%3B%20filename%2A%3DUTF-8%27%2712338-1578608220.jpeg&response-content-type=image%2Fjpeg&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIATEU2MX3TZE6K3J7U%2F20210527%2Fus-west-1%2Fs3%2Faws4_request&X-Amz-Date=20210527T203248Z&X-Amz-Expires=300&X-Amz-SignedHeaders=host&X-Amz-Signature=29ee09720a6f101709900d9f720146ba24a4efad0f56d5db6e8c8955f5a82023"
                        ]
                    }
                }
            }
        ]
    }
```

This endpoint retrieves a specific storefront.

### HTTP Request

`GET /api/v1/storefronts/<ID>`

### URL Parameters

| Name | Location | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path | ID of the requested storefront | Yes | integer |
