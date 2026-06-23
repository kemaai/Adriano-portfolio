# Adriano Silva

**AI Product Builder** — Pesquisa, especifica, projeta e entrega produtos digitais usando inteligência artificial como engine de produção.

São Paulo, Brasil · [LinkedIn](https://linkedin.com/in/adrianojsilva86) · [Email](mailto:adrianojsilva86@gmail.com) · +55 11 96652-4658

---

## Sobre Mim

Meu fluxo de trabalho combina pesquisa de mercado, especificação de produto, design de interface e orquestração de IA para transformar ideias em sistemas funcionais completos.

Não escrevo código linha por linha — e essa é minha vantagem. Pesquiso o mercado, entendo a necessidade do cliente, projeto a experiência e direciono a IA (Lovable, Claude Code, Replit, Antigravity) para construir. A IA é a mão-de-obra que executa o código; eu sou a cabeça que decide o que construir, como construir e se está certo. Num mercado onde empresas precisam de produtos digitais rápidos, minha função é eliminar meses de desenvolvimento substituindo por dias de orquestração — sem perder qualidade, segurança ou visão de produto.

Cada projeto começa com análise de necessidades do nicho, evolui para um PRD estruturado, passa por prototipação visual (wireframes/mockups como referência para a IA) e é construído em ciclos iterativos de prompt → revisão → ajuste. Uso Hermes Agent como orquestrador de agentes de IA para tarefas complexas de desenvolvimento e configuração de infraestrutura.

Tenho formação em Gestão de TI, MBA em IA e Estratégia de Dados, certificação Lovable Certified Diamond e experiência prática com Claude Code, Hermes Agent e múltiplas plataformas de geração de código por IA.

---

## Certificações e Formação

| Certificação | Instituição |
|---|---|
| Lovable Certified Diamond | Lovable |
| Pós-graduação — Vibe Coding AI | Impacta Tecnologia (2026-2027) |
| MBA — IA, Estratégia de Dados e Eficiência | Frons Educação (2024-2025) |
| Gestão em TI | Universidade Paulista (2014-2016) |
| Desenvolvimento de Sistemas | Senac (2014-2015) |

---

## Stack de Trabalho

**Orquestração de IA:** Lovable, Claude Code, Replit, Antigravity, Hermes Agent

**Infraestrutura:** Supabase (Auth, DB, Storage, Edge Functions, RLS), Cloudflare Workers, Paddle

**Frontend (gerado por IA com revisão manual):** React, TypeScript, Tailwind, shadcn/ui, TanStack Start, Framer Motion

**Ferramentas de Produto:** ChatGPT (PRD, especificação, geração de prompts), mockups/wireframes, pesquisa de mercado

---

## Projetos

### KemaFinance — Sistema de Gestão Financeira Pessoal com IA

[Repositório](https://github.com/kemaai/kema-finance)

Stack gerado por IA: React, TypeScript, Supabase, shadcn/ui, Gemini AI, Vite, PWA

Sistema completo de gestão financeira pessoal. Inclui dashboard com score financeiro 0-100 baseado em receitas, despesas, dívidas e investimentos, categorização inteligente, metas 50-30-20, relatórios CSV/PDF e consultoria financeira via Gemini AI (Edge Function). Funciona como PWA com suporte offline parcial. 19 mil linhas geradas em ambiente Lovable.

O que eu fiz: pesquisei necessidades de organização financeira pessoal, estruturei o PRD com as funcionalidades necessárias (dashboard, metas, consultoria IA), projetei o fluxo de telas com mockups de referência e direcionei a IA na criação e ajustes. Configurei RLS e políticas de segurança no Supabase.

---

### Moisés Perfumaria — Sistema de Gestão com Catálogo Online

[Repositório](https://github.com/kemaai/moises-perfumaria)

Stack gerado por IA: React, TypeScript, Supabase, shadcn/ui, Deno Edge, PWA

Sistema multi-tenant para perfumaria com catálogo online público integrado ao WhatsApp. Inclui PDV, controle de estoque, encomendas, recebíveis, CRM com templates de cobrança inteligentes e catálogo público PWA. 12 mil linhas geradas em ambiente Lovable.

O que eu fiz: levantei requisitos com cliente real do segmento de perfumaria, estruturei as funcionalidades de catálogo + PDV + estoque, projetei a UX do catálogo público e configurei Edge Function `catalog-order` com validação de dados. Ajustei políticas RLS por tenant.

---

### IMOVVY — Plataforma SaaS para Corretores de Imóveis

[Repositório](https://github.com/kemaai/oimovvy)

Stack gerado por IA: React, TypeScript, Supabase, Paddle, Deno Edge, Sentry

Plataforma SaaS para corretores de imóveis com CRM, catálogo público, billing via Paddle (assinatura recorrente), dois assistentes de IA (Maicon para suporte interno, Mavie para captura de leads no site público), suporte multi-agência com até 5 corretores, agenda de visitas, relatórios exportáveis e onboarding interativo. 15 mil linhas geradas em ambiente Lovable.

O que eu fiz: desenvolvi a especificação do produto SaaS (dois planos, trial de 14 dias, multi-agência), projetei a experiência de onboarding e as telas do catálogo público, configurei Edge Functions para Paddle e Lovable API via Claude Code e ajustei políticas de segurança por imobiliária/corretor.

---

### Amarella Creative — Site Premium Estúdio de Branding

[Repositório](https://github.com/kemaai/amarellacreative)

Stack gerado por IA: TanStack Start, React 19, Framer Motion, Tailwind v4, Cloudflare Workers, Bun

Site institucional premium para estúdio de branding e storytelling. Design editorial com 13 seções, animações cinematográficas, paleta oklch, scroll suave Lenis, deploy em Cloudflare Workers. 6 mil linhas geradas.

O que eu fiz: projetei a estrutura editorial do site (hero, serviços, processo, histórias, depoimentos), criei mockups de referência visual para cada seção, configurei o deploy no Cloudflare Workers e extraí o sistema de design como skill reutilizável.

---

### iVipCoin — Landing Page para Criptomoeda

[Repositório](https://github.com/kemaai/ivipcoin)

Stack gerado por IA: React, Vite, CoinGecko API, TanStack Query, Recharts, Tailwind, shadcn/ui

Landing page premium para criptomoeda listada na BSC. Inclui cotações ao vivo da CoinGecko, calculadora de investimento com preço histórico real, gráfico interativo de preço/volume, conversor IVIP-USD e suporte bilíngue (pt-BR/EN). 7 mil linhas geradas.

O que eu fiz: especifiquei as funcionalidades essenciais para uma landing page de cripto (preço vivo, calculadora, gráfico, tokenomics), projetei o layout escuro com dados em tempo real e configurei a integração com a API CoinGecko.

---

### Formulário KemaSites — Sistema de Briefing para Criação de Sites

[Repositório](https://github.com/kemaai/formulario-kemasites-72)

Stack gerado por IA: React, Vite, Supabase, Zod, react-hook-form, shadcn/ui

Sistema de briefing multi-etapas para captura de informações de clientes da KemaSites. 15 seções de coleta (do hero à autorização LGPD), upload de arquivos ao Supabase Storage, painel admin com geração automática de PRD em markdown. 10 mil linhas geradas.

O que eu fiz: estruturei as 15 seções necessárias para capturar todas as informações de um briefing de site, projetei o fluxo de duas etapas com validação Zod e configurei o painel admin com controle de acesso.

---

## Por que trabalhar comigo

Eu entrego produtos digitais completos — não apenas código. Meu valor está em:

- **Pesquisar e entender** o que o mercado e o cliente precisam
- **Estruturar e especificar** o produto antes de construir
- **Projetar a experiência** do usuário com mockups e referências visuais
- **Orquestrar ferramentas de IA** (Lovable, Claude Code, Hermes Agent, Replit) para gerar o código de forma rápida e iterativa
- **Revisar, testar e ajustar** cada funcionalidade até estar pronta

*"Sou o orquestrador. Pesquiso o mercado, entendo a necessidade do cliente, projeto a experiência e direciono a IA para construir. A IA é a mão-de-obra que executa o código; eu sou a cabeça que decide o que construir, como construir e se está certo. Num mercado onde empresas precisam de produtos digitais rápidos, minha função é eliminar meses de desenvolvimento substituindo por dias de orquestração — sem perder qualidade, segurança ou visão de produto."*

Empresas que precisam transformar ideias em produtos funcionais em dias, não meses, encontram em mim um profissional que combina visão de produto com capacidade de execução via IA.

---

## Contato

| Canal | Link |
|---|---|
| LinkedIn | /in/adrianojsilva86 |
| Email | adrianojsilva86@gmail.com |
| WhatsApp | +55 11 96652-4658 |
