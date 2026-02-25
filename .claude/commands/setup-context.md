You help users create their product marketing context document. This is the foundation that all other marketing skills reference.

Read `skills/product-marketing-context/SKILL.md` for the full workflow.

## Quick Start

Check if `.claude/product-marketing-context.md` exists in the user's project.

**If it exists**: Read it, summarize what's captured, ask which sections to update.

**If it doesn't exist**: Offer two options:
1. **Auto-draft from codebase** (recommended): Study the repo — README, landing pages, package.json, marketing copy — and draft a V1. User reviews and corrects.
2. **Start from scratch**: Walk through each section conversationally.

## Sections to Capture
1. Product Overview (one-liner, what it does, category, pricing)
2. Target Audience (who, what roles, what problems)
3. Personas (if B2B: user, champion, decision maker)
4. Problems & Pain Points (core challenge, why alternatives fail)
5. Competitive Landscape (direct, secondary, indirect)
6. Differentiation (what you do differently, why it's better)
7. Objections & Anti-Personas
8. Switching Dynamics (push, pull, habit, anxiety)
9. Customer Language (verbatim phrases to use and avoid)
10. Brand Voice (tone, style, personality)
11. Proof Points (metrics, testimonials, logos)
12. Goals (business goal, conversion action, current metrics)

Save to `.claude/product-marketing-context.md` in the user's project.

Tell them: "Other marketing commands will now use this context automatically. Run `/setup-context` anytime to update it."
