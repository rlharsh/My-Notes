---
type: SoftwareNote
title: Rebase
modificationDate: 2024-12-26 13:02
tags:
  - Git
  - Rebase
mastered: false
created: 2025-01-01T17:35
updated: 2025-01-02T12:45
---

# Rebase

"Rebase vs Merge" is a heavily debated topic in the Git world.

Rebase in Git moves or replays commits from one branch onto another, creating a linear history. It rewrites commit history by applying each commit from the source branch onto the target branch.

Say we have this commit history:

```text
A - B - C    main
   \
    D - E    feature_branch
```

We are working on `feature_branch`, and want to bring in the changes our team added to `main` so we're not working with a stale branch. We could merge `main` into `feature_branch`, but that would crete an additional merge commit. Rebase avoids a merge commit by replaying the commits from `feature_branch` on top of `main`. After a rebase, the history will look like this:

```text
A - B - C         main
         \
          D - E   feature_branch
```

- Both rebase and merge can be used to integrate changes from one branch into another.

- Merge can add an additional commit, rebase does not.

## Running Rebase

To use rebase to bring in changes onto a current branch (let's pretend we're on one called `jdsl`), we would run this while on the `jdsl` branch:

```bash
git rebase main
```

This command will do the following:

1. Checkout the latest commit from `main` into a temporary location

2. Replay each commit from `jdsl` one at a time onto this temporary location

3. Update the `jdsl` branch to point to the last replayed commit in the temporary location, making this the new permanent `jdsl`.

4. The rebase does *not* affect the `main` branch; `jdsl` now includes all changes from `main`.

## When to Rebase

An advantage of merge is that it preserves the true history of the project. It shows when branches were merged and where. One disadvantage is that it can create a lot of merge commits, which can make the history harder to read and understand.

A linear history is generally easier to read, understand, and work with. Some teams enforce the usage of one or the other on their `main` branch, but generally speaking, you'll be able to dwhatever you want with your own branches.

### Warning

You should *never* rebase a public branch (like `main`) onto anything else.

