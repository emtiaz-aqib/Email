# Skill: SEO Opportunity Research

## Purpose

Find and prioritize article, listicle, review, comparison, backlink, and product mention opportunities for HasThemes products.

## Shared Files To Use

Before researching or reporting, use:

- `../GLOBAL_RULES.md`
- `../context/product-context.md`
- `../context/seo-research-rules.md`
- `../templates/email-templates.md` if outreach copy is requested

## When To Use

Use this skill for:

- Finding websites to mention ShopLentor, WooLentor, Support Genix, Whols, Recurio, Swatchly, HashBar, or other products
- Competitor mention research
- Article listing opportunities
- Backlink prospecting
- Outreach target building
- SEO, AEO, or GEO visibility research
- Internal review of a prospect website/page for exchange collaboration approval

## Input Needed

Ask for or infer:

- Product name and URL
- Prospect domain
- Prospect suggested page URL, if provided
- Sender/company identity clues from thread history
- Target keyword cluster
- Competitors
- Target region if any
- Desired number of opportunities
- Whether live web research is available

## Workflow

1. If a prospect domain is provided, start in prospect review mode using `seo-research-rules.md`.
2. Evaluate the prospect-suggested page for relevance, banned-niche mentions, placement quality, and plugin presence.
3. If the plugin is already listed, flag duplicate risk and suggest update path or alternative relevant plugin.
4. Search the same prospect domain for 3-5 better relevant article options when needed.
5. Build keyword and competitor query sets for broader discovery when requested.
6. Inspect promising pages.
7. Check whether the HasThemes product is already mentioned.
8. Note competitors mentioned.
9. Find the best outreach path.
10. Score opportunities from 1 to 5.
11. Recommend pitch angle and next action.

## Quality Rules

- Use live research when available because rankings and pages change.
- Do not invent traffic, DR, DA, contact emails, or article dates.
- Distinguish verified facts from estimates.
- Avoid spammy, irrelevant, adult, casino, CBD, drug, dating, or gray-area sites.
- Prioritize WordPress, WooCommerce, Elementor, SaaS, eCommerce, and marketing relevance.

## Output Format

For prospect review mode:

```text
Internal Review:
Sender/company context:
Prospect domain:
Prospect suggested page:
Niche fit: Pass/Fail
Banned-niche check: Clear/Flagged
Plugin presence check: Listed / Not Listed
Placement quality: High/Medium/Low
Suggested relevant article options (3-5):
1) URL - Topic fit - Suggested plugin match - Reason
2) URL - Topic fit - Suggested plugin match - Reason
3) URL - Topic fit - Suggested plugin match - Reason
Risk level:
Decision:
Recommendation: Proceed Exchange / Ask Better Page / Suggest Alternative Plugin / Decline / Guest Post Only If Strategic
```

For broad opportunity research:

```markdown
## Top Opportunities

| Priority | Website | Article / Topic | URL | Product Status | Competitors Mentioned | Score | Outreach Path | Pitch Angle |
|---:|---|---|---|---|---|---:|---|---|

## Article Update Suggestions

- [Suggestion]

## Outreach Message

[Draft outreach email]

## Next Actions

1. [Action]
2. [Action]
```

## Example User Instruction

Find article opportunities where ShopLentor can be added to WooCommerce plugin listicles.

## Example Final Output

```markdown
## Top Opportunities

| Priority | Website | Article / Topic | URL | Product Status | Competitors Mentioned | Score | Outreach Path | Pitch Angle |
|---:|---|---|---|---|---|---:|---|---|
| 1 | ExampleWP | Best WooCommerce Plugins | https://example.com/best-woocommerce-plugins | Missing | ShopEngine, JetWooBuilder | 5 | Contact page | Position ShopLentor as an all-in-one WooCommerce store builder. |

## Outreach Message

Hi [Name],

I noticed your article on the best WooCommerce plugins and thought ShopLentor could be a useful addition for readers looking to customize WooCommerce store pages.

Would you be open to reviewing ShopLentor for a possible mention in the article?

Best regards,
HasThemes Team
```
