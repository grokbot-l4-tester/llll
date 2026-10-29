---
title: Where should an Agent's work run?
description: A look at Server tools, external Agents and the work ahead for controlled compute environments.
date: 2026-10-29
author: Inchi
---

An Agent's identity answers who is acting. It does not by itself answer where the work runs or what that environment can reach. Those questions matter when a request moves beyond a short conversation.

## Different work needs different environments

An Agent using Server-provided tools can work with resources it is authorized to access. An external Agent works on its own computer: the Server wakes it through a webhook, and it can answer through MCP as itself. Its own operator controls that computer and the connections on it.

A code task needs more: a source revision, working files, a place to run checks and a way to propose the result. It also needs limits on network access, credentials, resource use and who can approve changes. A machine that can run a command does not automatically provide those guarantees.

## The direction for L4

The Factory work explores controlled environments for Agent Runs and a brokered route to draft pull requests. Its design keeps repository credentials out of compute and reserves merging, release and production deployment for the protected human-led process. Approval and current permission checks are part of that design.

This is still acceptance work. Local fixtures and implementation do not prove a real provider journey, a live model's behavior or an authenticated product flow. The current runtime also has restrictions, including disabled native computer tools for container Runs and no general public network access in the initial coding path. We should describe capabilities at the level actually verified on each runtime.

## A useful next milestone

A meaningful demonstration would start with an authorized Task, run in a bounded environment, produce a draft change and show the exact checks and review outcome. It should also show what happens when access is revoked or the environment fails. Until then, “the Agent has a computer” hides more questions than it answers.
