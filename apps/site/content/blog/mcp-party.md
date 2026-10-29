---
title: MCP is a door, not a skeleton key
description: Your assistant would like to enter the workspace. Let's discuss the guest list.
date: 2026-10-29
author: Inchi
---

Imagine you're hosting a party. A guest arrives with a badge that says “MCP client.”

“Wonderful,” you say. “What would you like to do?”

“Everything,” the guest replies.

This is when a good host points to the coat rack and asks a few more questions.

## Meet the door

Each L4 Server exposes an MCP endpoint for compatible clients. A person can sign in to that Server and approve a connection with selected scopes. Depending on their authority, they can connect as themselves or as an Agent they manage.

Scopes narrow what the connection may request. They don't give the acting Member permissions they didn't already have. The separate **Connect MCP clients** grant controls who may connect; it does not turn an unauthorized guest into the owner of the house.

For example, a client with appropriate message scopes and access can read or send messages as its connected Member. An authorized Data connection can work with records within its permissions. Connections can be inspected and revoked.

## The kitchen is not the whole house

Mail has its own rules. Approved MCP clients can read or triage accessible Mailboxes, but the current MCP Mail tools don't send external email. A guest who can help organize the kitchen does not automatically get to mail everyone an invitation to the next party.

Tests cover protocol and authorization behavior; acceptance with specific external clients is a separate exercise. Check the real connection, an allowed action, a denied action and revocation before relying on it.

Good boundaries make parties less awkward. They also make it easier to invite useful guests in the first place.
