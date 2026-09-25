# SmartReply for Claude and Grok Build

SmartReply is an AI customer service platform for e-commerce brands. It automates social media customer service, comment moderation, and customer support across Facebook, Instagram, YouTube, Gmail, Shopify, Amazon, and Slack.

This plugin connects your AI assistant to your SmartReply account so you can manage your AI customer service agent directly from your assistant: set it up, tune how it replies to comments and messages, test replies before they go live, search customer conversations, handle escalations, and approve or decline actions like refunds and replacements.

Website: https://smartreply.io

## Requirements

- A SmartReply account. Sign up at https://smartreply.io.
- Claude Code, Claude with plugin support (Cowork), or Grok Build.

## Installation

Clone this repository and start your assistant from its parent folder:

```sh
# Claude Code
claude --plugin-dir ./smartreply-plugin

# Grok Build
grok --plugin-dir ./smartreply-plugin
```

Grok Build supports the included Claude-format manifest, skills, commands, and MCP configuration. Use `/mcps` in Grok Build to inspect or authenticate the SmartReply connection. Marketplace installation is available only after the relevant listing is approved; this package does not imply a Grok web connector listing.

On first use, Your assistant asks you to sign in to SmartReply. Sign in with your SmartReply account and approve access. The assistant can only see and change what your SmartReply user is allowed to access.

Channel connections (Facebook, Instagram, Gmail, and others) are completed inside SmartReply. The assistant gives you the link, and you finish the provider sign-in in your browser. The assistant never asks for your passwords or provider tokens.

## What you can do

**Set up your AI customer service agent**
- "Help me set up SmartReply for my store."
- "Which of my channels are connected, and are any having problems?"

**Train and tune replies**
- "Add an instruction that customers can use OCTOBER20 for 20% off during October."
- "Pull the FAQs from our shipping policy page and add them to my agent."
- "Why does my agent give the wrong answer about returns? Fix it and test it."

**Test before going live**
- "Test how my agent replies to a comment asking if this product ships to Canada."

**Manage customer service day to day**
- "Find the conversation with this customer and pause automatic replies."
- "Show my open escalations and help me reply to the first one."
- "Show pending refund requests for my agent."
- "Undo the instruction change I made this morning."

## Commands

- `/smartreply:escalations` shows escalations waiting on you and helps you respond.
- `/smartreply:test-reply` tests how your agent answers a customer comment or message.

## Safety

- Changes run with your SmartReply permissions and the scopes you approved.
- The assistant checks the exact action and target before refunds, replacements, orders, address changes, or customer replies. If your request already authorizes those details, it does not ask again.
- Configuration changes can be rolled back with SmartReply recovery points.

## Privacy

SmartReply's privacy policy: https://smartreply.io/policy-pages/privacy-policy

Terms of service: https://smartreply.io/policy-pages/terms-of-service

## Support

Visit https://smartreply.io or email support@smartreply.io.


## Connection and data access

MCP server: `https://app.smartreply.io/api/mcp`.

Public documentation: https://help.smartreply.io/article/connect-ai-assistants-mcp

Authentication uses SmartReply OAuth with S256 PKCE and dynamic client registration for supported clients. No API key or credential is bundled. The connected user chooses a SmartReply company; current permissions and the `smartreply:read` / `smartreply:write` scopes control available operations. The backend supports rotating refresh tokens and a 60-day inactivity window, renewed by authenticated use or refresh. The assistant must support renewal; expired or revoked connections require sign-in again.

The package connects to `app.smartreply.io` for MCP tools and OAuth. Tool results may contain requested company settings, support conversations, and action details, which are shared with the assistant. Customer replies and approved actions can invoke the company's connected providers through SmartReply. Provider passwords and access tokens are not returned as tool content. Provider sign-in stays in SmartReply.

This package contains no executable hooks, install scripts, local MCP processes, or filesystem access tools. It does not include SmartReply application source code or customer data.
