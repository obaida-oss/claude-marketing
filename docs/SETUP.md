# Setup Guide

## Quick Start (5 minutes)

### Option 1: Clone into your project
```bash
cd your-project/
git clone https://github.com/YOUR_USERNAME/claude-marketing.git .claude-marketing
```

Then symlink or copy what you need:
```bash
# Copy commands into your project's .claude/commands/
cp -r .claude-marketing/.claude/commands/* .claude/commands/

# Copy skills
cp -r .claude-marketing/skills .claude/skills

# Copy tools
cp -r .claude-marketing/tools .claude/tools

# Copy templates and marketing directories
cp -r .claude-marketing/templates ./templates
cp -r .claude-marketing/marketing ./marketing
```

### Option 2: Use as a standalone project
```bash
git clone https://github.com/YOUR_USERNAME/claude-marketing.git
cd claude-marketing
```

Open in Claude Code and start using commands.

### Option 3: Git submodule
```bash
cd your-project/
git submodule add https://github.com/YOUR_USERNAME/claude-marketing.git .claude-marketing
```

---

## First Run

### 1. Set up your product context
```
/setup-context
```
This walks you through creating `.claude/product-marketing-context.md` — the foundation that all marketing skills reference. Takes 10-15 minutes.

### 2. Generate your first content
```
/content-batch
```
Generates a full week of social content (7 tweets, 2 LinkedIn posts, 3 Reddit answers).

### 3. Write cold emails
```
/cold-emails
```
Generates 3 email sequences tailored to your product and audience.

---

## Recommended Tool Stack

Set up these accounts for the full marketing workflow:

### Free (Start Here)
| Tool | Purpose | URL |
|------|---------|-----|
| HubSpot CRM | Pipeline tracking | https://app.hubspot.com/signup/crm |
| Calendly | Demo call booking | https://calendly.com |
| Twitter/X | Build in public | https://twitter.com |
| LinkedIn | Thought leadership | https://linkedin.com |
| Buffer (free tier) | Social scheduling | https://buffer.com |

### Paid (When Ready to Scale)
| Tool | Purpose | Cost | URL |
|------|---------|------|-----|
| Apollo.io | Lead prospecting | $99/mo | https://app.apollo.io |
| Instantly.ai | Cold email sending | $97/mo | https://instantly.ai |
| 3 email domains | Sender reputation | ~$30/yr | Namecheap/Cloudflare |

### Environment Variables
Create a `.env` file in your project (never commit this):

```bash
# CRM
HUBSPOT_API_KEY=your-hubspot-private-app-token

# Prospecting
APOLLO_API_KEY=your-apollo-api-key

# Cold Email
INSTANTLY_API_KEY=your-instantly-api-key

# Scheduling
CALENDLY_API_KEY=your-calendly-api-key

# Social (optional)
BUFFER_ACCESS_TOKEN=your-buffer-token
```

---

## HubSpot CRM Setup

1. Sign up at https://app.hubspot.com/signup/crm (free)
2. Create Private App: Settings → Integrations → Private Apps
   - Scopes: `crm.objects.contacts.read/write`, `crm.objects.deals.read/write`
3. Configure deal pipeline stages:

| Stage | Probability |
|-------|------------|
| Lead Identified | 10% |
| Contacted | 15% |
| Replied | 25% |
| Call Booked | 40% |
| Demo Given | 50% |
| Proposal Sent | 70% |
| Negotiation | 85% |
| Closed Won | 100% |
| Closed Lost | 0% |

4. Add custom contact properties:
   - `lead_source` (Dropdown: Free Tool / Twitter / Reddit / Cold Email / Partnership / Referral)
   - `company_url` (URL)
   - Any properties specific to your business

---

## CLI Tools

All 51 CLI tools are zero-dependency Node.js scripts. Use them like:

```bash
# Set API key
export APOLLO_API_KEY=your-key

# Search for prospects
node tools/clis/apollo.js people search --titles "CEO" --employees "1,50"

# Schedule social posts
node tools/clis/buffer.js posts create --text "Your post" --channels "twitter"

# Check email campaign stats
node tools/clis/instantly.js campaigns analytics --id "campaign_id"
```

See `tools/REGISTRY.md` for the full list of available tools.
