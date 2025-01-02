---
type: SoftwareNote
title: Environmental Variables
modificationDate: 2024-12-19 08:20
tags:
  - Bash
  - Variables
  - Environmental
mastered: false
created: 2025-01-01T17:42
updated: 2025-01-02T12:48
---

# What are environmental variables?

Environmental variables are a type of variable that are available to *all* programs that we run within our shell.

## Viewing environmental variables

You can view your current environmental variables by using the command `env`.

## Setting an environmental variable

You can set an environmental variable by using the `export` command:

```bash
export NAME="Ronald"
```

Once we set an environmental variable in our shell, we can use it as before:

```bash
echo $NAME
# Ronald
```


