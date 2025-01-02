---
type: SoftwareNote
title: Permissions
modificationDate: 2024-12-18 14:34
tags:
  - Bash
  - Files
  - Permissions
mastered: false
created: 2025-01-01T17:42
updated: 2025-01-02T12:49
---

# Users

Unix-like systems support multiple users. Each user has their own home directory, their own files, and their own permissions.

## Sudo

The `sudo` keyword lets us run commands as a "superuser". It's short for "superuser do". In order to use `sudo` we will first need a password with superuser privileges.

# Permissions

In a Unix-like operating system, permissions control who can do what to which files and directories. The permissions of an individual file or directory are visually represented as a 10-character string:

```bash
drwxrwxrwx
```

The first digit in a permissions string signifies whether this is a directory, or a file. If it is represented as a `d`, then it is a file, if it is a `-` then it is a file.

The next `3` groups of `3` signal as follows:

### Group 1 - User

The first group of `3` are the current users permissions.

### Group 2 - Group

The second group of `3` is the group.

### Group 3 - Others

The second group of `3` is others.

### Changing Permissions

The `chmod` command lets us change the permissions of a file or directory. It is short for "change mode".

```bash
chmod -R u=rwx,g=rwx,o=rwx DIRECTORY_NAME
```

# Executables

Files with a `.sh` extension are shell scripts. They are just text files that contain shell commands. You can run a file in your shell by just typing its filepath:

```bash
mydir/program.sh
```

If you are trying to execute a program within the current directory, you need to prefix it with `./`:

```bash
./program.sh
```

# Changing Owner

The `chown` command, which stands for "change owner" allows us to change the owner of a file or directory, and it requires root privileges.

```bash
sudo chown -R root contacts
```

Let's break down this command:

- `sudo` - Run as the root user

- `chown` - Command to change the owner

- `-R` - "Recursive", meaning also apply the changes to everything inside the directory

- `root` - The name of the new owner

- `contacts` - The directory to change the owner of

