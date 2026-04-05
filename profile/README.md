<div align="center">

<img src="public/logo.png" alt="BizAnalyticsAI Logo" width="90" height="90" />

# BizAnalyticsAI

**Enterprise SaaS Platform for Business Intelligence, Predictive Analytics & AI-Powered Decision Making**

[![Next.js](https://img.shields.io/badge/Next.js-16-black?logo=next.js&logoColor=white)](https://nextjs.org)
[![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=black)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)](https://typescriptlang.org)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-4-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com)
[![Supabase](https://img.shields.io/badge/Supabase-PostgreSQL-3ECF8E?logo=supabase&logoColor=white)](https://supabase.com)
[![Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-black?logo=vercel&logoColor=white)](https://vercel.com)
[![PWA](https://img.shields.io/badge/PWA-Enabled-5A0FC8?logo=pwa&logoColor=white)](public/manifest.json)
[![i18n](https://img.shields.io/badge/i18n-pt--BR%20%7C%20en--US%20%7C%20es--ES-7c3aed)](messages/)
[![License](https://img.shields.io/badge/License-Proprietary-red)](LICENSE)

[**Website**](https://bizanalyticsai.com.br) · [**Dashboard**](https://bizanalyticsai.com.br/dashboard) · [**Documentation**](https://bizanalyticsai.com.br/docs) · [**API Reference**](https://bizanalyticsai.com.br/dashboard/api) · [**Support**](https://bizanalyticsai.com.br/suporte)

</div>

---

## Table of Contents

- [Overview](#overview)
- [Platform Pillars](#platform-pillars)
- [Tech Stack](#tech-stack)
- [Architecture](#architecture)
- [Application Modules](#application-modules)
  - [Public Site](#public-site)
  - [User Dashboard](#user-dashboard)
  - [Admin Panel](#admin-panel)
  - [Student Portal](#student-portal)
- [API Reference](#api-reference)
- [Solutions Ecosystem](#solutions-ecosystem)
  - [LTD Hub Desktop](#1-ltd-hub-desktop)
  - [NexaBrain Desktop](#2-nexabrain-desktop)
  - [AI Agents Platform](#3-ai-agents-platform)
  - [BusinessPlans AI](#4-businessplans-ai)
  - [Mobile App](#5-mobile-app)
  - [VS Code Extension](#6-vs-code-extension)
  - [Browser Extension](#7-browser-extension)
  - [Python Library](#8-python-library)
- [Database Schema](#database-schema)
- [Internationalization](#internationalization)
- [White-Label Customization](#white-label-customization)
- [eBooks Library](#ebooks-library)
- [PWA Support](#pwa-support)
- [Getting Started](#getting-started)
- [Environment Variables](#environment-variables)
- [Deployment](#deployment)
- [Project Structure](#project-structure)

---

## Overview

**BizAnalyticsAI** is a production-grade SaaS platform built for entrepreneurs, business analysts, and growth-stage companies that need deep operational and predictive intelligence. The platform combines a powerful web dashboard with an ecosystem of eight companion products — desktop applications, mobile apps, IDE extensions, and developer libraries — all integrated through a shared Supabase backend with full Row Level Security.

The platform is live at [bizanalyticsai.com.br](https://bizanalyticsai.com.br) and serves three distinct user portals: the main user dashboard (`/dashboard`), an admin control panel (`/admin`), and a student collaboration portal (`/alunos`).

### Key Differentiators

| Feature | Description |
|---|---|
| **AI-Powered Analytics** | Monte Carlo simulations, Churn/LTV modeling, and predictive revenue forecasting |
| **Business Plan Builder** | AI-assisted structured business plan creation with export to PDF |
| **Financial Viability Engine** | Break-even analysis, payback period, and operational margin calculators |
| **Market Intelligence** | TAM/SAM/SOM, industry segmentation, Porter's Five Forces, and competitive mapping |
| **KPI Management** | Real-time key performance indicator tracking with goal-setting and benchmarks |
| **Multi-Product Ecosystem** | 8 companion products: desktop, mobile, IDE extensions, browser extension, Python library |
| **Per-User White-Label** | Each user customizes their own dashboard — colors, branding, navigation order — with full isolation |
| **Tri-Portal Architecture** | Separate, independently secured portals for users, admins, and students |
| **Multilingual** | Native support for Portuguese (pt-BR), English (en-US), and Spanish (es-ES) |
| **PWA Ready** | Full offline capability with service worker, app manifest, and install prompt |
| **OpenAPI** | Auto-generated OpenAPI spec at `/api/v1/openapi` |

---

## Platform Pillars

```
┌────────────────────────────────────────────────────────────────────────┐
│                          BizAnalyticsAI                                 │
│                                                                          │
│  ┌──────────────┐  ┌──────────────┐  ┌────────────┐  ┌─────────────┐  │
│  │  Business    │  │  Predictive  │  │   Market   │  │  Financial  │  │
│  │  Planning    │  │  Analytics   │  │  Intel.    │  │  Modeling   │  │
│  │              │  │              │  │            │  │             │  │
│  │ Plan Builder │  │ Monte Carlo  │  │ TAM/SAM    │  │ Break-Even  │  │
│  │ Canvas AI    │  │ Churn / LTV  │  │ PESTEL     │  │ Payback     │  │
│  │ Roadmap      │  │ Forecasting  │  │ Porter 5F  │  │ Unit Econ.  │  │
│  └──────────────┘  └──────────────┘  └────────────┘  └─────────────┘  │
│                                                                          │
│  ┌──────────────┐  ┌──────────────┐  ┌────────────┐  ┌─────────────┐  │
│  │  Data        │  │  AI Chat     │  │  Reports & │  │  KPI        │  │
│  │  Analysis    │  │  Assistant   │  │  Export    │  │  Tracking   │  │
│  │              │  │              │  │            │  │             │  │
│  │ CSV Import   │  │ NexaBrain    │  │ PDF / CSV  │  │ Custom Goals│  │
│  │ Chart Builder│  │ Context-Aware│  │ Scheduled  │  │ Alerts      │  │
│  │ AI Insights  │  │ Multi-Model  │  │ Branded    │  │ Benchmarks  │  │
│  └──────────────┘  └──────────────┘  └────────────┘  └─────────────┘  │
└────────────────────────────────────────────────────────────────────────┘
```

---

## Tech Stack

### Frontend

| Technology | Version | Purpose |
|---|---|---|
| **Next.js** | 16.0.10 | App Router, SSR, API Routes, Edge Middleware |
| **React** | 19.2.0 | UI rendering, hooks, concurrent features |
| **TypeScript** | 5.x | End-to-end static typing |
| **Tailwind CSS** | 4.1.9 | Utility-first styling with CSS custom properties |
| **Radix UI** | Latest | 40+ accessible, headless UI primitives |
| **Recharts** | 2.15.4 | Composable data visualization charts |
| **React Hook Form** | 7.60.0 | Performant, zero-dependency form management |
| **Zod** | 3.25.76 | Schema declaration and runtime validation |
| **next-intl** | 4.8.3 | Type-safe i18n (3 locales, cookie-based detection) |
| **next-themes** | 0.4.6 | Dark/light mode with zero flash |
| **Lucide React** | 454.0 | 454 consistent, customizable SVG icons |
| **Sonner** | 1.7.4 | Opinionated toast notifications |
| **Embla Carousel** | 8.5.1 | Lightweight carousel/slider |
| **React Resizable Panels** | 2.1.7 | Resizable split-panel layouts |
| **Vaul** | Latest | Drawer / bottom sheet component |
| **React Markdown** | 10.1.0 | Markdown rendering with remark-gfm |
| **html2canvas + jsPDF** | Latest | Client-side PDF generation |
| **Vercel Analytics** | 1.3.1 | Page views, Web Vitals, user flows |

### Backend & Data

| Technology | Version | Purpose |
|---|---|---|
| **Supabase** | 2.99.3 | PostgreSQL, Auth, Realtime, Storage, Edge Functions |
| **@supabase/ssr** | 0.9.0 | Cookie-based session management for App Router |
| **Next.js API Routes** | — | 60+ RESTful endpoints, versioned at `/api/v1/` |
| **Nodemailer** | 8.0.3 | Transactional email delivery |

### Infrastructure

| Technology | Purpose |
|---|---|
| **Vercel** | Hosting, CDN, Edge Network, Serverless Functions |
| **Supabase** | Managed PostgreSQL + Auth backend |
| **PWA / Service Worker** | Offline support, app installability |
| **ESLint** | Code quality and consistency enforcement |

---

## Architecture

### High-Level System Diagram

```
┌────────────────────────────────────────────────────────────────────┐
│                           Client Browser                            │
│                                                                      │
│   ┌─────────────┐   ┌─────────────┐   ┌─────────────────────────┐ │
│   │ Public Site │   │  Dashboard  │   │  Admin · Student Portal │ │
│   │     /       │   │  /dashboard │   │  /admin  ·  /alunos     │ │
│   └──────┬──────┘   └──────┬──────┘   └────────────┬────────────┘ │
│          └────────────────┬┘────────────────────────┘              │
└───────────────────────────┼────────────────────────────────────────┘
                            │ HTTPS
┌───────────────────────────▼────────────────────────────────────────┐
│                        Vercel Edge Network                          │
│                                                                      │
│  ┌────────────────────────────────────────────────────────────┐    │
│  │                    Next.js Middleware                        │    │
│  │                                                              │    │
│  │  Matcher: /dashboard/* · /admin/* · /alunos/* · /login      │    │
│  │                                                              │    │
│  │  /login, /registro  → getSession() (cookie, no network)     │    │
│  │  /dashboard+        → getUser()   (validates with Supabase) │    │
│  │                                                              │    │
│  │  Public routes: middleware bypassed entirely → zero latency  │    │
│  └────────────────────────────────────────────────────────────┘    │
│                                                                      │
│  ┌────────────────────────────────────────────────────────────┐    │
│  │                   Next.js App Router                         │    │
│  │                                                              │    │
│  │   Server Components    Client Components    API Routes       │    │
│  │   (SSR / RSC)          ("use client")       /api/**          │    │
│  │                                                              │    │
│  │   i18n via next-intl   Context (auth,        60+ endpoints   │    │
│  │   3 locales            customization)        v1 versioned    │    │
│  └────────────────────────────────────────────────────────────┘    │
└───────────────────────────┬────────────────────────────────────────┘
                            │ Supabase SDK
┌───────────────────────────▼────────────────────────────────────────┐
│                            Supabase                                 │
│                                                                      │
│  ┌─────────────┐  ┌──────────────┐  ┌──────────────────────────┐  │
│  │ PostgreSQL  │  │     Auth     │  │    Row Level Security     │  │
│  │             │  │              │  │                          │  │
│  │ 30+ tables  │  │ JWT Cookies  │  │  Per-user isolation       │  │
│  │ JSONB cols  │  │ 3 user types │  │  is_admin() DEFINER      │  │
│  │ 20+ migr.   │  │ user/admin/  │  │  org-scoped policies     │  │
│  │ Triggers    │  │ student      │  │                          │  │
│  └─────────────┘  └──────────────┘  └──────────────────────────┘  │
└────────────────────────────────────────────────────────────────────┘
```

### Authentication Architecture

Three user types, each with their own session context and protected portal:

```
User type     Portal         Auth method          Role check
──────────────────────────────────────────────────────────────
Regular user  /dashboard     Supabase JWT cookie  RLS per-user
Admin         /admin         Supabase JWT cookie  is_admin() fn
Student       /alunos        Supabase JWT cookie  student record
```

**Session persistence:** `localStorage` caches user identity per-user key (`bizanalytics_auth_user`) for instant re-render across route navigations. Supabase validates asynchronously. Clearing on logout prevents cross-account data leaking.

### Dashboard Customization Architecture

```
Mount → getUser() from Supabase
      ↓
resetDom()                      ← wipe previous user's CSS vars
      ↓
Read localStorage[userId]       ← fast initial render
      ↓
Load from user_dashboard_settings (Supabase)  ← source of truth
      ↓
applyToDom(settings)            ← override :root CSS variables
      ↓
--accent · --background · --sidebar · --card · --foreground · --radius
```

---

## Application Modules

### Public Site

The marketing and content site built on the `(public)` route group with shared Navbar + Footer layout. No authentication required.

#### All Public Pages

| Route | Description |
|---|---|
| `/` | Homepage — hero, features showcase, social proof, CTA |
| `/sobre` | Company story, mission, and values |
| `/funcionalidades` | Full feature list with interactive demos |
| `/produtos` | Product catalog overview |
| `/precos` | Pricing tiers with feature comparison |
| `/clientes` | Customer case studies and logos |
| `/recursos` | Resources hub |
| `/tutoriais` | Step-by-step tutorials |
| `/webinars` | Webinar schedule and on-demand recordings |
| `/ebooks` | Free ebook download gate (lead capture) |
| `/blog` | Editorial blog with pagination |
| `/blog/[slug]` | Article page with markdown, comments, and likes |
| `/docs` | Developer documentation |
| `/comunidade` | Community portal |
| `/suporte` | Support center |
| `/contato` | Contact form with Nodemailer delivery |
| `/status` | Platform uptime and incident dashboard |
| `/equipe` | Team directory with roles |
| `/carreiras` | Open positions |
| `/investidores` | Investor relations |
| `/imprensa` | Press kit and media assets |
| `/parceiros` | Partner program |
| `/solucoes` | Solution ecosystem overview |
| `/solucoes/web` | Web platform deep-dive |
| `/solucoes/desktop` | Desktop application detail |
| `/solucoes/mobile` | Mobile app detail |
| `/solucoes/businessplans` | BusinessPlans AI detail |
| `/solucoes/extensao-vscode` | VS Code extension detail |
| `/solucoes/extensao-navegador` | Browser extension detail |
| `/solucoes/biblioteca-python` | Python library detail |
| `/privacidade` | Privacy policy |
| `/termos` | Terms of service |
| `/cookies` | Cookie policy |
| `/gdpr` | GDPR compliance statement |
| `/licencas` | Open-source license attributions |

#### Navbar

The `Navbar` component features:
- Mega-menu with dropdown column panels (up to 6 columns)
- Auth-aware CTA: "Login" / "Register" for guests; "Dashboard" button for authenticated users
- Mobile drawer with expandable sections
- Theme toggle (dark/light)
- Language switcher (3 locales)
- Smooth scroll detection for transparent → frosted glass transition

---

### User Dashboard

Protected at `/dashboard/*`. Requires valid Supabase JWT session.

#### Feature Modules

| Module | Route | Core Functionality |
|---|---|---|
| **Overview** | `/dashboard` | Summary KPI cards, activity feed, quick period selector |
| **Onboarding** | `/dashboard/onboarding` | Business profile setup: industry, stage, revenue, team size |
| **Business Plan Builder** | `/dashboard/plano-negocios` | AI-assisted plan with sections: Executive Summary, Market, Financials, Operations |
| **My Plans** | `/dashboard/planos` | Saved plans list with status (draft / published) and version history |
| **Viability Calculator** | `/dashboard/viabilidade` | Break-even point, payback period, operational margin, ROI |
| **Predictive Analysis** | `/dashboard/analise-preditiva` | Monte Carlo simulation, Churn rate modeling, LTV projection |
| **Market Analysis** | `/dashboard/mercado` | TAM/SAM/SOM, segmentation, Porter's Five Forces, PESTEL |
| **Data Analysis** | `/dashboard/analise-dados` | CSV import, chart builder, AI-generated insights |
| **Reports** | `/dashboard/relatorios` | Scheduled reports, PDF/CSV export with branding |
| **KPI Indicators** | `/dashboard/indicadores` | Custom KPI dashboard with goal tracking and alerts |
| **Downloads** | `/dashboard/downloads` | Resource library, ebooks, templates |
| **API & Integrations** | `/dashboard/api` | API key management, usage stats, integration docs |
| **AI Chat** | `/dashboard/chat-ia` | Context-aware AI assistant with conversation history |
| **NexaBrain** | `/dashboard/nexabrain` | NexaBrain AI model integration panel |
| **Testimonial** | `/dashboard/depoimento` | Submit and manage customer testimonials |
| **Documentation** | `/dashboard/docs` | In-app knowledge base |
| **Personalization** | `/dashboard/white-label` | Per-user branding, colors, navigation customization |
| **Profile** | `/dashboard/perfil` | Account settings, avatar, password, preferences |
| **Notifications** | `/dashboard/notificacoes` | Notification center with read/unread management |

#### Dashboard Layout

```
┌──────────────────────────────────────────────────────────┐
│  Header: Search · Theme · Language · Notifications · User │
├──────────────┬───────────────────────────────────────────┤
│              │                                            │
│   Sidebar    │           Main Content Area               │
│              │                                            │
│  Logo/Brand  │  max-width: 1600px   overflow-y: auto     │
│  User info   │                                            │
│  Nav items   │  children (page component)                │
│  (ordered    │                                            │
│  per prefs)  │                                            │
│              │                                            │
│  ── ── ──    │                                            │
│  Back to Site│                                            │
│  Logout      │                                            │
└──────────────┴───────────────────────────────────────────┘
```

The sidebar supports:
- **Collapse** to 72px icon-only mode
- **Mobile drawer** with backdrop overlay
- **Dynamic order** — sorted by user's `nav_order` preference
- **Hidden items** — items in `hidden_nav_items` are removed entirely
- **Custom branding** — `settings.brand_name` replaces "BizAnalyticsAI"; `settings.logo_url` replaces the default logo
- **Custom background color** via `settings.sidebar_color`

#### Onboarding Tutorial

First-time visitors see a guided 20-step tutorial popup:

- One step per dashboard route with dedicated icon, gradient color, and description
- Animated progress bar and dot navigator
- Feature list and "Pro tip" callout per step
- **Previous / Next** buttons — each Next navigates to that route
- Completion persisted to `localStorage` — never shown again after first run

---

### Admin Panel

Protected at `/admin/*`. Session must satisfy `is_admin() = true` in Supabase.

> **Important:** The admin layout does **not** call `signOut()` on unauthorized access — it only redirects to `/admin/login`. This prevents destroying the user's `/dashboard` session when navigating between portals.

#### Admin Sections

| Route | Purpose |
|---|---|
| `/admin` | System overview with key operational metrics |
| `/admin/alunos` | Student enrollment: create, approve, deactivate |
| `/admin/clientes` | Customer account management |
| `/admin/equipes` | Team structures and role assignments |
| `/admin/projetos` | Cross-team project tracking |
| `/admin/tarefas` | Task board with GitHub Issues sync |
| `/admin/conversas` | All platform conversations and messages |
| `/admin/blog` | Blog CRUD: create, edit, publish, archive |
| `/admin/depoimentos` | Testimonial moderation (approve/reject) |
| `/admin/feedback` | User feedback review and tagging |
| `/admin/downloads` | Manage downloadable content library |
| `/admin/contato` | Contact form submission inbox |
| `/admin/api-keys` | Platform-level API key management |
| `/admin/api-docs` | Auto-generated API documentation browser |
| `/admin/banco-de-dados` | Database table introspection |
| `/admin/chat-ia` | AI chat conversation logs and usage |
| `/admin/analytics` | Platform-wide analytics: MAU, DAU, retention |
| `/admin/relatorios` | Generated report management |
| `/admin/configuracoes` | Global platform settings |
| `/admin/logs` | Audit log and system event log |

---

### Student Portal

Protected at `/alunos/*`. Requires an active student record in Supabase.

| Route | Purpose |
|---|---|
| `/alunos` | Portal entry and enrollment |
| `/alunos/dashboard` | Student main dashboard |
| `/alunos/dashboard/chat` | Team real-time chat |
| `/alunos/dashboard/equipe` | Team management and member roles |
| `/alunos/dashboard/projetos` | Project showcase and portfolio |
| `/alunos/dashboard/perfil` | Student profile and settings |
| `/alunos/dashboard/notificacoes` | Notification center |

---

## API Reference

All endpoints at `/api/**`. V1 versioned endpoints at `/api/v1/**`. Full OpenAPI spec available at `GET /api/v1/openapi`.

### Analytics Engines

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/api/analytics/monte-carlo` | Run Monte Carlo revenue simulation |
| `POST` | `/api/analytics/churn-ltv` | Churn rate and LTV calculations |
| `POST` | `/api/analytics/break-even` | Break-even point analysis |
| `POST` | `/api/v1/analytics/monte-carlo` | V1 Monte Carlo |
| `POST` | `/api/v1/analytics/churn-ltv` | V1 Churn / LTV |
| `POST` | `/api/v1/analytics/break-even` | V1 Break-even |

### AI

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/api/ai/chat` | Send message to AI assistant |
| `POST` | `/api/ai/generate` | Generate text content |
| `POST` | `/api/nexabrain` | NexaBrain AI integration |
| `POST` | `/api/v1/ai/chat` | V1 AI chat |
| `POST` | `/api/v1/ai/generate` | V1 AI generation |
| `POST` | `/api/chatbot` | Site chatbot |

### User & Authentication

| Method | Endpoint | Description |
|---|---|---|
| `GET/POST` | `/api/profile` | Current user profile |
| `GET/POST/DELETE` | `/api/profiles` | All user profiles |
| `GET/DELETE` | `/api/profiles/[id]` | Single profile |
| `GET` | `/api/v1/me` | Authenticated user info |
| `GET/POST/DELETE` | `/api/v1/me/keys` | User API keys |
| `GET/DELETE` | `/api/v1/me/keys/[id]` | Single API key |
| `POST` | `/api/stats` | User statistics |
| `POST` | `/api/onboarding` | Onboarding data submission |

### Notifications

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/notifications` | User notifications |
| `GET/POST/PUT` | `/api/v1/notifications` | V1 notifications CRUD |
| `GET/DELETE` | `/api/v1/notifications/[id]` | Single notification |

### Blog

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/blog/[slug]` | Fetch post by slug |
| `GET/POST` | `/api/blog/[slug]/comments` | Post comments |
| `POST` | `/api/blog/[slug]/comments/[id]/like` | Like a comment |
| `POST` | `/api/blog/[slug]/like` | Like a post |
| `POST` | `/api/blog/[slug]/view` | Track page view |
| `GET` | `/api/v1/blog` | List all posts (V1) |
| `GET` | `/api/v1/blog/[slug]` | Single post (V1) |

### Communication

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/api/contact` | Contact form submission |
| `POST` | `/api/newsletter` | Newsletter signup |
| `POST` | `/api/feedback` | User feedback |
| `GET/POST` | `/api/conversations` | Conversation list |
| `GET/POST/DELETE` | `/api/conversations/[id]` | Conversation detail |
| `GET/POST` | `/api/conversations/[id]/messages` | Messages in conversation |
| `POST` | `/api/conversations/broadcast` | Broadcast to all users |

### Teams & Projects

| Method | Endpoint | Description |
|---|---|---|
| `GET/POST` | `/api/teams` | Teams CRUD |
| `GET/POST/DELETE` | `/api/teams/[id]` | Team detail |
| `GET/POST` | `/api/testimonials` | Testimonials |
| `GET/DELETE` | `/api/testimonials/[id]` | Single testimonial |

### Students

| Method | Endpoint | Description |
|---|---|---|
| `GET/POST` | `/api/students` | Student list and enrollment |
| `GET/POST/DELETE` | `/api/students/[id]` | Student detail |
| `POST` | `/api/students/register` | Student registration |
| `POST` | `/api/students/site` | Public student listing |
| `GET/POST` | `/api/student-teams` | Student team management |
| `GET/POST/DELETE` | `/api/student-teams/members` | Team membership |
| `GET/POST/DELETE` | `/api/student-projects` | Student projects |

### Tasks & GitHub Sync

| Method | Endpoint | Description |
|---|---|---|
| `GET/POST` | `/api/tasks` | Tasks CRUD |
| `GET/DELETE` | `/api/tasks/[id]` | Task detail |
| `POST` | `/api/tasks/github-sync` | Sync tasks to GitHub Issues |
| `POST` | `/api/tasks/notify` | Task notifications |

### Admin

| Method | Endpoint | Description |
|---|---|---|
| `GET/POST` | `/api/admin/analytics` | System-wide analytics |
| `GET/POST/DELETE` | `/api/admin/api-keys` | Platform API keys |
| `GET/POST/DELETE` | `/api/admin/blog` | Blog management |
| `GET/POST/DELETE` | `/api/admin/downloads` | Downloads management |
| `GET` | `/api/admin/stats` | Detailed system statistics |
| `GET` | `/api/admin/database` | DB introspection |
| `POST` | `/api/admin/testimonials` | Testimonial management |
| `POST` | `/api/admin/me` | Admin profile |
| `GET` | `/api/logs` | Audit and system logs |
| `GET` | `/api/v1/openapi` | Full OpenAPI specification |

---

## Solutions Ecosystem

The `solucoes/` directory contains **eight companion products** that extend BizAnalyticsAI beyond the web platform into desktop, mobile, IDE, and programmatic interfaces.

```
solucoes/
├── desktop/                     ← LTD Hub Desktop (Electron)
├── nexabrain-desktop/           ← NexaBrain Desktop (Electron + Python LLM)
├── agents/                      ← AI Agents Platform (React + Node.js)
│   └── pixel-agents/            ← Pixel art agent visualizer (VS Code)
├── softwares/
│   └── BusinessPlans/           ← BusinessPlans AI (Electron)
├── app/
│   ├── mobile/                  ← Mobile App (React Native / Expo)
│   └── web/                     ← Web App variant
├── extensions/
│   ├── vscode/                  ← VS Code Extension
│   └── web/                     ← Browser Extension
└── libs/
    ├── python/                  ← Python Library (PyPI)
    └── data/                    ← Data utilities
```

---

### 1. LTD Hub Desktop

> **Cross-platform Electron desktop application — the full student and admin portal as a native app.**

| Attribute | Detail |
|---|---|
| **Stack** | Electron 31+, React 18, TypeScript, Tailwind CSS |
| **Platforms** | Windows (`.exe`), macOS (`.dmg`), Linux (`.deb` / `.AppImage`) |
| **Location** | `solucoes/desktop/` |

**Features:**
- Complete student portal UI with offline support
- Team management and project tracking
- Real-time chat and messaging
- Admin control panel
- GitHub project sync
- Auto-update mechanism

**Platform Guides:**
| Guide | File |
|---|---|
| Windows | `desktop/windows-README.md` |
| macOS | `desktop/macos-README.md` |
| Arch Linux | `desktop/archlinux-README.md` |

---

### 2. NexaBrain Desktop

> **Electron application for local AI model training, deployment, and interaction.**

| Attribute | Detail |
|---|---|
| **Stack** | Electron 33+, React, TypeScript, Python (LLM backend) |
| **Platforms** | Windows, macOS, Linux (including Arch) |
| **Location** | `solucoes/nexabrain-desktop/` |
| **Releases** | Pre-built binaries in `nexabrain-desktop/release/` |

**Features:**
- Local LLM inference interface
- Model training and fine-tuning workflow
- Context-aware AI assistant with session management
- Conversation history and context windows
- Cross-platform binary distribution

**Platform Guides:**
| Guide | File |
|---|---|
| Windows | `nexabrain-desktop/windows-README.md` |
| macOS | `nexabrain-desktop/macos-README.md` |
| Linux | `nexabrain-desktop/README-linux.md` |
| Arch Linux | `nexabrain-desktop/README-archlinux.md` |

---

### 3. AI Agents Platform

> **Full-stack operational platform with 35+ autonomous AI agents, real-time orchestration, J.A.R.V.I.S voice interface, and Pixel Office visualization.**

| Layer | Technology |
|---|---|
| **Frontend** | React 18, Vite 5, Tailwind CSS, Recharts, Socket.IO Client |
| **Backend** | Node.js 20+, Express, Socket.IO |
| **Database** | SQLite (`node:sqlite`) |
| **AI** | OpenRouter / OpenAI / Anthropic (configurable per agent) |
| **Voice** | Fish Audio TTS |
| **Email** | Nodemailer + Gmail SMTP |
| **Integration** | GitHub REST + GraphQL (Issues, Projects V2) |
| **Deploy** | Vercel (`vercel.json` included) |
| **Location** | `solucoes/agents/` |

**Features:**
- Real-time agent dashboard with Socket.IO
- Task board with full state machine: `pending → working → completed / failed`
- Individual agent status, performance metrics, and delegation log
- J.A.R.V.I.S voice assistant with TTS
- **Pixel Office** — multi-floor virtual office with animated pixel art agents (can be displayed inside VS Code via `pixel-agents/`)
- GitHub Issues and Projects V2 bidirectional sync
- Admin controls: force sync, reset stuck agents, broadcast tasks

---

### 4. BusinessPlans AI

> **Standalone Electron desktop app for AI-powered business plan generation — works fully offline.**

| Attribute | Detail |
|---|---|
| **Stack** | Electron, React, TypeScript, Tailwind CSS |
| **Location** | `solucoes/softwares/BusinessPlans/` |
| **Binaries** | `dist/` — Windows (`.exe`), macOS (`.dmg`), Linux (`.deb`, `.AppImage`) |

**Features:**
- Guided AI-powered business plan wizard (section by section)
- AI text generation at each plan section
- Export to PDF and Word
- Fully offline with local storage
- Import from web dashboard (Supabase sync)

---

### 5. Mobile App

> **React Native / Expo mobile application for iOS and Android.**

**Location:** `solucoes/app/mobile/`

**Features:**
- Full BizAnalyticsAI dashboard experience on mobile
- Push notifications via Expo
- Biometric authentication (Face ID / fingerprint)
- Offline data synchronization
- Native charts and visualizations

---

### 6. VS Code Extension

> **LTD Hub VS Code extension — project management, analytics, and team features inside the IDE.**

**Location:** `solucoes/extensions/vscode/`

Also available: `solucoes/agents/pixel-agents/` — visualizes the AI Agents platform characters as animated pixel art directly within VS Code while Claude Code runs.

**Features:**
- Project tracking and task board panel
- Team presence indicators
- Direct Supabase integration
- AI code insights
- Keyboard shortcuts for common workflows

---

### 7. Browser Extension

> **Web browser extension for BizAnalyticsAI productivity and market intelligence tools.**

**Location:** `solucoes/extensions/web/`

**Features:**
- Quick-access popup with dashboard metrics
- Page annotation with business insights
- Market data overlay on competitor pages
- Lead capture integration
- Sync with web dashboard

---

### 8. Python Library

> **PyPI-compatible library for programmatic access to BizAnalyticsAI analytics engines.**

**Location:** `solucoes/libs/python/`

**Features:**
- Monte Carlo revenue simulation
- Churn rate and LTV analysis
- Break-even calculation toolkit
- Pandas DataFrame and CSV connectors
- Full REST API client wrapper

```python
from bizanalyticsai import MonteCarloSimulator, ChurnAnalyzer

# Run 10,000 Monte Carlo scenarios
sim = MonteCarloSimulator(iterations=10_000)
result = sim.run(
    revenue=50_000,
    growth_rate=0.08,
    volatility=0.15
)
print(f"P90 annual revenue: R$ {result.percentile(90):,.0f}")

# Churn and LTV analysis
churn = ChurnAnalyzer()
ltv = churn.calculate_ltv(
    arpu=299,
    churn_rate=0.035,
    gross_margin=0.72
)
print(f"Customer LTV: R$ {ltv:,.0f}")
```

---

## Database Schema

Built on **Supabase (PostgreSQL)** with Row Level Security enabled on all tables. Users can only read and write their own data. Admin access is enforced via `is_admin()` `SECURITY DEFINER` functions that bypass RLS safely.

### Core User Tables

| Table | Primary Key | RLS Scope | Description |
|---|---|---|---|
| `profiles` | `user_id` | Per-user | Extended profiles with business data |
| `business_plans` | `id` | Per-user | Saved business plan documents |
| `business_profiles` | `user_id` | Per-user | Onboarding business configuration |
| `user_dashboard_settings` | `user_id` | Per-user | White-label preferences (colors, layout, branding) |
| `notifications` | `id` | Per-user | User notification records |
| `user_api_keys` | `id` | Per-user | User-generated API keys |

### Content Tables

| Table | Description |
|---|---|
| `blog_posts` | Articles — title, slug, markdown body, published_at |
| `blog_comments` | Nested comment threads with like counts |
| `blog_likes` | Post like tracking (user_id + post_id) |
| `testimonials` | Customer testimonials with moderation status |
| `downloads` | Downloadable resource metadata |
| `newsletter_subscribers` | Email subscription list |
| `contact_messages` | Contact form submissions |
| `feedback` | User satisfaction feedback |

### Organization & Multi-Tenancy Tables

| Table | Description |
|---|---|
| `organizations` | Multi-tenant organization accounts |
| `organization_members` | Membership with roles: `owner`, `admin`, `member` |
| `white_label_configs` | Org-level white-label brand configuration |
| `white_label_pages` | Custom organization pages |
| `white_label_audit_log` | Change audit trail for org settings |

### Team & Project Tables

| Table | Description |
|---|---|
| `teams` | Team definitions |
| `team_members` | Team composition with role assignment |
| `projects` | Project records linked to teams |
| `tasks` | Task management with GitHub Issues sync |

### Student Tables

| Table | Description |
|---|---|
| `students` | Enrolled student records |
| `student_teams` | Student team groupings |
| `student_team_members` | Team composition |
| `student_projects` | Student project portfolio entries |
| `student_registration_keys` | Single-use enrollment codes |

### System Tables

| Table | Description |
|---|---|
| `admin_users` | Admin account records |
| `system_logs` | Audit and error log entries |
| `conversations` | Chat session records |
| `conversation_messages` | Individual messages in a conversation |
| `ai_usage_logs` | AI model invocation tracking |
| `security_sessions` | Active session management |

### Database Functions

```sql
-- Security functions (SECURITY DEFINER — bypass RLS safely)
is_admin()                           -- TRUE if calling user has admin role
is_org_owner(p_org_id UUID)          -- TRUE if calling user owns the org
is_org_member(p_org_id UUID)         -- TRUE if calling user is a member
is_org_admin_member(p_org_id UUID)   -- TRUE if calling user is org admin
get_my_organization()                -- Returns the caller's organization row
is_organization_slug_available(slug) -- TRUE if slug is not taken
handle_updated_at()                  -- Trigger: auto-update updated_at column
create_organization(name, slug)      -- Creates org + owner member + white-label config
```

### Migrations Reference

```
supabase/migrations/
├── 20260403_business_profiles.sql
├── 20260403_fix_business_plans_rls.sql
├── 20260403_white_label_foundation.sql
├── 20260403_white_label_rls_fix.sql
├── 20260405_user_dashboard_settings.sql
├── 20260405_fix_user_dashboard_settings_nulls.sql
└── backup/
    ├── 000_complete_schema.sql        ← Master schema reference
    ├── 001_admin_system.sql
    ├── 002_constraints_and_tables.sql
    ├── 003_admin_function.sql
    ├── 004_count_functions.sql
    ├── 005_is_admin_function.sql
    ├── 006_fix_rls_policies.sql
    ├── 007_feedback_table.sql
    ├── 008_downloads_table.sql
    ├── 009_seed_admin.sql
    ├── 010_newsletter.sql
    ├── 011_blog.sql
    ├── 012_tasks.sql
    ├── 013_teams_sector.sql
    ├── 014_students.sql
    ├── 015_chat.sql
    ├── 016_user_api_keys.sql
    └── ...20+ additional schema files
```

---

## Internationalization

The platform ships with full multilingual support across all user-facing strings.

| Locale | Language | Default |
|---|---|---|
| `pt-BR` | Portuguese (Brazil) | ✅ |
| `en-US` | English (United States) | — |
| `es-ES` | Spanish (Spain) | — |

### Detection Order

```
1. NEXT_LOCALE cookie       ← set by LanguageSwitcher, persists 1 year
2. Accept-Language header   ← browser preference
3. Default: pt-BR
```

No URL prefixes — locale is transparent to the user. The `LanguageSwitcher` component offers two display variants:
- `variant="navbar"` — full flag + label for desktop navigation
- `variant="compact"` — icon-only for dashboard header and mobile

### Coverage

All translation keys live in `messages/pt-BR.json`, `messages/en-US.json`, and `messages/es-ES.json`:

- Navigation labels and page titles
- Dashboard module names and descriptions
- Form labels, placeholders, and validation messages
- Toast notifications and error messages
- Onboarding tutorial steps
- Legal page content
- CTA buttons and marketing copy

---

## White-Label Customization

Every user can independently customize the look and feel of their dashboard. Settings are stored in `user_dashboard_settings` in Supabase and are **fully isolated per account** — changes made by one user never affect any other user.

### Customization Options

| Tab | Options |
|---|---|
| **Identidade** | Platform name (replaces "BizAnalyticsAI"), logo URL |
| **Cores** | Accent color, primary color, background, sidebar, cards, text |
| **Navegação** | Sidebar item order (↑↓), show/hide individual items |
| **Visual** | Border radius (Sharp / Rounded / Pill), 6 preset color palettes |

### Live Preview

The settings page includes a live preview panel (right column, sticky) that reflects all changes in real-time — simulated sidebar, card, and button — before the user clicks "Salvar alterações".

### Technical Implementation

```typescript
// Per-user cache key — prevents settings leaking between accounts
const cacheKey = (userId: string) =>
  `bizanalytics_dash_settings_${userId}`;

// Applied to :root CSS custom properties
applyToDom(settings);
// Maps to: --accent · --ring · --background · --sidebar · --card
//          --foreground · --radius

// On logout: CSS vars are removed from :root
resetDom();

// On login of a different user: resetDom() before applying new settings
```

### Isolation Guarantees

- `useState` always initializes with `DEFAULT_SETTINGS` — never reads localStorage before knowing the user ID
- localStorage cache key includes the user ID
- `resetDom()` called on every login to clear previous user's CSS vars
- Supabase RLS enforces that `user_dashboard_settings` rows are only accessible by their owner
- Logout clears CSS vars from `:root`

---

## eBooks Library

The platform includes a library of professionally designed, LaTeX-typeset eBooks available to users in the Downloads section.

| Title | Topics |
|---|---|
| **Análise de Churn e LTV** | Churn modeling (5 parts, 20 sections, 33 colored boxes, 9 formulas), LTV calculation, retention playbooks, cohort analysis |
| **Análise de Mercado: Guia Prático** | TAM/SAM/SOM, Porter's Five Forces, PESTEL, value chain, competitive mapping, JTBD, buyer behavior, forecasting, beachhead market, validation hierarchy |
| **KPIs que Importam para Startups** | Key metrics by stage, OKR framework, tracking implementation |
| **Monte Carlo para Empreendedores** | Financial simulation theory, uncertainty modeling, scenario planning |
| **Tendências em IA 2025** | AI landscape, generative AI, business applications, strategic roadmap |
| **Viabilidade Financeira Descomplicada** | Break-even, payback, unit economics, SaaS financial modeling |
| **Guia Completo de Plano de Negócios 2025** | Full plan methodology: executive summary through financial projections |

All eBooks are:
- 100% **self-contained** LaTeX (no external style file dependencies)
- Professionally designed with `tcolorbox` colored boxes, formulas, and tables
- Available as PDF in `docs/latex/pdf/`
- Gated behind the download center for lead capture on the public site

---

## PWA Support

BizAnalyticsAI is a full Progressive Web App — installable on desktop and mobile.

| Feature | Implementation |
|---|---|
| **Service Worker** | `public/sw.js` — caching strategy for offline support |
| **Web App Manifest** | `public/manifest.json` — name, icons, theme, display mode |
| **Offline Fallback** | `/app/offline/page.tsx` — custom branded offline page |
| **iOS Icon** | `public/apple-icon.png` — `apple-touch-icon` |
| **PWA Registration** | `components/pwa-register.tsx` — registers SW on first mount |
| **Favicons** | `icon.svg`, `icon-light-32x32.png`, `icon-dark-32x32.png` |

---

## Getting Started

### Prerequisites

- **Node.js** ≥ 20
- **npm** ≥ 10
- **Supabase** project (free tier is sufficient for development)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/your-org/bizanalyticsai.git
cd bizanalyticsai

# 2. Install dependencies
npm install

# 3. Configure environment
cp .env.example .env.local
# Edit .env.local with your Supabase credentials and API keys

# 4. Set up the database
# Go to your Supabase project → SQL Editor
# Run each file in supabase/migrations/ in chronological order
# Or: supabase db push (if using Supabase CLI)

# 5. Start the development server
npm run dev
# → http://localhost:3000
```

### Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Start development server with Hot Module Replacement |
| `npm run build` | Build optimized production bundle |
| `npm run start` | Serve production build locally |
| `npm run lint` | Run ESLint across the codebase |

---

## Environment Variables

Create a `.env.local` file in the project root:

```env
# ── Supabase ─────────────────────────────────────────────────────────
NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key
SUPABASE_SERVICE_ROLE_KEY=your-service-role-key

# ── AI Providers ─────────────────────────────────────────────────────
OPENAI_API_KEY=sk-...
ANTHROPIC_API_KEY=sk-ant-...
OPENROUTER_API_KEY=sk-or-...

# ── Email (Nodemailer) ────────────────────────────────────────────────
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your@email.com
EMAIL_PASS=your-app-password

# ── GitHub Integration (Tasks sync — optional) ────────────────────────
GITHUB_TOKEN=ghp_...
GITHUB_OWNER=your-org
GITHUB_REPO=your-repo

# ── App ──────────────────────────────────────────────────────────────
NEXT_PUBLIC_APP_URL=https://bizanalyticsai.com.br
```

---

## Deployment

### Vercel (Recommended)

Connect the GitHub repository to Vercel for automatic production deployments on every push to `main`.

```bash
# One-time setup via CLI
npm i -g vercel
vercel --prod
```

**Vercel configuration:**
- Framework preset: **Next.js** (auto-detected)
- Node.js version: **20.x**
- Add all environment variables in **Project Settings → Environment Variables**
- Set **Production** and **Preview** environments separately

### Supabase

1. Create a project at [supabase.com](https://supabase.com)
2. Open **SQL Editor** and run each migration in `supabase/migrations/` in order
3. Enable **Row Level Security** on all tables (migrations handle this)
4. In **Authentication → URL Configuration**, add your Vercel domain to Redirect URLs
5. Copy your **Project URL** and **anon key** to `.env.local`

---

## Project Structure

```
bizanalyticsai/
├── app/                             # Next.js App Router (all routes)
│   ├── (public)/                    # Public site (Navbar + Footer layout)
│   │   ├── layout.tsx
│   │   ├── page.tsx                 # Homepage
│   │   ├── login/
│   │   ├── registro/
│   │   ├── blog/[slug]/
│   │   ├── solucoes/
│   │   └── ...30+ public pages
│   ├── (dashboard)/                 # User portal (Sidebar layout)
│   │   ├── layout.tsx               # Sidebar + header + customization context
│   │   └── dashboard/
│   │       ├── page.tsx             # Overview
│   │       ├── plano-negocios/
│   │       ├── analise-preditiva/
│   │       ├── white-label/         # Per-user customization
│   │       └── ...17 feature routes
│   ├── admin/                       # Admin panel
│   │   ├── layout.tsx               # Admin auth guard
│   │   └── ...20 admin routes
│   ├── (students)/                  # Student portal
│   │   └── alunos/
│   ├── api/                         # API endpoints
│   │   ├── analytics/               # Monte Carlo, Churn/LTV, Break-even
│   │   ├── ai/                      # Chat, generate
│   │   ├── blog/                    # CRUD + comments + likes
│   │   ├── admin/                   # Admin-only endpoints
│   │   ├── v1/                      # Versioned API
│   │   └── ...60+ routes
│   ├── offline/                     # PWA offline page
│   └── layout.tsx                   # Root layout (theme + i18n + analytics)
│
├── components/
│   ├── ui/                          # 40+ Radix UI + shadcn components
│   ├── dashboard/                   # Dashboard-specific components
│   │   ├── onboarding-tutorial.tsx  # 20-step first-time guide
│   │   ├── charts/                  # Recharts wrappers
│   │   └── sections/                # Page sections (pipeline, reports...)
│   └── site/                        # Public site components
│       ├── navbar.tsx               # Mega-menu navbar
│       ├── footer.tsx
│       └── ai-chatbot.tsx
│
├── hooks/
│   ├── use-dashboard-customization.ts  # White-label context + Supabase sync
│   ├── use-business-profile.ts
│   ├── use-mobile.ts
│   └── use-toast.ts
│
├── lib/
│   ├── utils.ts                     # cn() (clsx + twMerge)
│   ├── api-auth.ts                  # API auth helpers
│   ├── export-utils.ts              # PDF / CSV export
│   ├── openapi.ts                   # OpenAPI spec generation
│   └── supabase/
│       ├── client.ts                # Browser Supabase client
│       ├── server.ts                # Server Supabase client
│       └── middleware.ts            # Optimized auth middleware
│
├── types/
│   └── admin.ts                     # Full TypeScript interface library
│
├── messages/
│   ├── pt-BR.json                   # Portuguese — default
│   ├── en-US.json                   # English
│   └── es-ES.json                   # Spanish
│
├── i18n/
│   ├── routing.ts                   # Locale list and default
│   └── request.ts                   # Server-side locale detection
│
├── supabase/
│   └── migrations/                  # PostgreSQL schema + RLS policies
│
├── public/
│   ├── logo.png
│   ├── manifest.json                # PWA manifest
│   ├── sw.js                        # Service worker
│   └── apple-icon.png
│
├── solucoes/                        # 8 companion products
│   ├── README.md                    # Ecosystem overview
│   ├── desktop/                     # LTD Hub Desktop
│   ├── nexabrain-desktop/           # NexaBrain Desktop
│   ├── agents/                      # AI Agents Platform
│   ├── app/mobile/                  # Mobile App
│   ├── softwares/BusinessPlans/     # BusinessPlans AI
│   ├── extensions/vscode/           # VS Code Extension
│   ├── extensions/web/              # Browser Extension
│   └── libs/python/                 # Python Library
│
├── docs/
│   ├── DEVELOPERS.md                # Developer reference guide
│   ├── stack.md                     # Tech stack notes
│   └── latex/                       # eBook LaTeX source files
│       └── pdf/                     # Compiled eBook PDFs
│
├── scripts/                         # GitHub task automation scripts
├── middleware.ts                    # Next.js edge middleware (auth guard)
├── next.config.mjs                  # Next.js configuration
├── postcss.config.mjs               # PostCSS + Tailwind pipeline
└── tsconfig.json                    # TypeScript configuration
```

---

<div align="center">

**Built with precision by the LTD — Laboratório de Tecnologia e Desenvolvimento.**

[![Website](https://img.shields.io/badge/bizanalyticsai.com.br-7c3aed?style=for-the-badge&logo=googlechrome&logoColor=white)](https://bizanalyticsai.com.br)

*BizAnalyticsAI — Intelligence that drives decisions.*

</div>
