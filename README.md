## Feature 3 
Add Main Section to the code 

# Git Workflow Overview

This repository demonstrates a complete Git workflow including branching, pull requests, rebasing, cherry-picking, squashing commits, and release tagging.

---

## Initial Setup

- Created `main` branch → added `main.txt`
- Created `develop` branch from `main` → added `develop.txt`
- Created `commit-msg` file in .git/hooks for commit message hook. 

---

## Feature 1 (f1)

- Created from `develop`
- Added: `first.txt`, `second.txt`, `third.txt`
- Pushed branch and raised PR
- Merged into `develop`

---

## Feature 2 (f2)

- Created from `develop`
- Added: `nav.txt`, `search.txt`
- Pulled latest changes from `develop`
- Raised PR → merged into `develop`
- `develop` now contains both **f1** and **f2** changes

---

## Release v1.0.0

- Raised PR from `develop` → merged into `main`
- Pulled latest changes locally
- Added tag on `main`:

  v1.0.0

---

## Feature 3

- Created from `develop`
- Added `README` file
- Raised PR → merged into `develop`

---

## Feature 4

- Created from `develop`
- Cherry-picked `README` commit from Feature 3
- Added commits:
  - `bottom`
  - `footer`
  - `footer_styles`
- Removed last commit using interactive rebase (`-i drop`)
- Re-added `footer_styles`
- Squashed `bottom`, `footer`, and `footer_styles` into a single commit using interactive rebase
- Raised PR → merged into `develop`

---

## Final Merge

- Raised PR from `develop` → merged into `main`
- Pulled all latest changes locally for both `main` and `develop`

---

## Concepts Covered

- Branching strategy (`main`, `develop`, feature branches)
- Pull Requests (PR workflow)
- Merging branches
- Cherry-pick commits
- Interactive rebase (drop, squash)
- Release tagging (`v1.0.0`)
- Syncing local and remote branches

---

This project provides a clear example of structured Git workflow from feature development to production release.