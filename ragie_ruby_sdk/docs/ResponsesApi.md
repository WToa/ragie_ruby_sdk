# RagieRubySdk::ResponsesApi

All URIs are relative to *https://api.ragie.ai*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_response_responses_post**](ResponsesApi.md#create_response_responses_post) | **POST** /responses | Create Response |
| [**get_response_responses_response_id_get**](ResponsesApi.md#get_response_responses_response_id_get) | **GET** /responses/{response_id} | Get Response |


## create_response_responses_post

> <Response> create_response_responses_post(request)

Create Response

Create a response. This will generate an LLM or agentic response. At this time the only supported model is `deep-search`. Responses may be streamed or returned synchronously. The `retrieve` tool is currently the only supported tool, more tools will be added in the future. A single partition may be provided in the retrieve tool. If omitted the `default` partition is used.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ResponsesApi.new
request = RagieRubySdk::Request.new({input: 'input_example'}) # Request | 

begin
  # Create Response
  result = api_instance.create_response_responses_post(request)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ResponsesApi->create_response_responses_post: #{e}"
end
```

#### Using the create_response_responses_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Response>, Integer, Hash)> create_response_responses_post_with_http_info(request)

```ruby
begin
  # Create Response
  data, status_code, headers = api_instance.create_response_responses_post_with_http_info(request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Response>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ResponsesApi->create_response_responses_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **request** | [**Request**](Request.md) |  |  |

### Return type

[**Response**](Response.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_response_responses_response_id_get

> <Response> get_response_responses_response_id_get(response_id)

Get Response

Get a response by its ID. This will return the response and its status. If the response is still in progress, the status will be `in_progress`. If the response is completed, the status will be `completed`. If the response is failed, the status will be `failed`.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ResponsesApi.new
response_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Get Response
  result = api_instance.get_response_responses_response_id_get(response_id)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ResponsesApi->get_response_responses_response_id_get: #{e}"
end
```

#### Using the get_response_responses_response_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Response>, Integer, Hash)> get_response_responses_response_id_get_with_http_info(response_id)

```ruby
begin
  # Get Response
  data, status_code, headers = api_instance.get_response_responses_response_id_get_with_http_info(response_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Response>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ResponsesApi->get_response_responses_response_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **response_id** | **String** |  |  |

### Return type

[**Response**](Response.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

