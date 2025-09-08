# RagieRubySdk::DocumentsApi

All URIs are relative to *https://api.ragie.ai*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_document**](DocumentsApi.md#create_document) | **POST** /documents | Create Document |
| [**create_document_from_url**](DocumentsApi.md#create_document_from_url) | **POST** /documents/url | Create Document From Url |
| [**create_document_raw**](DocumentsApi.md#create_document_raw) | **POST** /documents/raw | Create Document Raw |
| [**delete_document**](DocumentsApi.md#delete_document) | **DELETE** /documents/{document_id} | Delete Document |
| [**get_document**](DocumentsApi.md#get_document) | **GET** /documents/{document_id} | Get Document |
| [**get_document_chunk**](DocumentsApi.md#get_document_chunk) | **GET** /documents/{document_id}/chunks/{chunk_id} | Get Document Chunk |
| [**get_document_chunk_content**](DocumentsApi.md#get_document_chunk_content) | **GET** /documents/{document_id}/chunks/{chunk_id}/content | Get Document Chunk Content |
| [**get_document_chunks**](DocumentsApi.md#get_document_chunks) | **GET** /documents/{document_id}/chunks | Get Document Chunks |
| [**get_document_content**](DocumentsApi.md#get_document_content) | **GET** /documents/{document_id}/content | Get Document Content |
| [**get_document_source**](DocumentsApi.md#get_document_source) | **GET** /documents/{document_id}/source | Get Document Source |
| [**get_document_summary**](DocumentsApi.md#get_document_summary) | **GET** /documents/{document_id}/summary | Get Document Summary |
| [**list_documents**](DocumentsApi.md#list_documents) | **GET** /documents | List Documents |
| [**patch_document_metadata**](DocumentsApi.md#patch_document_metadata) | **PATCH** /documents/{document_id}/metadata | Patch Document Metadata |
| [**update_document_file**](DocumentsApi.md#update_document_file) | **PUT** /documents/{document_id}/file | Update Document File |
| [**update_document_from_url**](DocumentsApi.md#update_document_from_url) | **PUT** /documents/{document_id}/url | Update Document Url |
| [**update_document_raw**](DocumentsApi.md#update_document_raw) | **PUT** /documents/{document_id}/raw | Update Document Raw |


## create_document

> <Document> create_document(file, opts)

Create Document

On ingest, the document goes through a series of steps before it is ready for retrieval. Each step is reflected in the status of the document which can be one of [`pending`, `partitioning`, `partitioned`, `refined`, `chunked`, `indexed`, `summary_indexed`, `keyword_indexed`, `ready`, `failed`]. The document is available for retrieval once it is in ready state. The summary index step can take a few seconds. You can optionally use the document for retrieval once it is in `indexed` state. However the summary will only be available once the state has changed to `summary_indexed` or `ready`.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
file = File.new('/path/to/some/file') # File | The binary file to upload, extract, and index for retrieval. The following file types are supported: Plain Text: `.eml` `.html` `.json` `.md` `.msg` `.rst` `.rtf` `.txt` `.xml` Images: `.png` `.webp` `.jpg` `.jpeg` `.tiff` `.bmp` `.heic` Documents: `.csv` `.doc` `.docx` `.epub` `.epub+zip` `.odt` `.pdf` `.ppt` `.pptx` `.tsv` `.xlsx` `.xls`.
opts = {
  mode: RagieRubySdk::Mode2OneOf.new, # Mode2 | 
  metadata: { key: nil}, # Hash<String, MetadataValue1> | Metadata for the document. Keys must be strings. Values may be strings, numbers, booleans, or lists of strings. Numbers may be integers or floating point and will be converted to 64 bit floating point. 1000 total values are allowed. Each item in an array counts towards the total. The following keys are reserved for internal use: `document_id`, `document_type`, `document_source`, `document_name`, `document_uploaded_at`, `start_time`, `end_time`.
  external_id: 'external_id_example', # String | An optional identifier for the document. A common value might be an id in an external system or the URL where the source file may be found.
  name: 'name_example', # String | An optional name for the document. If set, the document will have this name. Otherwise it will default to the file's name.
  partition: 'partition_example' # String | An optional partition identifier. Documents can be scoped to a partition. Partitions must be lowercase alphanumeric and may only include the special characters `_` and `-`.  A partition is created any time a document is created.
}

begin
  # Create Document
  result = api_instance.create_document(file, opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->create_document: #{e}"
end
```

#### Using the create_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Document>, Integer, Hash)> create_document_with_http_info(file, opts)

```ruby
begin
  # Create Document
  data, status_code, headers = api_instance.create_document_with_http_info(file, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Document>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->create_document_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **file** | **File** | The binary file to upload, extract, and index for retrieval. The following file types are supported: Plain Text: &#x60;.eml&#x60; &#x60;.html&#x60; &#x60;.json&#x60; &#x60;.md&#x60; &#x60;.msg&#x60; &#x60;.rst&#x60; &#x60;.rtf&#x60; &#x60;.txt&#x60; &#x60;.xml&#x60; Images: &#x60;.png&#x60; &#x60;.webp&#x60; &#x60;.jpg&#x60; &#x60;.jpeg&#x60; &#x60;.tiff&#x60; &#x60;.bmp&#x60; &#x60;.heic&#x60; Documents: &#x60;.csv&#x60; &#x60;.doc&#x60; &#x60;.docx&#x60; &#x60;.epub&#x60; &#x60;.epub+zip&#x60; &#x60;.odt&#x60; &#x60;.pdf&#x60; &#x60;.ppt&#x60; &#x60;.pptx&#x60; &#x60;.tsv&#x60; &#x60;.xlsx&#x60; &#x60;.xls&#x60;. |  |
| **mode** | [**Mode2**](Mode2.md) |  | [optional] |
| **metadata** | [**Hash&lt;String, MetadataValue1&gt;**](Hash.md) | Metadata for the document. Keys must be strings. Values may be strings, numbers, booleans, or lists of strings. Numbers may be integers or floating point and will be converted to 64 bit floating point. 1000 total values are allowed. Each item in an array counts towards the total. The following keys are reserved for internal use: &#x60;document_id&#x60;, &#x60;document_type&#x60;, &#x60;document_source&#x60;, &#x60;document_name&#x60;, &#x60;document_uploaded_at&#x60;, &#x60;start_time&#x60;, &#x60;end_time&#x60;. | [optional] |
| **external_id** | **String** | An optional identifier for the document. A common value might be an id in an external system or the URL where the source file may be found. | [optional] |
| **name** | **String** | An optional name for the document. If set, the document will have this name. Otherwise it will default to the file&#39;s name. | [optional] |
| **partition** | **String** | An optional partition identifier. Documents can be scoped to a partition. Partitions must be lowercase alphanumeric and may only include the special characters &#x60;_&#x60; and &#x60;-&#x60;.  A partition is created any time a document is created. | [optional] |

### Return type

[**Document**](Document.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json


## create_document_from_url

> <Document> create_document_from_url(create_document_from_url_params)

Create Document From Url

Ingest a document from a publicly accessible URL. On ingest, the document goes through a series of steps before it is ready for retrieval. Each step is reflected in the status of the document which can be one of [`pending`, `partitioning`, `partitioned`, `refined`, `chunked`, `indexed`, `summary_indexed`, `keyword_indexed`, `ready`, `failed`]. The document is available for retrieval once it is in ready state. The summary index step can take a few seconds. You can optionally use the document for retrieval once it is in `indexed` state. However the summary will only be available once the state has changed to `summary_indexed` or `ready`.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
create_document_from_url_params = RagieRubySdk::CreateDocumentFromUrlParams.new({url: 'url_example'}) # CreateDocumentFromUrlParams | 

begin
  # Create Document From Url
  result = api_instance.create_document_from_url(create_document_from_url_params)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->create_document_from_url: #{e}"
end
```

#### Using the create_document_from_url_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Document>, Integer, Hash)> create_document_from_url_with_http_info(create_document_from_url_params)

```ruby
begin
  # Create Document From Url
  data, status_code, headers = api_instance.create_document_from_url_with_http_info(create_document_from_url_params)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Document>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->create_document_from_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_document_from_url_params** | [**CreateDocumentFromUrlParams**](CreateDocumentFromUrlParams.md) |  |  |

### Return type

[**Document**](Document.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_document_raw

> <Document> create_document_raw(create_document_raw_params)

Create Document Raw

Ingest a document as raw text. On ingest, the document goes through a series of steps before it is ready for retrieval. Each step is reflected in the status of the document which can be one of [`pending`, `partitioning`, `partitioned`, `refined`, `chunked`, `indexed`, `summary_indexed`, `keyword_indexed`, `ready`, `failed`]. The document is available for retrieval once it is in ready state. The summary index step can take a few seconds. You can optionally use the document for retrieval once it is in `indexed` state. However the summary will only be available once the state has changed to `summary_indexed` or `ready`.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
create_document_raw_params = RagieRubySdk::CreateDocumentRawParams.new({data: RagieRubySdk::Data.new}) # CreateDocumentRawParams | 

begin
  # Create Document Raw
  result = api_instance.create_document_raw(create_document_raw_params)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->create_document_raw: #{e}"
end
```

#### Using the create_document_raw_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Document>, Integer, Hash)> create_document_raw_with_http_info(create_document_raw_params)

```ruby
begin
  # Create Document Raw
  data, status_code, headers = api_instance.create_document_raw_with_http_info(create_document_raw_params)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Document>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->create_document_raw_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_document_raw_params** | [**CreateDocumentRawParams**](CreateDocumentRawParams.md) |  |  |

### Return type

[**Document**](Document.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_document

> <DocumentDelete> delete_document(document_id, opts)

Delete Document

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
document_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The id of the document.
opts = {
  async: true, # Boolean | If true, performs document deletion asynchronously
  partition: 'partition_example' # String | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition.
}

begin
  # Delete Document
  result = api_instance.delete_document(document_id, opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->delete_document: #{e}"
end
```

#### Using the delete_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentDelete>, Integer, Hash)> delete_document_with_http_info(document_id, opts)

```ruby
begin
  # Delete Document
  data, status_code, headers = api_instance.delete_document_with_http_info(document_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentDelete>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->delete_document_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** | The id of the document. |  |
| **async** | **Boolean** | If true, performs document deletion asynchronously | [optional] |
| **partition** | **String** | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition. | [optional] |

### Return type

[**DocumentDelete**](DocumentDelete.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_document

> <DocumentGet> get_document(document_id, opts)

Get Document

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
document_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The id of the document.
opts = {
  partition: 'partition_example' # String | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition.
}

begin
  # Get Document
  result = api_instance.get_document(document_id, opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->get_document: #{e}"
end
```

#### Using the get_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentGet>, Integer, Hash)> get_document_with_http_info(document_id, opts)

```ruby
begin
  # Get Document
  data, status_code, headers = api_instance.get_document_with_http_info(document_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentGet>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->get_document_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** | The id of the document. |  |
| **partition** | **String** | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition. | [optional] |

### Return type

[**DocumentGet**](DocumentGet.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_document_chunk

> <DocumentChunkDetail> get_document_chunk(document_id, chunk_id, opts)

Get Document Chunk

Gets a document chunk by its document and chunk ID.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
document_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The id of the document.
chunk_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The ID of the chunk.
opts = {
  partition: 'partition_example' # String | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition.
}

begin
  # Get Document Chunk
  result = api_instance.get_document_chunk(document_id, chunk_id, opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->get_document_chunk: #{e}"
end
```

#### Using the get_document_chunk_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentChunkDetail>, Integer, Hash)> get_document_chunk_with_http_info(document_id, chunk_id, opts)

```ruby
begin
  # Get Document Chunk
  data, status_code, headers = api_instance.get_document_chunk_with_http_info(document_id, chunk_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentChunkDetail>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->get_document_chunk_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** | The id of the document. |  |
| **chunk_id** | **String** | The ID of the chunk. |  |
| **partition** | **String** | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition. | [optional] |

### Return type

[**DocumentChunkDetail**](DocumentChunkDetail.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_document_chunk_content

> Object get_document_chunk_content(document_id, chunk_id, opts)

Get Document Chunk Content

Returns the content of a document chunk in the requested format. Can be used to stream media of the content for audio/video documents.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
document_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The id of the document.
chunk_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The ID of the chunk.
opts = {
  media_type: 'text/plain', # String | The desired media type of the content to return described as a mime type. An error will be returned if the requested media type is not supported for the chunk's document type.
  download: true, # Boolean | Whether to return the content as a file download or a raw stream. If set to `true`, the content will be returned as a named file for download.
  partition: 'partition_example', # String | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition.
  range: 'range_example' # String | 
}

begin
  # Get Document Chunk Content
  result = api_instance.get_document_chunk_content(document_id, chunk_id, opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->get_document_chunk_content: #{e}"
end
```

#### Using the get_document_chunk_content_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> get_document_chunk_content_with_http_info(document_id, chunk_id, opts)

```ruby
begin
  # Get Document Chunk Content
  data, status_code, headers = api_instance.get_document_chunk_content_with_http_info(document_id, chunk_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->get_document_chunk_content_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** | The id of the document. |  |
| **chunk_id** | **String** | The ID of the chunk. |  |
| **media_type** | **String** | The desired media type of the content to return described as a mime type. An error will be returned if the requested media type is not supported for the chunk&#39;s document type. | [optional] |
| **download** | **Boolean** | Whether to return the content as a file download or a raw stream. If set to &#x60;true&#x60;, the content will be returned as a named file for download. | [optional][default to false] |
| **partition** | **String** | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition. | [optional] |
| **range** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/octet-stream, audio/mpeg, text/plain


## get_document_chunks

> <DocumentChunkList> get_document_chunks(document_id, opts)

Get Document Chunks

List all document chunks sorted by index in ascending order. May be limited to a range of chunk indices with the `start_index` and `end_index` parameters. Documents created prior to 9/18/2024, which have not been updated since, have chunks which do not include an index and their index will be returned as -1. They will be sorted by their ID instead. Updating the document using the `Update Document File` or `Update Document Raw` endpoint will regenerate document chunks, including their index. Results are paginated with a max limit of 100. When more chunks are available, a `cursor` will be provided. Use the `cursor` parameter to retrieve the subsequent page.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
document_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The id of the document.
opts = {
  start_index: 56, # Integer | The inclusive starting index of the chunk range to list. If omitted and `end_index` is present effectively limits results to at most one chunk matching `end_index`. If both `start_index` and `end_index` are omitted, results are not limited by index.
  end_index: 56, # Integer | The inclusive ending index of the chunk range to list. If omitted and `start_index` is present effectively limits results to at most one chunk matching `start_index`. If both `start_index` and `end_index` are omitted, results are not limited by index.
  cursor: 'cursor_example', # String | An opaque cursor for pagination
  page_size: 56, # Integer | The number of items per page (must be greater than 0 and less than or equal to 100)
  partition: 'partition_example' # String | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition.
}

begin
  # Get Document Chunks
  result = api_instance.get_document_chunks(document_id, opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->get_document_chunks: #{e}"
end
```

#### Using the get_document_chunks_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentChunkList>, Integer, Hash)> get_document_chunks_with_http_info(document_id, opts)

```ruby
begin
  # Get Document Chunks
  data, status_code, headers = api_instance.get_document_chunks_with_http_info(document_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentChunkList>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->get_document_chunks_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** | The id of the document. |  |
| **start_index** | **Integer** | The inclusive starting index of the chunk range to list. If omitted and &#x60;end_index&#x60; is present effectively limits results to at most one chunk matching &#x60;end_index&#x60;. If both &#x60;start_index&#x60; and &#x60;end_index&#x60; are omitted, results are not limited by index. | [optional] |
| **end_index** | **Integer** | The inclusive ending index of the chunk range to list. If omitted and &#x60;start_index&#x60; is present effectively limits results to at most one chunk matching &#x60;start_index&#x60;. If both &#x60;start_index&#x60; and &#x60;end_index&#x60; are omitted, results are not limited by index. | [optional] |
| **cursor** | **String** | An opaque cursor for pagination | [optional] |
| **page_size** | **Integer** | The number of items per page (must be greater than 0 and less than or equal to 100) | [optional][default to 10] |
| **partition** | **String** | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition. | [optional] |

### Return type

[**DocumentChunkList**](DocumentChunkList.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_document_content

> <DocumentWithContent> get_document_content(document_id, opts)

Get Document Content

Get the content of a document. The `media_type` parameter can be used to request the content in a different format. When requesting as `application/json` additional metadata about the document will be included. If the original document contained content such as images or other non-textual media, this response will include a text description of that media instead of the original file data. Using mime types such as `audio/mpeg` or `video/mp4` will stream the file in a format that can be provided to an audio video player.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
document_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The id of the document.
opts = {
  media_type: 'text/plain', # String | The desired media type of the content to return described as a mime type. An error will be returned if the requested media type is not supported for the document's type.
  download: true, # Boolean | Whether to return the content as a file download or a raw stream. If set to `true`, the content will be returned as a named file for download.
  partition: 'partition_example', # String | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition.
  range: 'range_example' # String | 
}

begin
  # Get Document Content
  result = api_instance.get_document_content(document_id, opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->get_document_content: #{e}"
end
```

#### Using the get_document_content_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentWithContent>, Integer, Hash)> get_document_content_with_http_info(document_id, opts)

```ruby
begin
  # Get Document Content
  data, status_code, headers = api_instance.get_document_content_with_http_info(document_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentWithContent>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->get_document_content_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** | The id of the document. |  |
| **media_type** | **String** | The desired media type of the content to return described as a mime type. An error will be returned if the requested media type is not supported for the document&#39;s type. | [optional] |
| **download** | **Boolean** | Whether to return the content as a file download or a raw stream. If set to &#x60;true&#x60;, the content will be returned as a named file for download. | [optional][default to false] |
| **partition** | **String** | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition. | [optional] |
| **range** | **String** |  | [optional] |

### Return type

[**DocumentWithContent**](DocumentWithContent.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_document_source

> File get_document_source(document_id, opts)

Get Document Source

Get the source file of a document. The source file is the original file that was uploaded to create the document. If the document was created from a URL, the source file will be the content of the URL. If the document was created by a connection, the source file will vary based on the type of the connection. For example, a Google Drive connection will return the file that was synced from the Google Drive, while a SalesForce connection would return a JSON file of the data synced from SalesForce.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
document_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The id of the document.
opts = {
  partition: 'partition_example' # String | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition.
}

begin
  # Get Document Source
  result = api_instance.get_document_source(document_id, opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->get_document_source: #{e}"
end
```

#### Using the get_document_source_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(File, Integer, Hash)> get_document_source_with_http_info(document_id, opts)

```ruby
begin
  # Get Document Source
  data, status_code, headers = api_instance.get_document_source_with_http_info(document_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => File
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->get_document_source_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** | The id of the document. |  |
| **partition** | **String** | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition. | [optional] |

### Return type

**File**

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/octet-stream, application/json


## get_document_summary

> <DocumentSummary> get_document_summary(document_id, opts)

Get Document Summary

Get a LLM generated summary of the document. The summary is created when the document is first created or updated. Documents of types ['xls', 'xlsx', 'csv', 'json'] are not supported for summarization. Documents greater than 1M in token length are not supported. This feature is in beta and may change in the future.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
document_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The id of the document.
opts = {
  partition: 'partition_example' # String | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition.
}

begin
  # Get Document Summary
  result = api_instance.get_document_summary(document_id, opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->get_document_summary: #{e}"
end
```

#### Using the get_document_summary_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentSummary>, Integer, Hash)> get_document_summary_with_http_info(document_id, opts)

```ruby
begin
  # Get Document Summary
  data, status_code, headers = api_instance.get_document_summary_with_http_info(document_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentSummary>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->get_document_summary_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** | The id of the document. |  |
| **partition** | **String** | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition. | [optional] |

### Return type

[**DocumentSummary**](DocumentSummary.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_documents

> <DocumentList> list_documents(opts)

List Documents

List all documents sorted by created_at in descending order. Results are paginated with a max limit of 100. When more documents are available, a `cursor` will be provided. Use the `cursor` parameter to retrieve the subsequent page.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
opts = {
  cursor: 'cursor_example', # String | An opaque cursor for pagination
  page_size: 56, # Integer | The number of items per page (must be greater than 0 and less than or equal to 100)
  filter: 'filter_example', # String | The metadata search filter. Returns only items which match the filter. The following filter operators are supported: $eq - Equal to (number, string, boolean), $ne - Not equal to (number, string, boolean), $gt - Greater than (number), $gte - Greater than or equal to (number), $lt - Less than (number), $lte - Less than or equal to (number), $in - In array (string or number), $nin - Not in array (string or number). The operators can be combined with AND and OR. Read [Metadata & Filters guide](https://docs.ragie.ai/docs/metadata-filters) for more details and examples.
  partition: 'partition_example' # String | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition.
}

begin
  # List Documents
  result = api_instance.list_documents(opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->list_documents: #{e}"
end
```

#### Using the list_documents_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentList>, Integer, Hash)> list_documents_with_http_info(opts)

```ruby
begin
  # List Documents
  data, status_code, headers = api_instance.list_documents_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentList>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->list_documents_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **cursor** | **String** | An opaque cursor for pagination | [optional] |
| **page_size** | **Integer** | The number of items per page (must be greater than 0 and less than or equal to 100) | [optional][default to 10] |
| **filter** | **String** | The metadata search filter. Returns only items which match the filter. The following filter operators are supported: $eq - Equal to (number, string, boolean), $ne - Not equal to (number, string, boolean), $gt - Greater than (number), $gte - Greater than or equal to (number), $lt - Less than (number), $lte - Less than or equal to (number), $in - In array (string or number), $nin - Not in array (string or number). The operators can be combined with AND and OR. Read [Metadata &amp; Filters guide](https://docs.ragie.ai/docs/metadata-filters) for more details and examples. | [optional] |
| **partition** | **String** | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition. | [optional] |

### Return type

[**DocumentList**](DocumentList.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## patch_document_metadata

> <ResponsePatchdocumentmetadata> patch_document_metadata(document_id, patch_document_metadata_params, opts)

Patch Document Metadata

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
document_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The id of the document.
patch_document_metadata_params = RagieRubySdk::PatchDocumentMetadataParams.new({metadata: { key: 3.56}}) # PatchDocumentMetadataParams | 
opts = {
  partition: 'partition_example' # String | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition.
}

begin
  # Patch Document Metadata
  result = api_instance.patch_document_metadata(document_id, patch_document_metadata_params, opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->patch_document_metadata: #{e}"
end
```

#### Using the patch_document_metadata_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ResponsePatchdocumentmetadata>, Integer, Hash)> patch_document_metadata_with_http_info(document_id, patch_document_metadata_params, opts)

```ruby
begin
  # Patch Document Metadata
  data, status_code, headers = api_instance.patch_document_metadata_with_http_info(document_id, patch_document_metadata_params, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ResponsePatchdocumentmetadata>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->patch_document_metadata_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** | The id of the document. |  |
| **patch_document_metadata_params** | [**PatchDocumentMetadataParams**](PatchDocumentMetadataParams.md) |  |  |
| **partition** | **String** | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition. | [optional] |

### Return type

[**ResponsePatchdocumentmetadata**](ResponsePatchdocumentmetadata.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_document_file

> <DocumentFileUpdate> update_document_file(document_id, file, opts)

Update Document File

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
document_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The id of the document.
file = File.new('/path/to/some/file') # File | The binary file to upload, extract, and index for retrieval. The following file types are supported: Plain Text: `.eml` `.html` `.json` `.md` `.msg` `.rst` `.rtf` `.txt` `.xml` Images: `.png` `.webp` `.jpg` `.jpeg` `.tiff` `.bmp` `.heic` Documents: `.csv` `.doc` `.docx` `.epub` `.epub+zip` `.odt` `.pdf` `.ppt` `.pptx` `.tsv` `.xlsx` `.xls`.
opts = {
  partition: 'partition_example', # String | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition.
  mode: RagieRubySdk::Mode2OneOf.new # Mode2 | 
}

begin
  # Update Document File
  result = api_instance.update_document_file(document_id, file, opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->update_document_file: #{e}"
end
```

#### Using the update_document_file_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentFileUpdate>, Integer, Hash)> update_document_file_with_http_info(document_id, file, opts)

```ruby
begin
  # Update Document File
  data, status_code, headers = api_instance.update_document_file_with_http_info(document_id, file, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentFileUpdate>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->update_document_file_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** | The id of the document. |  |
| **file** | **File** | The binary file to upload, extract, and index for retrieval. The following file types are supported: Plain Text: &#x60;.eml&#x60; &#x60;.html&#x60; &#x60;.json&#x60; &#x60;.md&#x60; &#x60;.msg&#x60; &#x60;.rst&#x60; &#x60;.rtf&#x60; &#x60;.txt&#x60; &#x60;.xml&#x60; Images: &#x60;.png&#x60; &#x60;.webp&#x60; &#x60;.jpg&#x60; &#x60;.jpeg&#x60; &#x60;.tiff&#x60; &#x60;.bmp&#x60; &#x60;.heic&#x60; Documents: &#x60;.csv&#x60; &#x60;.doc&#x60; &#x60;.docx&#x60; &#x60;.epub&#x60; &#x60;.epub+zip&#x60; &#x60;.odt&#x60; &#x60;.pdf&#x60; &#x60;.ppt&#x60; &#x60;.pptx&#x60; &#x60;.tsv&#x60; &#x60;.xlsx&#x60; &#x60;.xls&#x60;. |  |
| **partition** | **String** | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition. | [optional] |
| **mode** | [**Mode2**](Mode2.md) |  | [optional] |

### Return type

[**DocumentFileUpdate**](DocumentFileUpdate.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json


## update_document_from_url

> <DocumentUrlUpdate> update_document_from_url(document_id, update_document_from_url_params, opts)

Update Document Url

Updates a document from a publicly accessible URL. On ingest, the document goes through a series of steps before it is ready for retrieval. Each step is reflected in the status of the document which can be one of [`pending`, `partitioning`, `partitioned`, `refined`, `chunked`, `indexed`, `summary_indexed`, `keyword_indexed`, `ready`, `failed`]. The document is available for retrieval once it is in ready state. The summary index step can take a few seconds. You can optionally use the document for retrieval once it is in `indexed` state. However the summary will only be available once the state has changed to `summary_indexed` or `ready`.

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
document_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The id of the document.
update_document_from_url_params = RagieRubySdk::UpdateDocumentFromUrlParams.new({url: 'url_example'}) # UpdateDocumentFromUrlParams | 
opts = {
  partition: 'partition_example' # String | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition.
}

begin
  # Update Document Url
  result = api_instance.update_document_from_url(document_id, update_document_from_url_params, opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->update_document_from_url: #{e}"
end
```

#### Using the update_document_from_url_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentUrlUpdate>, Integer, Hash)> update_document_from_url_with_http_info(document_id, update_document_from_url_params, opts)

```ruby
begin
  # Update Document Url
  data, status_code, headers = api_instance.update_document_from_url_with_http_info(document_id, update_document_from_url_params, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentUrlUpdate>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->update_document_from_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** | The id of the document. |  |
| **update_document_from_url_params** | [**UpdateDocumentFromUrlParams**](UpdateDocumentFromUrlParams.md) |  |  |
| **partition** | **String** | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition. | [optional] |

### Return type

[**DocumentUrlUpdate**](DocumentUrlUpdate.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_document_raw

> <DocumentRawUpdate> update_document_raw(document_id, update_document_raw_params, opts)

Update Document Raw

### Examples

```ruby
require 'time'
require 'ragie_ruby_sdk'
# setup authorization
RagieRubySdk.configure do |config|
  # Configure Bearer authorization: auth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = RagieRubySdk::DocumentsApi.new
document_id = '38400000-8cf0-11bd-b23e-10b96e4ef00d' # String | The id of the document.
update_document_raw_params = RagieRubySdk::UpdateDocumentRawParams.new({data: RagieRubySdk::Data.new}) # UpdateDocumentRawParams | 
opts = {
  partition: 'partition_example' # String | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition.
}

begin
  # Update Document Raw
  result = api_instance.update_document_raw(document_id, update_document_raw_params, opts)
  p result
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->update_document_raw: #{e}"
end
```

#### Using the update_document_raw_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentRawUpdate>, Integer, Hash)> update_document_raw_with_http_info(document_id, update_document_raw_params, opts)

```ruby
begin
  # Update Document Raw
  data, status_code, headers = api_instance.update_document_raw_with_http_info(document_id, update_document_raw_params, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentRawUpdate>
rescue RagieRubySdk::ApiError => e
  puts "Error when calling DocumentsApi->update_document_raw_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** | The id of the document. |  |
| **update_document_raw_params** | [**UpdateDocumentRawParams**](UpdateDocumentRawParams.md) |  |  |
| **partition** | **String** | An optional partition to scope the request to. If omitted, accounts created after 1/9/2025 will have the request scoped to the default partition, while older accounts will have the request scoped to all partitions. Older accounts may opt in to strict partition scoping by contacting support@ragie.ai. Older accounts using the partitions feature are strongly recommended to scope the request to a partition. | [optional] |

### Return type

[**DocumentRawUpdate**](DocumentRawUpdate.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

