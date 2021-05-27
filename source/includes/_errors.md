# Errors

### Error Messages

In general, when you encounter an error, you will receive JSON in the body of the response, detailing specifics of the error, e.g.:

`{ error: "storefront_id is empty" }`

### Error Codes

You may encounter some of the following errors:

Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request is invalid. 
401 | Unauthorized -- Your API key is wrong.
404 | Not Found -- A specified entity could not be found.
405 | Not Allowed -- Method not allowed on endpoint. 
500 | Internal Server Error -- We had an unexpected problem. Please contact our engineering team if it does not resolve itself. 
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
