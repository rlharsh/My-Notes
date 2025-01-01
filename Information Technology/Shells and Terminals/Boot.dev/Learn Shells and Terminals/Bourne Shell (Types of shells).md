---
type: SoftwareNote
title: Bourne Shell (Types of shells)
modificationDate: 2024-12-19 08:17
tags: []
mastered: false
created: 2025-01-01T17:42
updated: 2025-01-01T11:43
---

# Types of shells

- Ubuntu on WSL: [Bash](https://en.wikipedia.org/wiki/Bash_(Unix_shell)) shell.

- macOS: [Zsh](https://en.wikipedia.org/wiki/Z_shell) shell.

- Linux: Bash, Zsh, FIsh

## Differences between shells

- `sh` - The Bourne shell. This is the original Unix shell and is [POSIX-compliant](https://en.wikipedia.org/wiki/POSIX). Very basic and doesn't have many quality-of-life features.

- `bash` - The Bourne Again shell. The most popular shell on Linux. It builds on `sh`, but also has added features.

- `zsh` - The Z shell. The most popular shell on macOS. Like `bash`, it does what `sh` can do, but also has added features.

Both `zsh` and `bash` are "sh-compatible" shells, meaning they can run `.sh` scripts, but they also have added features that generally make them more pleasant to use. 

## Configuration files

The configuration files for each shell type can be found below:

### Bash

```bash
.bashrc
```

### Zsh

```bash
.zshrc
```

The configuration files for each of these can be found in the home directory:

```bash
~/.bashrc
~/.zshrc
```

**IMPORTANT:** The configuration file runs automatically when you start a new shell session.

