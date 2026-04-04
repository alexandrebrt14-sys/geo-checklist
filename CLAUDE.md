# CLAUDE.md

## REGRA #0 — IDIOMA (MANDATÓRIA, INVIOLÁVEL)

**TODO conteúdo produzido neste repositório DEVE ser em Português do Brasil (pt-BR) com ortografia correta e acentuação completa.**

Proibido: texto sem acentos ("nao" em vez de "não", "voce" em vez de "você").
Exceção: código em inglês, mensagens de commit em inglês, artigos DEV.to/Hashnode em inglês.

---

# CLAUDE.md — Workspace alexandrecaramaschi.com + brasilgeo.ai

## Identidade do Projeto

Este workspace contém dois projetos independentes de Alexandre Caramaschi:
- **alexandrecaramaschi.com** → `landing-page-geo/` (Next.js 16, Vercel)
- **brasilgeo.ai** → `brasilgeo-worker/` (Cloudflare Workers)

O proprietário é Alexandre Caramaschi, CEO da Brasil GEO.

## Regras Obrigatórias

### Sem Emojis
Proibido emojis em qualquer conteúdo ou documentação.

### Naming (NUNCA usar)
- "Especialista #1" — proibido em qualquer contexto
- "GEO Brasil" — ordem errada; correto: "Brasil GEO"
- "Source Rank" — nome legado
- sourcerank.ai ou geobrasil.com.br — domínios legados

### Credential Canônico (usar sempre)
```
CEO da Brasil GEO, ex-CMO da Semantix (Nasdaq), cofundador da AI Brasil
```

### Contato
- WhatsApp: +55 62 99187-7534
- Email: caramaschiai@caramaschiai.io
- Email pessoal: alexandre.brt14@gmail.com

## API Keys
Fonte de verdade: C:/Sandyboxclaude/geo-orchestrator/.env

## Stack Técnico

### alexandrecaramaschi.com
- Next.js 16 + React 19 + TypeScript
- Tailwind CSS 4 (CSS variables em globals.css)
- Framer Motion (animações)
- Sonner (toasts)
- Vercel (deploy automático on push to master)
- GA4: G-3N78Z8ZV5F
- Clarity: vyojp0isv3
- Design system: Salesforce/Lucida (variáveis em globals.css)

### brasilgeo.ai
- Cloudflare Workers (worker-fixed.js)
- Static assets (44 arquivos)
- GA4: G-BW1Q4NYD3E + G-8T7V16FM4T
- Deploy: npx wrangler deploy --name brasilgeo

## Comandos Rápidos

```bash
# Landing page (alexandrecaramaschi.com)
cd C:/Sandyboxclaude/landing-page-geo
npm run dev          # Dev server porta 3000
npx next build       # Build de produção
git push origin master  # Deploy automático no Vercel

# brasilgeo.ai
cd C:/Sandyboxclaude/brasilgeo-worker
npx wrangler deploy --name brasilgeo  # Deploy no Cloudflare

# Submeter para indexação (após deploy)
curl -X POST "https://api.indexnow.org/indexnow" \
  -H "Content-Type: application/json" \
  -d '{"host":"alexandrecaramaschi.com","key":"b8e4a2c7f1d94e5fa3b6d8e0c2a7f1e4","urlList":["https://alexandrecaramaschi.com/"]}'

# GitHub repos open-source (branch main, não master)
cd C:/Sandyboxclaude/geo-checklist && git push origin main
cd C:/Sandyboxclaude/llms-txt-templates && git push origin main
cd C:/Sandyboxclaude/entity-consistency-playbook && git push origin main
cd C:/Sandyboxclaude/geo-taxonomy && git push origin main
```

## Estrutura de Componentes (landing-page-geo)

```
src/components/
├── AnimateIn.tsx          # Framer Motion wrapper (fade-in on scroll)
├── AnimatedCounter.tsx    # Number animation on viewport entry
├── ArticlesSection.tsx    # Featured articles grid
├── AudienceSection.tsx    # Target audience (B2B + Creators)
├── AuthorSection.tsx      # Alexandre bio + credentials
├── BigQuote.tsx           # Dark section with stats
├── BrasilGeoSection.tsx   # Platform + community
├── Breadcrumbs.tsx        # Reusable breadcrumbs + JSON-LD
├── ContactFormSection.tsx # Contact form
├── CtaSection.tsx         # Final CTA (dark bg)
├── FaqSection.tsx         # Accordion FAQ (Framer Motion)
├── Footer.tsx             # Newsletter + links + social
├── Hero.tsx               # Main hero (pain-focused copy)
├── JsonLd.tsx             # 29 Schema.org types
├── PricingSection.tsx     # 4-tier pricing
├── ProblemSection.tsx     # 3 problem cards
├── ReadingProgress.tsx    # Progress bar + ScrollToTop
├── RoiCalculator.tsx      # Interactive ROI calculator
├── ScopeSection.tsx       # Sprint deliverables
├── SocialProofSection.tsx # Stats + testimonial carousel
├── TestimonialCarousel.tsx # Auto-advancing carousel
├── TimelineSection.tsx    # Sprint timeline
├── Topbar.tsx             # Sticky navigation
├── TransformationSection.tsx # Before/after comparison
├── UrgencyBar.tsx         # Top urgency bar
└── WhatsAppFloat.tsx      # Floating WhatsApp button
```

## Páginas (src/app/)

### Principais
/ → Home (conversion landing page)
/sobre → About Alexandre
/conteudos → Content hub (7 pilares HBR/MIT Sloan)
/insights → 25 editorial insights
/artefacto → Hub de conhecimento (Guias, FAQs, Frameworks)
/busca → Internal search
/mapa-do-site → HTML sitemap
/metodologia → Sprint GEO methodology
/cases → Case studies
/podcast → GEO Talk podcast
/talks → Speaking engagements
/research → Publications
/press-kit → Media kit
/como-aparecer-no-chatgpt → ChatGPT visibility guide
/business-to-agent → B2A concept

### Subpáginas
/insights/{slug} → 25 insight pages
/artigos/{slug} → 21 dynamic articles (via src/lib/articles.ts)
/artefacto/faq/{slug} → 3 FAQ pages
/artefacto/guia/{slug} → 3+ guide pages

## Contas e Acessos

| Plataforma | Email | Papel |
|---|---|---|
| GitHub | alexandre.brt14@gmail.com | Owner |
| Vercel | via GitHub OAuth | Admin |
| GA4 (AC) | caramaschiai@caramaschiai.io | Admin |
| GA4 (AC) | alexandre.brt14@gmail.com | Admin |
| GA4 (BG) | geobbrasil@gmail.com | Admin |
| Clarity | caramaschiai@caramaschiai.io | Admin |
| Clarity | alexandre.brt14@gmail.com | Admin |
| Cloudflare | ti@brasilgeo.ai | Admin |
| Hostinger | bbrasilgeo@gmail.com | Owner |

## Padrões de Código

### Botões — SEMPRE usar inline style para cor do texto
```tsx
// Botão com fundo colorido → texto branco garantido
<a className="sf-btn-primary" style={{ color: '#ffffff' }}>Texto</a>

// Botão com fundo branco → texto escuro garantido
<a className="sf-btn-outline" style={{ color: '#181818' }}>Texto</a>
```

### Seções — Alternar backgrounds
```
Seção 1: bg-white (branco)
Seção 2: bg-[var(--bg-muted)] (cinza #f3f3f3)
Seção 3: bg-white
...etc
```

### Labels de seção
```tsx
<p className="sf-label mb-2">TEXTO EM CAPS</p>
```

### Animações de scroll
```tsx
import AnimateIn from "@/components/AnimateIn";
<AnimateIn><h2>Heading</h2></AnimateIn>
<AnimateIn delay={0.2}><div>Content</div></AnimateIn>
```

### Cores principais (CSS vars)
```
--accent: #0176d3 (Salesforce blue)
--accent-dark: #014486
--success: #2e844a (green buttons)
--card-dark: #032d60 (navy sections)
--text: #181818
--text-muted: #444444
--border: #d8d8d8
--bg-muted: #f3f3f3
--radius: 8px
```

## Logs e Referência

- Auditoria completa: `C:\Sandyboxclaude\AUDITORIA_COMPLETA_SESSAO_2026-03-21_V2.txt`
- PDFs GEO: `C:\Sandyboxclaude\GEO Brasil Fevereiro\GEO\` (53 PDFs)
- Prompts operacionais: `C:\Sandyboxclaude\Logss\prompts_claude_geo_alexandre_caramaschi.md`
- Inventário unificado: `C:\Sandyboxclaude\Logss\INVENTARIO_UNIFICADO_BRASILGEO_2026-03-21.txt`

## Workflow Padrão

1. **Antes de editar**: Sempre `Read` o arquivo primeiro
2. **Após editar**: `npx next build` para validar
3. **Para deploy**: `git add -A && git commit && git push origin master`
4. **Após deploy**: Submeter URLs ao IndexNow
5. **Para subpáginas**: Usar Breadcrumbs component
6. **Para novos insights**: Criar em /insights/{slug}/page.tsx + adicionar ao index
7. **Para copy**: Foco na DOR do empresário (tráfego caindo, IA invisível)
