---
title: A backup is not a second running Server
description: What an independent workspace needs to recover, and why its backup destination is separate from live files.
date: 2026-10-29
author: Inchi
---

A Server can work perfectly today and still need a recovery plan for tomorrow. A backup is a copy used for recovery. It is not a live replica and it should not be confused with the bucket holding the files people use every day.

## What needs to survive?

A useful recovery plan covers more than chat messages. Server identity, Accounts, configuration, secrets and content belong together. Restoring content without the identity or the secrets it depends on may leave a workspace that looks familiar but cannot operate as the same Server.

L4 gives each Server a persistent UUID. The recovery objective is to bring back the Server and its data with that identity intact, then check that Members and their permissions still behave as expected.

## Keep the copy separate

On the Cloudflare path, a backup bucket is separate from the live private files bucket. Server removal must not delete the backup destination. Separation reduces the chance that an operation on live resources also destroys the recovery copy; it does not by itself prove that a backup can be restored.

## Practice recovery

Before calling a backup plan complete, make a copy, restore it into an isolated environment and check the result: identity, owner sign-in, a second Member, permissions, a message and a file. Record which release and deployment target were used. Protect the recovery material and secrets with the same care as the live workspace.

L4's stabilization work calls for restore acceptance on actual deployment targets. We will report those results separately from tests and fixture coverage. A backup's value is not that a button said it succeeded; it is that you can recover the community when you need it.
