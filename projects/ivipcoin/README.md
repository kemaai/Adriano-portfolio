# 🪙 iVipCoin — Landing Page Cripto com Dados Ao Vivo

**Stack:** React 18 · Vite · CoinGecko API · TanStack Query · Recharts · Tailwind · shadcn/ui · i18n

---

## 🎯 Sobre

Landing page premium para a criptomoeda **iVipCoin** (BSC) — site institucional com cotações **ao vivo da CoinGecko**, **calculadora de investimento** com simulação histórica, **conversor IVIP↔USD**, **gráfico de preço interativo** e **suporte bilíngue (pt-BR + EN)**.

**7.049 linhas** · **11 componentes** · **i18n pt/EN** · **Integração PancakeSwap**

> 💼 **Projeto para cliente real** — empresa de criptomoedas com token listado na Binance Smart Chain.

---

## 📋 Funcionalidades

| Funcionalidade | Descrição |
|---|---|
| **🏠 Hero** | Preço IVIP ao vivo da CoinGecko, variação 24h, market cap, volume — com atualização automática a cada 60s |
| **📊 CryptoMarquee** | Ticker infinito com preços reais de BTC, ETH, USDT, XRP, BNB |
| **💎 Features** | 6 recursos: LTE (Learn & Earn), Distribuição de Lucros, Queimas Mensais, Renda Passiva, IA, iViPay Stablecoin |
| **🧮 Calculadora** | Simulação de investimento com **preço histórico REAL** — escolha o valor e período (7/30/180/365 dias), veja lucro ou prejuízo estimado |
| **💱 Conversor** | IVIP ↔ USD bidirecional calculado com preço ao vivo |
| **📈 Gráfico** | Preço + Volume combinados (Area + Bar), 4 períodos, estatísticas (máxima, mínima, volume médio, variação) |
| **🔥 Burn Counter** | Contador animado de 15,8M tokens queimados (12,4% do supply), ativado por Intersection Observer |
| **📋 Tokenomics** | Endereço do contrato BSC com cópia com 1 clique, link BSCScan |
| **👥 Perfis** | 4 personas de investidor: Iniciante, Intermediário, Profissional, Institucional |
| **🌐 i18n** | pt-BR + EN com toggle por bandeira no header |
| **🔗 Compra** | Redirecionamento direto para PancakeSwap |
| **📄 Páginas** | Termos de Serviço, Política de Privacidade, 404 |

## 🌐 Integrações

| Integração | Finalidade |
|---|---|
| **CoinGecko API** | Preço IVIP, histórico, top 5 criptomoedas — fallback com dados reais |
| **BSCScan** | Verificação do contrato na BSC |
| **PancakeSwap** | Link para compra do token |

## 🎨 Design

| Elemento | Detalhe |
|---|---|
| **Tema** | Escuro cripto — purple profundo + laranja/âmbar |
| **Efeitos** | Glassmorphism, gradientes, blur-3d, glow pulsante |
| **Animações** | CSS fade-in, marquee infinito, pulsar glow |
| **Cards** | Vidro fosco com hover glow |

## 🛠️ Stack

```
Framework:  React 18 + Vite
Router:     react-router-dom
API:        CoinGecko (TanStack Query, refetch 60s)
Gráficos:   Recharts (ComposedChart)
i18n:       Context API (pt-BR / EN)
Estilo:     Tailwind + glassmorphism
UI:         shadcn/ui
```

## 🔗 Token

| Info | Valor |
|---|---|
| **Contrato (BSC)** | `0xbdc87a65e0b6bfb631847b7de815d2b07dec8ee7` |
| **Blockchain** | Binance Smart Chain (BSC) |
| **Compra** | PancakeSwap |

---

<p align="center">
  <i>Landing premium para criptomoeda com dados ao vivo e simulação de investimento — Vibe Coding 💎</i>
</p>
