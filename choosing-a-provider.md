---
layout: default
title: Choosing an AI Provider
nav_order: 3
---

# Choosing an AI Provider

BatchGen Text with AI works with any OpenAI-compatible API. Nine providers are built in — you just pick one, get an API key, and paste it in. No other configuration needed.

---

## Quick recommendation

| If you want... | Use |
|---|---|
| Cheapest option for bulk generation | **DeepSeek** |
| Best overall quality | **OpenAI** (gpt-4o or gpt-4o-mini) |
| Fastest responses | **Groq** |
| No account required (pay-as-you-go, many models) | **OpenRouter** |
| European data residency | **Mistral AI** |

---

## All supported providers

| Provider | Strengths | Free tier | Sign up |
|---|---|---|---|
| **OpenAI** | Best quality, most reliable, widest model range | No (credits on signup) | [platform.openai.com](https://platform.openai.com) |
| **DeepSeek** | Extremely low cost, strong quality | Yes (limited) | [platform.deepseek.com](https://platform.deepseek.com) |
| **OpenRouter** | Access to 100+ models from one key, pay per use | No | [openrouter.ai](https://openrouter.ai) |
| **Groq** | Very fast inference, good for high-volume batches | Yes (rate limited) | [console.groq.com](https://console.groq.com) |
| **Mistral AI** | Strong multilingual support, EU-based | Yes (limited) | [console.mistral.ai](https://console.mistral.ai) |
| **Together AI** | Wide model selection, competitive pricing | Yes ($1 credit) | [api.together.ai](https://api.together.ai) |
| **xAI (Grok)** | Grok models, good reasoning | No | [console.x.ai](https://console.x.ai) |
| **Fireworks AI** | Fast, cost-effective, fine-tuned models | Yes ($1 credit) | [fireworks.ai](https://fireworks.ai) |
| **Cerebras** | Ultra-fast inference on large models | Yes (limited) | [cloud.cerebras.ai](https://cloud.cerebras.ai) |

---

## Cost considerations

All providers charge per **token** — roughly 1 token per 0.75 words. For content generation:

- A 800-word blog article uses roughly 1,500–2,500 tokens total (prompt + output)
- A batch of 20 articles uses roughly 30,000–50,000 tokens
- At DeepSeek's rates (~$0.14/million tokens), a 20-article batch costs a few cents
- At OpenAI gpt-4o-mini rates (~$0.15/million input, $0.60/million output), similar cost

The app displays token usage per article and a total at the end of each run, so you can track costs in real time.

---

## Using a custom endpoint

If you use a self-hosted model (Ollama, LM Studio, LocalAI) or a provider not in the list, select **Custom** from the provider dropdown and enter your endpoint's base URL manually.

The endpoint must be OpenAI-compatible (`/chat/completions` format). See [Finding Your Base URL](base-url) for details.

---

## Switching providers

You can switch providers at any time from the settings icon. Each API key is saved separately — switching providers doesn't delete your previous keys.
