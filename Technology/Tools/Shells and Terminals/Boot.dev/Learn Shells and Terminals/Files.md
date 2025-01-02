---
type: SoftwareNote
title: Files
modificationDate: 2024-12-18 13:52
tags:
  - Bash
  - Files
mastered: false
created: 2025-01-01T17:42
updated: 2025-01-02T12:48
---

# The cat command

The `cat` command is used to view the contents of a file. It is short for "concatenate".

```bash
# Print the contents of a file to the terminal
cat file1.txt

# Concatenate the contents of multiple files and print them to the terminal
cat file1.txt file2.txt
```

# Head and Tail

## The head command

The `head` command prints the first `n` lines of a file, where `n` is a number you specify.

```bash
head -n 10 file1.txt
```

If you do not specify a number, it will default to 10.

# More or less

The `more` and `less` commands let you view the contents of a file, one page (or line) at a time.

The `less` command does everything that the `more` command does, but also has more features. As a general rule, you should use the `less` instead of `more` command.

- Passing the `N` argument will display line numbers.

- You can use spacebar to scroll down one page at a time.

- You can go up one page by pressing `b`.

- You can quite by pressing `q`.

# Touch

The touch command is designed to update the access and modification timestamps of a file. By default if a the specified file does not exist, `touch` will create an empty file with the given filename.

```bash
touch new_file.txt
```

You can also create multiple files at once by listing them:

```bash
touch some_file.txt some_other_file.txt
```

# Move

The move command moves a single file, or a directory from one location to another. You can also use it to rename a file or to move it to a different directory alltogether.

### Renaming a file

```bash
mv some_file.txt some_other_name.txt
```

### Moving a file from current directory to another directory

```bash
mv some_file.txt some_directory/some_file.txt
```

### Moving a file from current directory to parent directory

```bash
mv some_file.txt ../some_file.txt
```

### Moving without renaming

```bash
mv some_file.txt some_directory/
```

# Remove

The remove command deletes a file or empty directory:

```bash
rm some_file.txt
```

- You can add a `-r` flag to tell the `rm` command to delete a directory and *all* of its contents recursively.

```bash
rm -r some_directory
```

# Copy

The copy command does you would expect: it copies a file from one location to another.

```bash
cp source_file.txt destination/
```

- You can also copy a directory and all of its contents recursively by adding the `-R` flag.

```bash
cp -R my_dir new_dir
```

# Grep

The `grep` command allows us to search for text within files. 

## Basic usage

The most basic usage of `grep` is to search for a string in a file. For example, if we wanted to search for the word "hello" in the file `hello.txt`, we could run:

```bash
grep "hello" hello.txt
```

This will print out every line in `hello.txt` that contains the word "hello". 

- It is important to remember that `grep` is case-sensitive.

## Grep with multiple files

We can also search multiple files at once. For example, if we wanted to search for the word "hello" in `hello.txt` and `hello2.txt` we could run:

```bash
grep "hello" hello.txt hello2.txt
```

## Recursive search

Furthermore, we can also search an entire directory, including all subdirectories. For example if we wanted to search for the word "hello" in the current directory and all subdirectories, we could run:

```bash
grep -r "hello" .
```

- The `.` is a special alias for the current directory.

# Find

The `find` command is a tool for finding files and directories by name, not their contents.

## Find a file by name

If you are looking for a file named `hello.txt`, you could use the `find` command to search for exactly that title:

```bash
find some_directory -name hello.txt
```

## Pattern search

The `find` command can also search for files that match a pattern. For example, if you wanted to find all files that end in `.txt`, you could run:

```bash
find some_directory -name "*.txt"
```

```bash
# Finda all filenames that contain the word "chad"
find some_directory -name "*chad"
```


