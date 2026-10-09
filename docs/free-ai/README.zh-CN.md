<h1 align="center">免费用于编程的 AI</h1>

<p align="center">31 个可以免费用来写代码的 AI：有免费计划的编程工具、免费 API、注册赠送额度的 API，以及本地模型</p>

<p align="center"><sub>最后核对：2026-10-10（以各服务商官方文档为准）</sub></p>

<p align="center"><a href="README.md">한국어</a> · <a href="README.en.md">English</a> · <a href="README.zh-CN.md">简体中文</a></p>

---

## 目录

- [这份列表的不同之处](#这份列表的不同之处)
- [一览](#一览)
- [怎么用](#怎么用)
- [马上试试](#马上试试)
- [有免费计划的编程工具 (4)](#有免费计划的编程工具-4)
- [长期免费的 API (13)](#长期免费的-api-13)
- [注册赠送额度的 API (6)](#注册赠送额度的-api-6)
- [本地模型，不限用量 (8)](#本地模型不限用量-8)
- [把多个 AI 组成一个团队](#把多个-ai-组成一个团队)
- [发现错误？](#发现错误)

## 这份列表的不同之处
- **不只是 API。** 有免费计划的编程工具（Copilot、Cursor 等）和在自己电脑上运行的本地模型也收录在内。
- **标明输入是否会被用于训练。** 没有核实的地方直接写“未核实”，不做猜测。
- **标明核对日期。** 每一项都对照官方文档核对过，条件变化时会更新。

## 一览
| 分组 | 数量 | 例子 |
|---|---|---|
| 有免费计划的编程工具 | 4 | GitHub Copilot, Cursor, Mistral Vibe, OpenCode |
| 长期免费的 API | 13 | Google Gemini API, Groq, OpenRouter, NVIDIA NIM |
| 注册赠送额度的 API | 6 | Cerebras, Fireworks, Nebius, Novita |
| 本地模型，不限用量 | 8 | Ollama, LM Studio, llama.cpp, Jan |

## 怎么用
1. 从下面的表里选一个。第一次用推荐 Groq，每天大约可以免费调用 1,000 次。
2. 点 **获取密钥** 链接创建密钥并复制。
3. 把 **Base URL** 和密钥填进任何兼容 OpenAI 的工具或 SDK。表里的服务都提供兼容 OpenAI 的地址。

## 马上试试

可用的模型名称因密钥而异，先列出来看看。（以 Groq 为例）

```python
from openai import OpenAI

client = OpenAI(base_url="https://api.groq.com/openai/v1", api_key="GROQ_API_KEY")
for m in client.models.list():
    print(m.id)
```

```bash
curl https://api.groq.com/openai/v1/models -H "Authorization: Bearer $GROQ_API_KEY"
```

## 有免费计划的编程工具 (4)

| 工具 | 怎么用 | 官方说明 |
|---|---|---|
| **GitHub Copilot** | 使用 GitHub Copilot 订阅，免费计划也可以 | [文档](https://github.com/github/copilot-cli) |
| **Cursor** | 使用 Cursor 订阅，免费的 Hobby 计划也可以 | [文档](https://cursor.com/docs/cli/installation) |
| **Mistral Vibe** | 使用 Mistral 账号，免费也能用 | [文档](https://docs.mistral.ai/vibe/code/cli/install-setup) |
| **OpenCode** | 可用 ChatGPT 订阅、付费 Copilot、OpenCode Zen 或 Go，或 API 密钥。不登录时使用 OpenCode 免费模型，发送的内容可能被用于改进模型 | [文档](https://opencode.ai/docs) |

## 长期免费的 API (13)

| 服务 | 免费条件 | 输入用于训练 | Base URL | 密钥 | 文档 |
|---|---|---|---|---|---|
| **Google Gemini API** | Flash 和 Flash-Lite 免费，有请求次数限制 | 免费层可能用于训练 | `https://generativelanguage.googleapis.com/v1beta/openai` | [获取密钥](https://aistudio.google.com/apikey) | [文档](https://ai.google.dev/gemini-api/docs/openai) |
| **Groq** | 免费，约每分钟 30 次、每天 1,000 次请求，因模型而异 | 未核实 | `https://api.groq.com/openai/v1` | [获取密钥](https://console.groq.com/keys) | [文档](https://console.groq.com/docs/openai) |
| **OpenRouter** | :free 模型每分钟 20 次、每天 50 次。充值 10 美元以上后每天 1,000 次 | 未核实 | `https://openrouter.ai/api/v1` | [获取密钥](https://openrouter.ai/settings/keys) | [文档](https://openrouter.ai/docs/api/reference/limits) |
| **NVIDIA NIM** | 免费，约每分钟 40 次请求，用于开发和测试 | 未核实 | `https://integrate.api.nvidia.com/v1` | [获取密钥](https://build.nvidia.com/settings/api-keys) | [文档](https://build.nvidia.com/) |
| **Mistral** | 免费计划包含每月额度 | 免费层可能用于训练 | `https://api.mistral.ai/v1` | [获取密钥](https://console.mistral.ai/api-keys) | [文档](https://docs.mistral.ai/api/) |
| **Hugging Face** | 免费用户每月 0.10 美元额度，PRO 用户 2 美元 | 未核实 | `https://router.huggingface.co/v1` | [获取密钥](https://huggingface.co/settings/tokens/new?ownUserPermissions=inference.serverless.write&tokenType=fineGrained) | [文档](https://huggingface.co/docs/inference-providers/index) |
| **SambaNova** | 免费，最多每分钟 20 次、每天 20 次请求 | 未核实 | `https://api.sambanova.ai/v1` | [获取密钥](https://cloud.sambanova.ai/apis) | [文档](https://docs.sambanova.ai/docs/en/get-started/api-keys-urls) |
| **Z.ai GLM** | 部分 Flash 模型免费 | 未核实 | `https://api.z.ai/api/paas/v4` | [获取密钥](https://z.ai/manage-apikey/apikey-list) | [文档](https://docs.z.ai/guides/develop/http/introduction) |
| **Cohere** | 试用密钥：每月最多 1,000 次调用，每分钟 20 次 | 未核实 | `https://api.cohere.ai/compatibility/v1` | [获取密钥](https://dashboard.cohere.com/api-keys) | [文档](https://docs.cohere.com/docs/compatibility-api) |
| **Ollama Cloud** | 免费计划有入门额度。仅限部分模型，一次只处理一个请求 | 未核实 | `https://ollama.com/v1` | [获取密钥](https://ollama.com/settings/keys) | [文档](https://docs.ollama.com/api/openai-compatibility) |
| **Vercel AI Gateway** | 每个团队每月 5 美元额度，首次付款后结束 | 未核实 | `https://ai-gateway.vercel.sh/v1` | [获取密钥](https://vercel.com/d?to=%2F%5Bteam%5D%2F%7E%2Fai-gateway%2Fapi-keys&title=AI+Gateway+API+Keys) | [文档](https://vercel.com/docs/ai-gateway/sdks-and-apis/openai-chat-completions) |
| **Cloudflare Workers AI** | Workers AI 模型每天有 10,000 个免费 Neurons 额度（因模型而异，超出后按量付费） | 不用于训练 | `https://api.cloudflare.com/client/v4/accounts/{account_id}/ai/v1` | [获取密钥](https://dash.cloudflare.com/profile/api-tokens) | [文档](https://developers.cloudflare.com/ai-gateway/usage/rest-api/) |
| **FreeLLMAPI** | 中转本身免费，限制取决于你添加的各个服务商 | 免费层可能用于训练 | `http://127.0.0.1:3001/v1` |  | [文档](https://github.com/tashfeenahmed/freellmapi) |

## 注册赠送额度的 API (6)

| 服务 | 免费条件 | 输入用于训练 | Base URL | 密钥 | 文档 |
|---|---|---|---|---|---|
| **Cerebras** | 没有长期免费层。添加付款方式后可获得 30 天内有效的 5 美元额度 | 未核实 | `https://api.cerebras.ai/v1` | [获取密钥](https://cloud.cerebras.ai/platform) | [文档](https://inference-docs.cerebras.ai/resources/openai) |
| **Fireworks** | 注册送 1 美元额度 | 未核实 | `https://api.fireworks.ai/inference/v1` | [获取密钥](https://app.fireworks.ai/settings/users/api-keys) | [文档](https://docs.fireworks.ai/tools-sdks/openai-compatibility) |
| **Nebius** | 注册并绑定银行卡后获得 30 天内有效的 1 美元额度 | 未核实 | `https://api.tokenfactory.nebius.com/v1` | [获取密钥](https://tokenfactory.nebius.com/project/api-keys) | [文档](https://docs.tokenfactory.nebius.com/) |
| **Novita** | 注册送额度 | 未核实 | `https://api.novita.ai/openai` | [获取密钥](https://novita.ai/settings/key-management) | [文档](https://docs.novita.ai/guides/llm-api) |
| **Upstage Solar** | 注册送额度 | 未核实 | `https://api.upstage.ai/v1` | [获取密钥](https://console.upstage.ai/api-keys) | [文档](https://console.upstage.ai/docs) |
| **Alibaba Qwen (Model Studio)** | 注册送 Token | 未核实 | `https://dashscope-intl.aliyuncs.com/compatible-mode/v1` | [获取密钥](https://modelstudio.console.alibabacloud.com/ap-southeast-1/settings/api-key) | [文档](https://www.alibabacloud.com/help/en/model-studio/) |

## 本地模型，不限用量 (8)

安装程序并下载模型后，把下面的地址当作兼容 OpenAI 的地址使用。不需要密钥。

| 程序 | 条件 | 默认地址 | 文档 |
|---|---|---|---|
| **Ollama** | 免费，在你的电脑上运行 | `http://127.0.0.1:11434/v1` | [文档](https://docs.ollama.com/api/openai-compatibility) |
| **LM Studio** | 免费，在你的电脑上运行 | `http://127.0.0.1:1234/v1` | [文档](https://lmstudio.ai/docs/developer/api-changelog) |
| **llama.cpp** | 免费，在你的电脑上运行 | `http://127.0.0.1:8080/v1` | [文档](https://github.com/ggml-org/llama.cpp/blob/master/tools/server/README.md) |
| **Jan** | 免费，在你的电脑上运行 | `http://127.0.0.1:1337/v1` | [文档](https://www.jan.ai/docs/desktop/api-preference) |
| **Foundry Local** | 免费，在你的电脑上运行 | `http://127.0.0.1:5272/v1` | [文档](https://learn.microsoft.com/en-us/azure/foundry-local/reference/reference-cli) |
| **Docker Model Runner** | 免费，在你的电脑上运行 | `http://127.0.0.1:12434/engines/v1` | [文档](https://docs.docker.com/ai/model-runner/api-reference/) |
| **vLLM** | 免费，运行在你自己的服务器上 | `http://127.0.0.1:8000/v1` | [文档](https://docs.vllm.ai/en/latest/serving/online_serving/) |
| **SGLang** | 免费，运行在你自己的服务器上 | `http://127.0.0.1:30000/v1` | [文档](https://docs.sglang.ai/) |

## 把多个 AI 组成一个团队
连接这里的几个 AI 后，[MoaEditor](../../README.zh-CN.md) 会把它们编成由总负责人、组长、员工和实习生组成的团队，分工完成任务。一个 AI 用到上限时，下一个接着做。点击 **Connect free AIs** 会依次连接 Copilot、Cursor、Groq、OpenRouter 和本地模型（应用界面目前只有韩语和英语）。适用于 Windows，可免费使用。

## 发现错误？
如果条件有变或有遗漏，请附上官方页面链接提交 [issue](https://github.com/moaeditor/moaeditor/issues/new/choose)。详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

本列表的文字和 data.json 以 [CC BY 4.0](LICENSE) 授权，可自由使用。服务名称是各自所有者的商标。
