# Troubleshooting

## `401 Unauthorized`

Wrong or missing key. Re-copy the RouterHub key.

## `404` on every path

Wrong base URL. Copy the exact value from the dashboard.

## `404 model_not_found`

The model ID is wrong, renamed or retired. Use the live catalogue.

## `400 Bad Request`

Check:

- `messages` array;
- role names;
- field support;
- protocol (Chat vs Messages).

## `429 Too Many Requests`

Check balance and rate limits; add backoff; reduce concurrency.

## Empty response or unsupported stream

Confirm the model supports streaming. Disable it for a compatibility test.

## Tool calls fail

Confirm the exact model supports tools, validate the schema, and inspect the returned `tool_calls`.

## Claude Code ignores the model

Use an Anthropic Messages-compatible entry, not a Chat-only DeepSeek/GLM/Qwen entry.

## Migration from OpenRouter fails

- Check the base URL.
- Replace the OpenRouter model slug with the RouterHub model ID.
- Confirm protocol support.
- Test a simple `Reply with OK` request.
- Compare usage and errors.

## Still stuck?

Collect the path, status code, error body, model ID, client version and timestamp. Contact [RouterHub support](https://t.me/routerhubsi). Never send your full API key.

## Next steps

- [API quickstart](./06-api-quickstart.md)
- [Migration](./05-migration-from-openrouter.md)
- [FAQ](./10-faq.md)
