# SmartReply for Claude

SmartReply is an AI customer service platform for e-commerce brands. It automates social media customer service, comment moderation, and customer support across Facebook, Instagram, YouTube, Gmail, Shopify, Amazon, and Slack.

This plugin connects Claude to your SmartReply account so you can manage your AI customer service agent directly from Claude: set it up, tune how it replies to comments and messages, test replies before they go live, search customer conversations, handle escalations, and approve or decline actions like refunds and replacements.

Website: https://smartreply.io

## Requirements

- A SmartReply account. Sign up at https://smartreply.io.
- Claude Code, or Claude with plugin support (Cowork).

## Installation

Install SmartReply from the Claude plugin directory, or add this repository as a plugin source and install `smartreply`.

On first use, Claude asks you to sign in to SmartReply. Sign in with your SmartReply account and approve access. Claude can only see and change what your SmartReply user is allowed to access.

Channel connections (Facebook, Instagram, Gmail, and others) are completed inside SmartReply. Claude gives you the link, and you finish the provider sign-in in your browser. Claude never asks for your passwords or provider tokens.

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
- Claude confirms with you before approving or declining refunds, replacements, orders, or address changes, and before sending a reply to a customer.
- Configuration changes can be rolled back with SmartReply recovery points.

## Privacy

SmartReply's privacy policy: https://smartreply.io/policy-pages/privacy-policy

Terms of service: https://smartreply.io/policy-pages/terms-of-service

## Support

Visit https://smartreply.io or email support@smartreply.io.
