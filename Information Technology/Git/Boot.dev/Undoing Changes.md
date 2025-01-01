---
type: SoftwareNote
title: Undoing Changes
modificationDate: 2024-12-26 13:43
tags: []
mastered: false
created: 2025-01-01T17:35
updated: 2025-01-01T11:37
---

# Undoing Changes

Git has the ability to undo changes. 

## Git Reset Soft

The git reset command can be used to undo the last commit(s) or any changes in the index and the worktree.

```bash
git reset --soft COMMITHASH
```

The `--soft` option is useful if you just want to go back to a previous commit, but keep all of your changes. Any changes will be uncommitted and staged, while uncommited changes will remain staged or unstaged as before.

## Git Reset Hard

If you don't want to keep the changes you can reset to a previous commit by using the following command:

```bash
git reset --hard COMMITHASH
```

This is useful if you just want to go back to a previous commit and discard all the changes.

### Danger

This command can be very dangerous. If we were to simply delete a committed file, it would be trivially easy to recover because it is tracked in Git. However, if we used `git reset --hard` to undo committing that file, it would be deleted for good.

