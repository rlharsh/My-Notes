---
type: SoftwareNote
title: Filesystem
modificationDate: 2024-12-17 12:28
tags: []
mastered: false
created: 2025-01-01T17:42
updated: 2025-01-01T11:43
---

# What is a filesystem?

All the data stored on your computer is organized into files and directories. Files and directories are organized into a tree-like structure called a filesystem.

- When you first logon to terminal it will put you in your root directory.

- To get the working directory, make use of the `pwd` (print working-directory) command.

## Absolute vs Relative Paths

```bash
vehicles
├── cars
│   ├── fords
│   │   ├── mustang.txt
│   │   └── focus.txt
```

When inside the top-level `vehicles` directory, the relative path to the `mustang.txt` file is:

```bash
cars/fords/mustang.txt
```

However, when we're inside the `cars` directory, the relative path to the `mustang.txt` file is just:

```bash
fords/mustang.txt
```

Or when inside the `fords` directory, just:

```bash
mustang.txt
```

## Absolute Paths

An absolute path is a path that starts at the root of the filesystem. On Unix-like systems, the root is denoted by a forward slash `/`.

```bash
/vehicles/cars/fords/mustang.txt
```

So, when inside the `fords` directory, you can use either:

```bash
/vehicles/cars/fords/mustang.txt
```

or

```bash
mustang.txt
```


