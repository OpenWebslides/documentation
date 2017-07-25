# Errors

## HTTP status code

<aside class="notice">This error section is stored in a separate file in `includes/_errors.md`. Slate allows you to optionally separate out your docs into many files...just save them to the `includes` folder and add them to the top of your `index.md`'s frontmatter. Files are included in the order listed.</aside>

The API uses the following HTTP error codes:


Status code | Description
---------- | -------
400 | Bad Request -- Invalid data or URL
401 | Unauthorized -- Invalid or no API token
403 | Forbidden -- Not authorized to perform action
404 | Not Found
405 | Method Not Allowed
406 | Not Acceptable -- `Content-Type` should be `application/vnd.api+json`
410 | Gone -- Resource has been removed
422 | Unprocessable Entity -- Malformed `data` object
429 | Too Many Requests -- Rate limiting in effect (to be included in future updates)
500 | Internal Server Error -- The server had a problem. Please try again later.
503 | Service Unavailable -- Temporarily offline for maintenance. Please try again later.

## JSON API error code

Besides HTTP status codes, the API provides additional error codes in the returned `errors` object under the `code` variable:

Error code | Description
---------- | -------
100 | Validation error
101 | Invalid resource
102 | Filter not allowed
103 | Invalid field value
104 | Invalid field
105 | Param not allowed
106 | Param missing
107 | Invalid filter value
109 | Key order mismatch
110 | Key not included in URL
112 | Invalid include
113 | Relation exists
114 | Invalid sort criteria
115 | Invalid links object
116 | Type mismatch
117 | Invalid page object
118 | Invalid page value
119 | Invalid field format
120 | Invalid filters syntax
121 | Save failed
122 | Invalid data format
400 | Bad request
403 | Forbidden
404 | Record not found
406 | Not acceptable
415 | Unsupported media type
423 | Locked
500 | Internal server error
