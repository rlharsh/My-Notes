---
type: SoftwareNote
title: Git Config
modificationDate: 2024-12-26 10:18
tags: []
mastered: false
created: 2025-01-01T17:35
updated: 2025-01-01T11:38
---

# Git Config

Git stores author information so that when you're making a commit it can track *who* made the change. Here's how you might update your global Git configuration:

```bash
git config --add --global user.name "ThePrimeagen"
git config --add --global user.email "the.primeagen@aol.com"
```

Taking a look at the command:

- `git config`: The command to interact with your Git configuration.

- `--add`: Flag stating we want to add a configuration.

- `--global`: Flag stating we want this configuration to be stored globally in your  `~/.gitconfig`. The opposite is "local", which stores the configuration in the current repository only.

- `user`: The section

- `name`: The key within the section

- `"ThePrimeagen"`: The value you want to set for the key.

## Viewing the contents of your config:

You can view the contents of your config by using the following command:

```bash
git config --list --local
```

```bash
git config --list --global
```

# Get

As mentioned above, you can use `--list` to see *all* of the configuration values, but the `--get` flag is useful for getting a single value.

```bash
git config --get <key>
```

Keys are in the format `<section>.<keyname>`. For example:

- `user.name`

- `webflyx.ceo`

# Unset

The `--unset` flag is used to remove a configuration value. For example:

```bash
git config --unset <key>
```

# Duplicates

As with a dictionary values are in a key/value store, and we are not allowed to have duplicate keys. Oddly enough, Git does not cate.

## Unset All

The `--unset-all` flag is useful if we *really* want to purge all instances of a key from our configuration.

```bash
git config --unset-all example.key
```

# Remove a section

The `--remove-section` flag is used to remove an entire section for our Git configuration. For example:

```bash
git config --remove-section section
```

# Locations

There are several locations where Git can be configured.

- **system:** `/etc/gitconfig`, a file that configures Git for all users on the system

- **global:** `~.gitconfig`, a file that configures Git for all projects of a user

- **local:** `.git/config`, a file that configures Git for a specific project

- **worktree:** `.git/config.worktree`, a file that configures Git for part of a project.

Most of the time we will be using `--global` to set things such as our username and email. Other times we will be using `--local` to set project-specific configurations.

## Overriding

If we set a configuration in a more specific location, it will override the same configuratino in a more general location. For example, if we set `user.name` in the local configuration, it will override the `user.name` set in the global configuration.

