# Model Catalogue

RouterHub publishes **37 model entries**. The live catalogue is the source of truth:

<https://routerhub.si/models>

## Families

| Family | Examples |
|---|---|
| OpenAI | GPT-6.1 Sol, GPT-6 Astra, GPT-6 Sol, GPT-5.6 Sol, GPT-5.6 Terra |
| Anthropic | Claude Fable 5.1, Claude Opus 5.5, Claude Sonnet 5.5, Claude Haiku 5.5 |
| Google | Gemini 4 Argon |
| xAI | Grok 4.7, Grok 4.6, Grok 4.5 |
| DeepSeek | V4.1 Flash, V4 Pro, plus uncensored/abliterated entries |
| Z.ai | GLM 5.3, GLM 5.3 Flash, plus uncensored/abliterated entries |
| Qwen | Qwen 3.8 Max and Qwen 3.8 Max Uncensored |

## Exact IDs and formats

| Model | API ID | Protocol |
|---|---|---|
| DeepSeek V4.1 Flash | `deepseek-v4.1-flash` | Chat Completions |
| DeepSeek V4.1 Flash Uncensored | `deepseek-v4.1-flash-uncensored` | Chat Completions |
| DeepSeek V4.1 Flash Abliterated | `deepseek-v4.1-flash-abliterated` | Chat Completions |
| DeepSeek V4 Pro Uncensored | `deepseek-v4-pro-uncensored` | Chat Completions |
| DeepSeek V4 Pro Abliterated | `deepseek-v4-pro-abliterated` | Chat Completions |
| GLM 5.3 | `glm-5.3` | Chat Completions |
| GLM 5.3 Uncensored | `glm-5.3-uncensored` | Chat Completions |
| GLM 5.3 Abliterated | `glm-5.3-abliterated` | Chat Completions |
| GLM 5.3 Flash | `glm-5.3-flash` | Chat Completions |
| GLM 5.3 Flash Uncensored | `glm-5.3-flash-uncensored` | Chat Completions |
| GLM 5.3 Flash Abliterated | `glm-5.3-flash-abliterated` | Chat Completions |
| Qwen 3.8 Max | `qwen3.8-max` | Chat Completions |
| Qwen 3.8 Max Uncensored | `qwen3.8-max-uncensored` | Chat Completions |
| GPT-6.1 Sol | `gpt-6.1-sol` | Responses |
| Claude Sonnet 5.5 | `claude-sonnet-5-5` | Anthropic Messages |

This is not the full 37-model list. Use the live page or `models.json` for the complete catalogue.

## Rules

- Use the exact model ID.
- Confirm the protocol.
- Do not assume an OpenRouter slug maps to the same RouterHub ID.
- Availability can change.
- Check pricing and cached-input rates separately.

## Next steps

- [Migration](./05-migration-from-openrouter.md)
- [Pricing](./07-pricing.md)
- [Troubleshooting](./12-troubleshooting.md)
