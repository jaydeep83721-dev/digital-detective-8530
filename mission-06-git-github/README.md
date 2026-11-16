# Mission 6 — Git and GitHub

## 1. Task / Objective

The objective of Mission 6 is to understand version control, practise the Git workflow, create and use branches, and learn how Pull Requests support collaboration.

## 2. Work Completed

### Task 6.1 — Understand the Basic Git Workflow

I inspected my repository status, staged a specific README file, committed the changes, and reviewed my Git history.

| Git Operation | Command | Purpose |
|---|---|---|
| Check repository status | `git status` | Displays the current branch and file changes. |
| Stage selected changes | `git add` | Prepares specific changes for the next commit. |
| Create a commit | `git commit` | Records staged changes in the repository history. |
| View commit history | `git log` | Displays previously recorded commits. |

**Commands used:**

```bash
git branch
git status
git log -5 --oneline

git add mission-06-git-github/README.md
git commit -m "Document basic Git workflow"
git log -2 --oneline
```

**Observation:**

Initially, my repository was on the `main` branch and synchronized with `origin/main`.

I modified the Mission 6 README, staged the changes, and created commit `f5a839c`.

I learned that staging prepares changes, while committing records them in Git history.

### Task 6.2 — Create and Use a Branch

I created a new branch named `update-about` to make changes without immediately modifying the main branch.

**Commands used:**

```bash
git switch -c update-about
git branch
```

I opened the root `README.md` and added a new section titled **My Learning**.

The section describes my learning experiences involving:

1. Operating systems, processes, and file permissions.
2. Terminal commands and file management.
3. Python and number systems.

After saving the README, I staged and committed the changes.

```bash
git add README.md
git commit -m "Add learning summary to project README"
git push -u origin update-about
```

**Observation:**

The new branch was successfully created and published on GitHub.

Branch name: `update-about`

Commit: `491b7cd`

The changes were isolated from the `main` branch.

### Task 6.3 — Create a Pull Request

I created a Pull Request to propose merging the README changes from `update-about` into `main`.

**Pull Request Details:**

- PR Number: #1
- Title: Add My Learning section to project README
- Base Branch: `main`
- Compare Branch: `update-about`
- Changed File: `README.md`
- Status: Open — Not merged

**Pull Request URL:**

https://github.com/jaydeep83721-dev/digital-detective-8530/pull/1

**Steps Performed:**

1. Opened my GitHub repository.
2. Selected the `update-about` branch for comparison with `main`.
3. Created a Pull Request with a descriptive title and summary.
4. Reviewed the changes proposed in the root README.
5. Left the Pull Request open because the assignment specifies merging only when instructed.

**What I Learned:**

A branch allows developers to work on changes separately from the main codebase.

A Pull Request allows proposed changes to be reviewed and discussed before they are merged.

This workflow helps teams collaborate while keeping the main branch stable.

### Task 6.4 — Git Command Glossary

| Git Operation | Command | Explanation |
|---|---|---|
| Initialise repository | `git init` | Creates a new Git repository. |
| Check status | `git status` | Displays modified, staged, and untracked files. |
| Stage changes | `git add` | Selects changes for the next commit. |
| Commit changes | `git commit` | Saves a snapshot of staged changes. |
| View history | `git log` | Displays previous commits. |
| Create branch | `git branch <name>` | Creates a new branch. |
| List branches | `git branch` | Displays local branches. |
| Switch branches | `git switch <name>` | Changes the active branch. |
| Publish changes | `git push` | Uploads commits to a remote repository. |
| Retrieve remote changes | `git fetch` | Downloads remote updates without merging them. |
| Update local branch | `git pull` | Fetches and integrates remote changes into the current branch. |

## 3. Commands / Tools Used

- Git — Version control and commit management.
- GitHub — Repository hosting and Pull Request creation.
- Visual Studio Code — Editing Markdown documentation.
- macOS Terminal — Executing Git commands.

## 4. My Understanding

Git is a version control system that records the history of changes made to project files.

The staging area allows developers to select which changes should be included in a commit.

Branches provide separate lines of development, allowing changes to be prepared without immediately modifying the main branch.

GitHub Pull Requests provide a way to propose, inspect, and discuss changes before merging them.

## 5. Difficulties Faced

Initially, I was unsure where to create a Pull Request because I was looking for the option inside Visual Studio Code.

I also encountered a Git credential-helper path warning during some GitHub push operations.

## 6. How I Resolved Them

I opened my repository on the GitHub website and used its Pull Request interface to compare the `update-about` and `main` branches.

The Git pushes succeeded despite the credential-helper warning, so it did not prevent the assignment activities from being completed.

## 7. Evidence / Files

The Mission 6 directory contains:

```text
mission-06-git-github/
└── README.md
```

Additional evidence is available in the GitHub repository:

- Commit history demonstrating the Git workflow.
- Published `update-about` branch.
- Pull Request #1 showing the proposed README changes.

## 8. Commit Details

**Task 6.1 commit:** `f5a839c` — Document basic Git workflow

**Task 6.2 commit:** `491b7cd` — Add learning summary to project README

**Mission 6 final documentation commit:** `e28d035`

**Pull Request:** #1 — Open, not merged.

**Final documentation push:** Successfully pushed to GitHub.

**Repository:**

https://github.com/jaydeep83721-dev/digital-detective-8530
