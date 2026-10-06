<p align="center"><img src="assets/icon.png" width="96" alt="MoaEditor"></p>

<h1 align="center">MoaEditor</h1>

<p align="center"><b>가진 AI 전부, 한 팀으로.</b><br>여러 AI를 총괄, 팀장, 직원, 인턴으로 조직해 일을 나눠 맡기는 코드 에디터</p>

<p align="center">
  <a href="https://moaeditor.dev"><b>홈페이지</b></a> ·
  <a href="https://moaeditor.dev/download/"><b>다운로드</b></a> ·
  <a href="docs/free-ai/README.md"><b>무료 AI 30곳</b></a> ·
  <a href="https://github.com/moaeditor/moaeditor/issues/new/choose"><b>버그와 의견</b></a>
</p>

<p align="center"><sub>Windows 10, 11 · 최신 버전 0.1.9</sub> · <a href="README.en.md">English</a></p>

![모아에디터 화면: 왼쪽 AI 조직, 가운데 AI가 고친 코드, 오른쪽 홈에 팀장과 총괄의 보고](https://moaeditor.dev/shots/hero.webp)

## 목차

- [AI를 회사처럼 조직합니다](#ai를-회사처럼-조직합니다)
- [무엇을 만들지 적으면 AI가 팀을 짭니다](#무엇을-만들지-적으면-ai가-팀을-짭니다)
- [지시하고 결재합니다](#지시하고-결재합니다)
- [한도가 차도 일이 멈추지 않습니다](#한도가-차도-일이-멈추지-않습니다)
- [사용량을 아낍니다](#사용량을-아낍니다)
- [보조 AI가 한 번 더 살핍니다](#보조-ai가-한-번-더-살핍니다)
- [가진 AI는 다 연결합니다](#가진-ai는-다-연결합니다)
- [구독이 없어도 무료 AI로](#구독이-없어도-무료-ai로)
- [회사, 학교, 공공기관](#회사-학교-공공기관)
- [설치](#설치)

## AI를 회사처럼 조직합니다

![AI가 짠 팀: 총괄 Claude Opus, 팀장 Codex, 직원 Claude Sonnet과 Cursor, 인턴 내 PC 모델](assets/team.png)

- **총괄**이 계획을 세우고 결과를 검토합니다. **팀장**이 일을 나누고, **직원**이 구현하고, **인턴**은 내 PC 모델로 간단한 일을 맡습니다.
- 사람 이름, 팀, 직급, 역할을 정할 수 있습니다. 팀방과 1:1 대화로 팀이나 한 사람에게만 따로 말할 수도 있습니다.
- 막힌 일은 힌트, 다른 AI, 상급자가 직접, 한 단계 위 순서로 올라갑니다.

## 무엇을 만들지 적으면 AI가 팀을 짭니다

- "무엇을 만들 건가요?"에 한 줄만 적으면, 연결한 AI 가운데 가장 잘하는 AI가 자리마다 맞는 AI를 앉힙니다.
- AGENTS.md, CLAUDE.md, .gitignore 같은 프로젝트 안내 파일도 함께 만들어 둡니다.
- 마음에 들지 않는 칸은 표에서 바로 고치면 됩니다.

## 지시하고 결재합니다

![내 지시, 총괄의 계획과 승인하고 실행 단추, 바뀐 파일과 걸린 시간 보고](assets/flow.png)

- 홈에 할 일을 적으면 총괄이 계획을 보여 줍니다. <b>[승인하고 실행]</b>으로 한 번에 맡기거나 <b>[단계마다 결재]</b>로 하나씩 확인합니다.
- 허가 방식을 고릅니다: 계획만, 모두 물어보기, 중요한 것만 물어보기, 자동.
- 끝나면 바뀐 파일과 걸린 시간을 보고합니다. 바뀐 코드를 검토하고, 파일마다 되돌리거나 실행 전으로 통째로 되돌리고, 그대로 커밋할 수 있습니다.

## 한도가 차도 일이 멈추지 않습니다

- 한 AI의 사용량이 다 차거나 막히면 연결해 둔 다른 AI가 이어서 하고, 홈에 한 줄로 알립니다.
- 누가 이어받을지는 총괄이 모델마다 최근 7일 동안 얼마나 성공했고 얼마나 걸렸는지 보고 고릅니다.
- 사용량이 80%쯤 되면 미리 알립니다.

## 사용량을 아낍니다

**비싼 모델에 드는 비용을 최대 85%까지 줄입니다.**

- 비싼 AI는 계획과 검토에만 쓰고, 양이 많은 구현은 더 싼 모델이나 무료 API가, 단순한 일은 내 PC 모델이 맡습니다.
- 누구에게 맡길지 고르기, 고쳤다는 보고가 맞는지 확인하기 같은 작은 판단은 보조 AI가 해서 비싼 모델 사용량을 쓰지 않습니다.
- 자리마다 "자동"으로 두면 일을 해낼 수 있는 모델 가운데 싼 쪽을 고릅니다.
- 생각 수준도 사람마다 정하거나 자동으로 두면, 어려운 일은 높게, 간단한 일은 낮게 맞춥니다.

<sub>85%는 계산 예시입니다. 계획과 검토가 전체 일의 15%라고 보고, 구현은 무료 API, 단순한 일은 내 PC 모델이 맡는 경우를 모든 일을 Claude Opus 5.5 하나로 할 때와 [Anthropic 공식 요금](https://platform.claude.com/docs/en/about-claude/pricing)(2026년 10월 6일 기준)으로 비교했습니다. 실제 절감 폭은 작업과 연결한 AI에 따라 다르고, 여러 AI가 함께 일하는 만큼 전체 토큰 수는 늘 수 있습니다. 비슷한 방식을 다룬 [RouteLLM](https://github.com/lm-sys/RouteLLM) 연구에서는 쉬운 질문을 싼 모델로 보내 MT Bench에서 GPT-4 성능의 95%를 유지하면서 비용을 최대 85% 줄였습니다.</sub>

## 보조 AI가 한 번 더 살핍니다

- "고치지 않고 고쳤다"는 보고와 위험해 보이는 명령을 한 번 더 걸러 냅니다.
- 메모리 8GB 이상인 NVIDIA 그래픽카드가 있으면 이 PC에서 돌려 아무것도 밖으로 보내지 않습니다. 없으면 모아에디터가 제공하는 보조 AI(로그인하면 하루 2,000회)나 내 Cloudflare 토큰으로 씁니다. 끌 수도 있습니다.

## 가진 AI는 다 연결합니다

![구독, 무료 API, 내 PC 모델이 모아에디터 하나로 연결되는 그림](assets/connect.png)

- **구독 도구 13가지:** Claude Code, Codex, GitHub Copilot, Cursor, Gemini CLI, OpenCode, Kimi Code, Qwen Code, goose, Augment, Mistral Vibe, Factory Droid, Cline. 각 회사의 공식 프로그램으로 로그인하고, 로그인 정보 파일은 읽지 않습니다.
- **API 키:** OpenAI, Anthropic, Google Gemini 같은 AI 회사부터 Groq, OpenRouter 같은 추론 서비스, 회사 클라우드와 국내 모델까지. 키는 이 PC의 보안 저장소에만 둡니다.
- **내 PC 모델:** Ollama, LM Studio, llama.cpp, Jan, Foundry Local, Docker Model Runner, vLLM, SGLang. 인터넷도 사용량도 쓰지 않습니다.
- **[한 번에 연결]:** 설치, 로그인, 실제 확인까지 이 PC의 AI를 차례로 연결합니다.

## 구독이 없어도 무료 AI로

![무료 AI 한 번에 연결과 무료 AI 30곳](assets/free.png)

<b>[무료 AI 한 번에 연결]</b>을 누르면 GitHub Copilot과 Cursor의 무료 요금제, Groq와 OpenRouter의 무료 키, 이 PC에 맞는 내 PC 모델을 차례로 연결합니다. 그 밖에 무료로 쓸 수 있는 곳까지 모두 30곳을 [무료 AI 목록](docs/free-ai/README.md)에 정리해 두었습니다. 무료 등급은 각 회사가 정한 한도와 조건 안에서 내 계정으로 씁니다.

## 회사, 학교, 공공기관

- **회사 요금제 구독:** Claude, ChatGPT(Codex), Copilot, Gemini의 Team, Business, Enterprise 계정을 공식 CLI로 연결합니다.
- **회사 클라우드 API와 사내 GPU 서버:** 사내 서버를 연결하면 코드가 회사 망 밖으로 나가지 않습니다.
- **폐쇄망과 망분리:** 서명된 라이선스 파일 하나로 기업 권한을 켭니다. 로그인 없이 사내 GPU 서버와 PC의 로컬 모델만 씁니다.
- **교실:** AI가 일을 나누고, 검토하고, 막히면 위로 올리는 과정을 학생이 그대로 봅니다.
- 문의: [기업·학교·공공 안내](https://moaeditor.dev/enterprise/), admin@moaeditor.dev

## 설치

1. [다운로드 페이지](https://moaeditor.dev/download/)에서 설치 파일을 받습니다. 관리자 권한 없이 내 사용자 폴더에 설치됩니다.
2. 아직 코드 서명을 적용하기 전이라 Microsoft Defender SmartScreen이 경고를 띄울 수 있습니다. <b>[추가 정보]</b>를 누른 뒤 <b>[실행]</b>을 누르면 설치가 계속됩니다. 서명은 준비 중입니다.
3. 받은 파일이 맞는지 확인하려면 PowerShell에서 아래 값과 비교하세요.

```powershell
Get-FileHash .\MoaEditorUserSetup-x64-0.1.9.exe -Algorithm SHA256
```

| 버전 | 파일 | SHA-256 |
|---|---|---|
| 0.1.9 | MoaEditorUserSetup-x64-0.1.9.exe | `4360b59c529e298a7446818554790adec1eba5812a16bc2077a94b1a6a651796` |

화면은 에디터의 표시 언어를 따라 한국어나 영어로 나옵니다. 개인, 학생, 교육 기관과 비영리 기관, 직원 50명 미만 회사는 무료로 쓸 수 있습니다.

## 개인정보와 키

- API 키는 운영체제 보안 저장소에 두고, 코드와 지시는 내 PC에서 고른 AI 회사로 바로 갑니다. 모아에디터 서버를 거치지 않습니다.
- 자세한 내용: [개인정보 처리방침](https://moaeditor.dev/legal/privacy/), [이용약관](https://moaeditor.dev/legal/terms/)

## 버그와 의견

[이슈](https://github.com/moaeditor/moaeditor/issues/new/choose)에 남겨 주세요. 보안 문제는 공개 이슈 대신 admin@moaeditor.dev로 알려 주세요.

## 이 저장소에 대해

이 저장소는 모아에디터의 소개, 버전 기록, 버그와 의견을 받는 곳입니다. 앱의 소스 코드는 여기에 올리지 않습니다. 모아에디터는 Microsoft Visual Studio Code의 오픈소스 버전(Code - OSS, MIT 라이선스)을 바탕으로 만들었으며, Microsoft와 관련이 없습니다.

© 2026 주식회사 호라이즌 (Horizon Co., Ltd.)
