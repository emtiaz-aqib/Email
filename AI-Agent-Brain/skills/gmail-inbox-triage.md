# Skill: Gmail Inbox Triage

## Purpose

Safely review Gmail emails, classify importance, suggest labels, identify reply needs, and protect the live inbox from accidental changes.

## Shared Files To Use

Before reviewing Gmail or recommending actions, use:

- `../GLOBAL_RULES.md`
- `../context/gmail-safety-rules.md`
- `../context/company-context.md`
- Relevant task skill only after triage if the user asks for a draft

## When To Use

Use this skill for:

- Reviewing unread emails
- Finding important messages
- Separating newsletters from business emails
- Detecting customer, payment, security, and partnership emails
- Suggesting labels
- Recommending draft replies

## Input Needed

Ask for or infer:

- Gmail search scope
- Number of emails to review
- Whether only unread emails should be checked
- Whether the user wants labels, drafts, or only analysis

## Core Safety Rule

Manual approval mode is required.

Follow `../context/gmail-safety-rules.md` as the source of truth for inbox safety.

Never automatically:

- Send emails
- Create drafts
- Archive
- Delete
- Mark read or unread
- Apply labels
- Click links
- Open suspicious attachments
- Unsubscribe

## Workflow

1. Search the requested email scope.
2. Review sender, subject, snippet, and body context.
3. Classify each email.
4. Assign importance and confidence.
5. Suggest labels only.
6. Recommend whether a draft is needed.
7. Wait for explicit approval before changing anything.

## Categories

Use practical categories:

- Customer Support
- Billing or Refund
- Security
- Marketplace or Platform
- Partnership
- Sponsorship
- SEO Collaboration
- Sales Lead
- Newsletter
- Promo
- Cold Outreach
- Suspicious
- Needs Manual Review

## Importance Levels

- Critical: security, payment processor problems, legal, account suspension, chargebacks, urgent billing.
- High: customers, refunds, real partner replies, marketplace messages, sales leads.
- Medium: relevant collaborations, affiliate offers, product listing opportunities.
- Low: newsletters, webinars, generic promotions.
- Suspicious: unknown document links, urgent login/payment requests, mismatched sender/link domains.

## Output Format

```markdown
## Email Review Summary

No inbox changes were made.

| Email | Short Summary | Category | Importance | Confidence | Suggested Label | Draft Needed | Reason |
|---|---|---|---:|---:|---|---|---|
| Sender / Subject | 8-14 word summary | Category | High | 90% | AI / Important Review | Maybe | Short reason |

### Top Priority
- [Email]: [why it matters]

### Possible Replies
- [Email]: [reply recommendation]

### Low Priority
- [Email]: [why low priority]

### Suspicious
- [Email]: [manual verification warning]

### Recommended Next Action
- [Next step]
```

## Example User Instruction

Review my unread Gmail emails and tell me which ones need attention.

## Example Final Output

```markdown
## Email Review Summary

No inbox changes were made.

| Email | Short Summary | Category | Importance | Confidence | Suggested Label | Draft Needed | Reason |
|---|---|---|---:|---:|---|---|---|
| FastSpring / Payment notification | Payment-related message may need billing review. | Billing | High | 95% | AI / Important Review | Maybe | Payment platform messages can affect revenue or customer billing. |
| Product Hunt / Daily digest | General product newsletter with no direct action. | Newsletter | Low | 90% | AI / Newsletter | No | Informational email only. |

### Recommended Next Action
- Review the payment-related email first, then approve any labels or drafts you want created.
```
