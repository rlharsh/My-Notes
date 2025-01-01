---
type: SoftwareNote
title: Branches
modificationDate: 2024-12-26 12:10
tags: []
mastered: false
created: 2025-01-01T17:35
updated: 2025-01-01T11:37
---

# What is a Branch?

Simply put, a Git branch allows us to keep track of different changes separately.

Let us say that we have a web project that we want to experiment with changing the color scheme. Rather than changing the entire project directly (as of right now, our `master` branch), we could create a new branch called `color_scheme` and work within that branch. When we are done, and if we like the changes we can then **merge** the `color_scheme` branch back into the `master` branch. If we don't like the changes, we can simply delete the `color_scheme` branch.

## Under the hood

A branch is just a named pointer to a specific commit. When we create a new branch, we are creating a new pointer to a specific commit.

## Checking the branch

We can see what branch we are currently working on by running the following command:

```bash
git branch
```

# Default Branch

Git's default branch is `main`. It used to be `master` but was changed to be more "inclusive".

# Renaming a branch

To rename a branch we can run the following command:

```bash
git branch -m oldname newname
```

# Creating A Branch

To create a new branch and not switch to it immediately, run the following command:

```bash
git branch my_new_branch
```

To create a new branch and immediately switch to it, run the following command:

```bash
git switch -c my_new_branch
```

The `switch` command allows us to switch branches, and the `-c` flag tells Git to create a new branch if it doesn't already exist.

When we create a new branch, it uses the *current commit* that we are on as the branch base. For example, if we're on our `main` branch with 3 commits, `A`, `B`, and `C`, and we run `git switch -c my_new_branch`, our new branch will look like this:

[oah2FRD](Images/oah2FRD.md)

# Switching branches

To switch branches, run the following command:

```bash
git switch branch

# or, the old way:
git checkout prime
```

# Log Flags

As we know, `git log` shows us the history of commits in our repo. There are several more flags that can be used to make the output easier to read.

The first of which is `--decorate`. It can be one of:

- `short` (the default)

- `full` (shows the full ref name)

- `no` (no decoration)

# Merge

Once you have completed the work on your branch, you will want to merge back into the main branch so that the changes will make its way to the final product.

## Merge Commits

A merge commit is the result of merging two branches together.

Let's say we start with this:

```text
A - B - C    main
   \
    D - E    vimchadsonly
```

And we merge `vimchadsonly` into `main` by running this while on `main`:

```bash
git merge vimchadsonly
```

The above merge will:

1. find the "merge base" commit, or "best common ancestor" of the two branches. In this case `A`.

2. Replays the changes from `main`, starting from the best common ancestor, into a new commit.

3. Replays the changes from `vimchadsonly` onto `main`, starting from the best common ancestor.

4. Records the result as a new commit, in our case, `F`.

5. `F` is special because it has *two parents*, `C` and `E`.

**After**

```text
A - B - C - F    main
   \     /
    D - E        vimchadsonly
```

## Merge Logs

Output from the `git log --oneline --decorate --graph --parents` command should look something like this:

```bash
*   89629a9 d234104 b8dfd64 (HEAD -> main) F: Merge branch 'add_classics'
|\
| * b8dfd64 fba0999 (tag: 5.8, add_classics) D: add classics
* | d234104 fba0999 (tag: 6.1) E: update contents
|/
* fba0999 1381199 (tag: 3.8, origin/master, origin/main, master) C: add quotes
* 1381199 a21228f (tag: 3.7) B: add titles.md
* a21228f A: add contents.md
```

Each asterisk `*` represents a commit in the repository. There are multiple commit hashes on each line because the `--parents` flag logs the parent hash(es) as well.

## Fast Forward Merge

The simplest type of merge is a [fast-forward merge](https://git-scm.com/docs/git-merge#_fast_forward_merge). Let's say that we start with this:

```text
      C     delete_vscode
     /
A - B       main
```

And we run this while on `main`:

```bash
git merge delete_vscode
```

Because `delete_vscode` has *all the commits* that `main` has, Git automatically does a fast-forward merge. I moves the pointer of the "base" branch to the tip of the "feature" branch:

```text
            delete_vscode
A - B - C   main
```


