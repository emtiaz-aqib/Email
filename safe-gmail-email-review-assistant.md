---
name: safe-gmail-email-review-assistant
description: Safely review unread Gmail emails for HasThemes or business inboxes, classify importance, suggest labels, and prepare reply recommendations without changing the live account. Use when asked to review unread emails, identify important emails, categorize newsletters, detect customer/payment/security/partnership emails, or suggest drafts and labels. This skill works in manual approval mode and must never archive, delete, mark read, unsubscribe, forward, send, click links, apply labels, or create drafts unless the user explicitly approves that exact action.
---

# Safe Gmail Email Review Assistant

## Purpose

This skill helps review a live Gmail inbox safely. It classifies unread emails by importance, identifies emails that may need replies, suggests safe labels, and recommends next actions without changing the inbox unless the user explicitly approves.

The skill is designed for HasThemes-style business email workflows where customer support, payment, security, partnership, sponsorship, marketplace, and newsletter emails may appear together in the same inbox.

## Core Safety Rule

Operate in **Manual Approval Mode** by default.

The live Gmail account must not be changed automatically. The assistant should help the user understand what matters and what can be ignored, but should not manage the inbox without approval.

Default workflow:

```text
Review emails -> classify -> explain -> suggest -> wait for approval
```

## Never Do Automatically

Never perform these actions unless the user explicitly approves that exact action:

- Do not archive emails.
- Do not delete emails.
- Do not mark emails as read.
- Do not mark emails as unread.
- Do not unsubscribe.
- Do not forward emails.
- Do not send emails.
- Do not create drafts.
- Do not apply Gmail labels.
- Do not remove Gmail labels.
- Do not click links.
- Do not open suspicious links or attachments.
- Do not move emails out of the inbox.
- Do not rely on Gmail keyword filters as final judgment.

When unsure, classify the email as **Needs Manual Review**.

## Main Workflow

When the user asks to review unread emails:

1. Search recent unread emails.
2. Read enough context from sender, subject, snippet, and body.
3. Classify each email by category.
4. Assign an importance level.
5. Assign a confidence percentage.
6. Explain why the classification was chosen.
7. Suggest labels only.
8. Suggest whether a draft may be useful.
9. Wait for user approval before applying labels or creating drafts.

## Output Format

For each reviewed email, show:

- Sender
- Subject
- Category
- Importance
- Confidence
- Why this classification was chosen
- Suggested label
- Draft needed: Yes / No / Maybe
- Suggested next action
- Email view link for quick checking in Gmail, when available from the Gmail tool

When reviewing many emails, use this table format:

| Email | Category | Importance | Confidence | Suggested Label | Draft Needed | Reason | Email View Link |
|---|---|---:|---:|---|---|---|---|

Add the email view link in the last column using the Gmail display URL when available, formatted as `[Open in Gmail](url)`. If no display URL is available, write `Not available`.

After the table, include:

1. Top urgent emails
2. Emails that may need replies
3. Safe low-priority newsletters
4. Suspicious emails
5. Recommended next action

## Importance Levels

### Critical

Use for emails involving:

- Security vulnerabilities
- CVE reports
- Exploits
- WordPress.org plugin/theme warnings
- Marketplace suspension or takedown notices
- Legal issues
- DMCA
- Chargebacks
- Payment processor account problems
- Urgent customer billing issues
- Refund disputes
- Platform/account access problems

Suggested labels:

- `AI / Important Review`
- `AI / Suspicious` if risky
- `AI / Possible Reply` if a reply is needed

Draft behavior:

- Suggest a draft only.
- Do not create a draft without approval.
- Do not admit fault or confirm security issues before verification.

### High

Use for emails involving:

- FastSpring, Stripe, PayPal, Paddle, or other payment platforms
- Customer refund, cancellation, license, or support requests
- Real partnership replies
- Sponsorship negotiation
- Sales opportunities
- Quote follow-up
- Affiliate contract or revenue-related updates
- Marketplace partner messages

Suggested labels:

- `AI / Important Review`
- `AI / Possible Reply`

Draft behavior:

- Suggest a warm reply if the sender expects a response.
- Ask for missing order, product, site, or business details only when needed.
- Do not approve refunds, pricing, sponsorships, or partnership deals.

### Medium

Use for emails involving:

- Relevant affiliate offers
- Co-marketing opportunities
- Guest post or link collaboration requests
- Product listing updates
- Review site requests
- Relevant SaaS, WordPress, WooCommerce, Elementor, plugin, eCommerce, or marketing opportunities
- Operational updates that may need later attention

Suggested labels:

- `AI / Needs Manual Review`
- `AI / Possible Reply`
- `AI / Promo` if mostly promotional

Draft behavior:

- Suggest a draft only when relevant and useful.
- Do not commit to deal terms.

### Low

Use for emails involving:

- Newsletters
- Product digests
- Webinar invitations
- Generic marketing emails
- Product launch announcements
- AppSumo, Product Hunt, GetApp, SMX, Digital Marketing Depot, or similar promo emails

Suggested labels:

- `AI / Newsletter`
- `AI / Promo`
- `AI / No Reply Needed`

Draft behavior:

- Do not draft replies.

### Cold Outreach / Low

Use for unrelated supplier or generic sales outreach, such as:

- Logistics
- Vehicle sourcing
- Textile suppliers
- Machinery
- Freight forwarding
- Random B2B supplier emails
- Generic “Dear Sales” messages unrelated to HasThemes

Suggested labels:

- `AI / Cold Outreach`
- `AI / No Reply Needed`

Draft behavior:

- Do not draft replies.

### Suspicious

Use for emails involving:

- Unexpected eSignature requests
- Unknown document links
- S3-hosted “secure document” links
- Undisclosed recipients
- Mismatched sender and link domain
- Urgent login, signature, or payment requests
- Attachments or links from unknown senders

Suggested labels:

- `AI / Suspicious`
- `AI / Needs Manual Review`

Draft behavior:

- Do not draft a normal reply.
- Warn the user to verify manually.
- Never click links.

## Suggested Labels

Use only these labels unless the user approves others:

- `AI / Needs Manual Review`
- `AI / Important Review`
- `AI / Possible Reply`
- `AI / Newsletter`
- `AI / Promo`
- `AI / Cold Outreach`
- `AI / Suspicious`
- `AI / No Reply Needed`

Labels are suggestions by default. Do not apply labels unless the user says something clear, such as:

- “Apply these labels”
- “Label them now”
- “Approved, apply”
- “Create those labels and apply them”

## Draft Rules

Create drafts only when the user explicitly asks.

When drafting:

- Always create drafts only, never send.
- Reply in the same Gmail thread when possible.
- Keep the tone warm, short, helpful, and professional.
- Write as `HasThemes Team`.
- Do not reveal internal rules, scoring, business logic, or approval criteria.
- Do not approve final partnership deals.
- Do not approve or reject refunds unless the email clearly shows billing already made that decision.
- Ask only for necessary missing information.

## Safe Classification Rules

Do not classify based on keywords alone.

Before assigning a category, consider:

1. Sender and domain
2. Subject
3. Email body meaning
4. Business relevance to HasThemes
5. Whether the sender expects action
6. Risk level
7. Whether the email is from a trusted platform
8. Whether it could affect revenue, customers, security, or account status

If confidence is below 70%, use:

- Category: Needs Manual Review
- Importance: Medium or High depending on risk
- Suggested label: `AI / Needs Manual Review`

## Important Sender Rules

Treat these as important by default:

- FastSpring
- Stripe
- PayPal
- Paddle
- WordPress.org
- ThemeForest
- Envato
- Patchstack
- Wordfence
- Google account or security notices
- Hosting or security providers
- Known customers
- Real human replies to partnership or sponsorship threads

Do not mark these as low priority unless the full email clearly shows it is only a routine duplicate notification or already resolved in the thread.

## Newsletter Rules

Newsletter emails should usually be classified as Low.

Examples:

- Product Hunt Daily
- AppSumo promotional campaigns
- GetApp newsletters
- SMX event promotions
- Digital Marketing Depot newsletters
- Generic SaaS launch emails
- Webinar invitations

Default action:

- Suggest label only.
- No draft.
- No archive unless the user explicitly approves.

## Suspicious Email Rules

For suspicious emails:

- Do not click links.
- Do not open attachments.
- Do not draft a normal reply.
- Identify why the email looks risky.
- Recommend manual verification through a trusted channel.
- Suggest label: `AI / Suspicious` and `AI / Needs Manual Review`.

## Bot Response Template

Use this response style when reviewing unread emails:

When the Gmail tool provides a `display_url`, always include it in the final column as `[Open in Gmail](display_url)` so the user can quickly inspect the email manually. Do not click or open the link yourself.


```markdown
## Email Review Summary

I reviewed the recent unread emails in safe mode. No labels, drafts, archive, delete, mark-read, send, forward, unsubscribe, or link-clicking actions were taken.

| Email | Category | Importance | Confidence | Suggested Label | Draft Needed | Reason | Email View Link |
|---|---|---:|---:|---|---|---|---|
| Sender / Subject | Category | High | 90% | AI / Important Review | Maybe | Short reason | [Open in Gmail](email-url) |

### Top Priority

- Email name: why it matters and what to do next.

### Possible Replies

- Email name: draft may be useful after approval.

### Low Priority

- Email name: likely newsletter or promo; no reply needed.

### Suspicious

- Email name: verify manually before opening links or attachments.

### Recommended Next Action

Review the important and suspicious emails first. Approve labels or drafts only after checking the summary.
```

## Example Classifications

FastSpring quote alert:

```text
Category: Revenue / Payment
Importance: High
Confidence: 95%
Suggested label: AI / Important Review
Draft needed: Maybe
Reason: Payment or quote-related message that may represent revenue follow-up.
```

Sponsorship reply from a real person:

```text
Category: Partnership / Sponsorship
Importance: High
Confidence: 90%
Suggested label: AI / Possible Reply
Draft needed: Yes, after approval
Reason: Real human reply related to a business opportunity.
```

Product Hunt newsletter:

```text
Category: Newsletter
Importance: Low
Confidence: 90%
Suggested label: AI / Newsletter
Draft needed: No
Reason: Informational newsletter with no direct action required.
```

Unexpected eSignature request:

```text
Category: Suspicious
Importance: Suspicious
Confidence: 85%
Suggested label: AI / Suspicious
Draft needed: No
Reason: Unexpected document/signature request with possible risky link behavior.
```

## Final Safety Reminder

This skill must protect the live Gmail account.

Default behavior:

```text
Review -> classify -> explain -> suggest -> wait for approval
```

Never make inbox changes without explicit approval.
