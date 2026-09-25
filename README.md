# SmartReply for Claude

Connect Claude to SmartReply to inspect AI customer support settings, prepare FAQs, update requested instructions, test replies, search conversations, and manage permitted actions and escalations.

Website: https://smartreply.io

MCP endpoint: https://app.smartreply.io/api/mcp

## Package contents

This standalone package contains the Claude plugin manifest, account-assistance skill, public MCP URL, and brand icons. It contains no application source code, customer data, credentials, or application repository history.

## Authentication and release status

A SmartReply account is required. Each connection must identify a user and company. Access follows current permissions and OAuth scopes. Use `smartreply:read` for inspection and `smartreply:write` for requested changes. Provider login remains in SmartReply.

This package is prepared for Claude, but Claude authentication has not yet been validated end to end. The existing server was configured with a predefined ChatGPT OAuth client and callback. Before public submission, configure and test the actual Claude client registration and exact callback using the chosen Claude surface. Do not assume the ChatGPT callback works in Claude. Do not loosen redirect validation or publish access tokens in this repository.

For temporary tests on a Claude surface that supports manually supplied bearer tokens, the signed-in SmartReply `/mcp/testing` page can issue a one-hour MCP token. A normal SmartReply integration API key is not interchangeable with that token.

## Example requests

- List my SmartReply agents and read the selected agent’s current instructions.
- Add the October promotion to this agent’s instructions, preserving unrelated content.
- Extract FAQs from this public webpage and prepare the requested configuration.
- Test this customer question in the sandbox and explain the result.
- Show accessible escalations and help me respond to the selected customer.

User-requested changes execute directly with permission checks. Preview-only requests do not authorize applying changes. The host may request tool confirmation. Uncertain outcomes must be inspected before retrying.

## Local validation

Run `claude plugin validate .` from this directory. Manifest validation does not establish that remote authentication works.

## Directory submission

Use the URL of the separate public repository in Link to plugin. Leave Path within repository blank, because this package is at the repository root. Homepage: https://smartreply.io. Do not submit the private application repository.
