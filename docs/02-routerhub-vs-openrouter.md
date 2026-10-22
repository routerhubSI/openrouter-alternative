# RouterHub vs OpenRouter

A practical comparison. OpenRouter-specific details belong to OpenRouter; verify them on the official site.

| Area | RouterHub | OpenRouter |
|---|---|---|
| **Type** | Prepaid API gateway | Model routing/marketplace platform |
| **Catalogue** | 37 published models | Check OpenRouter |
| **Model families** | GPT, Claude, Gemini, Grok, DeepSeek, GLM, Qwen | Check OpenRouter |
| **Billing** | Prepaid, pay per token, card/crypto | Check OpenRouter |
| **Subscription** | None | Check OpenRouter |
| **API formats** | OpenAI Chat Completions; Anthropic Messages where supported | Check OpenRouter |
| **Uncensored/abliterated** | Explicit entries where listed | Depends on current listings |
| **Routing features** | Focused gateway | OpenRouter-specific routing features may be broader |
| **Migration** | OpenAI-compatible base URL/key/ID change | — |

## Where RouterHub is different

### 1. Prepaid simplicity

RouterHub uses prepaid credits and pay-per-token billing. There is no subscription.

### 2. Explicit reduced-refusal entries

The catalogue separates standard, uncensored and abliterated entries:

```text
deepseek-v4.1-flash
deepseek-v4.1-flash-uncensored
deepseek-v4.1-flash-abliterated
glm-5.3-flash
glm-5.3-flash-uncensored
glm-5.3-flash-abliterated
```

### 3. Published model IDs and prices

The catalogue publishes exact IDs and per-million-token rates. This reduces guessing during migration.

### 4. Both OpenAI and Anthropic styles

OpenAI-compatible entries use Chat Completions. Supported Claude entries use Anthropic Messages. Confirm the protocol per model.

## Where OpenRouter may still be better

- You rely on OpenRouter-specific routing or provider selection.
- You need an integration that only works with OpenRouter.
- You need a specific model or provider not listed on RouterHub.
- You prefer OpenRouter’s account, billing or marketplace setup.

## Decision rule

- If the blocker is **access + simple prepaid billing + uncensored/abliterated entries**, evaluate RouterHub.
- If the blocker is **OpenRouter-specific routing or marketplace features**, stay with OpenRouter or verify a direct equivalent.

## Next steps

- [Why switch](./03-why-switch.md)
- [Migration](./05-migration-from-openrouter.md)
- [Model catalogue](./04-model-catalogue.md)
