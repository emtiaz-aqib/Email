# Skill: Internal Task Summary

## Purpose

Convert emails, chats, notes, meetings, or scattered updates into clear internal summaries and action lists.

## Shared Files To Use

Before summarizing, use:

- `../GLOBAL_RULES.md`
- `../context/company-context.md` when the audience or signature matters

## When To Use

Use this skill for:

- Email thread summaries
- Meeting notes
- Daily work summaries
- Follow-up lists
- Task extraction
- Project status updates
- Internal handoff notes

## Input Needed

Ask for or infer:

- Source text or thread
- Audience for the summary
- Desired detail level
- Deadline or priority if available
- Owner names if available

## Workflow

1. Read the source material.
2. Identify the main decision, request, or issue.
3. Extract action items.
4. Assign owners only when clearly stated.
5. Highlight deadlines and blockers.
6. Keep the summary practical.

## Tone Rules

- Clear and neutral
- Brief but complete
- Action-oriented
- Easy to scan

## Do

- Separate facts from assumptions.
- Mention unclear ownership.
- Include deadlines.
- Highlight blockers.

## Don't

- Add tasks that were not implied.
- Invent owners or dates.
- Include unnecessary email history.
- Overwrite uncertainty with confidence.

## Output Format

```text
Summary:
- [Main point]

Action Items:
- [Task] - Owner: [Name/Unassigned] - Deadline: [Date/Not specified]

Important Details:
- [Detail]

Open Questions:
- [Question]

Recommended Next Step:
- [Next step]
```

## Example User Instruction

Summarize this email thread and list what I need to do next.

## Example Final Output

```text
Summary:
- The partner is interested in a content collaboration but needs confirmation on topic, timeline, and link placement.

Action Items:
- Confirm preferred article topic - Owner: Imtiaz - Deadline: Not specified
- Share target URL and anchor text - Owner: Imtiaz - Deadline: Not specified
- Ask partner for publishing timeline - Owner: Imtiaz - Deadline: Not specified

Important Details:
- The partner is open to reviewing a WooCommerce-related topic.
- Link placement has not been confirmed yet.

Open Questions:
- Will the partner provide a do-follow link?
- What is the expected publication date?

Recommended Next Step:
- Reply with the topic suggestion and ask for link type and timeline.
```
