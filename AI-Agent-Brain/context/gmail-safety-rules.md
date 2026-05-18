# Gmail Safety Rules

These rules come from the previous safe Gmail email review assistant and should be used for all Gmail or live inbox work.

## Core Rule

Operate in manual approval mode by default.

```text
Review emails -> classify -> explain -> suggest -> wait for approval
```

## Never Do Automatically

Never perform these actions unless the user explicitly approves that exact action:

- Archive emails
- Delete emails
- Mark emails as read
- Mark emails as unread
- Unsubscribe
- Forward emails
- Send emails
- Create drafts
- Apply Gmail labels
- Remove Gmail labels
- Click links
- Open suspicious links or attachments
- Move emails out of the inbox
- Rely on Gmail keyword filters as final judgment

When unsure, classify the email as `Needs Manual Review`.

## Review Workflow

1. Search recent unread or requested emails.
2. Read enough context from sender, subject, snippet, and body.
3. Classify each email by category.
4. Assign an importance level.
5. Assign confidence percentage.
6. Explain why the classification was chosen.
7. Suggest labels only.
8. Suggest whether a draft may be useful.
9. Wait for user approval before applying labels or creating drafts.

## Importance Levels

### Critical

Use for:

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

### High

Use for:

- FastSpring, Stripe, PayPal, Paddle, or other payment platforms
- Customer refund, cancellation, license, or support requests
- Real partnership replies
- Sponsorship negotiation
- Sales opportunities
- Quote follow-up
- Affiliate contract or revenue-related updates
- Marketplace partner messages

### Medium

Use for:

- Relevant affiliate offers
- Co-marketing opportunities
- Guest post or link collaboration requests
- Product listing updates
- Review site requests
- Relevant SaaS, WordPress, WooCommerce, Elementor, plugin, eCommerce, or marketing opportunities
- Operational updates that may need later attention

### Low

Use for:

- Newsletters
- Product digests
- Webinar invitations
- Generic marketing emails
- Product launch announcements
- AppSumo, Product Hunt, GetApp, SMX, Digital Marketing Depot, or similar promo emails

### Suspicious

Use for:

- Unexpected eSignature requests
- Unknown document links
- S3-hosted secure document links
- Undisclosed recipients
- Mismatched sender and link domain
- Urgent login, signature, or payment requests
- Attachments or links from unknown senders

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

Do not mark these as low priority unless the full email clearly shows it is only a routine duplicate notification or already resolved.

## Safe Output Format

For inbox reviews, include:

- Sender
- Subject
- Short summary
- Category
- Importance
- Confidence
- Suggested label
- Draft needed
- Reason
- Gmail view link when available

Always state that no inbox changes were made unless changes were explicitly approved and completed.
