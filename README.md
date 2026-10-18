# HelpWell for Gemini CLI

Connect Gemini CLI to [HelpWell](https://helpwell.ai), by **Workado, LLC**. HelpWell brings your help desk, knowledge base, help docs, live chat support, support ticketing software, contacts, email marketing software and marketing automation for SaaS into one workspace.

This extension configures the hosted HelpWell MCP endpoint and includes starter prompts. It contains no account credentials or hosted application source.

## Install and connect

```sh
gemini extensions install https://github.com/ChainAI-Org/helpwell-gemini-extension
```

Restart Gemini CLI. Run `/mcp` to view the connection. If authentication is required, run `/mcp auth helpwell` and sign in to HelpWell in your browser. Choose the workspace, access level and tool areas you want to enable. Start with read-only access if you only need to review information.

The endpoint is `https://app.helpwell.ai/mcp`, using Streamable HTTP with OAuth and PKCE. Available tools depend on your workspace, role, plan and approved tool areas. You can change or revoke the connection in HelpWell's **Settings → AI assistants**.

## Example prompts

- Summarize my help desk inbox and draft replies for the oldest support tickets without sending them.
- Find unanswered live chat support questions and suggest knowledge base articles to fill the gaps.
- Review support desk response times and unresolved conversations from the last 30 days.
- Draft help docs explaining our SaaS onboarding flow, using verified product information.
- Draft an email marketing newsletter from these release notes and preview the eligible audience.
- Design a SaaS welcome journey and test the email marketing automation before publishing.
- Check our Resend email setup and list remaining configuration steps.
- Find our Stripe integration help docs and draft a billing support reply using only verified information.

The `/helpwell:triage`, `/helpwell:knowledge` and `/helpwell:marketing` commands provide starting points for these tasks.

## Requirements and limits

A HelpWell account and workspace are required. Features depend on your plan and configuration. Email delivery uses your own configured Resend account; Stripe workflows depend on your configured Stripe integration. The connector does not provide unrestricted access to either provider. AI-assisted features may require the workspace's AI configuration.

This extension does not automatically publish articles, activate marketing automation or send customer email. Actions still follow the permissions, confirmations and feature limits enforced by HelpWell and your MCP client.

The extension passes `gemini extensions validate` using Gemini CLI 0.64.0. End-to-end OAuth has been verified with Claude and Vercel; Gemini-specific authenticated tool execution is not yet independently verified.

## About and support

- Creator: Workado, LLC
- Publisher contact: Justin McGill, justin@brandwell.ai
- Support: support@helpwell.ai
- Website: https://helpwell.ai
- [Connection guide](https://docs.helpwell.ai/getting-started/ai-assistants)
- [Knowledge base](https://docs.helpwell.ai)
- [Privacy](https://helpwell.ai/privacy/)
- [Terms](https://helpwell.ai/terms/)
- [HelpWell open-source project](https://github.com/ChainAI-Org/helpwell)

Copyright 2026 Workado, LLC. This connector configuration is provided for connecting to HelpWell; use of the hosted service is governed by its terms.
