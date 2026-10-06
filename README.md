# Git DevOps Project

**DevOps Internship, Task 4:** Build a Version-Controlled DevOps Project with Git

## Objective

Manage a small DevOps project using Git and GitHub best practices: branching, meaningful commits, pull requests, tags, `.gitignore`, and Markdown documentation.

## Tools Used

* Git
* GitHub
* Git Bash (Windows)

## Branching Strategy

| Branch      | Purpose                                                    |
| ----------- | ---------------------------------------------------------- |
| `main`      | Stable, production-ready code. Tagged for releases.        |
| `dev`       | Integration branch where features are combined and tested. |
| `feature/*` | One branch per feature or change, created from `dev`.      |

## Workflow

1. Initialize the repository and push it to GitHub.
2. Create `dev` from `main`.
3. Create `feature/*` branches from `dev`.
4. Commit small, meaningful changes with clear messages (`feat:`, `docs:`, `chore:`).
5. Open a pull request from `feature/*` into `dev`, then merge.
6. Open a pull request from `dev` into `main`, then merge.
7. Tag the release on `main` (`v1.0.0`).

## What I Did

* Initialized a Git repository and pushed it to GitHub
* Created `main`, `dev`, and feature branches
* Merged changes using pull requests
* Added a `.gitignore` to exclude unwanted files
* Created an annotated tag `v1.0.0` for the release
* Documented Git commands and interview answers in this README

## Git Commands Used

### Setup

```bash
git init -b main
git remote add origin https://github.com/Manoj666333/devops-task-4-git.git
git push -u origin main
```

### Staging and Committing

```bash
git status
git add .
git commit -m "docs: update README"
git log --oneline --graph --all
```

### Branching

```bash
git branch
git checkout -b dev
git checkout -b feature/task-documentation
git push -u origin <branch>
```

### Merging

```bash
git checkout dev
git merge feature/task-documentation
git pull
```

### Tags

```bash
git tag -a v1.0.0 -m "First stable release"
git push origin v1.0.0
git tag
```

### Stash

```bash
git stash
git stash list
git stash pop
```

### Resolving Merge Conflicts

```bash
git merge <branch>

# Edit the conflicting files and remove:
# <<<<<<<
# =======
# >>>>>>>

git add <file>
git commit
```

## Pull Request Steps (GitHub)

1. Open the repository on GitHub.
2. Go to the **Pull requests** tab.
3. Click **New pull request**.
4. Select the **base** branch (target branch).
5. Select the **compare** branch (source branch).
6. Click **Create pull request**.
7. Review the changes.
8. Click **Merge pull request**.

## Tags

| Tag      | Description          |
| -------- | -------------------- |
| `v1.0.0` | First stable release |

