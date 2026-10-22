# Migrating from OpenRouter

The migration is usually smaller than a rewrite: base URL, key and model ID.

## 1. Create a RouterHub account

Go to [routerhub.si](https://routerhub.si/register?next=onboarding&utm_source=github&utm_medium=docs&utm_campaign=openrouter-alternative) and copy:

- API key;
- base URL;
- exact model ID.

## 2. Change the OpenAI client

```python
import os
from openai import OpenAI

client = OpenAI(
    api_key=os.environ["ROUTERHUB_API_KEY"],
    base_url=os.environ["ROUTERHUB_BASE_URL"],
)

response = client.chat.completions.create(
    model="MODEL_ID_FROM_DASHBOARD",
    messages=[
        {"role": "system", "content": "You are a precise assistant."},
        {"role": "user", "content": "Reply with OK."},
    ],
)
print(response.choices[0].message.content)
```

## 3. Map the model ID

Do not reuse the OpenRouter slug blindly.

| Intended model | RouterHub ID |
|---|---|
| DeepSeek V4.1 Flash | `deepseek-v4.1-flash` |
| DeepSeek V4.1 Flash Uncensored | `deepseek-v4.1-flash-uncensored` |
| DeepSeek V4.1 Flash Abliterated | `deepseek-v4.1-flash-abliterated` |
| GLM 5.3 Flash | `glm-5.3-flash` |
| GLM 5.3 Flash Uncensored | `glm-5.3-flash-uncensored` |
| GLM 5.3 Flash Abliterated | `glm-5.3-flash-abliterated` |
| Qwen 3.8 Max | `qwen3.8-max` |
| Qwen 3.8 Max Uncensored | `qwen3.8-max-uncensored` |

## 4. Compare response shapes

Check:

- streaming;
- tool calls;
- structured output;
- usage accounting;
- error format;
- supported protocol.

## 5. Test before switching traffic

Run a sample of real prompts and compare quality, latency, refusals and cost. Keep the old provider as fallback during the evaluation.

## 6. Update configuration

Move the key and base URL into environment variables or a secrets manager. Do not commit them.

## Common migration mistakes

- Using an OpenRouter model slug as a RouterHub ID.
- Using an Anthropic-style request against a Chat-only entry.
- Forgetting to update the base URL.
- Not checking the live price.
- Switching all traffic before testing.

## Next steps

- [API quickstart](./06-api-quickstart.md)
- [Model catalogue](./04-model-catalogue.md)
- [Troubleshooting](./12-troubleshooting.md)
