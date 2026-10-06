<p align="center"><img src="assets/icon.png" width="96" alt="MoaEditor"></p>

<h1 align="center">MoaEditor</h1>

<p align="center"><b>你所有的 AI，组成一个团队。</b><br>把多个 AI 编成总负责人、组长、员工和实习生，分工完成任务的代码编辑器</p>

<p align="center">
  <a href="https://moaeditor.dev/en/"><b>官网</b></a> ·
  <a href="https://moaeditor.dev/en/download/"><b>下载</b></a> ·
  <a href="docs/free-ai/README.zh-CN.md"><b>30 个免费 AI</b></a> ·
  <a href="https://github.com/moaeditor/moaeditor/issues/new/choose"><b>问题与建议</b></a>
</p>

<p align="center"><sub>Windows 10 和 11 · 最新版本 0.1.9 · 应用界面目前只有英语和韩语</sub></p>

<p align="center"><a href="README.md">English</a> · <a href="README.ko.md">한국어</a> · <b>简体中文</b></p>

![MoaEditor：左边是 AI 团队，中间是 AI 修改的代码，右边的主页里是组长和总负责人的汇报](https://moaeditor.dev/shots/hero.webp)

## 目录

- [像公司一样组织 AI](#像公司一样组织-ai)
- [写下需求 AI 自动组队](#写下需求-ai-自动组队)
- [下达任务并审批](#下达任务并审批)
- [用量到上限也不停工](#用量到上限也不停工)
- [节省用量](#节省用量)
- [辅助 AI 再检查一遍](#辅助-ai-再检查一遍)
- [连接你已有的所有 AI](#连接你已有的所有-ai)
- [没有订阅也能用免费 AI](#没有订阅也能用免费-ai)
- [企业学校与公共机构](#企业学校与公共机构)
- [安装](#安装)

## 像公司一样组织 AI

![AI 组建的团队：Claude Opus 当总负责人，Codex 当组长，Claude Sonnet 和 Cursor 当员工，本地模型当实习生](assets/team-en.png)

- **总负责人**制定计划并审查结果，**组长**拆分任务，**员工**动手实现，**实习生**用本地模型处理简单的活。
- 可以设置名字、团队、职级和角色。可以在团队群里对整个团队说话，也可以和某一个人单聊。
- 卡住的任务按顺序往上走：先给提示，再换一个 AI，再由上级亲自处理，最后再往上一级。

## 写下需求 AI 自动组队

- 在“你要做什么？”里写一句话，你已连接的 AI 中最强的那个会给每个位置安排合适的模型。
- 同时生成 AGENTS.md、CLAUDE.md、.gitignore 等项目说明文件。
- 不满意的地方直接在表格里改。

## 下达任务并审批

![你的任务、总负责人的计划和 Approve and Run 按钮、以及包含修改文件和耗时的汇报](assets/flow-en.png)

- 在主页写下任务，总负责人会先给出计划。用 **Approve and Run** 一次交出去，或用 **Approve Each Step** 逐步确认。
- 可以选择询问方式：只做计划、全部询问、只问重要的、自动。
- 完成后会汇报修改了哪些文件、用了多长时间。可以审查改动，按文件撤销或整体回到运行前，也可以直接提交。

## 用量到上限也不停工

- 某个 AI 用完额度或卡住时，已连接的其他 AI 会接着做，并在主页用一行字告诉你。
- 由谁接手，由总负责人根据每个模型最近 7 天的成功率和耗时来决定。
- 用量到 80% 左右会提前提醒。

## 节省用量

**昂贵模型的花费最多可减少 85%。**

- 昂贵的 AI 只负责计划和审查，大量的编码交给更便宜的模型或免费 API，简单的活交给本地模型。
- 把任务交给谁、汇报的修改是否真的做了，这类小判断由辅助 AI 处理，不占用昂贵模型的额度。
- 把位置设成“自动”，会在能完成任务的模型中选更便宜的。
- 思考强度可以按人设置，或设为自动：难的活想得深一些，简单的活想得浅一些。

<sub>85% 是计算示例：假设计划和审查占全部工作的 15%，编码用免费 API，简单的活用本地模型，按 [Anthropic 官方价格](https://platform.claude.com/docs/en/about-claude/pricing)（2026 年 10 月 6 日）与全部用 Claude Opus 5.5 完成相比。实际节省幅度取决于任务和所连接的 AI；多个 AI 协作时，总 token 数可能反而增加。在研究类似做法的 [RouteLLM](https://github.com/lm-sys/RouteLLM) 中，把较简单的问题交给更便宜的模型，在 MT Bench 上保持 GPT-4 95% 性能的同时，成本最多降低了 85%。</sub>

## 辅助 AI 再检查一遍

- 拦下“没改却说改好了”的汇报和看起来危险的命令。
- 有 8GB 以上显存的 NVIDIA 显卡时，它在你的电脑上运行，不向外发送任何东西。没有的话，可以用 MoaEditor 提供的辅助 AI（登录后每天 2,000 次）或你自己的 Cloudflare 令牌。也可以关闭。

## 连接你已有的所有 AI

![订阅、免费 API 和本地模型连接到 MoaEditor](assets/connect-en.png)

- **13 个订阅工具：** Claude Code、Codex、GitHub Copilot、Cursor、Gemini CLI、OpenCode、Kimi Code、Qwen Code、goose、Augment、Mistral Vibe、Factory Droid、Cline。每个都通过官方程序登录，MoaEditor 不读取它们的登录文件。
- **API 密钥：** 除了 OpenAI、Anthropic、Google Gemini 和 Groq、OpenRouter 等服务，也可以连接 DeepSeek、Moonshot（Kimi）、Z.ai（GLM）、阿里云 Qwen（Model Studio）和 MiniMax。内置的是这些服务的国际版接口（如 api.moonshot.ai、api.z.ai）。密钥只保存在这台电脑的安全存储里。
- **本地模型：** Ollama、LM Studio、llama.cpp、Jan、Foundry Local、Docker Model Runner、vLLM、SGLang。不用联网，也不占额度。
- **Connect all：** 依次安装、登录并实际检查这台电脑上的 AI。

## 没有订阅也能用免费 AI

![一键连接免费 AI 和 30 个免费选项](assets/free-en.png)

**Connect free AIs** 会依次连接 GitHub Copilot 和 Cursor 的免费计划、Groq 和 OpenRouter 的免费密钥，以及适合你电脑的本地模型。全部 30 个免费选项见 [免费 AI 列表](docs/free-ai/README.zh-CN.md)。免费层在各服务商规定的额度和条件内，用你自己的账号使用。

## 企业学校与公共机构

- **企业版订阅：** 通过官方 CLI 连接 Claude、ChatGPT（Codex）、Copilot、Gemini 的 Team、Business、Enterprise 账号。
- **企业云 API 和内部 GPU 服务器：** 连接内部服务器后，代码不会离开公司网络。
- **内网与隔离网络：** 用一个签名的许可证文件开启企业功能。无需登录，只使用内部 GPU 服务器和电脑上的本地模型。
- **课堂：** 学生可以直接看到 AI 如何分工、审查，以及卡住时如何往上交。
- 联系：[企业、学校与公共机构](https://moaeditor.dev/en/enterprise/)，admin@moaeditor.dev

## 安装

从 [下载页面](https://moaeditor.dev/en/download/) 下载并运行即可。支持 Windows 10 和 11，不需要管理员权限。个人、学生、学校、非营利机构以及员工少于 50 人的公司可以免费使用。

<sub>安装程序的代码签名正在准备中，Windows 可能会提示警告。跳过警告的方法和 SHA-256 值见下载页面。</sub>

## 隐私与密钥

- API 密钥保存在操作系统的安全存储里。代码和指令从你的电脑直接发送到你选择的 AI 服务商，不经过 MoaEditor 的服务器。
- 详情：[隐私政策](https://moaeditor.dev/en/legal/privacy/)、[使用条款](https://moaeditor.dev/en/legal/terms/)

## 问题与建议

请提交 [issue](https://github.com/moaeditor/moaeditor/issues/new/choose)。安全问题请发邮件到 admin@moaeditor.dev，不要公开提交。

## 关于这个仓库

这个仓库用于 MoaEditor 的介绍、版本记录以及接收问题与建议。应用的源代码不在这里发布。MoaEditor 基于 Microsoft Visual Studio Code 的开源版本（Code - OSS，MIT 许可证）开发，与 Microsoft 没有关联。

© 2026 Horizon Co., Ltd.
