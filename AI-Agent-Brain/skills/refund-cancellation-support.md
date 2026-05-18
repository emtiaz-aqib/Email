# Skill: Refund and Cancellation Support

## Purpose

Handle refund, cancellation, renewal, auto-renewal, subscription, and billing-sensitive customer replies calmly and safely.

## Shared Files To Use

Before drafting, use:

- `../GLOBAL_RULES.md`
- `../context/company-context.md`
- `../context/refund-policy-context.md`
- `../templates/email-templates.md` when a reusable reply fits

## When To Use

Use this skill for:

- Refund requests
- Renewal cancellation
- Auto-renewal complaints
- Subscription cancellation
- Billing confusion
- Duplicate charge claims
- Customer frustration about payment

## Input Needed

Ask for or infer:

- Product name
- Purchase source
- Order ID or purchase email
- Purchase date
- Renewal date if applicable
- Customer's issue
- Whether billing has already approved or rejected a refund

## Workflow

1. Acknowledge the customer's concern.
2. Identify product, purchase source, and order details.
3. Detect emotional tone: calm, confused, upset, or urgent.
4. Answer the main concern first in calm, practical language.
5. Avoid final approval or rejection unless already confirmed.
6. If details are missing, ask for order ID or purchase email.
7. If the customer is upset, escalate for billing review.
8. Keep policy references short and helpful.

## Tone Rules

- Calm and respectful
- Customer-retention focused
- Short and practical
- Never cold or dismissive
- Match customer tone safely with extra empathy when frustration is visible
- Do not mirror anger; de-escalate and keep control of the conversation

## Do

- Ask for order ID or purchase email when needed.
- Explain cancellation as stopping future renewals.
- Mention billing review when appropriate.
- Keep the customer reassured.

## Don't

- Approve or reject refunds without confirmation.
- Debate policy.
- Blame the customer for auto-renewal.
- Give unsupported refund-window claims.
- Invent refund policy links.

## Policy Source

Use `../context/refund-policy-context.md` for refund links, FastSpring cancellation guidance, money-back guarantee notes, and customer-retention handling.

## Output Format

```text
Hi [Name],

Thanks for your message. [Short acknowledgement]

[Billing/refund/cancellation response]

Best regards,
HasThemes Team
```

## Example User Instruction

Reply to a customer asking to cancel renewal and refund a recent auto-renewal.

## Example Final Output

```text
Hi David,

Thanks for your message. I understand your concern about the renewal charge.

Cancelling the subscription will stop future renewals. Since the renewal payment has already been processed, please share your order ID or purchase email and we will review the charge with our billing team to help with the best possible option.

Best regards,
HasThemes Team
```
