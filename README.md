# Claude Marketing

A plug-and-play marketing co-founder for Claude Code. Drop it into any project and get an AI marketing team.

## What's Inside

- **29 marketing skills** — cold email, social content, SEO, CRO, launch strategy, pricing, referral programs, and more
- **51 CLI tools** — zero-dependency Node.js CLIs for Apollo, HubSpot, Instantly, Buffer, Klaviyo, GA4, Stripe, and 40+ more
- **7 slash commands** — `/marketing`, `/content-batch`, `/cold-emails`, `/crm`, `/launch`, `/seo`, `/setup-context`
- **Cold email templates** — primary outreach, high-intent, partnership sequences
- **Pipeline tracker** — lead tracking, content metrics, weekly review
- **Marketing stack guide** — HubSpot + Apollo + Instantly setup with API examples

## Quick Start

### 1. Clone into your project

```bash
cd your-project/

# Clone
git clone https://github.com/YOUR_USERNAME/claude-marketing.git .claude-marketing

# Copy commands into your .claude/
mkdir -p .claude/commands
cp .claude-marketing/.claude/commands/* .claude/commands/

# Copy skills and tools
cp -r .claude-marketing/skills .claude/skills
cp -r .claude-marketing/tools .claude/tools

# Copy templates and marketing tracker
cp -r .claude-marketing/templates ./templates
cp -r .claude-marketing/marketing ./marketing
```

### 2. Set up your product context

Open your project in Claude Code and run:

```
/setup-context
```

This creates `.claude/product-marketing-context.md` — the foundation all marketing skills reference. Takes 10 minutes.

### 3. Generate content

```
/content-batch
```

Generates a full week: 7 tweets, 2 LinkedIn posts, 3 Reddit answers — all tailored to your product.

### 4. Write cold emails

```
/cold-emails
```

Generates 3 email sequences customized to your audience.

## Commands

| Command | What It Does |
|---------|-------------|
| `/setup-context` | Create your product marketing context (run first) |
| `/marketing` | Execute today's highest-priority marketing task |
| `/content-batch` | Generate a full week of social content |
| `/cold-emails` | Write cold email sequences |
| `/crm` | Manage your sales pipeline |
| `/launch` | Plan a product launch |
| `/seo` | Run an SEO audit |

## Skills (29)

| Category | Skills |
|----------|--------|
| **Conversion** | page-cro, signup-flow-cro, onboarding-cro, form-cro, popup-cro, paywall-upgrade-cro |
| **Content** | copywriting, copy-editing, cold-email, email-sequence, social-content, content-strategy |
| **SEO** | seo-audit, ai-seo, programmatic-seo, competitor-alternatives, schema-markup |
| **Ads** | paid-ads, ad-creative |
| **Analytics** | analytics-tracking, ab-test-setup |
| **Retention** | churn-prevention |
| **Growth** | free-tool-strategy, referral-program, marketing-ideas, marketing-psychology, launch-strategy, pricing-strategy, product-marketing-context |

## CLI Tools (51)

Zero-dependency Node.js CLIs. Set `{TOOL}_API_KEY` and go.

```bash
node tools/clis/apollo.js people search --titles "CEO" --employees "1,50"
node tools/clis/buffer.js posts create --text "Your post" --channels "twitter"
node tools/clis/instantly.js campaigns analytics --id "campaign_id"
```

Full list: [`tools/REGISTRY.md`](tools/REGISTRY.md)

## Recommended Stack

| Tool | Purpose | Cost |
|------|---------|------|
| HubSpot CRM | Pipeline tracking | Free |
| Apollo.io | Lead prospecting | Free / $99/mo |
| Instantly.ai | Cold email | $97/mo |
| Calendly | Demo booking | Free |
| Buffer | Social scheduling | Free / $6/mo |

Setup guide: [`docs/SETUP.md`](docs/SETUP.md)

## Project Structure

```
claude-marketing/
├── CLAUDE.md                  # Project context for Claude Code
├── README.md                  # This file
├── .claude/commands/          # 7 slash commands
├── skills/                    # 29 marketing skills
├── tools/                     # 51 CLI tools + integration guides
├── templates/cold-emails/     # Email sequence templates
├── marketing/                 # Tracker + generated content
└── docs/                      # Setup, stack guide, skills reference
```

## Credits

Marketing skills adapted from [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) (MIT License).

## License

MIT
