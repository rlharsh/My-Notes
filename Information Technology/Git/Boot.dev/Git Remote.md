---
type: SoftwareNote
title: Git Remote
modificationDate: 2024-12-26 14:22
tags: []
mastered: false
created: 2025-01-01T17:35
updated: 2025-01-01T11:37
---

# Git Remote

Often others may make code changes that we need to accept into our repo. This is where the "distributed version control system" comes from. We can have "remotes", which are just external repos with *mostly* the same Git history as our local repo.

## Adding a Remote

In git, another repo is called a "remote". The standard convention is that when you're treating the remote as the "authoritative source of truth" (such as GitHub) you would name it the "origin".

### Syntax

```bash
git remote add name url
```

### Fetch

Once we setup a remote, we will need to #fetch the contents.

**Syntax**

```bash
git fetch
```

The command above will download all the contents from our remote `.git/objects` directory into our current one.

## Merge

We can also merge branches between local and remote repos.

```bash
git merge remote/branch
```


