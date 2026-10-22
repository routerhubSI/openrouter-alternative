# Pricing

RouterHub uses prepaid, pay-per-token billing. Published rates are USD per million tokens and were checked **2026-10-27**.

| Model | API ID | Input | Output | Cached input |
|---|---|---:|---:|---:|
| DeepSeek V4.1 Flash | `deepseek-v4.1-flash` | $0.10 | $0.40 | $0.0026906 |
| DeepSeek V4.1 Flash Uncensored | `deepseek-v4.1-flash-uncensored` | $0.15 | $0.60 | $0.0026906 |
| DeepSeek V4.1 Flash Abliterated | `deepseek-v4.1-flash-abliterated` | $0.30 | $1.25 | $0.055 |
| DeepSeek V4 Pro | `deepseek-v4-pro` | $0.15 | $0.30 | $0.0016 |
| DeepSeek V4 Pro Uncensored | `deepseek-v4-pro-uncensored` | $0.20 | $0.40 | $0.0016 |
| DeepSeek V4 Pro Abliterated | `deepseek-v4-pro-abliterated` | $0.40 | $1.60 | $0.04 |
| GLM 5.3 | `glm-5.3` | $0.15 | $0.47142857 | $0.11659199 |
| GLM 5.3 Uncensored | `glm-5.3-uncensored` | $0.20 | $0.62857143 | $0.11659199 |
| GLM 5.3 Abliterated | `glm-5.3-abliterated` | $0.40 | $1.33333333 | $0.16 |
| GLM 5.3 Flash | `glm-5.3-flash` | $0.10 | $0.33333333 | $0.013453 |
| GLM 5.3 Flash Uncensored | `glm-5.3-flash-uncensored` | $0.15 | $0.50 | $0.013453 |
| GLM 5.3 Flash Abliterated | `glm-5.3-flash-abliterated` | $0.30 | $1.00 | $0.12 |
| Qwen 3.8 Max | `qwen3.8-max` | $0.20 | $0.60 | $0.025 |
| Qwen 3.8 Max Uncensored | `qwen3.8-max-uncensored` | $0.25 | $0.75 | $0.03125 |

The full 37-model catalogue is at [routerhub.si/models](https://routerhub.si/models).

## Cost per successful task

```text
cost_per_success = total cost / successful tasks
```

Include retries, failed requests, cached input and output tokens.

## Billing notes

- Prepaid balance; no subscription.
- Card and crypto top-ups.
- Cached-input rates can materially reduce repeated-prompt cost.
- Re-check prices before production deployment.

## Next steps

- [Uncensored and abliterated](./08-uncensored-and-abliterated.md)
- [Migration](./05-migration-from-openrouter.md)
- [FAQ](./10-faq.md)
