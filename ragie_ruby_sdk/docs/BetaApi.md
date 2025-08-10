# RagieRubySdk::BetaApi

All URIs are relative to *https://api.ragie.ai*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_authenticator**](BetaApi.md#create_authenticator) | **POST** /authenticators | Create Authenticator |
| [**create_authenticator_connection**](BetaApi.md#create_authenticator_connection) | **POST** /authenticators/{authenticator_id}/connection | Create Authenticator Connection |
| [**create_connection**](BetaApi.md#create_connection) | **POST** /connection | Create Connection |
| [**delete_authenticator_connection**](BetaApi.md#delete_authenticator_connection) | **DELETE** /authenticators/{authenticator_id} | Delete Authenticator |
| [**list_authenticators**](BetaApi.md#list_authenticators) | **GET** /authenticators | List Authenticators |


## create_authenticator

> <BaseGetAuthenticator> create_authenticator(payload)

Create Authenticator

Create White labeled connector credentials

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::BetaApi.new
payload = RagieRubySdk::CreateGoogleAuthenticator.new({provider: 'google', name: 'name_example', client_id: 'client_id_example', client_secret: 'client_secret_example'}) # Payload | 

begin
  # Create Authenticator
  result = api_instance.create_authenticator(payload)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling BetaApi->create_authenticator: #{e}"
end
```

#### Using the create_authenticator_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BaseGetAuthenticator>, Integer, Hash)> create_authenticator_with_http_info(payload)

```ruby
begin
  # Create Authenticator
  data, status_code, headers = api_instance.create_authenticator_with_http_info(payload)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BaseGetAuthenticator>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling BetaApi->create_authenticator_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **payload** | [**Payload**](Payload.md) |  |  |

### Return type

[**BaseGetAuthenticator**](BaseGetAuthenticator.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_authenticator_connection

> <Connection> create_authenticator_connection(authenticator_id, create_authenticator_connection)

Create Authenticator Connection

Create a connector for a given authenticator. This requires credentials dependent on the provider. For google drive it is a refresh token.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::BetaApi.new
authenticator_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 
create_authenticator_connection = RagieRubySdk::CreateAuthenticatorConnection.new({partition_strategy: RagieRubySdk::MediaModeParam.new, connection: RagieRubySdk::AuthenticatorConfluenceConnection.new({provider: 'confluence', data: [RagieRubySdk::ConfluenceData.new({resource_id: 'resource_id_example', space_id: 37, space_key: 'space_key_example', space_name: 'space_name_example'})], credentials: RagieRubySdk::OAuthRefreshTokenCredentials.new({refresh_token: 'refresh_token_example'})})}) # CreateAuthenticatorConnection | 

begin
  # Create Authenticator Connection
  result = api_instance.create_authenticator_connection(authenticator_id, create_authenticator_connection)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling BetaApi->create_authenticator_connection: #{e}"
end
```

#### Using the create_authenticator_connection_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Connection>, Integer, Hash)> create_authenticator_connection_with_http_info(authenticator_id, create_authenticator_connection)

```ruby
begin
  # Create Authenticator Connection
  data, status_code, headers = api_instance.create_authenticator_connection_with_http_info(authenticator_id, create_authenticator_connection)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Connection>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling BetaApi->create_authenticator_connection_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **authenticator_id** | **String** |  |  |
| **create_authenticator_connection** | [**CreateAuthenticatorConnection**](CreateAuthenticatorConnection.md) |  |  |

### Return type

[**Connection**](Connection.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


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

api_instance = RagieRubySdk::BetaApi.new
public_create_connection = RagieRubySdk::PublicCreateConnection.new({partition_strategy: RagieRubySdk::MediaModeParam.new, connection: RagieRubySdk::PublicBackblazeConnection.new({provider: 'backblaze', data: RagieRubySdk::BucketData.new({bucket: 'bucket_example'}), credentials: RagieRubySdk::BackblazeCredentials.new({key_id: 'key_id_example', application_key: 'application_key_example', region: 'region_example', endpoint: 'endpoint_example'})})}) # PublicCreateConnection | 

begin
  # Create Connection
  result = api_instance.create_connection(public_create_connection)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling BetaApi->create_connection: #{e}"
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
  puts "Error when calling BetaApi->create_connection_with_http_info: #{e}"
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


## delete_authenticator_connection

> <ResponseOK> delete_authenticator_connection(authenticator_id)

Delete Authenticator

Delete an authenticator. This requires all connections created by that authenticator to be deleted first.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::BetaApi.new
authenticator_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | 

begin
  # Delete Authenticator
  result = api_instance.delete_authenticator_connection(authenticator_id)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling BetaApi->delete_authenticator_connection: #{e}"
end
```

#### Using the delete_authenticator_connection_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ResponseOK>, Integer, Hash)> delete_authenticator_connection_with_http_info(authenticator_id)

```ruby
begin
  # Delete Authenticator
  data, status_code, headers = api_instance.delete_authenticator_connection_with_http_info(authenticator_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ResponseOK>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling BetaApi->delete_authenticator_connection_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **authenticator_id** | **String** |  |  |

### Return type

[**ResponseOK**](ResponseOK.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_authenticators

> <AuthenticatorList> list_authenticators(opts)

List Authenticators

List all authenticators sorted by created_at in descending order. Results are paginated with a max limit of 100. When more authenticators are available, a `cursor` will be provided. Use the `cursor` parameter to retrieve the subsequent page.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::BetaApi.new
opts = {
  cursor: 'cursor_example', # String | An opaque cursor for pagination
  page_size: 56 # Integer | The number of items per page (must be greater than 0 and less than or equal to 100)
}

begin
  # List Authenticators
  result = api_instance.list_authenticators(opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling BetaApi->list_authenticators: #{e}"
end
```

#### Using the list_authenticators_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthenticatorList>, Integer, Hash)> list_authenticators_with_http_info(opts)

```ruby
begin
  # List Authenticators
  data, status_code, headers = api_instance.list_authenticators_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthenticatorList>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling BetaApi->list_authenticators_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **cursor** | **String** | An opaque cursor for pagination | [optional] |
| **page_size** | **Integer** | The number of items per page (must be greater than 0 and less than or equal to 100) | [optional][default to 10] |

### Return type

[**AuthenticatorList**](AuthenticatorList.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

