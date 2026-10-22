# Uncensored and Abliterated Models

RouterHub publishes both uncensored and abliterated entries where available.

## Definitions

- **Abliterated** — model weights modified to reduce the refusal direction.
- **Uncensored** — a broader outcome: the model refuses less often, regardless of the method.

A model can be both. The label does not guarantee behavior; the exact model ID does.

## Current examples

| Family | Abliterated | Uncensored |
|---|---|---|
| DeepSeek V4.1 Flash | `deepseek-v4.1-flash-abliterated` | `deepseek-v4.1-flash-uncensored` |
| DeepSeek V4 Pro | `deepseek-v4-pro-abliterated` | `deepseek-v4-pro-uncensored` |
| GLM 5.3 | `glm-5.3-abliterated` | `glm-5.3-uncensored` |
| GLM 5.3 Flash | `glm-5.3-flash-abliterated` | `glm-5.3-flash-uncensored` |
| Qwen 3.8 Max | not listed | `qwen3.8-max-uncensored` |

## Price signal

For DeepSeek and GLM pairs, the uncensored entry is often cheaper. Qwen 3.8 Max Uncensored is more expensive than standard Qwen.

## What to test

- refusal rate on legitimate prompts;
- output quality;
- tone and repetition;
- tool calls and structured output;
- cost per successful task.

## Recommended reading

- [Uncensored vs abliterated comparison](https://github.com/routerhubSI/uncensored-vs-abliterated-ai)
- [Pricing](./07-pricing.md)
- [Safety](./11-safety.md)
