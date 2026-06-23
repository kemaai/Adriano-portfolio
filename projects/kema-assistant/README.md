# 🤖 KEMA — Assistente Inteligente Autônomo

**Stack:** Hermes Agent · OmniRoute · LLMs · Python · Docker · Redis · Chromium

---

## Sobre

Assistente pessoal autônomo que opera 24/7 via Telegram com capacidades multiplas de IA. Desenvolvido sobre o Hermes Agent (Nous Research), integrado ao ecossistema OmniRoute AI Gateway.

## Capacidades

| Capacidade | Tecnologia |
|---|---|
| 💬 Chat com LLMs | DeepSeek, Claude, Gemini, Groq (2927+ modelos via OmniRoute) |
| 🎨 Geração de imagens | Flux via pollinations |
| 🌐 Navegação web | Chrome 149 headless + Playwright |
| 👁️ Análise de imagens | Modelos com visão integrada |
| 🎙️ Síntese de voz (TTS) | Edge TTS — pt-BR-AntonioNeural |
| 👂 Transcrição de áudio (STT) | Groq Whisper Large V3 |
| 🔍 Busca web | DuckDuckGo (ddgs) |
| ⏰ Tarefas agendadas | Cron jobs no Hermes |

## Infraestrutura

```
omniroute         diegosouzapw/omniroute:latest-web   20128-20129 (AI Gateway)
omniroute-redis   redis:7-alpine                      6379 (Cache / Rate Limiter)
```

- **OmniRoute v3.8.32+** — 2927+ modelos, profile web com Chromium
- **CLIProxyAPI** — Importação OAuth (Codex, Gemini, Claude)
- **Redis** — Cache de sessão, rate limiting

---

> *Projeto pessoal — base da operação diária da KEMA*
