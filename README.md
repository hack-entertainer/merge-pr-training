# GitHub PR Playground

A tiny playground for learning real open-source collaboration.

This repo is intentionally simple.
The goal is to practice the mechanics of contributing without process overhead.

You will learn:

* forks
* branches
* commits
* pull requests
* merges
* merge conflicts
* syncing forks

---

# Roles

Typical setup:

```text id="mrh8hf"
maintainer → owns canonical repo
contributors → fork + submit PRs
```

You can simulate this with:

* two GitHub accounts
* two browsers
* two local clones

---

# Basic Flow

```text id="vhxgl7"
fork
→ branch
→ commit
→ push
→ PR
→ review
→ merge
```

That’s most of open source.

---

# Clone Your Fork

```zsh id="hfth6s"
git clone git@github.com:YOUR_USER/REPO.git
cd REPO
```

Add original repo as upstream:

```zsh id="5hgjje"
git remote add upstream \
git@github.com:ORIGINAL_OWNER/REPO.git
```

---

# Create a Branch

```zsh id="7axtj6"
git checkout -b feature/test-change
```

Make edits.

---

# Commit Changes

```zsh id="gkkk3m"
git add .
git commit -m "Describe change"
```

---

# Push Branch

```zsh id="u4r4rx"
git push origin feature/test-change
```

Then open a Pull Request on GitHub.

---

# Sync Your Fork

```zsh id="d7x4lo"
git checkout main
git fetch upstream
git merge upstream/main
git push origin main
```

---

# Merge Conflict Practice

To practice conflict resolution:

1. Two people edit the same line
2. Merge one branch first
3. Merge the second branch

Git will complain.

Resolve manually:

```text id="7d7ocd"
<<<<<<< HEAD
your code
=======
incoming code
>>>>>>> upstream/main
```

Then:

```zsh id="iv4g4d"
git add .
git commit
git push
```

---

# Useful Commands

```zsh id="t0d1rf"
git status
git branch
git remote -v
git log --oneline --graph
```

---

# Project Philosophy

This is a playground.

Keep changes:

* small
* experimental
* easy to review
* easy to delete

Learn by merging things.
