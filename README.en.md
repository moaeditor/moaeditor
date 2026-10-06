<p align="center"><img src="assets/icon.png" width="96" alt="MoaEditor"></p>

<h1 align="center">MoaEditor</h1>

<p align="center"><b>All your AIs, one team.</b><br>A code editor that organizes your AIs into a director, team leads, staff and interns and splits the work between them</p>

<p align="center">
  <a href="https://moaeditor.dev/en/"><b>Website</b></a> ·
  <a href="https://moaeditor.dev/en/download/"><b>Download</b></a> ·
  <a href="docs/free-ai/README.en.md"><b>30 free AIs</b></a> ·
  <a href="https://github.com/moaeditor/moaeditor/issues/new/choose"><b>Bugs and ideas</b></a>
</p>

<p align="center"><sub>Windows 10 and 11 · Latest 0.1.9</sub> · <a href="README.md">한국어</a></p>

![MoaEditor: the AI team on the left, code the AI changed in the middle, and the team lead’s and director’s reports in Home on the right](https://moaeditor.dev/shots/hero.webp)

## Contents

- [Organize AIs like a company](#organize-ais-like-a-company)
- [Describe the project and AI builds the team](#describe-the-project-and-ai-builds-the-team)
- [Direct and approve](#direct-and-approve)
- [Work keeps going at the limit](#work-keeps-going-at-the-limit)
- [Save quota](#save-quota)
- [A helper AI double-checks](#a-helper-ai-double-checks)
- [Connect every AI you have](#connect-every-ai-you-have)
- [No subscription? Free AIs](#no-subscription-free-ais)
- [Companies, schools and public sector](#companies-schools-and-public-sector)
- [Install](#install)

## Organize AIs like a company

![A team drafted by AI: Claude Opus as director, Codex as team lead, Claude Sonnet and Cursor as staff, a local model as intern](assets/team-en.png)

- The **director** plans and reviews, **team leads** split the work, **staff** build it, and **interns** handle simple jobs on a local model.
- Set names, teams, ranks and roles. Talk to a whole team in its room or to one person in a 1:1.
- Blocked work goes up in order: a hint, another AI, the manager doing it directly, then one level up.

## Describe the project and AI builds the team

- Write one line in “What are you building?” and the best AI you’ve connected seats the right model in each role.
- It also writes project guide files like AGENTS.md, CLAUDE.md and .gitignore.
- Edit anything right in the table.

## Direct and approve

![Your task, the director’s plan with Approve and Run, and the report with changed files and time taken](assets/flow-en.png)

- Write a task in Home and the director shows a plan. Hand it all off with **Approve and Run** or check each step with **Approve Each Step**.
- Pick how much it asks: Plan only, Ask for everything, Ask only for important things, or Auto.
- When it’s done you get the changed files and time taken. Review the diff, roll back a single file or the whole run, or commit as is.

## Work keeps going at the limit

- When an AI runs out of quota or gets stuck, another connected AI picks up and you get a one-line note in Home.
- The director picks who takes over by looking at how often each model succeeded and how long it took over the last 7 days.
- You get a heads-up at about 80% usage.
- What to do when Claude Code hits its limit is in [this guide](https://moaeditor.dev/en/guides/claude-code-limit/).

## Save quota

**Spend up to 85% less on expensive models.**

- Expensive AIs only plan and review; cheaper models or free APIs do the bulk of the coding and local models handle simple jobs.
- Small calls like who takes a task or whether a reported fix was really made are handled by the helper AI, so they use none of the expensive model’s quota.
- Set a seat to “Auto” and it picks a cheaper model that can still do the job.
- Set thinking level per person, or leave it on auto to go higher for hard work and lower for simple work.

<sub>The 85% is a worked example: planning and review taken as 15% of the work, coding on free APIs and simple jobs on a local model, compared with doing everything on Claude Opus 5.5 at [Anthropic’s official prices](https://platform.claude.com/docs/en/about-claude/pricing) as of October 6, 2026. Actual savings depend on the task and the AIs you connect, and total tokens can go up because several AIs work together. In the [RouteLLM](https://github.com/lm-sys/RouteLLM) study of a similar approach, sending easier questions to a cheaper model cut costs by up to 85% while keeping 95% of GPT-4’s performance on MT Bench.</sub>

## A helper AI double-checks

- It catches reports that claim a fix that wasn’t made, and commands that look dangerous.
- With an NVIDIA GPU with 8 GB or more, it runs on your PC and sends nothing out. Otherwise use the one MoaEditor provides (2,000 checks a day when signed in) or your own Cloudflare token. You can turn it off.

## Connect every AI you have

![Subscriptions, free APIs and local models connecting into MoaEditor](assets/connect-en.png)

- **13 subscription tools:** Claude Code, Codex, GitHub Copilot, Cursor, Gemini CLI, OpenCode, Kimi Code, Qwen Code, goose, Augment, Mistral Vibe, Factory Droid, Cline. Each signs in through the vendor’s official program; MoaEditor never reads their login files.
- **API keys:** AI labs like OpenAI, Anthropic and Google Gemini, inference services like Groq and OpenRouter, company clouds and Korean models. Keys stay in this PC’s secure storage.
- **Local models:** Ollama, LM Studio, llama.cpp, Jan, Foundry Local, Docker Model Runner, vLLM, SGLang. No internet, no quota.
- **Connect all:** installs, signs in and actually checks this PC’s AIs one after another.

## No subscription? Free AIs

![Connect free AIs and the 30 free options](assets/free-en.png)

**Connect free AIs** sets up GitHub Copilot’s and Cursor’s free plans, free Groq and OpenRouter keys, and a local model that fits your PC. All 30 free options are in the [free AI list](docs/free-ai/README.en.md). Free tiers are used with your own account within each provider’s limits and terms.

## Companies, schools and public sector

- **Company plan subscriptions:** connect Claude, ChatGPT (Codex), Copilot and Gemini Team, Business and Enterprise accounts through their official CLIs.
- **Company cloud APIs and in-house GPU servers:** with an in-house server, code never leaves your network.
- **Offline networks:** one signed license file turns on business features. No sign-in; only in-house GPU servers and local models.
- **Classrooms:** students see how AI splits work, reviews it and escalates when stuck.
- Contact: [Business, schools and public sector](https://moaeditor.dev/en/enterprise/), admin@moaeditor.dev

## Install

1. Get the installer from the [download page](https://moaeditor.dev/en/download/). It installs into your user folder without admin rights.
2. The installer isn’t code-signed yet, so Microsoft Defender SmartScreen may warn you. Click **More info**, then **Run anyway**. Signing is in progress. There’s a picture guide on the [download page](https://moaeditor.dev/en/download/).
3. To check the file, compare its hash in PowerShell:

```powershell
Get-FileHash .\MoaEditorUserSetup-x64-0.1.9.exe -Algorithm SHA256
```

| Version | File | SHA-256 |
|---|---|---|
| 0.1.9 | MoaEditorUserSetup-x64-0.1.9.exe | `4360b59c529e298a7446818554790adec1eba5812a16bc2077a94b1a6a651796` |

The interface follows the editor’s display language (Korean or English). Free for individuals, students, schools, nonprofits and companies with fewer than 50 employees.

## Privacy and keys

- API keys live in your OS secure storage. Code and instructions go straight from your PC to the AI vendor you chose, never through MoaEditor’s servers.
- Details: [Privacy Policy](https://moaeditor.dev/en/legal/privacy/), [Terms](https://moaeditor.dev/en/legal/terms/)

## Bugs and ideas

Open an [issue](https://github.com/moaeditor/moaeditor/issues/new/choose). Report security problems to admin@moaeditor.dev instead of a public issue.

## About this repository

This repository holds MoaEditor’s overview, release notes, and bug reports and ideas. The app’s source code isn’t published here. MoaEditor is built on Code - OSS (MIT), the open-source base of Microsoft Visual Studio Code, and isn’t affiliated with Microsoft.

© 2026 Horizon Co., Ltd.
