---
type: SoftwareNote
title: Gitignore
modificationDate: 2024-12-27 08:34
tags: []
mastered: false
created: 2025-01-01T17:35
updated: 2025-01-01T11:37
---

# Gitignore

Simply put, `.gitignore` allows us to have files in our project's directory that we *don't* want to track with Git.

For instance when working with Python, we probably want to automatically ignore generated files such as `.pyc` and `__pycache__`, or if we are building a server, then we would want to ignore the `.env` files. If working with JavaScript we would probably want to ignore the `node_modules` directory.

Here is an example of a `.gitignore` file, which exists at the root of a repot:

```text
node_modules
```

This will ignore every path containing `node_modules` as a "section". It ignores:

- `node_modules/code.js`

- `src/node_modules/code.js`

- `src/node_modules`

It does *not* ignore:

- `src/node_modules_2/code.js`

- `env/node_modules_3`

## Nested Gitignore

The `.gitignore` file does *not* need to be at the root of our projects. It is also common to have multiple `.gitignore` files in different directories. A nested `.gitignore` file only applies to the directory it is in (and its subdirectories).

# Patterns

It would be useless if `.gitignore` files only accepted exact filepath section names. Luckily we can filter down using the following methods:

## Wildcards

As with most other languages the `*` asterisks serves as a wildcard that will match any number of characters except for a forward-slash (`/`). As an example, we can ignore *all* `.txt` files by using the following pattern:

```text
*.txt
```

## Rooted Patterns

Patterns starting with a `/ `are anchored to the directory containing the `.gitignore` file. For example, this would ignore a `main.py` in the root directory, but not in any subdirectories:

```text
/main.py
```

## Negation

We can negate a pattern by prefixing it with an exclamation mark (`!`). For example if we wanted to ignore all `.txt` files *except* for `important.txt`, we would use the following pattern:

```text
*.txt
!important.txt
```

## Comments

We can also add comments to our `.gitignore` by starting a line with a `#`. For example:

```text
# Ignore all .txt files
*.txt
```

## Order matters

The order of patterns in a `.gitignore` file determines their effect, and patterns can override each other. For example:

```text
temp/
!temp/instructions.md
```

Everything from the `temp/` directory would be ignored *except* for `instructions.md`. However, if the order were reversed, `instructions.md` would be ignored.

## What to ignore

Here are some rules of thumb for coding projects:

1. Ignore things that can be *generated* (e.g. compiled code, minified files, etc.)

2. Ignore dependencies (e.g. `node_modules`, `venv`, `packages`, etc.)

3. Ignore things that are personal or specific to how you like to work (e.g. editor settings)

4. Ignore things that are sensitive or dangerous (e.g. `.env` files, passwords, API keys, etc.)


