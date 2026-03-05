# RagieRubySdk::ElementsApi

All URIs are relative to *https://api.ragie.ai*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_element**](ElementsApi.md#get_element) | **GET** /elements/{element_id} | Get Element For Document |
| [**list_elements**](ElementsApi.md#list_elements) | **GET** /documents/{document_id}/elements | List Elements For Document |


## get_element

> <ApiDocumentElement> get_element(element_id)

Get Element For Document

Returns an element for a specific id

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ElementsApi.new
element_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Get Element For Document
  result = api_instance.get_element(element_id)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ElementsApi->get_element: #{e}"
end
```

#### Using the get_element_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiDocumentElement>, Integer, Hash)> get_element_with_http_info(element_id)

```ruby
begin
  # Get Element For Document
  data, status_code, headers = api_instance.get_element_with_http_info(element_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiDocumentElement>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ElementsApi->get_element_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **element_id** | **String** |  |  |

### Return type

[**ApiDocumentElement**](ApiDocumentElement.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_elements

> <ListDocumentElements> list_elements(document_id, opts)

List Elements For Document

List the latest elements for a document. The results are sorted by index in ascending order. Results are paginated with a max limit of 100. When more elements are available, a `cursor` will be provided. Use the `cursor` parameter to retrieve the subsequent page

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ElementsApi.new
document_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
opts = {
  cursor: 'cursor_example', # String | An opaque cursor for pagination
  page_size: 56, # Integer | The number of items per page (must be greater than 0 and less than or equal to 100)
  type: [RagieRubySdk::DocumentElementType::CAPTION], # Array<DocumentElementType> | 
  index_start: 56, # Integer | 
  index_end: 56, # Integer | 
  partition: 'partition_example' # String | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition.
}

begin
  # List Elements For Document
  result = api_instance.list_elements(document_id, opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ElementsApi->list_elements: #{e}"
end
```

#### Using the list_elements_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListDocumentElements>, Integer, Hash)> list_elements_with_http_info(document_id, opts)

```ruby
begin
  # List Elements For Document
  data, status_code, headers = api_instance.list_elements_with_http_info(document_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListDocumentElements>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ElementsApi->list_elements_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |
| **cursor** | **String** | An opaque cursor for pagination | [optional] |
| **page_size** | **Integer** | The number of items per page (must be greater than 0 and less than or equal to 100) | [optional][default to 10] |
| **type** | [**Array&lt;DocumentElementType&gt;**](DocumentElementType.md) |  | [optional] |
| **index_start** | **Integer** |  | [optional] |
| **index_end** | **Integer** |  | [optional] |
| **partition** | **String** | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition. | [optional] |

### Return type

[**ListDocumentElements**](ListDocumentElements.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

