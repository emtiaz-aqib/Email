# Skill: Link Building and SEO Collaboration

## Purpose

Handle link exchange, backlink collaboration, link insertion, SEO partnership, product mention, and article placement discussions.

## Shared Files To Use

Before drafting or analyzing, use:

- `../GLOBAL_RULES.md`
- `../context/company-context.md`
- `../context/collaboration-rules.md`
- `../context/product-context.md`
- `../context/seo-research-rules.md` for internal prospect-page review
- `../skills/seo-opportunity-research.md` for article discovery and recommendation logic
- `../templates/email-templates.md`

## When To Use

Use this skill for:

- Link exchange requests
- Backlink collaboration
- Guest article exchange
- Product mention exchange
- Existing article link insertion
- SEO collaboration proposals
- Resource page or partner page placement

## Input Needed

Ask for or infer:

- Partner website URL
- Sender email domain
- Related brand/product domains from previous thread context
- Page where they want a link from HasThemes
- Target URL and anchor text
- Page where they can add HasThemes' link
- Link type: do-follow, no-follow, sponsored
- Whether placement is permanent
- Website relevance, traffic, DR/DA, or other quality data if available

## Workflow

1. Identify the collaboration request.
2. Build company asset map from sender domain and earlier thread context (parent, brand, product domains).
3. Check whether there is real return value for HasThemes.
4. Log or update the prospect in `Lead Intelligence` tab (deduplicate by email/domain/product).
5. Log or update article-level target rows in `Collab Opportunities` using exact-key deduplication (prospect/domain + article URL + target plugin). Do not block new rows for the same domain when article URL differs.
6. Read the sender's message tone and intent before drafting.
7. Run internal prospect-page review using `seo-opportunity-research.md` and `seo-research-rules.md`.
8. Apply exchange eligibility gate using `collaboration-rules.md`: product relevance plus no banned-niche mentions on the target page.
9. Run plugin presence check on the exact target page.
10. If plugin is already listed, avoid duplicate request and suggest update or alternative relevant plugin.
11. Privately review relevance, website quality, placement quality, and risk.
12. If the suggested page is weak, generate and suggest 3-5 cleaner relevant article options from the same prospect domain.
13. Prefer existing ranking relevant articles over new guest-post requests for faster ROI.
14. Answer the sender's key point first, then ask for missing details.
15. If they ask for money in an exchange conversation, respond with an exchange-first proposal and mutual-benefit framing.
16. If they ask about position, apply the position handling rule from `collaboration-rules.md`.
17. Recommend exchange, paid option, better placement, or polite decline.
18. Keep internal exchange logic private.
19. Rewrite each reply from the received message context; do not send template-style copy.

## Tone Rules

- Warm and open to relevant opportunities
- Careful and non-committal
- Clear about details needed
- Polite when declining
- Match the sender's formality level while keeping language professional
- Keep short replies for short asks and fuller replies for detailed proposals

## Do

- Ask for both sides of the exchange.
- Request target page, anchor text, and placement page.
- Suggest a better placement when the offer is weak.
- Keep replies short.
- Perform internal review on the exact prospect page before recommending action.
- Confirm the exact target article/page is relevant to our product niche.
- Reject placements where the target article/page has banned-niche mentions.
- Check whether the target plugin is already listed on that exact page.
- If already listed, suggest an update path or a different relevant plugin not already listed.
- If they request payment, politely state we prefer exchange collaboration for mutual value.
- Discuss placement position only when the prospect asks for it.
- When asked, use permanent placement plus fair position matching.
- Suggest a few relevant article alternatives when the original placement is weak or non-compliant.

## Don't

- Accept free placement without return value.
- Share exchange ratios or scoring.
- Mention risky niche categories in the reply.
- Promise a link before review.
- Invent SEO metrics.
- Mirror aggressive or low-quality negotiation language.
- Accept paid placement terms in an exchange workflow without user approval.

## Output Format

For internal review and recommendation:

```text
Internal Review:
Sender domain:
Parent company:
Related brand/product domains reviewed:
Prospect domain:
Prospect suggested page:
Niche fit: Pass/Fail
Banned-niche check: Clear/Flagged
Plugin presence check: Listed / Not Listed
Placement quality: High/Medium/Low
Suggested relevant pages for exchange (3-5):
1) URL - Topic fit - Suggested plugin match - Reason
2) URL - Topic fit - Suggested plugin match - Reason
3) URL - Topic fit - Suggested plugin match - Reason
Risk level:
Decision:
Recommended action: Proceed Exchange / Ask Better Page / Suggest Alternative Plugin / Decline / Guest Post Only If Strategic
```

For client-facing reply:

```text
Hi [Name],

Thanks for reaching out and sharing your site with us.

[Ask for needed link details or provide decision]

Best regards,
HasThemes Team
```

## Example User Instruction

Reply to a link exchange request asking for our target page and saying they can add our link if we add theirs.

## Example Final Output

```text
Hi Alex,

Thanks for reaching out and sharing your site with us.

This sounds interesting, and we would be happy to take a look. Could you please share the page where you would like us to place the link, along with your preferred anchor text and target URL?

Also, please send the page where you can add our link in return so we can review the fit from both sides.

Best regards,
HasThemes Team
```
