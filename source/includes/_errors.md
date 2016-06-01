# Errors

The Teamworks API uses the following error codes:

Error Code | Meaning
---------- | -------
200 OK | Indicates the request was successful. Used as success response code for all requests except for Inserts, which return a 201 Created.
201 Created | Indicates that a new resource was created successfully. The response will include a link to the new resource as a "Location" header as well as a "uri" parameter in the response body.
400 Invalid Request | The request failed due to issues with the data sent in the request. The response will include error message details.
401 Unauthorized | Either an Authorization header with API token was not included with the request or the token is invalid.
404 Not Found | The requested resource could not be found.
500 Server Error | The API server encountered an unexpected error and could not process your request. Teamworks technical support will be notified when these occur.
