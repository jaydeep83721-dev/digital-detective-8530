# Mission 3 — Understand the Operating System

## Objective

The objective of this mission is to explore the operating system, examine running processes, understand storage and filesystem paths, inspect file permissions, and learn about the responsibilities of an operating system.

All practical activities were performed using macOS Terminal.

---

## Task 3.1 — Explore Your Operating System

In this task, I used Terminal commands to inspect my operating system, current user account, available storage, and running system activity.

### Commands Used

```bash
sw_vers
uname -m
whoami
id
df -h /
top -l 1 -n 5 -stats pid,command,cpu,mem
```

### Observations

| Information Explored | What It Tells Me | My Observation (Privacy-Safe) |
|---|---|---|
| Operating system / system details | Identifies the installed OS, version, and processor architecture. | macOS 26.6.2, build 25G83, ARM64 architecture. |
| Current account identity | Identifies the active user, UID, and group memberships. | Local user detected with UID 501, primary group `staff`, and membership in `admin`. Username omitted. |
| Available and used storage | Shows filesystem capacity, used space, and available storage. | Root filesystem reported 460 GiB capacity, 12 GiB used, and 115 GiB available. |
| System activity snapshot | Displays running processes, CPU usage, and memory information. | 554 processes, 3 running, 551 sleeping, and 76.50% CPU idle. |

### Operating System Information

The `sw_vers` command reported:

- Product Name: macOS
- Product Version: 26.6.2
- Build Version: 25G83

The `uname -m` command returned `arm64`, indicating that the computer uses an ARM64 processor architecture.

### Storage Observation

I used the following command:

```bash
df -h /
```

The root filesystem reported:

- Size: 460 GiB
- Used: 12 GiB
- Available: 115 GiB
- Capacity: 10%

macOS uses APFS volumes that may share storage space. Therefore, the root filesystem's reported usage does not necessarily represent the total storage consumed by all volumes.

### System Activity Observation

The `top` command produced a snapshot showing:

- Total processes: 554
- Running processes: 3
- Sleeping processes: 551
- CPU user usage: 8.82%
- CPU system usage: 14.67%
- CPU idle: 76.50%
- Physical memory: 15 GiB used, 91 MiB unused

I also observed processes belonging to applications such as Visual Studio Code, Google Chrome, and Microsoft Word.

### What I Learned

I learned that the operating system manages multiple processes simultaneously and provides tools for monitoring CPU usage, memory usage, storage, and user accounts.

---

## Task 3.2 — Understand Processes

A process is a program that is currently executing. The operating system assigns resources such as CPU time and memory to processes.

### Commands Used

```bash
ps -ax -o pid,comm | head -n 15
ps -ax -o pid,comm | grep -i '[C]ode'
```

### Observations

The first command displayed running system processes and their process identifiers.

Examples from my Terminal output:

| PID | Process | Purpose |
|---|---|---|
| 1 | launchd | Starts and manages system services. |
| 340 | logd | Handles system logging. |
| 344 | fseventsd | Monitors filesystem changes. |
| 354 | powerd | Manages power-related functions. |

The second command searched for processes with names or executable paths containing `Code`.

Examples observed:

| PID | Process |
|---|---|
| 15676 | Visual Studio Code |
| 3264 | Code Helper (Renderer) |
| 6624 | Code Helper |
| 6626 | Code Helper (Plugin) |

I noticed that Visual Studio Code uses multiple processes for different application functions.

The search also matched some unrelated executable paths containing the letters `code`.

### Questions and Answers

**Q1. What is a process?**

A process is a running instance of a program. It uses system resources such as CPU time and memory to perform its operations.

**Q2. What does the PID column represent?**

PID stands for Process ID. It is a numeric identifier assigned by the operating system to distinguish one running process from another. A process's PID may change when the application is restarted.

**Q3. Give two examples of processes that may be running on your computer.**

1. **launchd:** A macOS system process responsible for starting and managing system services.
2. **Code Helper:** A process used by Visual Studio Code to perform application-related tasks.

### What I Learned

I learned that an application may use several processes and that the operating system assigns each process an identifier to help manage and monitor it.

---

## Task 3.3 — Understand Paths and Permissions

### Part A — Understanding Paths

I navigated between my assignment repository and the Mission 3 folder using Terminal commands.

### Commands Used

```bash
pwd
cd mission-03-operating-system
pwd
cd ..
pwd
```

### Observations

Initially, `pwd` displayed the path to my Digital Detective repository.

After executing `cd mission-03-operating-system`, the current working directory changed to the Mission 3 subfolder.

Executing `cd ..` returned me to the parent directory.

### Absolute Path

An absolute path specifies the complete location of a file or directory, starting from the filesystem root.

Example:

```text
/Users/[redacted]/Documents/digital-detective-8530/mission-03-operating-system
```

### Relative Path

A relative path specifies a location based on the current working directory.

Example, from the repository root:

```text
mission-03-operating-system
```

### Difference

An absolute path identifies a location independently of the current working directory.

A relative path depends on the directory from which it is interpreted.

### Part B — Understanding File Permissions

I navigated into the Mission 3 directory and inspected the README file.

Command:

```bash
ls -l README.md
```

### Observed Permission String

```text
-rw-r--r--@
```

### Permission Table

| Permission | Meaning | Example |
|---|---|---|
| `r` — Read | Allows a file's contents to be read. | Opening a text file. |
| `w` — Write | Allows a file to be modified. | Editing README.md. |
| `x` — Execute | Allows a file to be executed, subject to other system requirements. | Running an executable script. |

### Explanation of File Permissions

The permission string `-rw-r--r--@` indicates:

- The file owner has read and write permissions.
- The owning group has read permission.
- Other users have read permission.
- No execute permission is granted by these permission bits.
- The `@` indicates that macOS extended attributes are present.

The README file had a size of 0 bytes when its permissions were inspected.

### Observation

I confirmed that the owner could read and write the file but did not have execute permission.

No file or system permissions were changed during this activity.

### What I Learned

I learned how absolute and relative paths work and how filesystem permissions control access to files.

---

## Task 3.4 — Explain Operating-System Responsibilities

An operating system manages hardware resources, provides services to applications, and allows users to interact with their computer.

### Operating-System Responsibilities

| OS Responsibility | My Explanation | Example |
|---|---|---|
| Process management | Manages running programs and allocates CPU time to processes. | macOS manages Visual Studio Code and Chrome processes. |
| Memory management | Allocates memory to running applications and manages memory usage. | macOS provides memory for VS Code. |
| Device management | Coordinates communication between hardware devices and software. | Processing keyboard input. |
| File management | Organises files and directories and manages file operations. | Creating, opening, and saving README.md files. |
| User interface / shell | Provides ways for users to interact with the computer through graphical interfaces or commands. | Finder and the zsh Terminal. |
| Security and permissions | Controls access to files, applications, and system resources. | File permissions such as `rw-r--r--`. |

### Explanation

The operating system acts as an interface between hardware, applications, and users.

It manages CPU time, allocates memory, coordinates input and output devices, and organises files.

It also provides user interfaces and enforces permissions to help protect system resources.

### What I Learned

I learned that operating systems perform several responsibilities simultaneously to keep applications and hardware working together.

---

## Tools and Commands Used

| Tool / Command | Purpose |
|---|---|
| macOS Terminal | Perform command-line operations. |
| `sw_vers` | Display macOS version information. |
| `uname -m` | Identify machine architecture. |
| `whoami` | Identify the active user account. |
| `id` | Display user and group identifiers. |
| `df -h /` | Inspect root filesystem storage information. |
| `top` | Observe CPU, memory, and process activity. |
| `ps` | List running processes and PIDs. |
| `grep` | Search process information. |
| `head` | Limit displayed output. |
| `pwd` | Display the current working directory. |
| `cd` | Navigate between directories. |
| `ls -l` | Inspect file details and permissions. |

## Difficulties Faced

No significant difficulties were encountered while performing the Mission 3 activities.

I also took care to avoid publishing personal usernames, device names, and other identifying information in the documentation.

## Overall Learning Outcomes

Through Mission 3, I learned:

1. How to identify my operating system and processor architecture.
2. How to inspect active user information and group memberships.
3. How to observe filesystem storage usage.
4. How to monitor running processes, CPU usage, and memory usage.
5. How to identify processes using their PIDs.
6. The difference between absolute and relative paths.
7. How read, write, and execute permissions work.
8. The major responsibilities performed by an operating system.

## Conclusion

Mission 3 helped me understand how an operating system manages computer resources, processes, files, memory, hardware devices, and security.

By performing practical Terminal activities on macOS, I gained a clearer understanding of how operating-system concepts work in real situations.
