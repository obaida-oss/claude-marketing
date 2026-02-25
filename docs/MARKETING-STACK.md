# Marketing Stack Reference

## Architecture

```
Apollo.io ──→ HubSpot CRM ──→ Instantly.ai
(Find leads)   (Track pipeline)  (Send emails)
     │               │                   │
     │          Calendly                 │
     │         (Book calls)              │
     │               │                   │
     └───────────────┼───────────────────┘
                     │
    Twitter/X + LinkedIn + Reddit + Buffer
           (Build audience & inbound)
```

## HubSpot API Quick Reference

```bash
# Create contact
curl -X POST https://api.hubapi.com/crm/v3/objects/contacts \
  -H "Authorization: Bearer $HUBSPOT_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"properties": {"email": "...", "firstname": "...", "company": "..."}}'

# Create deal
curl -X POST https://api.hubapi.com/crm/v3/objects/deals \
  -H "Authorization: Bearer $HUBSPOT_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"properties": {"dealname": "...", "amount": "...", "dealstage": "..."}}'

# Search contacts
curl -X POST https://api.hubapi.com/crm/v3/objects/contacts/search \
  -H "Authorization: Bearer $HUBSPOT_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"filterGroups": [{"filters": [{"propertyName": "lead_source", "operator": "EQ", "value": "Cold Email"}]}]}'
```

## Apollo API Quick Reference

```bash
# Search people
curl -X POST https://api.apollo.io/api/v1/mixed_people/api_search \
  -H "x-api-key: $APOLLO_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"person_titles": ["CEO"], "organization_num_employees_ranges": ["1,50"]}'

# Enrich person
curl -X POST https://api.apollo.io/api/v1/people/match \
  -H "x-api-key: $APOLLO_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"email": "founder@company.com"}'
```

## Daily Marketing Workflow

### What Claude Does (via commands)
- `/content-batch` → generates weekly content
- `/cold-emails` → writes email sequences
- `/crm` → manages pipeline
- `/marketing` → executes highest-priority task

### What You Do
| Time | Task | Minutes |
|------|------|---------|
| Morning | Post today's content (copy-paste) | 5 |
| Morning | Reply to DMs/comments | 10 |
| Midday | Engage on 5 posts from target audience | 15 |
| Midday | Answer 1 community question | 10 |
| Afternoon | Take demo calls (if booked) | 15-30 |
| Weekly | Run `/content-batch` for next week | 5 |
| Weekly | Review pipeline in HubSpot | 10 |
