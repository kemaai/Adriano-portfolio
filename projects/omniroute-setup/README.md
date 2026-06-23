# ⚙️ OmniRoute — AI Gateway: Auditoria & Configuração

**Stack:** Docker · Redis · Chromium · Node.js · CLIProxyAPI

---

## Sobre

Auditoria completa e configuração do OmniRoute AI Gateway — um proxy/roteador de requisições LLM que expõe uma API compatível com OpenAI, suportando 2927+ modelos de 52+ provedores.

## O que foi feito

### Antes (instalação original)
- ❌ Sem Redis (requerido pela documentação)
- ❌ Sem `env_file` (.env com secrets)
- ❌ Container sem Chromium (web-cookie providers)
- ❌ Sem healthcheck
- ❌ Backups acumulados (~680MB)
- ❌ CLIProxyAPI binary com bug de flag (`-c` em vez de `-config`)

### Depois
- ✅ Redis 7 Alpine com healthcheck
- ✅ `.env` com `WS_BRIDGE_SECRET` criptográfico
- ✅ Imagem `latest-web` com Chromium 1228 + Playwright 1.61
- ✅ Compose com healthcheck, stop_grace_period, profiles
- ✅ Backup cleaning (5 mais recentes, ~170MB)
- ✅ CLIProxyAPI v7.2.28 corrigido no host + volume compartilhado

### Entregáveis
| Item | Resultado |
|---|---|
| Containers saudáveis | `omniroute` + `omniroute-redis` |
| Endpoint API | HTTP 200 em `/v1/models` |
| Models disponíveis | 2927+ |
| Chromium headless | ✅ Instalado |
| OAuth import | ✅ Endpoint `/api/oauth/cliproxy-import` pronto |
| Decryption errors | ✅ Investigado — warning inofensivo |

## Habilidades Técnicas Demonstradas

- Docker Compose com multi-profile e volumes
- Redis configuration e healthcheck
- Troubleshooting de Node.js apps (bug de flag, encryption key mismatch)
- CI/CD com ghcr.io e GitHub Container Registry
- Scripting Python para auditoria e correção
- Leitura e implementação de documentação técnica

---

> *Auditoria completa contra documentação oficial — estado limpo, sem gambiarras*
