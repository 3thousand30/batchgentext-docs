---
layout: default
title: Finding Your Base URL
nav_order: 4
---

# Finding Your Base URL

The **Base URL** is the root address of the AI provider's API. BatchGen Text with AI appends `/chat/completions` to it when making requests.

If you select one of the nine built-in provider presets, the Base URL is filled in automatically — you don't need to touch it. This page is mainly for custom endpoints or for understanding what the field means.

---

## Base URLs for all built-in providers

| Provider | Base URL |
|---|---|
| OpenAI | `https://api.openai.com/v1` |
| DeepSeek | `https://api.deepseek.com/v1` |
| OpenRouter | `https://openrouter.ai/api/v1` |
| Groq | `https://api.groq.com/openai/v1` |
| Mistral AI | `https://api.mistral.ai/v1` |
| Together AI | `https://api.together.xyz/v1` |
| xAI (Grok) | `https://api.x.ai/v1` |
| Fireworks AI | `https://api.fireworks.ai/inference/v1` |
| Cerebras | `https://api.cerebras.ai/v1` |

---

## Using a custom Base URL

Select **Custom** from the provider dropdown in the settings dialog, then enter your Base URL.

Common custom setups:

| Setup | Typical Base URL |
|---|---|
| Ollama (local) | `http://localhost:11434/v1` |
| LM Studio (local) | `http://localhost:1234/v1` |
| LocalAI | `http://localhost:8080/v1` |
| Azure OpenAI | `https://<your-resource>.openai.azure.com/openai/deployments/<deployment>` |
| Any OpenAI-compatible server | Varies — check your provider's docs |

The endpoint must support the OpenAI `/chat/completions` format. If your provider's docs show a different path structure, use the part before `/chat/completions` as the Base URL.

---

## Common mistakes

**Trailing slash** — do not add a `/` at the end of the Base URL. Use `https://api.openai.com/v1` not `https://api.openai.com/v1/`.

**Including the endpoint path** — the Base URL should stop before `/chat/completions`. The app adds that part automatically.

**HTTP instead of HTTPS** — the app only opens HTTPS URLs for security. Local endpoints (localhost) are an exception handled by your local server setup.

---

## Testing your connection

After entering a Base URL and API key, click **Test connection** in the settings dialog. The app sends a lightweight request to verify the key works before you start a batch.

If the test fails, see [Troubleshooting](troubleshooting) for common error codes.
