---
description: Test how your SmartReply agent answers a customer comment or message
argument-hint: "[customer comment or message]"
---

Test the user's SmartReply agent in the sandbox.

1. List agents and pick the one the user means. Ask if it is unclear.
2. Use $ARGUMENTS as the customer's text. If it is empty, ask for a realistic customer comment or message.
3. Decide whether it is a public comment or a private message, and run the matching test with `run_smartreply_test`. Mention that sandbox tests can use AI credits.
4. Poll `get_smartreply_test_result` until it finishes. Queued is not a result.
5. Show the agent's reply and say whether it matches the brand's instructions and policies.
6. If the reply is wrong, find the instruction, rule, or FAQ that caused it, propose the smallest fix, and retest after the user approves the change.
