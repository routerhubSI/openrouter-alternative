# API Quickstart

## 1. Create an account

Go to [routerhub.si](https://routerhub.si/register?next=onboarding&utm_source=github&utm_medium=docs&utm_campaign=openrouter-alternative). Copy:

- API key — starts with `sk-`;
- base URL — exact value from the dashboard;
- model ID — from the live catalogue.

```bash
export ROUTERHUB_API_KEY="sk-..."
export ROUTERHUB_BASE_URL="https://.../v1"
```

## 2. OpenAI-compatible request

```python
import os
from openai import OpenAI

client = OpenAI(
    api_key=os.environ["ROUTERHUB_API_KEY"],
    base_url=os.environ["ROUTERHUB_BASE_URL"],
)

r = client.chat.completions.create(
    model="deepseek-v4.1-flash-uncensored",
    messages=[
        {"role": "system", "content": "Answer clearly and state assumptions."},
        {"role": "user", "content": "Compare two model choices for my workload."},
    ],
)
print(r.choices[0].message.content)
```

## 3. cURL

```bash
curl "$ROUTERHUB_BASE_URL/chat/completions" \
  -H "Authorization: Bearer $ROUTERHUB_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "MODEL_ID_FROM_DASHBOARD",
    "messages": [{"role": "user", "content": "Reply with OK."}]
  }'
```

## 4. Protocol check

- DeepSeek, GLM, Qwen, Grok and Gemini entries use **Chat Completions**.
- Claude entries use **Anthropic Messages**.
- OpenAI Responses entries use the Responses API.
- Confirm the protocol before integrating.

## 5. Common errors

| Error | Cause | Fix |
|---|---|---|
| `401` | Wrong/missing key | Re-copy key |
| `404` every path | Wrong base URL | Copy exact URL |
| `404 model_not_found` | Wrong model ID | Use live catalogue |
| `429` | Rate/balance limit | Check usage and balance |
| Empty response | Wrong protocol | Confirm Chat vs Messages |

## Next steps

- [Pricing](./07-pricing.md)
- [Migration](./05-migration-from-openrouter.md)
- [Troubleshooting](./12-troubleshooting.md)
