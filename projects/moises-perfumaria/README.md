# 🌹 Moisés Perfumaria — Sistema de Gestão com Catálogo Online

**Stack:** React 18 · TypeScript · Vite · Supabase · shadcn/ui · Tailwind CSS · TanStack Query · Recharts · Deno Edge Functions · PWA · WhatsApp API

---

## 🎯 Sobre

Sistema completo de gestão para perfumaria com **catálogo online público** multi-tenant — cada loja tem seu próprio slug (ex: `/catalogo/moises-perfumaria`). O cliente navega, monta carrinho e envia o pedido via WhatsApp sem precisar se cadastrar.

**12.930 linhas** · **17 páginas** · **14 tabelas** · **9 enums** · **12 RPCs** · **1 Edge Function**

> 💼 **Projeto para cliente real** — dono de perfumaria. Em produção via Lovable.

---

## 📋 Funcionalidades

| Módulo | Descrição |
|---|---|
| **🪟 Catálogo Público** | Vitrine com carrosséis (mais vendidos, destaques, novidades), busca, filtro por categoria, carrinho via localStorage, pedido enviado por WhatsApp + Edge Function |
| **📈 Dashboard** | Receita/lucro mensal, KPIs (estoque baixo, pedidos pendentes, recebíveis), gráfico 6 meses, alertas |
| **🧴 Produtos** | CRUD completo com imagem principal + galeria, categorias (masculino/feminino/unissex), tipo (estoque/encomenda/ambos), flag destaque/novidade |
| **💰 Vendas (PDV)** | Carrinho de venda com itens de estoque ou encomenda, múltiplos métodos de pagamento (dinheiro/cartão/pix/fiado), baixa automática de estoque |
| **📦 Estoque** | Movimentações (compra/ajuste/perda/cancelamento), histórico por produto, alerta de estoque mínimo |
| **🚚 Encomendas** | Pipeline tracking: aguardando_compra → comprado → em_trânsito → disponível → entregue, notificação WhatsApp |
| **💳 Recebíveis** | Contas a receber com pagamentos parciais, status (aberto/parcial/quitado/atrasado), cobrança via WhatsApp |
| **👥 Clientes (CRM)** | Cadastro com LGPD (função de anonimização), match automático por telefone nos pedidos do catálogo |
| **📊 Relatórios** | Vendas/lucro por período, performance por produto, exportação |
| **⚙️ Configurações** | Nome da loja, WhatsApp, templates de cobrança/catálogo/pedido customizáveis |

## 🔐 Segurança

- **Multi-tenant real** — todas as 14 tabelas protegidas por RLS com `tenant_id`
- **Roles:** `admin` / `staff` com permissões diferentes
- **Edge Function:** validação rigorosa de body, slug e consentimento LGPD
- **RPCs públicas:** security definer, escopo por slug, somente leitura
- **LGPD:** `anonymize_customer()` para exclusão de dados

## 💬 Integração WhatsApp

Sistema de templates inteligentes com placeholders (`{nome}`, `{valor}`, `{vencimento}`, `{link}`, `{itens}`) para:

| Template | Finalidade |
|---|---|
| `overdue` | Cobrança de valor vencido |
| `upcoming` | Lembrete de pagamento |
| `thanks` | Agradecimento pós-compra |
| `catalog` | Envio do link do catálogo |
| `orderConfirm` | Confirmação de pedido |
| `orderReady` | Aviso de pedido pronto |

## 🗄️ Banco de Dados

**14 tabelas:** `profiles`, `user_roles`, `products`, `product_images`, `customers`, `sales`, `sale_items`, `receivables`, `receivable_payments`, `orders`, `order_items`, `inventory_movements`, `notifications`, `app_settings`

**9 enums:** `app_role`, `product_category`, `product_type`, `movement_type`, `order_status`, `payment_method`, `sale_financial_status`, `receivable_status`, `sale_item_source`

## 🛠️ Stack

```
Frontend:  React 18, TypeScript, Vite, Tailwind, shadcn/ui
State:     TanStack React Query
Formulários: React Hook Form + Zod
Gráficos:  Recharts
PWA:       vite-plugin-pwa (instalável)
Backend:   Supabase (Auth, DB, Storage, Edge Functions)
Edge:      Deno (catalog-order — pedido público)
Testes:    Vitest + Testing Library
```

## 🚀 Desenvolvimento

```sh
git clone https://github.com/kemaai/moises-perfumaria.git
cd moises-perfumaria
npm i
npm run dev
```

---

<p align="center">
  <i>Sistema multi-tenant para perfumaria real, em produção — construído com Vibe Coding 💎</i>
</p>
