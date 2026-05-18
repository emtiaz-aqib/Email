# Skill Routing

Load `GLOBAL_RULES.md` first, then use this file to choose the most relevant skill.

## Primary Routing

- Cold outreach, warm outreach, prospecting, follow-up: `skills/email-outreach.md`
- Customer support, license, product issue, general customer reply: `skills/customer-reply.md`
- Refund, cancellation, renewal, billing-sensitive request: `skills/refund-cancellation-support.md`
- Paid guest post, paid link insertion, sponsorship, affiliate, co-marketing, product listing, pricing negotiation: `skills/partnership-negotiation.md`
- Link exchange, backlink, SEO collaboration, guest article exchange, resource page mention: `skills/link-building-seo-collaboration.md`
- Blog coordination, article brief, guest article topic, editorial reply, content update: `skills/content-collaboration.md`
- Odoo ERP inquiry, ERP discovery, implementation lead, sales qualification: `skills/odoo-erp-lead-qualification.md`
- Meeting notes, email thread summary, daily report, task extraction: `skills/internal-task-summary.md`
- Gmail inbox review, unread email classification, label recommendation: `skills/gmail-inbox-triage.md`
- Article/listing opportunity research, competitor mention research, backlink prospecting: `skills/seo-opportunity-research.md`

## Shared Context Routing

Use these shared files when needed:

- Company and signature rules: `context/company-context.md`
- Product names, URLs, positioning: `context/product-context.md`
- Collaboration rules and private negotiation logic: `context/collaboration-rules.md`
- Gmail safety and inbox triage rules: `context/gmail-safety-rules.md`
- Refund, cancellation, renewal, billing context: `context/refund-policy-context.md`
- SEO opportunity research rules: `context/seo-research-rules.md`
- Reusable email language: `templates/email-templates.md`

## If Multiple Skills Apply

Choose one primary skill and use shared context for the rest.

Examples:

- A Gmail email about a refund: primary skill `gmail-inbox-triage.md` for review, then `refund-cancellation-support.md` only if the user asks for a draft.
- A link exchange email in Gmail: primary skill `gmail-inbox-triage.md` for inbox review, then `link-building-seo-collaboration.md` for drafting.
- A paid guest post negotiation: primary skill `partnership-negotiation.md`, with `context/collaboration-rules.md`.
- A ShopLentor article opportunity search: primary skill `seo-opportunity-research.md`, with `context/product-context.md`.
