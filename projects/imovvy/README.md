# 🏠 IMOVVY — Plataforma SaaS para Corretores de Imóveis

**Stack:** React 18 · TypeScript · Vite · Supabase · shadcn/ui · Paddle · Sentry · Deno Edge · PWA · IA

---

## 🎯 Sobre

**IMOVVY** é uma plataforma SaaS completa para corretores de imóveis autônomos e imobiliárias — CRM, catálogo público, gestão de equipe, faturamento via **Paddle** (trial + planos recorrentes) e **dois assistentes de IA** (Maicon de suporte + Mavie comercial).

**15.931 linhas** · **28 páginas** · **70 componentes** · **13 tabelas** · **5 Edge Functions** · **38 migrations**

> 💼 **Projeto quase pronto** — testes E2E com Playwright em andamento.

---

## 📋 Funcionalidades

| Módulo | Descrição |
|---|---|
| **🏠 Landing Premium** | Dark theme dourado, animações, mockups, FAQ, SEO — 1.032 linhas |
| **🪟 Catálogo Público** | `/c/:slug` — busca, filtros (cidade/tipo/preço), WhatsApp, contador de views |
| **🏘️ Imóveis** | CRUD completo com fotos galeria, tipos (casa/apto/terreno/etc), PDF book automático, aprovação por imobiliária |
| **👥 CRM Clientes** | Kanban (frio/morno/quente/negociação/ganho/perdido), importação XLSX, atividades, temperatura |
| **💰 Vendas** | Funil com status tracking, comissão esperada vs recebida, atrelada a imóvel + cliente |
| **📅 Agenda** | Visitas e follow-ups com calendário, status, filtros por tipo, cliente e imóvel |
| **👥 Equipe** | Convites por email, até 5 corretores, aprovação de imóveis pela imobiliária |
| **🤖 Maicon (IA Suporte)** | Assistente com KB RAG, sugere próximo passo baseado na rota atual do app |
| **🤖 Mavie (IA Comercial)** | Assistente público na landing, captura lead qualificado por intenção de compra |
| **💳 Billing** | Paddle com trial 14 dias, planos (R$78,90/autônomo · R$178,90/imobiliária) |
| **📊 Relatórios** | Vendas/leads/imóveis, exportação PDF/XLSX/CSV, filtro por período e corretor |
| **⚙️ Configurações** | Perfil, avatar, WhatsApp, CRECI, logo com upload drag-and-drop |
| **🎫 Suporte** | Chamados (chamado/sugestão/elogio), anexos em bucket privado signed URL |
| **📄 LGPD** | Banner de consentimento + páginas de privacidade e termos |

## 🤖 Assistentes de IA

| Assistente | Local | Função |
|---|---|---|
| **Maicon** | `/app/suporte` (autenticado) | Suporte técnico — passos numerados, integração com KB e rota atual |
| **Mavie** | Landing (público) | Consultora comercial — captura lead qualificado via formulário |

Ambos usam **Edge Function `assistant-chat`** (286 linhas, Deno) que faz RAG sobre `kb_entries` com matching por keywords.

## 💳 Planos (via Paddle)

| Plano | Preço | Features |
|---|---|---|
| **Corretor Autônomo** | R$ 78,90/mês | Catálogo, CRM, agenda, IA, suporte |
| **Imobiliária** | R$ 178,90/mês | Tudo + até 5 corretores + aprovação + relatórios |

## 🗄️ Banco de Dados

**13 tabelas:** profiles, catalog_settings, properties, property_leads, property_views, clients, client_activities, sales, schedules, team_invites, subscriptions, support_tickets, kb_entries, assistant_conversations, assistant_messages

**12 enums:** account_type, lead_temperature, lead_source, property_type, property_purpose, property_status, property_condition, address_visibility, finalidade_cliente, forma_pagamento, support_ticket_status, support_ticket_type

## 🔐 Segurança

- **RLS granular** — `auth.uid()` em todas as tabelas
- **Buckets privados** — anexos de suporte via signed URL apenas
- **View pública** — `public_broker_profiles` só expõe colunas seguras
- **LGPD** — banner de consentimento + páginas legais
- **Sentry** — erro tracking nas Edge Functions

## 🛠️ Stack

```
Frontend:  React 18, TypeScript, Vite, Tailwind, shadcn/ui
Gráficos:  Recharts (AreaChart, BarChart, PieChart)
PDF:       jsPDF + jsPDF-AutoTable
Planilhas: xlsx (SheetJS)
Upload:    react-dropzone
Backend:   Supabase (Auth, DB, Storage, Edge Functions - Deno)
Pagamentos: Paddle (sandbox / live)
Monitoria:  Sentry
IA:         Lovable API + KB-empurrada RAG
Testes:     Vitest + Playwright (E2E planejado)
```

## 🚀 Desenvolvimento

```sh
git clone https://github.com/kemaai/oimovvy.git
cd oimovvy
npm i
cp .env.example .env  # preencha credenciais
npm run dev
```

---

<p align="center">
  <i>SaaS imobiliário quase em produção — billing, IA, multi-usuário, construído com Vibe Coding 💎</i>
</p>
