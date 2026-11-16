
# Mission 2 — Become Comfortable with the Terminal

## Objective

To understand and practise basic Terminal operations, safe file management, command-line flags, pipes, and package managers.

## Task 2.1 — Explore Basic Terminal Operations

I used the macOS Terminal to perform basic file and directory operations inside my Digital Detective repository.

### Commands, Purposes and Observations

| Operation / Command | What It Does | What I Observed |
|---|---|---|
| `pwd` | Displays the current directory path. | Showed the absolute path of my Digital Detective repository. |
| `ls` | Lists files and folders. | Displayed the README, evidence folder, and mission directories. |
| `ls -l` | Displays detailed file information. | Showed permissions, file sizes, owners, and modification dates. |
| `cd ..` | Moves to the parent directory. | Moved from the repository to the Documents directory. |
| `mkdir` | Creates a directory. | Created a terminal-practice folder inside Mission 2. |
| `touch` | Creates an empty file if it does not exist. | Created notes.txt with a size of 0 bytes. |
| `cp` | Copies a file. | Created a copy named notes-copy.txt. |
| `mv` | Moves or renames a file. | Renamed notes-copy.txt to notes-backup.txt. |
| `cat` | Displays a file's contents. | Initially displayed nothing because notes.txt was empty. |

### Learning Outcome

I learned how to navigate directories, inspect files, create folders, and manage files using Terminal commands.

---

## Task 2.2 — Practise File Changes Safely

### Activity

I created a practice directory inside Mission 2 and performed file-writing and backup operations.

Practice directory: `mission-02-terminal/terminal-practice/`

### Commands Used

```bash
echo "This is my first line of text." > notes.txt
echo "This is my second line of text." >> notes.txt
cat notes.txt

cp notes.txt notes-copy.txt
mv notes-copy.txt notes-backup.txt

cat notes-backup.txt
ls -l
```

### Observed Output

```text
This is my first line of text.
This is my second line of text.
```

Both notes.txt and notes-backup.txt contained the same two lines and had a size of 63 bytes.

### Questions and Answers

**Q1. What is the difference between replacing a file's contents and adding text to the end?**

The `>` operator replaces the existing contents of a file, while `>>` appends new text without removing the previous content.

**Q2. What is the difference between copying a file and moving a file?**

The `cp` command creates a duplicate while preserving the original file. The `mv` command moves or renames a file without leaving the original at its previous location.

**Q3. What information does the current-directory display provide?**

The `pwd` command displays the absolute path of the current working directory.

**Q4. Why is a directory-listing operation useful?**

The `ls` command helps identify available files and folders, navigate directories, and verify that file operations were successful.

### Learning Outcome

I learned the difference between overwriting and appending file contents and how to create backup copies safely.

---

## Task 2.3 — Understand Flags and Pipes

### Activity 1: Compare Directory Listings

Commands used:

```bash
ls
ls -l
ls -lah
```

### Observations

| Command | Observation |
|---|---|
| `ls` | Displayed notes.txt and notes-backup.txt. |
| `ls -l` | Displayed permissions, ownership, file sizes, and modification dates. |
| `ls -lah` | Included hidden directory entries and displayed human-readable sizes such as 63B and 128B. |

### Understanding Flags

- `-l` provides detailed listing information.
- `-a` includes hidden files and directory entries.
- `-h` displays file sizes in a human-readable format when used with `-l`.

A flag modifies how a command behaves.

### Activity 2: Understand Pipes

Command used:

```bash
ls -lah | head -n 3
```

### Observation

The command displayed only three lines:

1. The total block count.
2. The current directory entry (`.`).
3. The parent directory entry (`..`).

### Explanation

A pipe (`|`) sends the output of one command as input to another command.

In my example, `ls -lah` generated a detailed directory listing, while `head -n 3` displayed only its first three lines.

### Learning Outcome

I learned how command options change output and how pipes combine commands to filter information.

---

## Task 2.4 — Understand Package Managers

### Package Manager: Homebrew

I checked whether Homebrew was installed on my MacBook.

Command:

```bash
brew --version
```

Observed output:

```text
Homebrew 7.0.13
```

### Inspecting Installed Packages

Command used:

```bash
brew list
```

Homebrew displayed two categories of installed packages.

**Formulae examples:**

- node
- python@3.11
- ffmpeg
- gh
- go
- ripgrep

**Cask examples:**

- docker-desktop
- miniforge
- utm
- vagrant
- copilot-cli

### Why Are Package Managers Useful?

A package manager helps users install, update, and remove software using simple commands.

Homebrew manages software packages and their dependencies on macOS, reducing the need for manual downloads and configuration.

Package managers also make it easier to maintain and update installed software.

### Observation

Homebrew was already installed and managing multiple command-line tools and applications. No new packages were installed or removed during this activity.

---

## Tools Used

- macOS Terminal
- zsh shell
- Visual Studio Code
- Homebrew 7.0.13
- Git and GitHub

## Difficulties Faced

No significant difficulties were encountered while performing the Mission 2 Terminal activities.

## What I Learned

Through this mission, I learned:

1. How to navigate the filesystem using Terminal commands.
2. How to create, copy, move, and inspect files.
3. How to overwrite and append text safely.
4. How flags modify command behaviour.
5. How pipes connect the output and input of commands.
6. How Homebrew manages software packages.

## Conclusion

Mission 2 helped me become more comfortable with the command-line interface. I gained practical experience managing files, understanding command options, using pipes, and exploring software management on macOS.
