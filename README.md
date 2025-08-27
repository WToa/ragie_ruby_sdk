# Ragie Ruby SDK

A Ruby SDK for interacting with the Ragie API. This SDK is automatically generated from the OpenAPI specification and provides a convenient way to integrate Ragie services into your Ruby applications.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'ragie_ruby_sdk'
```

And then execute:

```bash
bundle install
```

Or install it yourself as:

```bash
gem install ragie_ruby_sdk
```

## Usage

Here's a basic example of how to use the SDK:

```ruby
require 'ragie_ruby_sdk'

# Initialize the client
client = RagieRubySdk::ApiClient.new

# Example API call (replace with actual endpoint)
# response = client.some_endpoint(params)
```

For detailed API documentation, refer to the [Ragie API Documentation](https://api.ragie.ai).

## Development

This SDK is generated from the OpenAPI specification using the OpenAPI Generator. To regenerate or update the SDK:

1. Ensure you have Docker installed
2. Run the GitHub Actions workflow or manually execute:
   ```bash
   docker run --rm \
     -v "$(pwd)/local:/local" \
     openapitools/openapi-generator-cli generate \
     -i https://api.ragie.ai/openapi.json \
     -g ruby \
     -o /local/ragie_ruby_sdk \
     --additional-properties=gemName=ragie_ruby_sdk,moduleName=RagieRubySdk,gemHomepage=https://www.ragie.ai/
   ```

The generated SDK will be placed in the `local/ragie_ruby_sdk` directory.

## Versioning

The SDK follows semantic versioning. Versions are automatically incremented based on changes detected in the generated code.

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For support and questions, please visit [Ragie Support](https://www.ragie.ai/support) or open an issue on GitHub.</content>
<parameter name="filePath">/home/wtoa/Development/ragie_ruby_sdk/README.md
