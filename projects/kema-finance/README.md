# 📊 KemaFinance — Gestão Financeira Pessoal Inteligente

**Stack:** React 18 · TypeScript · Vite · Supabase · shadcn/ui · Tailwind CSS · TanStack Query · Recharts · Gemini AI

---

## 🎯 Sobre

Sistema completo de gestão financeira pessoal utilizado diariamente para controle de receitas, despesas, investimentos e consultoria financeira com IA. Desenvolvido em **Lovable** (Vibe Coding) com arquitetura profissional e publicado como PWA.

> ⚡ **Uso real:** Aplicação em produção usada diariamente pelo autor para gerenciar finanças pessoais, clientes, serviços e instalações.

---

## 🏗️ Arquitetura

```
Frontend (React + Vite + shadcn/ui)
    │
    ├── Supabase Auth (autenticação + RLS)
    ├── Supabase Database (11 tabelas c/ RLS)
    ├── Supabase Storage (anexos de instalação)
    └── Edge Function → Gemini AI (consultor financeiro)
```

## 📊 Funcionalidades

| Módulo | Descrição | Status |
|---|---|---|
| **📈 Dashboard** | Visão geral — receitas, despesas, saldo, metas, filtro quinzenal/semanal/mensal | ✅ Produção |
| **👥 Clientes** | Cadastro completo com CPF/CNPJ com mascaramento PII | ✅ Produção |
| **✂️ Serviços** | Controle de serviços prestados com status de pagamento | ✅ Produção |
| **🔧 Instalações** | Gestão com cálculo automático de M² (valor/24), upload de anexos, status | ✅ Produção |
| **💸 Despesas** | Controle de despesas mensais com status de pagamento | ✅ Produção |
| **🏦 Empréstimos** | Gestão de empréstimos com saldo devedor dinâmico e parcelas | ✅ Produção |
| **⚠️ Dívidas Negativadas** | Controle de dívidas em aberto com valor atualizado | ✅ Produção |
| **📋 Relatórios** | Relatórios semanais/mensais/anuais com exportação CSV e PDF | ✅ Produção |
| **🎯 Metas Financeiras** | Regra 50-30-20 + meta de reserva de emergência (6 meses) | ✅ Produção |
| **🤖 Agente IA** | Consultor financeiro com Gemini — diagnóstico, alertas, score financeiro | ✅ Produção |
| **📱 PWA** | Instalável como app, funciona offline, notificações | ✅ Produção |
| **🔐 Segurança** | RLS + JWT + PII masking + validação de uploads + sanitização | ✅ Produção |

---

## 🧠 Agente Financeiro IA (Gemini)

O coração inteligente do sistema — uma **Edge Function no Supabase** que conecta ao **Gemini** para:

- 📊 **Diagnóstico Financeiro**: Score 0-100 com classificação 🔴/🟡/🟢
- 🚨 **Alertas Inteligentes**: despesas acima da média, dívidas críticas, saldo negativo
- 💡 **Consultoria Personalizada**: chat com IA que analisa dados reais do usuário
- 📐 **Cálculos Avançados**: percentual comprometido, capacidade de economia, meta de reserva
- 🔒 **Segurança**: JWT validation, limite de 50 mensagens, 4000 chars por mensagem

### Score Financeiro

| Score | Classificação | Critério |
|---|---|---|
| 0-39 | 🔴 Crítica | Déficit ou >80% comprometido |
| 40-69 | 🟡 Atenção | 60-80% comprometido |
| 70-100 | 🟢 Saudável | <60% comprometido |

---

## 📈 Estatísticas do Projeto

| Métrica | Valor |
|---|---|
| **Linhas de código** | ~19.323 (TypeScript/TSX) |
| **Componentes de negócio** | 42 |
| **Componentes UI (shadcn)** | 49 |
| **Páginas** | 14 |
| **Hooks customizados** | 13 |
| **Tabelas no banco** | 11 |
| **Migrations SQL** | 18 |
| **Edge Functions** | 1 (Gemini AI) |
| **Autenticação** | Supabase Auth + RLS |
| **PWA** | Service Worker + Manifest + Offline |

---

## 🔐 Segurança Implementada

- ✅ **Row Level Security** em todas as 11 tabelas
- ✅ **Defense in depth**: `.eq('user_id', user.id)` explícito no cliente
- ✅ **PII Masking**: CPF/CNPJ truncados (últimos 4 dígitos)
- ✅ **Upload validation**: validação de MIME type + tamanho
- ✅ **Edge Function segura**: JWT validation + rate limiting
- ✅ **Console logging desabilitado** em produção
- ✅ **Sanitização de inputs**: Zod schemas nos formulários

---

## 💾 Banco de Dados (11 tabelas)

```
profiles              → Dados do usuário (nome, avatar, email)
clientes              → Cadastro de clientes
servicos              → Serviços prestados com valores
instalacoes           → Instalações com cálculo M²
instalacao_anexos     → Upload de fotos/documentos
despesas              → Despesas mensais
emprestimos           → Empréstimos e financiamentos
pagamentos_emprestimo → Histórico de pagamentos
dividas_negativadas   → Dívidas em aberto
metas_financeiras     → Metas 50-30-20 + reserva
sites                 → Sites gerenciados
```

---

## 🎨 Design System

**Tema escuro premium:**
- Deep Navy (#080B1A) — fundo principal
- Indigo (#111631) — superfícies
- Laranja (#F97316) — destaques e ações
- Visual limpo, sem logos, gradientes sutis

---

## 🛠️ Stack Técnica Completa

```
Frontend:     React 18, TypeScript, Vite, Tailwind CSS, shadcn/ui
State:        TanStack React Query (server state)
Forms:        React Hook Form + Zod
Routing:      React Router DOM v6
Charts:       Recharts
Dates:        date-fns
PDF Export:   jsPDF + jspdf-autotable
Ícones:       Lucide React
PWA:          Vite PWA + Service Worker
Backend:      Supabase (Auth, DB, Storage, Edge Functions)
AI:           Gemini (via Edge Function)
CI:           GitHub
```

---

> *Sistema em produção, usado diariamente — 19.323 linhas, 14 páginas, 11 tabelas, IA integrada*
