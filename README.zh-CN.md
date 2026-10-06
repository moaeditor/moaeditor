<p align="center"><img src="assets/icon.png" width="96" alt="MoaEditor"></p>

<h1 align="center">MoaEditor</h1>

<p align="center">把多个 AI 编成总负责人、组长、员工和实习生，分工完成任务的代码编辑器</p>

<p align="center">
  <a href="https://moaeditor.dev/en/">官网</a> ·
  <a href="https://moaeditor.dev/en/download/">下载</a> ·
  <a href="docs/free-ai/README.zh-CN.md">30 个免费 AI</a> ·
  <a href="https://github.com/moaeditor/moaeditor/issues/new/choose">问题与建议</a>
</p>

<p align="center"><a href="README.md">English</a> · <a href="README.ko.md">한국어</a> · <b>简体中文</b></p>

![MoaEditor：左边是 AI 团队，中间是代码，右边是主页](https://moaeditor.dev/shots/hero.webp)

## 功能

### AI 组织架构

![Claude Opus 当总负责人，Codex 当组长，Claude Sonnet 和 Cursor 当员工，本地模型当实习生](assets/team-en.png)

- 总负责人做计划和审查，组长拆分任务，员工写代码，实习生用本地模型做简单的活。
- 名字、团队、职级和角色在表格里修改。
- 卡住的任务依次交给：提示、另一个 AI、上级、再上一级。
- 用一句话写下要做什么，AI 会给每个位置选模型，并生成 AGENTS.md、CLAUDE.md 和 .gitignore。

### 任务与审批

![任务、总负责人的计划和汇报](assets/flow-en.png)

- 在主页写下任务，总负责人先给出计划。Approve and Run 一次交出去，Approve Each Step 逐步确认。
- 询问方式：只做计划、全部询问、只问重要的、自动。
- 完成后显示修改的文件和耗时。可以按文件撤销、整体回到运行前，或直接提交。

### 额度与用量

- 某个 AI 用到上限或卡住时，由另一个已连接的 AI 接手，根据各模型最近 7 天的记录来选。
- 用量到 80% 左右会提醒。
- 昂贵的模型只做计划和审查，编码交给更便宜的模型或免费 API，简单的活交给本地模型。按我们的计算，昂贵模型的花费最多可减少 85%。<sup>1</sup>
- 模型和思考强度可以按位置设置，也可以设为自动。

### 辅助 AI

- 另有一个小模型检查“没改却说改好了”的汇报、危险命令，以及任务交给谁这类小判断。
- 有 8GB 以上显存的 NVIDIA 显卡时在本机运行；没有的话用 MoaEditor 提供的（登录后每天 2,000 次）或你自己的 Cloudflare 令牌。可以关闭。

### 连接

![订阅、免费 API 和本地模型](assets/connect-en.png)

- 13 个订阅工具：Claude Code、Codex、GitHub Copilot、Cursor、Gemini CLI、OpenCode、Kimi Code、Qwen Code、goose、Augment、Mistral Vibe、Factory Droid、Cline
- API 密钥：OpenAI、Anthropic、Google Gemini、Groq、OpenRouter、DeepSeek、Moonshot（Kimi）、Z.ai（GLM）、阿里云 Qwen（Model Studio）、MiniMax 等。国内服务内置的是国际版接口（如 api.moonshot.ai、api.z.ai）。
- 本地模型：Ollama、LM Studio、llama.cpp、Jan、Foundry Local、Docker Model Runner、vLLM、SGLang
- Connect all 会依次安装、登录并检查这台电脑上的 AI。

### 免费 AI

![一键连接免费 AI 和 30 个免费选项](assets/free-en.png)

- Connect free AIs 会连接 Copilot 和 Cursor 的免费计划、Groq 和 OpenRouter 的免费密钥，以及本地模型。
- 全部 30 个免费选项见 [列表](docs/free-ai/README.zh-CN.md)。

### 企业、学校与公共机构

- 可连接企业版订阅（Team、Business、Enterprise）、企业云 API 和内部 GPU 服务器。
- 内网环境用许可证文件代替登录。
- 联系：[企业、学校与公共机构](https://moaeditor.dev/en/enterprise/)，admin@moaeditor.dev

## 安装

从 [下载页面](https://moaeditor.dev/en/download/) 下载。支持 Windows 10 和 11。应用界面目前只有英语和韩语。

安装程序还没有代码签名，Windows 可能会提示警告。

## 价格

个人、学生、学校、非营利机构以及员工少于 50 人的公司免费使用。所连接 AI 的费用照常付给各服务商。[价格](https://moaeditor.dev/en/pricing/)

## 隐私

API 密钥保存在本机的安全存储里，代码和指令直接发送到你选择的 AI 服务商。[隐私政策](https://moaeditor.dev/en/legal/privacy/)、[使用条款](https://moaeditor.dev/en/legal/terms/)

## 问题与建议

请提交 [issue](https://github.com/moaeditor/moaeditor/issues/new/choose)。安全问题请发邮件到 admin@moaeditor.dev。

## 关于这个仓库

这里放介绍和 issue，没有源代码。MoaEditor 基于 Code - OSS（MIT）开发，与 Microsoft 没有关联。

---

<sub>1. 假设计划和审查占全部工作的 15%，与全部用 Claude Opus 5.5 完成相比，按 [Anthropic 官方价格](https://platform.claude.com/docs/en/about-claude/pricing)（2026-10-06）计算。实际效果因任务而异，多个 AI 协作时总 token 数可能增加。研究类似做法的 [RouteLLM](https://github.com/lm-sys/RouteLLM) 在 MT Bench 上保持 GPT-4 95% 性能的同时，成本最多降低了 85%。</sub>

© 2026 Horizon Co., Ltd.
