# 📋 Formulário KemaSites — Sistema de Briefing para Criação de Sites

**Stack:** React 18 · Vite · TypeScript · Supabase · shadcn/ui · Zod · react-hook-form

---

## 🎯 Sobre

Sistema de **briefing multi-etapas** para captura de informações de clientes da KemaSites — coleta todos os dados necessários para criar um site profissional: dados do cliente, empresa, design, galeria, depoimentos, FAQ, autorização e upload de arquivos. Tudo salvo no **Supabase** com **painel admin** completo para gestão dos leads e **geração automática de PRD**.

**10.194 linhas** · **15 seções** · **13 migrations** · **Upload direto ao Supabase Storage**

> 💼 **Ferramenta operacional real da KemaSites** — usada no dia a dia para capturar briefings de clientes.

---

## 📋 Funcionalidades

| Funcionalidade | Descrição |
|---|---|
| **📝 Formulário Multi-etapas** | 2 etapas com 15 seções — do hero à autorização LGPD |
| **☁️ Upload de Arquivos** | Até 50MB total, 10MB/arquivo, imagens + PDF → Supabase Storage |
| **🔄 Auto-save** | Persistência via localStorage — cliente não perde dados ao fechar |
| **✅ Validação Zod** | Schema completo de validação com mensagens em pt-BR |
| **📋 Resumo Final** | Modal de revisão com todos os dados antes do envio |
| **📄 Gerador de PRD** | Gera Documento de Requisitos do Produto (markdown) com download e cópia |
| **🔐 Painel Admin** | Autenticação Supabase, CRUD de leads, busca, filtro por status (aguardando/em_andamento/concluido) |
| **🖼️ Image Gallery** | Visualização de imagens com zoom |
| **👤 Auth** | Login/senha para acesso ao painel admin |

## 🏗️ Seções do Formulário

| # | Seção | Conteúdo |
|---|---|---|
| 1 | **Hero Principal** | Frase de destaque, imagem de fundo |
| 2 | **Dados do Cliente** | Nome, telefone, email, nicho (dropdown + personalizado) |
| 3 | **Dados da Empresa** | Nome, descrição, slogan, logomarca, site referência |
| 4 | **Serviços** | Até 6 serviços/produtos |
| 5 | **Diferenciais** | Diferenciais competitivos |
| 6 | **Sobre** | Texto até 5 linhas, imagem ilustrativa |
| 7 | **Galeria** | Múltiplas imagens do portfólio |
| 8 | **Contato** | Endereço, telefone, email, horário |
| 9 | **Redes Sociais** | Instagram, Facebook, WhatsApp, outras |
| 10 | **FAQ** | Perguntas frequentes (seção repetível) |
| 11 | **Depoimentos** | Depoimentos de clientes |
| 12 | **Trabalhos** | Portfólio de trabalhos realizados |
| 13 | **Domínio** | Domínio atual e desejado |
| 14 | **Sugestões** | Campo livre para observações |
| 15 | **Autorização** | Checkbox LGPD e autorização de publicação |

## 🛠️ Stack

```
Frontend:  React 18 + Vite + TypeScript
UI:        shadcn/ui (Radix + Tailwind)
Forms:     react-hook-form + Zod
Banco:     Supabase (Auth + DB + Storage)
Upload:    Supabase Storage (bucket client-files)
Persistência: localStorage auto-save
Admin:     Dashboard com busca, filtros, CRUD
Utils:     PRD generator (markdown), file validation
Router:    react-router-dom
```

## 📊 Estatísticas

| Métrica | Valor |
|---|---|
| **Linhas de código** | **10.194** |
| **Páginas** | 5 |
| **Seções do formulário** | 15 |
| **Migrations Supabase** | 13 |

---

<p align="center">
  <i>Sistema operacional de briefing para criação de sites — Vibe Coding 💎</i>
</p>
