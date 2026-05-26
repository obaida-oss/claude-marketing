# Claude Marketing

A marketing co-founder for any project, powered by Claude Code.

## What This Is

A plug-and-play marketing system for Claude Code. Drop it into any project and get:
- 29 expert marketing skills (cold email, SEO, social content, CRO, launch strategy, etc.)
- 51 CLI tools for marketing platforms (Apollo, HubSpot, Instantly, Buffer, etc.)
- Ready-to-use slash commands (`/marketing`, `/content-batch`, `/cold-emails`, `/crm`)
- Cold email templates, content calendar structure, pipeline tracking
- Product marketing context framework that all skills reference

## How to Use

### 1. Set Up Your Product Context
Run `/setup-context` or manually create `.claude/product-marketing-context.md` in your project. This captures your product, audience, positioning, and voice. All marketing skills reference it automatically.

### 2. Run Marketing Commands
| Command | What It Does |
|---------|-------------|
| `/setup-context` | Create your product marketing context (run this first) |
| `/marketing` | Execute today's highest-priority marketing task |
| `/content-batch` | Generate a full week of social content |
| `/cold-emails` | Write cold email sequences |
| `/crm` | Manage your sales pipeline |
| `/launch` | Plan a product launch |
| `/seo` | Run an SEO audit |

### 3. Use Marketing Skills
Skills are loaded automatically when relevant. You can also reference them directly:
- "Write a cold email for my SaaS product" → uses `cold-email` skill
- "Create social content for this week" → uses `social-content` skill
- "Audit my landing page for conversions" → uses `page-cro` skill

## Structure
```
claude-marketing/
├── CLAUDE.md                  # This file
├── .claude/
│   └── commands/              # Slash commands
│       ├── setup-context.md   # Set up product marketing context
│       ├── marketing.md       # Daily marketing co-founder
│       ├── content-batch.md   # Weekly content generation
│       ├── cold-emails.md     # Cold email sequence writing
│       ├── crm.md             # Pipeline management
│       ├── launch.md          # Launch planning
│       └── seo.md             # SEO audit
├── skills/                    # 29 marketing skills
├── tools/                     # 51 CLI tools + integration guides
├── templates/
│   ├── cold-emails/           # Cold email sequence templates
│   └── email-sequences/       # Lifecycle email templates
├── marketing/
│   ├── TRACKER.md             # Pipeline + metrics tracker (template)
│   └── content/               # Generated content goes here
└── docs/
    ├── SETUP.md               # Full setup guide
    ├── MARKETING-STACK.md     # Recommended tool stack
    └── SKILLS-REFERENCE.md    # All 29 skills explained
```

## Skills Available (29)

**Conversion Optimization**: page-cro, signup-flow-cro, onboarding-cro, form-cro, popup-cro, paywall-upgrade-cro

**Content & Copy**: copywriting, copy-editing, cold-email, email-sequence, social-content, content-strategy

**SEO & Discovery**: seo-audit, ai-seo, programmatic-seo, competitor-alternatives, schema-markup

**Paid & Distribution**: paid-ads, ad-creative

**Measurement & Testing**: analytics-tracking, ab-test-setup

**Retention**: churn-prevention

**Growth & Strategy**: free-tool-strategy, referral-program, marketing-ideas, marketing-psychology, launch-strategy, pricing-strategy, product-marketing-context

## CLI Tools (51)

Zero-dependency Node.js CLIs for marketing platforms. Set `{TOOL}_API_KEY` env var and go.

See `tools/REGISTRY.md` for the full list.

## Requirements
- Claude Code
- Node.js 18+ (for CLI tools)


## Skills Detail

### Conversion Optimization

**page-cro** — Optimize any marketing page (homepage, landing, pricing, feature) to improve conversion rates. Use when the user says "CRO," "this page isn't converting," or "improve conversions."

**signup-flow-cro** — Optimize the signup or registration flow. Use when the conversion issue is inside the signup process itself (forms, steps, friction).

**onboarding-cro** — Improve post-signup activation and onboarding. Use when users sign up but don't activate or reach the "aha moment."

**form-cro** — Optimize forms (contact, lead gen, checkout) outside of signup flows. Reduce abandonment and improve completion rates.

**popup-cro** — Design and optimize popups, modals, and overlays. Use for exit-intent, email capture, upgrade prompts, and announcements.

**paywall-upgrade-cro** — Improve free-to-paid conversion on paywalls and upgrade prompts. Use when users aren't converting from free to paid plans.

### Content & Copy

**copywriting** — Write or rewrite marketing copy for any page: homepage, landing pages, pricing, feature, about. Use for headlines, subheadlines, body copy, and CTAs. For email copy use email-sequence.

**copy-editing** — Polish and improve existing copy line-by-line. Use after a draft is written to tighten, clarify, and strengthen.

**cold-email** — Write B2B cold email sequences that get replies. Covers subject lines, opening lines, personalization, CTAs, and multi-touch follow-up sequences.

**email-sequence** — Write lifecycle and nurture email sequences (welcome, onboarding, re-engagement, promotional). Not for cold outreach — use cold-email for that.

**social-content** — Create social media content for Twitter/X, LinkedIn, Reddit, and other platforms. Use for individual posts or full content calendars.

**content-strategy** — Develop a content marketing strategy: topics, formats, channels, publishing cadence, and distribution plan.

### SEO & Discovery

**seo-audit** — Audit a website for SEO issues: technical SEO, on-page optimization, content quality, crawlability, and Core Web Vitals. Use when the user says "SEO audit" or "why am I not ranking."

**ai-seo** — Optimize content for AI search engines and answer engines (AEO, GEO, LLMO, AI Overviews, ChatGPT). Use when the user wants visibility in AI-generated answers.

**programmatic-seo** — Build SEO page templates at scale to target long-tail keywords. Use for location pages, comparison pages, use-case pages, or any repeatable page pattern.

**competitor-alternatives** — Create "[Competitor] alternative" and comparison pages to capture high-intent search traffic from people evaluating competing products.

**schema-markup** — Implement structured data (JSON-LD) to enable rich results in search: FAQPage, HowTo, Product, Review, Organization, and more.

### Paid & Distribution

**paid-ads** — Plan, write, and optimize paid advertising campaigns (Google Ads, Meta, LinkedIn). Covers campaign structure, targeting, bidding, and copy.

**ad-creative** — Write ad creative copy and concepts for paid social and display ads. Includes headlines, descriptions, and creative direction.

### Measurement & Testing

**analytics-tracking** — Set up and audit analytics tracking: GA4 events, conversion tracking, funnel analysis, and KPI dashboards.

**ab-test-setup** — Design and set up A/B tests properly: hypothesis, variants, sample size, duration, success metrics, and statistical significance.

### Retention

**churn-prevention** — Identify churn signals and create interventions: win-back campaigns, at-risk user outreach, cancellation flows, and retention offers.

### Growth & Strategy

**free-tool-strategy** — Plan and build free tools as a growth channel: tool ideation, SEO value, viral mechanics, and conversion paths.

**referral-program** — Design a referral program: incentive structure, mechanics, copy, and launch plan.

**marketing-ideas** — Generate creative marketing ideas and campaigns tailored to the product, audience, and growth stage.

**marketing-psychology** — Apply behavioral psychology principles to marketing: social proof, scarcity, anchoring, reciprocity, and loss aversion.

**launch-strategy** — Plan a product or feature launch: pre-launch buildup, launch day execution, post-launch follow-through, and channel strategy.

**pricing-strategy** — Develop or improve pricing: packaging, plan structure, price points, anchoring, and upgrade paths.

**product-marketing-context** — Establish and maintain the foundational product marketing context: positioning, ICP, value props, messaging, and competitive landscape. All other skills reference this context.
