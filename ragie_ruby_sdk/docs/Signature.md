# RagieRubySdk::Signature

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;Signature&#39;] |
| **content** | **String** | Content of the signature. |  |
| **description** | **String** | A detailed description of the signature. |  |
| **label** | **String** | The printed text indicating who should sign (e.g., &#39;Driver Signature&#39;, &#39;Authorized By&#39;). |  |
| **is_signed** | **Boolean** | True if a handwritten signature, digital signature, or stamp is present. False if blank. |  |
| **signer_name** | **String** | The name of the signer | [optional] |
| **date** | **String** | The date of the signature if present | [optional] |

## Example

```ruby
require 'ragie_ruby_sdk'

instance = RagieRubySdk::Signature.new(
  type: null,
  content: null,
  description: null,
  label: null,
  is_signed: null,
  signer_name: null,
  date: null
)
```

