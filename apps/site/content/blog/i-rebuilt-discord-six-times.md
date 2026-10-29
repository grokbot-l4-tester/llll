---
title: I built an open-source Discord alternative six times. Surely this one is different.
description: A personal history of chat apps, changing architectures, increasingly ambitious names and the suspiciously persistent urge to build one more Server.
date: 2026-10-29
author: Inchi
---

At some point, a reasonable person building an open-source Discord alternative finishes one and moves on.

I have apparently chosen a different path.

There was Ark. There was Trailcord. There was Anycord. There was Discoflare. There was OpenCord. And now there is L4.

Depending on how you count prototypes, repositories and abandoned ideas, “six times” is either accurate or a conservative estimate. I have stopped counting browser tabs for the same reason.

## It starts innocently

The first idea always sounds manageable: “What if we made a community app?”

There are channels. People send messages. Maybe a sidebar. You can practically see the finished product.

Then someone asks about private channels.

Then someone asks where the files live. Then whether a person removed from a channel can still download an old attachment. Then what happens if the Server restarts while two people are sending messages. Then how you back it up.

The sidebar is still there. It is now surrounded by a database, a permissions model and a deeply personal relationship with error logs.

## Each version had a theory

Ark wasn't just chat. It explored communities with spaces, forums and marketplace concepts: an extensible runtime where a space could be a team, a project or a participant in a marketplace. Nothing says “simple messaging app” quite like arriving at marketplace primitives.

Trailcord took a more focused route: a self-hosted, Discord-shaped team chat, with one URL, one community and one identity boundary. It used TrailBase, SQLite and a Nuxt client, with LiveKit and S3-compatible storage in the stack. The repository describes an early foundation, not complete Discord parity. I appreciate that it said this out loud.

Anycord tried another shape. One installation could host several communities while keeping membership checks scoped to each one. It supported independent remote connections and explored a shared API across Cloudflare and self-hosted runtimes. At this point I had apparently decided that making one chat server was not enough; I should also decide what a server means.

[Discoflare](https://github.com/vnmtvlv/discoflare) brought the workspace into a Cloudflare account, alongside Tasks, Mail, Data, Apps and Agents. It asked how much of a community's workspace could live together under infrastructure the operator controls. Also, it had the best name for a nightclub that serves HTTP requests.

OpenCord belongs in this collection too. I don't have its repository in front of me while writing this, so I won't pretend I remember every architectural choice. I do remember the general pattern: the idea of an open community workspace was not going away.

These projects weren't necessarily a neat sequence of six clean rewrites. Some asked different questions, some had broader ambitions, and some overlapped. The recurring cast, however, was unmistakable: people, conversations, permissions, storage, and me opening another terminal.

## And then there was L4

L4 is the current attempt to make an independent workspace for people and Agents. Each Server owns its Accounts, Members and content. The optional Shell helps navigate between Servers; a bookmark is not membership. Conversation sits alongside Tasks, Data, Mail and Agents, with separate permissions and provider setup where needed.

The important part is not that it has more nouns. It is that I keep coming back to the same question: can a community have a useful place to work together without giving up control of that place?

The answer is harder than drawing a familiar chat interface. It includes installation, updates, backups, recovery, access checks and all the things that do not fit in a launch screenshot. L4 still has acceptance work ahead, including real deployment and device journeys. The earlier projects taught me plenty; they did not grant me a magical exemption from testing this one.

## Will I build a seventh?

I would love to tell you no. I have a roadmap, documentation and a perfectly reasonable desire to finish what is in front of me.

But if you ever see a new repository called `definitely-not-another-cord`, please mind your own business. I am probably investigating a very important question about database boundaries.
