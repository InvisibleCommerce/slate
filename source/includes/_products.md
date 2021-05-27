# Products

## Get All Products

```shell
curl "https://nexus-staging.invisiblecommerce.com/api/v1/products" \
  -H "Authorization: 1234567890987654321"
```

> The above command returns JSON structured like this:

```json
[
    {
        "id": 32,
        "name": "Diamond Naturals Beef Meal & Rice Formula Adult Dry Dog Food",
        "brand_name": "Diamond",
        "category_name": "Dog > Dry Food",
        "description_body": "Real beef protein, along with added super foods, provides the energy and muscle building blocks your dog needs to stay active and strong. Guaranteed levels of vitamin E and selenium ensure that your dog is receiving optimum antioxidant nutrition, while omega-6 and omega-3 fatty acids from super foods help maintain healthy skin and a shiny coat. \r\n- Real beef protein for superior taste and nutrition\r\n- Guaranteed levels of vitamin E and selenium\r\n- Omega-6 and omega-3 fatty acids for skin and coat\r\n- Enhanced with super foods and probiotics\r\n- No corn, no wheat, no soy",
        "variants": [
            {
                "id": 224,
                "name": "40-lb",
                "full_name": "Diamond Naturals Beef Meal & Rice Formula Adult Dry Dog Food (40-lb)",
                "price": "35.99",
                "retail_price": "43.99",
                "global_barcode": "074198608331"
            }
        ],
        "images": [
            "https://invisible-commerce-development.s3.us-west-1.amazonaws.com/1pnx6vr2vqn162zwg7chupizb24z?response-content-disposition=inline%3B%20filename%3D%2230771-1569514668.jpeg%22%3B%20filename%2A%3DUTF-8%27%2730771-1569514668.jpeg&response-content-type=image%2Fjpeg&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIATEU2MX3TZE6K3J7U%2F20210527%2Fus-west-1%2Fs3%2Faws4_request&X-Amz-Date=20210527T025848Z&X-Amz-Expires=300&X-Amz-SignedHeaders=host&X-Amz-Signature=7d72e291d65f48cf9c355b810b9cbf49de4a133c8c3f643edb1cc64e13f39724",
            "https://invisible-commerce-development.s3.us-west-1.amazonaws.com/pmt6begyv2ybjssjbnxjy8cnlhty?response-content-disposition=inline%3B%20filename%3D%2230771-1575318206.jpeg%22%3B%20filename%2A%3DUTF-8%27%2730771-1575318206.jpeg&response-content-type=image%2Fjpeg&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIATEU2MX3TZE6K3J7U%2F20210527%2Fus-west-1%2Fs3%2Faws4_request&X-Amz-Date=20210527T025848Z&X-Amz-Expires=300&X-Amz-SignedHeaders=host&X-Amz-Signature=faffcbac242a420ff044b60a9559802bf53c4784a02e987d7d06ea7660ef9320"
        ]
    },
    {
        "id": 33,
        "name": "Diamond Naturals Extreme Athlete Dry Dog Food",
        "brand_name": "Diamond",
        "category_name": "Dog > Dry Food",
        "description_body": "Diamond Naturals Extreme Athlete is specifically formulated with optimal levels of protein, fat and whole grain to fuel your hard-working dog. Omega fatty acids and antioxidants help support ideal muscle condition, helping your dog stay active, strong and fit. \r\n- Ideal for highly active and sporting dogs\r\n- Chicken and rice formula\r\n- Optimal levels of protein and fat\r\n- Enhanced with super foods and probiotics\r\n- No corn, no wheat, no soy",
        "variants": [
            {
                "id": 221,
                "name": "40-lb",
                "full_name": "Diamond Naturals Extreme Athlete Dry Dog Food (40-lb)",
                "price": "42.99",
                "retail_price": "51.99",
                "global_barcode": "074198609543"
            }
        ],
        "images": [
            "https://invisible-commerce-development.s3.us-west-1.amazonaws.com/arpwdkn1ftx5bftgbyn205d1ia7p?response-content-disposition=inline%3B%20filename%3D%2230773-1569515308.jpeg%22%3B%20filename%2A%3DUTF-8%27%2730773-1569515308.jpeg&response-content-type=image%2Fjpeg&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIATEU2MX3TZE6K3J7U%2F20210527%2Fus-west-1%2Fs3%2Faws4_request&X-Amz-Date=20210527T025848Z&X-Amz-Expires=300&X-Amz-SignedHeaders=host&X-Amz-Signature=d26b3a5637f0578514c7c48e3a17baa168ed1e238818c00a43caed19b595d47a"
        ]
    }
]
```

This endpoint retrieves all products.

### HTTP Request

`GET https://nexus-staging.invisiblecommerce.com/api/v1/products`

### Query Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| page | query | Page offset to fetch. | No | integer |
| per_page | query | Number of results to return per page. | No | integer |
| offset | query | Pad a number of results. | No | integer |

## Get a Specific Product

```shell
curl "https://nexus-staging.invisiblecommerce.com/api/v1/products/34" \
  -H "Authorization: 1234567890987654321"
```

> The above command returns JSON structured like this:

```json
{
    "id": 34,
    "name": "Diamond Naturals Grain Free Whitefish & Sweet Potato Dry Dog Food",
    "brand_name": "Diamond",
    "category_name": "Dog > Dry Food",
    "description_body": "Diamond Pet Foods is proud to offer Diamond Naturals Grain-Free. All of the Diamond Naturals Grain-Free formulas are made with superior animal protein sources and zero grains to optimize digestion and limit exposure to allergy triggers. These formulas all provide key nutrients essential to your dog's health and vitality.\r\n\r\nProduct Features:\r\n* Protein Blend, Real beef, chicken or fish protein sources provide dogs with the amino acid building blocks necessary for ideal lean body condition\r\n* Fruits and Veggies - Sweet potatoes, peas, garbanzo beans, potatoes, blueberries and raspberries provide an excellent spectrum of phytonutrients\r\n* Antioxidant Formulation - Guaranteed levels of selenium and vitamin E help support a healthy lifestyle.\r\n* Grain-free foods provide optimal nutrition for dogs sensitive to grain\r\n* Made in the USA!!!",
    "variants": [
        {
            "id": 225,
            "name": "28-lb",
            "full_name": "Diamond Naturals Grain Free Whitefish & Sweet Potato Dry Dog Food (28-lb)",
            "price": "41.99",
            "retail_price": "50.99",
            "global_barcode": "074198611553"
        },
        {
            "id": 6332,
            "name": "14-lb",
            "full_name": "Diamond Naturals Grain Free Whitefish & Sweet Potato Dry Dog Food (14-lb)",
            "price": "24.99",
            "retail_price": "29.99",
            "global_barcode": "074198611546"
        }
    ],
    "images": [
        "https://invisible-commerce-development.s3.us-west-1.amazonaws.com/6e0alc0pyuvrz86rui5mv00yu88x?response-content-disposition=inline%3B%20filename%3D%2233653-1569516624.jpeg%22%3B%20filename%2A%3DUTF-8%27%2733653-1569516624.jpeg&response-content-type=image%2Fjpeg&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIATEU2MX3TZE6K3J7U%2F20210527%2Fus-west-1%2Fs3%2Faws4_request&X-Amz-Date=20210527T025849Z&X-Amz-Expires=300&X-Amz-SignedHeaders=host&X-Amz-Signature=a944129d765f3939ecde1e2a31053d8adaccb8a6f5fbb0b7251ad27796ba7ec9"
    ]
}
```

This endpoint retrieves a specific product.

### HTTP Request

`GET https://nexus-staging.invisiblecommerce.com/api/v1/products/<ID>`

### URL Parameters

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| id | path |  | Yes | integer |

