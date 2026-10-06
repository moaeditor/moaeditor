<h1 align="center">Free AI for coding</h1>

<p align="center">30 AIs you can code with for free: coding tools with a free plan, free APIs, sign-up credit, and local models</p>

<p align="center"><sub>Last checked: 2026-10-05 (against each provider’s official docs)</sub></p>

<p align="center"><a href="README.md">한국어</a> · <a href="README.en.md">English</a></p>

---

## Contents

- [What’s different here](#whats-different-here)
- [At a glance](#at-a-glance)
- [How to use](#how-to-use)
- [Try it](#try-it)
- [Coding tools with a free plan (4)](#coding-tools-with-a-free-plan-4)
- [APIs with an ongoing free tier (12)](#apis-with-an-ongoing-free-tier-12)
- [APIs with sign-up credit (6)](#apis-with-sign-up-credit-6)
- [Local models, no quota (8)](#local-models-no-quota-8)
- [Use several as one team](#use-several-as-one-team)
- [Spot a mistake?](#spot-a-mistake)

## What’s different here
- **Not just APIs.** Coding tools with a free plan (Copilot, Cursor and more) and local models are in the same list.
- **Whether your input is used for training** is noted. Where it wasn’t checked, it says so instead of guessing.
- **The date each entry was checked** against official docs, updated when terms change.

## At a glance
| Group | Count | Examples |
|---|---|---|
| Coding tools with a free plan | 4 | GitHub Copilot, Cursor, Mistral Vibe, OpenCode |
| APIs with an ongoing free tier | 12 | Google Gemini API, Groq, OpenRouter, NVIDIA NIM |
| APIs with sign-up credit | 6 | Cerebras, Fireworks, Nebius, Novita |
| Local models, no quota | 8 | Ollama, LM Studio, llama.cpp, Jan |

## How to use
1. Pick one from the tables below. If you’re new, start with Groq: about 1,000 free requests a day.
2. Create a key with the **Get key** link and copy it.
3. Put the **Base URL** and key into any OpenAI-compatible tool or SDK. Every service here exposes an OpenAI-compatible endpoint.

## Try it

Available model names depend on your key, so list them first. (Groq example)

```python
from openai import OpenAI

client = OpenAI(base_url="https://api.groq.com/openai/v1", api_key="GROQ_API_KEY")
for m in client.models.list():
    print(m.id)
```

```bash
curl https://api.groq.com/openai/v1/models -H "Authorization: Bearer $GROQ_API_KEY"
```

## Coding tools with a free plan (4)

| Tool | How you use it | Official page |
|---|---|---|
| **GitHub Copilot** | Works with GitHub Copilot, including the free plan | [Docs](https://github.com/github/copilot-cli) |
| **Cursor** | Works with a Cursor plan, including free Hobby | [Docs](https://cursor.com/docs/cli/installation) |
| **Mistral Vibe** | Works with a Mistral account, free too | [Docs](https://docs.mistral.ai/vibe/code/cli/install-setup) |
| **OpenCode** | Works with ChatGPT, paid Copilot, OpenCode Zen or Go, or an API key. Without signing in it uses OpenCode free models, which may use what you send to improve the model | [Docs](https://opencode.ai/docs) |

## APIs with an ongoing free tier (12)

| Service | Free terms | Trains on input | Base URL | Key | Docs |
|---|---|---|---|---|---|
| **Google Gemini API** | Flash and Flash-Lite are free. Request limits apply | Free tier may be used for training | `https://generativelanguage.googleapis.com/v1beta/openai` | [Get key](https://aistudio.google.com/apikey) | [Docs](https://ai.google.dev/gemini-api/docs/openai) |
| **Groq** | Free for about 30 requests a minute and 1,000 a day. Varies by model | Not checked | `https://api.groq.com/openai/v1` | [Get key](https://console.groq.com/keys) | [Docs](https://console.groq.com/docs/openai) |
| **OpenRouter** | :free models: 20 requests a minute, 50 a day. 1,000 a day after you add $10 or more | Not checked | `https://openrouter.ai/api/v1` | [Get key](https://openrouter.ai/settings/keys) | [Docs](https://openrouter.ai/docs/api/reference/limits) |
| **NVIDIA NIM** | Free for about 40 requests a minute, for development and testing | Not checked | `https://integrate.api.nvidia.com/v1` | [Get key](https://build.nvidia.com/settings/api-keys) | [Docs](https://build.nvidia.com/) |
| **Mistral** | The free plan includes monthly credits | Free tier may be used for training | `https://api.mistral.ai/v1` | [Get key](https://console.mistral.ai/api-keys) | [Docs](https://docs.mistral.ai/api/) |
| **Hugging Face** | Free gets $0.10 a month, PRO gets $2 in credits | Not checked | `https://router.huggingface.co/v1` | [Get key](https://huggingface.co/settings/tokens/new?ownUserPermissions=inference.serverless.write&tokenType=fineGrained) | [Docs](https://huggingface.co/docs/inference-providers/index) |
| **SambaNova** | Free for up to 20 requests a minute and 20 a day | Not checked | `https://api.sambanova.ai/v1` | [Get key](https://cloud.sambanova.ai/apis) | [Docs](https://docs.sambanova.ai/docs/en/get-started/api-keys-urls) |
| **Z.ai GLM** | Some Flash models are free | Not checked | `https://api.z.ai/api/paas/v4` | [Get key](https://z.ai/manage-apikey/apikey-list) | [Docs](https://docs.z.ai/guides/develop/http/introduction) |
| **Cohere** | Trial key: up to 1,000 calls a month and 20 a minute | Not checked | `https://api.cohere.ai/compatibility/v1` | [Get key](https://dashboard.cohere.com/api-keys) | [Docs](https://docs.cohere.com/docs/compatibility-api) |
| **Ollama Cloud** | The free plan has starter credits. Some models only, one request at a time | Not checked | `https://ollama.com/v1` | [Get key](https://ollama.com/settings/keys) | [Docs](https://docs.ollama.com/api/openai-compatibility) |
| **Vercel AI Gateway** | $5 in credits per team each month. Ends after your first payment | Not checked | `https://ai-gateway.vercel.sh/v1` | [Get key](https://vercel.com/d?to=%2F%5Bteam%5D%2F%7E%2Fai-gateway%2Fapi-keys&title=AI+Gateway+API+Keys) | [Docs](https://vercel.com/docs/ai-gateway/sdks-and-apis/openai-chat-completions) |
| **FreeLLMAPI** | The relay is free. Limits depend on each provider you add | Free tier may be used for training | `http://127.0.0.1:3001/v1` |  | [Docs](https://github.com/tashfeenahmed/freellmapi) |

## APIs with sign-up credit (6)

| Service | Free terms | Trains on input | Base URL | Key | Docs |
|---|---|---|---|---|---|
| **Cerebras** | Add a payment method to get $5 in credits for 30 days. There is no ongoing free tier | Not checked | `https://api.cerebras.ai/v1` | [Get key](https://cloud.cerebras.ai/platform) | [Docs](https://inference-docs.cerebras.ai/resources/openai) |
| **Fireworks** | $1 in credits when you sign up | Not checked | `https://api.fireworks.ai/inference/v1` | [Get key](https://app.fireworks.ai/settings/users/api-keys) | [Docs](https://docs.fireworks.ai/tools-sdks/openai-compatibility) |
| **Nebius** | Sign up and add a card to get $1 in credits for 30 days | Not checked | `https://api.tokenfactory.nebius.com/v1` | [Get key](https://tokenfactory.nebius.com/project/api-keys) | [Docs](https://docs.tokenfactory.nebius.com/) |
| **Novita** | Credits when you sign up | Not checked | `https://api.novita.ai/openai` | [Get key](https://novita.ai/settings/key-management) | [Docs](https://docs.novita.ai/guides/llm-api) |
| **Upstage Solar** | Credits when you sign up | Not checked | `https://api.upstage.ai/v1` | [Get key](https://console.upstage.ai/api-keys) | [Docs](https://console.upstage.ai/docs) |
| **Alibaba Qwen (Model Studio)** | Tokens when you sign up | Not checked | `https://dashscope-intl.aliyuncs.com/compatible-mode/v1` | [Get key](https://modelstudio.console.alibabacloud.com/ap-southeast-1/settings/api-key) | [Docs](https://www.alibabacloud.com/help/en/model-studio/) |

## Local models, no quota (8)

Install the program, download a model, then use the address below as an OpenAI-compatible endpoint. No key needed.

| Program | Terms | Default URL | Docs |
|---|---|---|---|
| **Ollama** | Free, runs on your PC | `http://127.0.0.1:11434/v1` | [Docs](https://docs.ollama.com/api/openai-compatibility) |
| **LM Studio** | Free, runs on your PC | `http://127.0.0.1:1234/v1` | [Docs](https://lmstudio.ai/docs/developer/api-changelog) |
| **llama.cpp** | Free, runs on your PC | `http://127.0.0.1:8080/v1` | [Docs](https://github.com/ggml-org/llama.cpp/blob/master/tools/server/README.md) |
| **Jan** | Free, runs on your PC | `http://127.0.0.1:1337/v1` | [Docs](https://www.jan.ai/docs/desktop/api-preference) |
| **Foundry Local** | Free, runs on your PC | `http://127.0.0.1:5272/v1` | [Docs](https://learn.microsoft.com/en-us/azure/foundry-local/reference/reference-cli) |
| **Docker Model Runner** | Free, runs on your PC | `http://127.0.0.1:12434/engines/v1` | [Docs](https://docs.docker.com/ai/model-runner/api-reference/) |
| **vLLM** | Free, your own server | `http://127.0.0.1:8000/v1` | [Docs](https://docs.vllm.ai/en/latest/serving/online_serving/) |
| **SGLang** | Free, your own server | `http://127.0.0.1:30000/v1` | [Docs](https://docs.sglang.ai/) |

## Use several as one team
Connect several of these and [MoaEditor](../../README.en.md) puts them into one team of a director, team leads, staff and interns and splits the work. When one hits its limit, the next picks up. “Connect free AIs” sets up Copilot, Cursor, Groq, OpenRouter and a local model one after another. Windows, free to use.

## Spot a mistake?
If terms changed or something is missing, open an [issue](https://github.com/moaeditor/moaeditor/issues/new/choose) with a link to the official page. See [CONTRIBUTING.md](CONTRIBUTING.md).

The text of this list and data.json are free to reuse under [CC BY 4.0](LICENSE). Service names are trademarks of their owners.
