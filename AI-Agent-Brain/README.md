# AI Agent Brain

This folder contains the global behavior rules and focused skill files for a HasThemes / HasTech IT Ltd AI work assistant.

## Lead Tracker

Primary lead intelligence sheet (single source of truth):

- [HasThemes Lead Intelligence Tracker](https://docs.google.com/spreadsheets/d/1iv3O3JLQoDbqAHP3FzBD_QtbbnVLmX4B7UICZrA3SpM/edit#gid=1858736051)
- Tabs:
  - `Lead Intelligence` for prospect/company profile logging
  - `Collab Opportunities` for article-level opportunity tracking
- Agent behavior: auto-check and auto-update row data in this sheet without per-update approval.

## Structure

```text
AI-Agent-Brain/
  GLOBAL_RULES.md
  ROUTING.md
  README.md
  context/
    company-context.md
    product-context.md
    collaboration-rules.md
    gmail-safety-rules.md
    refund-policy-context.md
    seo-research-rules.md
  templates/
    email-templates.md
  skills/
    email-outreach.md
    customer-reply.md
    partnership-negotiation.md
    link-building-seo-collaboration.md
    content-collaboration.md
    odoo-erp-lead-qualification.md
    internal-task-summary.md
    gmail-inbox-triage.md
    refund-cancellation-support.md
    seo-opportunity-research.md
```

## How To Use

1. Load `GLOBAL_RULES.md` first.
2. Use `ROUTING.md` to select the correct skill.
3. Load only the shared context files needed for the task.
4. Follow the selected skill's workflow and output format.
5. Keep internal logic private and produce only the output the user needs.

## Recommended Agent Instruction

Use this as the agent's base instruction:

```text
Read GLOBAL_RULES.md first. Then use ROUTING.md to choose the most relevant skill. Load only the shared context files needed for that task. Follow the selected skill exactly. If no skill matches, use GLOBAL_RULES.md and ask only for essential missing information.
```
