# 🐚 Bash Advanced Guide

This guide is a comprehensive reference to using advanced Bash commands and tools like `grep`, `sed`, and `awk`, along with basic and advanced shell operations.

---

## 🔧 Shell / CLI Basics

- A **shell** is a command-line interface (CLI) that interprets user commands to the operating system.
- Example command: `ls` (list directory contents)

---

## 📁 `ls` Command Variants

| Command       | Description |
|---------------|-------------|
| `ls -l`       | Long format listing (permissions, size, timestamp, etc.) |
| `ls -R`       | Recursively lists subdirectories |
| `ls -t`       | Sorts by timestamp |
| `ls -lt`      | Combines long listing and timestamp sort |
| `ls -la`      | Lists all files, including hidden ones |
| `ls -lr`      | Reverse order |
| `ls -s`       | Displays file sizes |
| `ls -lR \| grep .` | Grep through recursive listing |
| `ls *.`       | Wildcard usage |
| `ls ..`       | Contents of parent directory |

---

## 📄 File Operations

### `cat` - Concatenate

| Command         | Function |
|-----------------|----------|
| `cat > file`    | Create or overwrite a file |
| `cat >> file`   | Append data to a file |

### Combine Commands

```bash
command1 && command2 && command3
````

---

## 📂 Directory & File Management

| Command               | Description                |
| --------------------- | -------------------------- |
| `mkdir -p dir/newdir` | Create nested directories  |
| `mv old new`          | Rename file                |
| `mv file /dest`       | Move file                  |
| `cp file /dest`       | Copy file                  |
| `cp -r dir /dest`     | Copy directory recursively |
| `rm file`             | Delete file                |
| `rm -r folder`        | Delete folder              |

---

## 🔐 File Permissions

| Symbol | Meaning     |
| ------ | ----------- |
| u      | user        |
| g      | group       |
| o      | other       |
| r      | read (4)    |
| w      | write (2)   |
| x      | execute (1) |

### Symbolic

```bash
chmod ugo-r file
chmod -R ugo-r folder
```

### Numeric

```bash
chmod 664 filename
```

---

## 💬 Output & Viewing

| Command                             | Function                   |
| ----------------------------------- | -------------------------- |
| `echo 'text'`                       | Prints message or variable |
| `head filename`                     | View top lines             |
| `tail filename`                     | View bottom lines          |
| `head -20 filename`                 | First 20 lines             |
| `tail -n 30 filename \| head -n 10` | View specific section      |

---

## 🔀 Pipes & Word Count

| Command                | Function                        |
| ---------------------- | ------------------------------- |
| `command1 \| command2` | Pipe output of one into another |
| `wc filename`          | Line, word, char count          |

---

## 🔍 `grep` (Global Regular Expression Print)

| Command                | Function                |
| ---------------------- | ----------------------- |
| `grep 'word' file`     | Search for a word       |
| `grep -c 'word' file`  | Count matches           |
| `grep -h 'word' file`  | Hide filename in output |
| `grep -hi 'word' file` | Case-insensitive search |
| `grep -hir 'word'`     | Recursive search        |
| `grep -w 'word' file`  | Match whole words only  |
| `grep -o 'word' file`  | Only show matched word  |

---

## ⌛ History & Scripts

* `history 0` – Show previous commands
* `#!/bin/bash` – Shebang to define the interpreter at the start of a script

---

## 🌐 Node.js Installation

### For macOS (using Homebrew)

```bash
brew install node
node -v
```

### For Unix (using nvm)

```bash
nvm install node
```

### For Windows

Download from [https://nodejs.org](https://nodejs.org) and install.

---

## 🔍 Advanced Command Tools

### `grep` Advanced

| Flag   | Description                   |
| ------ | ----------------------------- |
| `-P`   | Perl-style regex              |
| `-v`   | Invert match                  |
| `-A n` | Show n lines **after** match  |
| `-B n` | Show n lines **before** match |
| `-C n` | Show n lines **around** match |

---

### `sed` (Stream Editor)

| Command                         | Description                    |
| ------------------------------- | ------------------------------ |
| `sed 's/pattern/replacement/g'` | Global replace                 |
| `sed -n '5,10p'`                | Show lines 5–10                |
| `sed '/pattern/d'`              | Delete matching lines          |
| `sed 'G'`                       | Add blank line after each line |
| `sed '1i\header'`               | Insert at start                |

---

### `awk` (Pattern Scanning & Processing)

| Command                             | Description                  |
| ----------------------------------- | ---------------------------- |
| `awk '{print $1, $NF}'`             | Print first and last columns |
| `awk -F ':' '{print $1}'`           | Use colon as field separator |
| `awk '{sum += $1} END {print sum}'` | Sum first column             |
| `awk 'NR % 2 == 0'`                 | Print even-numbered lines    |
| `awk 'length > 80'`                 | Print long lines             |














