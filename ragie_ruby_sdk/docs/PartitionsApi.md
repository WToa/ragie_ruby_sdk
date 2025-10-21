# RagieRubySdk::PartitionsApi

All URIs are relative to *https://api.ragie.ai*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_partition_partitions_post**](PartitionsApi.md#create_partition_partitions_post) | **POST** /partitions | Create Partition |
| [**delete_partition_partitions_partition_id_delete**](PartitionsApi.md#delete_partition_partitions_partition_id_delete) | **DELETE** /partitions/{partition_id} | Delete Partition |
| [**get_partition_partitions_partition_id_get**](PartitionsApi.md#get_partition_partitions_partition_id_get) | **GET** /partitions/{partition_id} | Get Partition |
| [**list_partitions_partitions_get**](PartitionsApi.md#list_partitions_partitions_get) | **GET** /partitions | List Partitions |
| [**set_partition_limits_partitions_partition_id_limits_put**](PartitionsApi.md#set_partition_limits_partitions_partition_id_limits_put) | **PUT** /partitions/{partition_id}/limits | Set Partition Limits |
| [**update_partition_partitions_partition_id_patch**](PartitionsApi.md#update_partition_partitions_partition_id_patch) | **PATCH** /partitions/{partition_id} | Update Partition |


## create_partition_partitions_post

> <Partition> create_partition_partitions_post(create_partition_params)

Create Partition

Create a new partition. Partitions are used to scope documents, connections, and instructions. Partitions must be lowercase alphanumeric and may only include the special characters `_` and `-`. A partition may also be created by creating a document in it. Limits for a partition may optionally be defined when creating.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::PartitionsApi.new
create_partition_params = RagieRubySdk::CreatePartitionParams.new({name: 'name_example'}) # CreatePartitionParams | 

begin
  # Create Partition
  result = api_instance.create_partition_partitions_post(create_partition_params)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling PartitionsApi->create_partition_partitions_post: #{e}"
end
```

#### Using the create_partition_partitions_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Partition>, Integer, Hash)> create_partition_partitions_post_with_http_info(create_partition_params)

```ruby
begin
  # Create Partition
  data, status_code, headers = api_instance.create_partition_partitions_post_with_http_info(create_partition_params)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Partition>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling PartitionsApi->create_partition_partitions_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_partition_params** | [**CreatePartitionParams**](CreatePartitionParams.md) |  |  |

### Return type

[**Partition**](Partition.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_partition_partitions_partition_id_delete

> Hash&lt;String, String&gt; delete_partition_partitions_partition_id_delete(partition_id)

Delete Partition

Deletes a partition and all of its associated data. This includes connections, documents, and partition specific instructions. This operation is irreversible.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::PartitionsApi.new
partition_id = 'partition_id_example' # String | 

begin
  # Delete Partition
  result = api_instance.delete_partition_partitions_partition_id_delete(partition_id)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling PartitionsApi->delete_partition_partitions_partition_id_delete: #{e}"
end
```

#### Using the delete_partition_partitions_partition_id_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, String&gt;, Integer, Hash)> delete_partition_partitions_partition_id_delete_with_http_info(partition_id)

```ruby
begin
  # Delete Partition
  data, status_code, headers = api_instance.delete_partition_partitions_partition_id_delete_with_http_info(partition_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, String&gt;
rescue RagieRubySdk::ApiError => e
  puts "Error when calling PartitionsApi->delete_partition_partitions_partition_id_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **partition_id** | **String** |  |  |

### Return type

**Hash&lt;String, String&gt;**

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_partition_partitions_partition_id_get

> <PartitionDetail> get_partition_partitions_partition_id_get(partition_id)

Get Partition

Get a partition by its ID. Includes usage information such as the number of documents and pages hosted and processed. The partition's limits are also included.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::PartitionsApi.new
partition_id = 'partition_id_example' # String | 

begin
  # Get Partition
  result = api_instance.get_partition_partitions_partition_id_get(partition_id)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling PartitionsApi->get_partition_partitions_partition_id_get: #{e}"
end
```

#### Using the get_partition_partitions_partition_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PartitionDetail>, Integer, Hash)> get_partition_partitions_partition_id_get_with_http_info(partition_id)

```ruby
begin
  # Get Partition
  data, status_code, headers = api_instance.get_partition_partitions_partition_id_get_with_http_info(partition_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PartitionDetail>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling PartitionsApi->get_partition_partitions_partition_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **partition_id** | **String** |  |  |

### Return type

[**PartitionDetail**](PartitionDetail.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_partitions_partitions_get

> <PartitionList> list_partitions_partitions_get(opts)

List Partitions

List all partitions sorted by name in ascending order. Results are paginated with a max limit of 100. When more partitions are available, a `cursor` will be provided. Use the `cursor` parameter to retrieve the subsequent page.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::PartitionsApi.new
opts = {
  cursor: 'cursor_example', # String | An opaque cursor for pagination
  page_size: 56 # Integer | The number of items per page (must be greater than 0 and less than or equal to 100)
}

begin
  # List Partitions
  result = api_instance.list_partitions_partitions_get(opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling PartitionsApi->list_partitions_partitions_get: #{e}"
end
```

#### Using the list_partitions_partitions_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PartitionList>, Integer, Hash)> list_partitions_partitions_get_with_http_info(opts)

```ruby
begin
  # List Partitions
  data, status_code, headers = api_instance.list_partitions_partitions_get_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PartitionList>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling PartitionsApi->list_partitions_partitions_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **cursor** | **String** | An opaque cursor for pagination | [optional] |
| **page_size** | **Integer** | The number of items per page (must be greater than 0 and less than or equal to 100) | [optional][default to 10] |

### Return type

[**PartitionList**](PartitionList.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## set_partition_limits_partitions_partition_id_limits_put

> <PartitionDetail> set_partition_limits_partitions_partition_id_limits_put(partition_id, partition_limit_params)

Set Partition Limits

Sets limits on a partition. Limits can be set on the total number of pages a partition can host and process. When the limit is reached, the partition will be disabled. A limit may be removed by setting it to `null`.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::PartitionsApi.new
partition_id = 'partition_id_example' # String | 
partition_limit_params = RagieRubySdk::PartitionLimitParams.new # PartitionLimitParams | 

begin
  # Set Partition Limits
  result = api_instance.set_partition_limits_partitions_partition_id_limits_put(partition_id, partition_limit_params)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling PartitionsApi->set_partition_limits_partitions_partition_id_limits_put: #{e}"
end
```

#### Using the set_partition_limits_partitions_partition_id_limits_put_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PartitionDetail>, Integer, Hash)> set_partition_limits_partitions_partition_id_limits_put_with_http_info(partition_id, partition_limit_params)

```ruby
begin
  # Set Partition Limits
  data, status_code, headers = api_instance.set_partition_limits_partitions_partition_id_limits_put_with_http_info(partition_id, partition_limit_params)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PartitionDetail>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling PartitionsApi->set_partition_limits_partitions_partition_id_limits_put_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **partition_id** | **String** |  |  |
| **partition_limit_params** | [**PartitionLimitParams**](PartitionLimitParams.md) |  |  |

### Return type

[**PartitionDetail**](PartitionDetail.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_partition_partitions_partition_id_patch

> <PartitionDetail> update_partition_partitions_partition_id_patch(partition_id, update_partition_params)

Update Partition

Updates a partition. This includes the partition's description and metadata schema.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::PartitionsApi.new
partition_id = 'partition_id_example' # String | 
update_partition_params = RagieRubySdk::UpdatePartitionParams.new # UpdatePartitionParams | 

begin
  # Update Partition
  result = api_instance.update_partition_partitions_partition_id_patch(partition_id, update_partition_params)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling PartitionsApi->update_partition_partitions_partition_id_patch: #{e}"
end
```

#### Using the update_partition_partitions_partition_id_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PartitionDetail>, Integer, Hash)> update_partition_partitions_partition_id_patch_with_http_info(partition_id, update_partition_params)

```ruby
begin
  # Update Partition
  data, status_code, headers = api_instance.update_partition_partitions_partition_id_patch_with_http_info(partition_id, update_partition_params)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PartitionDetail>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling PartitionsApi->update_partition_partitions_partition_id_patch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **partition_id** | **String** |  |  |
| **update_partition_params** | [**UpdatePartitionParams**](UpdatePartitionParams.md) |  |  |

### Return type

[**PartitionDetail**](PartitionDetail.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

