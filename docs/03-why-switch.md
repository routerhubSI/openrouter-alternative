# Why Switch? Practical Reasons

## 1. One prepaid key

Top up once and use the balance across supported families. This is simpler than maintaining multiple provider accounts.

## 2. Published prices

Compare input, output and cached-input rates per model. Estimate cost before switching.

## 3. Uncensored and abliterated entries

RouterHub publishes separate entries for reduced-refusal use cases:

- `deepseek-v4.1-flash-uncensored`
- `deepseek-v4.1-flash-abliterated`
- `glm-5.3-uncensored`
- `glm-5.3-flash-uncensored`
- `glm-5.3-flash-abliterated`

## 4. Compatible clients

Use OpenAI SDKs, cURL and compatible tools. Supported Claude entries use Anthropic Messages.

## 5. No subscription

Pay per token. No monthly plan is required.

## 6. Straightforward migration

In many cases the change is:

1. base URL;
2. API key;
3. model ID.

The request shape stays OpenAI-compatible for Chat entries.

## What to verify before switching

- model availability;
- exact model ID;
- protocol (Chat vs Messages);
- price and cached-input rate;
- streaming and tool support;
- quality on your prompts;
- fallback model.

## When not to switch

Stay with OpenRouter if you need its specific routing features, provider marketplace or an integration that RouterHub does not support.

## Next steps

- [RouterHub vs OpenRouter](./02-routerhub-vs-openrouter.md)
- [Migration](./05-migration-from-openrouter.md)
- [Pricing](./07-pricing.md)
