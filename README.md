# AurixCore

### One AI engine for every app you build.

By **IB Aura**.

<p align="center">
  <a href="https://github.com/IB-AURA/aurixcore-releases/releases/latest/download/aurixcore-windows-x64.zip"><img alt="Download for Windows" src="https://img.shields.io/badge/Download%20for-Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white"></a>
  <a href="https://github.com/IB-AURA/aurixcore-releases/releases/latest/download/aurixcore-macos-arm64.tar.gz"><img alt="Download for macOS (Apple silicon)" src="https://img.shields.io/badge/Download%20for-macOS%20(Apple%20silicon)-000000?style=for-the-badge&logo=apple&logoColor=white"></a>
  <a href="https://github.com/IB-AURA/aurixcore-releases/releases/latest/download/aurixcore-macos-intel.tar.gz"><img alt="Download for macOS (Intel)" src="https://img.shields.io/badge/Download%20for-macOS%20(Intel)-555555?style=for-the-badge&logo=apple&logoColor=white"></a>
  <a href="https://github.com/IB-AURA/aurixcore-releases/releases/latest/download/aurixcore-linux-x64.tar.gz"><img alt="Download for Linux" src="https://img.shields.io/badge/Download%20for-Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black"></a>
</p>

<p align="center"><sub>One click, no account needed. Phones and tablets need no download: open AurixCore in the browser and pair with the QR code.</sub></p>
---

## The story

It started with a simple problem.

We were building several AI tools at once: a coding IDE, an optimizer, an agent that works on your PC. Every one of them wanted its own API keys, its own model, its own quota, its own settings. When a free quota ran dry in the middle of work, the tool just stopped. When we switched provider, we rewired the app. When we wanted a local model, that was another project.

We kept rebuilding the same plumbing. So we stopped and asked: **what if all of it lived in one place?**

One engine that sits under every app. You enter your keys once. It picks the best model for the job. When a provider runs out, the next one takes over without you noticing. It can run models on your own machine. It can search the live web, read pages, analyse your spreadsheets and hand you finished Word, PowerPoint and Excel files. And it can touch your PC only when you say so.

That engine is AurixCore. We built it for ourselves first. Now it is yours to try.

## What you get

| | |
|---|---|
| **One place for models and keys** | Local models (llama.cpp built in) and cloud providers: Groq, Gemini, OpenRouter, NVIDIA, Mistral, SambaNova, Cohere, DeepSeek, OpenAI, Kimi, GLM. Enter a key once; it is kept in your system's secure store and never shown again. |
| **Never stuck on a quota** | A provider runs out, the next one takes over. All are out, your message is held and continues when one is back. |
| **It does the work** | Searches the live web, reads pages, analyses sales / consumption / feedback sheets with exact numbers, and builds Word, PowerPoint and Excel files you can preview and download from the chat. |
| **One API for all your apps** | OpenAI-compatible. Ask for a role (`fast`, `code`, `strong`, `vision`) instead of a model name and AurixCore routes it. |
| **Knows your machine** | Scans your RAM and graphics card and recommends local models that actually fit. |
| **PC control you can trust** | Off by default. You choose the folders. Reading is free inside them; writing files and running commands wait for your approval, and everything is logged. |
| **Phones too** | Pair with a QR code. A phone can chat; it cannot touch your files, your PC or your keys. |
| **Light** | A small program, not a heavy suite. The local model loads when needed and unloads when idle. Old PC? Run it in Docker with cloud models only. |
| **Keeps itself current** | Built-in updater: one click, checksum verified, and it rolls back on its own if a new version does not start. Only one copy stays on disk. |

## For developers: try it in two minutes

1. Download and unpack your build below.
2. Run `aurixcore` (`aurixcore.exe` on Windows), then `aurixcore link` and open the address it prints.
3. Add a free key in **Settings > API keys**.
4. Point any app at it:

```bash
curl http://127.0.0.1:7842/v1/chat/completions \
  -H "Authorization: Bearer YOUR_HUB_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"model":"fast","messages":[{"role":"user","content":"Hello"}]}'
```

Any OpenAI-style client works the same way: change the base URL and use a role as the model name. Your app never sees a provider key, and it keeps working when a provider changes or runs out.

## Download

Pick the button above or a file below. All builds are on the **[Releases page](../../releases/latest)**.

| System | Download |
|---|---|
| Windows 10 / 11 | [aurixcore-windows-x64.zip](https://github.com/IB-AURA/aurixcore-releases/releases/latest/download/aurixcore-windows-x64.zip) |
| macOS (Apple silicon) | [aurixcore-macos-arm64.tar.gz](https://github.com/IB-AURA/aurixcore-releases/releases/latest/download/aurixcore-macos-arm64.tar.gz) |
| macOS (Intel) | [aurixcore-macos-intel.tar.gz](https://github.com/IB-AURA/aurixcore-releases/releases/latest/download/aurixcore-macos-intel.tar.gz) |
| Linux (x64) | [aurixcore-linux-x64.tar.gz](https://github.com/IB-AURA/aurixcore-releases/releases/latest/download/aurixcore-linux-x64.tar.gz) |
| Docker (any system) | `ghcr.io/ib-aura/aurixcore` |

Every file has a `.sha256` next to it so you can verify it. On macOS, if the system blocks the first start, right-click the file and choose **Open** once.

## Private by design

- It listens on your own machine only, unless you turn on phone access.
- Keys live in Windows Credential Manager, macOS Keychain or the Linux Secret Service, not in config files or logs.
- Nothing is sent anywhere except to the model providers you chose and the web searches you ask for.
- The updater only accepts files from this repository and checks every download against its checksum.

## Tell us what you need, and what is wrong

We read everything.

- **[Something is wrong](../../issues/new?template=bug.yml)**: a bug or a crash. Tell us what happened.
- **[I am looking for something](../../issues/new?template=idea.yml)**: a feature, provider or model you want.
- **[Discussions](../../discussions)**: questions, comments, and what you built with it.

Inside the app, **Settings > Hub** shows your version and checks for updates.

---

*AurixCore, by IB Aura. One engine. All your apps.*
