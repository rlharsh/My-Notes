---
type: SoftwareNote
title: Path
modificationDate: 2024-12-19 08:38
tags: []
mastered: false
created: 2025-01-01T17:42
updated: 2025-01-01T17:42
---

# What is PATH?

The `PATH` variable is a variable that is "built-in" to our shell.

## Why is PATH important?

If it weren't for the `PATH`, we would have to remember the filesystem path of every executable that we wanted to run. For instance if we wanted to run the `ls` command to view the contents of a directory, we'd have to run `/bin/ls` (or whatever the location of the `ls` executable is on our system).

## Adding a directory to PATH

In order for us to add a directory to our `PATH` we need only run an `export` command (see [Environmental Variables](RonaldsSoftwareNotes/Environmental%20Variables.md)).

```bash
export PATH="$PATH:/path/to/new"
```

The `$PATH` part is a reference to the existing `PATH` variable. The `:` separates the existing directories from the new directory that we are adding.


