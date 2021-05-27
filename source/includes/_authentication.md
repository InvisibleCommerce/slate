# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here" \
  -H "Authorization: 1234567890987654321"
```

> Make sure to replace `1234567890987654321` with your API key.

Invisible Commerce uses API keys to allow access to the API. Our engineering team will provide you with an API key for our Staging environment. 

The API key must be included in all API requests to the server in an Authorization header:

`Authorization: 1234567890987654321`

Please notify us immediately if your token is compromised. We are also able to provide an additional token to aid in token rotation. 
<aside class="notice">
You must replace <code>1234567890987654321</code> with the API key supplied to you by our engineering team. 
</aside>