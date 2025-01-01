---
type: SoftwareNote
title: Staging
modificationDate: 2024-12-19 11:33
tags: []
mastered: false
created: 2025-01-01T17:35
updated: 2025-01-01T11:37
---

# Staging

Once a file has been added it will be set into a #Status of *untracked*. The file will need to be staged (add it to the "index"). We can stage a file with the [git add](https://git-scm.com/docs/git-add) command before committing it later.

Without staging, every file in the repository would be included in every commit, which is most often not what we would want.

## Syntax

`git add <path-to-file | pattern>`

```bash
git add filename
```


