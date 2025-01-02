---
type: SoftwareNote
title: Git Log
modificationDate: 2024-12-26 09:26
tags:
  - Git
  - Log
mastered: false
created: 2025-01-01T17:35
updated: 2025-01-02T12:45
---

# Git Log

A Git repot is a list of commits, where each commit represents the *full* state of the repository at a given point in time.

The log `git log` command shows a history of the commits in a repository. This is what makes Git a version control system. With `git log` you can see:

- Who made a commit

- When the commit was made

- What was changed

## Commit hash

Each commit has a unique identifier called a "commit hash". This is a long string of characters that uniquely identifies the commit. Here is an example:

```bash
5ba786fcc93e8092831c01e71444b9baa2228a4f
```

**Important:** Hash == Sha

### What affects a hash

- The commit message

- The author's name and email

- The date and time

- Parent (previous) commit hashes

# Viewing the last commit

In order to view the last commit we can run the following command:

```bash
git log -1
```

