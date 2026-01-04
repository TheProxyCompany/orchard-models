# orchard-models

Model profiles for [Orchard](https://github.com/TheProxyCompany): chat templates and control tokens for LLM inference on Apple Silicon.

## Structure

Each model family has its own directory containing:

- `control_tokens.json` - Model-specific tokens (BOS, EOS, role markers, capabilities)
- `chat_template.jinja` - Jinja2 template for formatting conversations

## Usage

This repository is included as a submodule in:
- [orchard-py](https://github.com/TheProxyCompany/orchard-py) - Python client
- [orchard-rs](https://github.com/TheProxyCompany/orchard-rs) - Rust client
- [orchard-swift](https://github.com/TheProxyCompany/orchard-swift) - Swift client

## Adding a new model

1. Create a directory named after the model family (e.g., `mistral/`)
2. Add `control_tokens.json` with the model's special tokens
3. Add `chat_template.jinja` with the conversation formatting template
4. Submit a PR

## License

Apache-2.0
