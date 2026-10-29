---
title: How an L4 Server gets installed on Cloudflare
description: A look at the published release, resources and owner setup behind the Cloudflare installer.
date: 2026-10-29
author: Inchi
---

Installing a workspace should not require an operator to connect a source repository or build the app on their laptop. L4's Cloudflare installer is designed around a published Server release and the owner's own Cloudflare account.

## From release to Server

In the Cloudflare tab of `/create`, an operator selects an account, names the Server and chooses a published release. The installer uses an authorized Cloudflare connection to create the Server's resources. It checks the release checksums before allocating them; a missing or mismatched checksum stops the install.

A Server gets its own Worker, database, tickets storage and Durable Objects. Where R2 is enabled, private files and backups use separate buckets. The installer can also use the supported basic storage path when R2 is unavailable. The resources belong to the operator's account, so Cloudflare's own limits and charges still apply.

The installer generates a Server UUID and uses it across resource names and Server identity. The owner then completes setup on the Server's own origin and creates the local owner Account. That Account belongs to this Server, not to a shared L4 identity service.

## What about updates?

The owner can let the Server keep Cloudflare access, encrypted with its Server secret, to perform supported updates. That option is on by default during installation. Updates use published, checksum-verified releases; an operator should also maintain and verify backups before relying on a recovery plan.

This installer is distinct from L4's own development deployment process. Official site and preview builds go through Git and Workers Builds; the customer installer works with immutable published artifacts in the customer's account.

## Verify the whole journey

An install is more than a successfully created Worker. Claim the owner Account, invite a second person, exchange a message and a file, reload and reconnect. Try the direct Server address and the Shell. Provider and browser behavior can differ, so record the environment and result rather than assuming one successful step proves the whole journey.
