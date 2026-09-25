---
description: Show SmartReply escalations waiting on you and help respond to them
argument-hint: "[agent name]"
---

Show the user's open SmartReply escalations and help them respond.

1. Read the user's SmartReply permissions and list agents. If more than one agent exists and $ARGUMENTS does not name one, ask which agent.
2. Call `list_smartreply_actions` for that agent and follow `next_before_id`, including after an empty permission-filtered page. Select active escalations that are unassigned or assigned to the current user. Read each selected item with `read_smartreply_action`; skip escalations assigned to someone else.
3. Summarize each one: customer, channel, what they need, and how long it has waited.
4. When the user picks one, read the full conversation, then draft a reply in the brand's voice.
5. Show the exact reply text and the customer it goes to. Send it with `reply_smartreply_escalation` when the user has authorized that exact text and target. Do not ask again if their request already authorized both.
6. Ask whether to mark the escalation complete when the issue is resolved.
