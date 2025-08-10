# OpenapiClient::DefaultApi

All URIs are relative to *https://api.ragie.ai*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**eventevent_post**](DefaultApi.md#eventevent_post) | **POST** /event | Event |


## eventevent_post

> Object eventevent_post(body)

Event

When events occur in Ragie such as a document being processed, we'll send this data to URLs that you can register in app. Learn more about webhooks in our docs: https://docs.ragie.ai/docs/webhooks.

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = OpenapiClient::DefaultApi.new
body =  # Body | 

begin
  # Event
  result = api_instance.eventevent_post(body)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling DefaultApi->eventevent_post: #{e}"
end
```

#### Using the eventevent_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> eventevent_post_with_http_info(body)

```ruby
begin
  # Event
  data, status_code, headers = api_instance.eventevent_post_with_http_info(body)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue OpenapiClient::ApiError => e
  puts "Error when calling DefaultApi->eventevent_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **body** | [**Body**](Body.md) |  |  |

### Return type

**Object**

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

