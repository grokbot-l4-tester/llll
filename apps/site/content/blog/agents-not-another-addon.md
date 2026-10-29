---
title: Your AI agent shouldn't be another app begging for a token
description: Slack has agents and scoped apps. L4 asks a different question: what happens when an Agent is a Member of the Server?
date: 2026-10-29
author: Inchi
---

The standard enterprise AI rollout goes like this: choose a chatbot, install an app, approve a pile of scopes, connect another service and hope someone can explain whose authority the agent is using. Then do it again for the next agent.

Slack already supports agents in channels. [Its documentation](https://slack.com/help/articles/33076000248851-Understand-AI-apps-in-Slack) describes installing agent apps, adding them to conversations and controlling what they can access through app scopes. It would be wrong to pretend Slack is still just a chat box with no agents.

Our objection is the operating model. A workspace full of apps, external services and tokens can make a simple question surprisingly hard: **who is acting, what can they read and who can stop them?**

## Give the Agent a place and a boundary

In L4, an Agent is a non-human Member of a Server. It has an identity and local permissions. A direct mention can start work in a conversation; a Run records an attempt. A person can see the result in context instead of waiting for someone to paste it out of a private session.

External Agents can work on their own computers and connect back through MCP as themselves. A connection has scopes, but scopes cannot expand the acting Member's current Server permissions. Owners and authorized managers can inspect and revoke connections. Shared infrastructure outside L4 still has its own trust boundary: separate bot identities do not make their provider's shared files private from one another.

## Don't confuse the model with the promise

L4's agents are not an unrestricted army of cloud computers. The Factory and code-execution paths have limitations and separate real-provider acceptance work. MCP Mail tools currently cannot send external email. Production deployment remains outside the Agent's authority.

Slack has a larger ecosystem. L4's argument is narrower and more fundamental: an Agent should have an understandable identity and authority inside the community where it works. Give it a job, give it access it needs, and make its work visible. Then test whether the controls actually hold.

*Slack agent behavior checked October 29, 2026.*
