---
type: SoftwareNote
title: Storing Data
modificationDate: 2024-12-26 09:36
tags:
  - Git
  - Data
  - Storing
mastered: false
created: 2025-01-01T17:35
updated: 2025-01-02T12:45
---

# Storing Data

Git stores an entire *snapshot* of files on a *per-commit* level. 

## Optimization

While it's true that Git stores entire snapshots, it *does* have some performance optimizations so that your `.git` directory doesn't get too unbearably learge.

- Git [compresses and packs](https://git-scm.com/book/en/v2/Git-Internals-Packfiles) files to store them more efficiently.

- Git deduplicates files that are the same across different commits. If a file doesn't change between commits, Git will only store it once.

