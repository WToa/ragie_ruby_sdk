# RagieRubySdk::ConnectionsApi

All URIs are relative to *https://api.ragie.ai*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_connection**](ConnectionsApi.md#create_connection) | **POST** /connection | Create Connection |
| [**create_oauth_redirect_url_connections_oauth_post**](ConnectionsApi.md#create_oauth_redirect_url_connections_oauth_post) | **POST** /connections/oauth | Create Oauth Redirect Url |
| [**delete_connection_connections_connection_id_delete_post**](ConnectionsApi.md#delete_connection_connections_connection_id_delete_post) | **POST** /connections/{connection_id}/delete | Delete Connection |
| [**get_connection_connections_connection_id_get**](ConnectionsApi.md#get_connection_connections_connection_id_get) | **GET** /connections/{connection_id} | Get Connection |
| [**get_connection_stats_connections_connection_id_stats_get**](ConnectionsApi.md#get_connection_stats_connections_connection_id_stats_get) | **GET** /connections/{connection_id}/stats | Get Connection Stats |
| [**list_connection_source_types_connections_source_type_get**](ConnectionsApi.md#list_connection_source_types_connections_source_type_get) | **GET** /connections/source-type | List Connection Source Types |
| [**list_connections_connections_get**](ConnectionsApi.md#list_connections_connections_get) | **GET** /connections | List Connections |
| [**set_connection_enabled_connections_connection_id_enabled_put**](ConnectionsApi.md#set_connection_enabled_connections_connection_id_enabled_put) | **PUT** /connections/{connection_id}/enabled | Set Connection Enabled |
| [**set_connection_limits_connections_connection_id_limit_put**](ConnectionsApi.md#set_connection_limits_connections_connection_id_limit_put) | **PUT** /connections/{connection_id}/limit | Set Connection Limits |
| [**sync_connection**](ConnectionsApi.md#sync_connection) | **POST** /connections/{connection_id}/sync | Sync Connection |
| [**update_connection_connections_connection_id_put**](ConnectionsApi.md#update_connection_connections_connection_id_put) | **PUT** /connections/{connection_id} | Update Connection |


## create_connection

> <Connection> create_connection(public_create_connection)

Create Connection

Create a connection. This is only for non-oauth connections such as S3 compatible connections, Freshdesk, and Zendesk.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ConnectionsApi.new
public_create_connection = RagieRubySdk::PublicCreateConnection.new({partition_strategy: RagieRubySdk::MediaModeParam.new, connection: RagieRubySdk::PublicBackblazeConnection.new({provider: 'backblaze', data: RagieRubySdk::BucketData.new({bucket: 'bucket_example'}), credentials: RagieRubySdk::BackblazeCredentials.new({key_id: 'key_id_example', application_key: 'application_key_example', region: 'region_example', endpoint: 'endpoint_example'})})}) # PublicCreateConnection | 

begin
  # Create Connection
  result = api_instance.create_connection(public_create_connection)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->create_connection: #{e}"
end
```

#### Using the create_connection_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Connection>, Integer, Hash)> create_connection_with_http_info(public_create_connection)

```ruby
begin
  # Create Connection
  data, status_code, headers = api_instance.create_connection_with_http_info(public_create_connection)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Connection>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->create_connection_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **public_create_connection** | [**PublicCreateConnection**](PublicCreateConnection.md) |  |  |

### Return type

[**Connection**](Connection.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_oauth_redirect_url_connections_oauth_post

> <OAuthUrlResponse> create_oauth_redirect_url_connections_oauth_post(o_auth_url_create)

Create Oauth Redirect Url

Creates a redirect url to redirect the user to when initializing an embedded connector.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ConnectionsApi.new
o_auth_url_create = RagieRubySdk::OAuthUrlCreate.new({redirect_uri: 'redirect_uri_example'}) # OAuthUrlCreate | 

begin
  # Create Oauth Redirect Url
  result = api_instance.create_oauth_redirect_url_connections_oauth_post(o_auth_url_create)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->create_oauth_redirect_url_connections_oauth_post: #{e}"
end
```

#### Using the create_oauth_redirect_url_connections_oauth_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OAuthUrlResponse>, Integer, Hash)> create_oauth_redirect_url_connections_oauth_post_with_http_info(o_auth_url_create)

```ruby
begin
  # Create Oauth Redirect Url
  data, status_code, headers = api_instance.create_oauth_redirect_url_connections_oauth_post_with_http_info(o_auth_url_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OAuthUrlResponse>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->create_oauth_redirect_url_connections_oauth_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **o_auth_url_create** | [**OAuthUrlCreate**](OAuthUrlCreate.md) |  |  |

### Return type

[**OAuthUrlResponse**](OAuthUrlResponse.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_connection_connections_connection_id_delete_post

> Hash&lt;String, String&gt; delete_connection_connections_connection_id_delete_post(connection_id, delete_connection_payload)

Delete Connection

Schedules a connection to be deleted. You can choose to keep the files from the connection or delete them all. If you keep the files, they will no longer be associated to the connection. Deleting can take some time, so you will still see files for a bit after this is called.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ConnectionsApi.new
connection_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
delete_connection_payload = RagieRubySdk::DeleteConnectionPayload.new({keep_files: false}) # DeleteConnectionPayload | 

begin
  # Delete Connection
  result = api_instance.delete_connection_connections_connection_id_delete_post(connection_id, delete_connection_payload)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->delete_connection_connections_connection_id_delete_post: #{e}"
end
```

#### Using the delete_connection_connections_connection_id_delete_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, String&gt;, Integer, Hash)> delete_connection_connections_connection_id_delete_post_with_http_info(connection_id, delete_connection_payload)

```ruby
begin
  # Delete Connection
  data, status_code, headers = api_instance.delete_connection_connections_connection_id_delete_post_with_http_info(connection_id, delete_connection_payload)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, String&gt;
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->delete_connection_connections_connection_id_delete_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |
| **delete_connection_payload** | [**DeleteConnectionPayload**](DeleteConnectionPayload.md) |  |  |

### Return type

**Hash&lt;String, String&gt;**

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_connection_connections_connection_id_get

> <Connection> get_connection_connections_connection_id_get(connection_id)

Get Connection

Get a connection.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ConnectionsApi.new
connection_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Get Connection
  result = api_instance.get_connection_connections_connection_id_get(connection_id)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->get_connection_connections_connection_id_get: #{e}"
end
```

#### Using the get_connection_connections_connection_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Connection>, Integer, Hash)> get_connection_connections_connection_id_get_with_http_info(connection_id)

```ruby
begin
  # Get Connection
  data, status_code, headers = api_instance.get_connection_connections_connection_id_get_with_http_info(connection_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Connection>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->get_connection_connections_connection_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |

### Return type

[**Connection**](Connection.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_connection_stats_connections_connection_id_stats_get

> <ConnectionStats> get_connection_stats_connections_connection_id_stats_get(connection_id)

Get Connection Stats

Lists connection stats: total documents active documents, total active pages.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ConnectionsApi.new
connection_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Get Connection Stats
  result = api_instance.get_connection_stats_connections_connection_id_stats_get(connection_id)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->get_connection_stats_connections_connection_id_stats_get: #{e}"
end
```

#### Using the get_connection_stats_connections_connection_id_stats_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConnectionStats>, Integer, Hash)> get_connection_stats_connections_connection_id_stats_get_with_http_info(connection_id)

```ruby
begin
  # Get Connection Stats
  data, status_code, headers = api_instance.get_connection_stats_connections_connection_id_stats_get_with_http_info(connection_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConnectionStats>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->get_connection_stats_connections_connection_id_stats_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |

### Return type

[**ConnectionStats**](ConnectionStats.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_connection_source_types_connections_source_type_get

> <ListConnectorSourceTypeInfo> list_connection_source_types_connections_source_type_get

List Connection Source Types

List available connection source types like 'google_drive' and 'notion' along with their metadata

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ConnectionsApi.new

begin
  # List Connection Source Types
  result = api_instance.list_connection_source_types_connections_source_type_get
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->list_connection_source_types_connections_source_type_get: #{e}"
end
```

#### Using the list_connection_source_types_connections_source_type_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ListConnectorSourceTypeInfo>, Integer, Hash)> list_connection_source_types_connections_source_type_get_with_http_info

```ruby
begin
  # List Connection Source Types
  data, status_code, headers = api_instance.list_connection_source_types_connections_source_type_get_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ListConnectorSourceTypeInfo>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->list_connection_source_types_connections_source_type_get_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ListConnectorSourceTypeInfo**](ListConnectorSourceTypeInfo.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_connections_connections_get

> <ConnectionList> list_connections_connections_get(opts)

List Connections

List all connections sorted by created_at in descending order. Results are paginated with a max limit of 100. When more documents are available, a `cursor` will be provided. Use the `cursor` parameter to retrieve the subsequent page.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ConnectionsApi.new
opts = {
  cursor: 'cursor_example', # String | An opaque cursor for pagination
  page_size: 56, # Integer | The number of items per page (must be greater than 0 and less than or equal to 100)
  filter: 'filter_example', # String | The metadata search filter. Returns only items which match the filter. The following filter operators are supported: $eq - Equal to (number, string, boolean), $ne - Not equal to (number, string, boolean), $gt - Greater than (number), $gte - Greater than or equal to (number), $lt - Less than (number), $lte - Less than or equal to (number), $in - In array (string or number), $nin - Not in array (string or number). The operators can be combined with AND and OR. Read [Metadata & Filters guide](https://docs.ragie.ai/docs/metadata-filters) for more details and examples.
  partition: 'partition_example' # String | An optional partition to scope the request to. If omitted, the request will be scoped to the default partition.
}

begin
  # List Connections
  result = api_instance.list_connections_connections_get(opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->list_connections_connections_get: #{e}"
end
```

#### Using the list_connections_connections_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConnectionList>, Integer, Hash)> list_connections_connections_get_with_http_info(opts)

```ruby
begin
  # List Connections
  data, status_code, headers = api_instance.list_connections_connections_get_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConnectionList>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->list_connections_connections_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **cursor** | **String** | An opaque cursor for pagination | [optional] |
| **page_size** | **Integer** | The number of items per page (must be greater than 0 and less than or equal to 100) | [optional][default to 10] |
| **filter** | **String** | The metadata search filter. Returns only items which match the filter. The following filter operators are supported: $eq - Equal to (number, string, boolean), $ne - Not equal to (number, string, boolean), $gt - Greater than (number), $gte - Greater than or equal to (number), $lt - Less than (number), $lte - Less than or equal to (number), $in - In array (string or number), $nin - Not in array (string or number). The operators can be combined with AND and OR. Read [Metadata &amp; Filters guide](https://docs.ragie.ai/docs/metadata-filters) for more details and examples. | [optional] |
| **partition** | **String** | An optional partition to scope the request to. If omitted, the request will be scoped to the default partition. | [optional] |

### Return type

[**ConnectionList**](ConnectionList.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## set_connection_enabled_connections_connection_id_enabled_put

> <Connection> set_connection_enabled_connections_connection_id_enabled_put(connection_id, set_connection_enabled_payload)

Set Connection Enabled

Enable or disable the connection. A disabled connection won't sync.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ConnectionsApi.new
connection_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
set_connection_enabled_payload = RagieRubySdk::SetConnectionEnabledPayload.new({enabled: false}) # SetConnectionEnabledPayload | 

begin
  # Set Connection Enabled
  result = api_instance.set_connection_enabled_connections_connection_id_enabled_put(connection_id, set_connection_enabled_payload)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->set_connection_enabled_connections_connection_id_enabled_put: #{e}"
end
```

#### Using the set_connection_enabled_connections_connection_id_enabled_put_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Connection>, Integer, Hash)> set_connection_enabled_connections_connection_id_enabled_put_with_http_info(connection_id, set_connection_enabled_payload)

```ruby
begin
  # Set Connection Enabled
  data, status_code, headers = api_instance.set_connection_enabled_connections_connection_id_enabled_put_with_http_info(connection_id, set_connection_enabled_payload)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Connection>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->set_connection_enabled_connections_connection_id_enabled_put_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |
| **set_connection_enabled_payload** | [**SetConnectionEnabledPayload**](SetConnectionEnabledPayload.md) |  |  |

### Return type

[**Connection**](Connection.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## set_connection_limits_connections_connection_id_limit_put

> <Connection> set_connection_limits_connections_connection_id_limit_put(connection_id, connection_limit_params)

Set Connection Limits

Sets limits on a connection. Limits can be set on the total number of pages a connection can sync. When the limit is reached, the connection will be disabled. Limit may be removed by setting it to `null`.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ConnectionsApi.new
connection_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
connection_limit_params = RagieRubySdk::ConnectionLimitParams.new # ConnectionLimitParams | 

begin
  # Set Connection Limits
  result = api_instance.set_connection_limits_connections_connection_id_limit_put(connection_id, connection_limit_params)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->set_connection_limits_connections_connection_id_limit_put: #{e}"
end
```

#### Using the set_connection_limits_connections_connection_id_limit_put_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Connection>, Integer, Hash)> set_connection_limits_connections_connection_id_limit_put_with_http_info(connection_id, connection_limit_params)

```ruby
begin
  # Set Connection Limits
  data, status_code, headers = api_instance.set_connection_limits_connections_connection_id_limit_put_with_http_info(connection_id, connection_limit_params)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Connection>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->set_connection_limits_connections_connection_id_limit_put_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |
| **connection_limit_params** | [**ConnectionLimitParams**](ConnectionLimitParams.md) |  |  |

### Return type

[**Connection**](Connection.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## sync_connection

> <ResponseOK> sync_connection(connection_id)

Sync Connection

Schedules a connector to sync as soon as possible.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ConnectionsApi.new
connection_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Sync Connection
  result = api_instance.sync_connection(connection_id)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->sync_connection: #{e}"
end
```

#### Using the sync_connection_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ResponseOK>, Integer, Hash)> sync_connection_with_http_info(connection_id)

```ruby
begin
  # Sync Connection
  data, status_code, headers = api_instance.sync_connection_with_http_info(connection_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ResponseOK>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->sync_connection_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |

### Return type

[**ResponseOK**](ResponseOK.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_connection_connections_connection_id_put

> <Connection> update_connection_connections_connection_id_put(connection_id, connection_base)

Update Connection

Updates a connections metadata or mode. These changes will be seen after the next sync.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::ConnectionsApi.new
connection_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
connection_base = RagieRubySdk::ConnectionBase.new({partition_strategy: RagieRubySdk::PartitionStrategy.new}) # ConnectionBase | 

begin
  # Update Connection
  result = api_instance.update_connection_connections_connection_id_put(connection_id, connection_base)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->update_connection_connections_connection_id_put: #{e}"
end
```

#### Using the update_connection_connections_connection_id_put_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Connection>, Integer, Hash)> update_connection_connections_connection_id_put_with_http_info(connection_id, connection_base)

```ruby
begin
  # Update Connection
  data, status_code, headers = api_instance.update_connection_connections_connection_id_put_with_http_info(connection_id, connection_base)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Connection>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling ConnectionsApi->update_connection_connections_connection_id_put_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connection_id** | **String** |  |  |
| **connection_base** | [**ConnectionBase**](ConnectionBase.md) |  |  |

### Return type

[**Connection**](Connection.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

