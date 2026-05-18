# Skill: Customer Reply

## Purpose

Write helpful, calm, and professional replies to customers about product questions, license issues, support needs, billing concerns, cancellations, and general communication.

## Shared Files To Use

Before drafting, use:

- `../GLOBAL_RULES.md`
- `../context/company-context.md`
- `../context/product-context.md` when product details or URLs are needed
- `../context/refund-policy-context.md` if refund, cancellation, renewal, or billing sensitivity appears
- `../templates/email-templates.md` when a reusable reply fits

## When To Use

Use this skill for:

- Product support replies
- License or account questions
- Billing questions
- Customer complaints
- Feature questions
- Bug report acknowledgements
- Renewal or cancellation messages
- General customer follow-ups

## Input Needed

Ask for or infer:

- Customer name
- Product name
- Issue summary
- Order ID, purchase email, or license key if needed
- Site URL if needed
- Screenshots or error details if needed
- Desired action or status

## Workflow

1. Understand the customer's issue and exact request.
2. Identify the customer's tone: calm, confused, frustrated, or urgent.
3. Acknowledge the concern with matching tone and professional calm.
4. Provide the clearest useful answer to the main point first.
5. Ask for only the missing details required to proceed.
6. Avoid blaming the customer.
7. Escalate to support or billing review when needed.
8. Rewrite naturally for that specific customer message; do not send template copy as final output.

## Tone Rules

- Warm and reassuring
- Patient and practical
- Short, not policy-heavy
- Clear about next steps
- Match customer tone safely without copying negative language
- Use shorter replies for short customer messages and fuller replies for detailed ones

## Do

- Thank the customer.
- Show that their concern is understood.
- Answer the customer's main question in the first response block.
- Ask for order details only when needed.
- Keep refund or billing replies careful and non-final unless approved.
- Recommend technical team review for bugs or complex issues.

## Don't

- Approve or reject refunds unless already confirmed.
- Promise fixes or timelines without confirmation.
- Sound defensive.
- Over-explain internal policy.
- Ask for unnecessary private information.
- Mirror rude or aggressive wording from the customer.

## Output Format

```text
Hi [Name],

Thanks for your message. [Short acknowledgement]

[Helpful answer or request for needed details]

[Next step]

Best regards,
HasThemes Team
```

## Example User Instruction

Reply to a customer who says their license is not activating.

## Example Final Output

```text
Hi John,

Thanks for your message. Sorry for the trouble with the license activation.

Could you please share your order ID or purchase email, along with the site URL where you are trying to activate the license? We will check the license status and help you resolve it.

Best regards,
HasThemes Team
```
