#  API Reference for Developers  v3

An API key is required for requests to be processed by the system. Once a user registers, an API key is automatically generated for this user. The API key must be sent with each request (see full example below). If the API key is not sent or is expired, there will be an error. Please make sure to keep your API key secret to prevent abuse.

##  Authentication

To authenticate with the API system, you need to send your API key as an authorization token with each request. You can see sample code below.

    curl --location --request POST 'https://socialtoapp.com/api/url/add' \ --header 'Authorization: Bearer YOURAPIKEY' \ --header 'Content-Type: application/json' \

##  Rate Limit

Our API has a rate limiter to safeguard against spike in requests to maximize its stability. Our rate limiter is currently caped at 30 requests per 1 minute.

Several headers will be sent alongside the response and these can be examined to determine various information about the request.
