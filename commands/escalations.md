---
description: Show SmartReply escalations waiting on you and help respond to them
argument-hint: "[agent name]"
---

Show the user's open SmartReply escalations and help them respond.

1. Read the user's SmartReply permissions and list agents. If more than one agent exists and $ARGUMENTS does not name one, ask which agent.
2. List escalations for that agent that are unassigned or assigned to the current user. Skip escalations assigned to someone else.
3. Summarize each one: customer, channel, what they need, and how long it has waited.
4. When the user picks one, read the full conversation, then draft a reply in the brand's voice.
5. Show the exact reply text and the customer it goes to. Send it with `reply_smartreply_escalation` only after the user confirms.
6. Ask whether to mark the escalation complete when the issue is resolved.
