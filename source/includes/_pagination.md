# Pagination

### Query Parameters

Pagination can be achieved by using the following parameters on endpoints that support pagination:

| Name | Located in | Description | Required | Type |
| ---- | ---------- | ----------- | -------- | ---- |
| page | query | Page offset to fetch. | No | integer |
| per_page | query | Number of results to return per page. | No | integer |
| offset | query | Pad a number of results. | No | integer |

### Pagination Headers

Endpoints that support pagination will also provide pagination information in the response headers:

| Name | Description | Type |
| ---- | ----------- | ---- |
| X-Total | Total number of matching records. |integer |
| X-Per-Page |  Number of records being returned per page. | integer |
| X-Total-Pages | Total number of pages. |integer |
| X-Page | Current page number being returned. |integer |
| X-Next-Page | Page number for the next page. |integer |
| X-Prev-Page | Page number for the previous page. |integer |
| X-Offset | Number of records skipped. |integer |

<aside class="notice">
A maximum <code>per_page</code> of 100 is supported. The default is 20.  
</aside>