# Mission 8 — Final Report and Submission

## 1. Task / Objective

The objective of Mission 8 is to review my Digital Detective assignment, verify that all missions and required programs are present, test the programs again, inspect my Git commit history, and prepare my GitHub repository for final submission.

## 2. Work Completed

### Task 8.1 — Review Repository Structure

I verified the repository structure using:

`git ls-files | sort`

The repository contains all nine mission directories, numbered from Mission 0 through Mission 8.

Each mission has its own `README.md` file. The repository also contains the Python programs and Terminal practice files created during earlier missions.

Important files include:

- `README.md` — Main project overview and mission index.
- `mission-04-programs/hello.py` — First Python program.
- `mission-05-numbers-data/number_converter.py` — Decimal number converter.
- `mission-06-git-github/README.md` — Git and GitHub activities.
- `mission-07-networking/README.md` — Network tests and explanations.
- `mission-08-final-report/README.md` — Final assignment report.

### Task 8.2 — Verify Git History

I ran:

`git log --oneline -15`

The Git history showed the commits created throughout the assignment.

| Mission | Commit | Description |
|---|---|---|
| Mission 0 | `f6827f3` | Repository setup |
| Mission 1 | `a7c1be4` | Computer basics and IPOS |
| Mission 2 | `f945871` | Terminal operations |
| Mission 3 | `bd63039` | Operating system and file management |
| Mission 4 | `74a8801` | Compilers, interpreters, and Python |
| Mission 5 | `e052327` | Number systems and converter |
| Mission 6 | `e28d035` | Git and GitHub collaboration |
| Mission 7 | `0708b31` | Networking and website communication |

There were additional documentation commits during Mission 6.

The separate commits make the development history easier to review.

### Task 8.3 — Verify Python Programs

I reran the Python programs to check that they were still working.

**Program 1 — Hello Python**

Command:

`python3 mission-04-programs/hello.py`

Observed output:

```text
Hello from Python
```

Result: Successful.

**Program 2 — Number Converter**

Command:

`python3 mission-05-numbers-data/number_converter.py`

Test input: `13`

Observed output:

```text
Binary: 0b1101
Hexadecimal: 0xd
```

Result: Successful.

Both programs produced the expected outputs during the final test.

### Task 8.4 — Review Documentation

I reviewed the root README and updated it with a learning summary, topics explored, program-running instructions, and the mission progress checklist.

I also corrected outdated commit and push status information in several earlier mission READMEs.

### Task 8.5 — Check GitHub Collaboration

During Mission 6, I created a branch named `update-about` and opened Pull Request #1.

Pull Request:

https://github.com/jaydeep83721-dev/digital-detective-8530/pull/1

The Pull Request remains open and unmerged because the assignment instructs me to merge only when requested.

## 3. Commands / Tools Used

| Command or Tool | Purpose |
|---|---|
| `git ls-files` | Display files tracked by Git. |
| `sort` | Arrange the file list alphabetically. |
| `git log --oneline` | Review commit history. |
| `git status` | Check branch and working-tree status. |
| `git diff --check` | Detect whitespace errors in changes. |
| `python3` | Execute and verify Python programs. |
| Visual Studio Code | Review and edit documentation. |
| GitHub | Host and review the completed assignment. |

## 4. My Understanding

This assignment connected several important computer science concepts through practical activities.

I learned how computer hardware and software work together, how an operating system manages programs and files, and how Terminal commands interact with the system.

Writing Python programs helped me understand how instructions are executed and how numbers and text are represented digitally.

Using Git and GitHub taught me how to track changes, organise my work into commits, use branches, and propose changes through Pull Requests.

Finally, the networking mission helped me understand how DNS, routers, protocols, clients, and servers enable communication across the Internet.

## 5. Difficulties Faced

One challenge during the assignment was understanding the difference between the Git working directory, staging area, and commit history.

I also encountered credential-helper warnings during some Git push operations.

During the final review, I noticed that several README files still contained outdated submission status information.

## 6. How I Resolved Them

I practised staging and committing individual files and checked the repository using `git status` and `git log`.

Although the credential-helper warnings appeared, the actual Git pushes succeeded, which I verified through the push output and the synchronized branch status.

I corrected the outdated documentation and tested my Python programs again before preparing the final report.

## 7. Evidence / Files

Evidence of the completed work is available in the GitHub repository:

https://github.com/jaydeep83721-dev/digital-detective-8530

The repository includes:

- README documentation for every mission.
- Python source files and verified program outputs.
- Terminal practice files.
- Git commit history.
- A GitHub Pull Request demonstrating branch-based collaboration.
- This final report.

I avoided including private computer, account, and network information in the submitted documentation.

## 8. Commit Details

**Branch:** `main`

**Mission 8 final commit message:** `Finalize Digital Detective assignment`

**Final commit hash:** To be recorded after committing.

**Final push status:** To be confirmed after pushing to GitHub.

**Repository:**

https://github.com/jaydeep83721-dev/digital-detective-8530
