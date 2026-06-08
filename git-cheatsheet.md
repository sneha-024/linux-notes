# Git Cheat Sheet

## What is Git?

Git is a distributed version control system used to track changes in files and projects over time.

It helps developers:

* Track changes
* Collaborate with teams
* Restore previous versions
* Manage project history

---

## Git vs GitHub

| Git                  | GitHub                    |
| -------------------- | ------------------------- |
| Version control tool | Cloud platform            |
| Runs locally         | Hosts repositories online |
| Tracks changes       | Stores repositories       |

---

## Common Git Commands

### Initialize Repository

```bash
git init
```

Creates a new Git repository.

---

### Check Status

```bash
git status
```

Shows modified, staged, and untracked files.

---

### Add Files

```bash
git add .
```

Stages all changes for commit.

---

### Commit Changes

```bash
git commit -m "Meaningful commit message"
```

Creates a snapshot of current changes.

Example:

```bash
git commit -m "Added Linux networking cheat sheet"
```

---

### View Commit History

```bash
git log
```

Displays commit history.

Compact view:

```bash
git log --oneline
```

---

### View Differences

```bash
git diff
```

Shows changes before committing.

---

### Push Changes

```bash
git push
```

Uploads local commits to GitHub.

---

### Pull Changes

```bash
git pull
```

Downloads and merges changes from GitHub.

---

## Good Commit Messages

Good:

```text
Added Day 03 process and systemctl notes
Created Linux networking cheat sheet
Updated README with Week 1 summary
```

Bad:

```text
changes
update
final
done
test
```

---

## Git Workflow

```text
Edit Files
    ↓
git status
    ↓
git add .
    ↓
git commit -m "message"
    ↓
git push
```

---

## Key Takeaways

* Git tracks file changes over time.
* Commits act as project checkpoints.
* GitHub stores repositories online.
* Meaningful commit messages improve project history.
* Version control is essential for DevOps and software development.
