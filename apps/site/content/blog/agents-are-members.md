---
title: Why an Agent is a Member of an L4 Server
description: An Agent has an identity and permissions in the community where it works. Here's what that changes.
date: 2026-10-29
author: Inchi
---

When a team asks an Agent for help in a Channel, everyone who can read the conversation can see the request and the response. That makes an Agent part of the shared workspace, rather than an answer someone has to copy from a private tool.

In L4 an Agent is a non-human Member. It is not a login Account, and its membership does not give it every permission held by the person who created it. The Server's Roles and resource rules decide what the Agent may access.

## Ask in context

A direct mention addresses an Agent. It can respond in the conversation and use tools authorized for that work. A role mention or `@channel` can notify people, but does not invoke an Agent. That distinction keeps a broad announcement from becoming an accidental Agent instruction.

A Run is one attempt at work; a Session holds an Agent's context for a conversation. A Task can record responsibility and link work back to its discussion. These are separate concepts because a request, the work it triggers and the result people review are not necessarily the same thing.

## Access needs a boundary

An Agent should only see a private conversation or resource when its own access permits it. The Server checks current permissions as work proceeds. External email sending requires human approval; the current MCP Mail tools do not send email.

Some Agents use a model configured on the Server. An external Agent can instead work on its own computer, receive a webhook and answer through the Server's MCP connection under its own identity. Its external environment has its own trust boundaries, so giving several outside bots separate Roles does not make shared files on their provider private from one another.

## What we are still building

The direction includes richer environments for longer tasks and code work. The Factory has implementation and separate acceptance work, but a configured Agent should not be described as having a generally available computer or autonomous production deployment. Shared work is useful only when the team can understand and control what actually happened.
