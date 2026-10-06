<h1 align="center">코딩에 무료로 쓰는 AI</h1>

<p align="center">돈을 내지 않고 코딩에 쓸 수 있는 AI 30곳. 무료 요금제 코딩 도구, 무료 API, 가입 크레딧, 내 PC 모델까지</p>

<p align="center"><sub>마지막 확인: 2026-10-05 (각 회사 공식 문서 기준)</sub></p>

<p align="center"><a href="README.md">한국어</a> · <a href="README.en.md">English</a></p>

---

## 목차

- [이 목록이 다른 점](#이-목록이-다른-점)
- [한눈에 보기](#한눈에-보기)
- [이렇게 쓰세요](#이렇게-쓰세요)
- [바로 써 보기](#바로-써-보기)
- [무료 요금제로 쓰는 코딩 도구 (4)](#무료-요금제로-쓰는-코딩-도구-4)
- [계속 무료로 쓰는 API (12)](#계속-무료로-쓰는-api-12)
- [가입하면 크레딧을 주는 API (6)](#가입하면-크레딧을-주는-api-6)
- [내 PC 모델, 사용량 없음 (8)](#내-pc-모델-사용량-없음-8)
- [여럿을 한 팀으로 쓰기](#여럿을-한-팀으로-쓰기)
- [고칠 곳이 있으면](#고칠-곳이-있으면)

## 이 목록이 다른 점
- **API만이 아닙니다.** 무료 요금제로 쓰는 코딩 도구(Copilot, Cursor 등)와 내 PC에서 돌리는 모델까지 함께 모았습니다.
- **입력이 학습에 쓰이는지** 적었습니다. 확인하지 못한 곳은 지어내지 않고 "확인 못 함"으로 둡니다.
- **공식 문서로 확인한 날짜**를 적고, 조건이 바뀌면 고칩니다.

## 한눈에 보기
| 묶음 | 수 | 예 |
|---|---|---|
| 무료 요금제로 쓰는 코딩 도구 | 4 | GitHub Copilot, Cursor, Mistral Vibe, OpenCode |
| 계속 무료로 쓰는 API | 12 | Google Gemini API, Groq, OpenRouter, NVIDIA NIM |
| 가입하면 크레딧을 주는 API | 6 | Cerebras, Fireworks, Nebius, Novita |
| 내 PC 모델, 사용량 없음 | 8 | Ollama, LM Studio, llama.cpp, Jan |

## 이렇게 쓰세요
1. 아래 표에서 하나를 고릅니다. 처음이라면 Groq가 쉽습니다. 무료로 하루 1,000회쯤 쓸 수 있습니다.
2. **키 만들기** 링크에서 키를 만들어 복사합니다.
3. **Base URL**과 키를 OpenAI 호환 도구나 SDK에 넣습니다. 표의 서비스는 모두 OpenAI 호환 주소를 냅니다.

## 바로 써 보기

쓸 수 있는 모델 이름은 키마다 다르니, 먼저 목록을 받아 보세요. (Groq 예시)

```python
from openai import OpenAI

client = OpenAI(base_url="https://api.groq.com/openai/v1", api_key="GROQ_API_KEY")
for m in client.models.list():
    print(m.id)
```

```bash
curl https://api.groq.com/openai/v1/models -H "Authorization: Bearer $GROQ_API_KEY"
```

## 무료 요금제로 쓰는 코딩 도구 (4)

| 도구 | 무엇으로 쓰나 | 공식 안내 |
|---|---|---|
| **GitHub Copilot** | GitHub Copilot 구독으로 씁니다. 무료 요금제도 됩니다 | [문서](https://github.com/github/copilot-cli) |
| **Cursor** | Cursor 구독으로 씁니다. 무료 Hobby 요금제도 됩니다 | [문서](https://cursor.com/docs/cli/installation) |
| **Mistral Vibe** | Mistral 계정으로 씁니다. 무료로도 쓸 수 있습니다 | [문서](https://docs.mistral.ai/vibe/code/cli/install-setup) |
| **OpenCode** | ChatGPT 구독, 유료 Copilot 구독, OpenCode Zen이나 Go, API 키로 씁니다. 로그인하지 않으면 OpenCode 무료 모델로 돌아가는데, 이때 보낸 내용은 모델 개선에 쓰일 수 있습니다 | [문서](https://opencode.ai/docs) |

## 계속 무료로 쓰는 API (12)

| 서비스 | 무료 조건 | 입력 학습 | Base URL | 키 | 문서 |
|---|---|---|---|---|---|
| **Google Gemini API** | Flash와 Flash-Lite는 무료입니다. 요청 수 제한이 있습니다 | 무료 등급은 학습에 쓰일 수 있음 | `https://generativelanguage.googleapis.com/v1beta/openai` | [키 만들기](https://aistudio.google.com/apikey) | [문서](https://ai.google.dev/gemini-api/docs/openai) |
| **Groq** | 무료로 분당 30회, 하루 1,000회쯤 씁니다. 모델마다 다릅니다 | 확인 못 함 | `https://api.groq.com/openai/v1` | [키 만들기](https://console.groq.com/keys) | [문서](https://console.groq.com/docs/openai) |
| **OpenRouter** | :free 모델은 분당 20회, 하루 50회. 10달러 이상 충전하면 하루 1,000회 | 확인 못 함 | `https://openrouter.ai/api/v1` | [키 만들기](https://openrouter.ai/settings/keys) | [문서](https://openrouter.ai/docs/api/reference/limits) |
| **NVIDIA NIM** | 개발과 테스트용으로 분당 40회쯤 무료 | 확인 못 함 | `https://integrate.api.nvidia.com/v1` | [키 만들기](https://build.nvidia.com/settings/api-keys) | [문서](https://build.nvidia.com/) |
| **Mistral** | 무료 플랜에 매달 크레딧이 들어 있습니다 | 무료 등급은 학습에 쓰일 수 있음 | `https://api.mistral.ai/v1` | [키 만들기](https://console.mistral.ai/api-keys) | [문서](https://docs.mistral.ai/api/) |
| **Hugging Face** | Free는 매달 0.10달러, PRO는 2달러 크레딧 | 확인 못 함 | `https://router.huggingface.co/v1` | [키 만들기](https://huggingface.co/settings/tokens/new?ownUserPermissions=inference.serverless.write&tokenType=fineGrained) | [문서](https://huggingface.co/docs/inference-providers/index) |
| **SambaNova** | 무료로 분당 20회, 하루 20회까지 | 확인 못 함 | `https://api.sambanova.ai/v1` | [키 만들기](https://cloud.sambanova.ai/apis) | [문서](https://docs.sambanova.ai/docs/en/get-started/api-keys-urls) |
| **Z.ai GLM** | 일부 Flash 모델은 무료 | 확인 못 함 | `https://api.z.ai/api/paas/v4` | [키 만들기](https://z.ai/manage-apikey/apikey-list) | [문서](https://docs.z.ai/guides/develop/http/introduction) |
| **Cohere** | Trial 키는 한 달 1,000회, 분당 20회까지 | 확인 못 함 | `https://api.cohere.ai/compatibility/v1` | [키 만들기](https://dashboard.cohere.com/api-keys) | [문서](https://docs.cohere.com/docs/compatibility-api) |
| **Ollama Cloud** | 무료 플랜에 시작 크레딧이 있습니다. 일부 모델만, 한 번에 요청 하나씩 씁니다 | 확인 못 함 | `https://ollama.com/v1` | [키 만들기](https://ollama.com/settings/keys) | [문서](https://docs.ollama.com/api/openai-compatibility) |
| **Vercel AI Gateway** | 팀마다 매달 5달러 크레딧. 한 번 결제하면 끝납니다 | 확인 못 함 | `https://ai-gateway.vercel.sh/v1` | [키 만들기](https://vercel.com/d?to=%2F%5Bteam%5D%2F%7E%2Fai-gateway%2Fapi-keys&title=AI+Gateway+API+Keys) | [문서](https://vercel.com/docs/ai-gateway/sdks-and-apis/openai-chat-completions) |
| **FreeLLMAPI** | 중계기는 무료입니다. 한도는 등록한 제공사마다 다릅니다 | 무료 등급은 학습에 쓰일 수 있음 | `http://127.0.0.1:3001/v1` |  | [문서](https://github.com/tashfeenahmed/freellmapi) |

## 가입하면 크레딧을 주는 API (6)

| 서비스 | 무료 조건 | 입력 학습 | Base URL | 키 | 문서 |
|---|---|---|---|---|---|
| **Cerebras** | 결제수단을 등록하면 5달러 크레딧을 30일 동안 줍니다. 상시 무료 등급은 없습니다 | 확인 못 함 | `https://api.cerebras.ai/v1` | [키 만들기](https://cloud.cerebras.ai/platform) | [문서](https://inference-docs.cerebras.ai/resources/openai) |
| **Fireworks** | 가입하면 1달러 크레딧을 줍니다 | 확인 못 함 | `https://api.fireworks.ai/inference/v1` | [키 만들기](https://app.fireworks.ai/settings/users/api-keys) | [문서](https://docs.fireworks.ai/tools-sdks/openai-compatibility) |
| **Nebius** | 가입하고 카드를 등록하면 1달러 크레딧을 30일 동안 줍니다 | 확인 못 함 | `https://api.tokenfactory.nebius.com/v1` | [키 만들기](https://tokenfactory.nebius.com/project/api-keys) | [문서](https://docs.tokenfactory.nebius.com/) |
| **Novita** | 가입하면 크레딧을 줍니다 | 확인 못 함 | `https://api.novita.ai/openai` | [키 만들기](https://novita.ai/settings/key-management) | [문서](https://docs.novita.ai/guides/llm-api) |
| **Upstage Solar** | 새로 가입하면 크레딧을 줍니다 | 확인 못 함 | `https://api.upstage.ai/v1` | [키 만들기](https://console.upstage.ai/api-keys) | [문서](https://console.upstage.ai/docs) |
| **Alibaba Qwen (Model Studio)** | 새로 가입하면 토큰을 줍니다 | 확인 못 함 | `https://dashscope-intl.aliyuncs.com/compatible-mode/v1` | [키 만들기](https://modelstudio.console.alibabacloud.com/ap-southeast-1/settings/api-key) | [문서](https://www.alibabacloud.com/help/en/model-studio/) |

## 내 PC 모델, 사용량 없음 (8)

내 PC 모델은 프로그램을 설치하고 모델을 받은 뒤, 아래 주소를 OpenAI 호환 주소로 씁니다. 키가 필요 없습니다.

| 프로그램 | 조건 | 기본 주소 | 문서 |
|---|---|---|---|
| **Ollama** | 무료, 내 PC에서 실행 | `http://127.0.0.1:11434/v1` | [문서](https://docs.ollama.com/api/openai-compatibility) |
| **LM Studio** | 무료, 내 PC에서 실행 | `http://127.0.0.1:1234/v1` | [문서](https://lmstudio.ai/docs/developer/api-changelog) |
| **llama.cpp** | 무료, 내 PC에서 실행 | `http://127.0.0.1:8080/v1` | [문서](https://github.com/ggml-org/llama.cpp/blob/master/tools/server/README.md) |
| **Jan** | 무료, 내 PC에서 실행 | `http://127.0.0.1:1337/v1` | [문서](https://www.jan.ai/docs/desktop/api-preference) |
| **Foundry Local** | 무료, 내 PC에서 실행 | `http://127.0.0.1:5272/v1` | [문서](https://learn.microsoft.com/en-us/azure/foundry-local/reference/reference-cli) |
| **Docker Model Runner** | 무료, 내 PC에서 실행 | `http://127.0.0.1:12434/engines/v1` | [문서](https://docs.docker.com/ai/model-runner/api-reference/) |
| **vLLM** | 무료, 직접 띄운 서버 | `http://127.0.0.1:8000/v1` | [문서](https://docs.vllm.ai/en/latest/serving/online_serving/) |
| **SGLang** | 무료, 직접 띄운 서버 | `http://127.0.0.1:30000/v1` | [문서](https://docs.sglang.ai/) |

## 여럿을 한 팀으로 쓰기
이 목록의 AI를 여럿 연결해 두면, [MoaEditor](../../README.md)가 총괄, 팀장, 직원, 인턴으로 팀을 짜서 일을 나눠 맡깁니다. 한 곳이 한도에 닿으면 다음 AI가 이어서 합니다. [무료 AI 한 번에 연결]을 누르면 Copilot, Cursor, Groq, OpenRouter, 내 PC 모델을 차례로 연결합니다. Windows용이고 무료로 쓸 수 있습니다.

## 고칠 곳이 있으면
조건이 바뀌었거나 빠진 곳이 있으면 [이슈](https://github.com/moaeditor/moaeditor/issues/new/choose)로 알려 주세요. 공식 문서 주소를 함께 적어 주시면 확인한 뒤 고칩니다. 자세한 방법은 [CONTRIBUTING.md](CONTRIBUTING.md)에 있습니다.

이 목록의 글과 data.json은 [CC BY 4.0](LICENSE)으로 자유롭게 쓸 수 있습니다. 서비스 이름은 각 회사의 상표입니다.
