# RagieRubySdk::WebhookEndpointsApi

All URIs are relative to *https://api.ragie.ai*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_webhook_endpoint**](WebhookEndpointsApi.md#create_webhook_endpoint) | **POST** /webhook_endpoints | Create Webhook Endpoint |
| [**delete_webhook_endpoint**](WebhookEndpointsApi.md#delete_webhook_endpoint) | **DELETE** /webhook_endpoints/{endpoint_id} | Delete Webhook Endpoint |
| [**get_webhook_endpoint**](WebhookEndpointsApi.md#get_webhook_endpoint) | **GET** /webhook_endpoints/{endpoint_id} | Get Webhook Endpoint |
| [**list_webhook_endpoints**](WebhookEndpointsApi.md#list_webhook_endpoints) | **GET** /webhook_endpoints | List Webhook Endpoints |
| [**update_webhook_endpoint**](WebhookEndpointsApi.md#update_webhook_endpoint) | **PATCH** /webhook_endpoints/{endpoint_id} | Update Webhook Endpoint |


## create_webhook_endpoint

> <WebhookEndpoint> create_webhook_endpoint(create_webhook_endpoint_payload)

Create Webhook Endpoint

Create a webhook endpoint to receive notifications about document status updates, connection sync progress, partition limits, and other tenant events.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::WebhookEndpointsApi.new
create_webhook_endpoint_payload = RagieRubySdk::CreateWebhookEndpointPayload.new({name: 'name_example', url: 'url_example'}) # CreateWebhookEndpointPayload | 

begin
  # Create Webhook Endpoint
  result = api_instance.create_webhook_endpoint(create_webhook_endpoint_payload)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling WebhookEndpointsApi->create_webhook_endpoint: #{e}"
end
```

#### Using the create_webhook_endpoint_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookEndpoint>, Integer, Hash)> create_webhook_endpoint_with_http_info(create_webhook_endpoint_payload)

```ruby
begin
  # Create Webhook Endpoint
  data, status_code, headers = api_instance.create_webhook_endpoint_with_http_info(create_webhook_endpoint_payload)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookEndpoint>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling WebhookEndpointsApi->create_webhook_endpoint_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_webhook_endpoint_payload** | [**CreateWebhookEndpointPayload**](CreateWebhookEndpointPayload.md) |  |  |

### Return type

[**WebhookEndpoint**](WebhookEndpoint.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_webhook_endpoint

> <ResponseOK> delete_webhook_endpoint(endpoint_id)

Delete Webhook Endpoint

Delete a webhook endpoint to stop delivering webhook notifications to its URL.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::WebhookEndpointsApi.new
endpoint_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Delete Webhook Endpoint
  result = api_instance.delete_webhook_endpoint(endpoint_id)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling WebhookEndpointsApi->delete_webhook_endpoint: #{e}"
end
```

#### Using the delete_webhook_endpoint_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ResponseOK>, Integer, Hash)> delete_webhook_endpoint_with_http_info(endpoint_id)

```ruby
begin
  # Delete Webhook Endpoint
  data, status_code, headers = api_instance.delete_webhook_endpoint_with_http_info(endpoint_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ResponseOK>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling WebhookEndpointsApi->delete_webhook_endpoint_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **endpoint_id** | **String** |  |  |

### Return type

[**ResponseOK**](ResponseOK.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_webhook_endpoint

> <WebhookEndpoint> get_webhook_endpoint(endpoint_id)

Get Webhook Endpoint

Get a webhook endpoint by its id.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::WebhookEndpointsApi.new
endpoint_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Get Webhook Endpoint
  result = api_instance.get_webhook_endpoint(endpoint_id)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling WebhookEndpointsApi->get_webhook_endpoint: #{e}"
end
```

#### Using the get_webhook_endpoint_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookEndpoint>, Integer, Hash)> get_webhook_endpoint_with_http_info(endpoint_id)

```ruby
begin
  # Get Webhook Endpoint
  data, status_code, headers = api_instance.get_webhook_endpoint_with_http_info(endpoint_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookEndpoint>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling WebhookEndpointsApi->get_webhook_endpoint_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **endpoint_id** | **String** |  |  |

### Return type

[**WebhookEndpoint**](WebhookEndpoint.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_webhook_endpoints

> <WebhookEndpointList> list_webhook_endpoints(opts)

List Webhook Endpoints

List all webhook endpoints sorted by created_at in descending order. Results are paginated with a max limit of 100. When more endpoints are available, a `cursor` will be provided. Use the `cursor` parameter to retrieve the subsequent page.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::WebhookEndpointsApi.new
opts = {
  cursor: 'cursor_example', # String | An opaque cursor for pagination
  page_size: 56 # Integer | The number of items per page (must be greater than 0 and less than or equal to 100)
}

begin
  # List Webhook Endpoints
  result = api_instance.list_webhook_endpoints(opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling WebhookEndpointsApi->list_webhook_endpoints: #{e}"
end
```

#### Using the list_webhook_endpoints_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookEndpointList>, Integer, Hash)> list_webhook_endpoints_with_http_info(opts)

```ruby
begin
  # List Webhook Endpoints
  data, status_code, headers = api_instance.list_webhook_endpoints_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookEndpointList>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling WebhookEndpointsApi->list_webhook_endpoints_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **cursor** | **String** | An opaque cursor for pagination | [optional] |
| **page_size** | **Integer** | The number of items per page (must be greater than 0 and less than or equal to 100) | [optional][default to 10] |

### Return type

[**WebhookEndpointList**](WebhookEndpointList.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_webhook_endpoint

> <WebhookEndpoint> update_webhook_endpoint(endpoint_id, update_webhook_endpoint_payload)

Update Webhook Endpoint

Update a webhook endpoint's name, URL, or active status. Use this to rotate endpoints or temporarily disable delivery without deleting the endpoint.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::WebhookEndpointsApi.new
endpoint_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
update_webhook_endpoint_payload = RagieRubySdk::UpdateWebhookEndpointPayload.new # UpdateWebhookEndpointPayload | 

begin
  # Update Webhook Endpoint
  result = api_instance.update_webhook_endpoint(endpoint_id, update_webhook_endpoint_payload)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling WebhookEndpointsApi->update_webhook_endpoint: #{e}"
end
```

#### Using the update_webhook_endpoint_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookEndpoint>, Integer, Hash)> update_webhook_endpoint_with_http_info(endpoint_id, update_webhook_endpoint_payload)

```ruby
begin
  # Update Webhook Endpoint
  data, status_code, headers = api_instance.update_webhook_endpoint_with_http_info(endpoint_id, update_webhook_endpoint_payload)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookEndpoint>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling WebhookEndpointsApi->update_webhook_endpoint_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **endpoint_id** | **String** |  |  |
| **update_webhook_endpoint_payload** | [**UpdateWebhookEndpointPayload**](UpdateWebhookEndpointPayload.md) |  |  |

### Return type

[**WebhookEndpoint**](WebhookEndpoint.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

