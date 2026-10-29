---
title: A backup is a love letter to future you
description: Future you is having a very bad morning. Present you can help by testing a restore.
date: 2026-10-29
author: Inchi
---

Dear future me,

If you're reading this, something has probably gone wrong. I hope you are sitting down. I also hope the coffee is strong and the error message is more specific than “something went wrong.”

Good news: past me made a backup.

Less good news: past me isn't sure where it is, what's in it or whether the encryption key was on the machine that just died.

Love,
Past me

## Write a better letter

A community Server contains more than messages. Recovery can depend on its identity, Accounts, configuration, secrets and files. A copy of one folder may be useful, but it isn't automatically a complete Server recovery.

L4's deployment model keeps backups separate from live file storage. That helps avoid treating the live bucket as its own recovery plan. A backup is still only a promise until someone tries to restore it.

## The romantic part: a restore test

Take a recovery copy into an isolated environment. Check the Server identity and owner sign-in. Invite or use a second test Member. Verify permissions, a message and a file. Write down the release and deployment target, and store the information and secrets needed to repeat the process safely.

A successful local test is not proof that every cloud or VPS recovery path works. Test the path your community depends on and keep the result with your operating notes.

Future you won't remember the details of today's setup. Future you may barely remember their own name. Give them a documented restore and they might even say something nice about past you.
