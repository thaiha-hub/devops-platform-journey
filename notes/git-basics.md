# Basics of Git

Git is a tool that tracks changes in your files over time. It lets you experiment safely, go back to older versions, and collaborate with others without breaking things.

## Worktree vs branches

### Branch

A **branch** is a separate line of work in Git.

Use a branch when you want to work on a new feature, bug fix, or experiment without changing the main code directly.

Example:

```bash
git switch -c feature-linux-notes
```

This command creates a new branch called `feature-linux-notes` and switches to it.

### Worktree

A **worktree** is another folder connected to the same Git repository.

It lets you work on more than one branch at the same time without switching branches in the same folder.

Example:

```bash
git worktree add ../project-hotfix main
```

This creates another folder called `project-hotfix` with the `main` branch checked out.

### Simple Difference

| Branch | Worktree |
|---|---|
| A separate line of development | A separate working folder |
| Used for features, fixes, or experiments | Used when working on multiple branches at once |
| You switch between branches in one folder | You keep branches open in different folders |

### When to Use Branch

Use a **branch** for normal daily Git work.

Example:

```bash
git switch -c feature-readme
git add .
git commit -m "Add README note"
```

This is good when you are learning Git or working on one task at a time.

### When to Use Worktree

Use a **worktree** when you need two branches open at the same time.

Example situation:

You are working on a feature branch, but suddenly you need to fix something on `main`.

Instead of switching branches and disturbing your current work, you can create a new worktree:

```bash
git worktree add ../repo-hotfix main
```

Now you have:

```text
repo/          # your current feature branch
repo-hotfix/   # main branch for quick fix
```

When you are done, clean up the worktree:

```bash
git worktree remove ../repo-hotfix
```

You can also see all your open worktrees with:

```bash
git worktree list
```

### Important Note

The same branch cannot be checked out in two worktrees at the same time. Git blocks this to avoid conflicts — two folders editing the same branch would overwrite each other's changes.

## Summary

- A **branch** is a line of development.
- A **worktree** is a separate folder for working on a branch.
- Start by learning branches first.
- Learn worktrees later when you want to work like a real developer handling several tasks at once.


