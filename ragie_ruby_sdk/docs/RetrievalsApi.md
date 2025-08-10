# OpenapiClient::RetrievalsApi

All URIs are relative to *https://api.ragie.ai*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**retrieve**](RetrievalsApi.md#retrieve) | **POST** /retrievals | Retrieve |


## retrieve

> <Retrieval> retrieve(retrieve_params)

Retrieve

### Examples

```ruby
require 'time'
require 'openapi_client'
# setup authorization
OpenapiClient.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = OpenapiClient::RetrievalsApi.new
retrieve_params = OpenapiClient::RetrieveParams.new({query: 'query_example'}) # RetrieveParams | 

begin
  # Retrieve
  result = api_instance.retrieve(retrieve_params)
  p result
rescue OpenapiClient::ApiError => e
  puts "Error when calling RetrievalsApi->retrieve: #{e}"
end
```

#### Using the retrieve_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Retrieval>, Integer, Hash)> retrieve_with_http_info(retrieve_params)

```ruby
begin
  # Retrieve
  data, status_code, headers = api_instance.retrieve_with_http_info(retrieve_params)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Retrieval>
rescue OpenapiClient::ApiError => e
  puts "Error when calling RetrievalsApi->retrieve_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **retrieve_params** | [**RetrieveParams**](RetrieveParams.md) |  |  |

### Return type

[**Retrieval**](Retrieval.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

